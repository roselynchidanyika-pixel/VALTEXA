# CAPEXX AI AGENT 🏛️

**AI-powered capital-project decision intelligence.**

CAPEXX turns any capital-project proposal — infrastructure, hospitals,
universities, innovation hubs, energy, mining, technology, manufacturing,
agriculture, transport or real estate, in any country — into a complete,
explainable decision analysis: financial returns, risk, currency (FX),
scenarios, stress tests, and a transparent recommendation, all produced by
**one central cash-flow engine**.

---

## ✨ What it does

| Module | What you get |
|---|---|
| **Login** | Royal-blue & white gate · seeded admins (`FraiserXX` / `M251232@1`, `admin` / `admin123`) · guest self-registration. DEMO ONLY — not for production. |
| **Home** | Cinematic introduction, animated **market-simulation ticker** (clearly labelled DEMONSTRATION ONLY), and the CAPEXX robot. |
| **Project Analysis** | Manual input, CSV/Excel/PDF upload, or the **GZU Mashava Innovation Hub** demo (hypothetical — never presented as real GZU data). |
| **Engine results** | NPV, IRR, MIRR, payback (simple + discounted), ARR, PI, DCF, EAA, break-even — each with formula → result → interpretation. |
| **Risk Radar** | Weighted 0–100 sensitivity-based risk score (LOW / MODERATE / HIGH) across 10 categories. |
| **Currency / FX** | Multi-currency cash flows for any supplier country; mismatches, exposure amounts, hedging notes and a transaction-level currency strategy. |
| **Scenarios & Stress** | BASE / OPTIMISTIC / PESSIMISTIC / EXTREME STRESS plus a 15-shock stress battery and tornado sensitivity. |
| **Decision engine** | Transparent rule-based score (financial + risk + scenario pillars) → **🟢 ACCEPT / 🟠 REVIEW / 🔴 REJECT** with a 10-second status-light overlay. Every rule is shown. |
| **AI interpretation** | WHAT / WHY / SO WHAT / WHAT IF / MONITOR for every result; "Why did CAPEXX reach this result?" is fully traceable: Input → Calculation → Evidence → Interpretation. |
| **Robot voice panel** | Reads the analysis aloud (gTTS, graceful fallback to a script), downloadable MP3. |
| **Portfolio** | Side-by-side comparison and a capital-allocation illustration (never ranks or recommends between projects). |
| **Compare & Select** | Four decision-support tools — ⬅️➡️ **Side-by-side** (metrics, risk-radar overlay, FX, scenarios in parallel columns), 🎯 **Funding scorecard** (objective 0–100 priority *value+risk+resilience+Vision-2030 alignment* with auto-conditions), 💵 **Budget selection** (knapsack optimisation: best priority set that fits a capital ceiling, with a −10% budget sensitivity), 🅰️🅱️ **A/B what-if** (base vs variant: capex +30%, revenue −20%, delay, FX shock…). All clearly labelled decision-support, not a vote. |
| **Exchange Rate Board** | Owns the FX rates used by the engine; optional live fetch from a public keyless API at run time; never invents rates. |
| **ASK CAPEXX AI** | Global investment research: concept knowledge base, live exchange rates, World Bank country statistics, Google News RSS company/country research, and questions about your own project results. Every answer cites real sources. |
| **Reports & Delivery** | Full Markdown report, professional email (real SMTP delivery only when configured), narration audio. |

## 🚀 Run it

```bash
pip install -r requirements.txt
streamlit run app.py
```

Your browser opens `http://localhost:8501`.

> Use a Python 3.9+ interpreter. The project is validated on Python 3.14 with
> streamlit 1.62, pandas 3.0, numpy 2.5, numpy-financial 1.1, plotly 7, gTTS 2.5.

## 💻 Demo credentials (DEMO ONLY)

| Role | Username | Password |
|---|---|---|
| ADMIN | `FraiserXX` | `M251232@1` |
| ADMIN | `admin` | `admin123` |
| GUEST | any new username | your own (≥4 chars) |

Passwords are stored as salted SHA-256 hashes in `users.json` (gitignored).

## 🧪 Tests

```bash
python -m pytest tests/ -q
```

Coverage: financials, risk, currency/FX, scenarios/stress, decision rules,
email honesty (never claims a send without SMTP confirmation), upload
validation, and the compare/select features (funding priority, knapsack
budget selection including billion-scale budgets, sample portfolio, Vision
2030 pillar mapping).

## 📁 Layout

```
assets/          brand + real photographic assets (see docs/data_sources.md)
capexx_engine.py central financial/risk/FX/decision engine (single source of truth)
capexx_ask.py    ASK CAPEXX AI research module  (verifiable, dated sources)
capexx_ai.py     AI interpretation + narration + voice layer (graceful fallback)
capexx_auth.py   demo authentication (seeded admins + guest registration)
docs/            methodology & data-source documentation
sample_data/     demo project CSV/Excel, template, sample portfolio
outputs/         generated reports (md) and audio (mp3)
tests/           pytest suite
.streamlit/      theme + secrets (secrets.toml is gitignored)
app.py           Streamlit application
```

## 📚 Documentation

- [docs/methodology.md](docs/methodology.md) — how CAPEXX works end to end
- [docs/financial_model.md](docs/financial_model.md) — the central cash-flow engine
- [docs/risk_methodology.md](docs/risk_methodology.md) — risk scoring
- [docs/currency_methodology.md](docs/currency_methodology.md) — FX & landed cost
- [docs/ai_methodology.md](docs/ai_methodology.md) — AI interpretation & robot
- [docs/email_setup.md](docs/email_setup.md) — enabling real email delivery
- [docs/data_sources.md](docs/data_sources.md) — data-source policy & asset licences

## ⚠️ Important caveats

- **Decision-support only.** CAPEXX does not replace professional financial,
  engineering, legal, tax or investment advice.
- **Never fabricates data.** Every external figure shows Source | Date |
  Status; live data is fetched (or declined) at run time. Market-simulation
  prices are labelled DEMONSTRATION ONLY.
- **GZU demo is hypothetical.** The innovation-hub figures are invented to
  demonstrate the platform and are never presented as actual GZU data.
- **Demo login only.** Bearer of the admin credentials must be replaced with a
  real identity provider before production use.

## 📄 License

MIT — see [LICENSE](LICENSE). Third-party photographic assets remain under
their own licences (CC BY 2.0 / CC BY-SA 4.0 / CC BY-SA 3.0 / Unsplash).

---

*CAPEXX AI AGENT © 2026*