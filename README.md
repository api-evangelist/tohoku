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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Tohoku University is a Japanese national research university in Sendai, founded in 1907 — one of the seven former Imperial Universities and a Designated National University. This repository catalogs the university's public, machine-readable footprint as an [APIs.json](https://apisjson.org) profile, and it settles **who operates each surface** before crediting any of them to the institution.

The honest shape is small and uneven. Exactly one unambiguously institution-operated API was found: **jMorp**, the Japanese Multi Omics Reference Panel published by the Tohoku Medical Megabank Organization, which answers anonymous GraphQL queries and full schema introspection. Everything else is a *relationship* rather than a contract — a tenant repository on NII's JAIRO Cloud, a Shibboleth IdP in the GakuNin federation, Crossref and ROR registrations. There is no central developer portal, no API key issuance, no open-data platform, no `llms.txt`, no MCP server and no published OpenAPI anywhere on `tohoku.ac.jp`.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/tohoku/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=tohoku-api-evangelist&utm_content=repo

## Type

- University / Public Research University / Index / Consumer / 3rd-Party

## Tags

University, Higher Education, Education, Research, Japan, National University, Public Research University, Genomics, Research Data, Institutional Repository, Identity Federation, Course Catalog, Library, Open Access, OAI-PMH, GraphQL

## Surfaces, and who operates them

Every entry carries an operator. `institution` means Tohoku University runs the thing the contract describes; `tenant` means the institution's data on someone else's platform; `federation` and `registry` mean the institution's own relationship inside a surface that is shared by design.

| Surface | Operator | Verified |
|---|---|---|
| **jMorp GraphQL API** — `https://jmorp.megabank.tohoku.ac.jp/api/graphql` | `institution` | Anonymous introspection (6.7 MB, 4,470 types, 305 query-root fields) plus two live domain queries, 2026-09-01 |
| **TOUR Institutional Repository OAI-PMH** — `https://tohoku.repo.nii.ac.jp/oai` | `tenant` | Identify / ListMetadataFormats / ListSets, HTTP 200, 2026-09-01 |
| **GakuNin Shibboleth IdP** — `https://idp.auth.tohoku.ac.jp/idp/shibboleth` | `federation` | EntityDescriptor found in the GakuNin aggregate metadata, 2026-09-01 |
| **Crossref DOI membership** — members 622, 1484, 2470 | `registry` | `api.crossref.org`, live DOI counts, 2026-09-01 |
| **ROR record** — `https://ror.org/01dq60k83` | `registry` | `api.ror.org`, HTTP 200, 2026-09-01 |

### jMorp — the one API that is actually theirs

Published by the Tohoku Medical Megabank Organization (ToMMo), an institute of the university, on the university's own registrable domain. Read-only: a `query_root` with 305 fields and a `subscription_root`, no mutation root. Coverage spans variants (ClinVar, dbNSFP, dbSNP, GATK CNV, ExpansionHunter), GENCODE gene models with Entrez / UniProt / RefSeq / PDB / HGNC cross-references, and a dataset catalog whose `dtaRequired` flag marks controlled-access data. No authentication, no API key, no rate-limit headers, no published OpenAPI, and no vendor documentation of the interface — the schema in this repository is **our** reconstruction from introspection, marked `method: probed`.

- Schema (SDL, 1.36 MB): [graphql/tohoku-jmorp-schema.graphql](graphql/tohoku-jmorp-schema.graphql)
- Notes: [graphql/tohoku-jmorp-graphql.md](graphql/tohoku-jmorp-graphql.md)
- Examples: [datasets](examples/tohoku-jmorp-datasets-example.json), [gene lookup](examples/tohoku-jmorp-gene-lookup-example.json)

## Artifacts

- Authentication: [authentication/tohoku-authentication.yml](authentication/tohoku-authentication.yml)
- Errors: [errors/tohoku-jmorp-errors.yml](errors/tohoku-jmorp-errors.yml)
- Conformance: [conformance/tohoku-conformance.yml](conformance/tohoku-conformance.yml)
- Plans: [plans/tohoku-plans-pricing.yml](plans/tohoku-plans-pricing.yml)
- Rate limits: [rate-limits/tohoku-rate-limits.yml](rate-limits/tohoku-rate-limits.yml)
- FinOps: [finops/tohoku-finops.yml](finops/tohoku-finops.yml)
- Review: [review.yml](review.yml)

## Education-regime conformance

Scored against the Kin Score `education` regime. Implemented: **OAI-PMH 2.0** (tenant), **Shibboleth** and **SAML 2.0** (federation), **Crossref** (registry), plus JPCOAR 1.0/2.0, Dublin Core, DDI and IEEE LOM metadata profiles on the repository. Not implemented: **DataCite** (zero providers match Tohoku — Japanese repositories mint through JaLC), **ORCID** (no institutional membership evidenced from a machine-readable source), **LTI**, **SCIM**, **OneRoster**, **Ed-Fi**, **Caliper**, **QTI**. Absences are recorded as `conforms: false` with evidence rather than omitted.

## Common Properties

- Website: https://www.tohoku.ac.jp/en/
- GitHub organization (Tohoku NLP Group, 72 public repos): https://github.com/cl-tohoku
- LinkedIn: https://www.linkedin.com/school/tohoku-univ/
- Privacy policy: https://www.tohoku.ac.jp/en/misc/privacy_policy.html
- Support / contact: https://www.tohoku.ac.jp/en/misc/contact.html
- News: https://www.tohoku.ac.jp/en/news/
- Open-access documentation: https://www.library.tohoku.ac.jp/support/openaccess/
- Research repository (TOUR): https://tohoku.repo.nii.ac.jp/
- Library catalog (OPAC): https://opac.library.tohoku.ac.jp/opac/opac_search/?lang=1&smode=1
- Course catalog (QuickSyllabus, no login): https://qsl.cds.tohoku.ac.jp/qsl/
- Identity federation (GakuNin metadata): https://metadata.gakunin.nii.ac.jp/gakunin-metadata.xml
- Research computing (Cyberscience Center): https://www.cc.tohoku.ac.jp/en/
- AI policy (generative-AI guidance for staff): https://olg.cds.tohoku.ac.jp/forstaff/ai-tools

## Timestamps

- Created: 2026-06-03
- Modified: 2026-09-01

## Notes

- Only publicly verifiable resources are cataloged, and every claim here was re-probed on 2026-09-01. No endpoints were fabricated.
- **No vendor contract is saved under this institution.** TOUR's OAI-PMH endpoint is implemented by NII JAIRO Cloud (WEKO3); the relationship is recorded, the vendor's contract is not.
- The GakuNin IdP entity is Tohoku University's, but its SSO endpoint is hosted for the university by SECIOSS (`slink.secioss.com`). Both facts are recorded rather than one being hidden.
- A second Tohoku University entity is registered in GakuNin as a Service Provider — the Corona Vaccine Reservation System — whose host no longer resolves. It is stale federation metadata for a retired service.
- `cl-tohoku` is the Tohoku NLP research group's GitHub organization, not central institutional IT. Other research code lives in individual lab organizations.
- The library OPAC is a public web interface with no documented API. QuickSyllabus is a public, no-login course catalog served as HTML with no JSON interface behind it. The UNIPA guest syllabus entry point was in scheduled maintenance (HTTP 503) at the time of the re-profile.
- `data.tohoku.ac.jp`, `opendata.tohoku.ac.jp` and `api.tohoku.ac.jp` do not resolve. There is no open-data portal.

## Maintainers

- Kin Lane — kin@apievangelist.com
