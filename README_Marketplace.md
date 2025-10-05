# PublicAccess Marketplace (Marketplace.Media + Buyers.chat + WCIBuy.com)

**Goal:** Shopify-style commerce layer that aggregates local merchants and syndicated offers to **LocalCommerce.news**, **LocalClassified.news**, **LocalShopper.news**, and **DailyShopper.news**, with discovery via **WCIBuy.com** and conversation/UI via **Buyers.chat**.

## Core Tenets
- **Multi-tenant:** Each town/region (and network) is a tenant.
- **Bring-your-own-store:** Merchants connect Shopify/WooCommerce or upload CSV.
- **Local-first discovery:** WCIBuy.com powers geolocated search and facets.
- **Syndication -> News:** Auto-generate posts for .news channels using templates.
- **Conversation UI:** Buyers.chat provides ask/answer, lead capture, and cart-to-merchant.
- **Moderation:** Admins approve classified and merchant onboarding.

## MVP Scope
1. Merchant onboarding (Connect Shopify).
2. Product/Inventory sync (webhooks).
3. WCIBuy search index + storefront views.
4. Auto-post to LocalCommerce.news & DailyShopper.news.
5. Classifieds submission + moderation queue.
6. Buyers.chat storefront: product grid, PDP, lead form, cart -> external checkout.

## V1 Enhancements
- Stripe Connect payouts; BOPIS; promotions/ads; Woo importer; AI enrichment with aiLocal.chat.

## Data Model
See `marketplace_schema.sql`.

## APIs
See `marketplace_api.yaml`. Gateway fronts ingestion, search, and syndication.

## Domain Wiring
Primary apps: Buyers.chat (UI), Marketplace.Media (merchant + admin), WCIBuy.com (search).
News channels: localcommerce.news, localclassified.news, localshopper.news, dailyshopper.news.
Catalogues: mapped per sheet in the uploaded workbook; see `marketplace_domain_inventory.csv`.

## Search & SEO
- WCIBuy index: facets (category, price, availability, distance, merchant).
- Per-town SEO pages: /city/{slug}/category/{slug} with canonical links to .news posts.

## Moderation & Editorial
- Admin can promote offers to homepage hero on .news sites.
- Classified posts require approval; merchants whitelisted per tenant.

## Privacy/Compliance
- CCPA/GDPR data export & deletion.
- Clear labeling of paid promotions.

