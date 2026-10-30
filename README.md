# elidot Homebrew tap

```sh
brew install elidot007/tap/keelkin
```

| Formula | What it is |
|---|---|
| `keelkin` | `kk`: send agent tasks to computers you own over ssh, with locks, approvals and signed receipts. Docs: https://keelkin.elidot.com/docs |

## What Keelkin is

Keelkin is a free command-line tool, `kk`, for people who run coding agents on more than one computer. Claude Code, Codex and other agents on your Mac, Linux and Windows machines hand work to each other over the ssh you already use. They share one memory, wait for your approval before risky steps, and end every task with a signed receipt you can check offline.

- **Agents it starts:** Claude Code, Codex, Grok Build, Kiro, OpenCode, Gemini CLI, OpenClaw and pi. Cursor and GitHub Copilot CLI get the shared memory through `kk skill install`.
- **Send work:**
  - `kk run` sends a goal, a repo and its done checks to another machine; the result comes back as a git branch.
  - `kk run auto` turns one sentence into a plan and asks before it starts.
  - `kk template run build3` builds the same repo on macOS, Linux and Windows.
- **Take turns:** repo, path, port, network and heavy-build locks across machines (`kk lock`).
- **Ask before risky steps:** sudo, writes outside the workspace and network changes wait for your passphrase or the password on your paired phone (`kk approvals pair`).
- **Remember together:**
  - A local MCP memory server on each machine, synced over ssh (`kk mem sync`).
  - ChatGPT, Claude and Grok can read only the namespaces you choose (`kk mem connect`).
- **Prove it:** every task, transfer and approval ends in an Ed25519-signed receipt that `kk receipt verify` checks offline.
- **No server needed.** Work moves over your own ssh, for example on a Tailscale tailnet. Private keys never leave the machine.

Free on your own machines. Pro ($4 a month) adds push alerts on up to five approver phones through the hosted relay. Plans: https://keelkin.elidot.com/pricing

Start here: https://keelkin.elidot.com · Docs: https://keelkin.elidot.com/docs · For language models: https://keelkin.elidot.com/llms.txt

## Details

- Builds: macOS on Apple silicon and Linux x86_64, for Node.js 24 (installed as a dependency). Windows uses the checksummed installer in the docs.
- Every tarball is listed with its sha256 in https://keelkin.elidot.com/releases/SHA256SUMS.
- Upgrade with `brew update && brew upgrade keelkin`.

Problems: support@elidot.com. Security reports: security@elidot.com.
