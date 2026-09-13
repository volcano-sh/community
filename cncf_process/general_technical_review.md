# General Technical Review - Volcano / Graduation

- **Project:** Volcano
- **Project Version:** v1.15.0
- **Website:** <https://volcano.sh/>
- **Date Updated:** 2026-06-02
- **Template Version:** v1.0
- **Template Link:** [cncf/toc general-technical-questions.md](https://github.com/cncf/toc/blob/main/toc_subprojects/project-reviews-subproject/general-technical-questions.md)
- **Description:** Volcano is a Kubernetes-native batch scheduling system for high-performance AI/ML, big data, HPC, and elastic workloads. It extends Kubernetes scheduling with gang scheduling, queue management, fair-share and quota policies, preemption/reclaim/backfill, topology-aware placement, heterogeneous device scheduling, and integrations with common workload frameworks.
- **Reviewers:** TBD

Reference revisions used while preparing this document:

- Volcano repository: [`d8dcf154bcb3f1a378374f95cf2460cfcda7663d`](https://github.com/volcano-sh/volcano/tree/d8dcf154bcb3f1a378374f95cf2460cfcda7663d)
- Volcano website repository: [`9f0409c161df8eed6439d06cbf73580797d21055`](https://github.com/volcano-sh/website/tree/9f0409c161df8eed6439d06cbf73580797d21055)
- Volcano community repository: [`00ccf774aa4309cf45da50729ae6e2ce688ed53f`](https://github.com/volcano-sh/community/tree/00ccf774aa4309cf45da50729ae6e2ce688ed53f)

## Overview

Volcano fills a gap in the Kubernetes ecosystem for batch, AI/ML, big data, HPC, genomics, and other high-performance workloads that require coordinated startup, resource queues, topology-aware scheduling, device-aware scheduling, and tenant-aware sharing policies. Kubernetes provides the extensibility points that make this possible, while Volcano contributes a scheduler, controller manager, admission webhook, command-line tooling, and Kubernetes Custom Resource Definitions (CRDs) for jobs, queues, and pod groups.

Volcano is designed to be Kubernetes-native. Users can run native Pods and Kubernetes workloads with `schedulerName: volcano`, or submit higher-level Volcano `Job` resources. Volcano integrates with frameworks including Spark, Flink, Ray, TensorFlow, PyTorch, Argo Workflows, MindSpore, PaddlePaddle, OpenMPI, Horovod, MXNet, Kubeflow Training Operator, KubeGene, and Cromwell. Public adoption includes Internet/Cloud, finance, manufacturing, medical, and cloud-provider use cases.

## Day 0 - Planning Phase

### Scope

#### Describe the roadmap process, how scope is determined for mid to long term features, as well as how the roadmap maps back to current contributions and maintainer ladder?

Volcano roadmap planning is community-driven and follows the public governance model in [GOVERNANCE.md](https://github.com/volcano-sh/community/blob/master/GOVERNANCE.md#volcano-roadmap), the community membership ladder in [community-membership.md](https://github.com/volcano-sh/community/blob/master/community-membership.md), and the release process in [version-release.md](https://github.com/volcano-sh/community/blob/master/version-release.md).

The project uses the following planning mechanisms:

- **Requirement collection:** Before a release, requirements are collected from community feedback, common user scenarios, GitHub issues, design proposals, and maintainer input.
- **Community review:** Requirements are discussed in public community meetings and reviewed for scenario value, design feasibility, implementation cost, and alignment with Volcano's scope.
- **Mapping to Contributions:** Issues are tagged with milestone labels and tracked on release project boards to ensure alignment with the roadmap.
- **Maintainer mapping:** Members, reviewers, approvers, and maintainers have documented responsibilities. Maintainers participate in release planning and help drive the overall technical roadmap.

#### Describe the target persona or user(s) for the project?

Volcano serves several primary personas:

- **Platform engineering teams** operating Kubernetes clusters for AI/ML, big data, HPC, research, and batch workloads.
- **ML infrastructure and AI platform teams** running distributed training, inference, LLM pipelines, and GPU/NPU-intensive workloads.
- **Big data and analytics teams** running Spark, Flink, Ray, Argo, MPI, or workflow workloads on Kubernetes.
- **HPC, genomics, bioinformatics, and scientific computing users** who need gang scheduling, topology-aware placement, and queue-based resource control.
- **Cluster administrators and SREs** who operate shared Kubernetes clusters and need multi-tenant quota, fair sharing, preemption, reclaim, monitoring, and operational control.

#### Explain the primary use case for the project. What additional use cases are supported by the project?

The primary use case is Kubernetes-native batch and high-performance workload scheduling. Volcano provides scheduling semantics that are critical for distributed jobs but are not fully covered by the default Kubernetes scheduler, including:

- Gang scheduling for jobs that should start all required tasks together.
- Queue-based scheduling and resource division across tenants and teams.
- Fair-share, proportion, capacity, preemption, reclaim, and backfill scheduling.
- Heterogeneous device scheduling for GPUs, vGPUs, NVIDIA MIG, NPUs, and other accelerators.
- Topology-aware scheduling for network-intensive and NUMA-sensitive workloads.
- Job lifecycle management through `Job`, `PodGroup`, and `Queue` APIs.

Additional supported use cases include:

- AI/ML and deep learning training with TensorFlow, PyTorch, Kubeflow, MindSpore, PaddlePaddle, Horovod, and MXNet.
- Ray and Spark workloads on Kubernetes.
- Big data and streaming workloads such as Flink and Spark.
- HPC and MPI workloads.
- Genomics and bioinformatics workflows such as KubeGene and Cromwell.
- Shared enterprise clusters that require tenant-aware resource governance.
- Online/offline workload colocation and descheduling through related Volcano subprojects and integrations.

#### Explain which use cases have been identified as unsupported by the project.

Volcano is not intended to replace Kubernetes as a general-purpose control plane. It is not a standalone batch platform independent of Kubernetes.

Unsupported or out-of-scope use cases include:

- Non-Kubernetes environments.
- Cloud-provider-specific resource provisioning as a core feature. Volcano can schedule workloads on cloud or on-premises Kubernetes clusters, but cloud infrastructure provisioning remains the responsibility of the adopter or an external platform.

#### Describe the intended types of organizations who would benefit from adopting this project. (i.e. financial services, any software manufacturer, organizations providing platform engineering services)?

Volcano is useful to organizations that run batch, AI/ML, big data, HPC, or accelerator-heavy workloads on Kubernetes, including:

- Cloud service providers and managed Kubernetes providers.
- Financial services organizations running analytics, risk, and big data workloads.
- Internet, media, and recommendation platform companies running large-scale ML and data processing.
- Manufacturing, autonomous driving, pharmaceutical, medical, genomics, and scientific research organizations.
- Enterprises building internal AI platforms or shared platform-engineering services.
- Universities and research institutions running shared HPC or ML clusters.
- SaaS and software vendors integrating Kubernetes-native workload orchestration into their products.

#### Please describe any completed end user research and link to any reports.

Volcano continuously collects user feedback through public issues, community meetings, adopters, design proposals, and case studies. Published user research and evidence include:

- [ING Bank: How Volcano empowers its big data analytics platform](https://www.cncf.io/blog/2023/02/21/ing-bank-how-volcano-empowers-its-big-data-analytics-platform/)
- [Why Spark chooses Volcano as built-in batch scheduler on Kubernetes](https://www.cncf.io/blog/2022/06/30/why-spark-chooses-volcano-as-built-in-batch-scheduler-on-kubernetes/)
- [Using Volcano as a custom scheduler for Apache Spark on Amazon EMR on EKS](https://docs.aws.amazon.com/emr/latest/EMR-on-EKS-DevelopmentGuide/tutorial-volcano.html)
- [Deploy Azure Machine Learning extension on AKS or Arc Kubernetes cluster](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-deploy-kubernetes-extension)
- [Practical Tips for Preventing GPU Fragmentation for Volcano Scheduler](https://developer.nvidia.com/blog/practical-tips-for-preventing-gpu-fragmentation-for-volcano-scheduler/)
- [Xiaohongshu content recommendation engine case study](https://volcano.sh/en/blog/xiaohongshu-en/)
- [Ruitian large-scale offline HPC jobs case study](https://volcano.sh/blog/ruitian-en/)
- [iQIYI cloud-native migration case study](https://volcano.sh/en/blog/aiqiyi-en/)
- [Volcano performance tuning for large-scale scenarios](https://github.com/volcano-sh/website/blob/9f0409c161df8eed6439d06cbf73580797d21055/docs/UserGuide/user_guide_how_to_tune_volcano_performance.md)

### Usability

#### How should the target personas interact with your project?

Users interact with Volcano through Kubernetes-native resources and tooling:

- Cluster administrators install Volcano into a Kubernetes cluster, typically in the `volcano-system` namespace.
- Workload owners submit `Job` resources or native Kubernetes workloads with `schedulerName: volcano`.
- Platform teams create and manage `Queue` resources to control tenant quota, priority, and resource sharing.
- Framework integrations generate Volcano-compatible resources. For example, Spark, Ray, PyTorch, TensorFlow, MPI, and other framework integrations can submit pods or jobs that are scheduled by Volcano.
- Operators inspect `Job`, `PodGroup`, `Queue`, events, logs, and Prometheus metrics to understand scheduling state and health.
- Advanced users customize scheduler actions and plugins via the `volcano-scheduler-configmap` ConfigMap.

#### Describe the user experience (UX) and user interface (UI) of the project.

Volcano's UX is Kubernetes-native and declarative:

- **YAML/API UX:** Users describe queues, pod groups, jobs, and workload templates as Kubernetes resources.
- **CLI UX:** Users can use `kubectl` for resources and `vcctl` for Volcano-specific operations.
- **Framework UX:** Many users interact indirectly through Spark, Ray, Kubeflow Training Operator, Argo, MPI, TensorFlow, PyTorch, or other framework tooling.
- **Configuration UX:** Administrators tune scheduling through a ConfigMap that declares actions and plugin tiers.
- **Observability UX:** Users view Kubernetes events, component logs, Prometheus metrics, and optional dashboards.
- **Dashboard UX:** The [Volcano dashboard subproject](https://github.com/volcano-sh/dashboard) provides a graphical interface for users who prefer a web UI.

#### Describe how this project integrates with other projects in a production environment.

Volcano integrates through Kubernetes APIs and scheduling extension points:

- **Kubernetes:** Volcano runs as Kubernetes workloads and extends Kubernetes with CRDs, admission webhooks, and a scheduler. It uses Kubernetes authentication, authorization, API storage, events, and controller reconciliation patterns.
- **Batch and ML frameworks:** Volcano integrates with Spark, Flink, Ray, TensorFlow, PyTorch, Kubeflow, MPI, PaddlePaddle, MindSpore, MXNet, Horovod, Argo, KubeGene, and Cromwell.
- **Monitoring:** Volcano exposes Prometheus-style metrics and can be monitored with Prometheus and Grafana.
- **Cloud providers:** AWS EMR on EKS and Azure Machine Learning on AKS document or support Volcano as a workload scheduler option.
- **Device plugins and accelerator stacks:** Volcano can be used with GPU, vGPU, MIG, NPU, DRA, and related device plugins to improve accelerator scheduling.
- **Related Volcano subprojects:** Volcano integrates with dashboard, devices, descheduler, resource-exporter, volcano-global, helm-charts, and website repositories under the Volcano organization.

### Design

#### Explain the design principles and best practices the project is following.

Volcano follows these design principles:

- **Kubernetes-native:** Use Kubernetes APIs, CRDs, controllers, admission webhooks, events, scheduler interfaces, and RBAC instead of inventing a separate platform.
- **Declarative APIs:** Users declare desired job, queue, and podgroup state; controllers and the scheduler reconcile toward that state.
- **Extensible scheduling:** The scheduler uses actions and plugins so adopters can configure or extend scheduling behavior for different domains.
- **Batch-first semantics:** Gang scheduling, queues, preemption/reclaim, backfill, and job lifecycle management are first-class concepts.
- **Multi-tenancy and fairness:** Queue policies support resource quota, borrowing, reclaiming, priority, and isolation across teams.
- **Cloud and vendor neutrality:** Volcano runs on upstream Kubernetes distributions across clouds and on-premises environments.
- **Operational transparency:** Scheduling state is observable through CRD status, events, logs, and metrics.
- **Community governance:** Project direction, membership, subprojects, releases, and security processes are documented publicly.

#### Outline or link to the project’s architecture requirements? Describe how they differ for Proof of Concept, Development, Test and Production environments, as applicable.

Architecture documentation:

- [Volcano architecture](https://volcano.sh/docs/Home/Architecture)
- [Volcano introduction and feature overview](https://volcano.sh/docs/Home/Introduction)
- [Volcano scheduler overview](https://volcano.sh/docs/Scheduler/Overview)

Volcano consists primarily of:

- **Scheduler:** Schedules jobs and pods to nodes using configured actions and plugins.
- **Controller manager:** Reconciles Volcano CRDs such as `Queue`, `PodGroup`, and `Job`.
- **Admission webhook:** Validates and mutates Volcano CRDs and related pods.
- **CLI/tooling:** `vcctl` and `kubectl` interactions.
- **CRDs:** APIs for jobs, queues, pod groups, and related scheduling constructs.

Environment differences:

- **Proof of Concept / local development:** Users can install with the development YAML or run `./hack/local-up-volcano.sh` for one-click local setup.
- **Development / test clusters:** Users generally install YAML or Helm releases, test example workloads, enable relevant plugins, and validate component readiness, events, and metrics.
- **Production:** Users should install a pinned release, configure resource requests/limits, tune scheduler plugins and admission settings, monitor metrics and logs, apply Kubernetes RBAC and network controls, and plan upgrades through Helm or controlled manifest changes.

#### Define any specific service dependencies the project relies on in the cluster.

Mandatory runtime dependencies:

- Kubernetes API server, CRDs, admission webhook support, and standard controller/scheduler mechanisms.
- Kubernetes cluster for storing Volcano CRDs, component configuration, workload objects, and status.
- ServiceAccounts, RBAC, Secrets, ConfigMaps, Deployments, Jobs, and Services.

Optional integrations:

- Prometheus and Grafana for metrics collection and dashboards.
- Volcano Dashboard for web UI.
- Device plugins and accelerator runtimes for GPU/NPU/vGPU/MIG scheduling.
- Descheduler, resource-exporter, and other Volcano subprojects for specialized operations.

#### Describe how the project implements Identity and Access Management.

Volcano itself is a scheduling platform that does not provide its own API server and relies on Kubernetes to store its API objects. Therefore, all identity and access management is handled by Kubernetes:

- Users access Volcano resources(Job/Queue/PodGroup) through the Kubernetes API server, which applies the cluster's configured authentication and authorization stack.
- Admission webhook access is protected by Kubernetes service and TLS mechanisms.

#### Describe how the project has addressed sovereignty.

Volcano is cloud-agnostic and does not require a proprietary hosted service. Scheduling decisions and workload metadata remain in the adopter's Kubernetes cluster and backing etcd. Users can run Volcano on-premises, in public cloud, at the edge, or in regulated environments.

For sovereignty-sensitive deployments:

- Users choose where clusters, API servers, etcd, logs, metrics, and dashboards are hosted.
- Volcano does not require calls to an external SaaS control plane for core scheduling.

#### Describe any compliance requirements addressed by the project.

Volcano helps adopters build compliant environments by providing Kubernetes-native access control, audit integration through Kubernetes, Apache-2.0 licensing, public security processes, and open governance.

Project-level compliance practices include:

- Apache License 2.0 for source code and releases.
- Public governance and Code of Conduct.
- License linting and FOSSA analysis in CI.
- OpenSSF Best Practices passing badge.
- OpenSSF Scorecard.
- Third-party security audit report.
- Security self-assessment.
- Private security reporting and coordinated vulnerability disclosure process.

#### Describe the project’s High Availability requirements.

Volcano components run as Kubernetes workloads and rely on Kubernetes self-healing. Production high availability recommendations include:

- Run multiple replicas of stateless components where supported and appropriate.
- Use Kubernetes Deployments to restart failed scheduler, controller-manager, and admission pods.
- Ensure the backing Kubernetes control plane and etcd are highly available.
- Protect the `volcano-system` namespace with resource requests/limits and scheduling constraints so Volcano components are not starved.

If Volcano's scheduler or controller manager is unavailable, already running workloads generally continue running on their assigned nodes, but new scheduling, queue state changes, job lifecycle updates, and reconciliation may be delayed. If the admission webhook is unavailable or overloaded, creation or mutation of affected resources may fail or be delayed depending on webhook policy and cluster configuration.

#### Describe the project’s resource requirements, including CPU, Network and Memory.

Resource requirements depend on cluster scale, workload count, pod count, queue count, plugin configuration, and scheduler actions.  For large-scale clusters, resource requests and limits should be adjusted accordingly.

#### Describe the project’s storage requirements, including its use of ephemeral and/or persistent storage.

Volcano components are primarily stateless. Persistent state is stored in Kubernetes through the API server and etcd as CRDs, ConfigMaps, Secrets, Jobs, Queues, PodGroups objects, events, and status.

#### Please outline the project’s API Design:

##### Describe the project’s API topology and conventions

Volcano follows Kubernetes API conventions:

- APIs are exposed as CRDs and standard Kubernetes resources.
- Specs define desired state; status fields report observed state.
- Resources use Kubernetes metadata, labels, annotations, owner references, and namespace scoping where appropriate.
- Users can operate resources with `kubectl`, client-go, framework controllers, and CI/CD systems.

Core APIs include:

- `batch.volcano.sh/v1alpha1` `Job` (`Job` / `vcjob`): advanced batch job abstraction with `minAvailable`, task templates, plugins, lifecycle policies, queue, priority, retries, and volume support.
- `scheduling.volcano.sh/v1beta1` `Queue`: tenant and resource governance abstraction with guarantee, deserved, weight, capability, priority, reclaimable, parent, and state fields.
- `scheduling.volcano.sh/v1beta1` `PodGroup`: gang-scheduling abstraction that groups strongly associated pods and declares `minMember`, `minResources`, priority, queue, phase, and conditions.

##### Describe the project defaults

Important defaults include:

- Components are installed into the `volcano-system` namespace by default.
- The scheduler name is `volcano`.
- If a `Job` omits `schedulerName`, Volcano documentation states that `volcano` is selected by default.
- The default scheduler configuration includes the actions `enqueue`, `allocate`, and `backfill`, and two plugin tiers: the first tier with `priority`, `gang`, and `conformance`; and the second tier with `overcommit`, `drf`, `predicates`, `proportion`, `nodeorder`, and `binpack`.
- A default queue is created when Volcano starts. Workloads that do not specify a queue are assigned to the `default` queue.
- A root queue is created for hierarchical queue support.

##### Outline any additional configurations from default to make reasonable use of the project

Production deployments should consider:

- In a large-scale cluster, administrators can adjust kube-api-qps and kube-api-burst for the Volcano scheduler, controller-manager, and other components.
- Pinning a release version rather than installing from `master`.
- Setting component resource requests and limits based on cluster scale.
- Configuring scheduler actions and plugin tiers for the target workload profile.
- Configuring `Queue` resources for tenant quotas, weights, capabilities, priorities, and hierarchy.
- Setting workload `schedulerName`, `queue`, `priorityClassName`, `minAvailable`, and `minResources` appropriately.
- Tuning controller worker threads, admission webhook timeout, and API server capacity for large-scale workloads.
- Enabling metrics scraping and dashboards.
- Reviewing RBAC and namespace isolation.

##### Describe any new or changed API types and calls - including to cloud providers - that will result from this project being enabled and used

Enabling Volcano installs a set of Custom Resource Definitions (CRDs) and supporting Kubernetes resources in the cluster. The API types are defined in the [volcano-sh/apis](https://github.com/volcano-sh/apis) repository and installed from the chart CRD bases. The added API groups and kinds include:

- `batch.volcano.sh/v1alpha1`: `Job` and `CronJob`.
- `scheduling.volcano.sh/v1beta1`: `Queue` and `PodGroup`.
- `bus.volcano.sh/v1alpha1`: `Command`.
- `nodeinfo.volcano.sh/v1alpha1`: `Numatopology`.
- `topology.volcano.sh/v1alpha1`: `HyperNode`.
- `config.volcano.sh/v1alpha1`: `ColocationConfiguration`.
- `shard.volcano.sh/v1alpha1`: `NodeShard`.

Additional CRDs such as `JobFlow` and `JobTemplate` in `flow.volcano.sh` are available through related subprojects and optional installation paths.

How API fields are defined and changed:

- **Go types are the source of truth.** Each kind is backed by Go structs in `volcano-sh/apis`. The CRD OpenAPI v3 structural schemas, deepcopy functions, and (where applicable) conversion functions are generated from these structs with `controller-gen` and code generators, rather than written by hand.
- **Internal hub plus served versions.** The `scheduling` group keeps an internal "hub" version (`pkg/apis/scheduling/types.go`) alongside the externally served `v1beta1` version (`pkg/apis/scheduling/v1beta1/types.go`), with generated conversion code (`zz_generated.conversion.go`). This hub-and-spoke pattern lets the internal representation evolve while the served API surface stays stable.
- **Backward-compatible field evolution.** Field changes between releases are predominantly additive: new fields are introduced as optional with safe defaults, so existing objects remain valid. Defaulting and validation for these fields are applied by the admission webhooks and the generated CRD schema.
- **Version lifecycle.** API maturity is expressed through Kubernetes-style version strings (`v1alpha1`, `v1beta1`). Disruptive changes are proposed publicly, surfaced in release notes and changelogs, and staged through the release process before any served version is changed or removed.

Volcano does not require calls to cloud provider APIs for core scheduling. It interacts with the Kubernetes API server to watch, list, create, update, validate, mutate, and bind Kubernetes resources and Volcano CRDs. Framework integrations and user workloads may interact with cloud services independently of Volcano.

##### Describe compatibility of any new or changed APIs with API servers, including the Kubernetes API server

- All Volcano CRDs are implemented using Kubernetes Custom Resource Definitions and are fully compatible with the Kubernetes API server.
- These CRDs follow Kubernetes API conventions for resource creation, update, deletion, and status reporting, and can be managed using standard Kubernetes tools (kubectl, client libraries, etc.).
- Volcano CRDs are versioned and validated using OpenAPI schemas, ensuring compatibility with Kubernetes admission controllers and API server validation mechanisms.
- No changes are made to existing Kubernetes APIs; Volcano only extends the API surface by adding new resource types.

##### Describe versioning of any new or changed APIs, including how breaking changes are handled

- Volcano CRDs use Kubernetes API versioning conventions, such as v1alpha1 and v1beta1 in their API group.
- New features and changes are introduced in alpha or beta versions before being promoted to stable (v1).
- Conversion webhooks are provided to support seamless migration between CRD versions when breaking changes are introduced.
- Deprecated fields and versions are announced in release notes and documentation, and are supported for a deprecation period before removal.
- Backward compatibility is maintained for stable APIs, and breaking changes are only introduced in new major or beta versions, following Kubernetes best practices.

##### Describe the project’s release processes, including major, minor and patch releases.

- Follows a structured release process for major, minor, and patch releases.
- Each release includes versioning, release notes, and changelogs to communicate new features, bug fixes, and deprecations.
- Release candidates are published for community testing before final releases.
- The process includes automated CI/CD checks, validation, and artifact publishing to container registries and GitHub artifacts.
- Deprecated features and APIs are maintained for a deprecation period before removal.
- See [Volcano Releases](https://github.com/volcano-sh/community/blob/master/version-release.md) for detailed release processes.

### Installation

#### Describe how the project is installed and initialized, e.g. a minimal install with a few lines of code or does it require more complex integration and configuration?

Installation is documented in [Installation](https://github.com/volcano-sh/website/blob/master/docs/GettingStarted/Installation.md) and the Volcano README. Supported modes include:

- **YAML manifests:** Apply the Volcano installation manifest to an existing cluster.
- **Helm:** Add the Volcano Helm repository and install the `volcano` chart into the `volcano-system` namespace.
- **From source / local development:** Run `./hack/local-up-volcano.sh` for a local development setup.

A minimal install can be a few commands, but production usage requires configuration of queues, plugins, resource requests/limits, observability, RBAC review, and workload-specific settings.

#### How does an adopter test and validate the installation?

- Each of the installation guides mentioned above includes validation steps.
- Checking `kubectl get all -n volcano-system` and verifying `volcano-admission`, `volcano-controllers`, `volcano-scheduler`, and the admission init job are healthy.
- Verifying CRDs are installed and API resources are discoverable.
- Submitting a small `Job` or a pod with `schedulerName: volcano`.
- Confirming a `PodGroup` is created where applicable and transitions through expected states.
- Scraping metrics and confirming scheduler/controller metrics are present.
- Running e2e examples or framework integrations relevant to the adopter's workload.

### Security

#### Please provide a link to the project’s cloud native security self assessment.

Volcano's security self-assessment is originally published at: https://github.com/cncf/tag-security/blob/main/community/assessments/projects/volcano/self-assessment.md

#### Please review the Cloud Native Security Tenets from TAG Security.

##### How are you satisfying the tenets of cloud native security projects?

- Security-sensitive changes are reviewed through public PRs, design discussions, CI, and maintainer review.
- Volcano relies on Kubernetes RBAC, ServiceAccounts, admission TLS, namespace isolation, and standard cluster security controls.
- Volcano inherits mature security mechanisms from Kubernetes, Go, TLS, container runtimes, and standard cluster operations.
- Private disclosure, distributor notifications, release, and public communication are well documented.

##### How do you recommend users alter security defaults in order to "loosen" the security of the project? Please link to any documentation the project has written concerning these use cases.

The project should not recommend loosening security in production. For development or testing, users may choose to:

- Run a local development installation with `./hack/local-up-volcano.sh`.
- Adjust any admission fail policy from `fail` to `ignore`.
- Generally Volcano does not require privilege. But when it comes to supporting colocation, the `volcano-agent` component needs some elevated permissions, which can be set via Helm args.

#### Security Hygiene

##### Please describe the frameworks, practices and procedures the project uses to maintain the basic health and security of the project.

Volcano maintains project health and security through:

- Pull-request-based development with code review.
- GitHub branch protection and OWNERS-based approval workflows.
- CI workflows for code verification, generated files, linting, unit tests, and e2e tests.
- License linting.
- FOSSA dependency/license analysis.
- Dependabot weekly updates for Go modules and GitHub Actions.
- Security reporting and coordinated disclosure process.
- A documented Product Security Team and fix lead process.
- Third-party security audit.
- Release branches, patch releases, and security release process.
- Transparent Governance: The project practices open governance with regular public meetings and community channels for raising and discussing security or health concerns.

##### Describe how the project has evaluated which features will be a security risk to users if they are not maintained by the project?

- Admission webhook validation and mutation.
- RBAC manifests and component ServiceAccount permissions.
- Scheduler plugins and algorithms that can affect tenant isolation, priority, preemption, and quota enforcement.
- Queue and PodGroup APIs that govern workload placement and resource sharing.
- GPU/NPU/device scheduling paths that affect tenant isolation and device allocation.
- Dependency updates and Kubernetes compatibility.
- Security release and vulnerability response processes.

The project evaluates these risks through public issue/PR review, maintainer responsibility, CI, dependency scanning, community feedback, security self-assessment, third-party audit findings, and production adopter experience.

#### Cloud Native Threat Modeling

##### Explain the least minimal privileges required by the project and reasons for additional privileges.

Volcano components require Kubernetes API permissions needed to watch and reconcile scheduling-related resources:

- Scheduler permissions to watch Pods, Nodes, PodGroups, Queues, Jobs, and related resources, and to bind or update scheduling-related state.
- Controller-manager permissions to create, update, and delete Volcano-managed resources and update statuses.
- Admission permissions to validate/mutate configured resources through Kubernetes admission webhooks.
- Access to ConfigMaps, Secrets, Services, and related installation resources necessary for component configuration and webhook operation.

Additional privileges are tied to optional features, framework integrations, device scheduling, or cluster-scoped queue/scheduling behavior. The project should continue to review RBAC for least privilege as APIs evolve.

##### Describe how the project is handling certificate rotation and mitigates any issues with certificates.

- When installing Volcano, users can either customize certificates or use the certificates automatically generated by volcano admission init job.
- When generating certificates through Volcano, the validity period of the certificates by default is 10 years.
- These certificates are stored in Kubernetes Secrets, and are manually provisioned and rotated by cluster administrators.

##### Describe how the project is following and implementing secure software supply chain best practices.

- Automated Testing and CI/CD Integration: Volcano integrates unit tests and end-to-end tests within its CI/CD pipeline. This ensures that any changes are validated early, reducing the risk of introducing vulnerabilities.
- Vulnerability Scanning: The project employs vulnerability scanning tools such as trivy, dependabot and gosec to identify and address known security issues in dependencies.
- Use of Lock Files and SBOM Generation: Volcano utilizes dependency lock files (e.g., go.mod) to ensure reproducibility. Automated generation of Software Bill of Materials (SBOMs) is now integrated into the CI/CD pipeline for all container images and components. This enhances transparency of software components and supports supply chain security.
- DCO Check: Committers are required to sign and comply with the Developer Certificate of Origin (DCO) to affirm the legitimacy and authorship of their contributions.
- Branch Protection: The project enforces branch protection rules to prevent unauthorized changes, enforce status checks, require pull request reviews, and control who can push to protected branches.
- License compliance: Automated license compliance checks are now integrated into the CI/CD pipeline. All dependencies are scanned and validated for license compatibility as part of every pull request and release build, ensuring transparency and legal compliance.
- Peer Review: Commits and builds are validated through peer-reviewed pull request workflows, requiring approval before merge.

## Day 1 - Installation and Deployment Phase

### Project Installation and Configuration

#### Describe what project installation and configuration look like.

A typical installation creates the `volcano-system` namespace and installs:

- `volcano-scheduler`
- `volcano-controllers`
- `volcano-admission`
- `volcano-admission-init` job
- `volcano-admission-service`
- Volcano CRDs
- RBAC, ServiceAccounts, ConfigMaps, and webhook configurations

Configuration includes:

- Scheduler actions and plugin tiers in `volcano-scheduler-configmap`.

### Project Enablement and Rollback

#### How can this project be enabled or disabled in a live cluster? Please describe any downtime required of the control plane or nodes.

Volcano can be enabled in a live Kubernetes cluster by installing the components and CRDs. No Kubernetes control-plane or node downtime is expected for installation. Existing workloads continue to use their current scheduler unless explicitly configured to use Volcano.

To use Volcano, adopters opt in by:

- Submitting `Job` resources.
- Setting `schedulerName: volcano` on pods or framework-generated workloads.
- Creating `Queue` resources and assigning workloads to queues.

To disable Volcano:

- Stop submitting new workloads that use Volcano.
- Change future workloads to another scheduler where appropriate.
- Wait for or migrate existing Volcano-managed workloads.
- Uninstall Helm release or delete manifests.
- Remove CRDs only after confirming no needed Volcano custom resources remain.

#### Describe how enabling the project changes any default behavior of the cluster or running workloads.

Installing Volcano adds CRDs, admission webhooks, components, RBAC, and an additional scheduler. It does not influence the default Kubernetes scheduler. Existing workloads are not affected unless they are configured explicitly to use `schedulerName: volcano` or Volcano-specific APIs.

Note: if both default kube-scheduler and volcano scheduler are used simultaneously, there may be interactions or conflicts depending on workload configuration and scheduling policies.

#### Describe how the project tests enablement and disablement.

Volcano uses CI workflows to run a suite of e2e tests before a PR is merged (see https://github.com/volcano-sh/volcano/tree/master/.github/workflows), which covers job management, scheduling, and other core functionalities.

#### How does the project clean up any resources created, including CRDs?

Cleanup depends on the installation method:

- **Helm:** Use `helm uninstall` for Helm-managed resources.
- **YAML manifests:** Delete the applied manifests and related namespace resources.
- **Local development:** Use the corresponding cleanup path from the local setup scripts.

Operators should remove workload custom resources before deleting CRDs. Deleting CRDs removes all instances of those custom resources. The `volcano-system` namespace can be removed after workloads and cluster-scoped resources are cleaned up. Optional monitoring, dashboard, and subproject components should be uninstalled separately.

### Rollout, Upgrade and Rollback Planning

#### How does the project intend to provide and maintain compatibility with infrastructure and orchestration management tools like Kubernetes and with what frequency?

Volcano has a defined compatibility matrix: https://github.com/volcano-sh/volcano#kubernetes-compatibility

In addition, Volcano checks the compatibility between the maintained versions and Kubernetes when any new release is planned.

#### Describe how the project handles rollback procedures.

Rollback depends on the installation method:

- **Helm:** Use `helm rollback` to return to a previous release revision.
- **YAML manifests:** Re-apply a previous tagged release manifest.
- **Source/local:** Check out a previous release and rerun the relevant setup path.

#### How can a rollout or rollback fail? Describe any impact to already running workloads.

Rollout or rollback can fail due to:

- Kubernetes version incompatibility.
- CRD schema/version mismatch.
- Incompatibility when some configuration API does not support forward compatibility.
- Misconfigured scheduler actions/plugins.

Already running pods generally continue running. Impact is primarily to new scheduling, job lifecycle reconciliation, queue updates, admission of new or updated resources, and framework submissions during the failure.

#### Describe any specific metrics that should inform a rollback.

Rollback should be considered when installation or upgrade causes sustained degradation in:

- Component readiness or restart counts.
- Scheduling high latency and low throughput.
- Job and task scheduling latency.
- Unscheduled task or unscheduled job counts.
- Queue pending/inqueue/running counts.
- API server errors related to Volcano resources.
- Spike in workload failures after upgrade.
- Component CPU/memory saturation.
- Error logs in scheduler, controller-manager, or admission.

Relevant Volcano metrics are documented in [metrics.md](https://github.com/volcano-sh/volcano/blob/d8dcf154bcb3f1a378374f95cf2460cfcda7663d/docs/design/metrics.md).

#### Explain how upgrades and rollbacks were tested and how the upgrade->downgrade->upgrade path was tested.

Volcano validates releases through CI workflows, and community beta testing. The documented release process includes code freeze, alpha/beta releases, user/community beta testing, and official release publication.

For a specific production environment, adopters should run explicit upgrade, downgrade, and re-upgrade tests in staging using their installation method, workload mix, CRDs, and scheduler configuration. The project should continue expanding automated upgrade/downgrade coverage and documenting tested paths for each release.

#### Explain how the project informs users of deprecations and removals of features and APIs.

All API changes are backward compatible which are announced in release notes and in the official website.

- GitHub [release notes](https://github.com/volcano-sh/volcano/releases).
- Public issues and PRs.
- Community meetings and mailing list discussions.
- Documentation updates on the website and repository.

#### Explain how the project permits utilization of alpha and beta capabilities as part of a rollout.

Volcano uses Kubernetes-style API versions and release stages. Alpha and beta releases may be published during release freeze, and some APIs use alpha/beta API version strings. Users can adopt these capabilities explicitly by installing the relevant release, enabling corresponding feature configuration, and submitting resources that use those APIs.

Production users should treat alpha and beta capabilities as opt-in, test them in staging, monitor them closely, and plan for potential API changes before stable graduation.

## Day 2 - Day-to-Day Operations Phase

### Scalability/Reliability

#### Describe how the project increases the size or count of existing API objects.

Using Volcano increases Kubernetes API object counts by adding:

- `Queue` objects.
- `PodGroup` objects, often one per Volcano job or workload group.
- `Job` objects when users submit jobs through Volcano's job API.
- Status updates and events for scheduling and lifecycle state.
- ConfigMaps, Services, Deployments, Jobs, and webhook configuration for the control plane.

Object growth is generally proportional to workload count, task/pod count, queue count, and enabled features.

#### Describe how the project defines Service Level Objectives (SLOs) and Service Level Indicators (SLIs).

Volcano exposes a number of [metrics](https://github.com/volcano-sh/volcano/blob/d8dcf154bcb3f1a378374f95cf2460cfcda7663d/docs/design/metrics.md) that adopters can use as SLIs for their own SLOs. All metrics are prefixed with `volcano_`.

Useful SLIs include:

- End-to-end scheduling session latency (`volcano_e2e_scheduling_latency_milliseconds`) and session open duration (`volcano_open_session_duration_milliseconds`).
- End-to-end job scheduling latency (`volcano_e2e_job_scheduling_latency_milliseconds`, `volcano_e2e_job_scheduling_duration`).
- Action and plugin scheduling latency (`volcano_action_scheduling_latency_milliseconds`, `volcano_plugin_scheduling_latency_milliseconds`).
- Task scheduling latency by stage (`volcano_task_scheduling_latency_milliseconds`, `volcano_scheduling_stage_duration_milliseconds`).
- Controller job-to-pod creation latency (`volcano_controller_job_to_pod_creation_latency_milliseconds`).
- Unscheduled task and job counts (`volcano_unschedule_task_count`, `volcano_unschedule_job_counts`).
- Queue PodGroup state counts (`volcano_queue_pod_group_pending_count`, `volcano_queue_pod_group_inqueue_count`, `volcano_queue_pod_group_running_count`, `volcano_queue_pod_group_unknown_count`).

#### Describe any operations that will increase in time covered by existing SLIs/SLOs.

The operations most likely to see increased latency under existing SLIs/SLOs are scheduling. In general, these operations become slower as the number of workload objects increases.

#### Describe the increase in resource usage in any components as a result of enabling this project, to include CPU, Memory, Storage, Throughput.

Enabling Volcano increases resource usage mainly in:

- **Volcano scheduler:** CPU and memory for scheduling cycles, caches, plugin logic, and node/job scoring.
- **Controller manager:** CPU and memory for reconciling jobs, queues, pod groups, and pods.
- **Admission:** CPU, memory, and network throughput for webhook validation and mutation.
- **Kubernetes API server/etcd:** Increased throughput and storage for CRDs, pods, events, status, and watch traffic.

The increase depends on workload scale and plugin configuration.

#### Describe which conditions enabling / using this project would result in resource exhaustion of some node resources (PIDs, sockets, inodes, etc.)

Possible resource-exhaustion conditions include:

- Very high pod creation rates causing admission webhook or API server saturation, which may need to increase the Linux socket file descriptor (FD) limit.
- Large scheduler caches causing memory pressure.


#### Describe the load testing that has been performed on the project and the results.

Volcano has published large-scale performance and tuning guidance in [How to Tune Volcano Performance in Large-Scale Scenarios](https://github.com/volcano-sh/website/blob/9f0409c161df8eed6439d06cbf73580797d21055/docs/UserGuide/user_guide_how_to_tune_volcano_performance.md). Testing used an extended `kube-scheduling-perf` framework, API server audit logs, and cumulative pod create/schedule metrics.

Key findings:

- Performance is scenario-dependent.
- When gang scheduling is enabled, Volcano's performance exceeds other schedulers in the tested batch scenarios, validating Volcano's core workload focus.
- Admission webhook timeout can become a bottleneck under large-scale, resource-constrained pod creation.
- Controller worker-thread count must be tuned; higher is not always better.
- API server/etcd contention between pod creation and scheduling can create visible stalls.
- Adequate resources and tuning are necessary for large production clusters.

#### Describe the recommended limits of users, requests, system resources, etc. and how they were obtained.

Recommended limits are workload- and cluster-specific. Volcano does not publish a single hard maximum for users, jobs, pods, queues, or requests. Instead, adopters should derive limits from:

- Published performance tuning guidance.
- Staging load tests using their workload shape.
- Kubernetes API server and etcd capacity.
- Scheduler and controller-manager resource usage.
- Admission webhook latency and error rates.
- Prometheus metrics cardinality and retention.
- Queue and tenant resource policies.

For large-scale scenarios, operators should tune component resources, admission timeouts, worker threads, scheduler configuration, and API server capacity based on measured results.

#### Describe which resilience pattern the project uses and how, including the circuit breaker pattern.

Volcano uses Kubernetes-native resilience patterns:

- **Reconciliation:** Controllers continuously reconcile desired and observed state.
- **Self-healing:** Kubernetes restarts failed component pods.
- **Idempotency:** Scheduling and controller operations are designed around observed resource state.
- **Backoff/retry:** Scheduler retries transient errors and pending workload.
- **Preemption/reclaim/backfill:** Scheduling actions improve resource utilization and restore fairness under contention.
- **Gang semantics:** Prevents partial startup of workloads that require a minimum runnable set.
- **Admission validation:** Rejects invalid resource configuration before it enters the system.

### Observability Requirements

#### Describe the signals the project is using or producing, including logs, metrics, profiles and traces. Please include supported formats, recommended configurations and data storage.

Volcano produces:

- **Metrics:** Prometheus-style metrics prefixed with `volcano_`, including scheduler latency, plugin/action latency, job scheduling latency, task stage latency, queue resource metrics, unscheduled counts, preemption metrics, controller latency, and Go runtime metrics.
- **Logs:** Component logs from scheduler, controller-manager, admission, and related pods.
- **Kubernetes events:** Scheduling and lifecycle information for jobs, pod groups, pods, and queues.
- **CRD status:** `Job`, `PodGroup`, and `Queue` status fields and conditions.

#### Describe how the project captures audit logging.

Volcano relies on Kubernetes audit logging for API-level audit records. Cluster administrators can enable Kubernetes audit policy to capture creation, updates, deletes, admissions, and status changes for Volcano CRDs and related pods.

Volcano component logs and Kubernetes events provide additional operational traces but are not a replacement for Kubernetes audit logs.

#### Describe any dashboards the project uses or implements as well as any dashboard requirements.

Volcano provides optional dashboard and monitoring integrations:

- [Volcano Dashboard](https://github.com/volcano-sh/dashboard) for web UI.
- Monitoring manifests in the Volcano repository for Prometheus/Grafana deployment.

#### Describe how the project surfaces project resource requirements for adopters to monitor cloud and infrastructure costs, e.g. FinOps.

Volcano does not implement a dedicated FinOps product. It surfaces resource signals that adopters can combine with their cost-management tools:

- Queue allocated/requested/deserved/capacity CPU, memory, and scalar resources.
- Queue weights, shares, overuse, and PodGroup state counts.
- Job and task scheduling metrics.
- Component CPU/memory usage.
- Accelerator resource usage through Kubernetes and device plugin integrations.

#### Which parameters is the project covering to ensure the health of the application/service and its workloads?

- Component readiness and liveness.
- Component restart count and pod status.
- Admission webhook latency/errors/timeouts.
- Scheduling latency and session duration.
- Queue pending/inqueue/running/unknown PodGroup counts.
- Unscheduled job/task counts.
- Job phase counts and retry counts.
- Preemption attempts and victims.
- Queue allocated/requested/deserved/capacity resources.
- API server errors for Volcano resources.
- Framework workload success/failure metrics.

#### How can an operator determine if the project is in use by workloads?

Operators can check:

- Pods with `schedulerName: volcano`.
- Existing `Job` resources.
- Existing `PodGroup` resources and owner references.
- Existing non-default `Queue` resources and queue allocation metrics.
- Scheduler metrics showing active scheduling sessions and job/task latency.
- Kubernetes events emitted by Volcano.
- Framework-created resources that reference Volcano scheduling.

#### How can someone using this project know that it is working for their instance?

A user can verify Volcano is working by:

- Confirming components are ready in `volcano-system`.
- Submitting a sample `Job`.
- Checking that the job's `PodGroup` is created and transitions to expected states.
- Confirming pods are bound to nodes by the Volcano scheduler.
- Verifying job phase transitions to running/completed or expected failure state.
- Checking events for scheduling decisions.
- Checking metrics for scheduler activity and successful scheduling latency.
- Running a framework integration test, such as Spark or PyTorch, where applicable.

#### Describe the SLOs (Service Level Objectives) for this project.

Volcano exposes metrics for adopters to define SLOs, but project-wide public SLO targets are currently best treated as environment-specific. Recommended adopter SLO areas include:

- Job scheduling latency, P99 latency should be <= 1 second over the last 5 minutes.


#### What are the SLIs (Service Level Indicators) an operator can use to determine the health of the service?

Important SLIs include:

| SLI | Example metric/source | Purpose |
| --- | --- | --- |
| Component availability | Kubernetes pod readiness/restarts | Confirms control-plane health |
| Scheduling session latency | `volcano_e2e_scheduling_latency_milliseconds` | Measures scheduling loop duration |
| Job scheduling latency | `volcano_e2e_job_scheduling_latency_milliseconds` / `volcano_e2e_job_scheduling_duration` | Measures job startup scheduling time |
| Action/plugin latency | `volcano_action_scheduling_latency_milliseconds`, `volcano_plugin_scheduling_latency_milliseconds` | Identifies scheduler bottlenecks |
| Task stage latency | `volcano_task_scheduling_latency_milliseconds` | Measures predicate/scoring/bind stages |
| Unscheduled workload count | `volcano_unschedule_task_count`, `volcano_unschedule_job_count` | Indicates scheduling failures or resource scarcity |
| Queue resource state | queue allocated/request/deserved/capacity metrics | Indicates tenant resource health |
| Queue workload state | queue PodGroup pending/inqueue/running/unknown metrics | Indicates queue backlog and progression |
| Admission health | webhook errors/timeouts and Kubernetes API metrics | Indicates admission bottlenecks |
| Controller latency | `volcano_controller_job_to_pod_creation_latency_milliseconds` | Measures job-to-pod creation delay |

### Dependencies

#### Describe the specific running services the project depends on in the cluster.

Mandatory services:

- Kubernetes API server.
- Kubernetes etcd through the API server.
- Kubernetes scheduler framework and pod binding mechanisms.
- In-cluster DNS/networking.
- Admission webhook service routing.

Optional services:

- Prometheus and Grafana.
- Volcano Dashboard.
- Device plugins and accelerator runtime services.
- External logging and tracing systems.
- Volcano subprojects for descheduling, multi-cluster, resource export, or dashboard functions.

#### Describe the project’s dependency lifecycle policy.

Volcano manages dependencies through:

- Go modules and `go.sum`.
- Dependabot weekly updates for Go modules and GitHub Actions.
- Kubernetes dependency updates aligned with supported Kubernetes versions.
- FOSSA and license scanning.
- CI verification and e2e testing before dependency changes merge.
- Release branches and patch releases for important fixes.
- Security process for vulnerability-driven updates.

#### How does the project incorporate and consider source composition analysis as part of its development and security hygiene? Describe how this source composition analysis (SCA) is tracked.

Volcano incorporates SCA through:

- FOSSA analysis in GitHub Actions.
- License linting workflows.
- Dependabot dependency update PRs.
- CodeQL and OpenSSF Scorecard signals.
- Go module metadata (`go.mod` and `go.sum`).
- Review of new dependencies during PR review.

Tracking occurs through GitHub Actions results, Dependabot PRs, release notes, security advisories where applicable, and repository dependency metadata.

#### Describe how the project implements changes based on source composition analysis (SCA) and the timescale.

SCA-driven changes are implemented through normal PR workflows. Routine dependency updates are handled continuously and weekly where Dependabot is configured. Security-related dependency updates are prioritized according to severity and may be released through patch or security releases using the documented security process.

### Troubleshooting

#### How does this project recover if a key component or feature becomes unavailable? e.g Kubernetes API server, etcd, database, leader node, etc.

Recovery behavior:

- **Scheduler unavailable:** Already running workloads continue, but new Volcano scheduling is delayed until the scheduler recovers.
- **Controller manager unavailable:** Existing pods continue, but job lifecycle, status, and reconciliation are delayed.
- **Admission unavailable:** Creation or update of affected resources may fail or block depending on webhook configuration.
- **Kubernetes API server/etcd unavailable:** Volcano cannot observe or update resources; reconciliation resumes after the API server recovers.
- **Node unavailable:** Kubernetes marks pods and nodes accordingly; Volcano considers updated node and pod state in later scheduling cycles.
- **Monitoring unavailable:** Scheduling continues, but visibility is reduced.

#### Describe the known failure modes.

Known failure modes include:

- Admission webhook timeout, certificate failure, or overload.
- Scheduler crash, OOM, CPU starvation, or misconfiguration.
- Controller manager crash, OOM, CPU starvation, or queue/job reconciliation delay.
- Kubernetes API server/etcd contention or unavailability.
- Insufficient cluster resources for gang scheduling or `minResources`.
- Queue closed, over capacity, misconfigured, or lacking deserved/guaranteed resources.
- Plugin/action misconfiguration or inappropriate ordering.
- Device plugin or accelerator unavailability.
- Kubernetes version incompatibility.

### Compliance

#### What steps does the project take to ensure that all third-party code and components have correct and complete attribution and license notices?

Volcano uses Apache-2.0 licensing and supports license compliance through:

- Repository `LICENSE` file.
- License linting CI workflow `make lint-licenses`.
- FOSSA analysis.
- Dependency metadata in Go modules.
- Review of third-party dependencies in PRs.
- A `licenses` directory in the repository for dependency license data.

#### Describe how the project ensures alignment with CNCF recommendations for attribution notices.

##### How are notices managed for third-party code incorporated directly into the project's source files?

Direct incorporation of third-party code should preserve upstream notices and licenses. Project-owned source files should carry the Volcano/Apache-2.0 header where required. Vendored or third-party code should be kept in dedicated paths where possible to avoid overwriting upstream notices.

##### How are notices retained for unmodified third-party components included within the project's repository?

Unmodified third-party components should retain their upstream license and attribution files. License linting and FOSSA analysis help detect missing or incompatible license metadata. The repository's `licenses` directory and module metadata provide traceability for dependencies.

##### How are notices for all dependencies obtained at build time included in the project's distributed build artifacts (e.g. compiled binaries, container images)?

Volcano's build and release process should include license and dependency metadata generated by the project's license tooling. The release process publishes source, binaries/manifests, and container images. The project should continue to ensure license data and notices are packaged or referenced from release artifacts and container image metadata in alignment with CNCF attribution recommendations.

### Security

#### Security Hygiene

##### How is the project executing access control?

- Kubernetes authentication and RBAC control access to Volcano CRDs and component permissions. Components use ServiceAccounts with RBAC. Users interact through the Kubernetes API server, which enforces cluster access controls.

#### Cloud Native Threat Modeling

##### How does the project ensure its security reporting and response team is representative of its community diversity (organizational and individual)?

The Product Security Team is documented publicly and initially consists of maintainers in the private Volcano security list. Current maintainers represent multiple organizations, including NVIDIA, Huawei, Baidu, and Hjmicro. The membership ladder provides an open path for contributors from any organization to become members, reviewers, approvers, maintainers, and owners through merit-based contribution.

##### How does the project invite and rotate security reporting team members?

The security process documents that the Security Team is responsible for organizing security response. Future security team composition can evolve from all maintainers to a subset as the community grows. New maintainers join through the documented membership process and can participate in security response according to project policy and need.

## Additional Links

- [Volcano website](https://volcano.sh/)
- [Volcano repository](https://github.com/volcano-sh/volcano)
- [Volcano community repository](https://github.com/volcano-sh/community)
- [Volcano website repository](https://github.com/volcano-sh/website)
- [Volcano documentation](https://github.com/volcano-sh/website/tree/9f0409c161df8eed6439d06cbf73580797d21055/docs)
- [Installation](https://github.com/volcano-sh/website/blob/9f0409c161df8eed6439d06cbf73580797d21055/docs/GettingStarted/Installation.md)
- [Architecture](https://github.com/volcano-sh/website/blob/9f0409c161df8eed6439d06cbf73580797d21055/docs/Home/Architecture.md)
- [Scheduler overview](https://github.com/volcano-sh/website/blob/9f0409c161df8eed6439d06cbf73580797d21055/docs/Scheduler/Overview.md)
- [Job concept](https://github.com/volcano-sh/website/blob/9f0409c161df8eed6439d06cbf73580797d21055/docs/Concepts/Job.md)
- [Queue concept](https://github.com/volcano-sh/website/blob/9f0409c161df8eed6439d06cbf73580797d21055/docs/Concepts/Queue.md)
- [PodGroup concept](https://github.com/volcano-sh/website/blob/9f0409c161df8eed6439d06cbf73580797d21055/docs/Concepts/PodGroup.md)
- [Metrics design](https://github.com/volcano-sh/volcano/blob/d8dcf154bcb3f1a378374f95cf2460cfcda7663d/docs/design/metrics.md)
- [Performance tuning](https://github.com/volcano-sh/website/blob/9f0409c161df8eed6439d06cbf73580797d21055/docs/UserGuide/user_guide_how_to_tune_volcano_performance.md)
- [Governance](https://github.com/volcano-sh/community/blob/00ccf774aa4309cf45da50729ae6e2ce688ed53f/GOVERNANCE.md)
- [Community membership](https://github.com/volcano-sh/community/blob/00ccf774aa4309cf45da50729ae6e2ce688ed53f/community-membership.md)
- [Maintainers](https://github.com/volcano-sh/community/blob/00ccf774aa4309cf45da50729ae6e2ce688ed53f/MAINTAINERS.md)
- [Security process](https://github.com/volcano-sh/community/blob/00ccf774aa4309cf45da50729ae6e2ce688ed53f/SECURITY.md)
- [Product Security Team](https://github.com/volcano-sh/community/blob/00ccf774aa4309cf45da50729ae6e2ce688ed53f/PST.md)
- [Release process](https://github.com/volcano-sh/community/blob/00ccf774aa4309cf45da50729ae6e2ce688ed53f/version-release.md)
- [Adopters](https://github.com/volcano-sh/community/blob/00ccf774aa4309cf45da50729ae6e2ce688ed53f/adopters.md)
- [OpenSSF Best Practices](https://bestpractices.coreinfrastructure.org/projects/3012)
- [OpenSSF Scorecard](https://scorecard.dev/viewer/?uri=github.com/volcano-sh/volcano)
- [Volcano 2025 Security Audit](https://volcano.sh/reports/Ada-Logics-Volcano-Security-Audit-2025.pdf)
