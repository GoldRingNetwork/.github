# Gold Ring Network

**GOLD v2 is live** at [goldring.top](https://goldring.top)

One Minecraft project — Hub + main world, guilds, events, shop.  
**One backend JVM** (`gold-api`). Worlds protected. GitOps via ArgoCD.

```
:25565  →  Velocity  →  Hub  →  gr-main
:443    →  edge  →  gold-website  ·  gold-api
```

---

## Active repositories

| Repo | Role |
|------|------|
| **[gold-api](https://github.com/GoldRingNetwork/gold-api)** | Unified backend — auth, API, billing · **1 JVM** |
| **[gold-website](https://github.com/GoldRingNetwork/gold-website)** | Next.js site — events, guilds, shop, profile |
| **[gold-infra](https://github.com/GoldRingNetwork/gold-infra)** | GitOps cluster · Helm · ArgoCD · api-edge |
| **[gold-plugins](https://github.com/GoldRingNetwork/gold-plugins)** | Paper / Velocity plugins monorepo |
| **[gold-game](https://github.com/GoldRingNetwork/gold-game)** | Purpur chart · tenants · resource packs |
| **[gold-docs](https://github.com/GoldRingNetwork/gold-docs)** | Architecture · cutover · world protection |

---

## How we ship

| Principle | Reality |
|-----------|---------|
| **GitOps** | Code → CI → chart tags → ArgoCD. No hand edits in cluster |
| **Single backend** | `gold-api` only — multi `gr-*-svc` cutover complete |
| **Worlds** | `hub-data` + `gr-main-data` · **Bound · Retain · protect=world** |
| **Prod** | `goldring.top` · always `main` |

---

## Archived

The multi-tenant platform era is **closed**.

~35 `gr-*` repos (microservices, Istio mesh, minigames, marketplace tooling) are **archived**.  
GOLD v2 runs exclusively on the six `gold-*` repos above.

---

**Play** · [goldring.top](https://goldring.top)  
**API** · `api.goldring.top`  
**Docs** · [gold-docs](https://github.com/GoldRingNetwork/gold-docs)
