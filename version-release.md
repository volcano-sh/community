# Volcano Version Release

This document describes how the Volcano community plans and publishes releases
for Volcano and its subprojects.

## Versioning

Volcano projects use versions in the `X.Y.Z` format.

* `X` is the major version. It is increased when a release contains
  incompatible API, behavior, or dependency changes.
* `Y` is the minor version. It is increased for regular feature releases that
  keep backward compatibility as much as possible.
* `Z` is the patch version. It is increased for bug fixes, security fixes,
  dependency updates, or packaging and documentation fixes that do not introduce
  new features.

For example, `1.13.2` means major version `1`, minor version `13`, and patch
version `2`.

Pre-release versions may be published when the maintainers think broader testing
is needed before an official release.

## Release Cadence

Volcano projects may follow different release cadences according to project
status, user requirements, and community discussion.

The Volcano main repository usually publishes a minor release every four months.
Release planning normally starts about one month before the target release date.
The release manager collects requirements, confirms the release scope, tracks
release blockers, and publishes the release plan to the community.

Some subprojects with a clear release plan may use their own cadence. For
example, Kthena usually publishes a minor release about every three months. The
cadence of such projects should be discussed in the community and reflected in
the project roadmap or release plan.

Other Volcano projects may use a flexible release cadence. They can publish a
release when there are enough feature updates, important bug fixes,
compatibility updates, or user requirements. Maintainers should still announce
the planned release scope and timeline in the community whenever possible.

## Version Plan

Version planning is an ongoing activity during the release cycle. Some work
items are planned before the cycle starts, while others may be added later based
on user feedback, community discussion, bug reports, or dependency changes.

The community may use GitHub Projects, issues, milestones, or roadmap documents
to track work items that are being considered for the next release. These lists
show the current focus of the release and are not a fixed commitment.

### Requirements Collection

Requirements are collected from common user scenarios, open issues, pull
requests, user cases, compatibility work, and maintainer proposals. The release
manager and maintainers may group related items and keep them in the release
tracking list for follow-up.

### Community Review

The requirement list can be submitted to the community meeting or discussed in
public issues and pull requests. Community members may evaluate the scenarios,
rationality, feature design points, development workload, compatibility impact,
test plan, documentation updates, and other dimensions of the requirements.

After the discussion, items that are ready and have enough owner support may be
included in the roadmap or release plan. Items that are not yet ready may be
moved to a later release.

## Version Release

### Release Branch

Before publishing a release, a new branch whose name is like `release-X.Y` or
`release-X.Y.Z` will be checked out to prepare the release. The exact branch
name can follow the convention of each repository.

Release related bug fixes, regression fixes, security fixes, documentation
fixes, and release engineering changes can be merged into the release branch.
Normal development may continue on master during the release period.

### Release Stabilization

Before the official release is published, maintainers should focus on release
blocking issues, compatibility problems, installation problems, and important
regressions found during community testing.

Users and community members are welcome to test the release branch or
pre-release artifacts if they are available. Feedback should be tracked in
public issues or pull requests whenever possible.

### Release Publication

We will publish every official release and related artifacts, such as source
archives, release notes, docker images, charts, or packages according to the
project. Users can find release artifacts in the release list and corresponding
image registry or package registry.

## Patch Release

Bug fix versions such as `X.Y.Z` are released any time we consider it necessary
after important bugs are fixed. Patch releases do not have a fixed cadence.

A patch release may be created for important bug fixes, security fixes,
Kubernetes or dependency compatibility fixes, regressions introduced by a recent
release, or packaging and installation fixes that affect users.

Patch releases should not include new features or intentional compatibility
breaks. Feature work should go to master and be included in a future minor or
major release.

## Supported Versions

Patch fixes are maintained for the current master branch and the latest three
release branches. When a new minor version is released, the supported release
branches move forward together.

For example, if the latest release branch is `release-1.13`, patch fixes may be
maintained for master, `release-1.13`, `release-1.12`, and `release-1.11`. After
`release-1.14` is published, the maintained branches become master,
`release-1.14`, `release-1.13`, and `release-1.12`. Earlier release branches
will no longer receive patch releases.

Only important bug fixes, security fixes, and low-risk compatibility fixes are
backported to supported release branches. Feature changes are not backported.

Backports are evaluated case by case, based on the impact on users, the risk of
the change, and whether it can be tested on the target branch.

## Exceptions

The release manager and maintainers may adjust the release date, release scope,
or supported patch branches when required by quality, security, compatibility,
or maintainer availability. Any significant change should be announced to the
community in advance whenever possible.
