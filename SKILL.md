---
name: software-engineering-teacher-preferences
description: "Distills and applies the grading preferences of the Software Engineering Basics teacher from lecture transcripts. Use when drafting, reviewing, polishing, or planning course project deliverables for this class: Feishu/online process documentation, team roles, task assignment and scoring, attendance/training records, requirements docs, product prototypes, UML/DFD/design docs, AI/tool-selection reports, testing/CI/CD plans, final project acceptance materials, or score-risk checklists. Emphasizes process evidence, traceability, requirements/prototype rigor, team collaboration, and AI-assisted but human-understood work."
---

# Software Engineering Teacher Preferences

## Core Judgment

Use this skill to make Software Engineering Basics course materials fit the teacher's grading taste.

The teacher rewards evidence-backed software engineering process more than a flashy final demo. Treat every output as something that should survive classroom inspection: who did what, when, why, how it was confirmed, where the evidence is, and how the artifact maps to requirements, design, implementation, and testing.

Prioritize these values:

- **Process over result-only delivery**: a weak final system can still score if requirements, documents, task management, and team process are solid; a working system with chaotic process is risky.
- **Evidence over claims**: include online-doc links, screenshots, timestamps, sign-offs, meeting notes, attendance records, task records, and change records. Never invent evidence; mark missing proof as `待补证据`.
- **Requirements and prototype first**: do not rush into coding. Spend enough effort clarifying functional requirements, performance/constraint requirements, user scenarios, and clickable prototypes.
- **Team collaboration as the target ability**: the course trains cooperation, role division, project management, and internal teaching, not only individual coding.
- **AI and tools are expected but must be understood**: encourage AI-assisted coding/prototyping/documentation, but require tool-selection rationale, human review, and explanations the team can defend.

## Default Workflow

When helping with a deliverable, first classify it as one of these types:

- Team/process material
- Requirements material
- Product prototype material
- UML/DFD/design material
- Implementation/testing/CI material
- Final acceptance/report material
- Exam-oriented concept review

Then add a score-oriented layer:

1. State the deliverable's purpose and inspection scenario.
2. Add responsible person, deadline, completion standard, and evidence location.
3. Make unclear customer or teacher assumptions explicit as `待确认`.
4. Add a "老师可能扣分点" section.
5. Add a "补救动作" section with concrete edits or missing artifacts.

## Team And Process Preferences

For team/project management outputs, make the team look like a small software company.

Include:

- Project manager/group leader, product manager or requirements analyst, frontend/backend/developer roles, QA/test role, deployment/operations role, and tool/documentation owner when relevant.
- A personal/team "说明书" style profile when useful: responsibility, working habits, interface person, upstream/downstream contacts, and current role.
- Task assignment in 5W form: who, does what, by when, to what standard, with what evidence.
- Workload decomposition and estimation. If building an internal scoring table, make workload the dominant category; attendance, document/training quality, attitude, cooperation, and comprehensive evaluation should be supporting categories.
- Attendance and participation evidence: signed sheet photo, Feishu check-in, meeting note, or other traceable proof.
- Internal training records: who learned a tool/topic, when they shared it, and what materials or notes remain.
- Feishu/online-doc-first collaboration. Prefer online documents with permissions set for the teacher to read. Avoid treating local Word uploads as the primary collaboration artifact unless the user explicitly needs a file export.

Use this task table pattern often:

| ID | Task | Owner | Deadline | Completion Standard | Workload Points | Evidence Link | Status |
|---|---|---|---|---|---:|---|---|
| T-01 | Define login requirements | Product manager | 5/20 22:00 | Reviewed by customer side, no open ambiguity | 3 | 待补链接 | In progress |

## Requirements Preferences

For requirements documents, write enough for an external team to implement without repeated phone calls.

Include:

- Project background and business goal, preferably tied to the simulated budget and customer value.
- Stakeholders and decision makers: who can confirm requirements, who only provides opinions, who is the designated contact.
- Functional requirements: "do what / do not do what".
- Performance and constraint requirements: response time, concurrency, data size, security, platform review constraints, legal/policy constraints, compatibility, deployment boundaries.
- User stories plus measurable acceptance criteria.
- Impact scope for seemingly small changes: affected pages, platforms, states, data, APIs, roles, payment/critical flows, and error cases.
- Requirement confirmation/baseline: version, reviewer, date, decision, and change-control rule.
- Requirement-change handling: describe impact analysis, re-confirmation, design/code/test trace, and final acceptance.

Use this requirements table pattern:

| Req ID | User/Scenario | Requirement | Constraints | Acceptance Criteria | Priority | Prototype Page | Customer Confirmation |
|---|---|---|---|---|---|---|---|
| FR-01 | Registered user logs in | Support phone + verification-code login | Code expires in 5 min | Wrong phone shows exact error copy; valid code enters home page | High | P-Login | 待确认 |

When the customer is vague, ask choice-based clarification questions and write the current assumption down. Do not silently decide business rules that belong to the customer.

## Prototype Preferences

The teacher expects a clickable graphical prototype, not just static screenshots.

For prototype work, cover:

- Page list and navigation map.
- Clickable paths for main user scenarios.
- Element-level behavior: button states, disabled/enabled rules, dropdown options, dialogs, empty states, loading states, error states, network failures, and permission states.
- Exact prompts/error copy where relevant.
- Validation rules: timing, field constraints, success/failure feedback.
- Business closure: the teacher or customer should be able to "walk through" a scenario and see no logic break.
- Global rules: naming, date/time format, pagination, file constraints, permission rules, and shared interaction patterns.

Use this prototype review table:

| Page | Entry | Key States | Validation/Error Copy | Click/Jump Result | Edge Cases | Open Questions |
|---|---|---|---|---|---|---|
| Login | App launch | Empty, loading, wrong code, success | `手机号有误，请重新输入` | Success goes to Home | Expired code, network error | 是否支持密码登录 |

For tool mentions, prefer Axure, 墨刀, Mockplus/摹客, or other RP tools when appropriate. The tool itself is less important than whether the team explains why it was selected and demonstrates the clickable result.

## Design, UML, And Traceability

For design materials, force traceability from requirement to design.

Include:

- UML use-case diagram for requirements when applicable. Clarify system boundary and external actors.
- UML/design docs that match the approved requirements rather than drifting into unrelated design.
- DFD for structured-analysis tasks when relevant; keep data-flow naming and layering consistent.
- ER/data dictionary/state diagram/flowchart when the project needs data or behavior modeling.
- Interface/API plan for front-back separation, including API owner, request/response fields, error codes, and status.
- Requirement-to-design-to-test trace table.

Use this traceability table:

| Req ID | Prototype Page | UML/DFD Element | API/Module | Test Case | Evidence | Status |
|---|---|---|---|---|---|---|
| FR-01 | P-Login | UC-Login | `/auth/sms-login` | TC-Login-01 | 待补链接 | Draft |

## AI And Tooling Preferences

Recommend AI and modern tools, but make the team accountable for them.

Include:

- Tool-selection mini report: candidates, free/team limits, collaboration support, learning cost, chosen tool, and reason.
- AI usage log: prompt purpose, generated artifact, human reviewer, modification summary, and unresolved risk.
- Programming environment choice: Cursor, CodeBuddy/Code Body, Trae, VS Code AI extensions, or other chosen IDEs are acceptable if documented.
- API/interface management tool when front-back separation is used.
- Testing and automation plan: unit tests, interface tests, pressure/performance tests when relevant, CI/CD or deployment automation if feasible.

Never present AI output as acceptable merely because AI produced it. The team must understand and explain the result.

## Final Acceptance Preferences

For final reports or presentations, organize around both delivery and process:

- What the customer asked for and how the team confirmed it.
- What was delivered, with scenario walkthrough and prototype/design/code/test evidence.
- Team organization, task decomposition, attendance, meetings, internal training, tool selection, and change records.
- Requirement changes and how they were handled.
- What failed or was incomplete, with honest process evidence and next-step plan.

Keep the story score-oriented: "we managed the process, controlled risk, left evidence, and can explain the tradeoffs."

## Review Checklist

Before returning or finalizing a course artifact, check:

- Does it show online-process evidence rather than only final claims?
- Are owners, deadlines, completion standards, and evidence links visible?
- Are requirements precise enough for another group to implement?
- Are unclear customer decisions marked and converted into questions?
- Does the prototype describe clickable flows, states, validation, and error feedback?
- Does design trace back to requirements and prototype pages?
- Is AI/tool usage documented with rationale and human review?
- Are obvious mistakes removed before a whole-group submission?
- Are deadline and baseline/change-control rules stated?
- Does the output include a short "老师可能扣分点" and "补救动作" section when reviewing?

## Avoid

- Do not optimize only for beautiful UI or runnable code.
- Do not skip requirements and start from implementation.
- Do not leave vague phrases like "提升用户体验" without acceptance criteria.
- Do not use static images as a substitute for an interactive prototype unless explicitly constrained.
- Do not claim attendance, sign-off, review, or tool usage evidence exists unless the user provided it.
- Do not produce local-file-centric process plans when Feishu/online documentation is the expected collaboration medium.
