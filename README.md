# Tohoku University (tohoku)

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
