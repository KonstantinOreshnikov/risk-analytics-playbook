# Metric Contracts

A metric contract prevents different teams from using the same label for different calculations.

## Minimum definition

Every material metric should document:

| Field | Question answered |
|---|---|
| Name | What is the metric called? |
| Business purpose | Which decision does it support? |
| Grain | One row represents what? |
| Numerator | What is counted or summed? |
| Denominator | What is the comparison base? |
| Population | Which records are eligible? |
| Exclusions | Which records are removed and why? |
| Observation date | When is the metric measured? |
| Maturity rule | When is an observation complete enough to use? |
| Unit | Count, currency, percentage, days, or another unit? |
| Owner | Who approves definition changes? |
| Controls | Which tests prove the result is trustworthy? |

## Example: generic conversion rate

```text
Name: Completed-case conversion rate
Purpose: Monitor movement through a generic process
Grain: One unique case
Numerator: Eligible cases reaching the completed state
Denominator: Eligible cases entering the measured stage
Observation date: Case entry date
Exclusions: Test and cancelled records
Unit: Percentage
```

This example is illustrative and contains no real decision or portfolio methodology.

## Change discipline

- version material definition changes;
- show the effective date;
- quantify the historical impact when possible;
- never silently backfill a new definition into an old series;
- keep display labels separate from calculation logic.

