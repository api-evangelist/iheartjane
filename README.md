# Jane / iHeartJane (iheartjane)

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
