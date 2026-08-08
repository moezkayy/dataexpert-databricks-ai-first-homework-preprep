<div align="center">

# 🧠 DataExpert : Databricks AI Bootcamp

### Prereqs for the Lakebase Ticketing App

*Learn the concept first. Then prove it.*

[![Made with HTML](https://img.shields.io/badge/built%20with-HTML%2FCSS%2FJS-f0a94e?style=flat-square)](#)
[![SQL Engine](https://img.shields.io/badge/SQL%20engine-sql.js%20(SQLite%20WASM)-57d9c6?style=flat-square)](#)
[![Deploy](https://img.shields.io/badge/deploy-Vercel-black?style=flat-square&logo=vercel)](#)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](#-license)
[![Made by](https://img.shields.io/badge/made%20by-Moez%20Khan-e7ecf5?style=flat-square)](https://github.com/moezkayy)

**[🚀 Live Demo](#)** · **[📖 Modules](#-whats-inside)** · **[🛠 Run Locally](#-running-it-locally)**

</div>

---

## 📌 What this is

A self-contained, single-file learning platform built to close one specific gap: showing up to a Databricks + Lakebase assignment knowing Postgres/FastAPI/React exist, but not yet having the fundamentals to actually build with them from scratch.

Every module follows the same rule: **teach the concept from zero with a worked example, then test it.** Nothing is quizzed before it's explained.

The centerpiece is a real, working SQL console — not a simulation. It runs an actual SQL engine in your browser (via `sql.js`, SQLite compiled to WebAssembly), pre-loaded with the exact `tickets` / `ticket_messages` schema from the bootcamp assignment. You write real SQL, it runs for real, and you get checked against the real result.

---

## 🏗 Building the actual Databricks app

This platform gets you the prerequisites — it isn't the homework itself. Once you've worked through modules 01–09, here's the real build sequence in Databricks:

1. **Create your Lakebase database** — in the Databricks workspace, go to **Lakebase** → create a **Project**, then a **Branch** (this is your working copy of the database), then note its connection details.
2. **Connect once with `psql`** to sanity-check access, then run your `CREATE TABLE` statements for `tickets` and `ticket_messages` directly — the same schema taught in Module 01/02 of this platform.
3. **Seed it** with at least 3 tickets, 2+ messages per ticket, and 2+ distinct statuses.
4. **Scaffold a Databricks App**: `databricks apps init` (or via the UI) — pick a template (Streamlit is fastest for this scope).
5. **Attach your Lakebase database as a resource** to the app. This is the step that auto-provisions a service principal, a Postgres role, and injects `PGHOST`/`PGUSER`/etc. as environment variables — no manual credential wiring needed.
6. **Write the CRUD logic**: list tickets, view a ticket's messages, create a ticket, add a message, update a ticket's status — all reading/writing Lakebase, never hardcoded data.
7. **Test locally** with `databricks apps run-local` against the real Lakebase instance before deploying.
8. **Deploy** with `databricks apps deploy`, then verify in the live app: existing data loads, a new ticket persists, a message persists, a status update persists — all surviving a page refresh.


---

## 🗂 What's inside

| # | Module | Covers |
|---|--------|--------|
| 01 | **Relational DB & SQL** | What a table, row, column, primary key, and foreign key actually are — from a pile of unstructured notes to a real schema |
| 02 | **SQL Console** *(hands-on)* | A live SQLite-backed database in-browser — SELECT, WHERE, ORDER BY, GROUP BY, JOIN, INSERT, UPDATE |
| 03 | **Python Fundamentals** | Variables, dicts/lists, functions, control flow, `try/except`, venvs & `os.environ` |
| 04 | **HTTP & APIs** | Client-server model, HTTP methods, status codes, JSON |
| 05 | **FastAPI & Backends** | Routes, path params, Pydantic models, auto-generated docs |
| 06 | **DB Connections & Safety** | Parameterized queries, SQL injection, connection pooling, transactions |
| 07 | **Frontend Basics** | `fetch()`, React state model, Streamlit's rerun model, input validation |
| 08 | **Secrets, Git & Packaging** | Environment variables, `.gitignore`, `requirements.txt`, git basics |
| 09 | **Databricks & Lakebase** | OLTP vs OLAP, project/branch hierarchy, service principals, OAuth tokens |

Progress is tracked per-module in the sidebar (○ not started · ◐ in progress · ● done) with an overall completion bar — all in-memory for the session, nothing leaves your browser.

---

## ✨ Features

- 📚 **Lesson-first design** — every module opens with a real explanation (worked examples, comparison tables, diagrams) before any question is asked
- 🖥️ **A genuine SQL sandbox** — not multiple-choice SQL, actual query execution against a live database seeded with the assignment's exact schema
- ✅ **Instant, meaningful feedback** — answers are checked against real query results, not string matching
- 🎯 **Zero setup** — one HTML file, no build step, no dependencies to install
- 🌓 **Console-styled UI** — dark, monospace-forward design that matches the tooling (Postgres, terminals, query consoles) it's teaching

---

## 🛠 Running it locally

No build step, no `npm install` — it's a single static file.

```bash
git clone https://github.com/moezkayy/dataexpert-lakebase-prep.git
cd dataexpert-lakebase-prep
open index.html   # or just double-click it / drag into a browser
```

That's it. The SQL engine loads from a CDN on first run, so you'll need an internet connection for that one asset.

---

## ☁️ Deployment

Deployed as a static site on **Vercel** — no framework, no build command, just the raw file served as-is. Pushes to `main` auto-deploy.

---

## 🧱 Tech stack

- **Vanilla HTML / CSS / JS** — no framework, no bundler
- **[sql.js](https://sql.js.org/)** — SQLite compiled to WebAssembly, for the in-browser SQL console
- **IBM Plex Mono / IBM Plex Sans** — typography
- **Vercel** — hosting

---


## 👤 About

Built by **Moez Khan** — Data Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-moezkayy-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/moezkayy)
[![GitHub](https://img.shields.io/badge/GitHub-moezkayy-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/moezkayy)

---

## 📄 License

MIT — do whatever you want with it, including using it to actually study.

<div align="center">
<sub>Built as bootcamp prep, not a bootcamp submission.</sub>
</div>| 09 | **Databricks & Lakebase** | OLTP vs OLAP, project/branch hierarchy, service principals, OAuth tokens |

Progress is tracked per-module in the sidebar (○ not started · ◐ in progress · ● done) with an overall completion bar — all in-memory for the session, nothing leaves your browser.

---

## ✨ Features

- 📚 **Lesson-first design** — every module opens with a real explanation (worked examples, comparison tables, diagrams) before any question is asked
- 🖥️ **A genuine SQL sandbox** — not multiple-choice SQL, actual query execution against a live database seeded with the assignment's exact schema
- ✅ **Instant, meaningful feedback** — answers are checked against real query results, not string matching
- 🎯 **Zero setup** — one HTML file, no build step, no dependencies to install
- 🌓 **Console-styled UI** — dark, monospace-forward design that matches the tooling (Postgres, terminals, query consoles) it's teaching

---

## 🛠 Running it locally

No build step, no `npm install` — it's a single static file.

```bash
git clone https://github.com/moezkayy/dataexpert-lakebase-prep.git
cd dataexpert-lakebase-prep
open index.html   # or just double-click it / drag into a browser
```

That's it. The SQL engine loads from a CDN on first run, so you'll need an internet connection for that one asset.

---

## ☁️ Deployment

Deployed as a static site on **Vercel** — no framework, no build command, just the raw file served as-is. Pushes to `main` auto-deploy.

---

## 🧱 Tech stack

- **Vanilla HTML / CSS / JS** — no framework, no bundler
- **[sql.js](https://sql.js.org/)** — SQLite compiled to WebAssembly, for the in-browser SQL console
- **IBM Plex Mono / IBM Plex Sans** — typography
- **Vercel** — hosting


## 👤 About

Built by **Moez Khan** — Data Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-moezkayy-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/moezkayy)
[![GitHub](https://img.shields.io/badge/GitHub-moezkayy-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/moezkayy)

---

## 📄 License

MIT — do whatever you want with it, including using it to actually study.

<div align="center">
<sub>Built as bootcamp prep, not a bootcamp submission.</sub>
</div>
