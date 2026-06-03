# Dependency management policy

This document describes how the Volcano project manages software dependencies.
It applies to the primary code repository [volcano-sh/volcano](https://github.com/volcano-sh/volcano)
and related subprojects under the [volcano-sh](https://github.com/volcano-sh/) organization.

## Declaring dependencies

- Go modules in `go.mod` and `go.sum` are the source of truth for Volcano core dependencies.
- Staging API dependencies are declared in `staging/src/volcano.sh/apis/go.mod` and `go.sum`.
- Contributors must follow the [license compliance rules](compliance.md#rules) when adding or updating dependencies.

## Updating dependencies

- [Dependabot](https://github.com/volcano-sh/volcano/blob/master/.github/dependabot.yml) proposes updates to Go modules and GitHub Actions dependencies.
- Maintainers review and merge dependency update pull requests using the normal [contribution workflow](contribute.md#contributor-workflow).
- Release timing and stabilization windows are described in the [version release policy](version-release.md).

## License and compliance

- Allowed and restricted licenses are defined in [compliance.md](compliance.md#license-compliance-check).
- License scanning in CI is configured in the Volcano repository (for example, FOSSA and license lint workflows).

## Security vulnerabilities in dependencies

- Report security issues privately as described in [SECURITY.md](SECURITY.md#private-disclosure-processes).
- The [Product Security Team (PST)](PST.md) coordinates fixes and releases when a dependency-related vulnerability affects Volcano.

## Release supply chain information

- Official releases are published on the [Volcano GitHub releases](https://github.com/volcano-sh/volcano/releases) page.
- Release artifacts and distribution points are documented in Volcano’s [SECURITY-INSIGHTS.yml](https://github.com/volcano-sh/volcano/blob/master/SECURITY-INSIGHTS.yml) when present on the default branch.
- SPDX software bill of materials (SBOM) archives may be attached to versioned releases for users and scanners to inspect included components.

## Related documents

- [Contributor Guide](contribute.md)
- [Security release process](SECURITY.md)
- [Open source compliance](compliance.md)
- [Version release policy](version-release.md)
