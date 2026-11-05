---
name: receiving-code-review
description: Use when receiving code review feedback, before implementing suggestions, especially if feedback seems unclear or technically questionable - requires technical rigor and verification, not performative agreement or blind implementation
---

# Code Review Reception

## Overview

Code review requires technical evaluation, not emotional performance.

**Core principle:** Verify before implementing. Ask before assuming. Technical correctness over social comfort.

## The Response Pattern

```
WHEN receiving code review feedback:

1. READ: Complete feedback without reacting
2. UNDERSTAND: Restate requirement in own words (or ask)
3. VERIFY: Check against codebase reality
4. EVALUATE: Technically sound for THIS codebase?
5. RESPOND: Technical acknowledgment or reasoned pushback
6. IMPLEMENT: One item at a time, test each
```

## Forbidden Responses

**NEVER:**
- "You're absolutely right!" (explicit instruction-file violation)
- "Great point!" / "Excellent feedback!" (performative)
- "Let me implement that now" (before verification)

**INSTEAD:**
- Restate the technical requirement
- Ask clarifying questions
- Push back with technical reasoning if wrong
- Just start working (actions > words)

## Handling Unclear Feedback

```
IF any item is unclear:
  STOP - do not implement anything yet
  ASK for clarification on unclear items

WHY: Items may be related. Partial understanding = wrong implementation.
```

**Example:**
```
your human partner: "Fix 1-6"
You understand 1,2,3,6. Unclear on 4,5.

❌ WRONG: Implement 1,2,3,6 now, ask about 4,5 later
✅ RIGHT: "I understand items 1,2,3,6. Need clarification on 4 and 5 before implementing."
```

## Source-Specific Handling

### From your human partner
- **Trusted** - implement after understanding
- **Still ask** if scope unclear
- **No performative agreement**
- **Skip to action** or technical acknowledgment

### From External Reviewers

Before implementing:
1. Check technical correctness for this codebase.
2. Check whether the suggestion breaks existing functionality.
3. Check the reason for the current implementation.
4. Check compatibility across platforms and versions.
5. Check whether the reviewer understands the full context.

If a suggestion seems wrong, push back with technical reasoning. If it cannot be verified, state what evidence is missing. If it conflicts with the user's prior decisions, stop and discuss it first.

**User rule:** External feedback should be treated skeptically, but checked carefully.

## YAGNI Check

If a reviewer proposes a "professional" feature, check whether it is actually used. If unused, ask whether it should be removed rather than expanding it. If used, implement the required improvement.

## Implementation Order

For multi-item feedback:
1. Clarify anything unclear first.
2. Address blocking issues (breakage, security).
3. Address simple fixes (typos, imports).
4. Address complex fixes (refactoring, logic).
5. Test each fix individually and verify there are no regressions.

## When To Push Back

Push back when a suggestion breaks functionality, lacks context, violates YAGNI, is technically incorrect, conflicts with compatibility needs, or contradicts the user's architectural decisions. Use technical reasoning and evidence, not defensiveness.

## Correcting an Incorrect Pushback

If verification shows the reviewer was right, state the correction factually, identify the evidence, and fix the issue without over-explaining.

## Common Mistakes

| Mistake | Better approach |
|---------|-----------------|
| Performative agreement | State the requirement or act |
| Blind implementation | Verify against the codebase first |
| Batching without testing | Fix and test one item at a time |
| Assuming the reviewer is right | Check the claim |
| Avoiding pushback | Prefer technical correctness |
| Implementing unclear items | Clarify first |
| Proceeding without evidence | State what cannot be verified |

## GitHub Thread Replies

When replying to inline review comments on GitHub, reply in the comment thread, not as a top-level pull request comment.
