---
name: cach-lam-viec-ky-thuat
description: "Cách người dùng mẫu muốn agent làm việc: tự chạy, kiểm chứng, giao hàng gọn [MẪU]"
metadata:
  type: feedback
---

# Cách làm việc kỹ thuật ưa thích [MẪU - thay bằng cách bạn làm việc]

> File này ghi cách vận hành cụ thể khi làm việc với agent. Khẩu vị giao tiếp chung nằm ở `preferences.md`.

## Tự chạy, ít hỏi

- Khi đã đề xuất được cách sửa, cứ sửa luôn, không dừng hỏi xác nhận từng bước nhỏ.
- Muốn tốc độ: nhận đủ tham số từ đầu để chạy một mạch không hỏi qua lại.
- Dùng chế độ tự động duyệt quyền cho quy trình dài để không bị ngắt giữa chừng.

## Kiểm chứng bằng thực nghiệm, không đoán

- Chỗ nào chưa chắc về hành vi công cụ hay dịch vụ ngoài thì gọi thật để kiểm tra, báo kết quả chính xác trước khi ghi thành quy tắc. Giả thuyết bị thực nghiệm bác thì sửa giả thuyết.
- Khi người dùng đã có quy trình chạy được cho đúng việc đó thì đọc và coi đó là chuẩn, không suy ra lại từ đầu.
- Sau khi sửa, tự test lại trên môi trường thật, không coi kiểm tra tĩnh là đủ.

## Giao hàng gọn và bền

- Việc xong thì dọn dẹp rồi commit và đẩy lên git, chỉ stage đúng tệp liên quan, chừa tệp do hệ thống quản lý và tệp tạm.
- Commit message tiếng Anh, dòng đầu ngắn dạng mệnh lệnh, thân liệt kê từng thay đổi.
- Script sửa cấu hình phải chạy lại được an toàn (chạy lại báo 0 thay đổi) và sao lưu bản gốc kèm thời gian trước khi ghi.
- Muốn gói bàn giao tự chứa mọi thứ trong thư mục dự án, không sửa cấu hình toàn máy; người dùng máy mới tự chạy script cài đặt.

## Viết và review

- Review thay đổi phải nêu đã đổi gì và kết luận rõ hợp lý hay không, kèm lỗi cụ thể và cách sửa cụ thể, không tóm tắt trung tính.
- Kỷ luật phạm vi: chỉ sửa đúng việc được giao, hoàn tác sửa ngoài phạm vi, giữ tính năng đang chạy ổn định.
- Mọi nút tùy chỉnh người dùng thấy được phải có tác dụng thật; logic tự động bên trong không được đè lên sửa tay của người dùng.
- Xuất ra phải khớp đúng những gì hiển thị trên màn hình; mọi cửa xuất phải dùng chung logic để cho kết quả giống nhau.
