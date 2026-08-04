# Jane / iHeartJane (iheartjane)

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

Jane Technologies (iHeartJane) is a cannabis ecommerce and marketplace platform that powers real-time online menus, point-of-sale and kiosk checkout, order and reservation flows, and the Jane Universal Product Catalog for 2,500+ dispensaries and brands across the United States and Canada. Consumers shop local products in real time at [iheartjane.com](https://www.iheartjane.com); retailers publish menus, run POS, and manage inventory through Jane for Business.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/iheartjane/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/iheartjane/refs/heads/main/apis.yml)

## Access Model (read this first)

Jane's developer surfaces are **real but partner-gated**. There is no open, self-service, unauthenticated public API:

- **Jane API** — a documented HTTP API published as a Swagger UI at [api.iheartjane.com/jane-api-docs](https://api.iheartjane.com/jane-api-docs/index.html), covering retrieval of live store menu products and generation of access tokens. The docs host and the API itself sit behind Cloudflare bot protection and require credentials issued by a Jane account representative.
- **Jane DM SDK** — a TypeScript/JavaScript Digital Merchandising SDK documented at [dm-sdk-docs.iheartjane.com](https://dm-sdk-docs.iheartjane.com). It explicitly "requires approval from Jane to enable on your menus." Initialization identifiers, package name, and endpoints are provisioned on approval.
- **Integrations** — Jane also offers tailored, POS-driven menu integrations (70+ POS systems) and syncs menus to Leafly and Weedmaps, arranged through partnership rather than a public API key.

Because both surfaces are gated behind approval and Cloudflare, the endpoints captured in `apis.yml` are **modeled from Jane's public documentation** (`endpointsModeled: true`) rather than exercised against a live open API. No OpenAPI, pricing, rate-limit, or FinOps artifacts are asserted here, to avoid fabricating a surface that cannot be independently verified.

## Tags

- Cannabis
- Ecommerce
- Marketplace
- Dispensary
- Menu
- Products
- Retail
- Point of Sale
- Personalization

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### Jane Menu Products API

Jane's documented HTTP API (Swagger UI at `api.iheartjane.com/jane-api-docs`) for retrieving live store menu products and generating the access tokens used to authenticate downstream calls. Surfaces a dispensary's real-time menu, brands, categories, and pricing from the Jane Universal Product Catalog. Partner-gated; operations are modeled from Jane's public documentation.

- **Human URL:** [https://api.iheartjane.com/jane-api-docs/index.html](https://api.iheartjane.com/jane-api-docs/index.html)
- **Base URL:** `https://api.iheartjane.com`
- **Endpoints modeled:** yes (access-gated)

#### Tags

- Menu
- Products
- Catalog
- Stores

#### Properties

- [API Reference](https://api.iheartjane.com/jane-api-docs/index.html)
- [Documentation](https://www.iheartjane.com/business/integrations)

### Jane Digital Merchandising SDK (Jane DM SDK)

A TypeScript/JavaScript library (client-side React/Angular/Vue and server-side Node.js/Express) that embeds MyHigh-powered personalization and publisher monetization widgets into a retailer's own menu: a Recommended Row of personalized products, a Recommended Sort for search ranking, a single-brand Top of Menu sponsored row, and a Cart Topper of sponsored and organic recommendations. Requires approval from Jane to enable on a menu.

- **Human URL:** [https://dm-sdk-docs.iheartjane.com/docs/api/](https://dm-sdk-docs.iheartjane.com/docs/api/)
- **Base URL:** `https://dm-sdk-docs.iheartjane.com`
- **Endpoints modeled:** yes (approval-gated SDK)

#### Tags

- Personalization
- Merchandising
- Advertising
- Widgets
- SDK

#### Properties

- [API Reference](https://dm-sdk-docs.iheartjane.com/docs/api/)
- [Documentation](https://dm-sdk-docs.iheartjane.com/docs/app/intro/)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/jane-technologies-inc)
- [Website](https://www.iheartjane.com)
- [Documentation](https://dm-sdk-docs.iheartjane.com)
- [Integrations](https://www.iheartjane.com/business/integrations)
- [Developer Portal](https://api.iheartjane.com/jane-api-docs/index.html)

## Pricing

Jane does not publish flat, self-service pricing. Third-party listings describe a quote-based, success/revenue-oriented model for retailers (contact Jane for a tailored quote); there is no public developer-tier price sheet. No `plans/` artifact is asserted here for that reason.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
