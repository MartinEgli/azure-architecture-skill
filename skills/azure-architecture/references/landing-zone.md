# Azure Landing Zone Reference

Use for `/azure landing-zone`.

## Core Decisions

- Management group hierarchy and policy inheritance
- Subscription model: platform, connectivity, identity, management, workload,
  sandbox, and environment separation
- Identity model: Entra ID, privileged roles, managed identities, workload
  identity, service principals, and break-glass
- Network topology: hub-spoke, Virtual WAN, DNS, private endpoints, firewall,
  NAT, ingress, egress, and peering
- Governance: Azure Policy, initiatives, exemptions, tags, naming, locks, and
  resource consistency
- Operations: monitoring, log collection, alert routing, backup, patching,
  update management, and incident ownership
- Security: Defender, Key Vault, secrets model, encryption, vulnerability
  management, and security review path

## Guardrails

- Do not assume one subscription is enough for enterprise separation.
- Do not put all workloads into platform subscriptions.
- Do not bypass policy for convenience without documenting exception owner and
  expiry.
- Hand detailed control approval to `enterprise-security-architecture`.

