# OpenPrescribing (openprescribing)

OpenPrescribing.net is an open-data service built and operated by the Bennett Institute for Applied Data Science at the University of Oxford. It turns the English Prescribing Dataset published monthly by the NHS Business Services Authority into public dashboards, prescribing-safety measures, and a free RESTful API covering primary-care GP prescribing across England. It is an independent academic analytics platform layered on NHS open data — not an NHS FHIR clinical system. Currently no registration or API key is required.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/openprescribing/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/openprescribing/refs/heads/main/apis.yml)

## Tags

- Healthcare
- United Kingdom
- NHS
- Prescribing
- Pharmacy
- Open Data
- Primary Care
- Public Health
- Analytics

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### OpenPrescribing Spending API

Retrieve total prescribing spending, quantity and items across the last five years of the English Prescribing Dataset — by BNF code (section, chemical or presentation) and by NHS organisation (practice, PCN, Sub-ICB Location, ICB, Regional Team), plus drug-tariff, price-per-unit, ghost-generic and bubble-chart data. Returns JSON or CSV.

- **Human URL:** [https://openprescribing.net/api/](https://openprescribing.net/api/)
- **Base URL:** `https://openprescribing.net/api/1.0`

#### Tags

- Prescribing
- Spending
- Pharmacy

### OpenPrescribing Measures API

Standardised NHS prescribing-quality and safety measures (numerators, denominators and calculated values) at national, Regional Team, ICB, Sub-ICB Location, PCN and practice level. These endpoints power the OpenPrescribing measure dashboards and are served under the public `/api/1.0/` surface. Returns JSON or CSV.

- **Human URL:** [https://openprescribing.net/api/](https://openprescribing.net/api/)
- **Base URL:** `https://openprescribing.net/api/1.0`

#### Tags

- Prescribing
- Measures
- Public Health

### OpenPrescribing Information API

Reference-data lookups for the prescribing dataset — search BNF sections, chemicals and presentations by name or code; look up NHS organisations (Sub-ICB Location or practice) by code or name; retrieve list size and ASTRO-PU details; and fetch Sub-ICB Location boundaries or approximate practice locations as GeoJSON.

- **Human URL:** [https://openprescribing.net/api/](https://openprescribing.net/api/)
- **Base URL:** `https://openprescribing.net/api/1.0`

#### Tags

- Reference Data
- BNF
- Organisations

## Common Properties

- [Website](https://openprescribing.net/)
- [Developer Portal](https://openprescribing.net/api/)
- [Documentation](https://openprescribing.net/api/)
- [API Reference](https://openprescribing.net/api/)
- [About](https://openprescribing.net/about/)
- [Support / FAQ](https://openprescribing.net/faq/)
- [GitHub Organization](https://github.com/bennettoxford)
- [Source Code](https://github.com/bennettoxford/openprescribing)
- [Blog](https://www.bennett.ox.ac.uk/openprescribing/blog/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
