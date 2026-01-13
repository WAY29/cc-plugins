---
description: "USE this before any creative work - creating features, building components, adding functionality, or modifying behavior. Explores user intent, requirements and design before implementation."
user-invocable: true
disable-model-invocation: true
---

# Brainstorming Ideas Into Designs

## Overview

Help turn ideas into fully formed designs and specs through natural collaborative dialogue.

Start by understanding the current project context, then gather requirements efficiently. Once you understand what you're building, present the design in logical sections, validating alignment at each step.

## The Process

**1. Understanding the idea:**
- **Context First:** Check the current project state (files, docs, recent commits) before asking anything.
- **Batch Questions:** Identify missing information and group questions logically by topic (e.g., Use Cases, Data Model, Constraints).
- **Use the Tool:** Construct a structured list of questions and use `AskUserQuestion` to present them to the user.
- **Iterate:** If the answers reveal new unknowns, follow up with another batch of focused questions.

**2. Exploring approaches:**
- **Options:** Propose 2-3 different technical approaches with trade-offs (Pros/Cons).
- **Recommendation:** Present options conversationally, clearly stating your recommended approach and the reasoning behind it.
- **Selection:** Use `AskUserQuestion` to ask the user to select an approach or provide feedback.

**3. Presenting the design:**
- **Incremental Reveal:** Once an approach is selected, present the design in logical chunks (e.g., "Data Model" then "API Structure").
- **Checkpoints:** After each chunk, ask if it looks correct so far before moving to the next.
- **Coverage:** Ensure the final design covers architecture, components, data flow, error handling, and testing strategies.

## After the Design
- Write the validated design to `docs/plans/YYYY-MM-DD-<topic>-design.md`.

## Key Principles

- **Efficient Inquiries:** Group 3-5 related questions to minimize back-and-forth latency.
- **Tool Usage:** Always use `AskUserQuestion` when waiting for user input to ensure the workflow pauses correctly.
- **Multiple Choice Preferred:** Provide options within your questions to reduce user cognitive load.
- **YAGNI Ruthlessly:** Remove unnecessary features from all designs; keep it lean.
- **Incremental Validation:** Present complex designs in sections; do not dump a massive spec all at once.
- **Flexibility:** Be ready to step back and refactor the plan if a requirement changes during the dialogue.