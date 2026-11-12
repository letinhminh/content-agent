---
name: performance-report
description: "Xây dựng báo cáo hiệu quả marketing với chỉ số chính, phân tích xu hướng, điểm thắng/thua và gợi ý tối ưu ưu tiên. Dùng khi kết thúc chiến dịch, khi chuẩn bị tóm tắt kênh hàng tuần/tháng/quý cho stakeholder, hoặc khi cần biến dữ liệu thành tóm tắt điều hành kèm ưu tiên kỳ tới."
argument-hint: "<thời gian hoặc chiến dịch>"
---

# Báo cáo hiệu quả (Performance Report)

Tạo báo cáo hiệu quả marketing với chỉ số chính, phân tích xu hướng, insight và gợi ý tối ưu.

## Kích hoạt

Người dùng chạy `/performance-report` hoặc yêu cầu báo cáo marketing, phân tích hiệu quả, kết quả chiến dịch hoặc tóm tắt chỉ số.

## Đầu vào

1. **Loại báo cáo** — xác định loại báo cáo người dùng cần:
   - **Campaign report** — hiệu quả của một chiến dịch cụ thể
   - **Channel report** — hiệu quả qua một kênh cụ thể (email, social, paid, SEO...)
   - **Content performance** — hiệu quả của các nội dung cụ thể
   - **Overall marketing report** — tóm tắt cross-channel (hàng tuần, hàng tháng, hàng quý)
   - **Custom** — phạm vi do người dùng định nghĩa

2. **Thời gian báo cáo** — cửa sổ thời gian (tuần trước, tháng trước, quý trước, khoảng ngày tùy chọn)

3. **Nguồn dữ liệu**:
   - Nếu đã kết nối marketing analytics, khám phá tài khoản và nền tảng nào có sẵn, rồi lấy dữ liệu hiệu quả tự động
   - Nếu đã kết nối product analytics: lấy dữ liệu hiệu quả tự động
   - Nếu chưa kết nối: yêu cầu người dùng cung cấp số liệu. Nhắc: "Vui lòng dán hoặc chia sẻ dữ liệu hiệu quả của bạn. Tôi làm việc được với spreadsheet, dữ liệu CSV, ảnh chụp dashboard mô tả bằng chữ, hoặc chỉ cần các con số chính."

4. **Kỳ so sánh** (không bắt buộc) — kỳ trước hoặc so với cùng kỳ năm trước để có bối cảnh xu hướng

5. **Đối tượng đọc** (không bắt buộc) — ai sẽ đọc báo cáo (phong cách tóm tắt điều hành vs chi tiết phân tích)

## Cấu trúc báo cáo

### 1. Tóm tắt điều hành
- Tổng quan 2-3 câu về hiệu quả trong kỳ
- Chỉ số headline kèm hướng xu hướng (tăng/giảm/đi ngang so với kỳ trước)
- Một thắng lợi chính và một lĩnh vực cần quan tâm

### 2. Bảng chỉ số chính

Trình bày chỉ số cốt lõi trong bảng tóm tắt:

| Chỉ số | Kỳ này | Kỳ trước | Thay đổi | Mục tiêu | Trạng thái |
|--------|---------|---------|----------|----------|-----------|

Chỉ số trạng thái:
- Đúng hướng (đạt hoặc vượt mục tiêu)
- Có rủi ro (dưới mục tiêu nhưng trong mức chấp nhận được)
- Lệch hướng (dưới mục tiêu đáng kể)

#### Chỉ số theo loại báo cáo

**Campaign Report:**
- Impressions và reach
- Click-through rate (CTR)
- Tỷ lệ chuyển đổi
- Chi phí mỗi chuyển đổi (CPA)
- Return on ad spend (ROAS) hoặc ROI
- Tổng chuyển đổi/đăng ký/leads

**Channel Report (Email):**
- Email đã gửi, đã deliver, đã bounce
- Open rate
- Click-through rate
- Tỷ lệ hủy đăng ký
- Tỷ lệ chuyển đổi

**Channel Report (Social):**
- Impressions và reach
- Tỷ lệ tương tác (like, comment, share)
- Tăng trưởng followers
- Click-through rate
- Bài đăng hiệu quả nhất

**Channel Report (Paid):**
- Chi tiêu
- Impressions và clicks
- CTR
- CPC và CPM
- Chuyển đổi và CPA
- ROAS

**Channel Report (SEO/Organic):**
- Organic sessions
- Thứ hạng từ khóa (thay đổi)
- Số trang đã index
- Backlinks thu được
- Trang hiệu quả nhất

**Content Performance:**
- Pageview và lượt truy cập duy nhất
- Thời gian trên trang
- Bounce rate
- Số lần share social
- Chuyển đổi quy về content
- Nội dung hiệu quả nhất và kém nhất

**Overall Marketing Report:**
- Tổng leads tạo ra
- Marketing qualified leads (MQLs)
- Đóng góp vào pipeline
- Chi phí sở hữu khách hàng (CAC)
- Tóm tắt từng kênh

### 3. Phân tích xu hướng
- Xu hướng hiệu quả trong kỳ (theo tuần hoặc theo tháng)
- Điểm ngoặt đáng chú ý và nguyên nhân
- Mẫu mùa vụ hoặc chu kỳ quan sát được
- So với benchmark hoặc mục tiêu

### 4. Điều gì đã hiệu quả
- 3-5 thắng lợi hàng đầu kèm dữ liệu cụ thể
- Vì sao chúng hiệu quả (giả thuyết)
- Cách lặp lại hoặc mở rộng

### 5. Điều gì cần cải thiện
- 3-5 nội dung hiệu quả thấp nhất kèm dữ liệu cụ thể
- Giả thuyết hiệu quả thấp
- Cách sửa đề xuất

### 6. Insight và quan sát
- Mẫu trong dữ liệu không hiển nhiên từ các chỉ số đơn lẻ
- Insight hành vi đối tượng
- Chủ đề nội dung hoặc creative thu hút được
- Yếu tố bên ngoài có thể ảnh hưởng (mùa vụ, tin tức, động thái đối thủ)

### 7. Gợi ý
Với mỗi đề xuất:
- Việc cần làm
- Vì sao (gắn với insight cụ thể từ dữ liệu)
- Tác động kỳ vọng (cao, trung bình, thấp)
- Công sức triển khai (cao, trung bình, thấp)
- Mức ưu tiên (ngay, sprint tới, quý tới)

Ưu tiên đề xuất theo ma trận 2x2:

| | Công sức thấp | Công sức cao |
|---|---|---|
| **Tác động cao** | Làm trước | Lên kế hoạch cho sprint tới |
| **Tác động thấp** | Làm nếu còn thời gian | Giảm ưu tiên |

### 8. Trọng tâm kỳ tới
- 3 ưu tiên hàng đầu cho kỳ sắp tới
- Test hoặc thí nghiệm nên chạy
- Mục tiêu cho các chỉ số chính

## Định nghĩa chỉ số và benchmark

### Email Marketing

| Chỉ số | Định nghĩa | Khoảng benchmark | Cho biết điều gì |
|--------|-----------|----------------|-----------------|
| Delivery rate | Email delivered / email sent | 95-99% | Sức khỏe danh sách và uy tín gửi |
| Open rate | Lượt mở duy nhất / email delivered | 15-30% | Hiệu quả subject line và người gửi |
| Click-through rate (CTR) | Lượt click duy nhất / email delivered | 2-5% | Mức độ liên quan nội dung và CTA |
| Click-to-open rate (CTOR) | Lượt click duy nhất / lượt mở duy nhất | 10-20% | Chất lượng nội dung email (với người đã mở) |
| Tỷ lệ hủy đăng ký | Số hủy / email delivered | <0.5% | Mức độ phù hợp nội dung-đối tượng và tần suất |
| Bounce rate | Số bounce / email sent | <2% | Chất lượng danh sách và vệ sinh dữ liệu |
| Tỷ lệ chuyển đổi | Chuyển đổi / email delivered | 1-5% | Hiệu quả email end-to-end |
| Doanh thu mỗi email | Tổng doanh thu / email sent | Tùy ngành | Quy đổi doanh thu trực tiếp |
| Tốc độ tăng danh sách | (Người đăng ký mới - hủy) / tổng danh sách | 2-5% mỗi tháng | Sức khỏe xây dựng đối tượng |

### Social Media

| Chỉ số | Định nghĩa | Cho biết điều gì |
|--------|-----------|-----------------|
| Impressions | Số lần nội dung được hiển thị | Phân phối và độ phủ nội dung |
| Reach | Số người dùng duy nhất đã thấy nội dung | Độ rộng đối tượng |
| Tỷ lệ tương tác | (Like + comment + share) / reach | Mức độ cộng hưởng nội dung |
| Click-through rate | Lượt click link / impressions | Hiệu quả thúc đẩy traffic |
| Tốc độ tăng followers | Followers mới ròng / tổng followers mỗi kỳ | Xây dựng đối tượng |
| Tỷ lệ share/repost | Số share / reach | Tính viral và advocacy |
| Tỷ lệ xem video | Views / impressions | Hiệu quả hook video |
| Tỷ lệ xem hết video | Lượt xem hoàn thành / tổng views | Chất lượng và độ dài video |
| Share of voice social | Mentions của bạn / tổng mentions ngành | Hiển thị thương hiệu so với đối thủ |

### Paid Advertising (Search và Social)

| Chỉ số | Định nghĩa | Cho biết điều gì |
|--------|-----------|-----------------|
| Impressions | Số lần quảng cáo được hiển thị | Mức dùng ngân sách và độ rộng targeting |
| Click-through rate (CTR) | Clicks / impressions | Mức độ liên quan creative và targeting |
| Chi phí mỗi click (CPC) | Tổng chi tiêu / clicks | Hiệu quả chi phí traffic |
| Chi phí mỗi 1000 hiển thị (CPM) | Tổng chi tiêu / (impressions/1000) | Hiệu quả chi phí nhận diện |
| Tỷ lệ chuyển đổi | Chuyển đổi / clicks | Hiệu quả landing page và offer |
| Chi phí mỗi chuyển đổi (CPA) | Tổng chi tiêu / chuyển đổi | Hiệu quả chi phí toàn funnel |
| Return on ad spend (ROAS) | Doanh thu / chi tiêu quảng cáo | Hiệu quả tạo doanh thu |
| Quality Score (search) | Điểm liên quan của Google (1-10) | Mức phù hợp ad-keyword-landing page |
| Frequency | Số lần trung bình người dùng thấy quảng cáo | Rủi ro ad fatigue |
| Chuyển đổi view-through | Chuyển đổi từ người dùng đã thấy nhưng không click | Ảnh hưởng chiến dịch display/awareness |

### SEO / Organic Search

| Chỉ số | Định nghĩa | Cho biết điều gì |
|--------|-----------|-----------------|
| Organic sessions | Lượt truy cập từ tìm kiếm tự nhiên | Hiệu quả SEO và độ phủ nội dung |
| Thứ hạng từ khóa | Vị trí với các từ khóa mục tiêu | Hiển thị trên tìm kiếm |
| Organic CTR | Clicks / impressions trên kết quả tìm kiếm | Hiệu quả tiêu đề và meta description |
| Số trang đã index | Số trang trong chỉ mục tìm kiếm | Crawlability và sức khỏe website |
| Domain authority | Điểm thẩm quyền bên thứ ba | Sức mạnh tổng thể của website |
| Backlinks | Số website bên ngoài link tới | Thẩm quyền nội dung và SEO off-page |
| Tốc độ tải trang | Thời gian đến interactive | UX và yếu tố xếp hạng |
| Tỷ lệ chuyển đổi organic | Chuyển đổi organic / organic sessions | Chất lượng nội dung và ý định |
| Trang vào hàng đầu | Trang được truy cập nhiều nhất từ organic | Nội dung thúc đẩy traffic organic nhất |

### Content Marketing

| Chỉ số | Định nghĩa | Cho biết điều gì |
|--------|-----------|-----------------|
| Pageview | Tổng lượt xem các trang nội dung | Độ phủ và phân phối nội dung |
| Lượt truy cập duy nhất | Người dùng riêng biệt xem nội dung | Quy mô đối tượng |
| Thời gian trung bình trên trang | Thời gian dành trên các trang nội dung | Mức độ tương tác và độ sâu |
| Bounce rate | Session một trang / tổng sessions | Mức độ phù hợp nội dung-đối tượng và UX |
| Độ sâu cuộn | Người dùng cuộn xa đến đâu trên trang | Mức độ tương tác xuyên suốt nội dung |
| Share social | Số lần nội dung được share trên social | Mức độ cộng hưởng và viral |
| Backlinks thu được | Link bên ngoài tới nội dung | Thẩm quyền nội dung và giá trị SEO |
| Tạo leads | Leads quy về nội dung | Hiệu quả chuyển đổi của nội dung |
| ROI nội dung | Doanh thu quy về / chi phí sản xuất nội dung | Hiệu quả đầu tư nội dung tổng thể |

### Overall Marketing / Pipeline

| Chỉ số | Định nghĩa | Cho biết điều gì |
|--------|-----------|-----------------|
| Marketing qualified leads (MQLs) | Leads đạt tiêu chí chất lượng marketing | Hiệu quả top-of-funnel |
| Sales qualified leads (SQLs) | MQLs được sales chấp nhận | Chất lượng leads |
| Tỷ lệ chuyển đổi MQL-to-SQL | SQLs / MQLs | Mức độ căn chỉnh marketing-sales và chất lượng leads |
| Pipeline tạo ra | Giá trị dollar của cơ hội tạo ra | Tác động marketing lên doanh thu |
| Tốc độ pipeline | Deal di chuyển nhanh thế nào qua pipeline | Mức khẩn và chất lượng chiến dịch |
| Chi phí sở hữu khách hàng (CAC) | Tổng chi phí marketing + sales / khách hàng mới | Hiệu quả sở hữu khách hàng |
| Thời gian hoàn vốn CAC | Số tháng thu hồi CAC từ doanh thu | Sức khỏe unit economics |
| Doanh thu từ marketing | Doanh thu từ deal có nguồn gốc marketing | Đóng góp trực tiếp của marketing |
| Doanh thu có marketing ảnh hưởng | Doanh thu từ deal có marketing chạm tới | Tác động marketing rộng hơn |

## Template báo cáo theo nhịp

### Báo cáo marketing hàng tuần
Format quét nhanh cho standup của team:
- **3 chỉ số hàng đầu** kèm thay đổi theo tuần
- **Điều gì hiệu quả** tuần này (1-2 bullet kèm dữ liệu)
- **Điều gì cần chú ý** (1-2 bullet kèm dữ liệu)
- **Ưu tiên tuần này** (3-5 việc hành động)

### Báo cáo marketing hàng tháng
Báo cáo stakeholder chuẩn:
1. Tóm tắt điều hành (3-5 câu)
2. Bảng chỉ số chính (bảng kèm so với tháng trước và mục tiêu)
3. Tóm tắt hiệu quả từng kênh
4. Điểm nổi bật và kết quả chiến dịch
5. Điều gì hiệu quả và không hiệu quả (kèm giả thuyết)
6. Gợi ý và ưu tiên tháng tới
7. Ngân sách chi vs kế hoạch

### Review kinh doanh hàng quý (QBR)
Review chiến lược cho lãnh đạo:
1. Hiệu quả quý so với mục tiêu
2. Lộ trình year-to-date
3. Phân tích ROI từng kênh
4. Tóm tắt hiệu quả chiến dịch
5. Quan sát cạnh tranh và thị trường
6. Gợi ý chiến lược cho quý tới
7. Đề xuất ngân sách và phân bổ
8. Thí nghiệm chính và bài học rút ra

### Nguyên tắc thiết kế dashboard
- Ưu tiên chỉ số gắn với mục tiêu kinh doanh (không phải vanity metrics)
- Thể hiện xu hướng theo thời gian, không chỉ snapshot một thời điểm
- Thêm bối cảnh so sánh: kỳ trước, mục tiêu, benchmark
- Dùng mã màu nhất quán: xanh (đúng hướng), vàng (có rủi ro), đỏ (lệch hướng)
- Nhóm chỉ số theo giai đoạn funnel hoặc câu hỏi kinh doanh
- Giữ dashboard trong một trang/màn hình — chi tiết đưa vào appendix
- Tần suất cập nhật theo nhịp quyết định (real-time cho paid, hàng tuần cho content)

## Phân tích xu hướng và dự báo

### Xác định xu hướng
Khi phân tích dữ liệu hiệu quả, tìm:

1. **Xu hướng định hướng**: chỉ số tăng, giảm hay đi ngang nhất quán qua 4+ kỳ?
2. **Điểm ngoặt**: hiệu quả đổi hướng ở đâu và điều gì đã xảy ra lúc đó?
3. **Mùa vụ**: có mẫu dự đoán được theo ngày trong tuần, tháng hoặc quý?
4. **Bất thường**: spike hoặc drop một lần — nguyên nhân là gì và có lặp lại được không?
5. **Chỉ số dẫn đường (leading indicators)**: chỉ số nào thay đổi trước và dự báo kết quả tương lai?

### Quy trình phân tích xu hướng
1. Vẽ chỉ số theo thời gian (ít nhất 8-12 điểm dữ liệu mới có ý nghĩa)
2. Xác định hướng tổng thể (tăng, giảm, ngang, chu kỳ)
3. Tính tốc độ thay đổi (đang tăng tốc hay chậm lại?)
4. Phủ lên các sự kiện chính (chiến dịch ra mắt, thay đổi sản phẩm, sự kiện thị trường)
5. So với benchmark hoặc mục tiêu
6. Xác định tương quan với các chỉ số khác
7. Hình thành giả thuyết về nguyên nhân (và lên kế hoạch test để kiểm chứng)

### Phương pháp dự báo đơn giản
- **Dự báo tuyến tính**: kéo dài đường xu hướng hiện tại về phía trước (hữu ích với chỉ số ổn định)
- **Trung bình di động**: làm mượt nhiễu bằng cách lấy trung bình 3-6 kỳ gần nhất
- **So sánh cùng kỳ năm trước**: dùng mẫu năm ngoái làm baseline, điều chỉnh theo tốc độ tăng trưởng
- **Phép toán funnel**: dự báo đầu ra từ đầu vào (ví dụ: tạo X leads với tỷ lệ chuyển đổi Y sẽ được Z khách hàng)
- **Mô hình kịch bản**: tạo kịch bản tốt nhất, kỳ vọng và xấu nhất

### Lưu ý dự báo
- Dự báo ngắn hạn (1-3 tháng) tin cậy hơn dài hạn
- Dự báo dựa trên ít hơn 12 điểm dữ liệu nên gắn cờ độ tin cậy thấp
- Yếu tố bên ngoài (thị trường, đối thủ, kinh tế) có thể làm mất hiệu lực dự báo theo xu hướng
- Luôn trình bày dự báo dưới dạng khoảng, không phải số chính xác

## Cơ bản về mô hình attribution

### Attribution là gì?
Attribution xác định điểm chạm marketing nào được ghi công cho một chuyển đổi. Quan trọng vì người mua thường tương tác nhiều kênh trước khi chuyển đổi.

### Mô hình attribution phổ biến

| Mô hình | Cách hoạt động | Phù hợp nhất | Hạn chế |
|---------|---------------|--------------|---------|
| Last touch | 100% ghi công cho tương tác cuối trước chuyển đổi | Hiểu trigger cuối cùng | Bỏ qua awareness và nurture |
| First touch | 100% ghi công cho tương tác đầu tiên | Hiểu hiệu quả top-of-funnel | Bỏ qua nurture và yếu tố chuyển đổi |
| Linear | Chia đều cho mọi điểm chạm | Đại diện công bằng mọi kênh | Không phản ánh tác động tương đối |
| Time decay | Nhấn vào điểm chạm gần chuyển đổi hơn | Góc nhìn cân bằng nghiêng về gần đây | Có thể đánh giá thấp awareness |
| Position-based (U-shaped) | 40% đầu, 40% cuối, 20% chia cho các điểm giữa | Đánh giá cả discovery và conversion | Trọng số hơi tùy tiện |
| Data-driven | Thuật toán ghi công dựa trên mẫu chuyển đổi | Đại diện chính xác nhất | Cần lượng dữ liệu lớn |

### Hướng dẫn thực hành attribution
- Bắt đầu với last-touch attribution nếu chưa có mô hình — đơn giản và khả thi nhất
- So sánh first-touch và last-touch để hiểu kênh nào thúc đẩy awareness vs conversion
- Dùng position-based (U-shaped) làm điểm giữa hợp lý cho hầu hết công ty B2B
- Data-driven attribution cần lượng chuyển đổi lớn mới có ý nghĩa thống kê
- Không mô hình nào hoàn hảo — dùng attribution theo hướng, không phải sự thật tuyệt đối
- Multi-touch attribution tốt hơn single-touch, nhưng mô hình nào cũng hơn không có mô hình

### Bẫy attribution
- Đừng tối ưu một kênh đơn lẻ dựa trên single-touch attribution
- Kênh awareness (display, social, PR) sẽ luôn trông tệ trong mô hình last-touch
- Kênh conversion (search, retargeting) sẽ luôn trông tệ trong mô hình first-touch
- Attribution tự báo ("bạn biết chúng tôi từ đâu?") mang lại góc nhìn định tính hữu ích nhưng không tin cậy về mặt định lượng
- Khoảng trống tracking cross-device và cross-channel khiến dữ liệu attribution luôn không đầy đủ

## Framework gợi ý tối ưu

### Quy trình tối ưu
1. **Xác định**: chỉ số nào dưới hiệu quả so với mục tiêu hoặc benchmark?
2. **Chẩn đoán**: vấn đề nằm ở đâu trong funnel? (impressions, clicks, chuyển đổi, giữ chân)
3. **Giả thuyết**: nguyên nhân hiệu quả thấp là gì? (đối tượng, thông điệp, creative, offer, timing, kỹ thuật)
4. **Ưu tiên**: cách sửa nào tác động lớn nhất với công sức ít nhất?
5. **Thử nghiệm**: thiết kế thí nghiệm để kiểm chứng giả thuyết
6. **Đo lường**: thay đổi có cải thiện chỉ số không?
7. **Mở rộng hoặc lặp lại**: nhân rộng thắng lợi diện rộng; lặp lại với test chưa kết luận hoặc thất bại

### Đòn bẩy tối ưu theo giai đoạn funnel

| Giai đoạn funnel | Tín hiệu vấn đề | Đòn bẩy tối ưu |
|-------------|---------------|---------------------|
| Awareness | Impressions thấp, reach thấp | Ngân sách, targeting, channel mix, định dạng creative |
| Interest | CTR thấp, tương tác thấp | Creative quảng cáo, headline, hook nội dung, targeting đối tượng |
| Consideration | Bounce rate cao, thời gian trên trang thấp | Nội dung landing page, tốc độ trang, mức độ liên quan nội dung, UX |
| Conversion | Tỷ lệ chuyển đổi thấp | Offer, CTA, độ dài form, tín hiệu tin cậy, layout trang |
| Retention | Churn cao, tương tác lại thấp | Onboarding, email nurture, trải nghiệm sản phẩm, support |

### Thực hành tốt khi testing
- Test một biến mỗi lần để kết quả sạch
- Định nghĩa chỉ số thành công trước khi chạy test
- Tính kích thước mẫu cần thiết trước khi bắt đầu (đừng kết thúc test sớm)
- Chạy test tối thiểu một chu kỳ kinh doanh đầy đủ (thường một tuần với B2B)
- Ghi lại mọi test và kết quả, bất kể kết quả thế nào
- Chia sẻ bài học trong team — test thất bại là thông tin giá trị
- Test khẳng định status quo không phải thất bại — nó xây niềm tin vào cách làm hiện tại

### Nhịp tối ưu liên tục
- **Hàng ngày**: theo dõi chiến dịch paid về pacing ngân sách, bất thường, quảng cáo bị từ chối
- **Hàng tuần**: review hiệu quả từng kênh, tạm dừng nội dung yếu, mở rộng nội dung thắng
- **Hai tuần một lần**: làm mới creative quảng cáo và test biến thể mới
- **Hàng tháng**: review hiệu quả toàn diện, xác định cơ hội tối ưu mới, cập nhật dự báo
- **Hàng quý**: review chiến lược về channel mix, phân bổ ngân sách, chiến lược targeting

## Định dạng đầu ra

- Dùng bảng để trình bày dữ liệu
- In đậm số liệu chính và xu hướng
- Giữ tóm tắt điều hành ngắn gọn (phù hợp để forward cho lãnh đạo)
- Thêm mục "appendix chi tiết" cho dữ liệu phức tạp nếu người dùng cung cấp nhiều chỉ số

## Sau báo cáo

Hỏi: "Bạn muốn tôi:
- Tạo bản tóm tắt slide-ready từ kết quả này?
- Soạn thảo email stakeholder với điểm chính?
- Đi sâu vào một chỉ số hoặc kênh cụ thể?
- Thiết lập template báo cáo để tái dùng kỳ tới?"
