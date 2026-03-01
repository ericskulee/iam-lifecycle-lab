# iam-lifecycle-lab
# IAM Lifecycle Lab — Joiner/Mover/Leaver + RBAC + Access Reviews

## What this is
A hands-on IAM lab demonstrating:
- Joiner/Mover/Leaver workflows
- RBAC role assignment
- deprovisioning/termination steps
- access review reporting

## Why it matters
Identity is a primary control for preventing breaches. This project shows governance: least privilege, lifecycle management, and periodic review.

## What’s included
- Containerized IAM environment (docker-compose)
- Scripts to create users, assign roles, disable users
- Access review report templates and exception handling

## Next improvements
- Add MFA notes and conditional access strategy
- Add group-based entitlement mapping

## Note on group-based role assignment
Group-based role assignments (“role-assignable groups”) are preferred for scalable least-privilege access.
This tenant does not have Entra ID P1/P2, so role-assignable groups are not available.
For this lab, roles are assigned directly to users while the intended group-based model is documented.
