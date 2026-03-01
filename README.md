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

- ## What I built
- 3 test users (VM Analyst, System Owner, Auditor)
- Groups representing VM roles (used for identity organization)
- Least-privilege role assignments (direct-to-user due to licensing constraints)
- MFA/security defaults enabled and validated
- Auditability demonstrated via sign-in logs

## Controls demonstrated
- Least privilege and separation of duties
- Strong authentication (MFA) / secure defaults
- Auditable access (sign-in logs)

## Role matrix

| Persona | Assigned role(s) | Allowed | Not allowed |
|---|---|---|---|
| VM Analyst | Security Reader (or closest available) | View security posture/findings | Change tenant-wide settings |
| System Owner | (Reader role or none) | View basic directory info / own sign-in | Assign roles / admin actions |
| Auditor | Reports Reader | View reports/logs for review | Make changes |

## Note on group-based role assignment
Group-based role assignments (“role-assignable groups”) are preferred for scalable least-privilege access.
This tenant does not have Entra ID P1/P2, so role-assignable groups are not available.
For this lab, roles are assigned directly to users while the intended group-based model is documented.
