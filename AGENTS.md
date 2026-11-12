# Khởi động agent, đọc đầu mỗi phiên làm việc

Đây là bộ nhớ dùng chung giữa người dùng và AI agent (CommandCode, Claude Code, Codex, Cursor...). Mọi agent đều có thể đọc được vì chỉ là Markdown cộng với quy ước `AGENTS.md`.

## Đầu mỗi phiên làm việc

1. Đọc `MEMORY.md` (mục lục, mỗi tệp một dòng) trong thư mục này.
2. Đọc `user.md` và `preferences.md` để biết người dùng là ai và muốn làm việc theo cách nào.
3. Đọc `TASKS.md` để biết việc đang mở, việc đang chờ ai và việc để sau.
4. Nếu công việc thuộc lĩnh vực nào trong `domains/`, đọc `domains/<tên>/_index.md` trước (chứa đường dẫn và bản đồ nội bộ), rồi đọc tiếp các tệp con cần thiết. Chỉ đọc tệp liên quan, không đọc hết.

## Khi học được điều mới

Ghi ngay vào tệp tương ứng (sở thích của người dùng, quyết định, bài học khi sửa lỗi, việc đang làm dở), rồi cập nhật `MEMORY.md` (mỗi tệp một dòng). Quy tắc:

- Một chủ đề một tệp, tên tệp viết thường có gạch nối. Không dồn nhiều chủ đề vào một tệp lớn.
- Mọi nội dung ghi vào bộ nhớ phải viết bằng tiếng Việt có đầy đủ dấu, trình bày đầy đủ và rõ ràng.
- Không bao giờ ghi bí mật: mật khẩu, token, khóa API.
- `state/` chứa việc đang làm dở, tồn tại ngắn ngày: tệp quá 7 ngày thì xóa.
- Trước khi đẩy lên git: chạy `git pull --rebase`. Nếu xung đột thì giữ bản trên remote, ghi bản local vào `state/xung-dot-<năm-tháng-ngày>.md`.

## Cách các công cụ đọc được tệp này

Mỗi công cụ trỏ về đây bằng một tệp dẫn ngắn đặt ở vị trí riêng của nó, nên giữ tệp này mỏng. Tài liệu dài để ở các tệp con.
