---
name: Analyse prescribing spending for a drug
description: Find the BNF code for a drug and retrieve its NHS primary-care prescribing spending over time, nationally or by organisation.
api: openapi/openprescribing-openapi.yml
operations: [getBnfCodes, getSpending, getSpendingByOrg]
---

# Analyse prescribing spending for a drug

The OpenPrescribing API is public and key-less — no authentication header is required. Base URL: `https://openprescribing.net/api/1.0`. All requests are HTTP GET; add `?format=json` (default) or `?format=csv`.

## Steps

1. **Resolve the BNF code.** Call `getBnfCodes` (`GET /bnf_code/?q=<name>`) with the drug/chemical/section name. Each result has a `type` (BNF chapter/section/paragraph/chemical/product/product format), an `id` (the BNF code) and a `name`. Pick the code at the granularity you want (e.g. a chemical code like `0212000AA` for all rosuvastatin, or a presentation code for a specific formulation).

2. **Get national spending.** Call `getSpending` (`GET /spending/?code=<bnf_code>`) to retrieve total spending, quantity and items by month across the last five years of data for that code. You can pass multiple codes comma-separated.

3. **Break down by organisation (optional).** Call `getSpendingByOrg` (`GET /spending_by_org/?code=<bnf_code>&org_type=<type>`) where `org_type` is one of `practice`, `pcn`, `ccg`/`sicbl`, `stp`/`icb`, `regional_team`. Add `&org=<code,code>` to restrict to specific organisations.

## Conventions & errors
- Multi-value params (`code`, `org`) are comma-separated.
- An unknown organisation code returns `400 {"detail": "Unknown organisation ID: ..."}`; an unrecognised `org_type` returns `400`. See `errors/openprescribing-problem-types.yml`.
- Data covers a rolling ~5-year window; results are monthly.
