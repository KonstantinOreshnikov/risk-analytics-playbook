# Risk Analytics Playbook

A practical, vendor-neutral playbook for building reliable risk analytics, repeatable reporting workflows, and decision-ready management information.

The material is intentionally generic. It contains no employer data, proprietary decision rules, internal thresholds, production schemas, or confidential methodology.

## What this repository covers

- analytical grain and metric contracts;
- data-quality and reconciliation controls;
- reproducible reporting workflows;
- management commentary that separates facts from interpretation;
- privacy-by-design rules for public analytical work;
- reusable review checklists.

## Operating model

```text
Business question
      ↓
Metric contract
      ↓
Source and grain validation
      ↓
Transformation and controls
      ↓
Reconciliation
      ↓
Decision-ready output
```

## Contents

| Guide | Purpose |
|---|---|
| [Metric contracts](docs/metric-contracts.md) | Define a metric before calculating it |
| [Data-quality framework](docs/data-quality-framework.md) | Test completeness, uniqueness, validity and reconciliation |
| [Reporting workflow](docs/reporting-workflow.md) | Move from a business question to a controlled report |
| [Management commentary](docs/management-commentary.md) | Write concise, evidence-based conclusions |
| [Public-work privacy gate](docs/privacy-gate.md) | Prevent confidential information from entering public repositories |
| [Release checklist](templates/release-checklist.md) | Final review before an analytical release |

## Core principles

1. Define the grain before writing SQL.
2. Treat metric definitions as contracts, not labels.
3. Reconcile totals before interpreting movements.
4. Keep transformation logic separate from presentation logic.
5. Make exceptions and exclusions visible.
6. Preserve a working baseline before optimizing it.
7. Publish only data and logic that are safe to disclose.

## Who this is for

Risk analysts, reporting teams, data analysts, analytics engineers and managers who need analytical outputs that can be understood, reproduced and challenged.

## License

Released under the [MIT License](LICENSE). Examples are educational and should be adapted to the governance and regulatory requirements of the relevant organization.

