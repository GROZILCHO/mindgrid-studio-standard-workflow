# MindGrid Studio Standard Workflow v1.0

Status: Draft

This document defines the standard operating model for future MindGrid Studio web projects coordinated between Rosen / MindGrid Studio, ChatGPT Lead Assistant, Codex, and optional specialist agents.

## Purpose

MindGrid Studio Standard Workflow v1.0 is a repeatable operating system for planning, building, documenting, QA-ing, deploying, and improving web projects.

It was created from practical lessons learned during the Mall Electro project and turns those lessons into a reusable workflow for future websites. The workflow is designed to reduce lost context, unclear implementation tasks, route drift, weak QA, asset confusion, and over-reliance on chat memory.

## Core Operating Idea

- GitHub is the source of truth and shared project memory.
- Notion is the operations and task tracking layer.
- ChatGPT Lead Assistant is the strategy, planning, QA, and Codex prompt layer.
- Codex is the implementation, documentation, validation, and file-editing layer.
- Rosen / MindGrid Studio is the project owner, operator, and final decision-maker.

The workflow separates thinking, documentation, implementation, and operational tracking so future projects can continue across long chats, agent changes, and phased delivery.

## Variant B Repository Model

The chosen repository model is Variant B:

- One master workflow repository stores the reusable process, templates, prompts, checklists, examples, and platform notes.
- Reusable starter-kit folders exist for general, React/Vite, and WordPress projects.
- Project-specific repositories are created separately.
- Each new project copies or adapts the appropriate starter kit.
- The workflow repository evolves independently from project repositories.

This model is better than using one direct template for everything because it:

- Allows React/Vite, WordPress, and general projects to coexist.
- Avoids forcing one technical stack on every project.
- Keeps the master workflow clean and reusable.
- Allows future starter kits to improve independently.
- Keeps project-specific decisions out of the master workflow unless they become reusable lessons.

## Roles And Responsibilities

### Rosen / MindGrid Studio

- Project owner.
- Business context provider.
- Final decision-maker.
- QA reviewer.
- Deployment/operator where needed.

### ChatGPT Lead Assistant

- Intake guide.
- Strategic planner.
- Information architecture assistant.
- Codex prompt author.
- QA interpreter.
- Workflow coordinator.
- Project continuity assistant.

### Codex Developer

- Repository file editor.
- Implementation assistant.
- Documentation assistant.
- Validation runner.
- Task reporter.
- Must follow allowed and forbidden file scope.

### Optional Specialist Agents

- Content Strategist.
- Visual Prompt Designer.
- SEO/AEO Specialist.
- QA/Release Specialist.
- Notion Ops Coordinator.

Specialist agents should operate through clear inputs and outputs. They should not replace the project source of truth stored in repository documents.

## Standard Project Phases

### 1. Project Setup

Purpose: create the project repository, copy the appropriate starter kit, and prepare the operating docs.

Main questions:

- What type of project is this?
- Which starter kit should be used?
- What files must exist before planning begins?
- Who owns decisions and validation?

Expected output documents:

- README.md
- AGENTS.md
- PROJECT_RULES.md
- CURRENT_STATUS.md
- NEXT_ACTIONS.md

Complete when: the project repository exists, starter docs are copied, roles are clear, and no implementation has started without baseline docs.

### 2. Project Intake

Purpose: capture the business, audience, constraints, goals, and required deliverables.

Main questions:

- What is the project trying to achieve?
- Who is the audience?
- What constraints are known?
- What is out of scope?

Expected output documents:

- PROJECT_BRIEF.md
- PROJECT_RULES.md
- CURRENT_STATUS.md

Complete when: the project brief and rules are clear enough to prevent guesswork during strategy and implementation.

### 3. Strategy And Positioning

Purpose: define the strategic direction, offer, positioning, conversion goals, and proof points.

Main questions:

- What should the site communicate?
- What should users do next?
- What claims are approved?
- What differentiates the project?

Expected output documents:

- PROJECT_BRIEF.md
- SEO_PLAN.md
- DECISIONS_LOG.md where real strategic decisions are made

Complete when: positioning, target audience, primary actions, and approved claims are documented.

### 4. Site Structure

Purpose: define pages, routes, navigation, content hierarchy, and user journeys.

Main questions:

- What pages are needed?
- What routes are approved?
- What navigation model should be used?
- What content belongs on each page?

Expected output documents:

- SITE_STRUCTURE.md
- SEO_PLAN.md
- DECISIONS_LOG.md where route or architecture decisions are made

Complete when: core routes, page hierarchy, navigation, and page purposes are approved.

### 5. Content System

Purpose: define page copy, content models, reusable sections, metadata, and editorial rules.

Main questions:

- What content is required for each page?
- What copy needs approval?
- What content is reusable?
- What SEO metadata is needed?

Expected output documents:

- CONTENT_MODEL.md
- SEO_PLAN.md
- PROJECT_RULES.md

Complete when: baseline content structure and metadata requirements are documented.

### 6. Design System

Purpose: define the visual direction, typography, color logic, component expectations, layout rules, and responsive principles.

Main questions:

- What visual direction supports the project?
- What colors and typography are approved?
- What components are expected?
- What design rules must Codex follow?

Expected output documents:

- DESIGN_SYSTEM.md
- PROJECT_RULES.md
- DECISIONS_LOG.md where design decisions are made

Complete when: implementation can begin without inventing visual rules.

### 7. Visual Asset Pipeline

Purpose: plan, source, generate, optimize, document, and use visual assets responsibly.

Main questions:

- What images are needed?
- Which assets are source, optimized, or runtime files?
- What alt text and SEO usage are required?
- Are any assets external, generated, licensed, or temporary?

Expected output documents:

- IMAGE_ASSET_REGISTER.md
- SEO_PLAN.md
- DESIGN_SYSTEM.md

Complete when: required assets are listed, usage is clear, and implementation is not relying on repeated generic images or unapproved fallbacks.

### 8. Repository Setup

Purpose: prepare the project files, folder structure, docs, rules, and environment notes for implementation.

Main questions:

- What stack or platform is being used?
- Which files can Codex edit?
- What validation commands exist?
- What should not be touched?

Expected output documents:

- README.md
- AGENTS.md
- PROJECT_RULES.md
- DEPLOYMENT_GUIDE.md
- CURRENT_STATUS.md

Complete when: Codex can run narrow tasks with clear scope and validation expectations.

### 9. Implementation With Codex

Purpose: execute controlled implementation and documentation tasks through repository files.

Main questions:

- What is the exact goal of this task?
- Which files are allowed?
- Which files are forbidden?
- What validation proves completion?
- Should tracking docs be updated?

Expected output documents:

- Codex task prompts
- CURRENT_STATUS.md
- NEXT_ACTIONS.md
- ISSUES_LOG.md when issues are found

Complete when: scoped tasks are implemented, validated, reported, and committed or prepared for review.

### 10. QA And Deployment

Purpose: validate strategy, content, routes, visuals, SEO, performance, accessibility basics, and deployment readiness.

Main questions:

- Do routes and links work?
- Is content accurate and approved?
- Are SEO basics in place?
- Are images optimized and appropriate?
- Is deployment safe?

Expected output documents:

- QA_CHECKLIST.md
- ISSUES_LOG.md
- DEPLOYMENT_GUIDE.md
- CURRENT_STATUS.md

Complete when: no major unresolved route, SEO, build, image, performance, or deployment issues remain.

### 11. Post-launch

Purpose: monitor the live project, record issues, verify production behavior, and identify improvement tasks.

Main questions:

- Is the live site working?
- Are there production-only issues?
- What should be improved next?
- What should be deferred?

Expected output documents:

- ISSUES_LOG.md
- NEXT_ACTIONS.md
- CURRENT_STATUS.md

Complete when: the live project has been checked and follow-up work is documented.

### 12. Retrospective

Purpose: capture reusable lessons after the project or a major phase.

Main questions:

- What worked?
- What failed or created friction?
- What should become part of the standard workflow?
- What should change in templates, prompts, or checklists?

Expected output documents:

- PROJECT_RETROSPECTIVE.md
- DECISIONS_LOG.md where workflow decisions are made
- CHANGELOG.md in this master repository when the workflow changes

Complete when: lessons are documented and reusable improvements are identified.

## Required Project Documents

Strategic documents:

- PROJECT_BRIEF.md: business context, audience, goals, constraints, and scope.
- PROJECT_RULES.md: operating rules, technical constraints, content rules, and do-not-touch areas.
- SITE_STRUCTURE.md: pages, routes, navigation, and information architecture.
- CONTENT_MODEL.md: page content, reusable blocks, editorial model, and content dependencies.
- DESIGN_SYSTEM.md: visual direction, typography, colors, components, and layout rules.
- SEO_PLAN.md: search intent, metadata, page targets, structured content, and SEO/AEO notes.
- IMAGE_ASSET_REGISTER.md: source images, optimized files, usage locations, alt text, and asset status.

Operational documents:

- QA_CHECKLIST.md: quality checks before deployment and release.
- CURRENT_STATUS.md: current project phase, completed work, active issues, next task, git status, validation, and handoff notes.
- NEXT_ACTIONS.md: prioritized next tasks with owner, status, dependency, and suggested next prompt/task.
- ISSUES_LOG.md: bugs, blockers, risks, unresolved questions, and production observations.
- DECISIONS_LOG.md: real strategic, architectural, technical, content, SEO, design, or workflow decisions.
- DEPLOYMENT_GUIDE.md: deployment process, environment notes, rollback notes, and release checks.

Handoff and continuity documents:

- PROJECT_HANDOFF.md: compact context for switching chats, agents, or project phases.
- PROJECT_RETROSPECTIVE.md: lessons learned after launch or major project milestones.

## Tracking Document Update Logic

CURRENT_STATUS.md should be updated after significant implementation, QA, deployment, or planning tasks.

NEXT_ACTIONS.md should be updated when there are concrete next steps.

ISSUES_LOG.md should be updated when bugs, blockers, risks, unresolved questions, or production observations are found.

DECISIONS_LOG.md should be updated only when real strategic, architectural, technical, content, SEO, design, or workflow decisions are made.

PROJECT_HANDOFF.md should be updated when switching chats or agents, pausing the project, ending a major phase, or preparing a new session.

Important rule: Codex must not update all tracking documents automatically after every small edit. Tracking document updates must be explicit or justified by a real project state change.

## Codex Task Protocol

Every Codex task should use a narrow, controlled structure:

- Context
- Goal
- Current State
- Allowed Files
- Forbidden Files
- Requirements
- Tracking Docs Update
- Validation
- Output Required
- Stop Conditions

Tasks must be narrow because Codex works best when the allowed surface is explicit, the expected outcome is testable, and unrelated files are protected. Broad tasks increase the risk of route drift, visual drift, SEO drift, accidental refactors, and unclear validation.

Codex should stop and report when:

- The working tree is dirty outside the expected scope.
- Required files are missing.
- Instructions are unclear.
- The task requires modifying forbidden files.
- Validation fails.
- A requested operation risks data loss.
- The change may create route, SEO, design, content, or workflow drift.

### Controlled Batch Tasks

Narrow scope does not always mean one page or one file. A larger logical batch can be more efficient and equally controlled when:

- The batch groups structurally related work.
- Allowed and forbidden files are explicit.
- The expected route, content, or output state is measurable.
- Automated guards cover the whole batch.
- One complete validation suite and one final report are required.

Use batch tasks for repeatable work such as related localization content groups. Use microtasks for isolated blockers, uncertain architecture, or defects with high regression risk. Do not use budget efficiency as a reason to weaken validation or combine translation, runtime activation, and public SEO activation without phase gates.

### Interrupted Task Recovery

When a Codex session ends with valid uncommitted work:

1. Do not reset, restore, clean, or overwrite the working tree.
2. Run `git status` and inspect the complete diff.
3. Classify each changed file against the interrupted task scope.
4. Preserve valid partial work and report unrelated changes before continuing.
5. Continue from the current state with the original completion criteria.
6. Rerun the full validation suite, not only the unfinished command.

Destructive cleanup commands must not be used before the existing changes are understood.

## GitHub As Project Memory

GitHub stores the durable project truth.

- The repository stores project files and project documentation.
- The docs folder carries context that should survive chat limits.
- Commits capture progress over time.
- AGENTS.md defines agent behavior and project rules.
- CURRENT_STATUS.md and PROJECT_HANDOFF.md allow new chats or agents to resume work.
- GitHub becomes especially important when ChatGPT chat context becomes too long, unavailable, or split across sessions.

Chat memory is useful, but it is not the system of record. If a detail matters for implementation, QA, deployment, or future continuation, it belongs in repository documentation.

## Notion As Operations Layer

Notion can track:

- Projects.
- Tasks.
- Owners.
- Deadlines.
- Status.
- Milestones.
- Retrospective notes.

Notion should not replace repository documentation for implementation rules, technical decisions, file scope, project constraints, or handoff context. Notion is the operational dashboard; GitHub remains the implementation memory.

## WordPress And React/Vite Note

React/Vite projects:

- GitHub can store nearly the full project.
- Build and deployment can be fully file-based.
- Validation can usually be handled with local build, lint, tests, preview, and deployment checks.

WordPress projects:

- GitHub is reliable for theme, plugin, code, and docs.
- GitHub is not enough for database, media library, Elementor layouts, plugin settings, menus, and content.
- WordPress requires a backup, export, staging, and restore strategy.

Detailed platform workflows belong in:

- `platform-workflows/REACT_VITE_WORKFLOW.md`
- `platform-workflows/WORDPRESS_WORKFLOW.md`

## Visual Asset Pipeline

Visual assets should be planned before implementation.

- Use IMAGE_ASSET_REGISTER.md.
- Separate source images, optimized images, and runtime usage.
- Avoid repeated generic images.
- Define alt text and SEO image usage.
- Optimize assets before deployment.
- Avoid external fallback images unless approved.
- Track whether assets are original, licensed, generated, temporary, or client-provided.

Asset decisions affect performance, SEO, visual quality, and brand trust, so they should not be improvised late in implementation.

## QA Gates

Standard QA gates:

- Strategy QA.
- Content QA.
- Route/link QA.
- Visual QA.
- SEO QA.
- Performance QA.
- Accessibility/basic usability QA.
- Deployment QA.
- Post-launch QA.

A project should not move to deployment if major unresolved route, SEO, build, image, or performance issues remain.

## Handoff And Chat-limit Protocol

When a ChatGPT conversation becomes too long, a specialist agent changes, or the project needs to pause:

1. Update CURRENT_STATUS.md.
2. Update ISSUES_LOG.md if new issues, risks, blockers, unresolved questions, or production observations exist.
3. Update NEXT_ACTIONS.md with concrete next tasks.
4. Create or update PROJECT_HANDOFF.md.
5. Commit changes when appropriate.
6. Start the new chat by asking the assistant to inspect PROJECT_HANDOFF.md, CURRENT_STATUS.md, DECISIONS_LOG.md, and AGENTS.md.

The purpose is to make continuation possible without relying on a single chat thread.

## Standard Project Start Command

"Start a new web project using MindGrid Studio Standard Workflow v1.0. First run Project Intake. Do not propose design, code or implementation before PROJECT_BRIEF.md, SITE_STRUCTURE.md and PROJECT_RULES.md are established."

## Versioning

- v1.0 is based on the Mall Electro project lessons.
- Future versions should be updated after real projects.
- Changes should be recorded in CHANGELOG.md.
- Major workflow changes should be logged in DECISIONS_LOG.md where relevant.

## Final Operating Principle

Do not rely on memory.
Do not rely on one chat.
Do not start with code.
Start with structure, documents, decisions, and controlled execution.
