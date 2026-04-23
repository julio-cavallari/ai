# AI

A curated repository of reusable guidance for AI coding agents. At the moment, this repository contains agent definitions focused on planning and review workflows.

### Agents

- `agents/code-reviewer.md`: a review-focused agent for validating completed implementation work.
- `agents/guided-planner.md`: a planning-focused agent that helps users shape an implementation plan before coding begins.

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
