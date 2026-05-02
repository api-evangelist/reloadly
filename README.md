# Reloadly

Reloadly is a global digital rewards and payments platform providing APIs for sending digital gift cards, airtime top-ups, and data bundles worldwide. The platform connects businesses to 3,000+ gift card brands across 14,000+ products in 140+ countries, and enables mobile airtime delivery across 800+ operators in 170+ countries.

Authentication uses OAuth 2.0 client credentials with separate sandbox and production environments. SDKs are available for Node.js, PHP, Python, Go, Java, and C#.

## Links

- **Website:** https://www.reloadly.com
- **Documentation:** https://docs.reloadly.com
- **Dashboard:** https://dashboard.reloadly.com
- **GitHub:** https://github.com/reloadly
- **Support:** https://support.reloadly.com

## APIs

### Gift Cards API
- **Base URL (Production):** https://giftcards.reloadly.com
- **Base URL (Sandbox):** https://giftcards-sandbox.reloadly.com
- **Documentation:** https://docs.reloadly.com/gift-cards
- **OpenAPI:** [openapi/reloadly-gift-cards-openapi.yml](openapi/reloadly-gift-cards-openapi.yml)

### Airtime API
- **Base URL (Production):** https://topups.reloadly.com
- **Base URL (Sandbox):** https://topups-sandbox.reloadly.com
- **Documentation:** https://docs.reloadly.com/airtime
- **OpenAPI:** [openapi/reloadly-airtime-openapi.yml](openapi/reloadly-airtime-openapi.yml)

## Authentication

All APIs use OAuth 2.0 client credentials:

```
POST https://auth.reloadly.com/oauth/token
{
  "client_id": "YOUR_CLIENT_ID",
  "client_secret": "YOUR_CLIENT_SECRET",
  "grant_type": "client_credentials",
  "audience": "https://giftcards.reloadly.com"
}
```

Tokens are valid 60 days (production) or 24 hours (sandbox).

## Artifacts

| Type | File |
|---|---|
| OpenAPI (Gift Cards) | [openapi/reloadly-gift-cards-openapi.yml](openapi/reloadly-gift-cards-openapi.yml) |
| OpenAPI (Airtime) | [openapi/reloadly-airtime-openapi.yml](openapi/reloadly-airtime-openapi.yml) |
| JSON Schema (Product) | [json-schema/reloadly-product-schema.json](json-schema/reloadly-product-schema.json) |
| JSON Schema (Order) | [json-schema/reloadly-order-schema.json](json-schema/reloadly-order-schema.json) |
| JSON Structure | [json-structure/reloadly-product-structure.json](json-structure/reloadly-product-structure.json) |
| JSON-LD Context | [json-ld/reloadly-context.jsonld](json-ld/reloadly-context.jsonld) |
| Spectral Rules | [rules/reloadly-rules.yml](rules/reloadly-rules.yml) |
| Vocabulary | [vocabulary/reloadly-vocabulary.yml](vocabulary/reloadly-vocabulary.yml) |

## Capabilities

| Capability | Description |
|---|---|
| [digital-rewards.yaml](capabilities/digital-rewards.yaml) | Unified gift cards + airtime workflow for rewards programs |
| [shared/gift-cards.yaml](capabilities/shared/gift-cards.yaml) | Gift Cards API shared definition |
| [shared/airtime.yaml](capabilities/shared/airtime.yaml) | Airtime API shared definition |

## Examples

- [List Products](examples/reloadly-list-products-example.json)
- [Place Order](examples/reloadly-place-order-example.json)
- [Send Top-Up](examples/reloadly-send-topup-example.json)
