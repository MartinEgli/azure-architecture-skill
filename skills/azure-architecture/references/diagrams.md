# Azure Architecture Diagrams

Use for `/azure diagram`.

## Scope

Create Azure architecture diagrams for:

- landing zones and management group hierarchy
- subscription and environment structure
- hub-spoke or Virtual WAN topology
- private endpoint, DNS, ingress, and egress views
- workload architecture at Azure service level
- governance and policy flow
- monitoring and operational ownership
- migration transition views

## Notation

- Mermaid `flowchart` for topology, governance, and service relationships.
- Mermaid `sequenceDiagram` for deployment, identity, or operational flows.
- Mermaid `timeline` or `gantt` for migration waves.
- PlantUML or C4-style notation when persistent architecture-as-code is needed.

## Rules

- Label region, subscription, environment, trust boundary, and ownership when
  known.
- Do not invent deployed resources or live configuration.
- Route detailed threat diagrams to `enterprise-security-architecture`.
- Route code/runtime diagrams to `software-architecture` or `dotnet-engineering`.

