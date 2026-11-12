---
name: email-sequence
description: "Thiết kế và soạn thảo chuỗi email nhiều bước với copy đầy đủ, timing, branching logic, điều kiện thoát và benchmark hiệu quả. Dùng khi xây dựng onboarding, lead nurture, re-engagement, win-back hoặc luồng ra mắt sản phẩm, khi cần drip campaign hoàn chỉnh kèm gợi ý A/B test, hoặc khi vẽ chuỗi end-to-end kèm sơ đồ flow."
argument-hint: "[loại chuỗi]"
---

# Chuỗi Email (Email Sequence)

Thiết kế và soạn thảo chuỗi email hoàn chỉnh với copy đầy đủ, timing, branching logic và benchmark hiệu quả cho bất kỳ use case vòng đời hoặc chiến dịch nào.

## Kích hoạt

Người dùng chạy `/email-sequence` hoặc yêu cầu tạo, thiết kế, xây dựng hoặc soạn thảo chuỗi email, drip campaign, nurture flow hoặc chuỗi onboarding.

## Đầu vào

Thu thập các thông tin sau từ người dùng. Nếu chưa có, hỏi trước khi bắt đầu:

1. **Loại chuỗi** — một trong các loại sau:
   - Onboarding
   - Lead nurture
   - Re-engagement
   - Ra mắt sản phẩm
   - Event follow-up
   - Upgrade/upsell
   - Win-back
   - Educational drip

2. **Mục tiêu** — chuỗi này cần đạt điều gì (ví dụ: kích hoạt người dùng mới, chuyển leads thành khách hàng, giảm churn, tăng tham dự sự kiện, upsell lên gói cao hơn)

3. **Đối tượng** — ai nhận chuỗi này, họ đang ở giai đoạn nào, và thông tin phân khúc liên quan (chức danh, ngành, trigger hành vi, vòng đời)

4. **Số lượng email** (không bắt buộc) — nếu không ghi, đề xuất số lượng theo loại chuỗi trong phần Template loại chuỗi bên dưới

5. **Ưu tiên timing/tần suất** (không bắt buộc) — khoảng cách mong muốn giữa các email (ví dụ: "mỗi 3 ngày", "hàng tuần", "dồn đầu tuần rồi giảm dần")

6. **Brand voice** — nếu đã cấu hình trong cài đặt local, áp dụng tự động và thông báo cho người dùng. Nếu chưa cấu hình, hỏi: "Bạn có brand voice guidelines muốn tôi theo không? Nếu không, tôi sẽ dùng tone chuyên nghiệp, gần gũi."

7. **Bối cảnh bổ sung** (không bắt buộc):
   - Offer, ưu đãi hoặc khuyến khích cụ thể cần đưa vào
   - CTA hoặc landing page cần link tới
   - Asset nội dung có sẵn (blog post, case study, video, hướng dẫn)
   - Tính năng sản phẩm cần nhấn mạnh
   - Điểm khác biệt với đối thủ cần tham chiếu

## Quy trình

### 1. Chiến lược chuỗi

Trước khi soạn thảo bất kỳ email nào, định nghĩa kiến trúc tổng thể của chuỗi:

- **Narrative arc** — chuỗi này kể câu chuyện gì xuyên suốt các email? Tiến triển cảm xúc và logic từ email đầu đến cuối là gì?
- **Ánh xạ hành trình** — mỗi email tương ứng với giai đoạn nào của hành trình người mua/người dùng (awareness, consideration, decision, activation, expansion)?
- **Logic leo thang** — cường độ, mức khẩn hoặc giá trị của mỗi email tăng dần thế nào?
- **Định nghĩa thành công** — hành động cụ thể nào báo hiệu chuỗi đã hoàn thành nhiệm vụ và người nhận nên thoát khỏi chuỗi?

### 2. Thiết kế từng email

Với mỗi email trong chuỗi, tạo:

#### Subject line
- Đưa 2-3 lựa chọn mỗi email
- Đa dạng cách tiếp cận: tò mò, nhấn lợi ích, khẩn cấp, cá nhân hóa, dạng câu hỏi
- Giữ dưới 50 ký tự khi có thể; ghi chú hành vi preview trên mobile

#### Preview text
- 40-90 ký tự bổ sung (không lặp lại) cho subject line
- Thêm bối cảnh hoặc gợi tò mò để tăng khả năng mở

#### Mục đích email
- Một câu giải thích vì sao email này tồn tại và nó thúc đẩy người nhận tới đâu

#### Body copy
- Bản nháp đầy đủ sẵn sàng dùng
- Thứ bậc rõ ràng: hook, thân, CTA
- Đoạn ngắn (tối đa 2-3 câu)
- Định dạng dễ quét với cụm từ chính in đậm ở nơi phù hợp
- Token cá nhân hóa ở nơi liên quan (ví dụ: tên, công ty, sản phẩm đã dùng)

#### CTA chính
- Text nút và đích đến
- Một CTA chính mỗi email (CTA phụ chỉ khi phù hợp với giai đoạn của chuỗi)

#### Timing
- Số ngày sau trigger event hoặc sau email trước
- Ghi chú nếu timing cần điều chỉnh theo tương tác (ví dụ: "gửi sớm hơn nếu đã mở nhưng chưa click")

#### Ghi chú phân khúc/điều kiện
- Ai nhận email này và ai bỏ qua
- Điều kiện hành vi hoặc thuộc tính (ví dụ: "chỉ gửi cho người dùng chưa hoàn thành thiết lập")

### 3. Logic chuỗi

Định nghĩa điều khiển luồng của chuỗi:

- **Điều kiện rẽ nhánh** — đường đi thay thế theo tương tác. Ví dụ:
  - "Nếu đã mở email 2 nhưng chưa click CTA, gửi email 2b (nhắc nhẹ hơn) thay vì email 3"
  - "Nếu đã click CTA trong email 1, bỏ email 2 và đi thẳng tới email 3"
- **Điều kiện thoát** — khi người nhận chuyển đổi (hoàn thành hành động mong muốn), loại họ khỏi chuỗi. Định nghĩa "chuyển đổi" là gì với chuỗi này.
- **Quy tắc vào lại** — ai có thể vào lại chuỗi? Trong điều kiện nào? (ví dụ: "nếu người dùng churn lại sau 90 ngày, vào lại chuỗi win-back")
- **Quy tắc chặn gửi (suppression)** — không gửi nếu người nhận đang trong chuỗi active khác, đã hủy đăng ký marketing, hoặc đã liên hệ support trong 48 giờ qua

### 4. Benchmark hiệu quả

Đưa benchmark kỳ vọng theo loại chuỗi để người dùng đặt mục tiêu:

| Chỉ số | Onboarding | Lead Nurture | Re-engagement | Win-back |
|--------|-----------|--------------|---------------|----------|
| Open rate | 50-70% | 20-30% | 15-25% | 15-20% |
| Click-through rate | 10-20% | 3-7% | 2-5% | 2-4% |
| Tỷ lệ chuyển đổi | 15-30% | 2-5% | 3-8% | 1-3% |
| Tỷ lệ hủy đăng ký | <0.5% | <0.5% | 1-2% | 1-3% |

Điều chỉnh benchmark theo ngành và đối tượng nếu người dùng đã cung cấp bối cảnh.

## Template theo loại chuỗi

Dùng các template này làm framework bắt đầu. Điều chỉnh độ dài và nội dung theo mục tiêu và đối tượng của người dùng.

**Onboarding (5-7 email trong 14-21 ngày):**
Chào mừng và đặt kỳ vọng -- Thắng nhanh để thấy giá trị -- Giới thiệu kỹ tính năng cốt lõi -- Tính năng nâng cao hoặc tích hợp -- Social proof và cộng đồng -- Hỏi thăm và xin feedback -- Nhắc nâng cấp hoặc bước tiếp theo

**Lead Nurture (4-6 email trong 3-4 tuần):**
Nội dung giáo dục đặt giá trị lên đầu -- Xác định nỗi đau -- Định vị giải pháp kèm bằng chứng -- Social proof và kết quả -- CTA nhẹ (dùng thử, demo, tài nguyên) -- CTA trực tiếp (mua, đặt lịch, đăng ký)

**Re-engagement (3-4 email trong 10-14 ngày):**
"Nhớ bạn" kèm lý do hấp dẫn để quay lại -- Nhắc giá trị họ đang bỏ lỡ -- Ưu đãi hoặc offer độc quyền -- Cơ hội cuối với deadline rõ ràng

**Win-back (3-5 email trong 30 ngày):**
Hỏi thăm thân thiện xem điều gì đã sai -- Có gì mới kể từ khi họ rời đi -- Offer đặc biệt hoặc khuyến khích quay lại -- Xin feedback (kể cả nếu họ không quay lại) -- Lời tạm biệt cuối với cánh cửa vẫn mở

**Ra mắt sản phẩm (4-6 email trong 2-3 tuần):**
Teaser hoặc thông báo trước -- Thông báo ra mắt kèm chi tiết đầy đủ -- Spotlight tính năng hoặc use case -- Social proof và kết quả ban đầu -- Offer giới hạn thời gian hoặc bonus -- Cơ hội cuối hoặc nhắc nhở

**Event follow-up (3-4 email trong 7-10 ngày):**
Cảm ơn kèm điểm chính hoặc bản ghi -- Tổng hợp tài nguyên từ sự kiện -- Offer liên quan hoặc bước tiếp theo -- Khảo sát feedback

**Upgrade/Upsell (3-5 email trong 2-3 tuần):**
Ăn mừng cột mốc sử dụng hoặc thành công -- Khoảng trống tính năng hoặc giới hạn họ đang chạm tới -- Lợi ích nâng cấp kèm bằng chứng -- Ưu đãi giới hạn thời gian -- So sánh trực tiếp các gói

**Educational drip (5-8 email trong 4-6 tuần):**
Giới thiệu và điều họ sẽ học -- Bài 1: khái niệm nền tảng -- Bài 2: khái niệm trung cấp -- Bài 3: khái niệm nâng cao -- Ứng dụng thực hành hoặc bài tập -- Tổng hợp tài nguyên -- Tốt nghiệp và bước tiếp theo

## Tích hợp công cụ

### Nếu đã kết nối email marketing (ví dụ: Klaviyo, Mailchimp, Customer.io)
- Tham chiếu cách thiết lập chuỗi dạng flow hoặc automation trên nền tảng
- Ghi chú tính năng đặc thù cần dùng (ví dụ: smart send time, conditional splits, A/B testing)
- Ánh xạ logic rẽ nhánh theo khái niệm flow builder trực quan của nền tảng

### Nếu đã kết nối marketing automation hoặc CRM (ví dụ: HubSpot, Marketo)
- Tham chiếu dữ liệu lead scoring để định hình phân khúc và điều kiện thoát
- Dùng dữ liệu vòng đời (lifecycle stage) để điều chỉnh thông điệp theo từng phân khúc
- Ghi chú cách thiết lập enrollment trigger dựa trên thuộc tính CRM hoặc thành viên danh sách

### Nếu chưa kết nối công cụ nào
- Giao tất cả nội dung email ở dạng sẵn sàng copy-paste
- Kèm checklist thiết lập mà người dùng có thể làm theo trên bất kỳ nền tảng email nào:
  1. Tạo automation hoặc flow
  2. Thiết lập enrollment trigger
  3. Thêm từng email với độ trễ quy định
  4. Cấu hình branching và điều kiện thoát
  5. Thiết lập theo dõi cho các chỉ số được đề xuất

## Đầu ra

Trình bày chuỗi hoàn chỉnh với các mục sau:

### Bảng tổng quan chuỗi

| # | Subject Line | Mục đích | Timing | CTA chính | Điều kiện |
|---|-------------|----------|--------|----------|-----------|

### Bản nháp đầy đủ từng email
Mỗi email gồm subject line options, preview text, mục đích, body copy, CTA, timing và ghi chú phân khúc.

### Sơ đồ luồng chuỗi
Sơ đồ dạng text thể hiện luồng email, đường rẽ nhánh và điểm thoát. Dùng format rõ ràng như:

```
[Trigger] --> Email 1 (Ngày 0)
                |
          Đã mở? --Có--> Email 2 (Ngày 3)
                |              |
                Chưa      Đã click CTA? --Có--> [THOÁT: Đã chuyển đổi]
                |              |
                v              Chưa
          Email 1b (Ngày 2)    |
                |              v
                +--------> Email 3 (Ngày 7)
                               |
                               v
                          Email 4 (Ngày 10)
                               |
                          [THOÁT: Hoàn thành chuỗi]
```

### Ghi chú logic rẽ nhánh
Tóm tắt tất cả điều kiện, điểm thoát và quy tắc chặn gửi trong danh sách tham khảo.

### Gợi ý A/B test
- 2-3 A/B test đề xuất (subject line, text CTA, thời gian gửi, độ dài email)
- Cái gì test, cách chia, và cách đo người thắng

### Chỉ số cần theo dõi
- Chỉ số chuyển đổi chính của chuỗi
- Chỉ số từng email: open rate, CTR, tỷ lệ hủy đăng ký
- Chỉ số cấp chuỗi: tỷ lệ chuyển đổi tổng, thời gian chuyển đổi, điểm rớt
- Tần suất review đề xuất (ví dụ: "Review hiệu quả hàng tuần trong tháng đầu, sau đó hàng tháng")

## Sau khi có chuỗi

Hỏi: "Bạn muốn tôi:
- Sửa copy hoặc tone cho email cụ thể nào?
- Thêm đường rẽ nhánh cho kịch bản cụ thể?
- Tạo biến thể chuỗi này cho phân khúc đối tượng khác?
- Soạn thảo các biến thể A/B test cho subject line?
- Xây một chuỗi đồng hành (ví dụ: follow-up sau mua hàng từ lead nurture này)?"
