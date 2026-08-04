# OpenPrescribing (openprescribing)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
