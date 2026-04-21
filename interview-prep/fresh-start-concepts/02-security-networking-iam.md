# Security, IAM, and Networking (Concept Deep Dive)

## Concept 1: Microsoft Entra ID

### What it is
Identity provider for users, applications, and workload access.

### Core constructs
- Tenant
- Users/groups
- App registrations and enterprise applications
- Conditional access
- MFA and PIM

### Interview deep-dive
- How do you secure admin accounts?
- How do you design access for B2B partners?
- How do you implement least privilege at enterprise scale?

## Concept 2: Managed Identity

### What it is
Azure-managed identity for resources to authenticate without storing credentials.

### Why preferred
No secret in code/config; safer rotation and lifecycle management.

### Pitfall
Over-permissioned identity assignments.

## Concept 3: Key Vault

### Purpose
Store secrets, keys, certificates securely with audit and access controls.

### Best practices
- Private endpoint access for sensitive workloads
- Rotate secrets and keys
- Use RBAC model consistently

## Concept 4: Network Segmentation

### Core components
- VNets and subnets
- NSGs
- Route tables
- Azure Firewall
- Private endpoints

### Architect point
Design east-west and north-south traffic controls explicitly.

## Concept 5: Private Endpoints

### What it solves
Access PaaS services over private IP, reducing public exposure risk.

### Trade-off
Adds DNS and network complexity.

## Concept 6: WAF

### Purpose
Protects web applications from common OWASP attacks.

### Where used
- App Gateway WAF
- Front Door WAF

## Concept 7: Zero Trust

### Principle
Never trust implicitly. Continuously verify identity, device, context, and access intent.

### Practical implementation
- Conditional access
- Least privilege RBAC
- Micro-segmentation
- Strong logging and anomaly monitoring

## Concept Questions (Practice)

1. Entra ID vs RBAC: how are they related and different?
2. Why managed identity is better than secrets in app settings?
3. When do you enforce private endpoints?
4. How do NSG, Firewall, and WAF differ?
5. How do you operationalize Zero Trust in Azure?

