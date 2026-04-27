# AI

A curated repository of reusable guidance for AI coding agents. At the moment, this repository contains agent definitions and reusable skills focused on planning and review workflows.

### Agents

- `agents/code-reviewer.md`: a review-focused agent for validating completed implementation work.
- `agents/guided-planner.md`: a planning-focused agent that helps users shape an implementation plan before coding begins.

### Skills

- `skills/planning-question-gate/SKILL.md`: a planning guardrail skill that requires guided questions and explicit user approvals before any plan is drafted.

## What each agent does

### Code Reviewer

The Code Reviewer agent is intended for post-implementation review. It compares finished work against the original plan or requirements and checks whether the result is complete, justified, and maintainable.

Its main responsibilities are:

- verify alignment between the delivered implementation and the original plan;
- assess code quality, naming, maintainability, testing, and error handling;
- review architecture and design decisions, including separation of concerns and extensibility;
- inspect documentation and adherence to project standards;
- report issues with clear severity levels and actionable recommendations.

Use this agent when implementation already exists and you want a structured review of correctness, quality, and plan adherence.

### Guided Planner

The Guided Planner agent is intended for pre-implementation planning. It works interactively with the user to clarify requirements, research only when needed, and produce an explicit implementation plan.

Its main responsibilities are:

- ask guided questions before making material planning decisions;
- avoid autonomous implementation decisions that the user has not approved;
- do targeted discovery or research only to sharpen the next question or validate an approved direction;
- write a detailed implementation plan after requirements and decisions are confirmed;
- keep planning separate from execution and hand implementation off to another agent.

Use this agent when the problem is still being defined, when tradeoffs need user approval, or when you want a plan captured before coding starts.

## What each skill does

### Planning Question Gate

The Planning Question Gate skill is intended for planning conversations where unresolved trade-offs or ambiguities exist. It keeps the process in guided questioning until each material decision is explicitly approved by the user.

Its main responsibilities are:

- identify and surface unresolved material decisions one at a time;
- ask focused, approval-oriented questions before moving forward;
- avoid drafting plans while any material decision remains open;
- summarize decisions and boundaries, then request explicit approval;
- allow plan drafting only after all material decisions are resolved and approved.

Use this skill when you want planning discipline, clear user ownership of decisions, and no autonomous assumption-making in plan creation.
