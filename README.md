<div align="center">

# Bishwa Bandhu Parmar
### Freelance Full-Stack Developer — MERN / Next.js — moving deeper into backend engineering

[![Email](https://img.shields.io/badge/Email-bishwabandhuparmar06%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:bishwabandhuparmar06@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-bishwabandhu06-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bishwabandhu06/)
[![Portfolio](https://img.shields.io/badge/Portfolio-bishwabandhu.me-000000?style=flat-square&logo=vercel&logoColor=white)](https://bishwabandhu.me/)
[![Fiverr](https://img.shields.io/badge/Hire%20me-Fiverr-1DBF73?style=flat-square&logo=fiverr&logoColor=white)](https://www.fiverr.com/s/yvzo745)

</div>

---

## About

I build and ship full-stack web products end to end — frontend, backend, database schema, and deployment — for freelance clients. Three of those products are in production today: a restaurant QR-ordering SaaS, an e-commerce storefront, and a real-estate rental marketplace.

My default stack is React/Next.js on the frontend and Node.js/Express on the backend. I've shipped with both MongoDB and PostgreSQL, and I'm deliberately pushing further into backend engineering — relational schema design, caching, containerization, and system design — rather than staying frontend-comfortable.

## Currently Focused On

- **SQL depth** — writing raw SQL against Postgres (via the `pg` driver, no ORM) instead of defaulting to Mongoose, to build real relational-schema instincts
- **System design fundamentals** — caching, load balancing, rate limiting, message queues (see roadmap below)
- **Docker & containerized deployments** — moving off free-tier PaaS cold-starts toward reproducible container-based deploys
- **DSA** — active on LeetCode, GeeksforGeeks, Codeforces, and HackerRank

---

## Featured Projects

### 🍽️ BhojanQR — QR-Based Restaurant Ordering SaaS
**Live:** [bhojanqr.com](http://bhojanqr.com) &nbsp;|&nbsp; **Repo:** private (client-owned) — public companion: [BhojanQRMobile](https://github.com/bishwa-bandhu-parmar-06/BhojanQRMobile)

A multi-tenant SaaS product for restaurants: diners scan a table QR code, browse a live digital menu, and place orders that land directly on the restaurant's dashboard — no app install, no waiter round-trips.

- **Problem solved:** replaces paper menus and manual order-taking with a real-time, self-serve ordering flow restaurants can run per-table
- **Core capabilities:** QR-triggered ordering flow, real-time order updates to a restaurant dashboard, payment integration, order/menu analytics for owners, mobile-first PWA so no app store install is required
- **Architecture:** multi-tenant SaaS — each restaurant operates its own menu, orders, and dashboard behind one shared platform
- **Mobile:** a React Native companion app ([BhojanQRMobile](https://github.com/bishwa-bandhu-parmar-06/BhojanQRMobile)) is in early development alongside the PWA
- **Future improvements:** public API for POS integrations, offline-first order queuing for spotty restaurant Wi-Fi

---

### 🛒 MartXpress — Full-Stack E-Commerce Platform
**Live:** [martxpress.onrender.com](https://martxpress.onrender.com/) &nbsp;|&nbsp; **Repo:** [github.com/.../martXpress](https://github.com/bishwa-bandhu-parmar-06/martXpress)

A client-server e-commerce storefront built to practice a clean separation between a React frontend and a REST API backend.

- **Architecture:** React client → REST API (Node.js/Express) → MongoDB, deployed as a single service on Render
- **Implemented:** product browsing & search, product detail pages, cart management, JWT-based user authentication, fully responsive UI
- **Security:** JWT auth with a secrets-based `.env` configuration, server-side request validation on the Express layer
- **Deployment:** hosted on Render (free tier — first load after idle can take ~30s to spin up, a known trade-off of the hosting tier rather than the app)
- **Future improvements:** payment gateway (Stripe/Razorpay), wishlist, order tracking, admin product dashboard — intentionally scoped out of v1 to ship the core shopping flow first

---

### 🏡 GayaRent — Direct-to-Tenant Property Rental Marketplace
**Live:** [gaya-rent.onrender.com](https://gaya-rent.onrender.com/) &nbsp;|&nbsp; **Repo:** [github.com/.../Gaya_Rent](https://github.com/bishwa-bandhu-parmar-06/Gaya_Rent)

A rental marketplace connecting property owners directly with tenants, cutting out brokerage fees.

- **Why PostgreSQL:** chosen over MongoDB deliberately — the domain (owners, tenants, properties, admin approvals) is inherently relational, and I wanted to build real SQL fluency instead of leaning on an ORM. The backend talks to Postgres (hosted on Supabase) through a thin custom wrapper over the raw `pg` module — no Prisma/Sequelize — so every query is hand-written SQL
- **Architecture:** monorepo with a Next.js 14 (App Router) client and an Express server, communicating over a REST API
- **Core capabilities:** multi-role auth (Tenant / Owner / Admin dashboards), CSV bulk-upload for property listings, geolocation-based "near me" search, direct WhatsApp contact between tenant and owner (no in-app messaging layer to maintain), admin approval workflow for new owner partners
- **Frontend:** Tailwind CSS + shadcn/ui, Redux Toolkit with Redux Persist for client state, NextAuth/Google OAuth
- **Security:** JWT auth, `bcrypt` password hashing, `Helmet` + `CORS` on the Express layer
- **Future improvements:** migrate the raw SQL layer to a lightweight query builder (Kysely) as the schema grows, add Redis caching for property search results

---

## Engineering Skills

| Category | Technologies |
|---|---|
| **Languages** | JavaScript, TypeScript, SQL, Java, C++, C, Python |
| **Frontend** | React, Next.js (App Router), Redux Toolkit, Tailwind CSS, shadcn/ui, HTML5/CSS3 |
| **Backend** | Node.js, Express.js, REST API design, JWT Auth, Google OAuth / NextAuth |
| **Databases** | PostgreSQL (raw SQL via `pg`, Supabase-hosted), MongoDB, MySQL |
| **Cloud** | AWS S3 (file uploads), Render, Supabase |
| **Security** | JWT, bcrypt, Helmet, CORS, Role-Based Access Control |
| **Tools** | Git/GitHub, Postman, Figma |
| **Currently learning** | Docker, Redis, System Design fundamentals |

---

## System Design — Learning Roadmap

What I'm deliberately building toward, beyond CRUD apps:

- [x] REST API design & client-server separation
- [x] Relational schema design (PostgreSQL, no ORM)
- [x] Multi-role auth & access control
- [ ] Redis caching
- [ ] Rate limiting
- [ ] Message queues (BullMQ / RabbitMQ)
- [ ] Load balancing & horizontal scaling
- [ ] Docker & containerized deployments
- [ ] API Gateway patterns
- [ ] Microservices decomposition
- [ ] Observability (logging, metrics, tracing)

---

## Certifications & Achievements

- **GirlScript Summer of Code 2024 (Extended Edition)** — Contributor
- **Google Cybersecurity** — Google, via Coursera *([view](https://www.coursera.org/account/accomplishments/specialization/certificate/ELVAELDJ76GE))*
- **Full Stack Web Development – MERN** — Apna College *([view](https://mycourse.app/FDyhcMkkPonCg3n89))*
- **Flipkart Grid 6.0** — Certificate of Participation *([view](https://unstop.com/certificate-preview/cf7d8644-cfc5-45ff-950e-e6f091ca084c))*

---

## Open Source

No merged external contributions yet — actively looking to change that. Repos on my shortlist, picked to match my stack:

| Repo | Why it's relevant |
|---|---|
| [supabase/supabase](https://github.com/supabase/supabase) | I already run GayaRent's Postgres on Supabase — natural next step to contribute upstream |
| [tiangolo/fastapi](https://github.com/tiangolo/fastapi) | Learning FastAPI as a second backend framework alongside Express |
| [encode/django-rest-framework](https://github.com/encode/django-rest-framework) | Deepening Django REST as I broaden past Node |
| [appwrite/appwrite](https://github.com/appwrite/appwrite) | Backend-as-a-service, heavy Docker usage — good testbed for containerization learning |
| [docker/awesome-compose](https://github.com/docker/awesome-compose) | Approachable, example-driven — matches where I am with Docker right now |

---

## Technical Writing (upcoming)

Planning to write from what I've actually hit building the projects above, not generic tutorials:

- Why I dropped an ORM for raw SQL on GayaRent — and when I'd add one back
- JWT auth across a multi-role system (Tenant/Owner/Admin) — lessons from GayaRent
- REST API design for a multi-tenant SaaS — BhojanQR's data model
- Redis caching for a property-search endpoint (planned, once implemented)
- Deploying Node/Next monorepos on Render vs. a Docker-based setup

---

## Coding Profiles

<div align="center">

[![LeetCode](https://img.shields.io/badge/LeetCode-bishwabandhu06-FFA116?style=flat-square&logo=leetcode&logoColor=white)](https://leetcode.com/u/bishwabandhu06/)
[![GeeksforGeeks](https://img.shields.io/badge/GfG-bishwabandhu06-2F8D46?style=flat-square&logo=geeksforgeeks&logoColor=white)](https://www.geeksforgeeks.org/profile/bishwabandhu06)
[![Codeforces](https://img.shields.io/badge/Codeforces-bishwabandhu06-1F8ACB?style=flat-square&logo=codeforces&logoColor=white)](https://codeforces.com/profile/bishwabandhu06)
[![HackerRank](https://img.shields.io/badge/HackerRank-bishwabandhu06-2EC866?style=flat-square&logo=hackerrank&logoColor=white)](https://www.hackerrank.com/profile/bishwabandhu06)

<img src="https://leetcard.jacoblin.cool/bishwabandhu06?ext=contest" alt="LeetCode Stats" />

</div>

## GitHub Activity

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=bishwa-bandhu-parmar-06&show_icons=true&theme=default&hide_border=true&count_private=true" alt="GitHub Stats" height="165" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=bishwa-bandhu-parmar-06&layout=compact&hide_border=true&theme=default" alt="Top Languages" height="165" />
</div>

---

## Contact

📧 [bishwabandhuparmar06@gmail.com](mailto:bishwabandhuparmar06@gmail.com) &nbsp;·&nbsp;
💼 [LinkedIn](https://www.linkedin.com/in/bishwabandhu06/) &nbsp;·&nbsp;
🌐 [bishwabandhu.me](https://bishwabandhu.me/) &nbsp;·&nbsp;
🧑‍💻 [Fiverr](https://www.fiverr.com/s/yvzo745)
