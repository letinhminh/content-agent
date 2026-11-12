---
name: draft-content
description: "Soạn thảo blog post, social media, email newsletter, landing page, thông cáo báo chí, case study với định dạng theo từng kênh và gợi ý SEO. Dùng khi viết bất kỳ nội dung marketing nào, khi cần lựa chọn headline hoặc subject line, hoặc khi chuyển thể thông điệp cho kênh, đối tượng, brand voice cụ thể."
argument-hint: "<loại nội dung và chủ đề>"
---

# Soạn thảo nội dung (Draft Content)

Tạo bản nháp nội dung marketing phù hợp với loại nội dung, đối tượng và brand voice cụ thể.

## Kích hoạt

Người dùng chạy `/draft-content` hoặc yêu cầu soạn thảo, viết, tạo nội dung marketing.

## Đầu vào

Thu thập các thông tin sau từ người dùng. Nếu chưa có, hỏi trước khi bắt đầu:

1. **Loại nội dung** — một trong các loại sau:
   - Blog post
   - Bài đăng mạng xã hội (ghi rõ nền tảng: LinkedIn, X/Twitter, Instagram, Facebook, TikTok)
   - Email newsletter
   - Copy landing page
   - Thông cáo báo chí
   - Case study

2. **Chủ đề** — chủ đề hoặc góc tiếp cận của nội dung

3. **Đối tượng mục tiêu** — nội dung dành cho ai (chức danh, ngành, cấp bậc, nỗi đau)

4. **Thông điệp chính** — 2-4 điểm chính cần truyền đạt

5. **Tone** — ví dụ: có thẩm quyền, gần gũi, truyền cảm hứng, kỹ thuật, hóm hỉnh (bỏ trống nếu đã có brand voice)

6. **Độ dài** — số từ mục tiêu hoặc giới hạn định dạng (ví dụ: "1000 từ", "280 ký tự", "3 đoạn văn")

## Brand voice

- Nếu người dùng đã cấu hình brand voice trong file cài đặt local, áp dụng tự động và thông báo cho người dùng.
- Nếu chưa cấu hình, hỏi: "Bạn có brand voice guidelines muốn tôi theo không? Nếu không, tôi sẽ dùng tone chuyên nghiệp trung tính."
- Áp dụng nhất quán tone đã chọn trong toàn bộ bản nháp.

## Tạo nội dung theo loại

### Blog post
- Headline hấp dẫn (đưa 2-3 lựa chọn)
- Mở bài có hook (câu hỏi, thống kê, phát biểu táo bạo hoặc câu chuyện)
- 3-5 mục có tiêu đề phụ mô tả rõ ràng
- Điểm hỗ trợ, ví dụ hoặc dữ liệu trong mỗi mục
- Kết bài kèm call to action rõ ràng
- Gợi ý SEO: từ khóa chính, đưa vào headline và đoạn đầu tiên, từ khóa liên quan trong tiêu đề phụ

### Bài đăng mạng xã hội
- Định dạng và độ dài phù hợp từng nền tảng
- Hook ngay dòng đầu tiên
- Gợi ý hashtag (3-5 hashtag phù hợp)
- Call to action hoặc gợi ý tương tác
- Emoji phù hợp với brand và nền tảng
- LinkedIn: giọng điệu chuyên nghiệp, ngắt dòng cho dễ đọc
- X/Twitter: ngắn gọn, súc tích, trong giới hạn ký tự
- Instagram: ngôn ngữ hình ảnh, kể chuyện, khối hashtag
- TikTok: kịch bản nói 30-45 giây, hook 3 giây đầu

### Email newsletter
- Subject line (đưa 2-3 lựa chọn, cân nhắc tỷ lệ mở)
- Preview text
- Lời chào
- Các mục thân có thứ bậc rõ ràng
- Nút call to action
- Lời ký
- Nhắc nhở link hủy đăng ký

### Copy landing page
- Headline và subheadline
- Copy hero section
- 3-4 giá trị nổi bật dạng bullet hoặc mục
- Chỗ dành cho social proof (gợi ý vị trí testimonial hoặc thống kê)
- Call to action chính và phụ
- Gợi ý mục FAQ
- SEO: gợi ý meta title và meta description

### Thông cáo báo chí
- Headline theo chuẩn thông cáo báo chí
- Dateline và địa điểm
- Đoạn lead (ai, cái gì, khi nào, ở đâu, tại sao)
- Quote hỗ trợ (hướng dẫn viết placeholder)
- Boilerplate công ty (placeholder)
- Liên hệ báo chí (placeholder)
- Định dạng thông cáo báo chí chuẩn

### Case study
- Tiêu đề nhấn vào kết quả
- Tổng quan khách hàng (ngành, quy mô, thách thức)
- Mục thách thức
- Mục giải pháp (đã triển khai cái gì)
- Mục kết quả kèm số liệu (hỏi người dùng để lấy dữ liệu)
- Placeholder quote khách hàng
- Call to action

## Gợi ý SEO (cho nội dung web)

Với blog post, landing page và các nội dung hướng web khác:
- Gợi ý từ khóa chính dựa trên chủ đề
- Gợi ý vị trí đặt từ khóa: headline, đoạn đầu tiên, tiêu đề phụ, meta description
- Gợi ý cơ hội liên kết nội bộ và bên ngoài
- Đề xuất meta description (dưới 160 ký tự)
- Ghi chú cơ hội alt text cho hình ảnh

## Đầu ra

Trình bày bản nháp với định dạng rõ ràng. Sau bản nháp, kèm thêm:
- Ghi chú ngắn về brand voice và tone đã áp dụng
- Gợi ý SEO (với nội dung web)
- Gợi ý bước tiếp theo (ví dụ: "Review cùng team", "Thêm quote khách hàng", "Ghép với hình ảnh")

Kết thúc bằng câu hỏi: "Bạn muốn tôi chỉnh sửa mục nào, thay đổi tone, hoặc tạo biến thể cho kênh khác không?"
