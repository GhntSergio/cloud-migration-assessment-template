# Atlassian Cloud Migration Assessment Template

![Atlassian](https://img.shields.io/badge/Atlassian-Data%20Center%20to%20Cloud-0052CC?style=flat&logo=atlassian&logoColor=white)

A reusable framework to run a **Data Center to Cloud assessment** for Jira, Jira Service Management and Confluence: what to inventory, how to score Marketplace apps, how to log risks, and how to turn findings into a migration roadmap.

It is built for consultants and Atlassian admins who need to deliver a clear, defensible recommendation to a steering committee.

## What is inside

| File | Use it for |
|---|---|
| [`assessment-checklist.md`](assessment-checklist.md) | Step-by-step inventory of the source instance, by domain |
| [`app-compatibility-matrix.csv`](app-compatibility-matrix.csv) | Scoring every Marketplace app: Cloud availability, feature gaps, data migration path, decision |
| [`risk-register.csv`](risk-register.csv) | Logging and scoring migration risks with owners and mitigations |

Open the CSV files in Excel or Google Sheets, or import them into Confluence tables.

## Assessment approach

```text
1. Scope        Products, instances, environments, deadlines, constraints
2. Inventory    Users, projects, spaces, customizations, apps, integrations
3. Analyze      Cloud compatibility, data volume, gaps, risks
4. Decide       Keep / replace / retire for each app and customization
5. Roadmap      Migration waves, cleanup tasks, test plan, communication
```

### 1. Scope

- Products and versions in scope, number of instances (instance merges change everything).
- Target Cloud plan (Standard, Premium, Enterprise) and why: sandbox, release tracks, data residency, user limits.
- Hard constraints: contract end dates, freeze periods, compliance (data residency, SSO, audit).

### 2. Inventory

Use [`assessment-checklist.md`](assessment-checklist.md). Collect data from:

- **JCMA / CCMA** pre-migration checks and the **app assessment** screen.
- Database or REST API exports for counts (projects, spaces, custom fields, workflows, filters).
- Interviews with project admins and app owners.

### 3. Analyze

For each app, fill [`app-compatibility-matrix.csv`](app-compatibility-matrix.csv):

| Column | What to check |
|---|---|
| Cloud version exists | Marketplace listing and vendor documentation |
| Feature parity | Features used on DC that are missing or different in Cloud |
| Data migration path | Automated (via JCMA/CCMA), vendor tool, manual, or none |
| Usage | Number of projects/spaces/users actually using the app |
| Decision | Keep, Replace (native or other app), Retire |

Typical hotspots: scripting apps (scripts must be rewritten for Cloud APIs), apps that store data outside Jira fields, custom field types without a Cloud equivalent, and reporting apps.

### 4. Decide

- Retire what is unused before migrating: fewer apps, fields and workflows mean lower risk and cost.
- Prefer native Cloud features (Automation, Assets, Advanced Roadmaps / Plans, Forms) when they cover the need.
- Log every gap and its workaround in [`risk-register.csv`](risk-register.csv).

### 5. Roadmap

A target plan usually contains:

- **Cleanup wave**: archive inactive projects and spaces, merge duplicate custom fields, delete unused workflows and schemes.
- **Test migration** to a Cloud sandbox, with a functional test plan per business area.
- **Migration waves** grouped by business unit or dependency, each with a go/no-go.
- **User onboarding**: SSO/SCIM (Atlassian Guard), user communication, training.
- **Hypercare** after each wave.

## Deliverables checklist

- [ ] Executive summary: recommendation, effort, main risks, timeline
- [ ] Instance inventory with key figures
- [ ] App compatibility matrix with decisions
- [ ] Risk register with mitigations and owners
- [ ] Target trajectory and migration waves
- [ ] Cleanup backlog to run before migration

## Contributing

Suggestions from other migration projects are welcome through issues or pull requests.

## License

MIT
