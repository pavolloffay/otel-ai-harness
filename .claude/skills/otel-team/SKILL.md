---
name: otel-team
description: >
  Red Hat build of OpenTelemetry team overview, upstream context, and contribution approach.
  Use when you need to understand the team's scope, mission, or how to engage with upstream OpenTelemetry.
---

# Red Hat build of OpenTelemetry Team

## Team Overview

The team develops and maintains **Red Hat build of OpenTelemetry** — a supported OpenTelemetry distribution for OpenShift. The product provides a telemetry pipeline for collecting traces, metrics, and logs from applications and infrastructure.

**Scope:**
- OpenTelemetry Collector (GA) — vendor-agnostic telemetry pipeline
- OpenTelemetry Operator (GA) — Kubernetes operator managing collector lifecycle
- Target Allocator (GA) — Prometheus scrape target distribution
- Auto-instrumentation injection (Technology Preview)

**Not in scope:** Backend storage (Tempo, Prometheus, Loki are separate products), UI/console plugins (separate team ownership).

### Team Members

| Name              | Role               | GitHub        |
|-------------------|--------------------|---------------|
| Pavol Loffay      | Engineer           | @pavolloffay  |
| Benedikt Bongartz | Engineer           | @frzifus      |
| Ozzy Walsh        | Engineer           | @ozzywalsh    |
| Ishwar Kanse      | (Quality) Engineer | @IshwarKanse |

### Red Hat Slack
- Team: `#team-ocp-tracing`
- OpenTelemetry support: `#forum-opentelemetry`
- Tracing support: `#forum-ocp-tracing`

### Jira
- Project key: **TRACING** on `redhat.atlassian.net`

## Upstream Context

The team actively contributes to the upstream **OpenTelemetry** project (CNCF). The contribution strategy is **upstream-first** — features and fixes should land upstream before being included in the product distribution.


### Contribution Approach

1. **Upstream first**: New features and bug fixes go to the upstream OpenTelemetry repos before downstream inclusion
2. **Fork-based workflow**: Push to personal fork, PR against `origin/main`, squash before merging
3. **Component selection**: The Red Hat distro does not fork the collector — `manifest.yaml` declaratively selects upstream components, and OpenTelemetry Collector Builder (OCB) generates the binary
4. **Minimize divergence**: Carry as few downstream-only patches as possible

### Upstream Community

- OpenTelemetry is a CNCF project: https://opentelemetry.io
- Operator SIG: https://github.com/open-telemetry/opentelemetry-operator
- Collector SIG: https://github.com/open-telemetry/opentelemetry-collector
- Community meetings and SIG schedules: https://github.com/open-telemetry/community