# Data-Quality Framework

Reliable reporting requires controls at source, transformation and output level.

## Control dimensions

| Dimension | Typical test | Failure signal |
|---|---|---|
| Completeness | Required fields are populated | Unexpected null rate |
| Uniqueness | Primary key is unique at declared grain | Duplicate keys |
| Validity | Values match type and allowed domain | Invalid dates or categories |
| Consistency | Related fields obey defined relationships | Completed case without completion date |
| Timeliness | Latest expected period is present | Missing reporting date |
| Reconciliation | Totals match an authoritative source | Unexplained count or amount difference |

## Minimum control pack

1. Row count and distinct-key count.
2. Duplicate-key list.
3. Minimum and maximum dates.
4. Null rate for material fields.
5. Distribution of statuses and categories.
6. Sums of key measures.
7. Comparison with the previous successful run.
8. Reconciliation to an independent control total.

## Investigation order

When totals differ, check in this order:

1. reporting period;
2. population and exclusions;
3. grain and duplication;
4. joins and effective dates;
5. typing and null handling;
6. aggregation logic;
7. source-system restatements.

This order prevents premature tuning of calculations when the real problem is population mismatch.

