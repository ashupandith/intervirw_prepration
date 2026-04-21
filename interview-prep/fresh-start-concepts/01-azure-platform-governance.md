# Azure Platform and Governance (Concept Deep Dive)

## Concept 1: Management Groups

### What it is
Top-level container to organize subscriptions and apply governance at scale.

### Why it matters
You can apply policy and RBAC inheritance centrally across many subscriptions.

### Interview deep-dive checks
- Why use management groups vs applying policy on each subscription?
- How many levels of hierarchy do you design and why?
- How do you align management groups with business units and compliance?

### Common mistakes
- Flat hierarchy with no ownership model
- Too many custom exceptions

## Concept 2: Subscriptions

### What it is
Security, billing, quota, and operational boundary.

### How to design
- Separate by environment, workload criticality, or business unit
- Keep production isolated from non-production

### Interview deep-dive checks
- How do you decide per-app subscription vs shared subscription?
- How do you handle quota and cost visibility at scale?

## Concept 3: Resource Groups

### What it is
Logical grouping for lifecycle and access management of resources.

### Best practice
- Group resources that share lifecycle, deployment, and ownership
- Avoid giant shared resource groups across unrelated systems

## Concept 4: Landing Zones

### What it is
Predefined enterprise cloud foundation: identity, network, policy, logging, security.

### What interviewers expect
- You understand it is operating model + governance, not just networking
- You can explain platform team vs app team responsibilities

### Must-cover components
- Identity baseline
- Hub-spoke networking
- Policy guardrails
- Monitoring and security posture
- Cost governance

## Concept 5: Azure Policy

### What it is
Policy-as-code mechanism to enforce and audit standards.

### Modes
- Audit
- Deny
- Append/modify (where supported)

### Good examples
- Only approved regions
- Mandatory tags
- Require diagnostic settings
- Restrict public network access

## Concept 6: RBAC

### What it is
Role-based access control for users, groups, service principals, managed identities.

### Architect-level patterns
- Least privilege
- Group-based assignments
- Scope inheritance control
- Separation of duties

## Concept 7: Tagging and Cost Controls

### Why tags matter
Ownership, environment, cost-center, compliance classification.

### Cost control methods
- Budgets and alerts
- Right sizing and autoscale tuning
- Reservations/savings plans for stable workloads
- Chargeback/showback reports

## End-to-End Scenario

Design governance for 200 subscriptions:
1. Build management group hierarchy by BU and environment.
2. Define platform baseline policies in root/shared groups.
3. Separate prod/non-prod subscriptions with clear ownership.
4. Enforce mandatory tagging and diagnostics.
5. Implement RBAC model and privileged access workflows.
6. Add budget alerts and monthly governance review.

## Concept Questions (Practice)

1. Difference between management group policy and subscription policy?
2. When should subscriptions be split?
3. How do you control policy exceptions safely?
4. How do you enforce governance without slowing delivery?
5. How do you measure governance maturity?

