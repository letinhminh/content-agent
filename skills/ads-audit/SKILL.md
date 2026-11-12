---
name: "ads-audit"
description: "Audit và tối ưu quảng cáo trả phí đa nền tảng. Audit Google, Meta, YouTube, LinkedIn, TikTok, Microsoft, Apple, Amazon Ads với hơn 250 kiểm tra có trọng số, chấm điểm 0-100, benchmark ngành và khuyến nghị khả thi. Dùng /ads audit để chạy audit toàn diện."
---

# Ads Audit: Audit và Tối ưu Quảng cáo Trả phí

## 10 Nguyên tắc

**5 cặp nguyên tắc:** QUAN SÁT × 2 (Bên ngoài + Bên trong) → LẮNG NGHE → TƯ DUY → KẾT NỐI × 2 (Ngang + Hệ thống) → CẢM NHẬN → CHẤP NHẬN → SÁNG TẠO → PHÁT TRIỂN

1. **QUAN SÁT — Đầu vào bên ngoài**: Thu thập dữ liệu trước khi hình thành giả thuyết. Xuất dữ liệu tài khoản (export), SERP, trang đích (landing page).
2. **QUAN SÁT — Nhận thức nội bộ (metacognition)**: Audit cách bạn đang suy nghĩ. Có bias không?
3. **LẮNG NGHE — Tiếp nhận chủ động**: Đọc brief chiến dịch, hướng dẫn của nền tảng, phản hồi cộng đồng trước khi đưa ra khuyến nghị.
4. **TƯ DUY — Xử lý phê phán**: Tính unit economics bằng tay. Xây dựng phễu: impression → click → landing → micro-conversion → conversion chính → doanh thu → mua lại.
5. **KẾT NỐI — Hiểu biết chiều ngang**: So khớp pattern giữa các nền tảng. Ràng buộc ngân sách ở nền tảng này thường đi kèm cơ hội mở rộng ở nền tảng kia.
6. **KẾT NỐI — Điều phối hệ thống**: Toàn bộ hệ thống tracking + attribution + bidding hoạt động như một hệ thống thống nhất, không phải các mảnh rời rạc.
7. **CẢM NHẬN — Trí tuệ cảm xúc**: Đọc giữa dòng brief chiến dịch. "More leads" có thể là "I'm getting fired if pipeline drops".
8. **CHẤP NHẬN — Khiêm tốn trí tuệ**: Nói "Tôi không biết" khi dữ liệu chưa đủ. Không khuyến nghị Smart Bidding nếu không biết conversion volume.
9. **SÁNG TẠO — Đầu ra sáng tạo**: Kết hợp dữ liệu + insight thành deliverable có thể hành động.
10. **PHÁT TRIỂN — Vòng lặp lặp lại**: Mỗi audit là baseline cho lần audit tiếp theo.

## Thu thập Ngữ cảnh (Bắt buộc trước mọi audit)

Hỏi những câu này (gộp vào 1 message):
1. **Ngành / Loại hình kinh doanh**: SaaS · Thương mại điện tử (E-commerce) · Dịch vụ địa phương (Local Service) · Doanh nghiệp B2B · Sản phẩm thông tin (Info Products) · Ứng dụng di động (Mobile App) · Bất động sản (Real Estate) · Y tế (Healthcare) · Tài chính (Finance) · Agency · Khác
2. **Ngân sách hàng tháng**: Tổng budget và phân bổ theo từng nền tảng (ước lượng cũng được)
3. **Mục tiêu chính**: Doanh số / Doanh thu (Sales/Revenue) · Leads / Demos · Cài đặt ứng dụng (App Installs) · Cuộc gọi (Calls) · Nhận diện thương hiệu (Brand)
4. **Nền tảng đang chạy**: Đang dùng nền tảng nào?

Nếu người dùng cung cấp dữ liệu ngay từ đầu, trích xuất ngữ cảnh và tiến hành — không hỏi lại.

## Hệ thống Chấm điểm có Trọng số

### Công thức
```
S_total = Σ(C_pass × W_sev × W_cat) / Σ(C_total × W_sev × W_cat) × 100
```
- `C_pass` = 1 (ĐẠT), 0.5 (CẢNH BÁO), 0 (KHÔNG ĐẠT)
- `W_sev` = hệ số mức độ nghiêm trọng (Critical 5.0, High 3.0, Medium 1.5, Low 0.5)
- `W_cat` = trọng số danh mục
- Kết quả: 0-100

### Xếp hạng (Grade)
| Điểm | Xếp hạng |
|------|----------|
| 90-100 | A |
| 75-89 | B |
| 60-74 | C |
| 40-59 | D |
| <40 | F |

### Điểm Tổng hợp
```
Aggregate = Sum(Platform_Score × Platform_Budget_Share)
```

---

## AUDIT GOOGLE ADS (80 kiểm tra)

**Trọng số danh mục:** Conversion 25% | Lãng phí (Waste) 20% | Cấu trúc 15% | Từ khóa 15% | Quảng cáo 15% | Cài đặt 10%

### Theo dõi Conversion (25%)
- [G01] Google tag (gtag.js) đã cài đặt và firing trên tất cả các trang
- [G02] Enhanced Conversions đang bật (dữ liệu first-party đã hash)
- [G03] Consent Mode v2 đã triển khai (bắt buộc cho EU/EEA)
- [G04] Conversion actions được map đúng (primary vs secondary)
- [G05] Cấu hình nhập conversion offline (cho lead gen)
- [G06] Server-side tagging qua GTM (được khuyến nghị)
- [G07] Mô hình attribution: ưu tiên Data-Driven (last-click chỉ là fallback)
- [G08] Phân tích độ trễ conversion (conversion lag)
- [G09] Cấu hình cross-domain tracking nếu có nhiều domain
- [G10] Property GA4 đã liên kết với Google Ads
- [G11] Trạng thái conversion action: tất cả đang ở trạng thái RECEIVING
- [G12] Theo dõi conversion CTV cho các chiến dịch YouTube

### Chi tiêu lãng phí / Từ khóa phủ định (20%)
- [G13] Search Terms Report đã được xem xét (tối thiểu 30 ngày gần nhất)
- [G14] Bao phủ negative keyword: shared lists + cấp độ campaign
- [G15] Audit placement hiển thị (Display): loại trừ các site kém chất lượng
- [G16] Tỷ lệ invalid click trong ngưỡng cho phép (<10%)
- [G17] Broad Match chỉ dùng cùng Smart Bidding (KHÔNG bao giờ dùng một mình)
- [G18] Campaign brand / non-brand đã tách riêng
- [G19] Targeting địa lý chính xác (không lãng phí chi tiêu quốc tế)
- [G20] Quy tắc negative keyword: Exact Match [keyword] mặc định, Phrase Match "keyword" cho intent patterns, nguồn từ Search Terms Report thực tế, không bao giờ dùng Broad Match negatives

### Cấu trúc Tài khoản (15%)
- [G21] Tổ chức campaign theo logic kinh doanh
- [G22] Ad groups theo theme chặt chẽ (tối đa 15-20 keywords/group)
- [G23] Ad groups RSA có ≥3 quảng cáo đang active
- [G24] Campaign PMax cấu trúc đúng (asset groups, signals)
- [G25] Đánh giá SKAGs — migrate sang themed groups
- [G26] Campaign labels / naming conventions nhất quán
- [G27] Cài đặt ưu tiên campaign: không conflict (không split cùng keyword)
- [G28] Campaign experiment đang active
- [G29] Campaign draft không bị bỏ abandoned
- [G30] Shared budgets được dùng ở nơi phù hợp
- [G31] Frequency capping đã đặt cho Display/YouTube
- [G32] Nhóm campaign theo funnel stage

### Từ khóa & Quality Score (15%)
- [G33] Chiến lược match type: Exact → Phrase → Broad theo lộ trình
- [G34] Phân phối Quality Score: mục tiêu trung bình ≥7
- [G35] Từ khóa QS thấp đã được flag (<5 = KHÔNG ĐẠT, 5-6 = CẢNH BÁO)
- [G36] Kiểm tra keyword cannibalization
- [G37] Theo dõi impression share cho các keyword hàng đầu
- [G38] Bid adjustments theo keyword đã đặt (device/location/audience)
- [G39] Khai thác Search Terms Report để tạo negatives hàng tuần
- [G40] Bao phủ từ khóa long-tail trong mỗi ad group

### Quảng cáo & Assets (15%)
- [G41] RSA: ≥8 headlines duy nhất, ≥3 descriptions mỗi ad group
- [G42] RSA: ad strength "Good" hoặc "Excellent"
- [G43] Pin usage tối thiểu và có chiến lược
- [G44] Ad extensions: sitelinks (≥4), callouts (≥4), structured snippets, image
- [G45] Dynamic keyword insertion dùng hợp lý
- [G46] Ad copy có CTA, value proposition, differentiators
- [G47] Asset group PMax: tối thiểu 5 headlines, 5 descriptions, 3 images, 1 logo
- [G48] PMax: product feed đầy đủ, không có disapproval
- [G49] Image extensions active cho RSA
- [G50] Call ad extensions: số điện thoại chính xác
- [G51] Price extensions đã test cho e-commerce / SaaS
- [G52] Campaign Demand Gen: mix video + image

### Cài đặt & Targeting (10%)
- [G53] ECPC được flag là deprecated — migrate sang Smart Bidding
- [G54] Bid strategy phù hợp với maturity và mục tiêu của campaign
- [G55] Budget pacing: không campaign nào bị limited by budget
- [G56] Ad schedule căn theo giờ kinh doanh / conversion patterns
- [G57] Device bid adjustments dựa trên performance data
- [G58] Location targeting: "Presence" không phải "Presence or Interest"
- [G59] Network settings: Search Partners đã review, Display opt-out
- [G60] Landing page experience: tốc độ tải, mobile-friendliness, relevance
- [G61] Ad rotation: "Optimize" (không "Rotate indefinitely")
- [G-AI1] AI Max: đã đánh giá `enable_ai_max` — kỷ luật negative keyword, AI Brief
- [G-AI2] AI Brief: kiểm tra chất lượng output, brand safety
- [G-AI3] FUE (Final URL Expansion): kiểm tra unintended landing pages
- [G-AI4] Brand exclusions trong các campaign AI Max

---

## AUDIT META ADS (50 kiểm tra)

**Trọng số danh mục:** Pixel/CAPI 30% | Creative 30% | Cấu trúc 20% | Audience 20%

### Pixel & CAPI Health (30%)
- [M01] Meta Pixel đã cài đặt và firing trên tất cả các trang
- [M02] Conversions API (CAPI) active server-side
- [M03] Event Match Quality (EMQ) ≥8.0 cho Purchase
- [M04] Đủ tất cả standard events: PageView, ViewContent, AddToCart, InitiateCheckout, Purchase, Lead, CompleteRegistration
- [M05] Deduplication qua event_id giữa Pixel và CAPI
- [M06] CAPI Gateway được ưu tiên hơn manual implementation
- [M07] Custom domain đã cấu hình cho CAPI (không bị ad-blockers)
- [M08] Test events đã verify trong Events Manager
- [M09] Đầy đủ parameters: tất cả matching fields đã populate
- [M10] Server-side hit ratio ≥80%

### Creative & Andromeda (30%)
- [M11] ≥10 creatives thực sự khác biệt (genuinely distinct)
- [M12] Không cặp nào Similarity Score >60% (Andromeda suppression)
- [M13] Format diversity: ≥3 formats (image, video, carousel, collection)
- [M14] Hook diversity (video): ≥3 hook patterns
- [M15] Headline diversity: ≥3 structures
- [M16] Creative lifespan TOF ≤4 tuần (frequency >3 = warning)
- [M17] Creative lifespan BOF ≤7 tuần (frequency >8 = warning)
- [M18] Creative-as-targeting score: Concept+Format+Visual+Hook+Headline /10 — mục tiêu ≥8
- [M19] CTR decline >20% trong 14 ngày = flag
- [M20] Video creatives: ≤15 giây cho TOF, ≤30 giây cho BOF
- [M21] Carousel ads: ≥3 cards, value prop duy nhất mỗi card
- [M22] Đã test UGC-style content

### Cấu trúc Tài khoản (20%)
- [M23] Campaign objective khớp với funnel stage
- [M24] Advantage+ Sales / App Campaigns đã được đánh giá
- [M25] ASC/AAC: MAPI v25 migrated sang objective-default model
- [M26] Ad set consolidation: tránh learning phase hell
- [M27] Budget sufficiency: ≥5 lần CPA mỗi ad set
- [M28] Tối thiểu 3 ads mỗi ad set
- [M29] Dynamic Creative đã được test
- [M30] CBO (Campaign Budget Optimization) đã bật
- [M31] Campaign spending cap đã đặt
- [M32] Không edit khi đang ở learning phase
- [M33] Ad scheduling căn theo thời điểm conversion trong ngày
- [M34] Tối thiểu 1 tuần dữ liệu trước khi scaling
- [M-AND1] Entity-ID clustering: kiểm tra fingerprint creative visual/headline/body
- [M-AND2] Advantage+ Audience ON/OFF có chủ ý
- [M-AND3] iOS ATT opt-in rate được theo dõi
- [M-AND4] CAPI làm backup khi Pixel data drops

### Audience & Targeting (20%)
- [M35] Kiểm tra audience overlap: loại overlap >50%
- [M36] Exclusion targeting: exclude converters khỏi prospecting
- [M37] Custom Audiences: pixel events, customer list, engagement
- [M38] Lookalike source ≥1,000 (lý tưởng 5,000-50,000)
- [M39] Retargeting: frequency cap ≤3/day, dynamic product ads
- [M40] Advantage+ audience ON/OFF có chủ ý

---

## AUDIT LINKEDIN ADS (27 kiểm tra)

**Trọng số danh mục:** Technical 25% | Audience 25% | Creative 20% | Lead Gen 15% | Bidding 15%

### Cài đặt Technical (25%)
- [L01] Insight Tag đã cài đặt và firing
- [L02] Conversions API active
- [L03] Full funnel conversion events (lead → revenue)
- [L04] Revenue attribution tracking đã bật
- [L05] CRM integration (Salesforce/HubSpot)
- [L-CRM1] CRM revenue attribution active

### Audience Targeting (25%)
- [L06] Job titles cụ thể (không chỉ functions)
- [L07] Company size filtering khớp ICP
- [L08] Seniority level phù hợp
- [L09] Matched Audiences: retargeting + contact lists
- [L10] ABM company lists đã upload
- [L11] Audience expansion: OFF cho precision, ON cho scale
- [L12] Predictive audiences đã được test

### Creative & Lead Gen (35%)
- [L13] TLA ≥30% budget ($2.29-4.14 CPC so với $13.23 standard)
- [L14] Format diversity: ≥2 formats (Sponsored Content, Message Ads, Document Ads, Video)
- [L15] Video ads đã được test
- [L16] Refresh creative mỗi 4-6 tuần
- [L17] Document Ads đã được test (7% engagement rate)
- [L18] Lead Gen Form ≤5 fields (13% CVR)
- [L19] Lead Gen Form synced CRM real-time
- [L20] Campaign objective khớp funnel stage
- [L21] A/B testing active
- [L22] Message ad frequency ≤1 per 30-45 days
- [L-CRM2] EU messaging compliance

### Bidding & Budget (15%)
- [L23] Bắt đầu Manual CPC, Maximum Delivery = expensive
- [L24] Daily budget ≥$50 Sponsored Content
- [L25] CTR ≥0.44% Sponsored Content
- [L26] CPC $5-7 avg
- [L27] Lead-to-opportunity rate được theo dõi
- [L28] Attribution 30-day click / 7-day view

---

## AUDIT TIKTOK ADS (28 kiểm tra)

**Trọng số danh mục:** Creative 30% | Technical 25% | Bidding 20% | Cấu trúc 15% | Performance 10%

### Creative (30%)
- [T05] ≥6 creatives mỗi ad group
- [T06] Tất cả video 9:16 vertical 1080×1920
- [T07] Nội dung trông native (không corporate)
- [T08] Hook trong 1-2 giây đầu tiên
- [T09] Không creative nào active >7 ngày với declining CTR
- [T10] Spark Ads đã được test (~3% CTR)
- [T20] TikTok Shop integration (e-commerce)
- [T21] Video Shopping Ads đã được test
- [T22] Caption SEO với high-intent keywords
- [T23] Trending audio được dùng (sound-on)
- [T24] Custom CTA button
- [T25] Tuân thủ safe zone: X:40-940, Y:150-1470
- [T-SR1] Spark Ads đã scale beyond initial test

### Technical & Bidding (45%)
- [T01] TikTok Pixel đã cài đặt
- [T02] Events API + ttclid passback
- [T26] Events API Gateway đã được đánh giá
- [T27] Standard events đã cấu hình
- [T28] Advanced matching parameters
- [T11] Bid strategy: Lowest Cost vs Cost Cap
- [T12] Budget ≥50 lần target CPA mỗi ad group
- [T13] ≥50 conversions/7 ngày mỗi ad group
- [T-SR2] 3x Kill Rule (CPA >3 lần target = pause)

### Cấu trúc & Performance (25%)
- [T03] Tách riêng campaign prospecting vs retargeting
- [T04] Smart+ campaigns đã được test
- [T14] Search Ads Toggle đã bật
- [T15] Placement: TikTok, Pangle đã review
- [T16] Dayparting căn chỉnh
- [T-SR3] Ad group bid cap đã đặt
- [T17] CTR ≥1.0% in-feed
- [T18] CPA trong target
- [T19] Avg video watch time ≥6s

---

## AUDIT MICROSOFT ADS (24 kiểm tra)

**Trọng số danh mục:** Technical 25% | Syndication 20% | Cấu trúc 20% | Creative 20% | Cài đặt 15%

- [MS01] UET tag đã cài đặt
- [MS02] Enhanced conversions đã bật
- [MS03] Google Ads import đã validated
- [MS04] Search partner network đã review
- [MS05] Audience Network có chủ ý
- [MS06] Bid mục tiêu thấp hơn Google 20-35%
- [MS07] PMax LinkedIn targeting + Target New Customers
- [MS08] Campaign structure theo best practices
- [MS09] Budget 20-30% của Google
- [MS10] LinkedIn profile targeting (lợi thế B2B)
- [MS-SI1] Scheduled import conflict resolution
- [MS11] RSA ≥8 headlines, ≥3 descriptions
- [MS12] Multimedia Ads đã được test
- [MS13] Copy optimized cho Bing demographics
- [MS19] Đã dùng Action Extension
- [MS20] Filter Link Extension đã được test
- [MS21] Video extensions (9:16)
- [MS14] Copilot chat placement đã bật (73% CTR lift)
- [MS15] Native conversion goals (không imported)
- [MS16] CPC thấp hơn Google 20-40%
- [MS17] CVR tương đương Google
- [MS18] Impression share được theo dõi
- [MS-CM1] Consent Mode V2 verified
- [MS-CM2] CTV placement reviewed

---

## AUDIT APPLE ADS (ASA) (23 kiểm tra)

**Trọng số danh mục:** Cấu trúc 25% | Bid Health 20% | Creative 20% | Attribution 20% | Budget 15%

- [ASA01] Brand campaign: tên app của mình + misspellings
- [ASA02] Competitor campaign
- [ASA03] Category campaigns: high-intent generics
- [ASA04] Search Match campaigns active
- [ASA05] Search Match ISOLATED khỏi Exact Match
- [ASA06] Search Terms Report → promote winners
- [ASA07] Today Tab campaigns đã được test
- [ASA08] Product Page placements đã bật
- [ASA09] Manual CPT cho new accounts
- [ASA10] Maximize Conversions auto-bidder (≥5 lần CPA budget)
- [ASA11] Bids phân biệt theo match type
- [ASA12] Keyword-level CPT bids
- [ASA13] TTR ≥2.5% Search Results, ≥1.5% Search Tab
- [ASA14] Conversion rate 50-65% brand, 20-40% category
- [ASA15] Custom Product Pages đã tạo
- [ASA16] CPPs có unique screenshots + text
- [ASA17] Product Page Optimization A/B test
- [ASA18] AdAttributionKit registered
- [ASA19] View-through attribution: 24h post-impression
- [ASA20] Configurable attribution windows
- [ASA21] ATT opt-in rate được theo dõi
- [ASA22] CPA Goals với >100 installs/month mỗi campaign
- [ASA23] TAP coverage (Today/Search/Product Pages)

---

## AUDIT AMAZON ADS (20 kiểm tra)

**Trọng số danh mục:** Thu hoạch Search-Term 25% | ACOS/TACOS 20% | Cấu trúc 15% | Bidding 15% | Brands 10% | Display 10% | DSP 5%

- [AZ01] Auto campaigns per ASIN cluster
- [AZ02] Search Term Report reviewed last 60 days
- [AZ03] Converting terms Auto → Manual Exact
- [AZ04] Non-converting terms Exact Match negative
- [AZ05] Cadence khai thác hàng tuần (weekly mining cadence)
- [AZ06] Portfolio-level ACOS targets (tied to margin)
- [AZ07] TACOS trend được theo dõi (not single point)
- [AZ08] TACOS target ≤10% mature brands
- [AZ09] ACOS: brand <5%, category 15-25%, discovery 25-40%
- [AZ10] Portfolio theo funnel hoặc product line
- [AZ11] Auto + Manual Exact per ASIN
- [AZ12] Manual Keyword + Manual Product + Auto
- [AZ13] Mọi priority ASIN có ≥1 SP campaign
- [AZ14] Dynamic bidding (không Fixed)
- [AZ15] Top of Search placement bid cho terms high-converting
- [AZ16] Sponsored Brands HSA per storefront
- [AZ17] SB Video cho high-AOV products
- [AZ18] Sponsored Display audiences + contextual
- [AZ19] Amazon DSP programmatic awareness
- [AZ20] Brand Analytics được dùng (Search Terms, Repeat Purchase)

---

## ATTRIBUTION VÀ TRACKING LIÊN NỀN TẢNG

### Attribution iOS (AdAttributionKit)
- AAK registered with Apple Ads
- SKAN → AAK migration complete (post-Apr 10, 2025)
- 24h view-through window configured
- Configurable windows per campaign
- ATT opt-in ≥30%; nếu <30% = modeled reliance
- Privacy threshold: consolidate <1k installs/week campaigns

### Attribution Web
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

## BENCHMARK NGÀNH 2026

### Google Ads Search
| Ngành (Industry) | CPC | CTR | CVR |
|------------------|-----|-----|-----|
| E-commerce | $1.15 | 4.13% | 2.81% |
| B2B SaaS | $4.50-8.00 | 4.28% | 1.65% |
| Local Services | $7.85-15.00 | 5.50-6.37% | 7.33-15.0% |
| Legal | $8.58-9.21 | 5.20-5.97% | 4.60-5.09% |
| Finance | $3.46-3.77 | 4.65-8.33% | 2.55-3.50% |
| Healthcare | $40+ | 4.90% | 3.10% |
| Real Estate | $1.55-2.53 | 8.43% | 3.28% |

### Meta Ads
| Chỉ số (Metric) | Benchmark |
|-----------------|-----------|
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
| Chỉ số (Metric) | Benchmark |
|-----------------|-----------|
| CPC | $5-7 (median $3.94) |
| CTR | 0.44-0.65% |
| CPL | $60-150+ |
| Lead Gen Form CVR | 13% (3.25× landing pages) |
| TLA CPC | $2.29-4.14 (vs $13.23 standard) |

### TikTok & Microsoft
| Nền tảng (Platform) | Benchmark chính |
|---------------------|-----------------|
| TikTok CPM | ~$4.26 |
| TikTok Spark Ads CTR | ~3% (vs ~2% standard) |
| Microsoft CPC | 20-40% lower than Google |
| Microsoft Copilot | 73% CTR lift |

---

## CỔNG CHẤT LƯỢNG (Quy tắc cứng — không bao giờ vi phạm)

1. **Broad Match → Smart Bidding**: Không recommend Broad Match nếu không có Smart Bidding
2. **3x Kill Rule**: Flag CPA >3 lần target → pause
3. **Budget sufficiency**: Meta ≥5 lần CPA / ad set, TikTok ≥50 lần CPA / ad group
4. **Learning phase**: Không recommend edits khi campaign đang learning
5. **Compliance**: Luôn check Special Ad Categories
6. **Creative**: Không silent video trên TikTok (sound-on)
7. **Attribution default**: 7-day click / 1-day view (Meta), Data-Driven (Google)
8. **Andromeda diversity**: Flag nếu <10 creatives thực sự khác biệt (genuinely distinct)
9. **Privacy infrastructure gate**: Verify tracking stack trước optimization
10. **Không bao giờ Broad Match negatives**: Dùng Exact Match [keyword] hoặc Phrase Match "keyword"

---

## MẪU ĐẦU RA

### Tóm tắt Điều hành (Executive Summary)
```
Điểm Sức khỏe Quảng cáo: XX/100 (Xếp hạng: X)
Ngày Audit: YYYY-MM-DD

Điểm từng Nền tảng:
- Google Ads: XX (Xếp hạng X) — XX kiểm tra, X critical, X high
- Meta Ads: XX (Xếp hạng X) — XX kiểm tra, X critical, X high
- LinkedIn Ads: XX (Xếp hạng X) — XX kiểm tra, X critical, X high
- TikTok Ads: XX (Xếp hạng X) — XX kiểm tra, X critical, X high
- Microsoft Ads: XX (Xếp hạng X) — XX kiểm tra, X critical, X high
- Apple Ads: XX (Xếp hạng X) — XX kiểm tra, X critical, X high
- Amazon Ads: XX (Xếp hạng X) — XX kiểm tra, X critical, X high

Critical Issues hàng đầu:
1. [ID] — [Nền tảng] — [Vấn đề] — [Tác động] — [Hành động] — [ETA]

Quick Wins (fix <15 phút):
1. ...
```

### Phần từng Nền tảng
Mỗi nền tảng có điểm, xếp hạng, category breakdown (ĐẠT/CẢNH BÁO/KHÔNG ĐẠT), findings + remediation.

### Phân tích Liên Nền tảng
- Budget allocation (actual vs recommended)
- Tracking consistency (cùng events?)
- Creative consistency (messaging aligned?)
- Attribution overlap (double-counting?)

### Khuyến nghị Chiến lược
- Ưu tiên nền tảng theo loại hình kinh doanh
- Reallocation budget
- Cơ hội scaling
- Kill list (cần pause ngay)
