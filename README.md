# Tohoku University

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

Tohoku University is a Japanese national research university in Sendai, founded in 1907, one of the seven former Imperial Universities and a Designated National University. Its programmable footprint is small, unevenly distributed, and mostly NOT operated by central IT — which is the honest shape for a university, and the profile says so rather than padding it. Exactly one unambiguously institution-operated API was found: jMorp, the Japanese Multi Omics Reference Panel published by the Tohoku Medical Megabank Organization at jmorp.megabank.tohoku.ac.jp, which answers anonymous GraphQL queries and full schema introspection over a 305-field read-only query root. Everything else is a relationship rather than a contract: the TOUR institutional repository is a tenant on NII's JAIRO Cloud (WEKO3) with a live OAI-PMH 2.0 endpoint; the university operates its own SAML 2.0 Shibboleth Identity Provider registered in the GakuNin national academic federation; and three of its units are Crossref DOI-registering members. There is no central developer portal, no API key issuance, no open-data platform, no llms.txt, no MCP server and no published OpenAPI anywhere on tohoku.ac.jp. Public course information is served as HTML by the university's own QuickSyllabus, not as an API.

**Areas:** University · Higher Education · Education · Research · Japan · National University · Public Research University · Genomics · Research Data · Institutional Repository · Identity Federation · Course Catalog

## Tohoku University on APIs.io

Everything profiled for Tohoku University is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/tohoku/](https://apis.io/providers/tohoku/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [jMorp GraphQL API (Tohoku Medical Megabank Organization)](https://apis.io/apis/tohoku/jmorp-graphql/) — Public, anonymous, read-only GraphQL API for jMorp — the Japanese Multi Omics Reference Panel published by the Tohoku Medical Megabank Organization (ToMMo),…
- [TOUR Institutional Repository OAI-PMH](https://apis.io/apis/tohoku/tour-oai-pmh/) — OAI-PMH 2.0 metadata harvesting endpoint for TOUR (TOhoku University Repository). The collection, the departmental set hierarchy and the administrative…
- [GakuNin Shibboleth Identity Provider](https://apis.io/apis/tohoku/gakunin-shibboleth-idp/) — Tohoku University's own SAML 2.0 Identity Provider, registered in GakuNin — the Japanese academic access-management federation operated by NII. entityID…
- [Crossref DOI Registration Membership](https://apis.io/apis/tohoku/crossref-membership/) — Three Tohoku University units are Crossref members registering DOIs under their own prefixes, verified against api.crossref.org on 2026-09-01 — member 622…
- [ROR Organization Record](https://apis.io/apis/tohoku/ror-registration/) — Tohoku University's Research Organization Registry record, ROR ID 01dq60k83, carrying the English, romanized and Japanese names and the canonical…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [jMorp GraphQL API — Tohoku University (ToMMo)](https://apis.io/graphqls/tohoku/tohoku-jmorp-graphql/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Tohoku Context](https://apis.io/jsonld/tohoku/tohoku-context/)

#### Examples (3)

Example requests and responses.

- [Tohoku Jmorp Datasets Example](https://apis.io/examples/tohoku/tohoku-jmorp-datasets-example/)
- [Tohoku Jmorp Gene Lookup Example](https://apis.io/examples/tohoku/tohoku-jmorp-gene-lookup-example/)
- [Tohoku Tour Oai Pmh Identify Example](https://apis.io/examples/tohoku/tohoku-tour-oai-pmh-identify-example/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Tohoku Authentication](https://apis.io/security/tohoku/tohoku-authentication/)
- [Tohoku Domain Security](https://apis.io/security/tohoku/tohoku-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Tohoku Plans Pricing](https://apis.io/plans/tohoku/tohoku-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Tohoku Rate Limits](https://apis.io/rate-limits/tohoku/tohoku-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Tohoku Finops](https://apis.io/finops/tohoku/tohoku-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.tohoku.ac.jp/en/)
- [Documentation](https://www.library.tohoku.ac.jp/support/openaccess/)
- [Support](https://www.tohoku.ac.jp/en/misc/contact.html)
- [Blog](https://www.tohoku.ac.jp/en/news/)
- [Privacy policy](https://www.tohoku.ac.jp/en/misc/privacy_policy.html)
- [GitHub](https://github.com/cl-tohoku)

## API Evangelist rating

**Kin Score 23.0** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 20.4 |
| Contract governance | 4.5 |
| Operational transparency | 7.9 |
| Developer ergonomics | 28.6 |
| Access clarity | 15.8 |

**Agent readiness 4.4** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 20.6** — Education & Research

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/tohoku/](https://apis.io/providers/tohoku/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Tohoku University: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/tohoku/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
