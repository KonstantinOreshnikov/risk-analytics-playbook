# Analytical Release Checklist

## Definition

- [ ] Business question and audience are clear
- [ ] Grain is documented
- [ ] Metric population, exclusions and time logic are documented
- [ ] Material definition changes are versioned

## Data and code

- [ ] Referenced fields exist in the source
- [ ] Row count and distinct-key count are reviewed
- [ ] Duplicates are explained or removed intentionally
- [ ] Date coverage is correct
- [ ] Key totals reconcile
- [ ] Nulls and anomalous values are reviewed

## Output

- [ ] Labels, units and periods are explicit
- [ ] Charts preserve meaningful scale
- [ ] Commentary separates facts from hypotheses
- [ ] Limitations are visible

## Public-release safety

- [ ] Data are synthetic or explicitly public
- [ ] No confidential names, identifiers or thresholds remain
- [ ] Git history has been scanned
- [ ] Ownership and license are clear

