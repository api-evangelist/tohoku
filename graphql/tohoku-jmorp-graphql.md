# jMorp GraphQL API — Tohoku University (ToMMo)

    generated: 2026-09-01
    method: derived
    x-derived-from: live GraphQL introspection, run 2026-09-01
    x-source-url: https://jmorp.megabank.tohoku.ac.jp/api/graphql
    x-operator: institution

## What this is

jMorp (Japanese Multi Omics Reference Panel) is the public reference-panel portal published by the
**Tohoku Medical Megabank Organization (ToMMo)**, an institute of Tohoku University. It runs on the
university's own registrable domain (`megabank.tohoku.ac.jp`), so under the university pipeline's
operator axis it is `x-operator: institution` — this is Tohoku University's own engineering, not a
vendor contract running under its name.

It is the only unambiguously institution-operated, machine-readable API found on Tohoku University's
public surface, and it was missed entirely by the 2026-06-03 profile.

## The endpoint

| | |
|---|---|
| Endpoint | `POST https://jmorp.megabank.tohoku.ac.jp/api/graphql` |
| Human portal | https://jmorp.megabank.tohoku.ac.jp/ |
| Transport | HTTP POST, `content-type: application/json` |
| Authentication | **None.** Anonymous queries are answered in full. |
| Introspection | **Enabled.** A full `__schema` introspection returns 6.7 MB of JSON. |
| Server | Apache in front of a Hasura-style GraphQL engine (`code: validation-failed`, `PersistedQueryNotSupported`) |
| Response headers | `x-request-id` (UUID) on every response; no rate-limit headers observed |

## The schema

Reconstructed into SDL at `graphql/tohoku-jmorp-schema.graphql` (1.36 MB, 4,459 type definitions)
from a live introspection query on 2026-09-01.

| | |
|---|---|
| Query root | `query_root`, **305 fields** |
| Subscription root | `subscription_root` (live-query streaming) |
| Mutation root | none — the API is read-only |
| Object types | 1,645 |
| Input object types | 2,336 (Hasura comparison/order-by boilerplate) |
| Enums | 479 |
| Custom scalars | 10 |

The domain is genomics and multi-omics reference data. Representative query fields:

- **Variant / genome** — `clinvar`, `dbnsfp`, `dbsnpToPosition`, `gatkCnvPosition`,
  `expansionHunterCount`, `snpeffGencodeLof`
- **Gene models** — `gencodeGene`, `gencodeTranscript`, `gencodeExonPosition`, `entrezGene`,
  `gencodeToUniprot`, `gencodeToPdb`, `gencodeToRefseq`
- **Datasets** — `dataset`, `datasetFile`, `datasetFileCategory` (each dataset carries a
  `dtaRequired` flag saying whether a Data Transfer Agreement is needed)
- Every entity also has an `…Aggregate` counterpart for count/avg/min/max/stddev/variance.

## Verified calls

Both queries below were run anonymously on 2026-09-01 and returned HTTP 200 with real data; the
full request/response pairs are saved in `examples/`.

```graphql
query Datasets { dataset(limit: 3, orderBy: {datasetId: ASC}) { datasetId name shortDescription dtaRequired } }
query Gene { gencodeGene(where: {gencodeSymbol: {_eq: "BRCA1"}}, limit: 2) { gencodeGeneIdBase gencodeSymbol gencodeGeneType gencodeLevel hgncId } }
```

## What is NOT here

- No published OpenAPI, no `/.well-known/` catalog, no llms.txt, no MCP server, no agent card.
- No developer portal, no key issuance, no documented rate limits or terms of use for the API.
- No SDL is published by ToMMo itself — the schema in this repo is **our** reconstruction from
  introspection, which is why it is marked `method: probed` and not `searched`.
- `/api/user/profile/` returns 403; there is an authenticated tier behind the portal login for
  controlled-access datasets (`dtaRequired: true`), which is not documented publicly.
