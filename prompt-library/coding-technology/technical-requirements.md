# Technical Requirements Clarifier

## Purpose
Translate a business or user problem into clear, testable technical requirements. Define users, workflows, system behaviour, constraints, quality attributes, acceptance criteria and the smallest viable scope without prematurely prescribing a solution.

## When to use
Use before building or changing software, integrating services, automating a workflow, commissioning development or handing requirements to a technical team.

## Required inputs
- Problem statement and desired outcome
- Users, roles and affected stakeholders
- Current process/system and pain points
- Known workflows, data and integrations
- Platform, environment and technology constraints
- Security, privacy, compliance and accessibility needs
- Performance, availability and scale expectations
- Budget, timeline and operational constraints

## Instructions
1. Restate the problem and desired outcome in user/business terms. Separate the problem from any proposed technical solution.
2. Identify user roles, permissions and relevant operating contexts. Describe each user's goals and constraints.
3. Map the current and proposed workflows, including triggers, inputs, outputs, exceptions, failure states and human hand-offs.
4. Define functional requirements as observable system behaviours. Give each requirement a unique identifier and priority.
5. Define non-functional requirements such as performance, reliability, security, privacy, accessibility, maintainability, scalability, observability and recovery. Make them measurable where possible.
6. Specify data requirements: entities, fields, sources, ownership, validation, retention, access, migration and deletion. Do not assume sensitive data is required.
7. Identify interfaces, APIs, external services, authentication, dependencies and integration failure handling.
8. Record constraints, assumptions, decisions, open questions and risks separately. Flag contradictions and missing information.
9. Define acceptance criteria for each high-priority requirement using testable conditions. Include normal, boundary, error and permission scenarios.
10. Prioritise scope into must-have, should-have, could-have and out-of-scope. Identify the smallest viable release and explicitly defer nonessential complexity.
11. Propose technical options only after requirements are clear. Compare trade-offs and identify decisions requiring an architect or security review.
12. Produce a traceability view linking user needs to requirements, acceptance tests and release scope.

## Expected output
- Problem statement and objectives
- User roles and workflow maps
- Functional requirements with IDs and priorities
- Non-functional requirements and measurable targets
- Data and integration requirements
- Security, privacy and operational constraints
- Assumptions, risks and open questions
- Prioritised MVP scope and exclusions
- Acceptance criteria and test scenarios
- Requirement-to-test traceability matrix

## Quality checks
- Requirements describe outcomes and observable behaviour
- Functional and non-functional needs are both covered
- Requirements are testable, prioritised and traceable
- Error, boundary and access-control cases are included
- Data handling and security are explicit
- Assumptions and unresolved decisions are visible
- Scope is feasible and avoids premature complexity

## Source
Original prompt, informed by software requirements engineering and product discovery practices; no upstream prompt text reproduced.

## Testing notes
Scenario: A small business requests an order-tracking system but has not specified user roles, integrations, data retention or performance targets. Observed: The prompt separates the problem from a proposed solution, identifies open questions, defines testable requirements and prioritises an MVP without prematurely selecting a technology stack. Result: PASS. Limitation: Requirements remain provisional until stakeholders confirm missing constraints.

## Status
Tested