---
name: quy-chuan-bai-blog-ltch
description: "Quy chuẩn bài blog cho thương hiệu mẫu Lớp Toán Cô Hạnh: định dạng, văn phong, dịch thuật và checklist QA"
metadata:
  type: project
---

# Quy chuẩn bài blog: Lớp Toán Cô Hạnh

**Phạm vi:** biên soạn bài blog giáo dục dài 800-1200 từ, trả đúng một JSON với các khóa `title`, `meta_description`, `body_vi`, `body_en`. Không bọc code fence.

**Why:** bài blog là nguồn tìm kiếm (SEO) và xây uy tín, cần đúng cấu trúc, văn phong ấm áp, số liệu trung thực.

**How to apply:** khi viết blog, đọc tệp này cùng [[quy-tac-viet-social-ltch]] và [[giong-thuong-hieu-ltch]], lấy fact từ input, rà checklist cuối.

## 1. Định dạng văn bản

- Cấm tuyệt đối mọi gạch ngang dài (em dash, en dash...): chuyển về hyphen ngắn `-` có khoảng trắng hai bên khi làm dấu phân cách.
- Dùng Markdown chuẩn: `##` cho tiêu đề phụ, `-` cho bullet, `**` để in đậm từ khoá.
- Đoạn văn tối đa 4-5 câu, xuống dòng rõ ràng cho dễ đọc trên mobile.

## 2. In đậm, in nghiêng

- Bắt buộc in đậm tên khoá học, tên chương trình khi làm chủ ngữ.
- Bắt buộc in đậm chỉ số kết quả: "tăng 23% sự tự tin", "85% phụ huynh hài lòng".
- In nghiêng tên bài toán mẫu, tên sách/thiết bị cụ thể khi nhắc lần đầu.

## 3. Số liệu và chuẩn hóa chữ

- Cắt số 0 thừa thập phân: `9.00%` thành `9%`, `563.10K` thành `563.1K`.
- Tiếng Việt: nghìn phân cách `.`, thập phân `,`. Tiếng Anh ngược lại.
- Tên riêng từ ALL CAPS chuyển Title Case, giữ acronym (TOEIC, IELTS, SAT).

## 4. Từ cấm và văn phong

- Không dùng lời hứa điểm số: "đảm bảo 9 điểm", "cam kết đậu". Dùng "xây nền tảng vững", "hiểu bản chất để tự tin làm bài".
- Không so sánh hạ thấp đối thủ. Dùng trung lập: "cùng đồng hành", "phù hợp với lộ trình của con".
- Giọng ấm áp, khích lệ, có ví dụ đời thường (chia bánh, đếm tiền lẻ...).

## 5. Cấu trúc bài blog

- `title`: 1 câu hỏi hoặc hứa hẹn giá trị, dưới 60 ký tự, có từ khoá.
- `meta_description`: tóm tắt 150-160 ký tự, chứa từ khoá chính.
- `body_vi`: mở bài nêu nỗi đau (sợ Toán) → thân bài 3 phần (nguyên nhân, cách tiếp cận, ví dụ) → kết bài CTA.
- `body_en`: bản dịch tương đương, giữ cấu trúc đoạn, thuật ngữ giáo dục chuẩn.

## 6. Checklist trước khi xuất

- Đủ 4 khóa JSON, title < 60 ký tự, meta 150-160 ký tự.
- Không còn gạch dài, Markdown đúng chuẩn, in đậm/nghiêng đúng quy tắc.
- Số liệu khớp input, tên khoá học đúng, không hứa điểm số.
- body_vi và body_en tương ứng từng đoạn, CTA placeholder còn nguyên.
