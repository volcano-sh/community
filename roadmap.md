# Volcano 2026 Roadmap

See also [Volcano Technical Roadmap for 2026 and Beyond](https://docs.google.com/presentation/d/1B0zdtqaCKEoh3jKNDNqekJPOOO84K8Ni/edit?slide=id.p1#slide=id.p1) for technical stack view.

With the rapid growth of large models and Cloud Native AI, Kthena (inference) and agentCube (agent) joined the Volcano community in 2025. In 2026 we will deliberately expand AI-related capabilities while maintaining existing features' stability and backward compatibility.

## Volcano Scheduler

1. Pluggable Sharding Controller Strategy
   - Define standardized policy interfaces and extension points for sharding controllers.
   - Enable pluggable implementations so the community can contribute custom sharding strategies while preserving testability and compatibility.
2. Agent Scheduler (evolution + stability)
   - Current advances: predicates and nodeOrder are supported.
   - Microservice scheduling migrated from session model to Agent Scheduler framework.
   - Roadmap: progressively open additional plugin points.
   - Stability plan: isolate immature logic via feature-gate, and prioritize code quality improvements, unit/e2e coverage, and robust regression testing before enabling by default.
3. Training scenarios (AI training & elasticity)
   - Optimize job-level preemption and rebalancing both within and across queues for better fairness and responsiveness.
   - Provide elastic scheduling for distributed training (e.g., PyTorch Elastic / Gang scheduling).
   - Align training and inference resources toward unified pools, offering two operational modes: pure preemptive and scheduled preemptive to fit diverse workload requirements.
4. Big data scenarios
   - Improve scheduling for batch and streaming big-data workloads and resource-aware integration with common big-data frameworks.
   - Solicit concrete community use-cases and contributions to refine policies and operator integrations.

## Kthena

1. Workloads
   - Support for additional inference engines
     - Current runtime supports VLLM only. Phased support for additional inference engines (beginning with SGLang) will be added.
   - LeaderWorkerSet (LWS) migration support
     - LWS is widely deployed in production. Provide a clear migration path and tooling so existing LWS deployments can transition to Kthena ModelServing with minimal disruption.
2. Router
   - Open architecture and ecosystem integration
     - Adopt open, composable APIs (e.g., GIE, gateway-api-inference-extension) to enable multi-engine and multi-vendor integrations. Initial engine support: VLLM and SGLang.
   - Traffic scheduling algorithms
   - Implement session-affinity and pluggable traffic scheduling policies. Community input on additional algorithms and trade-offs is welcome.
3. AutoScaler

    Native HPA is pod-metric centric and insufficient when multiple pods form the minimum serving unit. Kthena AutoScaler supports independent scaling at group and role granularity.

   - Group and role-level scaling
   - Planned capabilities
     - Compact multi-dimensional scaling across hyperNode, node, servingGroup, and role levels.
     - Dynamic generation of configurations to meet user SLAs.
     - Research feasibility of dynamic PD ratio approaches (research discussion and experiments encouraged).
4. Further priorities
   - Fault rapid-recovery: combine Gang scheduling with network-topology awareness to enable fast intra-ServingGroup/Role pod migration.
   - Observability: define and export key component metrics (community input needed on metric priorities).
   - Fast start/stop: work with vllm and sglang communities to optimize cold-start and shutdown paths.

## AgentCube

1. Support for multiple agent frameworks
   - Provide first-class integrations with mature agent frameworks to enable diverse developer ecosystems: LangChain, AutoGen, CrewAI, LLamaIndex, Dify, Verl.
   - Expose pluggable adapters so contributors can add or optimize framework-specific behaviors.
2. AgentCube Router evolution
   - Current: basic routing.
   - Planned: authentication and authorization, tenant-level quota and concurrency controls, session persistence, and WebSocket support to enable secure, multi-tenant, low-latency agent workflows.
3. Picod expansion
   - Python support available now; plan to add Jupyter support for interactive workloads.
   - Evaluate additional language runtimes based on community business scenarios and demand.
4. SDK and runtime capabilities
   - Existing: CodeInterpreter and agentRuntime support create and invoke.
   - Roadmap: add active sandbox suspension, fast wake-up, and fault-tolerant recovery.
   - Expand SDK surface and language bindings across releases following semantic versioning.
5. AgentCube workloads and CRD strategy
   - Current: basic adaptations for agentRuntime and CodeInterpreter; need to identify richer workload requirements and real-world use cases (MCP tools, BrowserUse, MobileUse, etc.).
   - The agent-sandbox CRD is used today; the long-term core API is under community discussion, and feedback is welcome.
   - Improve warm-pool and session management (global warm-pool to reduce resident resource fragmentation, idle-time policies, and dynamic session recovery).

## Resource Management

As computer hardware diversifies, Volcano will broaden support for heterogeneous accelerators to meet evolving industry demands. In 2026 we plan to add native support for Ascend, Metax, and Cambricon, and extend unified resource management across multiple GPU generations and vendor platforms. This work enables consistent discovery, accounting, and scheduling of industry compute resources, reducing fragmentation for mixed-hardware clusters.

Key capabilities:

- Multi-vendor device support: drivers, device plugins, and CRD mappings for Ascend, Metax, Cambricon, and additional accelerators.
- Unified resource model: consistent APIs and allocation semantics across device generations and vendors to simplify scheduling and tenancy.
- Topology-aware scheduling: integrate network- and topology-awareness (e.g., NUMA, NIC/GPU locality, fabric links) to optimize placement and cross-node traffic for distributed AI workloads.
- Interoperability and extensibility: pluggable adapters and metrics exporters to enable vendor integrations and community-contributed optimizations.

## Ecosystem Integration

- Volcano Scheduler
  - Native support for Ascend, Metax, and Cambricon (including native device plugin, DRA driver, etc.).
  - Separate the HyperNode controller, promote the HyperNode API as a first-class citizen in the Kubernetes community, and establish an initiative for HyperNode.
  - Integrate network-topology-aware scheduling capabilities (including support for subgroup granularity) into more communities.
  - Support the Karmada scheduler hypernode estimator, providing network-topology-aware scheduling capabilities in multi-scheduler scenarios.
- Kthena
  - ModelServing supports LeaderWorkerSet, llm-d, and aibrix for existing users.
  - ModelServing supports MoonCake and LMCache. A user guide is currently available; next step is exploring best practices for deploying role support with kv-cache and publishing an updated guide.
  - Router supports diverse APIs such as GIR and gateway-api-inference-extension.
- AgentCube
  - Provide first-class integrations with mature agent frameworks to enable diverse developer ecosystems: LangChain, AutoGen, CrewAI, LLamaIndex, Dify, Verl.
  - Support Agent-sandbox. At this stage, agentCube uses agent-sandbox as its workload API. If agentCube transitions to its own API in the future, keep support for the agent-sandbox API.
  - Support additional programming languages, such as Jupyter and TypeScript.

