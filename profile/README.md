<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=9a160e&height=280&section=header&text=SHoNgxBoNg&fontSize=80&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Private%20Discord%20Bot%20Ecosystem&descAlignY=63&descAlign=50" />

<br/>

[![Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/sxb)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://choosealicense.com/licenses/mit)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node](https://img.shields.io/badge/Node-%3E%3D18.20.4-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Donate](https://img.shields.io/badge/Donate-PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/shkour)

<br/>

> Seven services that run one Discord community: a shared gateway relay, three bots, a rendering API,
> a shared data layer, and a web platform — built for performance, scalability, and full control.

</div>

---

## 📑 Table of Contents

- [✨ What the Ecosystem Does](#-what-the-ecosystem-does)
- [🏗️ Projects](#️-projects)
- [⚡ Architecture](#-architecture)
- [🔑 How the Pieces Connect](#-how-the-pieces-connect)
- [⚙️ Tech & Acknowledgments](#️-tech--acknowledgments)
- [👥 Developers](#-developers)
- [🤝 Support](#-support)
- [💛 Donate](#-donate)
- [🔒 Privacy Policy](#-privacy-policy)
- [📄 License](#-license)

---

## ✨ What the Ecosystem Does

| Area | Description |
|---|---|
| 🛡️ **Moderation & Auditing** | Warnings, timeouts, bans, bulk cleanup, and a full audit trail of every gateway event |
| 🎮 **Games & Events** | 27 single-player games, 2 duo games, and 9 multiplayer systems (Bank, Mafia, Codenames, Roulette, Hide & Seek, Chairs, Geo, Party, Stop) |
| 💰 **Economy & Leveling** | Dual-currency wallets, XP from text and voice, daily streaks, transfers with a risk engine, and clan credit |
| 🎙️ **Dynamic Voice Rooms** | Join-to-create channels with privacy controls, trust/block lists, room codes, and protection perks |
| 🎫 **Tickets & Staff Ops** | Auto-routed support tickets with hosted HTML transcripts, staff activity scoring, and vacation management |
| 💳 **Subscriptions & Gifts** | Four tiers (Starter, Pro, Elite, Ultimate) driven by Dodo Payments, Ko-fi and Patreon webhooks, with role sync, grace periods, gift codes, and status cards |
| 🖼️ **Server-Side Rendering** | Every card, chart, and game board is drawn server-side by the API and delivered to Discord as an image |
| 🛂 **Command Permissions** | One authority for who may run which command, published by the API and edited from the dashboard — the bots ask, they do not decide |
| 🎨 **Profiles & Cosmetics** | Badges, frames, backgrounds, effects and colorways over a member-designed profile card layout |
| 🌍 **Public Site & Member Area** | A bilingual English/Arabic website with leaderboards, pricing and checkout, plus a member area for billing, cosmetics and personal stats |
| 📊 **Web Administration** | A Next.js admin portal over the whole data layer, with JWT + OTP auth and role-based access control |

---

## 🏗️ Projects

<table>
  <thead>
    <tr>
      <th>Project</th>
      <th>Role</th>
      <th>Stack</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://github.com/1SHoNgxBoNg/SHoNgHub"><b>📡 SHoNgHub</b></a></td>
      <td>Gateway event relay. Holds the single privileged-intent Discord connection and fans events out to every bot over Redis Streams</td>
      <td>@discordjs/ws · Fastify · Redis Streams</td>
    </tr>
    <tr>
      <td><a href="https://github.com/1SHoNgxBoNg/SHoNgBot"><b>🤖 SHoNgBot</b></a></td>
      <td>Main systems bot — temp voice, tickets, clans, staff, economy, subscriptions, and scheduled jobs</td>
      <td>discord.js · Fastify · Postgres · Redis</td>
    </tr>
    <tr>
      <td><a href="https://github.com/1SHoNgxBoNg/SHoNgArena"><b>🎮 SHoNgArena</b></a></td>
      <td>Games and events client — 38 games, profiles, leaderboards, whispers, and the transfer/wallet risk engine</td>
      <td>discord.js · Redis · Supabase</td>
    </tr>
    <tr>
      <td><a href="https://github.com/1SHoNgxBoNg/SHoNgLogix"><b>📝 SHoNgLogix</b></a></td>
      <td>Event auditor — captures 32 gateway events into log channels and warehouses them in Postgres, with an Oracle mirror. Also runs OCR scam detection on images</td>
      <td>discord.js · Postgres · Oracle · Tesseract.js</td>
    </tr>
    <tr>
      <td><a href="https://github.com/1SHoNgxBoNg/SHoNgAPI"><b>🔌 SHoNgAPI</b></a></td>
      <td>Backend microservice — renders every card and game board, receives the payment webhooks, and serves the command-permission and support control planes</td>
      <td>NestJS · Fastify · Rust canvas · sharp</td>
    </tr>
    <tr>
      <td><a href="https://github.com/1SHoNgxBoNg/SHoNgDashboard"><b>🖥️ SHoNgDashboard</b></a></td>
      <td>The web platform — a bilingual public site, a member account area with checkout and cosmetics, and a 34-page admin portal, all behind one edge with three session kinds</td>
      <td>Next.js 16 · React 19 · Tailwind v4</td>
    </tr>
    <tr>
      <td><a href="https://github.com/1SHoNgxBoNg/SHoNgDatabase"><b>🗄️ SHoNgDatabase</b></a></td>
      <td>Shared data layer — Mongoose schemas, economy config, subscription tiers and provider catalogs, command-permission keys, cosmetics, and the game-stats engine, plus a Prisma layer over the Arena SQL warehouse. Imported by all five services above</td>
      <td>TypeScript · Mongoose · Prisma</td>
    </tr>
  </tbody>
</table>

---

## ⚡ Architecture

One Discord application holds the privileged intents. Everything else consumes relayed events.
The system reads top to bottom in four layers: the relay, the bot clients, the services, and the
shared data layer underneath all of them.

```mermaid
flowchart TD
    %% ─── Ingress ───────────────────────────────────────────────
    Members["👥 Discord Members"]
    Web["🌐 Visitors · Members · Operators"]
    Pay["💳 Dodo Payments · Ko-fi · Patreon"]

    %% ─── 1. Relay ──────────────────────────────────────────────
    subgraph Relay ["① Gateway Relay — the one privileged connection"]
        Hub["📡 SHoNgHub<br/>@discordjs/ws · Fastify :3200"]
        Streams[("Redis Streams<br/>hub:events:*")]
        Hub -->|XADD| Streams
    end

    %% ─── 2. Bots ───────────────────────────────────────────────
    subgraph Clients ["② Bot Clients — own tokens · non-privileged intents"]
        direction LR
        Bot["🤖 SHoNgBot<br/>Fastify :3002"]
        Arena["🎮 SHoNgArena"]
        Logix["📝 SHoNgLogix"]
    end

    %% ─── 3. Services ───────────────────────────────────────────
    subgraph Services ["③ Services"]
        direction LR
        API["🔌 SHoNgAPI — NestJS :5002<br/>rendering · payments<br/>command permissions · support"]
        Dash["🖥️ SHoNgDashboard — Next.js 16<br/>public site · member area · admin portal"]
    end

    %% ─── 4. Data ───────────────────────────────────────────────
    subgraph Foundation ["④ Shared Data Layer"]
        Shared["🗄️ @shong/database<br/>schemas · cosmetics · permissions<br/>GameStats · Arena SQL"]
        Stores[("MongoDB Atlas · PostgreSQL · Redis")]
        Shared --> Stores
    end

    %% ─── Ingress ───
    Members -->|gateway events| Hub
    Web -->|HTTPS| Dash
    Pay -->|webhooks| API

    %% ─── Fan-out ───
    Streams -->|XREADGROUP| Bot
    Streams -->|XREADGROUP| Arena
    Streams -->|XREADGROUP| Logix
    Hub -.->|message history| Bot

    %% ─── Bots act directly on Discord ───
    Clients ==>|REST · own token| Members

    %% ─── Service traffic ───
    Bot <-->|renders · permission checks| API
    Arena <-->|renders · permission checks| API
    Dash <-->|transcripts · subscription sync| Bot
    Dash <-->|support · permissions · renders| API

    %% ─── Everything sits on the shared layer ───
    Clients --> Shared
    Services --> Shared
```

### Who touches which store

Every service shares one Redis instance and one MongoDB cluster; PostgreSQL is split between the
`public` warehouse and the Prisma-managed `arena` schema.

| Service | MongoDB | PostgreSQL | Redis |
|---|---|---|---|
| 📡 **SHoNgHub** | — | — | Streams, member directory, leader lock |
| 🤖 **SHoNgBot** | Domain model | Warehouse writes, batched | Relay, caches, staff activity |
| 🎮 **SHoNgArena** | Domain model | Supabase reads | Relay, GameStats queue — owns the flusher |
| 📝 **SHoNgLogix** | Three models only | Primary store, mirrored to Oracle | Relay, mirror queue, flags |
| 🔌 **SHoNgAPI** | Domain model | Arena schema via `@shong/database/sql` | Idempotency, metrics, permission cache |
| 🖥️ **SHoNgDashboard** | Domain model | `stats_*` RPCs | Rate limits, caches, key browser |

---

## 🔑 How the Pieces Connect

**SHoNgHub owns the gateway.** Discord intents govern only what the Gateway pushes to a connection —
they have no bearing on the REST API. So one application holds `MessageContent` and `GuildMembers`,
normalises each event, and `XADD`s it to a Redis Stream. Each bot reads its own consumer group and
replays the untouched payload through discord.js's internal actions, so handlers see exactly the
objects a live gateway would have produced. Interactions never pass through the Hub — they stay
direct, because they must be acknowledged within three seconds.

All three bots consume the relay. SHoNgLogix subscribes to the widest set — all four message events
and all three member events — because an auditor that misses an event has failed at its one job.

**SHoNgAPI owns rendering.** No bot draws images in-process. Profile cards, leaderboards, game
boards, wheel GIFs, and tier cards are all HTTP calls to the API, which renders them with a
Rust-backed canvas and returns base64 PNGs.

**SHoNgAPI also owns the control planes.** Command permissions and the external support desk are
served from one place, so the bots, the Arena and the dashboard read one authority instead of three.
A bot publishes its command registry and asks whether a caller may run a command; it never decides
for itself. The rollout is staged through a shared namespace and per-guild enforcement flags, so
enforcement can be switched on one guild at a time and rolled back by changing a value.

**One payment provider at a time.** `PAYMENTS_PROVIDER` decides which processor module the API even
constructs — no route, no client, no boot check for the other. Paddle is archived rather than
deleted, so flipping back is one value and a redeploy. Two things are never gated: gift-code
redemption, because a gift code outlives the provider that sold it, and the Paddle *read* paths in
the dashboard, because archiving a provider must not strip a paying subscriber of the ability to see
their invoices or manage their plan.

**@shong/database owns the schema.** It is a `file:` dependency, not a published package, so it must
be built before any consumer. Every service's local `schema/` or `models/` folder is a thin re-export
shim over it. It publishes subpaths — `/command-permissions`, `/cosmetics` and `/sql` — that stay
importable without a Mongoose connection, which is what lets a command registry load one during
module evaluation.

**One Redis, one Mongo cluster.** All services share both. Redis carries the Hub streams, the member
directory, caches, rate limits, permission caches, and webhook idempotency keys — each namespaced to
avoid collisions. PostgreSQL carries two separate things: the `public` warehouse SHoNgLogix fills and
the dashboard reads, and the `arena` schema that `@shong/database` manages with Prisma.

```text
/home/ubuntu/shong/
├── SHoNgDatabase/     # build first — every other project depends on it
├── SHoNgHub/          # build second — the three bots depend on its packages/
├── SHoNgAPI/
├── SHoNgBot/
├── SHoNgArena/
├── SHoNgLogix/
└── SHoNgDashboard/
```

---

## ⚙️ Tech & Acknowledgments

<div align="center">

[![Discord.js](https://img.shields.io/badge/Discord.js-Library-5865F2?style=flat-square&logo=discord&logoColor=white)](https://github.com/discordjs/discord.js)
[![MongoDB](https://img.shields.io/badge/MongoDB-Database-47A248?style=flat-square&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-336791?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Supabase](https://img.shields.io/badge/Supabase-BaaS-3ECF8E?style=flat-square&logo=supabase&logoColor=white)](https://supabase.com/)
[![Redis](https://img.shields.io/badge/Redis-Streams%20%26%20Cache-DC382D?style=flat-square&logo=redis&logoColor=white)](https://redis.io)
[![Sentry](https://img.shields.io/badge/Sentry-Monitoring-362D59?style=flat-square&logo=sentry&logoColor=white)](https://sentry.io/)
[![TypeScript](https://img.shields.io/badge/TypeScript-Language-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![NestJS](https://img.shields.io/badge/NestJS-Framework-E0234E?style=flat-square&logo=nestjs&logoColor=white)](https://nestjs.com/)
[![Fastify](https://img.shields.io/badge/Fastify-Server-000000?style=flat-square&logo=fastify&logoColor=white)](https://fastify.dev/)
[![Next.js](https://img.shields.io/badge/Next.js-Frontend-000000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Prisma](https://img.shields.io/badge/Prisma-ORM-2D3748?style=flat-square&logo=prisma&logoColor=white)](https://www.prisma.io/)

</div>

---

## 👥 Developers

<div align="center">

| Developer | GitHub |
|---|---|
| **ShkourBashtawi** | [![GitHub](https://img.shields.io/badge/GitHub-ShkourBashtawi-181717?style=flat-square&logo=github)](https://github.com/ShkourBashtawi) |
| **ArrioProgrammer** | [![GitHub](https://img.shields.io/badge/GitHub-ArrioProgrammer-181717?style=flat-square&logo=github)](https://github.com/ArrioProgrammer) |
| **PHANTOM** | [![GitHub](https://img.shields.io/badge/GitHub-PHANTOM-181717?style=flat-square&logo=github)](https://github.com/yosefyakop) |

</div>

---

## 🤝 Support

- 🐛 **Open an Issue** — [Report a bug or request a feature](https://github.com/1SHoNgxBoNg/SHoNgBot/issues)
- 💬 **Join our Discord** — [discord.gg/sxb](https://discord.gg/sxb) for real-time support

---

## 💛 Donate

If you find this project useful and would like to support its continued development, a donation means a lot to us!

<div align="center">

[![Donate via PayPal](https://img.shields.io/badge/Donate-PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/shkour)

</div>

---

## 🔒 Privacy Policy

- [SHoNgxBoNg Bot Privacy Policy](https://github.com/1SHoNgxBoNg/.github/blob/main/profile/SHoNgxBoNg_bot.md)
- [SHoNgArena Privacy Policy](https://github.com/1SHoNgxBoNg/.github/blob/main/profile/arena_privacy.md)

---

## 📄 License

All projects in this ecosystem are licensed under the **MIT License**.

---

<div align="center">

[![GitHub Followers](https://img.shields.io/github/followers/1SHoNgxBoNg?style=social)](https://github.com/1SHoNgxBoNg)

<sub>Made with ❤️ by the SHoNgxBoNg team</sub>

</div>
