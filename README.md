# Tohoku University (tohoku)

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

Tohoku University is a national research university in Sendai, Japan, founded in 1907 and ranked #107 in the QS World University Rankings 2025. This repository catalogs the university's public, machine-readable developer/API footprint as an [APIs.json](https://apisjson.org) profile. The verified footprint is centered on scholarly infrastructure: the TOUR (TOhoku University Repository) institutional repository exposes a live OAI-PMH 2.0 metadata endpoint via NII's JAIRO Cloud (WEKO3). No central developer portal or open-data platform was found publicly documented.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/tohoku/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=tohoku-api-evangelist&utm_content=repo

## Type

- Index / Consumer / 3rd-Party

## Tags

Education, Higher Education, University, Research, Japan, Open Access, Institutional Repository, OAI-PMH, Library

## APIs

- **TOUR Institutional Repository OAI-PMH** — OAI-PMH 2.0 metadata harvesting for the TOhoku University Repository (WEKO3 / JAIRO Cloud). Verified live (Identify, ListMetadataFormats). Base URL: `https://tohoku.repo.nii.ac.jp/oai`.
  - Docs: https://www.library.tohoku.ac.jp/support/openaccess/
  - Repository: https://tohoku.repo.nii.ac.jp/

## Plans

- [plans/tohoku-plans-pricing.yml](plans/tohoku-plans-pricing.yml)

## Rate Limits

- [rate-limits/tohoku-rate-limits.yml](rate-limits/tohoku-rate-limits.yml)

## FinOps

- [finops/tohoku-finops.yml](finops/tohoku-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.tohoku.ac.jp/en/
- GitHub (Tohoku NLP research group): https://github.com/cl-tohoku
- LinkedIn: https://www.linkedin.com/school/tohoku-univ/
- Library: https://www.library.tohoku.ac.jp/en/
- Catalog (OPAC): https://opac.library.tohoku.ac.jp/opac/opac_search/?lang=1&smode=1
- Review: [review.yml](review.yml)

## Notes

- Only publicly verifiable resources are cataloged. The TOUR OAI-PMH endpoint was confirmed live on 2026-06-03 (valid Identify and ListMetadataFormats responses).
- No central, self-service API developer portal, open-data platform, course/timetable/SIS API, or documented SSO/OAuth client-registration program was found publicly.
- The library OPAC is a public web interface; no documented public API was confirmed. The WEKO3 search endpoint returned HTTP 400 and is not cataloged.
- `cl-tohoku` is the Tohoku NLP research group GitHub org, not central institutional IT; other research code lives in individual lab orgs.
- No endpoints were fabricated.

## Maintainers

- Kin Lane — kin@apievangelist.com
