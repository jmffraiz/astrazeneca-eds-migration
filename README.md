# AstraZeneca.com → EDS Migration Sizing

**Source:** astrazeneca.com  
**Sitemap crawled:** 7 April 2026 (`https://www.astrazeneca.com/azcomsitemap.xml`)  
**Platform:** AEM CMS (current) → AEM Edge Delivery Services (EDS)  
**Interactive dashboard:** [az-migration-analysis.html](./az-migration-analysis.html)

---

## Site at a Glance


| Metric                          | Value                    |
| ------------------------------- | ------------------------ |
| Total pages (sitemap)           | **2,456**                |
| Distinct page templates         | **12**                   |
| EDS blocks required             | **21**                   |
| Press + medical releases share  | **73.6%** of total pages |
| Estimated delivery (Scenario C) | **~28 weeks**            |


---

## Site Structure

### Top-level sections


| Section               | Pages | % of site |
| --------------------- | ----- | --------- |
| `media-centre`        | 1,808 | 73.6%     |
| `country-sites`       | 215   | 8.8%      |
| `what-science-can-do` | 111   | 4.5%      |
| `our-company`         | 109   | 4.4%      |
| `investor-relations`  | 55    | 2.2%      |
| `r-d`                 | 36    | 1.5%      |
| `our-therapy-areas`   | 33    | 1.3%      |
| `sustainability`      | 32    | 1.3%      |
| `az-suppliers`        | 20    | 0.8%      |
| `partnering`          | 14    | 0.6%      |
| Other                 | ~23   | 0.9%      |


### media-centre breakdown


| Sub-section        | Pages | Notes                                                  |
| ------------------ | ----- | ------------------------------------------------------ |
| `press-releases`   | 1,606 | Year-based URLs (`/YYYY/slug`), archive from 2009–2026 |
| `medical-releases` | 127   | Flat URLs (no year folder)                             |
| `articles`         | 69    | Editorial, Veeva ID footer                             |
| Static pages       | 6     | pdf, archive, contacts, image-and-broadcast-library    |


### country-sites breakdown


| Country            | Pages          |
| ------------------ | -------------- |
| Thailand           | 173            |
| Singapore          | 17             |
| 24 other countries | 1–2 pages each |


### Press release year distribution


| Years     | Pages                |
| --------- | -------------------- |
| 2009–2018 | ~751 (older archive) |
| 2019–2021 | ~376                 |
| 2022–2023 | ~251                 |
| 2024–2026 | ~228 (most recent)   |


---

## 12 Identified Page Templates

### Low complexity

#### 1. Press Release

- **Count:** 1,606 pages (65.4% of site)
- **URL pattern:** `/media-centre/press-releases/YYYY/slug.html`
- **Structure:** Title → date/location standfirst → body paragraphs with quotes → "Notes to Editors" section → media/investor contacts
- **Blocks:** `hero-text`, `rich-text`, `contact-card`, `download-list`
- **Example:** [Full Year Q4 2025 Results](https://www.astrazeneca.com/media-centre/press-releases/2026/full-year-q4-2025-results.html)

#### 2. Medical Release

- **Count:** 127 pages (5.2%)
- **URL pattern:** `/media-centre/medical-releases/slug.html` (flat, no year folder)
- **Structure:** Similar to press release. Clinical data announcement, About sections (compound, trial, disease), media/investor contacts footer
- **Blocks:** `hero-text`, `rich-text`, `contact-card`
- **Example:** [Anifrolumab Phase II Lupus Data](https://www.astrazeneca.com/media-centre/medical-releases/Arthritis-and-Rheumatology-publishes-positive-Phase-II-data-on-anifrolumab-in-lupus-14112016.html)

---

### Medium complexity

#### 3. Editorial Article

- **Count:** 69 pages (2.8%)
- **URL pattern:** `/media-centre/articles/slug.html`
- **Structure:** Hero image → H2/H3 sections → stats callout blocks → related articles carousel → "You may also like" → back-to-index link → Veeva ID footer
- **Blocks:** `hero`, `rich-text`, `stats-callout`, `related-articles`, `cta-banner`
- **Example:** [Pioneering New Possibilities for the Rare Disease Community](https://www.astrazeneca.com/media-centre/articles/pioneering-new-possibilities-for-the-rare-disease-community.html)

#### 4. What Science Can Do Topic

- **Count:** 107 pages (4.4%)
- **URL pattern:** `/what-science-can-do/topics/{sub-topic}/slug.html`
- **Sub-topics:** disease-understanding (31), next-generation-therapeutics (22), clinical-innovation (15), technologies (14), data-science-ai (12), sustainability (11), covid-19 (2)
- **Structure:** Hero → author bylines (name + title) → topic tags → body sections → related stories → email signup CTA → "You may also like" → Veeva ID
- **Blocks:** `hero`, `author-byline`, `rich-text`, `topic-tags`, `related-articles`, `email-signup`
- **Example:** [Turning Nature's Messengers into Medicines](https://www.astrazeneca.com/what-science-can-do/topics/next-generation-therapeutics/turning-natures-messengers-medicines-innovation-peptide-discovery-development.html)

#### 5. People Profile

- **Count:** ~100 pages (4.1%)
- **URL pattern:** `/our-company/our-people/slug.html`
- **Structure:** Name + title + photo → biography text → career timeline with year ranges → featured publications list
- **Blocks:** `profile-hero`, `rich-text`, `timeline`, `publications-list`
- **Example:** [Cristina Durán — President, Evinova](https://www.astrazeneca.com/our-company/our-people/cristina-duran.html)

#### 6. Investor Relations

- **Count:** 55 pages (2.2%)
- **URL pattern:** `/investor-relations/slug.html`
- **Structure:** Mix of list pages (annual reports with year-grouped PDF downloads back to 2004), results/events pages with webcast links, and financial information pages
- **Blocks:** `hero-text`, `download-list`, `year-group`, `webcast-cta`
- **Example:** [Annual Reports](https://www.astrazeneca.com/investor-relations/annual-reports.html)

#### 7. Sustainability

- **Count:** 32 pages (1.3%)
- **URL pattern:** `/sustainability/{sub-topic}/slug.html`
- **Sub-topics:** nature, ethics-compliance, health-equity, climate-change, resources, health-systems-resilience, workforce-safety-and-health, partnerships-and-alliances
- **Structure:** Hub + detail pages with stats, targets, report downloads, infographic-style content sections
- **Blocks:** `hero`, `stats-callout`, `rich-text`, `download-list`, `nav-cards`
- **Example:** [Ethics & Compliance](https://www.astrazeneca.com/sustainability/ethics-compliance.html)

#### 8. Partnering / AZ Suppliers

- **Count:** 34 pages (1.4%)
- **URL pattern:** `/partnering/slug.html`, `/az-suppliers/slug.html`
- **Structure:** Partnering interest pages, supplier portal (Coupa integration), external funding forms. Some pages may require iframe/embed strategy for Coupa rather than native EDS.
- **Blocks:** `hero-text`, `rich-text`, `cta-banner`, `external-embed`
- **Examples:** [Why Partner with AZ](https://www.astrazeneca.com/partnering/why-partner-with-astrazeneca.html) · [Coupa Supplier Portal](https://www.astrazeneca.com/az-suppliers/az-coupa-supplier.html)

---

### High complexity

#### 9. R&D Deep Content

- **Count:** 36 pages (1.5%)
- **URL pattern:** `/r-d/{sub-topic}/slug.html`
- **Structure:** Very long-form pages with jump-to navigation, embedded video references, tabbed content panels, partnership cards, pipeline data, external collaboration listings, CTA sections. Heavy rich media use.
- **Blocks:** `hero`, `breadcrumb`, `jump-nav`, `video-embed`, `cards-grid`, `accordion`, `partner-list`, `cta-banner`, `references`
- **Example:** [Cell Therapies](https://www.astrazeneca.com/r-d/next-generation-therapeutics/cell-therapies.html)

#### 10. Therapy Area Hub

- **Count:** 33 pages (1.3%)
- **URL pattern:** `/our-therapy-areas/{area}.html` and sub-pages
- **Therapy areas:** Oncology, CVRM, Respiratory & Immunology, Vaccines & Immune Therapies, Rare Disease
- **Structure:** Hub/landing page with navigation tiles to sub-areas, disease spotlight sections, team member cards, dynamic latest news feed, resources section, CTA banners
- **Blocks:** `hero`, `breadcrumb`, `nav-cards`, `disease-spotlight`, `team-card`, `news-feed`, `resources`
- **Example:** [Oncology Therapy Area Hub](https://www.astrazeneca.com/our-therapy-areas/oncology.html)

#### 11. Country Sites

- **Count:** 215 pages (8.8%)
- **URL pattern:** `/country-sites/{country}/...`
- **Structure:** Local market content. Thailand (173 pages) and Singapore (17 pages) have significant depth; 24 other countries have 1–2 pages. Requires dedicated localisation strategy.
- **Blocks:** `locale-routing`, `hero`, `rich-text`, `nav-cards`
- **Examples:** [Thailand](https://www.astrazeneca.com/country-sites/thailand.html) · [Singapore](https://www.astrazeneca.com/country-sites/singapore.html)

#### 12. Homepage

- **Count:** 1 page (unique)
- **URL:** `https://www.astrazeneca.com/`
- **Structure:** Full-screen hero with video/image, trending story highlight, editorial article cards, CEO quote with results CTA, animated stat counter ("197 projects"), location showcases, sustainability teaser. Highly designed with many bespoke sections.
- **Blocks:** `hero-video`, `featured-articles`, `quote-cta`, `stat-counter`, `location-card`, `sustainability-teaser`
- **Example:** [astrazeneca.com](https://www.astrazeneca.com/)

---

## 21 EDS Blocks Required


| Block               | Templates                                | Coverage | Example page                                                                                                                                                                                |
| ------------------- | ---------------------------------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `hero`              | 9/12                                     | 90%      | [Oncology hub](https://www.astrazeneca.com/our-therapy-areas/oncology.html)                                                                                                                 |
| `rich-text`         | 11/12                                    | 100%     | [Rare disease article](https://www.astrazeneca.com/media-centre/articles/pioneering-new-possibilities-for-the-rare-disease-community.html)                                                  |
| `hero-text`         | Press/Medical releases                   | 40%      | [Q4 2025 results](https://www.astrazeneca.com/media-centre/press-releases/2026/full-year-q4-2025-results.html)                                                                              |
| `stats-callout`     | Articles, WSCD, Sustainability           | 45%      | [Rare disease article](https://www.astrazeneca.com/media-centre/articles/pioneering-new-possibilities-for-the-rare-disease-community.html)                                                  |
| `author-byline`     | WSCD Topics                              | 15%      | [Peptide discovery](https://www.astrazeneca.com/what-science-can-do/topics/next-generation-therapeutics/turning-natures-messengers-medicines-innovation-peptide-discovery-development.html) |
| `related-articles`  | Articles, WSCD, R&D                      | 40%      | [Rare disease article](https://www.astrazeneca.com/media-centre/articles/pioneering-new-possibilities-for-the-rare-disease-community.html)                                                  |
| `email-signup`      | WSCD Topics                              | 15%      | [Peptide discovery](https://www.astrazeneca.com/what-science-can-do/topics/next-generation-therapeutics/turning-natures-messengers-medicines-innovation-peptide-discovery-development.html) |
| `jump-nav`          | R&D deep content                         | 20%      | [Cell therapies](https://www.astrazeneca.com/r-d/next-generation-therapeutics/cell-therapies.html)                                                                                          |
| `video-embed`       | R&D, Therapy hubs                        | 25%      | [Cell therapies](https://www.astrazeneca.com/r-d/next-generation-therapeutics/cell-therapies.html)                                                                                          |
| `cards-grid`        | Multiple hub pages                       | 55%      | [Oncology hub](https://www.astrazeneca.com/our-therapy-areas/oncology.html)                                                                                                                 |
| `accordion`         | R&D, FAQ sections                        | 30%      | [Cell therapies](https://www.astrazeneca.com/r-d/next-generation-therapeutics/cell-therapies.html)                                                                                          |
| `download-list`     | Press releases, Investor, Sustainability | 50%      | [Annual reports](https://www.astrazeneca.com/investor-relations/annual-reports.html)                                                                                                        |
| `timeline`          | People profiles                          | 15%      | [Cristina Durán](https://www.astrazeneca.com/our-company/our-people/cristina-duran.html)                                                                                                    |
| `publications-list` | People profiles                          | 15%      | [Cristina Durán](https://www.astrazeneca.com/our-company/our-people/cristina-duran.html)                                                                                                    |
| `news-feed`         | Therapy hubs, Homepage                   | 30%      | [Oncology hub](https://www.astrazeneca.com/our-therapy-areas/oncology.html)                                                                                                                 |
| `quote-cta`         | Homepage, R&D pages                      | 20%      | [Homepage](https://www.astrazeneca.com/)                                                                                                                                                    |
| `stat-counter`      | Homepage                                 | 10%      | [Homepage](https://www.astrazeneca.com/)                                                                                                                                                    |
| `breadcrumb`        | Most content pages                       | 80%      | [Cell therapies](https://www.astrazeneca.com/r-d/next-generation-therapeutics/cell-therapies.html)                                                                                          |
| `topic-tags`        | WSCD Topics                              | 15%      | [Peptide discovery](https://www.astrazeneca.com/what-science-can-do/topics/next-generation-therapeutics/turning-natures-messengers-medicines-innovation-peptide-discovery-development.html) |
| `contact-card`      | Press/Medical releases                   | 40%      | [Medical release](https://www.astrazeneca.com/media-centre/medical-releases/Arthritis-and-Rheumatology-publishes-positive-Phase-II-data-on-anifrolumab-in-lupus-14112016.html)              |
| `external-embed`    | Partnering/Suppliers                     | 10%      | [Coupa supplier](https://www.astrazeneca.com/az-suppliers/az-coupa-supplier.html)                                                                                                           |


---

## Effort Sizing

### Workstreams (Scenario C — new content only)


| Workstream                     | Scope                                  | Complexity | Points      | Notes                                                          |
| ------------------------------ | -------------------------------------- | ---------- | ----------- | -------------------------------------------------------------- |
| Block development              | 21 blocks                              | High       | 55          | Heaviest engineering work; blocks reused across templates      |
| Template builds                | 12 templates                           | High       | 28          | Wire up blocks into page templates; content model per template |
| Content import scripts         | Press releases + people profiles       | Medium     | 20          | Node.js scripts to batch-import from current CMS               |
| Global styles + typography     | styles.css, fonts.css, lazy-styles.css | Medium     | 12          | Design system tokens, brand fonts, responsive grid             |
| Header + footer                | Global navigation + footer nav         | Medium     | 8           | Mega-nav with therapy area dropdowns                           |
| Performance + accessibility QA | Lighthouse 100 across all templates    | Medium     | 10          | LCP optimisation, WCAG 2.2 AA, keyboard navigation             |
| Country sites (Thailand)       | 173-page local site                    | High       | 15          | Locale routing, separate template setup or separate repo       |
| Integrations                   | Veeva, analytics, Coupa                | Medium     | 10          | Analytics data layer, Veeva ID display, supplier portal embed  |
| EDS setup + infra              | GitHub, Code Sync, domain config       | Low        | 5           | One-time setup of AEM bot, preview/live domains                |
| Content migration QA           | Sampling + spot-checks                 | Low        | 7           | Author and QA validation of migrated content                   |
| **Total**                      |                                        |            | **150 pts** | ~1 pt = 1 dev day for senior EDS developer                     |


### Archive scope scenarios


| Scenario                               | Pages    | Press releases               | Import scripts | Δ effort     |
| -------------------------------------- | -------- | ---------------------------- | -------------- | ------------ |
| A — Full archive                       | 2,456    | All 2009–2026                | ~3 scripts     | +40 pts      |
| B — 5-year archive                     | ~1,040   | 2022–2026                    | ~2 scripts     | +18 pts      |
| **C — New content only ✓ Recommended** | **~650** | **2024–2026 + archive link** | **~1 script**  | **Baseline** |


---

## Key Risks & Decisions


| Risk                                 | Impact                                                                                                 | Decision needed     |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------- |
| **Press release archive scope**      | Biggest single scope lever — swings effort by 40 pts                                                   | Before Phase 1 ends |
| **Country sites localisation**       | Thailand's 173 pages need a dedicated locale strategy (separate site vs. multi-locale EDS)             | Before Phase 5      |
| **Video hosting**                    | R&D pages contain many embedded videos; need video hosting strategy (Brightcove? YouTube? Native EDS?) | Before Phase 3      |
| **Veeva ID / MLR approval workflow** | Medical content carries Veeva IDs and approval dates; must be validated with Regulatory                | Before Phase 2      |
| **Coupa supplier portal**            | AZ Suppliers section likely needs an iframe/embed rather than native EDS                               | Before Phase 4      |
| **Dynamic news feeds**               | Therapy area pages pull live press release listings; requires EDS indexing setup                       | Before Phase 3      |


---

## Recommended Migration Phases

### Phase 1 — Foundation & Core Templates (Weeks 1–6, ~50 pts)

Deliverables: global styles + fonts, header/footer blocks, `hero` block, `rich-text`, Press Release template, Medical Release template, import script v1, breadcrumb/navigation.

Start with the highest-volume, lowest-complexity content. Press releases alone are 65% of the site — getting these right first validates the EDS setup and import pipeline with real data.

### Phase 2 — Editorial & Thought Leadership (Weeks 7–12, ~40 pts)

Deliverables: Editorial Article template, WSCD Topic template, `stats-callout`, `author-byline`, `related-articles`, `email-signup`, `references`, `topic-tags`.

Articles and WSCD topics share many blocks — build once, reuse across both. Veeva ID / MLR validation process must be confirmed with Regulatory before this phase.

### Phase 3 — Deep Science & Therapy Content (Weeks 13–19, ~45 pts)

Deliverables: R&D Deep Content template, Therapy Area Hub template, `jump-nav`, `video-embed`, `cards-grid`, `accordion`, `news-feed` (EDS indexing), pipeline table block.

Highest per-page complexity. Content modeling with authors must happen before development. Video hosting strategy and EDS indexing must both be confirmed before work starts.

### Phase 4 — Corporate & Investor Content (Weeks 20–23, ~25 pts)

Deliverables: People Profile template, Investor Relations template, Sustainability pages, `timeline`, `download-list`, `publications-list`, `year-group`.

People profiles are consistent and structured — good candidate for bulk migration via import script. Annual report pages (back to 2004) need the same archive scope decision as press releases.

### Phase 5 — Homepage & Country Sites (Weeks 24–28, ~40 pts)

Deliverables: Homepage (bespoke design), `hero-video`, `stat-counter`, `featured-articles`, Thailand country site, locale routing, Coupa/supplier integration, go-live performance audit.

Homepage is deliberately last — it's high-visibility and unique, and benefits from all blocks already being built. Thailand's depth warrants consideration as a parallel stream once the core EDS setup is proven.

---

## Key Success Factors

- **Content-first:** Model every template in Word/Google Docs before writing any EDS code
- **Import scripts for volume:** Press releases and people profiles should be migrated programmatically, not manually
- **MLR/Veeva alignment:** Agree with Regulatory on how Veeva IDs and approval dates are stored in the EDS content model before Phase 2
- **Lighthouse 100 baseline:** Establish in Phase 1 and protect throughout — easier to maintain than recover
- **Archive decision early:** Press release scope must be decided before Phase 1 ends
- **Country site strategy:** Thailand's depth warrants a dedicated decision before Phase 5

