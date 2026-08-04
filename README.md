# EarthOptics

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

EarthOptics is a soil data measurement and mapping company headquartered in Minneapolis, Minnesota. It combines proprietary in-field proximal sensing hardware, robotics, genomics and laboratory testing with machine learning to produce high-resolution sub-field maps of soil compaction, fertility and nutrients, soil biology, moisture and soil organic carbon from far fewer physical samples than conventional soil testing. Results are delivered through the 360 PRO customer dashboard and a dealer network. EarthOptics merged with soil-biology company Pattern Ag and reports having mapped more than five million acres.

- Website: https://earthoptics.com/
- Application: https://app.earthoptics.com/
- GitHub: https://github.com/EarthOptics
- Secondary market listing: https://forgeglobal.com/earth-optics_stock/

## API posture

EarthOptics has **no public API program** — no developer portal, no API reference, no SDKs, and no self-serve API signup.

A private REST API exists at `https://api.earthoptics.com`, backing the 360 PRO application. It runs Django REST Framework behind gunicorn and exposes a drf-spectacular OpenAPI schema at `/api/schema/` and a Swagger UI at `/api/docs/` — both return HTTP 401 behind a Bearer JWT (`WWW-Authenticate: Bearer realm="api"`). The machine-readable contract therefore exists but is not publicly retrievable, so no OpenAPI has been captured here.

Artifacts in this repo record what was probed on 2026-08-01, including the negatives: no GraphQL, no gRPC, no AsyncAPI or webhooks, no MCP server, no A2A agent card, no status page, no changelog, and no compliance/trust center. See `apis.yml` for the full pointer set.
