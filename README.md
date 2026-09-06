# Electronic Arts (electronic-arts)

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

Electronic Arts (EA) is a global leader in digital interactive entertainment, developing and delivering games, content, and online services for internet-connected consoles, mobile devices, and personal computers. EA's portfolio includes franchises such as EA SPORTS FC, Madden NFL, Battlefield, The Sims, Apex Legends, and Need for Speed, supported by online services like the EA app, EA Play, and EA Help.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/electronic-arts/refs/heads/main/apis.yml)

## What Electronic Arts publishes

EA runs no public developer portal and publishes **no OpenAPI, GraphQL SDL, AsyncAPI, gRPC/Protobuf or WSDL contract** on any host. Contract discovery on 2026-09-06 probed `www.ea.com`, `ea.com`, `help.ea.com`, `ir.ea.com`, `api.ea.com`, `gateway.ea.com`, `accounts.ea.com`, `signin.ea.com`, `answers.ea.com` and `drop-api.ea.com`; every result, including the misses, is recorded in `well-known/electronic-arts-well-known.yml`.

Two things EA *does* publish are worth an integrator's attention:

- **EA Account OpenID Connect / OAuth 2.0** — `accounts.ea.com` serves a live OpenID Connect Discovery 1.0 document and RFC 8414 authorization-server metadata (both HTTP 200, `Last-Modified` 2026-09-02), plus the JWKS they reference. These three documents are the only machine-readable contract Electronic Arts publishes anywhere. Saved verbatim under `well-known/`.
- **EA SPORTS FC Community API** — announced 2026-07-27. A player grants an approved community site delegated read access to Ultimate Team data through EA's OAuth flow. Approved partners are FUT.GG, FUTBIN and FUTWIZ; EA states it is *not accepting further requests*. Partners may retain pulled data for at most 28 days. No base URL, endpoint list, scope reference or spec is published.

## Not published by Electronic Arts

No MCP server, no A2A agent card, no `security.txt`, no `api-catalog`, no `llms.txt` of EA's own, no API SDK on any package registry, no published rate limits, no API pricing, no API changelog, no CLI and no sandbox. EA's Maven Central and NuGet packages (`com.ea.async`, `com.ea.agentloader`, `com.ea.orbit`, `NetTAP`) are first-party engineering libraries, not API clients, and all last shipped between 2016 and 2019.

`graphql/_scaffold/` holds a **conceptual** GraphQL schema written by API Evangelist, not by EA. It was quarantined on 2026-09-06 and its `apis.yml` pointer removed; see `graphql/_scaffold/README.md`.

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Gaming, Video Games, Entertainment, Consumer, Player Services, Fortune 1000

## Timestamps

- **Created:** 2026-03-21
- **Modified:** 2026-09-06

## APIs

### Electronic Arts

Public-facing presence of Electronic Arts — corporate site, consumer game services, the EA app, EA Play and EA Help. Tracked as a Contract-position reference rather than a producer of public APIs.

**Human URL:** [https://www.ea.com](https://www.ea.com)

#### Properties

- [Website](https://www.ea.com)
- [Support](https://help.ea.com)
- [Careers](https://www.ea.com/careers)

### EA Account OpenID Connect / OAuth 2.0

EA's account authorization server: authorization code with PKCE S256, RS256 ID tokens, `openid`/`email`/`phone`/`profile` scopes. Client credentials are issued by EA; there is no public registration endpoint.

**Human URL:** [https://accounts.ea.com/.well-known/openid-configuration](https://accounts.ea.com/.well-known/openid-configuration)

**Base URL:** `https://accounts.ea.com/connect`

#### Properties

- [OpenID Connect discovery](https://accounts.ea.com/.well-known/openid-configuration)
- [Authentication](authentication/electronic-arts-authentication.yml)
- [OAuth scopes](scopes/electronic-arts-scopes.yml)
- [Well-known probe](well-known/electronic-arts-well-known.yml)

### EA SPORTS FC Community API

EA's only API programme. Player-delegated OAuth access to Ultimate Team data for three approved community sites; applications closed.

**Human URL:** [https://help.ea.com/en/articles/ea-sports-fc/community-api/](https://help.ea.com/en/articles/ea-sports-fc/community-api/)

#### Properties

- [Documentation](https://help.ea.com/en/articles/ea-sports-fc/community-api/)
- [Announcement (Pitch Notes, 2026-07-27)](https://www.ea.com/games/ea-sports-fc/fc-26/news/pitch-notes-fc26-community-api-update)
- [Authentication](authentication/electronic-arts-authentication.yml)
- [Support](https://help.ea.com)

## Common Properties

- [Electronic Arts Website](https://www.ea.com)
- [EA Help](https://help.ea.com)
- [EA Play](https://www.ea.com/ea-play)
- [EA Investor Relations](https://ir.ea.com)
- [EA Careers](https://www.ea.com/careers)
- [EA GitHub Organization](https://github.com/electronicarts)
- [EA server status](https://help.ea.com/en/server-status/)
- [EA Online Service Updates (service retirement policy)](https://www.ea.com/service-updates)
- [EA vulnerability disclosure policy](https://www.ea.com/security/disclosure)
- [EA User Agreement](https://www.ea.com/legal/user-agreement)
- [EA Privacy and Cookie Policy](https://www.ea.com/legal/privacy-and-cookie-policy)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
