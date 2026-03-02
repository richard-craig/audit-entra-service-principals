# audit-entra-service-principals
Script to create some basic risk based reports for Entra Service Principals.

The goal here is to provide visibility from a risk perspective of Service Principals.

For each principal ideally we want to know:
- What is it?
- Who owns it?
- What can it access?
- How does it authenticate?
- Is it actually being used?
- Is the risk acceptable?

For the reports I aiming to provide:
- All service principals with no owner
- All service principals with Graph application permissions
- All service principals with admin consent
- All service principals with Azure RBAC above resource-group scope
- All service principals using client secrets
- All principals with secrets/certs expiring in 90 days
- All principals with multiple active credentials
- All principals with no sign-in/activity in 90–180 days
- All newly created principals in last 90 days
- All third-party / externally published enterprise apps
