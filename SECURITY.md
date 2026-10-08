# Security policy

This policy applies to every public repository of the Gua project that has no security policy of its own. Gua is a prototype in an invite-only beta. Please report problems privately and give the maintainers time to fix them before you publish anything.

## Report a vulnerability

Where a repository shows **Report a vulnerability** under its Security tab, use it. The report is visible only to the maintainers. Repositories without that button are covered by the email route below.

If you cannot use GitHub, email [support@gua.global](mailto:support@gua.global) with "Security" in the subject. The mailbox is not encrypted, so keep the first message to a short description and the maintainers will take the details from there.

Do not open a public issue for a security problem.

Include what you found, how to reproduce it, the version or commit you tested, and what an attacker could do with it.

## What to expect

- An acknowledgement once a maintainer has read the report.
- Questions if the report needs them, and a note when the fix is released.
- There is no bug bounty.

## Upstream code

The Gua clients and the authentication service are forks of Element projects. A vulnerability in inherited upstream code should also be reported to Element under their [security disclosure policy](https://element.io/security/security-disclosure-policy), so that every fork receives the fix. Problems in the Matrix protocol or the Matrix SDKs go to the [Matrix.org Foundation](https://matrix.org/security-disclosure-policy/).
