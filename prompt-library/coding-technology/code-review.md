# Code Review & Risk Audit

## Purpose
Review supplied code or a change set for correctness, security, data handling, reliability, performance and maintainability. Report actionable findings with evidence, severity and minimal fixes; avoid speculative criticism and unnecessary rewrites.

## When to use
Use for pull requests, code changes, scripts, APIs, configuration, infrastructure definitions or targeted reviews of an existing codebase.

## Required inputs
- Code, diff or repository files to review
- Language, framework and runtime versions
- Intended behaviour and relevant requirements
- How the code is executed and deployed
- Tests and known failures
- Security, privacy and performance constraints
- Review scope and areas of concern

## Instructions
1. Confirm the review scope, changed files, intended behaviour and available context. Do not claim to have reviewed files that were not supplied or accessible.
2. Understand the execution path and relevant dependencies before judging individual lines. Trace inputs, state changes, side effects, outputs and error handling.
3. Check correctness against requirements, including boundary conditions, null/empty values, invalid input, concurrency, time zones, encoding and failure states where relevant.
4. Inspect security risks appropriate to the code: authentication, authorisation, injection, secrets, unsafe deserialisation, path handling, cryptography, dependency exposure and privilege boundaries.
5. Examine data handling: validation, privacy, logging, retention, access control, integrity, transactions and accidental disclosure.
6. Review reliability and operational behaviour: retries, timeouts, idempotency, resource cleanup, observability, rollback and graceful degradation.
7. Assess performance and scalability only where relevant evidence exists. Identify likely complexity or resource bottlenecks and distinguish measured issues from hypotheses.
8. Check maintainability: clarity, modularity, duplication, naming, API contracts, documentation and consistency with established project patterns.
9. For each finding provide severity (critical/high/medium/low), exact file and line/location where available, evidence, impact, conditions for occurrence and a minimal recommended fix.
10. Avoid reporting style preferences as defects. Do not invent vulnerabilities or claim exploitability without a plausible path.
11. Identify missing tests and propose targeted tests for high-risk paths. Do not claim tests were run unless they actually were.
12. Summarise overall risk, blockers and recommended merge decision, stating review limitations and any areas not examined.

## Expected output
- Review scope and limitations
- Executive risk summary
- Findings table: severity, location, evidence, impact and fix
- Positive observations where relevant
- Missing tests and suggested test cases
- Merge recommendation with rationale
- Follow-up questions or deeper review areas

## Quality checks
- Findings are grounded in inspected code
- Locations and reproduction conditions are precise
- Severity reflects realistic impact and likelihood
- Security concerns include a plausible attack or failure path
- Suggestions are minimal and compatible with project context
- Tests run and tests merely proposed are clearly distinguished
- Review limitations are explicit

## Source
Original prompt, informed by secure code review and software quality practices; no upstream prompt text reproduced.

## Testing notes
Scenario: Review an endpoint snippet accepting user input, with no visible authorisation check or accompanying tests. Observed: The prompt frames the missing check as a risk to validate, avoids claiming exploitability without a plausible path, and distinguishes proposed tests from tests run. Result: PASS. Limitation: A snippet-only review cannot establish whole-application security.

## Status
Tested