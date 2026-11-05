# Practical Solution Architecture

## Purpose
Design the simplest maintainable architecture that satisfies validated requirements and operational constraints. Explain components, boundaries, data flows, security, failure handling, deployment, trade-offs and phased verification.

## When to use
Use when designing a new application or service, integrating systems, modernising a platform, scaling an existing solution or evaluating architectural alternatives.

## Required inputs
- Business problem and validated requirements
- Users, workflows and expected system behaviour
- Expected scale, performance and availability needs
- Data types, sensitivity, ownership and lifecycle
- Existing systems, APIs and technology constraints
- Security, privacy, compliance and operational requirements
- Team capabilities, budget and delivery timeline
- Deployment environment and maintenance expectations

## Instructions
1. Restate the problem, architecture scope and success criteria. Distinguish confirmed requirements from assumptions.
2. Identify system actors, external dependencies, trust boundaries and major workflows.
3. Define the quality attributes that matter most, such as reliability, latency, scalability, security, privacy, cost, maintainability and portability. Rank trade-offs explicitly.
4. Propose a high-level architecture using the fewest components that meet the requirements. Explain each component's responsibility and why it exists.
5. Describe key data flows, APIs, protocols, state ownership, persistence, event handling and integration contracts.
6. Define data architecture: entities, storage choices, consistency needs, retention, backup, migration and deletion. Minimise sensitive data and restrict access.
7. Map security controls across identity, authentication, authorisation, secrets, encryption, network boundaries, audit logging and dependency management. Flag areas needing specialist review.
8. Analyse failure modes: component outage, network interruption, partial writes, retries, duplicate events, queue backlog, dependency limits and data corruption. Define timeouts, idempotency, recovery and graceful degradation.
9. Address deployment and operations: environments, configuration, CI/CD, observability, alerting, capacity, backup/restore, incident response and rollback.
10. Compare viable alternatives using consistent criteria. Explain costs, complexity, lock-in, operational burden and what evidence would justify a different choice.
11. Define an incremental implementation sequence with dependencies, milestones and verification gates. Start with the smallest viable architecture; defer speculative complexity.
12. Provide architecture risks, open decisions and a validation plan using prototypes, load tests, threat modelling or operational exercises as appropriate.

## Expected output
- Architecture objectives and constraints
- Context and component diagram (text or Mermaid when useful)
- Component responsibilities and interfaces
- Data flows and storage model
- Security and privacy controls
- Failure modes and recovery strategy
- Deployment and operational model
- Alternatives and trade-off comparison
- Phased implementation plan
- Risks, open decisions and verification plan

## Quality checks
- Every component supports a stated requirement
- Complexity is proportionate to current scale and risk
- Data ownership and trust boundaries are clear
- Security, privacy and failure recovery are addressed
- Operational costs and team capabilities are considered
- Alternatives are compared consistently
- Assumptions and unresolved decisions are explicit
- Architecture can be tested incrementally

## Source
Original prompt, informed by practical software architecture and reliability engineering practices; no upstream prompt text reproduced.

## Testing notes
Scenario: Design a low-volume booking service handling personal data, maintained by a small team with a limited budget. Observed: The prompt favours a proportionate architecture, covers data minimisation, access controls, failure handling and operating burden, and avoids assuming enterprise scale. Result: PASS. Limitation: Compliance, threat modelling and load requirements need deployment-specific review.

## Status
Tested