---
name: "claude-ads"
description: "Multi-platform paid advertising audit & optimization. Audit Google, Meta, YouTube, LinkedIn, TikTok, Microsoft, Apple, Amazon Ads với 250+ weighted checks, scoring 0-100, industry benchmarks, và actionable recommendations. Dùng /ads audit để chạy audit toàn diện."
---

# Claude Ads: Paid Advertising Audit & Optimization

## 10-Principle Thinking Framework

Mọi audit, plan, hay creative output đều vận hành dưới một kỷ luật nhận thức chung. Không phải checklist hay phase model — mà là mindset gate.

**5 cặp nguyên tắc:** OBSERVE × 2 (External + Internal) → LISTEN → THINK → CONNECT × 2 (Lateral + System) → FEEL → ACCEPT → CREATE → GROW

1. **OBSERVE — External Input**: Thu thập data trước khi hình thành giả thuyết. Export account data, SERP, landing page.
2. **OBSERVE — Internal Metacognition**: Audit cách bạn đang suy nghĩ. Có bias không? Đang áp dụng B2B heuristic cho local plumber?
3. **LISTEN — Active Receptivity**: Đọc campaign brief, platform guidance, community feedback trước khi recommend.
4. **THINK — Critical Processing**: Tính unit economics bằng tay. Xây funnel: impression → click → landing → micro-conversion → primary conversion → revenue → repeat.
5. **CONNECT — Lateral Insight**: Pattern matching giữa các platform. Budget constraint chỗ này thường đi kèm scaling opportunity chỗ kia.
6. **CONNECT — System Orchestration**: Toàn bộ hệ thống tracking + attribution + bidding hoạt động như một hệ thống, không phải silo.
7. **FEEL — Emotional Intelligence**: Đọc giữa dòng campaign brief. "More leads" có thể là "I'm getting fired if pipeline drops."
8. **ACCEPT — Intellectual Humility**: Nói "I don't know" khi data không đủ. Không recommend Smart Bidding nếu không biết conversion volume.
9. **CREATE — Generative Output**: Kết hợp data + insight thành actionable deliverable.
10. **GROW — Iterative Loop**: Mỗi audit là baseline cho lần sau.

## Context Intake (Bắt buộc trước mọi audit)

Hỏi những câu này (gộp vào 1 message):
1. **Ngành / Loại hình business**: SaaS · E-commerce · Local Service · B2B Enterprise · Info Products · Mobile App · Real Estate · Healthcare · Finance · Agency · Other
2. **Ngân sách hàng tháng**: Tổng budget và phân bổ per-platform (approximate OK)
3. **Mục tiêu chính**: Sales/Revenue · Leads/Demos · App Installs · Calls · Brand
4. **Platform đang chạy**: Platform nào đang dùng?

Nếu user cung cấp data upfront, extract context và proceed — không hỏi lại.

## Weighted Scoring System

### Công thức
```
S_total = Σ(C_pass × W_sev × W_cat) / Σ(C_total × W_sev × W_cat) × 100
```
- `C_pass` = 1 (PASS), 0.5 (WARNING), 0 (FAIL)
- `W_sev` = severity multiplier (Critical 5.0, High 3.0, Medium 1.5, Low 0.5)
- `W_cat` = category weight
- Result: 0-100

### Grade
| Score | Grade |
|-------|-------|
| 90-100 | A |
| 75-89 | B |
| 60-74 | C |
| 40-59 | D |
| <40 | F |

### Aggregate Score
```
Aggregate = Sum(Platform_Score × Platform_Budget_Share)
```

---

## GOOGLE ADS AUDIT (80 checks)

**Category Weights:** Conversion 25% | Waste 20% | Structure 15% | Keywords 15% | Ads 15% | Settings 10%

### Conversion Tracking (25%)
- [G01] Google tag (gtag.js) installed và firing trên tất cả pages
- [G02] Enhanced Conversions active (hashed first-party data)
- [G03] Consent Mode v2 implemented (EU/EEA required)
- [G04] Conversion actions mapped correctly (primary vs secondary)
- [G05] Offline conversion import configured (cho lead gen)
- [G06] Server-side tagging via GTM (recommended)
- [G07] Attribution model: Data-Driven preferred (last-click fallback)
- [G08] Conversion lag analysis
- [G09] Cross-domain tracking configured nếu có multiple domains
- [G10] GA4 property linked với Google Ads
- [G11] Conversion action status: tất cả đang RECEIVING
- [G12] CTV conversion tracking cho YouTube campaigns

### Wasted Spend / Negatives (20%)
- [G13] Search Terms Report reviewed (last 30 days minimum)
- [G14] Negative keyword coverage: shared lists + campaign-level
- [G15] Display placement audit: exclude low-quality sites
- [G16] Invalid click rate trong norms (<10%)
- [G17] Broad Match chỉ dùng với Smart Bidding (KHÔNG bao giờ không có)
- [G18] Brand/non-brand campaigns separated
- [G19] Geographic targeting precise (không wasted international spend)
- [G20] Negative keyword rules: Exact Match [keyword] default, Phrase Match "keyword" cho intent patterns, nguồn từ Search Terms Report thực tế, không bao giờ Broad Match negatives

### Account Structure (15%)
- [G21] Campaign organization theo business logic
- [G22] Ad groups themed tightly (15-20 keywords max/group)
- [G23] RSA ad groups có ≥3 active ads
- [G24] PMax campaigns structured correctly (asset groups, signals)
- [G25] SKAGs evaluated — migrate to themed groups
- [G26] Campaign labels/naming conventions consistent
- [G27] Campaign priority settings: không conflict (same keywords split)
- [G28] Experiment campaigns active
- [G29] Draft campaigns không bị abandoned
- [G30] Shared budgets used where appropriate
- [G31] Frequency capping set cho Display/YouTube
- [G32] Campaign groupings theo funnel stage

### Keywords & Quality Score (15%)
- [G33] Match type strategy: Exact → Phrase → Broad progression
- [G34] Quality Score distribution: aim ≥7 average
- [G35] Low QS keywords flagged (<5 = FAIL, 5-6 = WARNING)
- [G36] Keyword cannibalization check
- [G37] Impression share tracked cho top keywords
- [G38] Keyword bid adjustments set (device/location/audience)
- [G39] Search Terms Report negative mining weekly
- [G40] Long-tail keyword coverage trong mỗi ad group

### Ads & Assets (15%)
- [G41] RSA: ≥8 unique headlines, ≥3 descriptions per ad group
- [G42] RSA: ad strength "Good" hoặc "Excellent"
- [G43] Pin usage minimal và strategic
- [G44] Ad extensions: sitelinks (≥4), callouts (≥4), structured snippets, image
- [G45] Dynamic keyword insertion used appropriately
- [G46] Ad copy includes CTA, value proposition, differentiators
- [G47] PMax asset group: tối thiểu 5 headlines, 5 descriptions, 3 images, 1 logo
- [G48] PMax: product feed đầy đủ, không có disapproval
- [G49] Image extensions active cho RSA
- [G50] Call ad extensions: phone number chính xác
- [G51] Price extensions tested cho e-commerce / SaaS
- [G52] Demand Gen campaigns: video+image mix

### Settings & Targeting (10%)
- [G53] ECPC flagged as deprecated — migrate to Smart Bidding
- [G54] Bid strategy phù hợp campaign maturity và goals
- [G55] Budget pacing: không campaign nào limited by budget
- [G56] Ad schedule aligned với business hours/conversion patterns
- [G57] Device bid adjustments based on performance data
- [G58] Location targeting: "Presence" not "Presence or Interest"
- [G59] Network settings: Search Partners reviewed, Display opt-out
- [G60] Landing page experience: load speed, mobile-friendliness, relevance
- [G61] Ad rotation: "Optimize" (không "Rotate indefinitely")
- [G-AI1] AI Max: `enable_ai_max` evaluated — negative keyword discipline, AI Brief
- [G-AI2] AI Brief quality-check output, brand safety
- [G-AI3] FUE (Final URL Expansion): kiểm tra unintended landing pages
- [G-AI4] Brand exclusions trong AI Max campaigns

---

## META ADS AUDIT (50 checks)

**Category Weights:** Pixel/CAPI 30% | Creative 30% | Structure 20% | Audience 20%

### Pixel & CAPI Health (30%)
- [M01] Meta Pixel installed và firing on all pages
- [M02] Conversions API (CAPI) active server-side
- [M03] Event Match Quality (EMQ) ≥8.0 cho Purchase
- [M04] All standard events: PageView, ViewContent, AddToCart, InitiateCheckout, Purchase, Lead, CompleteRegistration
- [M05] Deduplication via event_id giữa Pixel và CAPI
- [M06] CAPI Gateway preferred over manual implementation
- [M07] Custom domain configured cho CAPI (không bị ad-blockers)
- [M08] Test events verified trong Events Manager
- [M09] Parameters completeness: all matching fields populated
- [M10] Server-side hit ratio ≥80%

### Creative & Andromeda (30%)
- [M11] ≥10 genuinely distinct creatives
- [M12] Không cặp nào Similarity Score >60% (Andromeda suppression)
- [M13] Format diversity: ≥3 formats (image, video, carousel, collection)
- [M14] Hook diversity (video): ≥3 hook patterns
- [M15] Headline diversity: ≥3 structures
- [M16] TOF creative lifespan ≤4 weeks (frequency >3 = warning)
- [M17] BOF creative lifespan ≤7 weeks (frequency >8 = warning)
- [M18] Creative-as-targeting score: Concept+Format+Visual+Hook+Headline /10 — target ≥8
- [M19] CTR decline >20% over 14 days = flag
- [M20] Video creatives: ≤15s TOF, ≤30s BOF
- [M21] Carousel ads: ≥3 cards, unique value prop per card
- [M22] UGC-style content tested

### Account Structure (20%)
- [M23] Campaign objective matching funnel stage
- [M24] Advantage+ Sales / App Campaigns evaluated
- [M25] ASC/AAC: MAPI v25 migrated to objective-default model
- [M26] Ad set consolidation: avoid learning phase hell
- [M27] Budget sufficiency: ≥5x CPA per ad set
- [M28] Minimum 3 ads per ad set
- [M29] Dynamic Creative tested
- [M30] CBO (Campaign Budget Optimization) enabled
- [M31] Campaign spending cap set
- [M32] Không edit khi đang learning phase
- [M33] Ad scheduling aligned with conversion time-of-day
- [M34] Minimum 1 week data before scaling
- [M-AND1] Entity-ID clustering: creative visual/headline/body fingerprint check
- [M-AND2] Advantage+ Audience ON/OFF intentional
- [M-AND3] iOS ATT opt-in rate tracked
- [M-AND4] CAPI as backup khi Pixel data drops

### Audience & Targeting (20%)
- [M35] Audience overlap check: loại overlap >50%
- [M36] Exclusion targeting: exclude converters từ prospecting
- [M37] Custom Audiences: pixel events, customer list, engagement
- [M38] Lookalike source ≥1,000 (ideal 5,000-50,000)
- [M39] Retargeting: frequency cap ≤3/day, dynamic product ads
- [M40] Advantage+ audience ON/OFF intentional

---

## LINKEDIN ADS AUDIT (27 checks)

**Category Weights:** Technical 25% | Audience 25% | Creative 20% | Lead Gen 15% | Bidding 15%

### Technical Setup (25%)
- [L01] Insight Tag installed và firing
- [L02] Conversions API active
- [L03] Full funnel conversion events (lead → revenue)
- [L04] Revenue attribution tracking enabled
- [L05] CRM integration (Salesforce/HubSpot)
- [L-CRM1] CRM revenue attribution active

### Audience Targeting (25%)
- [L06] Specific job titles (không just functions)
- [L07] Company size filtering matches ICP
- [L08] Seniority level appropriate
- [L09] Matched Audiences: retargeting + contact lists
- [L10] ABM company lists uploaded
- [L11] Audience expansion: OFF precision, ON scale
- [L12] Predictive audiences tested

### Creative & Lead Gen (35%)
- [L13] TLA ≥30% budget ($2.29-4.14 CPC vs $13.23 standard)
- [L14] Format diversity: ≥2 formats (Sponsored Content, Message Ads, Document Ads, Video)
- [L15] Video ads tested
- [L16] Creative refresh every 4-6 weeks
- [L17] Document Ads tested (7% engagement rate)
- [L18] Lead Gen Form ≤5 fields (13% CVR)
- [L19] Lead Gen Form synced CRM real-time
- [L20] Campaign objective matches funnel stage
- [L21] A/B testing active
- [L22] Message ad frequency ≤1 per 30-45 days
- [L-CRM2] EU messaging compliance

### Bidding & Budget (15%)
- [L23] Start Manual CPC, Maximum Delivery = expensive
- [L24] Daily budget ≥$50 Sponsored Content
- [L25] CTR ≥0.44% Sponsored Content
- [L26] CPC $5-7 avg
- [L27] Lead-to-opportunity rate tracked
- [L28] 30-day click / 7-day view attribution

---

## TIKTOK ADS AUDIT (28 checks)

**Category Weights:** Creative 30% | Technical 25% | Bidding 20% | Structure 15% | Performance 10%

### Creative (30%)
- [T05] ≥6 creatives per ad group
- [T06] All video 9:16 vertical 1080×1920
- [T07] Native-looking content (không corporate)
- [T08] Hook in first 1-2 seconds
- [T09] No creative active >7 days với declining CTR
- [T10] Spark Ads tested (~3% CTR)
- [T20] TikTok Shop integration (e-commerce)
- [T21] Video Shopping Ads tested
- [T22] Caption SEO with high-intent keywords
- [T23] Trending audio used (sound-on)
- [T24] Custom CTA button
- [T25] Safe zone compliance: X:40-940, Y:150-1470
- [T-SR1] Spark Ads scaled beyond initial test

### Technical & Bidding (45%)
- [T01] TikTok Pixel installed
- [T02] Events API + ttclid passback
- [T26] Events API Gateway evaluated
- [T27] Standard events configured
- [T28] Advanced matching parameters
- [T11] Bid strategy: Lowest Cost vs Cost Cap
- [T12] Budget ≥50x target CPA per ad group
- [T13] ≥50 conversions/7 days per ad group
- [T-SR2] 3x Kill Rule (CPA >3x target = pause)

### Structure & Performance (25%)
- [T03] Separate prospecting vs retargeting campaigns
- [T04] Smart+ campaigns tested
- [T14] Search Ads Toggle enabled
- [T15] Placement: TikTok, Pangle reviewed
- [T16] Dayparting aligned
- [T-SR3] Ad group bid cap set
- [T17] CTR ≥1.0% in-feed
- [T18] CPA within target
- [T19] Avg video watch time ≥6s

---

## MICROSOFT ADS AUDIT (24 checks)

**Category Weights:** Technical 25% | Syndication 20% | Structure 20% | Creative 20% | Settings 15%

- [MS01] UET tag installed
- [MS02] Enhanced conversions enabled
- [MS03] Google Ads import validated
- [MS04] Search partner network reviewed
- [MS05] Audience Network intentional
- [MS06] Bid targets 20-35% lower than Google
- [MS07] PMax LinkedIn targeting + Target New Customers
- [MS08] Campaign structure follows best practices
- [MS09] Budget 20-30% của Google
- [MS10] LinkedIn profile targeting (B2B advantage)
- [MS-SI1] Scheduled import conflict resolution
- [MS11] RSA ≥8 headlines, ≥3 descriptions
- [MS12] Multimedia Ads tested
- [MS13] Copy optimized cho Bing demographics
- [MS19] Action Extension utilized
- [MS20] Filter Link Extension tested
- [MS21] Video extensions (9:16)
- [MS14] Copilot chat placement enabled (73% CTR lift)
- [MS15] Native conversion goals (không imported)
- [MS16] CPC 20-40% lower than Google
- [MS17] CVR comparable to Google
- [MS18] Impression share tracked
- [MS-CM1] Consent Mode V2 verified
- [MS-CM2] CTV placement reviewed

---

## APPLE ADS (ASA) AUDIT (23 checks)

**Category Weights:** Structure 25% | Bid Health 20% | Creative 20% | Attribution 20% | Budget 15%

- [ASA01] Brand campaign: own app name + misspellings
- [ASA02] Competitor campaign
- [ASA03] Category campaigns: high-intent generics
- [ASA04] Search Match campaigns active
- [ASA05] Search Match ISOLATED from Exact Match
- [ASA06] Search Terms Report → promote winners
- [ASA07] Today Tab campaigns tested
- [ASA08] Product Page placements enabled
- [ASA09] Manual CPT for new accounts
- [ASA10] Maximize Conversions auto-bidder (≥5x CPA budget)
- [ASA11] Bids differentiated by match type
- [ASA12] Keyword-level CPT bids
- [ASA13] TTR ≥2.5% Search Results, ≥1.5% Search Tab
- [ASA14] Conversion rate 50-65% brand, 20-40% category
- [ASA15] Custom Product Pages created
- [ASA16] CPPs have unique screenshots + text
- [ASA17] Product Page Optimization A/B test
- [ASA18] AdAttributionKit registered
- [ASA19] View-through attribution: 24h post-impression
- [ASA20] Configurable attribution windows
- [ASA21] ATT opt-in rate tracked
- [ASA22] CPA Goals with >100 installs/month per campaign
- [ASA23] TAP coverage (Today/Search/Product Pages)

---

## AMAZON ADS AUDIT (20 checks)

**Category Weights:** Search-Term Harvesting 25% | ACOS/TACOS 20% | Structure 15% | Bidding 15% | Brands 10% | Display 10% | DSP 5%

- [AZ01] Auto campaigns per ASIN cluster
- [AZ02] Search Term Report reviewed last 60 days
- [AZ03] Converting terms Auto → Manual Exact
- [AZ04] Non-converting terms Exact Match negative
- [AZ05] Weekly mining cadence
- [AZ06] Portfolio-level ACOS targets (tied to margin)
- [AZ07] TACOS trend tracked (not single point)
- [AZ08] TACOS target ≤10% mature brands
- [AZ09] ACOS: brand <5%, category 15-25%, discovery 25-40%
- [AZ10] Portfolio theo funnel hoặc product line
- [AZ11] Auto + Manual Exact per ASIN
- [AZ12] Manual Keyword + Manual Product + Auto
- [AZ13] Mọi priority ASIN có ≥1 SP campaign
- [AZ14] Dynamic bidding (không Fixed)
- [AZ15] Top of Search placement bid for high-converting terms
- [AZ16] Sponsored Brands HSA per storefront
- [AZ17] SB Video for high-AOV products
- [AZ18] Sponsored Display audiences + contextual
- [AZ19] Amazon DSP programmatic awareness
- [AZ20] Brand Analytics used (Search Terms, Repeat Purchase)

---

## CROSS-PLATFORM ATTRIBUTION & TRACKING

### iOS Attribution (AdAttributionKit)
- AAK registered with Apple Ads
- SKAN → AAK migration complete (post-Apr 10, 2025)
- 24h view-through window configured
- Configurable windows per campaign
- ATT opt-in ≥30%; nếu <30% = modeled reliance
- Privacy threshold: consolidate <1k installs/week campaigns

### Web Attribution
- GA4 model: Data-Driven vs Last-Click — intentional?
- Google Ads: Data-Driven default
- Meta CAPI: 7-day click / 1-day view
- event_id cross-platform dedup strategy
- Consent Mode V2: EEA enforcement verified

### Server-Side Tracking
- sGTM on Cloud Run/GCS with custom domain
- Meta CAPI Gateway (auto-hashing)
- EMQ ≥8.0 Purchase
- event_id dedup: browser vs server matched
- Server-side hit ratio ≥80%
- PII SHA-256 hashing before forwarding

---

## INDUSTRY BENCHMARKS 2026

### Google Ads Search
| Industry | CPC | CTR | CVR |
|----------|-----|-----|-----|
| E-commerce | $1.15 | 4.13% | 2.81% |
| B2B SaaS | $4.50-8.00 | 4.28% | 1.65% |
| Local Services | $7.85-15.00 | 5.50-6.37% | 7.33-15.0% |
| Legal | $8.58-9.21 | 5.20-5.97% | 4.60-5.09% |
| Finance | $3.46-3.77 | 4.65-8.33% | 2.55-3.50% |
| Healthcare | $40+ | 4.90% | 3.10% |
| Real Estate | $1.55-2.53 | 8.43% | 3.28% |

### Meta Ads
| Metric | Benchmark |
|--------|-----------|
| CTR (Traffic) | 1.71% |
| CTR (Leads) | 2.59% |
| CPC | $0.70-$1.92 |
| CVR (Leads) | 7.72% |
| CPL (Leads) | $27.66 |
| ROAS (all) | 2.19:1 |
| ROAS (Advantage+ Sales) | 4.52:1 |
| Creative fatigue TOF | frequency >3 warning, >5 fail |
| Creative fatigue BOF | frequency >8 warning, >12 fail |
| 25 distinct creatives | 17% more conversions, 16% lower cost |

### LinkedIn Ads
| Metric | Benchmark |
|--------|-----------|
| CPC | $5-7 (median $3.94) |
| CTR | 0.44-0.65% |
| CPL | $60-150+ |
| Lead Gen Form CVR | 13% (3.25× landing pages) |
| TLA CPC | $2.29-4.14 (vs $13.23 standard) |

### TikTok & Microsoft
| Platform | Key Benchmarks |
|----------|---------------|
| TikTok CPM | ~$4.26 |
| TikTok Spark Ads CTR | ~3% (vs ~2% standard) |
| Microsoft CPC | 20-40% lower than Google |
| Microsoft Copilot | 73% CTR lift |

---

## QUALITY GATES (Hard Rules — never violate)

1. **Broad Match → Smart Bidding**: Không recommend Broad Match nếu không có Smart Bidding
2. **3x Kill Rule**: Flag CPA >3x target → pause
3. **Budget sufficiency**: Meta ≥5x CPA / ad set, TikTok ≥50x CPA / ad group
4. **Learning phase**: Không recommend edits khi campaign đang learning
5. **Compliance**: Luôn check Special Ad Categories
6. **Creative**: Không silent video trên TikTok (sound-on)
7. **Attribution default**: 7-day click / 1-day view (Meta), Data-Driven (Google)
8. **Andromeda diversity**: Flag nếu <10 genuinely distinct creatives
9. **Privacy infrastructure gate**: Verify tracking stack trước optimization
10. **Không bao giờ Broad Match negatives**: Dùng Exact Match [keyword] hoặc Phrase Match "keyword"

---

## OUTPUT TEMPLATE

### Executive Summary
```
Ads Health Score: XX/100 (Grade: X)
Audit Date: YYYY-MM-DD

Platform Scores:
- Google Ads: XX (Grade X) — XX checks, X critical, X high
- Meta Ads: XX (Grade X) — XX checks, X critical, X high
- LinkedIn Ads: XX (Grade X) — XX checks, X critical, X high
- TikTok Ads: XX (Grade X) — XX checks, X critical, X high
- Microsoft Ads: XX (Grade X) — XX checks, X critical, X high
- Apple Ads: XX (Grade X) — XX checks, X critical, X high
- Amazon Ads: XX (Grade X) — XX checks, X critical, X high

Top Critical Issues:
1. [ID] — [Platform] — [Issue] — [Impact] — [Action] — [ETA]

Quick Wins (fix <15 min):
1. ...
```

### Per-Platform Section
Mỗi platform có score, grade, category breakdown (PASS/WARNING/FAIL), findings + remediation.

### Cross-Platform Analysis
- Budget allocation (actual vs recommended)
- Tracking consistency (cùng events?)
- Creative consistency (messaging aligned?)
- Attribution overlap (double-counting?)

### Strategic Recommendations
- Platform prioritization theo business type
- Budget reallocation
- Scaling opportunities
- Kill list (cần pause ngay)
