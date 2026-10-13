# City Grill Performance Overview

Interactive financial dashboard for **City Grill Group** (Romanian restaurant and hospitality group).

## What the dashboard shows

- Consolidated revenue FY2023–FY2025 and the FY2026 target (EUR 100M / RON 500M+)
- Average bill (FY2023, H1 2024, FY2025)
- Year-over-year growth: 2024 group, 2025 existing brands vs consolidated (acquisition-affected), required growth for 2026 with the H1 2026 reported growth marked inside it
- EUR / RON switch, year selector, reset, hover tooltips, sortable data table with sources

## Repository contents

| Path | Content |
| --- | --- |
| `index.html` | The dashboard (single file) |
| `data/dashboard_values.csv` | Every value shown on the dashboard, in EUR and RON, with the BNR rate used, growth rates, status, dashboard grade, whether acquisition revenue is included, and observation/source IDs |
| `data/dashboard_observations.csv` | The 23 source observations the dashboard reads, in the Phase 1 schema |
| `sources/ARTICLES.md` | Every article used: link, publisher, date, what the dashboard takes from it and the observation IDs |
| `data/source_register.csv` | Sources used by the dashboard, plus sources added for this release (S52 company website, S53 BNR 2023 cross-check, S54 BNR) |
| `phase1/` | Full Phase 1 research: Excel workbook (9 sheets, live KPI formulas), CSV exports, research report |

## Method

- **Currency.** Figures reported in RON are converted to EUR, and figures reported in EUR to RON, at the BNR annual average of the same year: 2023 4.9464, 2024 4.9746, 2025 5.0415. Growth is calculated with both years in the same currency, so rates differ slightly between EUR and RON. No 2026 annual average exists yet, so the 2026 target uses the two values announced by the company.
- **Grades (dashboard).** A = value reported by the company; B = target or derived value (calculation, conversion). In the Phase 1 dataset the same company figures are graded B, because they come from company releases reproduced in the press rather than filed accounts.
- **Acquisitions.** FY2023 excludes acquisition revenue; FY2024 inclusion of Marty (55% acquired Oct 2024) is not confirmed; FY2025 consolidated includes Marty Restaurants and Aubergine; FY2025 existing brands excludes them.

## Limitations

- Company figures come from company announcements reproduced in Romanian business media; they were not checked against filed financial statements.
- Group profit, EBITDA, monthly revenue and 2026 actual revenue are not public and are not shown.
- 2025 consolidated growth (+32.1% in EUR) includes acquisitions and is not organic.
- H1 2026 growth (+2%) has an unspecified scope and no published absolute value.
- The 2023 BNR average appears as 4.9464 in the dataset and 4.9465 in one relay (S53); the difference does not change any displayed value.
- Independent dashboard on public data; not an official City Grill Group document. Logo and colours are taken from citygrillgroup.ro.

## Main sources

- [Bursa.ro – City Grill Group: cifra de afaceri de 90 milioane euro in 2025](https://www.bursa.ro/city-grill-group-cifra-de-afaceri-de-90-milioane-euro-in-2025-si-venituri-in-crestere-cu-10-procente-23555851)
- [Ziarul Financiar – City Grill Group a incheiat 2025 cu 90 mil. euro](https://www.zf.ro/zf-24/city-grill-group-cel-mare-lant-restaurante-capital-romanesc-fondat-23073813)
- [Epoch Daily – pragul de 500 mil. lei](https://epochdaily.ro/economie/grupul-city-grill-depaseste-pentru-prima-data-pragul-de-500-mil-lei-afaceri-in-timp-ce-piata-horeca-scade)
- [RHN – City Grill invests EUR 6.5 million](https://rhn.ro/en/city-grill-invests-eur-6-5-million-and-expands-network/)
- [Romania-Insider – EUR 60 mln turnover in 2024](https://romania-insider.com/city-grill-group-estimates-over-eur-60-mln-turnover-2024)
- [Romania-Insider – EUR 31 mln in H1 2024](https://www.romania-insider.com/business/city-grill-group-eur-31-mln-revenue-first-6-months-18-growth)
- [Ziarul Financiar – City Grill preia pachetul majoritar Marty](https://www.zf.ro/zf-24/tranzactie-piata-horeca-grupul-restaurante-city-grill-controlat-22509996)
- [Financiarul.ro – BNR curs mediu anual 2025](https://financiarul.ro/economie/bnr-calculeaza-cursul-mediu-anual-al-euro-la-5-0415-lei-pentru-2025/)

Full list with the figures taken from each article: `sources/ARTICLES.md` and `data/source_register.csv`.
