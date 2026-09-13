# Access Control

This document describes the access control rules used by the Volcano project to protect project repositories, release-related assets, and security response work. These rules apply to normal project operations and security response work.

## GitHub Organization Access

Access to Volcano GitHub repositories is granted according to the community roles documented in [community-membership.md](../community-membership.md).

Privileged access is granted only when it is required for the contributor's current project responsibilities. Access should be scoped to the relevant repository, package, or communication channel instead of granted broadly across the organization.

Accounts with write, maintain, administration, package publishing, or security response access must have two-factor authentication enabled.

## Repository Permissions

Repository permissions follow least privilege. Contributors should receive the minimum access required to perform their current role, and elevated access should be limited to the repositories or packages where it is needed.

Changes to privileged access follow the membership and maintainer processes documented by the community. Access should be removed or reduced when a contributor changes role, steps down, or no longer needs the access.

## Branch Protection and Merge Control

Normal code and documentation changes are submitted through GitHub pull requests. Direct pushes to protected branches should be restricted to project maintenance cases where a pull request is not practical.

Important branches should be protected by GitHub branch protection rules or rulesets. The required controls may vary by repository, but protected branches should require review and successful project checks before merge.

Contributions are subject to DCO verification. Project checks, including tests, linting, image or manifest checks, and security scans, may be required according to the configuration of each repository.

Repository administrators and maintainers should avoid bypassing branch protection except for exceptional project maintenance needs. When bypass is used, the change should still be visible in the repository history and follow normal project review where practical.

## Account and Credential Controls

Privileged GitHub accounts must use two-factor authentication. Access tokens, deploy keys, automation credentials, and package publishing credentials should be limited to the access required for their purpose.

Credentials used for automation or release work should be rotated or revoked when they are no longer needed, when ownership changes, or when there is reason to believe they may have been exposed.

## Security Response Access

Private vulnerability reports are handled through the Volcano security mailing list and are shared only with the Security Team and contributors required to investigate, fix, or release the issue.

Embargoed vulnerability information is handled on a need-to-know basis:

- Security reports are discussed in private channels until public disclosure.
- Fix teams are limited to the maintainers and contributors needed to develop and review the remediation.
- Private distributors must follow the embargo policy documented in [private-distributors-list.md](private-distributors-list.md).
- Any unintended disclosure of embargoed information must be reported to the Security Team immediately.

## Access Changes

Repository and security response access should be updated when contributors change roles, step down, or no longer need the access required for their previous responsibilities.

Security Team membership is maintained in [security-groups.md](security-groups.md#the-security-team). Private distributor notification membership is maintained according to [private-distributors-list.md](private-distributors-list.md).
