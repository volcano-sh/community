## Private Distributor Notifications

Private distributor notifications provide advance, actionable information to selected Volcano distributors when early coordination is needed for a security release. This process is not intended for general security announcements or individual notification requests.

The Volcano project does not publish a private distributor recipient list. The Security Team maintains the recipient information privately and uses it only for coordinated security disclosure.

Advance notifications may use the [private distributor notification email template](./comms-templates/private-distributor-notification-email.md).

### Embargo Policy

Recipients of private distributor notifications must share the information only within their teams, on a need-to-know basis, to get the related issue fixed in their distribution. The information must not be made public, shared, nor even hinted at otherwise, except with the Security Team's explicit approval. This holds true until the public disclosure date and time agreed by the Security Team.

Before any information is shared with respective members of your team required to fix an issue, they must agree to the same terms and only find out information on a need-to-know basis.

In the unfortunate event you share the information beyond what is allowed by this policy, you *must* urgently inform [the Security Team](mailto:volcano-security@googlegroups.com) of exactly what information leaked and to whom, as well as the steps that will be taken to prevent future leaks.

Repeated offenses may lead to removal from private distributor notifications.

### Contributing Back

This is a cooperative process. Private distributors are expected to review or test proposed patches when asked, point out potential issues such as incomplete fixes or newly introduced bugs, and report useful feedback to the Security Team.

### Membership

Membership is managed by the Security Team. Requests are reviewed against the criteria below. Accepted contacts are recorded privately by the Security Team rather than published in this repository.

### Membership Criteria

Private distributor notifications are for distributors that need to prepare fixes or notices for their users before a vulnerability is publicly disclosed. If Volcano is used only inside one organization, that organization can follow the public advisory and fixed release instead of joining this list.

To be eligible for private distributor notifications, your distribution should:

1. Have an actively monitored security email alias for Volcano security notifications.
2. Serve users outside your own organization, such as users of a Volcano distribution, product, or hosted service.
3. Show a public track record of fixing security issues, such as advisories, CVE fixes, or release notes.
4. Be independently maintained and not only a rebuild of another distribution.
5. Show participation in the Volcano community, such as issues, pull requests, testing, release communication, or community discussion.
6. Accept the Embargo Policy that is outlined above.
7. Be willing to contribute back, such as by reviewing fixes, testing patches, or helping with release communication.
8. Be vouched for by an existing trusted Volcano community participant when requested by the Security Team.

**Removal**: If your distribution stops meeting one or more of these criteria after joining, it may be removed from private distributor notifications.

### Request to Join

Send a request to [volcano-security@googlegroups.com](mailto:volcano-security@googlegroups.com), filling in the criteria template in [the request email template](./comms-templates/private-distributor-notification-request.md).
