---
name: quy-tac-viet-website-ltch
description: "Quy tắc viết website cho thương hiệu mẫu Lớp Toán Cô Hạnh: trang chủ, trang khoá học, tuyển sinh; Markdown và checklist QA"
metadata:
  type: project
---

# Quy tắc viết website: Lớp Toán Cô Hạnh

**Phạm vi:** chỉ sản xuất nội dung trang chủ, trang khoá học và trang tuyển sinh; trả đúng một JSON với các khóa `home_vi`, `home_en`, `course_vi`, `course_en`. Không bọc code fence.

**Why:** website là nơi phụ huynh ra quyết định, cần chuyên nghiệp, tin cậy, trung thực, đúng cấu trúc để đăng không cần sửa tay.

**How to apply:** lấy fact từ input chuẩn hoá, dùng cấu trúc cố định và checklist, đối chiếu [[quy-chuan-bai-blog-ltch]] và [[giong-thuong-hieu-ltch]].

## 1. Nguồn sự thật và trung thực dữ liệu

- Rank, số lượng học viên, tỉ lệ hài lòng là dữ liệu tường minh từ input, không suy diễn.
- Không tính lại metric. Chỉ dùng trường đã chuẩn hoá. Không làm tròn khác input.
- Mỗi đoạn khoá học kết bằng đúng các chỉ số: số buổi, số học viên, tỉ lệ hài lòng. Cấm thay bằng giá trị tuyệt đối bịa.
- Tên riêng bị khoá: khoá học, chương trình, giáo viên, địa điểm. Nhắc tới là giữ đầy đủ, không gán nhầm lớp.

## 2. Trình bày chữ

- Chỉ dùng hyphen ASCII `-`, có khoảng trắng hai bên khi phân cách. Cấm en dash, em dash, minus sign.
- Giữ cách viết hoa chuẩn hoá từ input. Giữ nguyên acronym (TOEIC, IELTS, SAT).
- Trong JSON giữ Markdown bình thường, không thêm `\` trước `* ** # [ ]`.

## 3. Định dạng Markdown bắt buộc

- In đậm tên khoá học khi làm chủ ngữ: `**Luyện thi Toán 9**`.
- In đậm nhãn chỉ số: `**tỉ lệ hài lòng** 92%`. Không in đậm con số đơn lẻ.
- In đậm từ khoá loại hình: `**khoá học**, **cố vấn học tập**, **lộ trình cá nhân hoá**`.
- In nghiêng tên giáo viên, tên sách, tên bài toán mẫu khi nhắc lần đầu.

## 4. Giọng văn

- Ấm áp, khích lệ, chuyên môn đáng tin. Xoá từ quảng cáo sáo rỗng: "siêu tốc", "cam kết đậu", "bứt phá".
- Cấm hứa điểm số. Dùng "xây nền tảng", "tự tin làm bài", "tiến bộ đo lường được".
- Không so sánh hạ thấp trung tâm khác.

## 5. Cấu trúc chuẩn bản Việt

1. `home_vi`: H1 `# Lớp Toán Cô Hạnh - Đồng hành cùng con chinh phục Toán`. Intro in nghiêng ngắn. 3 block: Vì sao chọn chúng tôi / Lộ trình / Cảm nhận phụ huynh. CTA cuối.
2. `course_vi`: mỗi khoá học 1 đoạn: tên in đậm, số buổi, đối tượng, kết quả đo lường, CTA.
3. `home_en` / `course_en`: bản dịch tương ứng, giữ cấu trúc, thuật ngữ giáo dục chuẩn.

## 6. Kiểm tra cuối

- Đủ 4 khóa JSON, cấu trúc block đúng, placeholder link còn nguyên.
- Không còn gạch dài, Markdown đúng, in đậm/nghiêng đúng.
- Số liệu khớp input, tên khoá học đúng lớp, không hứa điểm số.
- Bản Việt và Anh tương ứng từng đoạn, CTA placeholder còn nguyên.
