# Systematic Debugging

## Purpose
Diagnose software defects through evidence-led hypothesis testing. Reproduce the issue, isolate its cause, apply the smallest safe correction and verify the result without claiming a fix that has not been tested.

## When to use
Use for errors, crashes, incorrect output, performance regressions, integration failures, intermittent behaviour, deployment problems and unexpected system behaviour.

## Required inputs
- Expected and actual behaviour
- Exact error messages, logs or screenshots
- Steps to reproduce and frequency
- Relevant code, configuration and recent changes
- Runtime, environment and dependency versions
- Tests already performed and their results
- Impact, urgency and rollback constraints

## Instructions
1. Restate the defect as expected behaviour versus observed behaviour. Identify affected users, environment, scope and severity.
2. Gather reproducible evidence: exact steps, inputs, outputs, logs, timestamps, versions and environmental conditions. Separate observations from interpretations.
3. Check whether the issue is reproducible. If intermittent, identify frequency, triggering conditions and what evidence is available when it occurs.
4. Establish a baseline and inspect recent changes, dependencies, configuration, data changes and external service status that could plausibly explain the regression.
5. Trace the failing path from input through relevant components to the observed output. Identify the earliest point where actual behaviour diverges from expected behaviour.
6. Generate a short ranked list of hypotheses. For each, state supporting evidence, contradicting evidence and a test that would distinguish it from alternatives.
7. Design the smallest safe diagnostic test. Change one variable at a time, preserve the original state and avoid destructive actions in production.
8. Run or propose targeted tests for the suspected cause. Clearly distinguish tests actually executed from commands the user should run.
9. Identify root cause only when evidence supports it. If not proven, label it the leading hypothesis and state what would confirm it.
10. Propose the minimal correction and explain why it addresses the cause rather than masking the symptom. Consider regression and security implications.
11. Define verification: reproduce the original failure, run relevant unit/integration/regression tests and check adjacent behaviour.
12. Provide rollback or mitigation steps for high-impact changes. Record remaining uncertainty and monitoring needed after deployment.

## Expected output
- Defect statement and impact
- Reproduction steps and environment
- Evidence collected and timeline
- Ranked hypotheses with discriminating tests
- Root cause or current leading hypothesis
- Minimal fix or safe next diagnostic step
- Verification plan and actual test results
- Rollback/mitigation and remaining risks

## Quality checks
- Expected and actual behaviour are precise
- Evidence is separated from assumptions
- Tests isolate hypotheses and avoid unnecessary changes
- Root cause is not asserted prematurely
- Production safety and data preservation are considered
- Fix is verified against the original reproduction
- Tests run versus tests proposed are explicit
- Remaining uncertainty and rollback needs are stated

## Source
Original prompt, informed by scientific debugging and software incident diagnosis practices; no upstream prompt text reproduced.

## Testing notes
Scenario: An API intermittently returns HTTP 500 after a deployment; logs are incomplete and rollback is available. Observed: The prompt separates observations from hypotheses, ranks discriminating tests, avoids declaring an unproven root cause and includes safe rollback and verification steps. Result: PASS. Limitation: Root cause remains unknown until logs and reproduction evidence are examined.

## Status
Tested