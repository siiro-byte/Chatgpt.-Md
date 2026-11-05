# Decision Log & Review

## Purpose
Create a durable, auditable record of important decisions so teams can understand what was decided, why, on what evidence, by whom and under which conditions the decision should be revisited.

## When to use
Use for product, business, operational, technical, project, policy and resource-allocation decisions that may need to be understood or reviewed later.

## Required inputs
- Decision or question being resolved
- Date and decision owner/participants, if known
- Context, objective and constraints
- Options considered
- Evidence, data and sources
- Decision criteria and trade-offs
- Chosen option and rationale
- Risks, assumptions and implementation actions
- Review date or trigger, if known

## Instructions
1. State the decision question clearly and explain why it arose now.
2. Record the context, objective, scope, constraints and consequences of delaying or not deciding.
3. List the options genuinely considered, including the status quo where relevant. Distinguish options considered from options rejected before formal evaluation.
4. Record decision criteria and their relative importance. Include strategic fit, user/customer impact, cost, time, risk, reversibility and feasibility where relevant.
5. Summarise the evidence used, including source, date, quality and limitations. Separate facts, estimates, assumptions and opinions.
6. Document the chosen option and the reasoning that connects it to the criteria. Note material trade-offs and why alternatives were not selected.
7. Record who made or approved the decision and when only if supplied. Do not infer authority or approval from meeting attendance.
8. List implementation actions with owners, deadlines and dependencies where known. Mark missing assignments explicitly.
9. Identify risks, unintended consequences and assumptions that could invalidate the decision.
10. Define review conditions: date, milestone, metric threshold, new evidence or external event that should trigger reconsideration.
11. Record the expected outcome and how it will be evaluated. Avoid inventing targets not agreed by the decision owner.
12. When reviewing an old decision, compare actual outcomes with expectations and record whether to maintain, adapt or reverse it. Preserve the original entry and add a dated review note rather than silently rewriting history.

## Expected output
- Decision ID/title and date
- Decision question and context
- Objective, constraints and criteria
- Options considered
- Evidence and assumptions register
- Decision, rationale and trade-offs
- Decision owner/approval status
- Actions, owners and deadlines
- Risks and invalidating assumptions
- Review trigger and success measures
- Dated review history, when applicable

## Quality checks
- Decision and scope are unambiguous
- Evidence is dated and traceable
- Assumptions and opinions are not presented as facts
- Options and trade-offs are documented fairly
- Approval and ownership are not inferred
- Review triggers are observable
- Historical changes preserve an audit trail

## Source
Original prompt, informed by decision-recording and organisational learning practices; no upstream prompt text reproduced.

## Testing notes
Scenario: A team discusses selecting a software vendor, but notes omit the approver, decision date and review trigger. Observed: The prompt records options and evidence while marking approval, date and review trigger unknown; it does not infer authority from attendance. Result: PASS. Limitation: The log is not an approval record until the decision owner confirms it.

## Status
Tested