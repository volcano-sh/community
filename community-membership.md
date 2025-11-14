
# Volcano Community Membership

**Note :** This document keeps changing based on the status and feedback of Volcano Community.

This document gives a brief overview of the Volcano community roles with the requirements and responsibilities associated with them.

| Role | Requirements | Responsibilities | Privileges |
| -----| ---------------- | ------------ | -------|
| [Member](#member) | Sponsor from 2 approvers, active in community, contributed to Volcano | Welcome and guide new contributors | Volcano GitHub organization Member |
| [Reivewer](#reviewer) | Sponsor from 2 maintainers, has basic experience and knowledge of domain, actively contributed to code and review | Review contributions from community members | Write access to specific packages in relevant repository |
| [Approver](#approver) | Sponsor from 2 maintainers, has good experience and knowledge of domain, actively contributed to code and review  | Review and approve contributions from community members | Write access to specific packages in relevant repository |
| [Maintainer](#maintainer) | Sponsor from 2 owners, shown good technical judgement in feature design/development and PR review | Participate in release planning and feature development/maintenance | Top level write access to relevant repository. Name entry in Maintainers file of the repository |

**Note :** For detailed role promotion process, please see [Role Promotion Process](#role-promotion-process). It is mandatory for all Volcano community members to follow Volcano [Code of Conduct](./code_of_conduct.md).

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

- Approver for at least 2 months
- Nominated by an existing Maintainer via GitHub issue
- Demonstrates good technical judgement in feature design/development
- Approved by majority (>50%) of active Maintainers through voting

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

**Note :** These roles are applicable only for Volcano github organization and repositories. Currently Volcano doesn't have a formal process for review and acceptance into these roles. We will come-up with a process soon.

## Role Promotion Process

### For Member, Reviewer, and Approver

1. **Application:** Submit Organization Membership Request via
   [membership.yaml issue template](https://github.com/volcano-sh/community/issues/new?template=membership.yaml)

2. **Sponsor Requirements:**
   - Member: 2 Approvers must sponsor
   - Reviewer: 2 Maintainers must sponsor
   - Approver: 2 Maintainers must sponsor

3. **Voting:** Sponsors express support by commenting in the issue
   (e.g., "+1, thanks for your contribution", "LGTM", or similar endorsement)

4. **Approval:** Once required number of valid sponsor votes received, membership is approved

5. **Onboarding:**
   - Add to appropriate OWNERS files（For reviewer/approver)
   - Grant GitHub organization membership (For member)

### For Maintainer

1. **Nomination:** Any existing Maintainer creates a GitHub issue proposing the candidate with nomination rationale (qualifications, contribution history, etc.)

2. **Voting:** All active Maintainers vote in the nomination issue. Vote formats could be: +1 (approve), 0 (abstain), -1 (object with reasoning)

3. **Approval Criteria:**
   Majority (>50%) of active Maintainers must vote +1

4. **Public Notice Period:**
   Once voting passes, open for community feedback for 1 week. Community members can raise concerns during this period

5. **Onboarding:**
   Add to MAINTAINERS.md via PR

### Notes

- All promotion discussions and votes happen in public GitHub issues for transparency
- Candidates should not vote for themselves
- Sponsors/voters from diverse organizations are preferred

[two-factor authentication]: https://help.github.com/articles/about-two-factor-authentication
