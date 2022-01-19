# How to Create a Subproject under Volcano Organization

## Background
As the scope of Volcano is growing larger, more and more contributors show great willing to create or donate a new subproject
for Volcano. This document details the subproject creation process and specifications.

## Workflow
![Subproject Creation Workflow](./images/subproject-creation-workflow.jpg)

### Send Proposal
The subproject founder send a proposal to the community by means of submitting an issue. What the issue must contain are
as follows:
* **Background**
* **Project Brief Introduction**
* **Founder Introduction**
* **License**

### Explanation Meeting
The community will assign a maintainer as the Sponsor to be responsible for the event end to end after receiving the 
proposal. The Sponsor will make a quick understanding of the project and then book an explanation meeting. The founder
should give a detailed description about the project.

#### Meeting Process
1. The founder makes the description.
2. The participants asked questions and the founder give the explanations.
3. Meeting voting
4. The Sponsor announces the vote result.

#### Required Description Items
* **The scope of the subject**
* **Project details**
* **License adoption**

#### Meeting Participants
* **All owners must attend the meeting. At least 2/3 current maintainers should be present.**
* **At least 1 represent from the founder organization should be present.**
* No special requirements for other roles.

#### Responsibilities For Sponsor
* Set the meeting time.
* Inform the meeting to all participants.
* Publish the meeting to the community.
* Host the meeting.

### Community Review
The community review consists of **meeting review** and **publicity review**. Only both reviews are passed shall the proposal be
recognised as passed.

#### Meeting Review
* Meeting Review is the review from the participants attending the explanation meeting.
* **Only all owners and maintainers have the voting rights.**
* **At least 2/3 approves from the group who have voting rights and no negative votes can be thought of proposal passed.**

#### Publicity Review
* Publicity Review is the review from all the community after the explanation meeting finishes.
* **Default publicity period is 2 weeks.** Anyone can ask questions about the proposal and the founder must give explanations.
* If no negative votes, the proposal will be considered as passed by default. The sponsor will announce the final result.
If there are still some critical questions or advices not be replied, the founder has the responsibility to improve the 
proposal and submit again. The sponsor undertake the task to pick out which are critical questions or advices.

### Improve the Proposal
The founder should improve the content of the proposal according to the feedback from meeting review and publicity review.
Then submit the proposal again.

### Project Self-Check
As to the projects which have already source code, the founder should finish the self-check according to the checklists
in the appendixes. If there is any questions, please contact with the sponsor for help.

### Material Submission
Once finish the project self-check, the founder will submit all the materials to the community. The material list can be
found under the appendix.

## Appendix
* Self-Check List

  | ID | Item | Description | Required | Compliance Conditions | Note |
  | :----:| :----: | :----: | :----: | :----: | :----: |
  | 1 | Code of Conduct | The conduct for the source code | Y | [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/) | Submit the code scanning report |
  | 2 | License | The License the project obeys | Y | [Apache 2.0](https://github.com/volcano-sh/volcano/blob/master/LICENSE) |  |
  | 3 | Readme | Brief introduction of the project along with the source code | Y |  |  |
  | 4 | CI/CD | The CI/CD to judge the compliance for all PRs | Y | [Github Action](https://docs.github.com/en/actions) |  |
  | 5 | Security | Security policy including vulnerability discovery and disposal | Y | [Security Release Process](https://github.com/volcano-sh/volcano/blob/master/SECURITY.md) | Submit security scanning report |
  | 6 | Roadmap | Roadmap file about the important features in the feature | Y |  |  |
  | 7 | Design Documentations | Documentations about the record of feature designs | Y |  |  |

* Material List

  | ID | Item | Description | Note |
  | :----:| :----: | :----: | :----: |
  | 1 | Source Code | The complete source code of the project |  |