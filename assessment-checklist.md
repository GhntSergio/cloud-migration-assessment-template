# Assessment Checklist

Tick each item and record the figure or the finding next to it. Items marked **(risk)** often turn into entries in the risk register.

## General

- [ ] Products and versions (Jira Software, JSM, Confluence)
- [ ] Number of instances in scope, and whether they will be merged **(risk)**
- [ ] Hosting, database type and size, attachment volume
- [ ] Environments available: production, staging, test
- [ ] Target Cloud plan and site(s)
- [ ] Deadlines: license renewal, contract end, freeze periods

## Users and access

- [ ] Total users, active users over the last 90 days
- [ ] User directories: internal, LDAP / Active Directory, crowd
- [ ] Identity provider and SSO target (Atlassian Guard, SCIM provisioning)
- [ ] Users with duplicate or missing email addresses **(risk)**
- [ ] Groups used in permissions, notifications and workflows
- [ ] External users / customers (JSM portal accounts)

## Jira

- [ ] Number of projects (active / inactive)
- [ ] Number of issues and attachment volume
- [ ] Custom fields: total, unused, duplicates **(risk)**
- [ ] Workflows, schemes (permission, notification, field configuration, screen)
- [ ] Workflow post-functions, conditions and validators from apps **(risk)**
- [ ] Boards, filters and dashboards (shared, owned by inactive users)
- [ ] Advanced Roadmaps / Plans usage
- [ ] Listeners, services, scheduled jobs

## Jira Service Management

- [ ] Service projects, request types, portals
- [ ] SLAs and calendars
- [ ] Queues and automation rules
- [ ] Assets / Insight schemas, object counts, imports and integrations **(risk)**
- [ ] Customer organizations and portal settings
- [ ] Email channels and incoming mail handlers

## Confluence

- [ ] Number of spaces (global / personal, active / inactive)
- [ ] Pages, blog posts, attachment volume
- [ ] Macros from apps used in pages **(risk)**
- [ ] Page templates and blueprints
- [ ] Space permissions and anonymous access
- [ ] Links between Confluence and Jira (application links)

## Apps and customizations

- [ ] Full app list with versions and license tiers
- [ ] Usage per app (projects, spaces, users)
- [ ] Scripts (ScriptRunner or similar): count, purpose, owner **(risk)**
- [ ] Custom plugins developed in-house **(risk)**
- [ ] Fill `app-compatibility-matrix.csv`

## Integrations

- [ ] Application links (Bitbucket, Bamboo, other Jira/Confluence instances)
- [ ] REST API consumers: scripts, BI tools, ERPs, CI/CD **(risk)**
- [ ] Webhooks and incoming integrations
- [ ] Reporting tools (eazyBI, BI connectors) and their data sources
- [ ] IP allowlisting and network constraints

## Governance and compliance

- [ ] Data residency requirements
- [ ] Audit log and retention needs
- [ ] Security policies: MFA, session duration, API token policy
- [ ] Admin roles in Cloud (org admin, site admin, product admin)

## Readiness

- [ ] JCMA / CCMA pre-migration checks run, errors listed
- [ ] Cleanup backlog defined
- [ ] Test migration planned on a sandbox
- [ ] Business testers identified per area
