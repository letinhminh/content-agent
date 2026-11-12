---
name: architecture
description: "Kiến trúc: thư mục này là trung tâm bộ nhớ cho AI agent của bạn"
metadata:
  type: reference
---

# Kiến trúc: thư mục này là trung tâm bộ nhớ duy nhất

Repo này không chứa code ứng dụng. Nó là **kho tri thức và khẩu vị** để mọi AI agent của bạn (CommandCode, Claude Code, Codex, Cursor...) đọc mỗi khi làm việc, bất kể công cụ nào.

## Thư mục này giữ tri thức

Nguồn chuẩn duy nhất cho **tri thức**: hồ sơ người dùng, cách làm việc ưa thích, tri thức theo lĩnh vực, việc đang làm dở. Mọi agent đọc qua `AGENTS.md` ở đầu mỗi phiên.

## Thư mục này giữ kỹ năng

`skills/` là nơi đặt kỹ năng dùng chung mọi công cụ. Kỹ năng riêng từng dự án thì để trong repo của dự án đó (ví dụ `.commandcode/`, `.claude/`). Không commit tệp chứa token hay mật khẩu.

## Quy tắc phân biệt

- Thứ thực thi được dùng chung mọi dự án (kỹ năng, MCP, agent con) thì để ở `skills/`.
- Thứ gắn chặt một dự án thì để trong repo của dự án đó, memory này chỉ ghi bản đồ và bài học rút ra.
- Thứ để đọc và nhớ (sở thích, quyết định, bài học, ngữ cảnh) thì để ở các tệp memory trong repo này.
- Khi hai bản sao của cùng một tài liệu lệch nhau thì gom về một nguồn chuẩn rồi mới sửa tiếp.
