# dsh-macos-intel

A build mirror of [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness).

A scheduled workflow replaces this tree with upstream's snapshot and builds the macOS
Intel (x86_64) desktop application, then publishes it as a GitHub Release and announces
the result in Feishu.

- Upstream: https://github.com/deepseek-ai/deepseek-harness (MIT)
- This repository is **not a fork**, because GitHub disables scheduled workflows in
  forks ("When a public repository is forked, scheduled workflows are disabled by
  default").
- The tree is upstream's files plus `.github/workflows/build-macos-intel.yml`.
  Upstream's own `.github` directory is deliberately excluded, so its workflows and
  Dependabot configuration never run here.
- Releases are ad-hoc signed and not notarized. After downloading, run
  `xattr -dr com.apple.quarantine "/Applications/DeepSeek Harness.app"`.
