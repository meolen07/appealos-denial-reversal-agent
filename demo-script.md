# AppealOS Demo Script

## Overview

This demo presents AppealOS, a multi-agent A2A healthcare workflow built on Prompt Opinion.

AppealOS helps care teams respond to denied prior authorizations by coordinating specialized agents that transform denial letters, patient context, and payer criteria into structured, evidence-backed appeal packets for clinician review.

---

## Demo Setup

This demonstration uses synthetic data only.

Case:
- Requested service: Lumbar spine MRI
- Scenario: Prior authorization denied
- Payer reason: Missing documentation for conservative therapy and neurologic findings

Inputs:
- Denial letter (unstructured text)
- Synthetic patient context (FHIR-style)
- Synthetic payer policy criteria

---

## Demo Flow

```text
Denial Letter -> Multi-Agent Review -> Evidence-to-Criteria Matrix -> Appeal Packet
```

---

## Step 1 - Present the Problem

Care teams must manually:
- Interpret denial letters
- Review fragmented clinical history
- Compare against payer policy
- Identify missing documentation
- Draft appeal materials

This process is time-consuming, error-prone, and difficult to audit.

---

## Step 2 - Introduce AppealOS

AppealOS coordinates multiple specialized agents using an A2A workflow.

```text
AppealOS Orchestrator Agent
|- Denial Interpreter Agent
|- Clinical Evidence Finder Agent
|- Policy Match Agent
|- Appeal Packet Writer Agent
|- Safety and Compliance Agent
```

Each agent focuses on a specific task.

The Orchestrator combines outputs into a structured appeal workspace.

---

## Step 3 - Show Prompt Opinion Integration

Show:
- AppealOS listed in the Prompt Opinion Marketplace
- The agent interface inside Prompt Opinion

Explain:

AppealOS is deployed as an A2A-enabled agent and can be invoked directly within the platform.

---

## Step 4 - Run the Demo Prompt

Paste and execute:

```text
Analyze this denied authorization and prepare an appeal packet for clinician review.

Healthcare context:
patient_id: synthetic-patient-001
requested_service: Lumbar spine MRI
payer_name: Synthetic Health Plan

Denial letter:
Coverage denied because submitted documentation does not show at least six weeks of conservative therapy or qualifying neurologic findings.

Payer policy:
Lumbar spine MRI may be considered when symptoms persist despite conservative therapy, or relevant neurologic findings are documented.

Synthetic patient context:
- 47-year-old synthetic patient
- Chronic low back pain with radicular symptoms
- Completed 8 weeks of physical therapy
- NSAID trial completed
- Positive straight-leg raise documented

Use synthetic data only. Do not diagnose or prescribe.
```

---

## Step 5 - Walk Through Output

### 1. Denial Summary

Show:
- Extracted denial reason
- Requested service
- Missing criteria

---

### 2. Patient Timeline

Show:
- Key encounters
- Therapy duration
- Clinical findings

Explain:

AppealOS reconstructs patient history from fragmented context.

---

### 3. Evidence-to-Criteria Matrix

Highlight this section as the core value:

| Payer Criterion | Evidence Found | Source | Gap | Next Action |
|---|---|---|---|---|

Explain:

This matrix maps:
- What the payer requires
- What evidence exists
- What is missing
- What to do next

This replaces manual chart review.

---

### 4. Missing Documentation

Show:
- Gaps clearly listed

Explain:

AppealOS does not fabricate missing data.

---

### 5. Appeal Readiness Score

Example:

```text
82/100 - Medium-High readiness
```

Explain:

This score reflects documentation completeness only.

It does not determine medical necessity or guarantee approval.

---

### 6. Appeal Strategy

Show:
- Recommended approach

Example:
- Emphasize completed conservative therapy
- Highlight neurologic findings
- Attach supporting documentation

---

### 7. Draft Appeal Letter

Show:
- Structured, professional letter

Explain:

This is a draft for clinician review, not an automated submission.

---

### 8. Peer-to-Peer Call Brief

Show:
- Key talking points

Explain:

Supports physician-to-physician review discussions.

---

### 9. Patient-Friendly Explanation

Show:
- Simple explanation of denial and next steps

---

### 10. Safety and Compliance Review

Show:
- Safety validation
- PHI check
- Boundary enforcement

Explain:

AppealOS ensures:
- No diagnosis
- No prescribing
- No fabricated evidence
- No autonomous action

---

## Step 6 - Key Innovation

AppealOS uses multi-agent coordination to:
- Interpret unstructured denial language
- Synthesize fragmented patient context
- Map evidence to payer criteria
- Generate structured, auditable appeal workflows

---

## Step 7 - Safety Statement

AppealOS is a workflow-support prototype.

It:
- Does not diagnose
- Does not prescribe
- Does not determine medical necessity
- Does not guarantee payer approval
- Does not submit appeals automatically
- Uses synthetic or de-identified data only

All outputs require clinician review.

---

## Step 8 - Closing

AppealOS transforms denial handling from a manual, fragmented process into a structured, multi-agent workflow that prepares evidence-backed appeal packets for clinician review.

---

## Timing Guide (Under 3 Minutes)

```text
0:00 - 0:15   Introduction
0:15 - 0:35   Problem
0:35 - 0:55   System overview
0:55 - 1:20   Platform integration
1:20 - 2:00   Live run
2:00 - 2:30   Output walkthrough
2:30 - 2:50   Key innovation
2:50 - 3:00   Safety + closing
```

---

## Presenter Notes

- Keep it fast and clear
- Highlight the matrix
- Emphasize workflow, not medicine
- Say "synthetic data" clearly
- Show multi-agent coordination, not chatbot
