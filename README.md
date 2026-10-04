# Awesome-Cloud-Gaming-Platform

# Awesome-Cloud-Gaming-Platform

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Game Streaming, Remote Play, Low-Latency Video & Self-Hosted Cloud Gaming*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Gaming**. These tools help players stream games from remote servers to any device, and help developers build self-hosted cloud gaming services with low-latency video, input forwarding, and multi-client support.

**Examples** include Xbox Cloud Gaming, GeForce NOW, PlayStation Plus Cloud Streaming, Amazon Luna, Boosteroid, Shadow PC, Blacknut, Utomik Cloud, Antstream Arcade, and AirGPU (the category leaders).

**Open-source emphasis**: Cloud gaming has a **maturing open-source ecosystem**, though **no open-source alternative matches the global server footprint of commercial platforms**. **Sunshine** (GPL-3.0) is the de facto standard for self-hosted game streaming, pairing with **Moonlight** clients for low-latency remote play with hardware encoding on AMD, Intel, and NVIDIA GPUs . **CloudMorph** provides decentralized, self-hosted Windows application streaming in the browser with Docker-based deployment . **CloudRetro** (by the same author) offers a complete retro-game streaming solution . **Wolf** provides a Kubernetes-native game streaming platform for multi-user environments. This section documents these production-grade solutions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## 📖 Table of Contents

- [☁️ SaaS/Hosted Platforms](#-saas-hosted-platforms)
- [🔓 Open-Source GitHub Projects](#-open-source-github-projects)
- [🤝 How to Contribute](#-how-to-contribute)
- [⚠️ Disclaimer](#-disclaimer)

## ☁️ SaaS/Hosted Platforms

> **📊 Market Context**: The global cloud gaming market is estimated at **~$8.5B in 2026**, growing toward **~$35B by 2032** at a **~26% CAGR** (Mordor Intelligence / MarketsandMarkets estimates). The sector is **moderately concentrated** at the platform tier — Microsoft, NVIDIA, Sony, and Amazon each command significant segments, but **AI infrastructure cost inflation is reshaping the economics**: GeForce NOW imposed a **100-hour monthly cap** in January 2026, and Xbox Cloud Gaming began limiting playtime by membership tier . Microsoft's gaming division reported **$5.34B in quarterly revenue (down 7% YoY)** amid hardware declines, while cloud infrastructure carries more of the gaming experience . No single vendor holds a winner-take-all position; regional specialists (Boosteroid, Shadow, Blacknut) compete on price and catalog breadth.

| Platform | Description | Pricing (Starting Tier) | Free Tier Limits | Company Size |
|----------|-------------|------------------------|------------------|--------------|
| **[Xbox Cloud Gaming](https://www.xbox.com/cloud-gaming)** | Microsoft's cloud gaming service. Streams Game Pass titles and owned games to Xbox, PC, mobile, and browser. | **Game Pass Ultimate**: **$19.99/month** (includes cloud gaming, 100+ games, EA Play) . **Game Pass Essential**: **$9.99/month** (no cloud gaming) . | **Ad-supported free tier (Xbox Insiders beta)**: Stream **owned games** with **~2 minutes of pre-session ads**, **1-hour session limit**, save warnings at 10 and 5 minutes remaining . | **~$331.8B revenue (Microsoft FY2026)**  |
| **[GeForce NOW](https://www.nvidia.com/en-us/geforce-now/)** | NVIDIA's cloud gaming service. Streams PC games from Steam, Epic, and other stores. RTX 5080 rigs on Ultimate tier. | **Performance**: **$9.99/month** (1440p, 6-hour sessions) . **Ultimate**: **$19.99/month** (4K, 8-hour sessions, RTX 5080) . **India**: ₹999/month (Performance), ₹1,999/month (Ultimate) . | **Free tier**: Ad-supported, **1-hour sessions**, **1080p/60fps**, standard queue, "Basic" rig (4 vCPU, 14GB RAM) . **100-hour monthly cap** introduced 2026; unused hours roll over up to 15 hours . | **~$3.5T market cap (NVIDIA FY2026 est.)** |
| **[PlayStation Plus Premium](https://www.playstation.com/en-us/ps-plus/)** | Sony's top-tier subscription with cloud streaming for PS3 classics and select PS4/PS5 titles. Streams to PS4, PS5, and PC. | **Premium**: **$19.99/month**, **$159.99/year** (US) . **Extra**: $134.99/year (no streaming) . **Essential**: $79.99/year . | **No free tier**. **Premium required** for cloud streaming. **7-day free trial** available for new subscribers (region-dependent). | **~$30B gaming revenue (Sony FY2025 est.)** |
| **[Amazon Luna](https://luna.amazon.com/)** | Amazon's cloud gaming service. Channels include Luna+, Ubisoft+, Family, and Retro. GameNight included with Prime. | **Luna Premium**: **$9.99/month** . **Luna+ channel**: additional subscription. **Ubisoft+**, **Family**, **Retro** channels sold separately . | **Prime members**: Rotating selection of games via **Luna Standard** at **no extra cost** . **Luna Premium**: **7-day free trial** (new subscribers only) . | **~$638B revenue (Amazon FY2025)**  |
| **[Boosteroid](https://boosteroid.com/)** | Ukrainian cloud gaming service with broad PC game access. No published hour caps. US server presence across seven states. | **Ultra**: **€12.89/month** (€7.49/month billed annually) . **Ultra Pro**: **€14.89/month** (promotional €8.97/month) with ray tracing and 4K/120fps . | **No free tier** — testing requires paying at least one billing cycle . | **Private (~$10M+ raised est.)** |
| **[Shadow PC](https://shadow.tech/)** | Cloud computing service providing a full Windows PC in the cloud. Used for gaming, design, and development. | **Shadow PC**: **$19.99/month** (starting) . **Shadow Ultra** and **Infinite** tiers available at higher price points. | **No free tier**. **No free trial** . | **Private (~$100M+ raised est.)** |
| **[Blacknut](https://www.blacknut.com/)** | French cloud gaming service with a curated catalog of 500+ games. No downloads, no playtime limits. | **Blacknut**: **$15.99/month** (unlimited access) . | **30-day free trial** exclusive on VIZIO OS (US residents, select models) . | **Private (~$20M+ raised est.)** |
| **[Antstream Arcade](https://www.antstream.com/)** | Retro cloud gaming service with 1,300+ licensed classics. Playable on iPhone, iPad, Android, PC, and consoles. | **Monthly**: **R$24.90** (~$5/month) . **Yearly**: **R$99.90** (~$20/year) . | **7-day free trial** on annual subscription . | **Private (~$10M+ raised est.)** |
| **[AirGPU](https://airgpu.com/)** | GPU cloud platform for gaming and rendering. Managed, BYOC, and self-managed options. | **SHARED (Managed)**: **$0/month** (evaluation) . **STANDARD (Managed)**: **$0.99/hour** . **ENTERPRISE (Managed)**: **$1.49/hour** . | **SHARED free tier**: One workspace for **evaluation and non-production testing** . **$600 free credits** for STANDARD trial . | **Private (~$5M+ raised est.)** |

## 🔓 Open-Source GitHub Projects

Sorted by star count (descending). Star badge links to each repo's stargazers page.

| Repo | Description | Stars |
|---|---|---|
| **[Sunshine](https://github.com/LizardByte/Sunshine)** — **The de facto standard for self-hosted game streaming.** Low-latency cloud gaming server with **AMD, Intel, and NVIDIA hardware encoding** (plus software encoding). Web UI for configuration and client pairing. Pairs with **Moonlight** clients on any device. GPL-3.0 . | [![Stars](https://img.shields.io/github/stars/LizardByte/Sunshine?style=social&color=white)](https://github.com/LizardByte/Sunshine/stargazers) | ~22,000 |
| **[Moonlight](https://github.com/moonlight-stream/moonlight-qt)** — **Open-source game streaming client.** Works with Sunshine and NVIDIA GameStream. Available on PC, Mac, Linux, Android, iOS, Apple TV, and more. GPL-3.0. | [![Stars](https://img.shields.io/github/stars/moonlight-stream/moonlight-qt?style=social&color=white)](https://github.com/moonlight-stream/moonlight-qt/stargazers) | ~12,000 |
| **[CloudMorph](https://github.com/giongto35/cloud-morph)** — **Decentralized, self-hosted cloud gaming/application platform.** Streams any Windows game or app to the browser with **Docker-based one-line deployment**. Low-latency streaming, OS event simulation, P2P network support. Also ships an **OpenEnv-compatible Wine environment** for RL agents . | [![Stars](https://img.shields.io/github/stars/giongto35/cloud-morph?style=social&color=white)](https://github.com/giongto35/cloud-morph/stargazers) | ~1,800 |
| **[Wolf](https://github.com/games-on-whales/wolf)** — **Kubernetes-native game streaming platform.** Runs multiple game streaming sessions on a single host with container isolation. Designed for multi-user cloud gaming servers. MIT. | [![Stars](https://img.shields.io/github/stars/games-on-whales/wolf?style=social&color=white)](https://github.com/games-on-whales/wolf/stargazers) | ~1,200 |
| **[CloudRetro](https://github.com/giongto35/cloud-game)** — **Self-hosted cloud gaming service for retro games.** Sister project to CloudMorph. Runs classic consoles in the cloud, streamed to any browser with collaborative play support. MIT . | [![Stars](https://img.shields.io/github/stars/giongto35/cloud-game?style=social&color=white)](https://github.com/giongto35/cloud-game/stargazers) | ~1,000 |

**Additional open-source options worth exploring:**

| Repo | Description |
|---|---|
| **[Selkies-GStreamer](https://github.com/selkies-project/selkies-gstreamer)** — Open-source low-latency remote desktop and application streaming platform. WebRTC-based, used for cloud gaming and GPU-accelerated remote work. | [![Stars](https://img.shields.io/github/stars/selkies-project/selkies-gstreamer?style=social&color=white)](https://github.com/selkies-project/selkies-gstreamer/stargazers) |
| **[GameStream (Sunshine fork)](https://github.com/LizardByte/Sunshine)** — Community-maintained fork of NVIDIA GameStream for local streaming. | [![Stars](https://img.shields.io/github/stars/LizardByte/Sunshine?style=social&color=white)](https://github.com/LizardByte/Sunshine/stargazers) |

## 🤝 How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## ⚠️ Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud gaming platforms handle sensitive account credentials and streaming data; ensure proper security configuration and compliance with platform terms of service.
- **Open-source reality**: The open-source ecosystem for cloud gaming is **maturing but incomplete**. **Sunshine** is the de facto standard for self-hosted game streaming, pairing with **Moonlight** clients for low-latency remote play with hardware encoding on AMD, Intel, and NVIDIA GPUs . **CloudMorph** provides decentralized, self-hosted Windows application streaming in the browser with Docker-based deployment . **Wolf** offers a Kubernetes-native multi-user game streaming platform. However, **no open-source alternative matches the global server footprint, catalog breadth, or managed infrastructure of commercial platforms** (Xbox Cloud Gaming, GeForce NOW, PlayStation Plus). The open-source path is **genuinely viable** for **local/remote play from your own gaming PC**, **self-hosted retro gaming services**, or **organizations with strong infrastructure engineering capacity** seeking full control over their game streaming stack.
- **Pricing caveat**: All pricing figures above are **verified against cited search results** but may change without notice. Regional pricing, promotional rates, and subscription terms vary significantly. Always check the provider's official page for current pricing.

---

**Made for gamers, self-hosting enthusiasts, cloud infrastructure engineers, and game streaming developers.**
Let's make cloud gaming more open, self-hostable, and accessible.
