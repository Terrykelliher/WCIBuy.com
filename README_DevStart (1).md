# PublicAccess Marketplace — Developer Quick-Start (v0.2, 2025-10-05)

## What’s here
- TypeScript/Express API skeleton (`api/`)
- Routes: products search, merchants, classifieds, Shopify webhook
- Scripts: Shopify OAuth stub
- `package.json`, `tsconfig.json`

## Run locally
```bash
npm install
npm run dev
# GET http://localhost:3000/health
```

## Next tasks
1. Wire `/products/search` to WCIBuy index (Algolia/Elastic equivalent).
2. Implement Shopify HMAC verification and topic routing.
3. Connect persistence (Postgres using schema provided earlier).
4. Add `/posts/publish` to push to .news CMS.
5. Build moderation endpoints and auth (tenant admin/editor).
