# Quarantined: conceptual GraphQL schema (NOT published by Electronic Arts)

Quarantined 2026-09-06 by the API Evangelist enrichment pipeline.

`electronic-arts-schema.graphql` and `electronic-arts-graphql.md` were written by API Evangelist,
not by Electronic Arts. The accompanying markdown says so in its own words:

> "This is a **conceptual** GraphQL schema for Electronic Arts (EA) gaming and player services.
> Electronic Arts does not currently publish a public developer API portal; this schema is derived
> from known EA service surfaces … documented through reverse engineering and public research."

It was nevertheless wired into `apis.yml` as `type: GraphQL`, which asserts to every reader — and to
the Kin Score — that EA publishes a GraphQL API. EA does not. Contract discovery on 2026-09-06 found
no GraphQL endpoint on any EA host, and EA's only API programme (the EA SPORTS FC Community API) is
an approved-partner OAuth surface with no published schema of any kind.

Action taken:

- Files moved here, to `graphql/_scaffold/`, rather than deleted — the audit trail is the point.
- The `type: GraphQL` pointer was removed from `apis.yml`.

Do not re-wire these files into `apis.yml`. If EA ever publishes a real schema, harvest it verbatim
into `graphql/` and register that.
