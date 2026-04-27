---
name: planning-question-gate
description: Use when creating a plan, roadmap, implementation plan, technical plan, or discovery plan and the user expects guided questions, explicit approvals, and no autonomous decisions.
user-invocable: false
---

# Planning Question Gate

## Overview

Planning is invalid when the agent fills in material decisions alone. Keep the conversation in guided questioning until the user has approved every decision that changes scope, behavior, enforcement, rollout, or verification.

## When to Use

- Planning requests, roadmaps, implementation plans, technical plans, or discovery plans
- Users who ask for guided questions, explicit approvals, or no autonomous decisions
- Requests with hidden trade-offs, unresolved scope, or multiple viable approaches

Do not use this after a plan has already been approved and execution has started.

## Non-Negotiables

- Never draft a plan while any material decision remains unresolved.
- Never treat silence, vague wording, or partial answers as approval.
- Recommendations are allowed. Decisions are not.
- Keep asking until all material decisions are approved or explicitly delegated by the user.
- If a new ambiguity appears later, reopen questions before continuing.

## Material Decisions

A decision is material when it changes any of the following:

- scope, exclusions, or success criteria
- architecture, enforcement strength, or fallback behavior
- file location, ownership, visibility, or invocation model
- naming that the user will see or depend on
- validation, approval gates, or rollout expectations

## Procedure

1. Surface the next material ambiguity.
2. Ask one focused question that resolves only that ambiguity.
3. Prefer multiple-choice options plus freeform input when that reduces ambiguity.
4. If a technical constraint changes the choice set, explain it briefly before asking.
5. Record the answer and move to the next unresolved material decision.
6. When no material decision remains open, summarize the current understanding, chosen decisions, and explicit boundaries.
7. Ask for explicit approval of that summary.
8. Only after approval, draft the plan.

## Recommendation Rule

When several approaches are viable:

- recommend one option
- explain the reason briefly
- wait for explicit approval before using it in the plan

## Exit Criteria

You may write the plan only when all of the following are true:

- no material decision remains open
- the current understanding has been summarized back to the user
- the user explicitly approved that summary

## Common Failures

- asking one broad question and assuming the rest
- moving from discovery straight to a plan
- treating approval of one option as approval of every downstream choice
- writing the plan first and asking for confirmation afterward