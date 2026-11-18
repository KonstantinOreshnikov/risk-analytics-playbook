# Portfolio Analysis Contracts

A metric is not ready for a management report until its observation grain, population and comparison basis are explicit. This page gives **generic educational patterns only**; it includes no actual portfolio figures, proprietary status mappings or internal thresholds.

## 1. Snapshot metrics versus longitudinal metrics

| Question | Grain | Required population / time rule | Frequent mistake |
|---|---|---|---|
| What is the current portfolio mix? | One eligible entity per reporting snapshot | Aligned observation date, status and measure | Combining multiple snapshots for one entity |
| How did a cohort change? | Origination cohort × common observation age | Compare equally mature cases | Mixing young and mature cohorts |
| Did an entity migrate? | Same entity paired across two periods | One unique record for each date, well-defined entry/exit policy | Comparing two cross-sectional groups as if paired |
| What share has a selected characteristic? | Eligible entity or exposure | Same population for numerator and denominator | Averaging group-level percentages |
| Is the portfolio concentrated? | Entity × segment × observation date | Mutually exclusive or explicitly overlapping segments | Double-counting nested categories |

## 2. Declare the contract

At minimum, document **entity key, period, source version, status interpretation, numerator, denominator, measure unit, eligibility, exclusions, maturity, aggregation and control total**.

A generic additive share is:

```text
Segment share = SUM(eligible segment measure)
              / NULLIF(SUM(eligible total measure), 0)
```

If the segment measure includes records excluded from the denominator, the rate is not interpretable. A zero denominator must return an undefined value with a visible reason, not a fabricated zero percent.

## 3. Synthetic cohort illustration

Every number below is **invented**.

| Fictional cohort | Eligible cases at comparable age | Cases in sample status | Share |
|---|---:|---:|---:|
| Cohort X | 100 | 8 | 8% |
| Cohort Y | 150 | 9 | 6% |

The cohort labels and status are generic. Comparing both at the same age is necessary but not sufficient: definitions, exclusions and observation coverage must also match. No business conclusion follows from these invented values.

## 4. Migration requires pairing

A transition matrix must join **the same entity** between observation A and B:

~~~mermaid
flowchart LR
  A["Entity at date A"] --> U{"Unique key at both dates?"}
  U -->|Yes| P["Pair A and B statuses"]
  U -->|No| E["Separate entrants / exits / gaps"]
  P --> M["Transition counts"]
  M --> R["Reconcile matched and unmatched populations"]
  E --> R
~~~

A matrix comparing two conflicting statuses **at a single date** is a *cross-sectional disagreement analysis*, not migration. Treat missing or newly entering entities as their own documented groups rather than silently removing them.

## 5. Quality gates

- Validate one unique entity per declared snapshot.
- Record observation-date availability and period boundaries.
- Reconcile matched, unmatched, entered and exited counts.
- Compare additive totals before and after a join.
- Test weighted rates at the **final filtered grouping level**.
- Explain exclusions, low-volume groups and missing periods.
- Separate observed movements from causal conclusions.

The related [Risk Reporting & SQL Workspace case study](https://github.com/KonstantinOreshnikov/KonstantinOreshnikov/tree/main/projects/risk-reporting-sql-workspace) shows how these contracts fit into an analytical engineering workflow.

---

**RU · Кратко:** синтетическая методология анализа портфеля: snapshot, cohort, migration, denominator, reconciliation и контроль исключений. Никаких внутренних правил или реальных показателей.
