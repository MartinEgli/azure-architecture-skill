# Evidence And Traceability

Use this reference whenever Azure architecture decisions, routing decisions,
diagrams, or governance recommendations depend on supplied inputs.

## Input Register

Track meaningful inputs by source type:

- User fact: stated directly by the user.
- Artifact: Azure diagram, IaC, `azure.yaml`, policy, inventory, landing zone
  document, ADR, workload description, or migration assessment.
- Tool result: Azure CLI output, Azure Resource Graph query, validation result,
  cost report, diagnostic output, quota check, or generated report.
- External source: cited Microsoft Learn page, Azure WAF/CAF guidance, policy,
  standard, or public source.
- Assumption: useful but unverified Azure or business premise.

## Traceability Rules

- Preserve tenant, subscription, region, resource, policy, tag, role, and
  service names exactly.
- Tie each architecture or routing decision to an input, source, tool result, or
  assumption.
- Do not claim regional availability, quota, pricing, or live configuration
  without current verification.
- Mark missing tenant, subscription, region, policy, and ownership information
  as gaps.
- Keep execution handoffs explicit so architecture advice does not masquerade as
  completed deployment.

## Evidence Receipt

For substantial outputs, include a compact receipt:

| Decision Or Handoff | Source/Input | Type | Confidence | Gap Or Follow-up |
| --- | --- | --- | --- | --- |

Use `not supplied` when the input is missing. Use `assumption` when proceeding
with a working premise.

## Verification Pattern

Follow the small-loop pattern:

1. Locate relevant workload, tenant, subscription, policy, IaC, and Azure
   inventory inputs.
2. Make the smallest scoped architecture or routing recommendation.
3. Verify the output against evidence, assumptions, Azure skill boundaries, and
   execution handoffs.

Avoid making live-resource claims when only target architecture evidence was
provided.
