# Gold Ring Network

**GOLD v2** — один Minecraft‑продукт на [goldring.top](https://goldring.top): Hub + gr-main, гильдии, ивенты, магазин/донат.

```
Players → Velocity → hub | gr-main
Web/API → api-edge → gold-api (1 JVM)
Worlds  → PVC Bound · ReclaimPolicy Retain
```

## Active repositories

| Repo | Role |
|------|------|
| [**gold-api**](https://github.com/GoldRingNetwork/gold-api) | Unified Spring Boot backend (auth, social, mc, billing, media, JWT) |
| [**gold-website**](https://github.com/GoldRingNetwork/gold-website) | Next.js site — events, guilds, shop, profile |
| [**gold-infra**](https://github.com/GoldRingNetwork/gold-infra) | GitOps · Argo CD · Helm · nginx edge · netpol |
| [**gold-plugins**](https://github.com/GoldRingNetwork/gold-plugins) | Paper / Velocity plugins monorepo |
| [**gold-game**](https://github.com/GoldRingNetwork/gold-game) | Purpur chart, tenants hub/main, resource packs |
| [**gold-docs**](https://github.com/GoldRingNetwork/gold-docs) | Architecture, cutover, ops |

## Stack (live)

- **Backend:** single JVM `gold-api` · image `ghcr.io/goldringnetwork/gold-api`
- **Edge:** nginx `api-edge` · auth_request → `/auth/check` on gold-api
- **Data:** CNPG Postgres · Redis · NATS · MinIO
- **MC:** Purpur hub + gr-main · Velocity proxy
- **Deploy:** push → CI → chart tag → Argo CD (no hand kubectl on prod)

## Archived

Multi‑tenant / Istio / minigames / marketplace era lives in **~35 archived `gr-*` repos**.  
They stay for history — not product. Active work is **only** the six `gold-*` repos above.

## Site

**https://goldring.top**
