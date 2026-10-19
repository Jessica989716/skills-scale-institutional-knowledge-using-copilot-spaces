# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.


---

## Additional Personas & Interaction Patterns

This section adds commonly needed personas, a short role summary, responsibilities, interactions with existing roles, and examples of decisions/handoffs they typically own.

### Delivery Lead (Delivery Manager)
Role summary
- Coordinates sprint/iteration execution and removes operational blockers so the delivery flow is smooth.

Responsibilities
- Track delivery commitments and sprint progress; surface risks and impediments.
- Facilitate delivery ceremonies (standups, sprint check-ins) when Product or Project leads are unavailable.
- Maintain sprint/iteration board hygiene and action items.

Interactions
- Daily with Developers, QA, and Project Manager; reports progress and risks to Product Manager.
- Escalates cross-team blockers to Product Lead or Project Manager as appropriate.

Example decisions / handoffs
- Owns the go/no-go checklist for an iteration’s release readiness and hands off deployment items to SRE/Platform.
- Notifies stakeholders on missed commitments and triggers scope re-planning.

Recommended Slack channels / notifications
- #delivery-<team>, #sprint-updates

---

### Engineering Manager
Role summary
- Owns technical staffing, career development, and capacity planning for the engineering team.

Responsibilities
- Manage hiring, assignments, and technical onboarding.
- Drive code-quality standards, tech-debt prioritization, and engineering health.
- Coordinate capacity planning and long-term technical roadmap trade-offs.

Interactions
- Works with Developers and Product Manager to balance scope vs. capacity.
- Collaborates with Delivery Lead on team velocity and resource allocation.

Example decisions / handoffs
- Approves capacity trade-offs and signs off on assignment changes during planning.
- Hands off prioritized tech-debt items to Product/Project tracking for scheduling.

Recommended Slack channels / notifications
- #eng-people, #eng-ops

---

### UX Researcher / Designer
Role summary
- Owns user research, design validation, and UX acceptance criteria for features.

Responsibilities
- Conduct research, usability tests, and accessibility checks.
- Produce design artifacts (wireframes, prototypes) and acceptance criteria.
- Validate solutions with users and measure usability outcomes.

Interactions
- Collaborates with Product Managers on requirements and with Developers/QA for implementation and validation.
- Participates in design reviews and acceptance conversations.

Example decisions / handoffs
- Signs off on UX acceptance criteria before a feature moves to development.
- Hands off final design assets and interaction notes to Developers and QA.

Recommended Slack channels / notifications
- #design, #ux-research

---

### QA Lead / Test Architect
Role summary
- Defines the testing strategy and ensures appropriate coverage across unit, integration, and end-to-end tests.

Responsibilities
- Define test strategy, automation goals, and test data requirements.
- Coordinate manual QA when required and maintain test environments.
- Track and report quality metrics (regressions, flakiness, coverage gaps).

Interactions
- Works closely with Developers on testability and with Product Managers on acceptance criteria.
- Provides test plans to Delivery Lead and reports quality risks to stakeholders.

Example decisions / handoffs
- Owns sign-off on release quality gates and hands off unresolved risks to Product/Delivery leads.
- Triggers regression or soak testing as part of pre-release validation.

Recommended Slack channels / notifications
- #qa, #test-automation

---

### Support Lead / Customer Operations Liaison
Role summary
- Manages triage for production issues, surfaces recurring customer problems, and owns support-facing runbooks.

Responsibilities
- Triage incidents and coordinate initial customer communications.
- Maintain runbooks, escalation paths, and known-issue documentation.
- Analyze trends in support tickets and feed them back to Product/Engineering.

Interactions
- Works with Engineers, SRE, and Product Managers on incident response and post-incident reviews.
- Provides prioritized customer-impact feedback to Product and Data Analysts.

Example decisions / handoffs
- Owns immediate customer-facing messaging and hands off technical incident work to SRE/Engineering.
- Requests hotfix prioritization from Product/Engineering when customer impact is high.

Recommended Slack channels / notifications
- #support, #incident-response

---

### Data Analyst / Product Analyst
Role summary
- Defines and monitors success metrics, instruments analytics, and analyzes experiments.

Responsibilities
- Specify metrics and instrumentation for features and experiments.
- Build dashboards and run analysis to inform product decisions.
- Validate outcomes against success criteria after releases.

Interactions
- Partners with Product Managers on metric definitions and with Engineers for instrumentation.
- Supports Retrospectives and decision-making with data-backed analysis.

Example decisions / handoffs
- Confirms metric readiness for launch and hands off dashboards to stakeholders for monitoring.
- Provides experiment analysis to Product for feature continuation or rollback decisions.

Recommended Slack channels / notifications
- #product-analytics, #metrics

---

### Security Liaison / AppSec Representative
Role summary
- Advises on security requirements, performs lightweight reviews, and coordinates with centralized security teams.

Responsibilities
- Run threat-modelling and security reviews for features; coordinate scans and remediation.
- Maintain security checklists and advise on compliance implications.
- Escalate critical issues to Security on-call or central AppSec.

Interactions
- Works with Developers and Product Managers to integrate security into design and acceptance criteria.
- Coordinates with Platform/SRE on infrastructure-level security controls.

Example decisions / handoffs
- Signs off on any feature-level security mitigations and hands off major risks to centralized Security for tracking.
- Requests a security freeze or additional testing when critical findings appear before release.

Recommended Slack channels / notifications
- #security, #appsec

---

### Platform / SRE Representative
Role summary
- Ensures deployment reliability, observability, and platform-level runbooks; participates in incident response.

Responsibilities
- Maintain deployment pipelines, observability dashboards, and platform runbooks.
- Participate in release planning for infra impacts and own platform mitigations.
- Lead platform-level incident response and post-incident follow-up.

Interactions
- Collaborates during release planning with Delivery Lead and Product Manager; supports Developers for post-deploy verifications.
- Works with Support Lead during infra-related incidents.

Example decisions / handoffs
- Owns rollbacks or platform mitigations for infra failures and coordinates handoff to Engineering for fixes.
- Signs off on platform-level readiness for major releases.

Recommended Slack channels / notifications
- #platform, #sre, #deployments
