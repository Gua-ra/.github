# Contributing to Gua

Gua is a prototype in an invite-only beta. Bug reports from testers and small, focused pull requests are welcome. `rust-opa-wasm` takes changes upstream, at [matrix-org/rust-opa-wasm](https://github.com/matrix-org/rust-opa-wasm). A repository's own `CONTRIBUTING.md`, where it has one, adds the setup and checks for that codebase.

## Reporting problems

- Security problems: follow the [security policy](SECURITY.md). Never a public issue.
- Bugs and requests: open an issue in the repository that owns the code, where issues are enabled (`gua-ios`, `gua-android`, `identity-service`, `gua-resolver`, `gua-branding`). For the web client and the authentication service, use the [support form](https://gua.global/support) or [support@gua.global](mailto:support@gua.global).

## Pull requests

- Branch from the repository's default branch (`develop` for the iOS and Android clients, `gua/main` for the web client, `main` elsewhere) and open the pull request against the `Gua-ra` repository, never against an upstream Element repository.
- One concern per pull request. Small is better.
- Commit subjects are conventional and short (`feat:`, `fix:`, `docs:`, `ci:`). A body is only for a constraint the diff cannot show. No AI attribution in commits or pull request text.
- The pull request body has `Summary`, `Changes` and `Validation`, plus `Rollout` when it is not obvious. Validation says what was observed working.
- Comments state the current invariant. No history, no narration.
- No personal names, hostnames or addresses in code, commits or pull request text. Public repositories describe infrastructure generically.
- Writing is plain and short. No em dashes.

## Licenses

There is no contributor license agreement. `identity-service`, `gua-resolver` and `gua-branding` have no license yet, so open an issue before sending code there. Each Element fork's `CONTRIBUTING.md` gives its copyright header rule.
