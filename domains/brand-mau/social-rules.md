---
name: quy-tac-viet-social-ltch
description: "Quy tắc viết social cho thương hiệu mẫu Lớp Toán Cô Hạnh: Facebook VI/EN, TikTok, LinkedIn, trung thực dữ liệu và cấu trúc bắt buộc"
metadata:
  type: project
---

# Quy tắc viết social cho Lớp Toán Cô Hạnh

**Phạm vi:** sản xuất caption cho Facebook (VI/EN), TikTok và LinkedIn, gói trong một JSON có các khóa `facebook_vi`, `facebook_en`, `tiktok_script`, `linkedin_en`. Không dùng code fence.

**Why:** nội dung phải giữ đúng giọng ấm áp, khích lệ, chuyên môn đáng tin, đúng số liệu và tên khoá học, không hứa hẹn điểm số.

**How to apply:** mỗi khi viết social, đọc tệp này trước, lấy fact từ input tháng hiện tại, đối chiếu checklist QA ở cuối. Liên hệ [[giong-thuong-hieu-ltch]] và [[doi-tuong-muc-tieu-ltch]].

## 1. Nguồn sự thật duy nhất

- Thứ tự ưu tiên: input chuẩn hoá tháng hiện tại, rồi quy tắc trung thực dữ liệu, rồi quy tắc cấu trúc và văn phong, cuối cùng mới là tài liệu ví dụ để học nhịp câu.
- Ví dụ chỉ dạy form và nhịp điệu, không bao giờ lấy số liệu, tên khoá học, ngày, địa điểm từ ví dụ.
- Nếu input không có bối cảnh, đi thẳng vào thông điệp chính, không bịa câu filler sáo rỗng.

## 2. Trung thực dữ liệu, không được thương lượng

- Mọi con số là fact bất biến, chỉ được chuyển định dạng hiển thị: `13.50%` thành `13.5%`, `400.00K` thành `400K`. Cấm đổi giá trị, làm tròn sai, suy ra số mới.
- Tên khoá học, chương trình, sự kiện là tên riêng nguyên tử: giữ đầy đủ, không rút gọn hay diễn giải.
- Không gán nhầm hoạt động từ lớp này sang lớp khác. Kiểm tra quyền sở hữu theo đúng lớp trước khi chốt.
- Được viết lại cấu trúc câu, mô tả hoạt động, nhưng phải giữ nguyên fact: tên lớp, số lượng học viên, kết quả đo lường, ngày, địa điểm. Không thêm nguyên nhân hay diễn giải không có căn cứ.

## 3. Chuẩn hoá trình bày

- Mọi biến thể gạch ngang dài đều đổi thành hyphen ASCII `-`, có khoảng trắng quanh hyphen khi làm dấu phân cách, ví dụ `Luyện thi - Chinh phục đề tham khảo`. Giữ hyphen từ vựng như `check-in`, `live-stream`.
- Tiếng Việt dùng phân cách nghìn là `.` và thập phân là `,`. Tiếng Anh dùng phân cách nghìn là `,` và thập phân là `.`.
- Giữ nguyên tên riêng, acronym và cách viết như input.

## 4. Giọng văn

- Giữ tone ấm áp, khích lệ, chuyên môn đáng tin theo [[giong-thuong-hieu-ltch]]. Tránh từ phóng đại như "đảm bảo điểm 9", "cam kết đậu", "bứt phá", "siêu tốc".
- Ưu tiên từ trung tính: đồng hành, cùng con tiến bộ, xây nền tảng, thấu hiểu, kiên nhẫn.
- Không so sánh hạ thấp trung tâm khác.

## 5. Cấu trúc Facebook

- Nhãn `[Caption Facebook]`, bản tiếng Việt trước, dòng phân cách `---`, rồi bản tiếng Anh.
- Mẫu mở đầu: `[Emoji] [Tên khoá học] tháng này cùng [SỐ] bạn nhỏ chinh phục [CHỦ ĐỀ], tăng [SỐ]% sự tự tin làm bài toán khó.`
- Luôn giữ CTA placeholder: tiếng Việt `👉 Đăng ký tại: [link]`, tiếng Anh `👉 Sign up at: [link]`. Không bịa URL.

## 6. Phong cách TikTok

- `tiktok_script` là kịch bản nói, độ dài 30-45 giây, hook 3 giây đầu hỏi hoặc gợi tòi mở, ví dụ `"Con bạn sợ Toán chỉ vì một sai lầm này..."`.
- Dùng ngôn ngữ nói, câu ngắn, emoji vừa phải. Kết bằng CTA `👉 Link đăng ký ở tiểu sử`.

## 7. Phong cách LinkedIn

- Chỉ tiếng Anh, hướng tới phụ huynh và đối tác giáo dục. Mở bằng editorial lead ngắn, nêu kết quả đo lường được, tổng độ dài không quá 3000 ký tự.
- Giữ nguyên số liệu, tên khoá học, không dùng shorthand dashboard.

## 8. Định dạng và kiểm tra cuối

- Trong caption cấm Markdown thô (bold, heading, bullet, link) trừ hashtag. Hashtag cuối bài được phép.
- Checklist bắt buộc: số khớp input, không tính lại; tên khoá học đầy đủ và đúng lớp; không còn gạch dài; giữ capitalization chuẩn; đủ 4 khóa JSON; CTA placeholder còn nguyên; không còn cú pháp Markdown ngoài hashtag.
