---
name: seo-audit
description: "Chạy SEO audit toàn diện — nghiên cứu từ khóa, phân tích on-page, khoảng trống nội dung, kiểm tra kỹ thuật và so sánh đối thủ. Dùng khi đánh giá sức khỏe SEO của website, khi tìm cơ hội từ khóa và khoảng trống nội dung mà đối thủ đang chiếm, hoặc khi cần kế hoạch hành động ưu tiên chia thành thắng nhanh và đầu tư chiến lược."
argument-hint: "<url hoặc chủ đề> [loại audit]"
---

# Audit SEO (SEO Audit)

Audit sức khỏe SEO của website, nghiên cứu cơ hội từ khóa, xác định khoảng trống nội dung và so sánh với đối thủ. Tạo kế hoạch hành động ưu tiên mà marketer có thể thi hành ngay.

## Kích hoạt

Người dùng chạy `/seo-audit` hoặc yêu cầu audit SEO, nghiên cứu từ khóa, phân tích khoảng trống nội dung, kiểm tra technical SEO hoặc so sánh SEO với đối thủ.

## Đầu vào

Thu thập các thông tin sau từ người dùng. Nếu chưa có, hỏi trước khi bắt đầu:

1. **URL hoặc domain** — website cần audit, hoặc chủ đề/từ khóa nếu chạy ở chế độ nghiên cứu từ khóa

2. **Loại audit** — một trong các loại sau:
   - **Full site audit** — review SEO end-to-end bao phủ tất cả các mục bên dưới
   - **Nghiên cứu từ khóa** — xác định cơ hội từ khóa cho chủ đề hoặc domain
   - **Phân tích khoảng trống nội dung** — tìm chủ đề đối thủ rank mà bạn không có
   - **Kiểm tra technical SEO** — crawlability, tốc độ, structured data, và vấn đề hạ tầng
   - **So sánh SEO với đối thủ** — benchmark SEO trực diện với đối thủ cụ thể

   Nếu không ghi, mặc định **full site audit**.

3. **Từ khóa hoặc chủ đề mục tiêu** (không bắt buộc) — từ khóa cụ thể người dùng đang nhắm tới hoặc muốn rank

4. **Đối thủ** (không bắt buộc) — domain hoặc công ty để so sánh. Nếu không có và loại audit cần dữ liệu đối thủ, dùng tìm kiếm web để xác định 2-3 đối thủ tiềm năng dựa trên domain và không gian từ khóa của người dùng.

## Quy trình

### 1. Nghiên cứu từ khóa

Nghiên cứu từ khóa liên quan tới domain, chủ đề hoặc từ khóa mục tiêu của người dùng.

**Nếu đã kết nối công cụ SEO:**
- Lấy dữ liệu từ khóa, lượng tìm kiếm, điểm độ khó, thứ hạng tự động
- Xác định từ khóa website đang rank và đang tăng/giảm ở đâu

**Nếu đã kết nối product analytics:**
- Đối chiếu từ khóa mục tiêu với dữ liệu organic traffic thật để kiểm chứng từ khóa nào thực sự mang lại lượt truy cập và chuyển đổi

**Nếu chưa kết nối công cụ:**
- Dùng tìm kiếm web để nghiên cứu bối cảnh từ khóa
- Ghi chú: "Để có dữ liệu lượng và độ khó chính xác hơn, kết nối công cụ SEO như Ahrefs hoặc Semrush qua MCP. Audit sẽ tự điền dữ liệu thứ hạng."

Với mỗi cơ hội từ khóa, đánh giá:
- **Từ khóa chính** — từ khóa ý định cao gắn trực tiếp với sản phẩm hoặc dịch vụ của người dùng
- **Từ khóa phụ** — từ khóa hỗ trợ và biến thể
- **Tín hiệu lượng tìm kiếm** — nhu cầu tương đối (cao, trung bình, thấp) dựa trên dữ liệu có sẵn
- **Độ khó từ khóa** — mức cạnh tranh của từ khóa (dễ, trung bình, khó)
- **Cơ hội long-tail** — cụm từ cụ thể, cạnh tranh thấp hơn, ý định rõ ràng
- **Từ khóa dạng câu hỏi** — truy vấn "how to", "what is", "why" giống kết quả People Also Ask
- **Phân loại ý định** — informational, navigational, commercial hoặc transactional

### 2. Audit SEO on-page

Với mỗi trang quan trọng (trang chủ, landing page hàng đầu, blog post gần đây), đánh giá:

- **Title tag** — có mặt, duy nhất, trong 50-60 ký tự, chứa từ khóa mục tiêu
- **Meta description** — có mặt, hấp dẫn, trong 150-160 ký tự, chứa call to action
- **Thẻ H1** — đúng một mỗi trang, chứa từ khóa chính
- **Cấu trúc H2/H3** — thứ bậc logic, dùng từ khóa phụ ở nơi tự nhiên
- **Dùng từ khóa** — từ khóa chính xuất hiện trong 100 từ đầu tiên, dùng tự nhiên trong toàn trang, không nhồi nhét
- **Internal linking** — các trang link tới nội dung liên quan, xác định trang mồ côi (orphan pages), anchor text mô tả rõ
- **Alt text hình ảnh** — mọi hình ảnh có alt mô tả, chứa từ khóa ở nơi phù hợp
- **Cấu trúc URL** — sạch, dễ đọc, chứa từ khóa, không có tham số thừa hoặc độ sâu quá lớn

### 3. Phân tích khoảng trống nội dung

Xác định những gì thiếu trong chiến lược nội dung của người dùng:

- **Độ phủ chủ đề của đối thủ** — chủ đề và từ khóa đối thủ rank mà website người dùng không bao phủ
- **Độ mới nội dung** — trang chưa cập nhật quá 12 tháng có thể đang mất thứ hạng
- **Nội dung mỏng (thin content)** — trang thiếu độ sâu để rank (dưới 300 từ với truy vấn informational, thiếu nội dung cốt lõi)
- **Thiếu loại nội dung** — định dạng đối thủ có mà người dùng không (hướng dẫn, trang so sánh, glossary, công cụ, template)
- **Khoảng trống funnel** — thiếu nội dung ở các giai đoạn cụ thể của hành trình mua hàng (awareness, consideration, decision)
- **Topic cluster** — cơ hội xây pillar page với nội dung hỗ trợ

### 4. Checklist Technical SEO

Đánh giá nền tảng kỹ thuật ảnh hưởng tới crawlability và thứ hạng:

- **Tốc độ trang** — xác định trang tải chậm và nguyên nhân có thể (hình ảnh lớn, script render-blocking, redirect quá nhiều)
- **Thân thiện mobile** — thiết kế responsive, tap target, cỡ chữ, cấu hình viewport
- **Structured data** — cơ hội dùng schema markup (FAQ, HowTo, Product, Article, Organization, Breadcrumb)
- **Crawlability** — cấu hình robots.txt, sự hiện diện và độ chính xác của XML sitemap, canonical tags, cách dùng noindex/nofollow
- **Link hỏng** — 404 nội bộ và bên ngoài, redirect chain
- **HTTPS** — kết nối an toàn, vấn đề mixed content
- **Core Web Vitals** — tín hiệu LCP, FID/INP, CLS dựa trên hành vi quan sát được
- **Indexation** — trang đáng lẽ được index nhưng chưa, rủi ro trùng lặp nội dung

### 5. So sánh SEO với đối thủ

Với mỗi đối thủ, so sánh:

- **Mức độ trùng từ khóa** — từ khóa cả hai website cùng rank, và mỗi bên rank cao hơn ở đâu
- **Khoảng trống từ khóa** — từ khóa đối thủ rank mà người dùng không
- **Tín hiệu domain authority** — sức mạnh website tương đối dựa trên hồ sơ backlink, referring domain, độ sâu nội dung
- **Độ sâu nội dung** — độ dài nội dung trung bình, độ phủ chủ đề, tần suất đăng
- **Quan sát hồ sơ backlink** — loại website link tới đối thủ, nội dung đáng link họ đã tạo
- **Quyền sở hữu SERP feature** — đối thủ nào xuất hiện trong featured snippet, People Also Ask, image pack hoặc knowledge panel
- **Lợi thế kỹ thuật** — khác biệt tốc độ website, trải nghiệm mobile, cách dùng structured data

## Đầu ra

### Tóm tắt điều hành

Mở đầu bằng tóm tắt 3-5 câu về sức khỏe SEO tổng thể. Nổi bật:
- Điểm mạnh lớn nhất của website
- 3 ưu tiên hàng đầu sẽ tạo tác động lớn nhất
- Đánh giá tổng thể: nền tảng vững chắc, cần cải thiện, hoặc có vấn đề nghiêm trọng

### Bảng cơ hội từ khóa

| Từ khóa | Độ khó ước tính | Điểm cơ hội | Thứ hạng hiện tại | Ý định | Loại nội dung đề xuất |
|---------|----------------|-------------|-------------------|--------|----------------------|

Điểm cơ hội: cao, trung bình hoặc thấp — dựa trên kết hợp nhu cầu tìm kiếm, độ khó và mức độ liên quan tới business của người dùng.

Gồm 15-25 cơ hội từ khóa, sắp xếp theo điểm cơ hội.

### Bảng vấn đề on-page

| Trang | Vấn đề | Mức độ | Cách sửa đề xuất |
|-------|--------|--------|------------------|

Mức độ:
- **Critical** — ảnh hưởng trực tiếp tới thứ hạng hoặc chặn indexation
- **High** — tác động đáng kể tới hiệu quả SEO
- **Medium** — vi phạm best practice, tác động vừa phải
- **Low** — cơ hội tối ưu nhỏ

### Gợi ý khoảng trống nội dung

Với mỗi khoảng trống nội dung xác định, đưa:
- **Chủ đề hoặc từ khóa** cần nhắm tới
- **Vì sao quan trọng** — nhu cầu tìm kiếm, độ phủ của đối thủ, giai đoạn funnel
- **Định dạng đề xuất** — blog post, landing page, hướng dẫn, trang so sánh...
- **Ưu tiên** — cao, trung bình hoặc thấp
- **Công sức ước tính** — thắng nhanh (1-2 giờ), vừa phải (nửa ngày), lớn (nhiều ngày)

### Checklist Technical SEO

| Hạng mục | Trạng thái | Chi tiết |
|----------|-----------|----------|

Trạng thái: Pass, Fail hoặc Warning.

### Tóm tắt so sánh đối thủ

| Chiều | Website bạn | Đối thủ A | Đối thủ B | Bên thắng |
|-------|-------------|-----------|-----------|-----------|
| (Gồm các hàng: số lượng từ khóa, độ sâu nội dung, tần suất đăng, tín hiệu backlink, điểm kỹ thuật, hiện diện SERP feature.)

### Kế hoạch hành động ưu tiên

Chia đề xuất thành hai nhóm:

**Thắng nhanh (làm trong tuần này):**
- Hành động dưới 2 giờ và có tác động ngay
- Ví dụ: sửa title tag, thêm meta description, sửa link hỏng, thêm alt text

**Đầu tư chiến lược (lên kế hoạch cho quý này):**
- Hành động cần nhiều công sức hơn nhưng thúc đẩy tăng trưởng dài hạn
- Ví dụ: xây topic cluster, tạo pillar page, ra mắt chiến dịch link building, overhaul cấu trúc website

Với mỗi mục hành động, gồm:
- Việc cần làm (cụ thể, rõ ràng)
- Tác động kỳ vọng (cao, trung bình, thấp)
- Ước tính công sức
- Dependencies (nếu có)

## Sau audit

Hỏi: "Bạn muốn tôi:
- Soạn thảo content brief cho các cơ hội từ khóa hàng đầu?
- Tạo title tag và meta description tối ưu cho các trang chính?
- Xây lịch content dựa trên phân tích khoảng trống?
- Đi sâu vào một mục cụ thể của audit?
- Chạy phân tích tương tự cho đối thủ hoặc domain khác?"
