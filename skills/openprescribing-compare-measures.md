---
name: Compare prescribing-quality measures across organisations
description: Look up an NHS organisation and compare its standardised prescribing-quality/safety measures against national and peer values.
api: openapi/openprescribing-openapi.yml
operations: [getOrgCodes, getMeasures, getMeasureByPractice, getMeasureBySicbl]
---

# Compare prescribing-quality measures across organisations

Public key-less API. Base URL: `https://openprescribing.net/api/1.0`. All GET; `?format=json|csv`.

## Steps

1. **Find the organisation.** Call `getOrgCodes` (`GET /org_code/?q=<name-or-code>&org_type=<type>`) to resolve a practice, PCN, Sub-ICB Location (CCG), ICB (STP) or Regional Team to its NHS code.

2. **Get the national baseline for a measure.** Call `getMeasures` (`GET /measure/?measure=<measure_id>`) for the all-England value of one or more standardised measures. Use `?tags=<tag>` to filter by measure tag.

3. **Get the organisation's values.** Call the matching level:
   - `getMeasureByPractice` — `GET /measure_by_practice/?org=<code>&measure=<measure_id>`
   - `getMeasureBySicbl` — `GET /measure_by_sicbl/?org=<code>&measure=<measure_id>`
   Each row includes `numerator`, `denominator`, `calc_value` and (where available) `percentile` per month, so you can rank the organisation against peers.

4. **Explain a value (optional).** Call `getMeasureNumeratorsByOrg` (`GET /measure_numerators_by_org/?measure=<measure_id>&org_type=<type>&org=<code>`) to see the individual presentations driving the measure's numerator.

## Conventions & errors
- `measure`, `tags` and `org` accept comma-separated lists.
- Missing required `measure`/`org` returns `400`. See `errors/openprescribing-problem-types.yml`.
