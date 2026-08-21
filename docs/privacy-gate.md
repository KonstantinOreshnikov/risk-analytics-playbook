# Privacy Gate for Public Analytical Work

Public repositories must contain only material that is safe to disclose and independently reusable.

## Blocked content

- employer or client data;
- internal schema, table and field names;
- proprietary thresholds, scorecards or decision rules;
- employee, customer, branch or counterparty identifiers;
- credentials, connection strings and infrastructure details;
- internal reports, screenshots, logos and templates;
- distributions that could allow confidential figures to be reconstructed;
- copied code whose ownership is unclear.

## Required checks

1. Replace domain-specific identifiers with neutral names.
2. Generate synthetic data independently of real distributions.
3. Search files and Git history for blocked terms.
4. Review comments, filenames, metadata and screenshots.
5. Confirm that examples teach a pattern rather than expose an implementation.
6. Obtain an independent review before publication when sensitivity is uncertain.

## Safe default

If a detail is not necessary to teach the public pattern, remove it.

