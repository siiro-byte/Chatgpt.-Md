# Prompt Library Test Report

**Test date:** 2026-11-05  
**Repository:** https://github.com/siiro-byte/Chatgpt.-Md  
**Commit under test:** aa7fde763f7bd7659ab8e44c448d41cce175f36b  
**Overall result:** NOT PASSED — remediation required

## Scope

The library currently contains eight categories and 38 canonical prompt files:
- Research & Intelligence: 9 existing prompts
- Marketing & Growth: 4
- Travel Editorial: 5
- Business & Strategy: 4
- Writing & Communication: 4
- Image, Video & Audio: 4
- Coding & Technology: 4
- Productivity & Learning: 4

The malformed legacy nested Research & Intelligence directory was excluded from the canonical prompt count.

## Test 1 — Structural completeness

**Result: Partial pass**

The 29 newly added prompts contain the expected section headings:
Purpose, When to use, Required inputs, Instructions, Expected output, Quality checks, Source, Testing notes and Status.

The original nine Research & Intelligence prompts contain task-specific processes and output requirements, but do not all follow the current standard template.

## Test 2 — Instruction specificity

**Result: Fail — 29 prompts affected**

The 29 newly added prompts use substantially the same generic instruction block. The task-specific details are largely confined to the Purpose section. This does not provide enough operational guidance for reliable specialist behaviour.

Required remediation:
- Write a genuinely task-specific instruction block for every prompt.
- Specify a step-by-step method appropriate to the task.
- Define a concrete output structure and decision criteria.
- Include relevant failure modes and safeguards.
- Make required inputs specific to the task rather than repeating generic placeholders.

Affected files are all prompt files under:
- marketing-growth/
- travel-editorial/
- business-strategy/
- writing-communication/
- image-video-audio/
- coding-technology/
- productivity-learning/

## Test 3 — Representative functional test: Travel Alert Verification

**Test input:** A hypothetical report says a border crossing may have closed. No official notice or independent source is supplied.

**Expected behaviour:** The prompt should refuse to treat the closure as confirmed; identify the authority to check; seek the effective date, location and affected travellers; distinguish a temporary disruption from a formal closure; and label the claim unverified until supported.

**Observed prompt design:** Its purpose describes several of these requirements, but its generic instruction block does not enforce a complete verification sequence or a sufficiently precise output. This is a design-level failure; no external fact verification was attempted.

## Test 4 — Functional coverage

**Result: Not yet completed**

The prompts have not all been run against realistic inputs. No prompt should be marked Tested or Approved on the basis of this report.

## Remediation and approval policy

1. Rewrite the 29 generic instruction blocks into complete, task-specific prompts.
2. Align the original nine Research & Intelligence prompts with the common template without weakening their existing workflows.
3. Run at least one realistic test for every prompt.
4. Record test input, expected behaviour, observed output, defects and revisions.
5. Change status to Tested only after a successful test; reserve Approved for reviewed prompts that meet the quality standard.

**Current status:** All 38 prompts remain Draft. No prompt has been approved by this audit.
