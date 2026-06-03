
# Volcano Community Membership

**Note :** This document keeps changing based on the status and feedback of Volcano Community.

This document gives a brief overview of the Volcano community roles with the requirements and responsibilities associated with them.

| Role | Requirements | Responsibilities | Privileges |
| -----| ---------------- | ------------ | -------|
| [Member](#member) | Sponsor from 2 approvers, active in community, contributed to Volcano | Welcome and guide new contributors | Volcano GitHub organization Member |
| [Reivewer](#reviewer) | Sponsor from 2 maintainers, has basic experience and knowledge of domain, actively contributed to code and review | Review contributions from community members | Write access to specific packages in relevant repository |
| [Approver](#approver) | Sponsor from 2 maintainers, has good experience and knowledge of domain, actively contributed to code and review  | Review and approve contributions from community members | Write access to specific packages in relevant repository |
| [Maintainer](#maintainer) | Sponsor from 2 maintainers, shown good technical judgement in feature design/development and PR review | Participate in release planning and feature development/maintenance | Top level write access to relevant repository. Name entry in Maintainers file of the repository |

**Note :** It is mandatory for all Volcano community members to follow Volcano [Code of Conduct](./code_of_conduct.md).

## Member

Members are active participants in the community who contribute by authoring PRs,
reviewing issues/PRs or participate in community discussions on slack/mailing list.

### Requirements

- Sponsor from 2 approvers
- Enabled [two-factor authentication] on their GitHub account
- Actively contributed to the community. Contributions may include, but are not limited to:
    - Authoring PRs
    - Reviewing issues/PRs authored by other community members
    - Participating in community discussions on slack/mailing list
    - Participate in Volcano community meetings

**NOTE:** In addition to contributing code to the community, if you are the contact person for an adopter, you can also apply to become a Member.

### Responsibilities and privileges

- Member of the Volcano GitHub organization
- Can be assigned to issues and PRs and community members can also request their review
- Participate in assigned issues and PRs
- Welcome new contributors
- Guide new contributors to relevant docs/files
- Help/Motivate new members in contributing to Volcano

## Reviewer

Reviewers are active members who have basic experience and knowledge of the domain.
They have actively participated in the issue/PR reviews and have identified relevant issues during review.

### Requirements

- Sponsor from 2 maintainers
- Member for at least 2 months
- Have reviewed good number of PRs
- Have good codebase knowledge

### Responsibilities and Privileges

- Review code to maintain/improve code quality
- Acknowledge and work on review requests from community members
- Have 'write access' to specific packages inside a repo, enforced via bot
- Continue to contribute and guide other community members to contribute in Volcano project

## Approver

Approvers are active members who have good experience and knowledge of the domain.
They have actively participated in the issue/PR reviews and have identified relevant issues during review.

### Requirements

- Sponsor from 2 maintainers
- Reviewer for at least 2 months
- Have reviewed good number of PRs
- Have good codebase knowledge

### Responsibilities and Privileges

- Review code to maintain/improve code quality
- Acknowledge and work on review requests from community members
- May approve code contributions for acceptance related to relevant expertise
- Have 'write access' to specific packages inside a repo, enforced via bot
- Continue to contribute and guide other community members to contribute in Volcano project

## Maintainer

Maintainers are approvers who have shown good technical judgement in feature design/development in the past.
Has overall knowledge of the project and features in the project.

### Requirements

- Deep understanding of the technical goals and direction of the project.
- Deep understanding of the technical domain (specifically the language) of the project.
- Sustained contributions to design and direction by doing all of:
  - Authoring and reviewing proposals
  - Initiating, contributing and resolving discussions (e.g. emails, GitHub issues, meetings)
  - Identifying subtle or complex issues in designs and implementation PRs
- Nominated by a maintainer and pass super-majority(two-thirds/ 66.66%) vote.

### Responsibilities and privileges

- Participate in release planning
- Maintain project code quality
- Ensure API compatibility with forward/backward versions based on feature graduation criteria
- Analyze and propose new features/enhancements in Volcano project
- Demonstrate sound technical judgement
- Mentor contributors and approvers
- Have top level write access to relevant repository (able click Merge PR button when manual check-in is necessary)
- Name entry in Maintainers file of the repository
- Participate & Drive design/development of multiple features

## Inactive members

_Members are continuously active contributors in the community._

A core principle in maintaining a healthy community is encouraging active participation. It is inevitable that people's focuses will change over time and they are not expected to be actively contributing forever.

However, serving as a maintainer or approver for one of the Volcano GitHub organizations comes with an elevated set of permissions. These capabilities should not be used by those that are not familiar with the current state of the Volcano project.

Therefore Maintainers or Approver who is extended period away from the project with no activity will be removed from the Volcano Github Organizations and will be required to go through the org membership process again after re-familiarizing themselves with the current state.

### How inactivity is measured

Inactive members are defined as members of one of the Volcano Organizations with **no** contributions across any organization within 18 months. This is measured by the CNCF [DevStats project].

**Note:** Devstats does not take into account non-code contributions. If a non-code contributing member is accidentally removed this way, they may open an issue to quickly be re-instated.

After an extended period away from the project with no activity those members would need to re-familiarize themselves with the current state before being able to contribute effectively.


**Note :** These roles are applicable only for Volcano github organization and repositories. Currently Volcano doesn't have a formal process for review and acceptance into these roles. We will come-up with a process soon.

[two-factor authentication]: https://help.github.com/articles/about-two-factor-authentication
[Devstats project]: https://volcano.devstats.cncf.io/
