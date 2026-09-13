# Private Distributor Notification Email Template

Use this email template when selected private distributors receive advance notification of a pending security release.

To: `<private distributor recipients>`

Subject: `[EMBARGOED] Volcano security notification: <CVE or advisory ID>`

This message is embargoed until `<public disclosure date and time, including timezone>`.

The Volcano Security Team is preparing a security release for `<affected component>`.

## Summary

- CVE or advisory ID: `<CVE-YYYY-NNNN or advisory ID>`
- Severity: `<critical/high/medium/low>`
- Affected versions: `<affected versions>`
- Planned fixed versions: `<planned fixed versions>`
- Planned public disclosure: `<date and time>`
- Impact: `<brief user-facing impact>`

## Mitigation

`<Describe mitigation steps if users cannot upgrade immediately. If no mitigation is available, state that upgrading is expected to be the mitigation.>`

## Fix Information

- Patch or pull request: `<link if available>`
- Release candidate or artifact: `<link if available>`
- Testing requested: `<what feedback is requested, if any>`

## Embargo Handling

Please share this information only with people in your organization who need it to prepare a fix or update. Do not disclose, hint at, or discuss this issue publicly before the public disclosure time without explicit approval from the Volcano Security Team.

If this information is accidentally disclosed, contact [volcano-security@googlegroups.com](mailto:volcano-security@googlegroups.com) as soon as possible with details about what was disclosed and to whom.

## References

- Private distributor notifications policy: https://github.com/volcano-sh/community/blob/master/security-team/private-distributors-list.md
- Security release process: https://github.com/volcano-sh/community/blob/master/security-team/security-release-process.md

Regards,

`<name>` on behalf of the Volcano Security Team
