# Repository Template

This repository is a lightweight starting point for new repositories. It serves as a template for standard repo structure. Copy it to establish a familiar layout then keep only the directories your project actually needs. It separates deployable applications, reusable code, infrastructure, documentation, project planning, and cross-project tests without imposing a language or build tool.

The folders in this repository, together with `README.md` and `AGENTS.md`, form the template. When creating a new repository, copy `README.md` and `AGENTS.md` as empty files. Do not copy their contents from this template.

## Current template structure

The following is the structure currently included in this repository (excluding Git metadata):

```text
repository/
├── .agents/
│   └── skills/
├── apps/
│   └── services/
├── docs/
│   ├── architecture/
│   └── product/
├── infra/
├── libs/
├── project/
│   ├── Initiative 1/
│   │   ├── Feature 1/
│   │   └── Feature 2/
│   └── Initiative 2/
├── tests/
│   ├── e2e/
│   └── performance/
├── AGENTS.md
└── README.md
```

| Folder                            | Purpose                                                                                                                                                                         |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `.agents/`                        | Repository-scoped workflows and guidance for coding agents.                                                                                                                     |
| `.agents/skills/`                 | Reusable agent skills.                                                                                                                                                          |
| `apps/`                           | Independently runnable or deployable applications.                                                                                                                              |
| `apps/services/`                  | Long-running backend services.                                                                                                                                                  |
| `docs/`                           | Durable documentation for the repository and product.                                                                                                                           |
| `docs/architecture/`              | System design, component boundaries, important technical flows, and ADRs.                                                                                                       |
| `docs/product/`                   | Product context and product-facing documentation.                                                                                                                               |
| `infra/`                          | Version-controlled infrastructure and deployment definitions. IaC.                                                                                                              |
| `libs/`                           | Reusable source code and shared contracts used by applications.                                                                                                                 |
| `project/`                        | Project-planning and execution material organized by initiative and feature. SDLC tasks are managed here (local replacement for Jira or other similar SDLC-supporting systems). |
| `project/Initiative 1/`           | Example initiative containing feature-level planning folders.                                                                                                                   |
| `project/Initiative 1/Feature 1/` | Example feature workspace within an initiative.                                                                                                                                 |
| `project/Initiative 1/Feature 2/` | Example feature workspace within an initiative.                                                                                                                                 |
| `project/Initiative 2/`           | Example initiative workspace.                                                                                                                                                   |
| `tests/`                          | Test suites that span project boundaries; project-local unit tests stay with their owner.                                                                                       |
| `tests/e2e/`                      | End-to-end user or system tests.                                                                                                                                                |
| `tests/performance/`              | Load, stress, and system-level performance tests.                                                                                                                               |
| `AGENTS.md`                       | Empty starter file for repository-wide coding-agent guidance.                                                                                                                   |
| `README.md`                       | Empty starter file for the new repository's overview and onboarding information.                                                                                               |

## Recommended enhanced structure

Use this fuller structure when the repository needs the corresponding capabilities. It is a taxonomy, not a requirement to commit empty directories.

```text
repository/
├── apps/
│   ├── services/<service-name>/
│   ├── workers/<worker-name>/
│   ├── jobs/<job-name>/
│   ├── web/<app-name>/
│   └── mobile/<app-name>/
├── libs/
│   ├── java/<library-name>/
│   ├── python/<library-name>/
│   ├── typescript/<library-name>/
│   └── contracts/<contract-name>/
├── infra/
│   ├── terraform/
│   ├── kubernetes/
│   └── helm/
├── docs/
│   ├── product/
│   ├── architecture/
│   └── runbooks/
├── project/
├── tools/
│   ├── scripts/
│   └── generators/
├── tests/
│   ├── integration/
│   ├── e2e/
│   └── performance/
├── .agents/skills/<skill-name>/SKILL.md
├── .github/
│   ├── workflows/
│   └── CODEOWNERS
├── AGENTS.md
├── README.md
├── CONTRIBUTING.md
└── SECURITY.md
```

| Folder | Purpose |
| --- | --- |
| `apps/` | Independently runnable or deployable projects. |
| `apps/services/` | Long-running network services, including APIs and backend services. |
| `apps/workers/` | Long-running consumers of queues, streams, or events. |
| `apps/jobs/` | Run-to-completion scheduled, batch, or maintenance workloads. |
| `apps/web/` | Browser applications and websites. |
| `apps/mobile/` | Native or cross-platform mobile applications. |
| `libs/` | Reusable, non-deployable source code. |
| `libs/java/` | Reusable libraries for the Java ecosystem. |
| `libs/python/` | Reusable libraries for the Python ecosystem. |
| `libs/typescript/` | Reusable libraries for the TypeScript ecosystem. |
| `libs/contracts/` | Shared language-neutral interfaces, such as OpenAPI, Protobuf, AsyncAPI, or schemas. |
| `infra/` | Infrastructure and deployment definitions. |
| `infra/terraform/` | Cloud resources, reusable modules, and environment composition. |
| `infra/kubernetes/` | Kubernetes manifests, bases, and overlays. |
| `infra/helm/` | Helm charts. |
| `docs/` | Durable repository documentation. |
| `docs/product/` | Product requirements, context, and supporting material. |
| `docs/architecture/` | System design, boundaries, and technical flows. |
| `docs/runbooks/` | Operational diagnosis, mitigation, recovery, and escalation procedures. |
| `project/` | Project-planning material, commonly organized by initiative and feature. |
| `tools/` | Tooling used to develop, validate, or manage the repository. |
| `tools/scripts/` | Developer-command wrappers and repository automation scripts. |
| `tools/generators/` | Project and code generators. |
| `tests/` | Cross-project test suites; keep unit tests with the owning project. |
| `tests/integration/` | Tests covering multiple projects or external dependencies. |
| `tests/e2e/` | End-to-end user or system journeys. |
| `tests/performance/` | Load, stress, and system-level performance tests. |
| `.agents/skills/` | Repository-wide reusable agent workflows. |
| `.github/` | GitHub-specific repository configuration. |
| `.github/workflows/` | CI, release, deployment, and infrastructure workflows. |
