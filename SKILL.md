---
name: software-engineering-teacher-preferences
description: "Distills and applies the grading preferences of the Software Engineering Basics teacher from lecture transcripts. Use when drafting, reviewing, polishing, or planning course project deliverables for this class: Feishu/online process documentation, team roles, task assignment and scoring, attendance/training records, requirements docs, product prototypes, UML/DFD/design docs, configuration/change-management records, UI/interaction reviews, AI/tool-selection reports, testing/CI/CD plans, final project acceptance materials, or score-risk checklists. Emphasizes process visibility, traceability, requirements/prototype rigor, version/change control, user-centered interface details, team collaboration, and AI-assisted but human-understood work."
---

# Software Engineering Teacher Preferences

## Core Judgment

Use this skill to make Software Engineering Basics course materials fit the teacher's grading taste.

The teacher rewards evidence-backed software engineering process more than a flashy final demo. Treat every output as something that should survive classroom inspection: who did what, when, why, how it was confirmed, where the evidence is, and how the artifact maps to requirements, design, implementation, and testing.

Prioritize these values:

- **Process over result-only delivery**: a weak final system can still score if requirements, documents, task management, and team process are solid; a working system with chaotic process is risky.
- **Evidence over claims**: include online-doc links, screenshots, timestamps, sign-offs, meeting notes, attendance records, task records, change records, Feishu meeting minutes, and requirement snapshots. Never invent evidence; mark missing proof as `待补证据`.
- **Requirements and prototype first**: do not rush into coding. Spend enough effort clarifying functional requirements, performance/constraint requirements, user scenarios, and clickable prototypes.
- **Change and version control reduce chaos**: requirements will change, so every important document and change should have identity, owner, version, date, approval, and impact analysis.
- **User-centered interface details matter**: do not stop at "there is a page"; describe response, feedback, error handling, undo/cancel, screen adaptation, input validation, and asset licensing.
- **Team collaboration as the target ability**: the course trains cooperation, role division, project management, and internal teaching, not only individual coding.
- **AI and tools are expected but must be understood**: encourage AI-assisted coding/prototyping/documentation, but require tool-selection rationale, human review, and explanations the team can defend.

## Default Workflow

When helping with a deliverable, first classify it as one of these types:

- Team/process material
- Requirements material
- Product prototype material
- UML/DFD/design material
- Configuration/change-management material
- UI/interaction material
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
- Feishu meeting evidence: use online meetings and `妙记`/minutes for team discussions when possible; preserve summaries, participants, decisions, and action items. "We discussed it on WeChat" is weak unless the key decisions are copied into traceable project records.
- Internal training records: who learned a tool/topic, when they shared it, and what materials or notes remain.
- Feishu/online-doc-first collaboration. Prefer online documents with permissions set for the teacher to read. Add knowledge-base entrances to team/personal说明书 when useful, and make permissions explicit. Avoid treating local Word uploads as the primary collaboration artifact unless the user explicitly needs a file export.
- Document contribution visibility: when collaborative writing matters, enable author display or equivalent history so the leader can see who wrote what. Define whether members can edit, comment, or delete others' content.
- Work proactively. If the teacher has already pointed out a missing process artifact and the team waits to be urged again, mark it as a process-score risk.

Use this task table pattern often:

| ID | Task | Owner | Deadline | Completion Standard | Workload Points | Evidence Link | Status |
|---|---|---|---|---|---:|---|---|
| T-01 | Define login requirements | Product manager | 5/20 22:00 | Reviewed by customer side, no open ambiguity | 3 | 待补链接 | In progress |

For knowledge-base/process organization, prefer a visible entry structure:

| Entry | Required Content | Evidence |
|---|---|---|
| Team说明书 | roles, contacts, work habits, knowledge-base link, permission notes | Feishu link |
| Meeting Minutes | participants, decisions, action items, unresolved questions | 妙记/recording link |
| Requirement Snapshot | customer original text, version, proposer, date, receiver | Feishu doc link |

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
- Original customer snapshot: preserve the customer's raw requirement version before rewriting it. Record version (`V1`, `V2`...), date, proposer, receiver, and where it came from.
- Current course-stage deliverables: requirements should eventually have three linked parts: online pure-text requirement document, RP/clickable prototype, and UML use-case analysis or use-case description. If UML has not been taught yet, mark it as `后续补充`.

Use this requirements table pattern:

| Req ID | User/Scenario | Requirement | Constraints | Acceptance Criteria | Priority | Prototype Page | Customer Confirmation |
|---|---|---|---|---|---|---|---|
| FR-01 | Registered user logs in | Support phone + verification-code login | Code expires in 5 min | Wrong phone shows exact error copy; valid code enters home page | High | P-Login | 待确认 |

When the customer is vague, ask choice-based clarification questions and write the current assumption down. Do not silently decide business rules that belong to the customer.

Use this baseline/version pattern:

| Version | Source | Proposer | Receiver | Date | Summary | Status |
|---|---|---|---|---|---|---|
| V1.0 | Customer raw doc | Group 1 PM | Group 2 PM | 5/20 | Initial tutoring appointment platform requirement | Baseline / 待确认 |

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
- Device and screen assumptions: specify PC/web/mobile/mini-program target, safe area, scroll behavior, pagination/infinite loading, and whether screenshots or tables are readable on the expected device.
- Asset legality: for icons, fonts, pictures, and screenshots, prefer free/commercially safe resources or record the source/license.

Use this prototype review table:

| Page | Entry | Key States | Validation/Error Copy | Click/Jump Result | Edge Cases | Open Questions |
|---|---|---|---|---|---|---|
| Login | App launch | Empty, loading, wrong code, success | `手机号有误，请重新输入` | Success goes to Home | Expired code, network error | 是否支持密码登录 |

For tool mentions, prefer Axure, 墨刀, Mockplus/摹客, or other RP tools when appropriate. The tool itself is less important than whether the team explains why it was selected and demonstrates the clickable result.

## UI And Interaction Preferences

For UI/prototype/design reviews, judge whether the team considered the user's convenience rather than the developer's convenience.

Cover:

- User control: avoid forcing users into unnecessary operations; support cancel/interrupt/undo where the scenario needs it.
- Reduced memory burden: do not require users to remember information from a previous page when the system can carry it forward, auto-fill it, or show it again.
- Consistency: keep terminology, colors, shortcuts, navigation, dialog behavior, and interaction rules consistent across pages.
- Clear and concise prompts: error/help text should say what happened and what the user should do; avoid long ambiguous paragraphs.
- Responsiveness: after a click, give feedback. For slow operations, disable repeated clicks, show loading/progress, and prevent duplicate submissions.
- Forgiveness: protect users from accidental destructive actions with confirmation, recovery, or undo when the cost is meaningful.
- Dialog semantics: define whether closing `X` equals cancel, confirm, or "must choose"; avoid yes/no dialogs where neither choice is clear.
- Input efficiency: use defaults, common values first, validation, QR scan, voice input, shortcuts, or auto extraction where they match the scenario.

Use this UI review table:

| Scenario | User Risk | UI Rule | Required Feedback | Recovery/Undo | Device Concern |
|---|---|---|---|---|---|
| Submit appointment | Duplicate submit on slow network | Disable button after first click | `提交中...` + progress/loading | Retry if failed | Mobile safe area |

## Design, UML, And Traceability

For design materials, force traceability from requirement to design.

Include:

- UML use-case diagram for requirements when applicable. Clarify system boundary and external actors.
- UML/design docs that match the approved requirements rather than drifting into unrelated design.
- DFD for structured-analysis tasks when relevant; keep data-flow naming and layering consistent.
- ER/data dictionary/state diagram/flowchart when the project needs data or behavior modeling.
- Interface/API plan for front-back separation, including API owner, request/response fields, error codes, and status.
- Requirement-to-design-to-test trace table.
- System design should answer "how to do it", not repeat "what to do". Cover architecture/structure design, data/database design, interface design, and process/detail design when relevant.
- Treat the requirement specification as the authority. If design, code, or test differs from the requirement, update and re-baseline the requirement first instead of letting documents become disconnected.
- For module design, prefer high cohesion and low coupling. Explain decomposition/reuse/interface decisions based on requirement stability rather than personal taste.

Use this traceability table:

| Req ID | Prototype Page | UML/DFD Element | API/Module | Test Case | Evidence | Status |
|---|---|---|---|---|---|---|
| FR-01 | P-Login | UC-Login | `/auth/sms-login` | TC-Login-01 | 待补链接 | Draft |

## Configuration And Change Control

Use lightweight software configuration management even for the course project. The goal is not bureaucracy; it is to make chaos visible and controllable.

Require:

- Unique identifiers for important artifacts: project abbreviation, document type, module, date, author, and version. Avoid names like `新建文档2`.
- A clear folder/knowledge-base structure: requirements, prototype, design, implementation, test, meeting minutes, training, change records, and final acceptance.
- Version history for baseline documents: who changed what, when, why, who approved it, and which downstream artifacts are affected.
- A lightweight change request form (CRF) for meaningful requirement/design changes.

Use this CRF pattern:

| CRF ID | Project | Requester | Date | Change Description | Impact Scope | Priority | Estimated Workload | Decision | Implementer | QA/Verifier | Evidence |
|---|---|---|---|---|---|---|---:|---|---|---|---|
| CRF-001 | PETM | Customer PM | 5/20 | Move booking entrance to home page | Home, permissions, prototype, API, tests | High | 2 person-days | 待审批 | 待定 | 待定 | 待补链接 |

For every accepted change, update related requirement, prototype, design, implementation, and test records. For rejected or delayed changes, record the reason.

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
- Configuration management evidence: naming rules, baselines, snapshots, version history, and CRF records.
- UI/interaction evidence: key scenarios showing response, error handling, undo/cancel, device adaptation, and input validation.
- What failed or was incomplete, with honest process evidence and next-step plan.

Keep the story score-oriented: "we managed the process, controlled risk, left evidence, and can explain the tradeoffs."

## Review Checklist

Before returning or finalizing a course artifact, check:

- Does it show online-process evidence rather than only final claims?
- Are owners, deadlines, completion standards, and evidence links visible?
- Are requirements precise enough for another group to implement?
- Are unclear customer decisions marked and converted into questions?
- Does the prototype describe clickable flows, states, validation, and error feedback?
- Does the UI review cover responsiveness, user memory burden, consistency, undo/cancel, input validation, device adaptation, and asset licensing?
- Does design trace back to requirements and prototype pages?
- Are document names, versions, authors, baseline snapshots, and change records identifiable?
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
- Do not let requirement, design, code, and test documents become separate stories.
- Do not ignore font/icon/image licensing when producing UI or public-facing materials.
