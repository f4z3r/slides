---
title: Beyond Containers
sub_title: Hands-on Polyglot Apps with wasmCloud
theme:
  path: ../assets/presenterm/theme.yaml
---

<!-- jump_to_middle -->
<!-- font_size: 2 -->
The Evolution of Architecture
===

<!--
speaker_note: |
  - Architectural background why Kubernetes came to be
-->

<!-- end_slide -->
Modular Monoliths
===

![image:width:90%](./assets/modular-monolith.excalidraw.png)

<!--
speaker_note: |
  - Complexity:
      - High entry barrier: Large code base
      - Single language: Usually one language for all functionalities
      - Upgrades are high risk: tech debt (everything needs to be redeployed)
  - Deployment:
      - Big releases: No individual deployment -> full rebuild
      - Large artifact: Extended downtime during deployment
      - Slow cycles: Reduced iteration speed
  - Operation:
      - Shared state: Difficult debugging
      - Tight coupling: High blast radius
      - Inflexible scaling: Resource waste
-->

<!-- end_slide -->
Microservices
===

![image:width:90%](./assets/microservices.excalidraw.png)

<!--
speaker_note: |
  - Microservices
  - Does not improve decoupling
  - Independent deployment
  - Every service owner of its data
  - Communication via REST
  - Complex deployment orchestration needed
-->

<!-- end_slide -->
Kubernetes
===

![image:width:40%](./assets/kubernetes-logo.png)

<!--
speaker_note: |
  - Largest ecosystem in the world:
    - K8s is a well established standard and a dominant abstraction layer.
  - Core Concept:
    - Orchestrating Containers and managing container lifecycle to ensure the cluster matches the declaratively defined state of your cluster.
  - Benefits:
    - Automates a lot around infrastructure (self-healing, scaling, etc)
  - Prime usage for integrations:
    - K8s is very extensible and benefits from a huge ecosystem (Prometheus, Grafana, etc..)

-->

<!-- end_slide -->
Kubernetes Shortcomings
===

<!-- column_layout: [1, 1] -->
<!-- column: 0 -->

## Compute Density

- Most containers contain OS
- REST servers everywhere
- Resource requests difficult

<!-- column: 1 -->

## Security

- Most containers contain OS
- Open by default

## Complexity

- AppDev needs knowhow
- No communication standard

<!-- reset_layout -->

<!--
speaker_note: |
  - ...
  - Is there a better way?
-->

<!-- end_slide -->
<!-- newlines: 2 -->

![image:width:90%](./assets/wasm.png)

<!--
speaker_note: |
  - Lightweight, secure runtime
  - Deny by default
  - Composable
-->

<!-- end_slide -->
wasmCloud
===

![image:width:90%](./assets/wasmcloud.excalidraw.png)

<!--
speaker_note: |
  - Modules contain only their own code
  - Can be independently deployed
  - Communication standardized and via wRPC
  - A way to split a modular monolith onto different hosts
  - Can be multi-lingual
  - Still rely on REST for inter app communication
-->

<!-- end_slide -->
wasmCloud
===

<!-- column_layout: [1, 1] -->
<!-- column: 0 -->

## Components

- Business logic
- KiB or MiB payloads
- Launched when needed
- Multi-lingual
- Require capabilities

## Links

- Compose entities at runtime
- Defined interfaces

<!-- column: 1 -->

## Capabilities

- Abstract interfaces
- Provide common functionality
- Independent of implementation

## Providers

- Implementation of capability
- Configurable
- Partially builtin

<!-- reset_layout -->

<!--
speaker_note: |
-->

<!-- end_slide -->
<!-- jump_to_middle -->
<!-- font_size: 3 -->
Demo
===

<!-- end_slide -->
<!-- font_size: 3 -->
Hands-On
===

<!-- jump_to_middle -->
<!-- font_size: 2 -->
<!-- alignment: center -->
github.com/f4z3r/wasmcloud-tutorial

<!--
speaker_note: |
  - Explain breaks etc
-->
