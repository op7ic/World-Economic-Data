# World Economic Data

Historical macroeconomic and microeconomic reference reports for the global economy, organized as one Markdown file per year.

Each yearly file is a research-style snapshot of the world economy for that specific year, covering global themes, the top economies, sector performance, financial markets, risks, and references.

## Coverage

| Item | Value |
|------|-------|
| Annual reports | 114 |
| First year | 1911 |
| Last year | 2025 |
| Missing years inside the covered range | 1918 |
| File naming pattern | `YYYY.md` |

The current repository contains reports from `1911.md` through `2025.md`, with `1918.md` currently missing.

## Repository Layout

- `1911.md` ... `2025.md`: one report per year
- `README.md`: project overview and example generation prompt
- `LICENSE`: repository license

## What Each Year File Contains

The reports follow a consistent structure:

1. Executive summary
2. Key themes of the year
3. Macroeconomic overview
4. Country-by-country review of the top 20 economies by GDP
5. Global microeconomic and sector deep dive
6. Financial markets
7. Risks, crises, and black swans
8. Year-over-year delta versus the prior year
9. Data confidence and gaps
10. References

Representative files such as `1911.md`, `1980.md`, and `2025.md` follow this same high-level layout.

## Notes on Historical Data

- Older years rely more heavily on reconstructed historical datasets and archival statistics.
- Coverage quality varies by country and period, especially for prewar economies, colonial territories, Soviet-bloc economies, and early developing-country series.
- When a metric cannot be verified, the report should say `Data not available` rather than estimate silently.
- Rankings should be historical for that year, not modern rankings projected backward.

## Adding a New Year

1. Copy the prompt template below.
2. Replace `{{YEAR}}` and `{{YEAR-1}}`.
3. Generate the report with source-backed historical research.
4. Save the result as `{{YEAR}}.md` in the repository root.
5. Verify citations, year-over-year comparisons, and any declared data gaps.

## Contributing

Contributions are welcome via pull request.

- Open a pull request for new year files, corrections, source improvements, formatting fixes, or documentation updates.
- Keep each yearly report self-contained and consistent with the structure documented in this README.
- Include source-backed changes only, and prefer explicit `Data not available` notes over unverified estimates.
- We review contributed data and documentation changes before merging.

## Example Prompt

The block below is the example prompt used to generate a yearly report. It is intentionally detailed so future additions stay consistent with the existing files.

```text
# MACRO/MICRO GLOBAL ECONOMIC ASSESSMENT - YEAR: {{YEAR}}

You are an economic historian and research analyst. Produce a comprehensive, research-grade macro and microeconomic assessment for {{YEAR}}, covering the top 20 economies by GDP for that specific year.

This is a durable reference document for a GitHub repository named World-Economic-Data. Every claim must be grounded in verifiable data. Do NOT fabricate statistics. If data is unavailable, state "Data not available" rather than guessing. Cross-reference at least 2 sources for GDP rankings and major claims. Prioritize primary sources: World Bank, IMF, OECD, BIS, Maddison Project Database, Penn World Table, central bank publications, UN Statistical Yearbook, and national statistics offices.

Search extensively (10-20+ queries). Start broad ("world economy {{YEAR}}", "GDP ranking {{YEAR}}"), then drill into countries, sectors, crises, and events. For pre-1990 Soviet bloc and developing nation GDP, use Maddison Project Database estimates and flag the uncertainty explicitly.

---

## OUTPUT STRUCTURE (follow exactly)

### 1. EXECUTIVE SUMMARY
3-5 paragraphs. What defined {{YEAR}} economically? Dominant forces, structural changes vs. prior year, surprises. Write as if briefing a senior economist who needs the big picture in 2 minutes.

### 2. KEY THEMES OF {{YEAR}}
Identify 4-8 defining economic themes (not just events, but analytical threads: policy regime shifts, structural transitions, crises, secular trend inflections). For each theme provide: significance in economic history, specific data/events in {{YEAR}}, countries most affected, and forward linkage to subsequent years.

### 3. MACROECONOMIC OVERVIEW

**3A. Global Aggregates:** World GDP and growth rate, global trade volume, reserve currency dynamics, global inflation trends, key commodity prices (oil, gold, copper, agricultural staples), international capital flow direction.

**3B. Monetary & Financial Conditions:** Interest rate environment in major economies (US, UK, Germany/Eurozone, Japan), central bank policy stance and key decisions, exchange rate regime context (Bretton Woods status / managed floats / pegs), key FX movements, credit conditions, stock market performance (major indices), bond market and yield curves.

**3C. Trade & Geopolitics:** Major trade agreements/disputes/tariffs, sanctions/embargoes, Cold War or geopolitical context affecting economic flows, regional integration developments (EEC, ASEAN, etc.), key bilateral economic tensions.

**3D. Commodities & Energy:** Oil price and production dynamics (OPEC context), key metals and minerals, agricultural commodity conditions, energy supply disruptions or discoveries.

**3E. Labor & Demographics:** Global employment trends, migration with economic significance, demographic shifts (baby boom/bust, urbanization), wage growth vs. productivity, labor market structural changes.

### 4. COUNTRY-BY-COUNTRY: TOP 20 ECONOMIES OF {{YEAR}}

First, list the top 20 countries by GDP for {{YEAR}} with estimated GDP figures and ranking. Note entries/exits vs. prior year. Use Maddison Project or World Bank historical data, not modern rankings applied retroactively.

For each of the 20 countries provide:

**Header:** Rank, country name, GDP (USD or local + USD equivalent), GDP growth (YoY %), population, GDP per capita.

**Macro indicators table:**

| Indicator | Value | YoY Change | Notes |
|-----------|-------|------------|-------|
| Real GDP Growth | | | |
| Inflation (CPI) | | | |
| Unemployment Rate | | | |
| Policy/Key Interest Rate | | | |
| Government Debt/GDP | | | |
| Current Account Balance (% GDP) | | | |
| Exchange Rate vs USD | | | |
| Budget Deficit/Surplus (% GDP) | | | |

**Economic narrative (2-4 paragraphs):** Dominant economic story, key policy decisions (fiscal, monetary, trade, industrial), structural changes or reforms, sector composition shifts, major corporate/industrial developments, social/political context, relationship to global themes from Section 2.

**Micro/sectoral highlights:** Leading sectors (growth drivers and contracting industries), notable corporate events (M&A, IPOs, bankruptcies, nationalizations, privatizations), innovation/technology with economic impact, consumer/household dynamics (confidence, debt, savings, consumption), banking and finance sector health, real estate/property conditions, major regulatory changes.

### 5. MICROECONOMIC & SECTORAL DEEP DIVE (GLOBAL)

**5A. Sector performance matrix:**

| Sector | Global Trend | Top Performing Countries | Key Drivers |
|--------|--------------|--------------------------|-------------|
| Manufacturing | | | |
| Agriculture | | | |
| Mining & Extraction | | | |
| Financial Services | | | |
| Construction | | | |
| Transport & Logistics | | | |
| Telecommunications | | | |
| Technology | | | |
| Energy | | | |
| Healthcare | | | |
| Consumer Goods | | | |
| Defense/Military-Industrial | | | |

**5B. Corporate landscape:** Largest companies globally (top 10-20 by revenue/market cap if data exists), major M&A, significant IPOs, notable bankruptcies/failures/nationalizations, emerging corporate giants or business model innovations.

**5C. Innovation & technology:** Key breakthroughs with economic implications, R&D spending trends, patent activity, infrastructure megaprojects.

**5D. Labor markets & human capital:** Sectoral employment shifts, wage dynamics across skill levels, education/workforce trends, union/labor movement developments, immigration/emigration affecting labor supply.

### 6. FINANCIAL MARKETS

**6A. Equity markets:** For each major stock exchange existing in {{YEAR}}: index level, annual return, bull/bear dynamics, sector rotation, market-moving events.

**6B. Fixed income:** Government bond yields (10Y for major economies), credit spreads if available, sovereign debt events.

**6C. Currencies:** Major pair movements, devaluations/revaluations, capital controls imposed or removed, reserve currency composition shifts.

**6D. Alternative assets:** Gold price and dynamics, real estate in major cities, other relevant asset classes.

### 7. RISKS, CRISES & BLACK SWANS
Active crises during {{YEAR}}, near-misses, systemic vulnerabilities building (with hindsight clearly labeled as hindsight), policy mistakes visible in retrospect, tail risks that materialized vs. those that did not.

### 8. YEAR-OVER-YEAR DELTA ({{YEAR}} vs. {{YEAR-1}})
Structural breaks or regime changes, trend accelerations or reversals, new risks that emerged, risks that resolved, shifts in economic power or influence, policy pivots. Be specific and concrete.

### 9. DATA CONFIDENCE & GAPS
Which countries had reliable statistics? Which metrics are estimates vs. official? Where does historical data conflict across sources? Which claims in this document have the weakest evidence? What important data simply does not exist for {{YEAR}}?

### 10. REFERENCES
All sources cited using IEEE/Vancouver style. Numbered sequentially. Include URLs where available.

---

## RESEARCH RULES (non-negotiable)

1. **No fabrication.** If you cannot find a figure, write "Data not available." Estimates must be labeled with method noted.
2. **Historical rankings only.** The top 20 in 1965 are not the same as 2024. Use Maddison Project or World Bank historical data.
3. **Currency context.** Note nominal vs. real terms, which year's dollars if adjusted. For pre-1971: note Bretton Woods fixed rate context.
4. **Hindsight discipline.** Clearly separate what was knowable at the time from what is only visible retrospectively.
5. **Micro depth.** Corporate events, sector dynamics, consumer behavior, and innovation are mechanisms through which macro trends manifest. They are not an afterthought.
6. **Geographic balance.** Do not default to US/UK/Western Europe bias. Japan, USSR, China, India, Brazil, and others deserve proportionate coverage.
7. **Intellectual honesty.** Where economists disagree about causes, note the disagreement. Where consensus exists, state it. Where confidence is low, say so.
8. **Soviet bloc / non-market economies.** GDP figures are rough approximations. Use Maddison estimates and flag uncertainty.
9. **Unemployment comparability.** Definitions vary across countries and eras. Flag this rather than presenting numbers as comparable.
10. **Target length.** Aim for 4,000-8,000 words depending on how eventful the year was.
11. **References are always at the end, IEEE/Vancouver style. Never inline.**

---

## IF OUTPUT IS TRUNCATED

If the response hits length limits, stop at a clean section break and note "[CONTINUED IN NEXT RESPONSE]". On continuation, pick up from the last completed section and finish through References.

---

Save the final output as: `{{YEAR}}.md`
```
