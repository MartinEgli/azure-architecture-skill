# Azure Architecture Method

Use for `/azure assess` and `/azure target`.

## Review Lenses

- Business criticality and workload goal
- Environment: dev, test, staging, production, regulated, or shared platform
- Identity: Entra ID, managed identity, RBAC, privileged access, break-glass
- Network: hub-spoke, Virtual WAN, private endpoints, DNS, egress, ingress
- Data: classification, residency, backup, retention, recovery, ownership
- Reliability: availability zones, region strategy, health probes, failover,
  backup, restore, and operational drills
- Security: platform guardrails, secrets, encryption, logging, vulnerability
  management, and security review triggers
- Operations: monitoring, alerting, incident ownership, runbooks, change control
- Cost: SKU posture, scaling model, reservations, budgets, and cost ownership
- Governance: management groups, subscriptions, policy, tags, naming, IaC

## Output Expectations

- Separate current state, target state, gaps, and decisions.
- State assumptions when tenant, subscription, region, or policy details are
  unknown.
- Route implementation to the right specialized Azure skill.
- Mark any item requiring `enterprise-security-architecture` review.

