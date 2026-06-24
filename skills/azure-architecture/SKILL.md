---
name: azure-architecture
description: >
  Azure Architecture skill for Azure target architecture, landing zones,
  management groups, subscriptions, identity, networking, governance, Azure
  Policy, RBAC, platform architecture, Well-Architected Framework review,
  Cloud Adoption Framework alignment, migration positioning, Azure diagrams,
  and routing to specialized Azure operational skills. Use when Codex needs to
  design or review Azure architecture rather than directly deploy, diagnose, or
  operate individual Azure resources.
---

# Azure Architecture

## Purpose

Design and review Azure architecture so platform structure, governance,
security handoffs, reliability, cost, operations, and execution routing are
clear before implementation.

## When to Use

Use when the user asks for:

- Azure target architecture
- Azure landing zone or platform architecture
- management group, subscription, or resource group structure
- hub-spoke, Virtual WAN, private endpoint, or egress architecture
- Entra ID, RBAC, managed identity, and access architecture at platform level
- Azure governance, policy, tagging, naming, or guardrails
- Azure Well-Architected or Cloud Adoption Framework alignment
- Azure migration strategy or workload placement
- Azure architecture diagrams
- routing to the correct Azure execution skill

## Do Not Use When

Do not use to directly deploy prepared applications. Use `azure-deploy`.

Do not use to create app infrastructure from source code or deployment intent.
Use `azure-prepare` or `azure-enterprise-infra-planner` depending on scope.

Do not use for live production troubleshooting. Use `azure-diagnostics`.

Do not use for exact cost queries. Use `azure-cost`.

Do not use for detailed security approval. Use
`enterprise-security-architecture`.

Do not use for .NET code, ASP.NET Core, EF Core, or C# engineering review. Use
`dotnet-engineering` or `software-architecture`.

Do not use for final evidence acceptance or productive-use governance. Use
`mournival-architecture`.

## Mandatory Rules

- Start from workload goal, business criticality, environment, constraints, and
  operating model.
- Separate platform architecture, workload architecture, governance, and
  deployment execution.
- Mark assumptions, missing tenant/subscription facts, and unverified Azure
  constraints.
- Keep architecture decisions, routing decisions, diagrams, and handoffs
  traceable to supplied inputs, tool results, sources, or clearly marked
  assumptions.
- Prefer Azure-native secure defaults: managed identity, least privilege,
  private access where justified, policy guardrails, observability, and
  repeatable IaC.
- Do not invent tenant policy, subscription limits, regional availability, or
  compliance status.
- Route execution, diagnostics, cost, quota, RBAC, and service-specific tasks to
  the specialized Azure skills when they are the main task.
- Escalate enterprise strategy to `enterprise-architecture`, security approval
  to `enterprise-security-architecture`, software structure to
  `software-architecture`, and .NET implementation to `dotnet-engineering`.

## Inputs Expected

- workload or platform goal
- target Azure environment
- tenant, subscription, region, and environment constraints
- identity and access model
- network and data access needs
- availability, recovery, and operational requirements
- governance, policy, compliance, and tagging constraints
- IaC preference such as Bicep or Terraform
- migration source or current-state architecture when relevant

## Modes

### /azure assess

Assess an Azure architecture for gaps, risks, WAF alignment, governance,
operability, and execution readiness. Read
`references/azure-architecture-method.md`.

### /azure target

Create Azure target architecture from workload goals and constraints. Read
`references/azure-architecture-method.md`.

### /azure landing-zone

Design or review landing zone structure, management groups, subscriptions,
networking, identity, policy, and operations. Read `references/landing-zone.md`.

### /azure waf

Review an Azure workload against Well-Architected pillars: reliability,
security, cost optimization, operational excellence, and performance
efficiency. Read `references/well-architected.md`.

### /azure governance

Define governance guardrails, policy, RBAC, tagging, naming, environment
separation, and operational ownership. Read `references/governance.md`.

### /azure migration

Position workload migration to Azure and identify target services, transition
risks, sequencing, and execution handoffs. Read `references/migration.md`.

### /azure diagram

Create or review Azure architecture diagrams using Mermaid, PlantUML, or
C4-style notation. Read `references/diagrams.md`.

### /azure route

Choose the correct specialized Azure skill or architecture skill for the
request. Read `references/skill-routing.md`.

## Evidence Handling

Use `references/evidence-traceability.md`.

- Evidence: supplied diagram, IaC, Azure inventory, policy, source document, or
  explicit user fact.
- Inference: architecture conclusion derived from evidence.
- Assumption: useful but unverified Azure or business hypothesis.
- Gap: missing input that can change architecture or execution route.

Include an Evidence Receipt for substantial findings, decisions, diagrams, or
recommendations.

## Output Contracts

Use `assets/templates/azure-architecture-output.md` unless the user asks for
another format.

## Quality Gates

- Workload goal and environment are explicit.
- Platform and workload concerns are separated.
- Identity, network, data, operations, reliability, cost, and governance are
  addressed at the right depth.
- Security approval concerns are handed to `enterprise-security-architecture`.
- Deployment execution is routed to the right Azure execution skill.
- Key Azure claims include source trace or are marked as assumptions.
- Diagram scope stays at Azure architecture level.
- Assumptions and gaps are visible.

## Boundaries

- Do not replace accountable cloud architecture board, security, compliance, or
  production approval.
- Do not perform live Azure changes unless the user explicitly asks and the task
  belongs to an execution skill.
- Do not claim regional availability, quota, or pricing without current
  verification.
- Do not turn service-specific operations into broad architecture advice.

## Output Style

- Clear, structured, Azure-native, and decision-oriented.
- Prefer tables for options, risks, and handoffs.
- Use Mermaid for quick diagrams and PlantUML/C4-style notation when the user
  wants architecture-as-code.
- End with execution handoffs when implementation is requested.
