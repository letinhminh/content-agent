# Bộ nhớ AI Agent mẫu cho người làm Content Marketing

Đây là một **khung sườn (template)** cho bộ nhớ dùng chung giữa bạn và AI agent (CommandCode, Claude Code, Codex, Cursor...). Học viên clone repo này về, sau đó cùng agent của mình điền thông tin cá nhân để biến nó thành "bộ não" riêng.

> Mọi file có thẻ `[MẪU]` là ví dụ minh hoạ. Thay bằng thông tin thật của bạn.

---

## QUY TẮC VÀNG cho AI agent (đọc trước khi sửa file nào)

Agent đừng vội sửa trực tiếp. Trước khi điền bất kỳ file nào, agent phải:

1. **LÊN KẾ HOẠCH** — Đọc cấu trúc thư mục, hiểu từng file làm gì, rồi đề xuất với người dùng *cách hoàn thiện folder này* (thiếu file nào, cần hỏi những gì). Chỉ bắt tay sửa khi người dùng đã đồng ý hướng đi.
2. **HỎI / ONBOARD** — Phỏng vấn người dùng để lấy thông tin thật (vai trò, khẩu vị phản hồi, bối cảnh marketing, công cụ đang dùng, quy tắc bảo mật). **Tuyệt đối không tự bịa** hồ sơ, sở thích hay số liệu của người dùng.
3. **GHI ĐÚNG KHẨU VỊ** — Mọi sửa đổi phải phản ánh đúng *cách người dùng muốn làm việc*, không áp đặt thói quen của agent hay của người khác. Khi chưa chắc, hỏi lại thay vì đoán.

Nguyên tắc: bộ nhớ này tồn tại để phục vụ người dùng, không phải để agent tự điền cho đầy.

---

## Cấu trúc thư mục

| File / thư mục | Mục đích |
|---|---|
| `AGENTS.md` | Hướng dẫn agent đọc bộ nhớ đầu mỗi phiên (không đổi trừ khi đổi quy trình). |
| `MEMORY.md` | Mục lục — mỗi file một dòng, để agent biết có gì. |
| `README.md` | File này — quy tắc vàng cho agent. |
| `TASKS.md` | Việc đang làm / chờ / để sau (mẫu). |
| `architecture.md` | Giải thích tại sao cấu trúc lại là thế này. |
| `user.md` | Hồ sơ người dùng `[MẪU]`. |
| `preferences.md` | Nguyên tắc phản hồi và làm việc ưa thích `[MẪU]`. |
| `cach-lam-viec-ky-thuat.md` | Cách làm việc cụ thể khi làm content / kỹ thuật `[MẪU]`. |
| `cong-viec-marketing.md` | Bối cảnh công việc marketing `[MẪU]`. |
| `domains/` | Tri thức theo lĩnh vực. `brand-mau/` là ví dụ brand guideline mẫu. |
| `skills/` | Các kỹ năng (skills) dùng chung mọi công cụ AI. |
| `state/` | Việc đang dở giữa các phiên, tồn tại ngắn ngày. |

---

## Gợi ý câu hỏi onboarding (agent nên hỏi)

Chia làm 5 nhóm, hỏi theo lượt, không dồn hết một lúc:

**1. Hồ sơ**
- Bạn làm vai trò gì (Content Creator, Social Media Manager, Freelancer...)?
- Bạn đang làm cho thương hiệu/channel nào? Quy mô thế nào?
- Bạn dùng máy gì, quen công cụ nào (macOS/Windows, Canva, Notion, các AI tool)?

**2. Khẩu vị phản hồi**
- Bạn thích nhận câu trả lời ngắn gọn hay chi tiết?
- Có điều gì agent nên tránh (từ ngữ, giọng điệu, đạo lý sáo rỗng)?
- Khi phân tích, bạn muốn chia thành phần hay tóm tắt một block?

**3. Bối cảnh marketing**
- Mục tiêu chính là gì (awareness, leads, bán hàng, xây cộng đồng)?
- Kênh nào đang tập trung (Facebook, TikTok, LinkedIn, Website, Email)?
- Phễu nội dung hiện tại của bạn đi như thế nào?

**4. Công cụ & quy trình**
- Bạn dùng AI tool nào? Có MCP/server nào cần kết nối không?
- Bạn muốn agent tự chạy hay hỏi xác nhận trước mỗi bước?
- Quy trình bàn giao (handoff) của bạn là gì?

**5. Bảo mật & ranh giới**
- Có thông tin nào cấm đưa lên production (tên thương hiệu thật của bên thứ ba, credential)?
- Có tài liệu nào chỉ được lưu local, không commit lên git?
- Ai có quyền đọc bộ nhớ này?

---

## Cách boot

Mỗi công cụ AI sẽ trỏ về file `AGENTS.md` của repo này làm điểm khởi động. Agent đọc `AGENTS.md` đầu mỗi phiên, theo đó đọc `MEMORY.md` rồi các file con liên quan. Bạn không cần làm gì thủ công.

---

## Cách đóng góp vào bộ nhớ

- Một chủ đề một file, tên file viết thường có gạch nối (`kebab-case`).
- Ghi bằng tiếng Việt có dấu, trình bày rõ ràng.
- Không ghi bí mật: mật khẩu, token, khóa API.
- `state/` chứa việc dở dang, tệp quá 7 ngày thì xoá.
- Khi hai bản sao của cùng tài liệu lệch nhau, gom về một nguồn chuẩn rồi mới sửa tiếp.
