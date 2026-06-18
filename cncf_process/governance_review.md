# Volcano Governance Review

What follows is a governance review and assessment for the Volcano project. The review was prepared as part of Volcano's application to move from Incubating to Graduated maturity in the CNCF. Completed assessments are submitted as PRs to the TOC repo to be placed in the project's dedicated directory.

## Summary and Assessment

**Status:** Satisfactory

### Executing the Assessment

This review primarily consists of an audit of Volcano's governance self-assessment in its Graduation application, along with review of the public governance, community, maintainer, security, and contribution documents in the [volcano-sh/community](https://github.com/volcano-sh/community) repository.

The project's self-assessment is available at [volcano-graduation-application.md](../volcano-graduation-application.md).

### Must-Fix Items

**The following issues have been identified that need to be resolved before [project milestone or other requirement]:**

No blocking governance issues were identified for Graduation. Volcano has public governance documentation, a contributor ladder, a maintainer list spanning multiple organizations, public contribution and communication channels, and a documented subproject process.

### Points of Excellence

**The following aspects of governance are exemplary, and can be referenced as examples for other projects to copy:**

- Volcano documents a clear contributor ladder from Member to Reviewer, Approver, and Maintainer, including requirements, responsibilities, and privileges for each role.
- Governance and decision making are public by default: proposals, maintainer changes, CNCF requests, and subproject acceptance are expected to happen through GitHub issues or pull requests.
- The maintainer body demonstrates vendor-neutrality and survivability, with active maintainers from NVIDIA, Huawei, Baidu, and Hjmicro.
- The community has expanded its meeting schedule across Asia, Europe, and Pacific time zones, which improves accessibility for a global contributor base.


### Areas for Improvement

**Over the next year, the project should work on the following issues to improve its governance, these are considered non-blocking:**

- Consolidate and keep subproject inventory in one canonical location, including each subproject's leadership, maturity/status, contribution path, communication channels, and alignment with Volcano's governance.

---

## Review

**The following review primarily consists of an audit on the project's self-assessment in their Graduation application.**

The project's self-assessment is available at [volcano-graduation-application.md](../volcano-graduation-application.md).

### Governance Summary

Volcano's governance is public, transparent, and generally aligned with CNCF Graduation expectations. The community maintains governance documentation, a contributor ladder, maintainership expectations, decision-making rules, community meeting information, contribution guidance, a Code of Conduct, security response documentation, and a subproject creation process in the public [volcano-sh/community](https://github.com/volcano-sh/community) repository.

The governance model is consensus-driven among maintainers, with proposals and decisions expected to happen through GitHub issues or pull requests. Maintainers represent multiple organizations, and the public maintainer list demonstrates that no single vendor controls the entire project. Contribution acceptance and repository ownership are supported by reviewer and approver roles, [OWNERS](../OWNERS) files, and PR review requirements.

### Governance Evolution

**Governance has continuously been iterated upon by the project as a result of their experience applying it, with the governance history demonstrating evolution of maturity alongside the project's maturity evolution.**
<br>
**Incubating:** Suggested | **Graduated:** Suggested

Volcano has evolved its governance as the project matured from Sandbox to Incubating and now toward Graduation. The project documents governance principles, maintainer expectations, role progression, subproject acceptance, security response, and community operations in the [volcano-sh/community](https://github.com/volcano-sh/community) repository.

Evidence of governance evolution includes:

- A formal community membership ladder in [community-membership.md](../community-membership.md), with Member, Reviewer, Approver, and Maintainer roles.
- Maintainer lifecycle evidence in [MAINTAINERS.md](../MAINTAINERS.md), including current maintainers and emeritus maintainers.
- Security response formalization in [SECURITY.md](../SECURITY.md).
- A documented process for adding projects under the Volcano organization in [GOVERNANCE.md](../GOVERNANCE.md) and [subproject-creation.md](../subproject-creation.md).
- Public meeting expansion across multiple time zones in [README.md](../README.md).

Assessment: Satisfactory. The project has demonstrated continuing governance iteration. The main non-blocking improvement is to ensure all governance documents are kept synchronized as processes evolve.

### Discoverability

**Clear and discoverable project governance documentation.**
<br>
**Incubating:** Suggested | **Graduated:** Required

Volcano's governance documentation is discoverable from the public community repository:

- Governance: [GOVERNANCE.md](../GOVERNANCE.md)
- Community membership: [community-membership.md](../community-membership.md)
- Maintainers: [MAINTAINERS.md](../MAINTAINERS.md)
- Contribution guide: [contribute.md](../contribute.md)
- Code of Conduct: [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md)
- Security policy: [SECURITY.md](../SECURITY.md)
- Subproject creation: [subproject-creation.md](../subproject-creation.md)

Assessment: Satisfactory. The relevant documents are public and discoverable. Link normalization across documents is recommended but not blocking.

### Accuracy and Clarity

**Governance is up to date with actual project activities, including any meetings, elections, leadership, or approval processes.**
<br>
**Incubating:** Suggested | **Graduated:** Required

The governance documents generally reflect current project activities:

- [README.md](../README.md) documents regular community meetings, meeting notes, Zoom link, and calendar subscription.
- [MAINTAINERS.md](../MAINTAINERS.md) lists current and emeritus maintainers.
- [community-membership.md](../community-membership.md) documents role requirements and responsibilities.
- [GOVERNANCE.md](../GOVERNANCE.md) documents consensus-based decision making through GitHub issues and pull requests.
- [subproject-creation.md](../subproject-creation.md) documents a proposal, explanation meeting, maintainer vote, public review, and material submission process for subprojects.

There are minor opportunities to remove stale wording and synchronize some references, such as Code of Conduct link casing and PST affiliation/contact details.

**Governance clearly documents [vendor-neutrality] of project direction.**
<br>
**Incubating:** Suggested | **Graduated:** Required

Volcano's governance principles require decisions and CNCF-related activities to happen publicly. The maintainer list shows active maintainers from NVIDIA, Huawei, Baidu, and Hjmicro. The decision-making model is based on maintainer consensus, with public GitHub issues and pull requests as the record of proposals and decisions. The documented subproject acceptance criteria also require support from a maintainer not associated or affiliated with the subproject author(s), which helps guard against single-vendor control of new subprojects.

Assessment: Satisfactory. Vendor-neutrality is demonstrated through both documentation and maintainer composition.

### Decisions and Role Assignments

**Document how the project makes decisions on leadership roles, contribution acceptance, requests to the CNCF, and changes to governance or project goals.**
<br>
**Incubating:** Suggested | **Graduated:** Required

Volcano documents consensus-based decision making in [GOVERNANCE.md](../GOVERNANCE.md). Proposals, ideas, and decisions are expected to be submitted through GitHub issues or pull requests. If consensus cannot be reached, maintainers may use a formal vote recorded in a GitHub issue or pull request, with one vote per maintainer and a two-third approval threshold.

Leadership role assignment is documented in [community-membership.md](../community-membership.md). Each role has sponsor requirements and eligibility criteria. Contribution acceptance is documented in [contribute.md](../contribute.md), including PR workflow, review expectations, and the requirement for maintainer approval. CNCF-related requests and participation are documented in [GOVERNANCE.md](../GOVERNANCE.md), which requires a public GitHub pull request for calls for participation when Volcano is involved in CNCF activities.

**Document how role, function-based members, or sub-teams are assigned, onboarded, and removed for specific teams (example: Security Response Committee).**
<br>
**Incubating:** Suggested | **Graduated:** Required

Role assignment for the main project is documented through the community membership ladder. Members, Reviewers, Approvers, Maintainers, each have documented requirements, sponsorship rules, responsibilities, and privileges.

Security team and process are documented in [Security Team](../security-team).

Assessment: Satisfactory.

### Maintainers and Maintainer Lifecycle

**Document a complete maintainer lifecycle process (including roles, onboarding, offboarding, and emeritus status).**
<br>
**Incubating:** Suggested | **Graduated:** Required

Volcano documents role progression in [community-membership.md](../community-membership.md), including eligibility requirements for Maintainers and Owners. Maintainers must be sponsored by two owners, have been Approvers for at least two months, be nominated by a project owner, and demonstrate good technical judgment in feature design and development. Owner promotion requires sponsorship from three owners, prior maintainer service, nomination, and no opposition from any project owner.

Offboarding is described in [GOVERNANCE.md](../GOVERNANCE.md): maintainers may step down if they can no longer fulfill maintainer expectations, and the organization will only forcefully remove a maintainer if the maintainer fails to meet Volcano community principles or the Code of Conduct. Emeritus status is documented in [MAINTAINERS.md](../MAINTAINERS.md).

**Demonstrate usage of the maintainer lifecycle with outcomes, either through the addition or replacement of maintainers as project events have required.**
<br>
**Incubating:** Suggested | **Graduated:** Required

Volcano demonstrates lifecycle usage through the current and emeritus maintainer lists. Current maintainers include representatives from multiple organizations, and former maintainers from Facebook, IBM, and Tencent are listed as Emeritus Maintainers. The graduation self-assessment also cites public issues/PRs for maintainer additions and emeritus transitions.

**Document complete list of current maintainers, including names, contact information, domain of responsibility, and affiliation.**
<br>
**Incubating:** Required | **Graduated:** Required

[MAINTAINERS.md](../MAINTAINERS.md) lists the current active maintainers by name, GitHub ID, and affiliation. Maintainers currently include representatives from NVIDIA, Huawei, Baidu, and Hjmicro. The community should consider adding explicit domain-of-responsibility information to the table or linking maintainers to relevant repository/package ownership areas.

**A number of active maintainers which is appropriate to the size and scope of the project.**
<br>
**Incubating:** Required | **Graduated:** Required

Volcano lists eight active maintainers. Given the project scope, including scheduler, controllers, CRDs, integrations, documentation, releases, security response, and subprojects, this is a reasonable maintainer base when combined with documented Reviewer and Approver roles.

**Project maintainers from at least 2 organizations that demonstrates survivability.**
<br>
**Incubating:** N/A | **Graduated:** Required

Volcano satisfies this requirement. Current maintainers represent four organizations: NVIDIA, Huawei, Baidu, and Hjmicro. No single organization holds all maintainer positions.

Assessment: Satisfactory.

### Ownership

**Code and Doc ownership in Github and elsewhere matches documented governance roles.**
<br>
**Incubating:** Required | **Graduated:** Required

Volcano uses [OWNERS](../OWNERS) files and documented Reviewer/Approver/Maintainer roles to align repository ownership with governance roles. [community-membership.md](../community-membership.md) describes Reviewer and Approver permissions for specific packages and repositories, with enforcement through automation/bots. The community repository includes an [OWNERS](../OWNERS) file listing reviewers and approvers.

Assessment: Satisfactory. Ownership is documented and reflected in repository metadata. The project should periodically audit [OWNERS](../OWNERS) files against the maintainer and approver lists.

### Code of Conduct

**Document adoption and adherence to the CNCF Code of Conduct or the project's CoC which is based off the CNCF CoC and not in conflict with it.**
<br>
**Incubating:** Required | **Graduated:** Required

Volcano documents adoption of the CNCF Code of Conduct in [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md), which states that Volcano follows the CNCF Code of Conduct and provides a maintainer contact address for reporting unacceptable behavior.

**CNCF Code of Conduct is cross-linked from other governance documents.**
<br>
**Incubating:** Required | **Graduated:** Required

The Code of Conduct is referenced from [GOVERNANCE.md](../GOVERNANCE.md), [community-membership.md](../community-membership.md), and [contribute.md](../contribute.md). Some links use older or differently cased paths, so the project should normalize these references to [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md).

Assessment: Satisfactory. The project has adopted the CNCF Code of Conduct and cross-links it from governance and contribution documents. Link normalization is a non-blocking improvement.

### Subprojects

**All subprojects, if any, are listed.**
<br>
**Incubating:** Required | **Graduated:** Required

The Graduation application lists subprojects and related repositories under the Volcano organization, including community, website, charts/helm charts, kthena, agentcube, volcano-global, apis, devices, dashboard, descheduler, resource-exporter, kubegene, and kubegene-website.

**If the project has subprojects: subproject leadership, contribution, maturity status documented, including add/remove process.**
<br>
**Incubating:** Suggested | **Graduated:** Required

Volcano documents subproject acceptance in [GOVERNANCE.md](../GOVERNANCE.md) and a more detailed creation process in [subproject-creation.md](../subproject-creation.md). A proposed subproject must be Apache-2.0 licensed, related to Volcano's ecosystem scope, supported by a maintainer not affiliated with the subproject authors, presented to the community, reviewed in a meeting, and go through a public review period.

The main improvement area is to maintain a canonical table of active subprojects that includes leadership, contribution path, communication channel, and maturity/status for each subproject.

Assessment: Mostly Satisfactory. The add process is strong and public, but subproject inventory and status should be consolidated.

### Contributors and Community

**Contributor ladder with multiple roles for contributors.**
<br>
**Incubating:** Suggested | **Graduated:** Suggested

Volcano has a multi-level contributor ladder documented in [community-membership.md](../community-membership.md): Member, Reviewer, Approver, Maintainer, and Owner. Each role includes requirements, responsibilities, and privileges.

**Clearly defined and discoverable process to submit issues or changes.**
<br>
**Incubating:** Required | **Graduated:** Required

The contribution process is documented in [contribute.md](../contribute.md), including how to find issues, file issues, create topic branches, submit pull requests, and participate in code review. The community [README.md](../README.md) links directly to this contributor guide.

**Project must have, and document, at least one public communications channel for users and/or contributors.**
<br>
**Incubating:** Required | **Graduated:** Required

Volcano documents public communication channels in [README.md](../README.md), including CNCF Slack, mailing list, Twitter, community meetings, meeting notes, Zoom, and calendar links.

**List and document all project communication channels, including subprojects (mail list/slack/etc.). List any non-public communications channels and what their special purpose is.**
<br>
**Incubating:** Required | **Graduated:** Required

The community [README.md](../README.md) documents the main public channels. [SECURITY.md](../SECURITY.md) documents private security disclosure and distributor announcement channels, including their special security coordination and embargo purposes. The project should add communication channel details to the recommended canonical subproject table where subprojects use distinct channels.

**Up-to-date public meeting schedulers and/or integration with CNCF calendar.**
<br>
**Incubating:** Required | **Graduated:** Required

The community [README.md](../README.md) documents biweekly meetings for Asia, Europe, and Pacific time zones and provides links to meeting notes, the Zoom meeting, a public calendar, and a subscription link.

**Documentation of how to contribute, with increasing detail as the project matures.**
<br>
**Incubating:** Required | **Graduated:** Required

Volcano provides a contributor guide covering issue selection, issue filing, PR workflow, review expectations, commit-message guidance, and testing expectations.

**Demonstrate contributor activity and recruitment.**
<br>
**Incubating:** Required | **Graduated:** Required

Volcano demonstrates contributor activity through ongoing GitHub issues and pull requests, a large public contributor base, multiple public communication channels, regular community meetings, and documented beginner-friendly issue discovery through `help wanted` and `good first issue` labels.

Assessment: Satisfactory. Contributor and community processes are well documented and publicly discoverable. Consolidating subproject communications would further improve completeness.

[project milestone or other requirement]: https://github.com/cncf/toc/tree/main/process#how-to-apply-to-move-levels
[vendor-neutrality]: https://contribute.cncf.io/maintainers/community/vendor-neutrality/