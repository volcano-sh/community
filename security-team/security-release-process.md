# Security Release Process

Volcano has always attached great importance to vulnerability management in development and maintenance. The Volcano community has adopted this security disclosures and response policy to ensure we responsibly handle critical issues.

<!-- toc -->

- [The Security Team](#the-security-team)
    - [The Security Team Membership](#the-security-team-membership)
        - [Joining](#joining)
        - [Stepping Down](#stepping-down)
        - [Responsibilities](#responsibilities)
            - [Associate](#associate)
- [Process an undisclosed vulnerability](#process-an-undisclosed-vulnerability)
- [Process a publicly disclosed vulnerability](#process-a-publicly-disclosed-vulnerability)
- [Vulnerability handling process](#vulnerability-handling-process)
- [Patch, Release, and Public Communication](#patch-release-and-public-communication)
    - [Fix Development Process](#fix-development-process)
    - [Fix Disclosure Process](#fix-disclosure-process)
- [Private Distributor Notifications](#private-distributor-notifications)
  <!-- /toc -->

## The Security Team

Security is of the highest importance and security vulnerabilities should be handled quickly and sometimes privately.

The Security Team is responsible for organizing the entire response, including internal communication and external disclosure, but will need help from relevant developers and release managers to successfully run this process. Security Team membership is managed in [security-groups.md](security-groups.md#the-security-team).

### The Security Team Membership

#### Joining

New potential members to the Security Team will first fill a minimum 3 month rotation in the [Associate](#associate) role. These individuals will be nominated by maintainers or current Security Team members.

#### Stepping Down

Members may step down at any time.

#### Responsibilities

- Members should remain active and responsive.
- Longer leaves of absence should be discussed on a case-by-case basis, and may include an associate temporarily onboarding.
- Members of a role should remove any other members that have not communicated a leave of absence and either cannot be reached for more than 2 months or are not fulfilling their documented responsibilities for more than 2 months. This may be done through a super-majority vote of members.

##### Associate

A role for those wishing to join the Security Team.

Their rotation will involve the following:

- Lead disclosures that are publicly disclosed or explicitly designated as low sensitivity, often because of reporter request, a low CVSS score, or a design issue that requires long-term refactoring.
- Assist in process improvements, bug bounty administration, audits, or other non-disclosure activities.

## Process an undisclosed vulnerability

The Volcano Community asks that all suspected vulnerabilities be privately and responsibly disclosed through the [vulnerability reporting process](SECURITY.md#report-a-vulnerability).

If the vulnerability is accepted, the Security Team will determine its remediation priority and develop remediations, including mitigations, patches, fixed versions, and other risk-reduction steps, by following the [vulnerability handling process](#vulnerability-handling-process).

## Process a publicly disclosed vulnerability

If you know of a publicly disclosed security vulnerability please IMMEDIATELY email [volcano-security@googlegroups.com](mailto:volcano-security@googlegroups.com) to inform the Security Team about the vulnerability so they may start the patch, release, and communication process.

If possible the Security Team will ask the person making the public report if the issue can be handled via a private disclosure process. If the reporter denies the request, the Security Team will move swiftly with the fix and release process.

## Vulnerability handling process

The following flowchart shows the vulnerability handling process. Reported vulnerabilities are handled according to this procedure.

![Vulnerability handling process](./images/vulnerability-handling-process.svg)

## Patch, Release, and Public Communication

All of the timelines below are suggestions and assume a Private Disclosure.

The Security Team drives the schedule using their best judgment based on severity, development time, and release manager feedback. If the fix relies on another upstream project's disclosure timeline, that will adjust the process as well. The Security Team will work with the upstream project to fit their timeline and best protect
our users.

The following is a timeline of a vulnerability process.

<img src="./images/vulnerability-process-timeline.PNG">

### Fix Development Process

This part should be completed within 1-7 days of disclosure.

After receiving any suspected vulnerability, the Security Team will discuss the issue with the reporter(s) and Volcano's security advisors to analyze/validate the vulnerability, assess its severity based on its actual impact on Volcano.

If the vulnerability is accepted, the Security Team will determine its remediation priority and develop remediations, including mitigations, patches, fixed versions, and other risk-reduction steps.

The Security Team will start the CVE process to obtain a CVSS score and CVE ID when applicable. The CVSS v3 standard adopted by the Volcano community assesses the impact of a vulnerability.

If the CVSS score is under ~4.0 ([a low severity score](https://www.first.org/cvss/specification-document#i5)) or the assessed risk is low the Security Team can decide to slow the release process down in the face of holidays, developer bandwidth, etc.

If the CVSS score is under ~7.0 (a medium severity score), the Security Team may choose to carry out the fix semi-publicly. This means that PRs are made directly in the public volcano-sh/volcano repo, while restricting discussion of the security aspects to private channels. The Security Team will make the determination whether there would be user harm in handling the fix publicly that outweighs the benefits of open engagement with the community.

Critical and High severity vulnerability fixes will typically receive an out-of-band release. Medium and Low severity vulnerability fixes will be released as part of the next Volcano [patch release](https://github.com/volcano-sh/volcano/releases).

Note: CVSS is convenient but imperfect. Ultimately, the Security Team has discretion on classifying the severity of a vulnerability.

### Fix Disclosure Process

With fix development underway, the Security Team needs to create an overall communication plan for the wider community. This disclosure process should begin after the Security Team has developed a fix or mitigation so that a realistic timeline can be communicated to users. Emergency releases for critical and high severity issues or fixes for issues already made public may affect the timelines below.

**Advance Vulnerability Disclosure to Private Distributors**

- Private distributors may receive advance notification of vulnerabilities that are assigned a CVE when early coordination is needed. The notification will include information that can be reasonably provided at the time, such as patches or links to PRs, proofs of concept or reproduction instructions, known mitigations, and timelines for public disclosure. Distributors should read about [private distributor notifications](#private-distributor-notifications) to find out the requirements for being included in this process.
- **What if a vendor breaks embargo?** The Security Team will assess the damage and will make the call to release earlier or continue with the plan. When in doubt push forward and go public ASAP.

**Fix Release Day**

Release process:
- The Security Team will cherry-pick the patches onto the master branch and all relevant release branches.
- The Release Managers will merge these PRs as quickly as possible. Changes shouldn't be made to the commits at this point, to prevent potential conflicts with the patches sent to distributors, and conflicts as the fix is cherry-picked around branches.
- The Release Managers will ensure all the binaries are built, publicly available, and functional.

Communications process:
- Private distributors may be notified in advance of a pending release containing security vulnerability fixes with the public messaging, date, and time of the announcement.
- The Security Team will announce the new releases, the CVE number, severity, and impact, and the
  location of the binaries to get wide distribution and user action. As much as possible this
  announcement should be actionable, and include any mitigating steps users can take prior to
  upgrading to a fixed version. The announcement will be sent via the following channels:
    - General announcement email ([template](./comms-templates/vulnerability-announcement-email.md)) to Volcano communication channels
    - Tracking issue opened in https://github.com/volcano-sh/volcano/issues ([template](./comms-templates/vulnerability-announcement-issue.md)) and prefixed with the associated CVE ID (if applicable)
    - [GitHub Security Advisories](https://github.com/volcano-sh/volcano/security/advisories) of Volcano
    - [Patch release](https://github.com/volcano-sh/volcano/releases), will have the fix details included in the patch release notes. Any public announcement sent for these fixes will link to the release notes.

## Private Distributor Notifications

This process is used to provide actionable information to selected distribution vendors when advance coordination is needed.

See the [private distributor notifications doc](private-distributors-list.md) for more information.
