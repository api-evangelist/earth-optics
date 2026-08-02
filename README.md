# EarthOptics

EarthOptics is a soil data measurement and mapping company headquartered in Minneapolis, Minnesota. It combines proprietary in-field proximal sensing hardware, robotics, genomics and laboratory testing with machine learning to produce high-resolution sub-field maps of soil compaction, fertility and nutrients, soil biology, moisture and soil organic carbon from far fewer physical samples than conventional soil testing. Results are delivered through the 360 PRO customer dashboard and a dealer network. EarthOptics merged with soil-biology company Pattern Ag and reports having mapped more than five million acres.

- Website: https://earthoptics.com/
- Application: https://app.earthoptics.com/
- GitHub: https://github.com/EarthOptics
- Secondary market listing: https://forgeglobal.com/earth-optics_stock/

## API posture

EarthOptics has **no public API program** — no developer portal, no API reference, no SDKs, and no self-serve API signup.

A private REST API exists at `https://api.earthoptics.com`, backing the 360 PRO application. It runs Django REST Framework behind gunicorn and exposes a drf-spectacular OpenAPI schema at `/api/schema/` and a Swagger UI at `/api/docs/` — both return HTTP 401 behind a Bearer JWT (`WWW-Authenticate: Bearer realm="api"`). The machine-readable contract therefore exists but is not publicly retrievable, so no OpenAPI has been captured here.

Artifacts in this repo record what was probed on 2026-08-01, including the negatives: no GraphQL, no gRPC, no AsyncAPI or webhooks, no MCP server, no A2A agent card, no status page, no changelog, and no compliance/trust center. See `apis.yml` for the full pointer set.
