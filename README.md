# GnurTool — Bộ tiện ích & Trạm trò chơi cho Windows

**GnurTool** là ứng dụng desktop cho **Windows 10/11 (64-bit)**, gom các công cụ dùng hằng ngày cho công việc, lập trình và một trạm trò chơi Arcade vào một chỗ. Dữ liệu lưu **cục bộ trên máy bạn**; app chỉ dùng mạng ở vài chức năng nêu rõ bên dưới.

<img width="1301" height="809" alt="image" src="https://github.com/user-attachments/assets/7e80de64-08c2-4ce0-be50-0b0bd3bd896b" />

---

## Tính năng

### Công cụ
- 📅 **Lịch âm dương** — lịch âm/dương song song, Can Chi, 24 tiết khí, ngày tốt, bát tự & phong thuỷ, văn khấn, sự kiện và đếm ngược.
- 🔑 **Quản lý mật khẩu** — két mã hoá cục bộ, trình sinh mật khẩu, tự khoá khi thu nhỏ hoặc không dùng, tự xoá clipboard sau 30 giây.
- 👤 **Hồ sơ cá nhân** — lưu thông tin, ảnh, tệp đính kèm theo danh mục; dữ liệu được mã hoá.
- 💬 **GnurtChat (LAN / WAN)** — nhắn tin và gửi tệp giữa các máy trong mạng nội bộ, hoặc qua Internet bằng phòng chat mã hoá đầu-cuối.
- ⚙️ **Bộ sinh API .NET** — kết nối SQL Server, đọc cấu trúc stored procedure và sinh mã C# (Controller, CQRS Query/Command, Handler, Validator, DTO, Repository) theo cấu trúc dự án ASP.NET Core Web API.
- 📊 **Tạo mã SQL tự động** — từ file Excel sinh lệnh `CREATE TABLE`, stored procedure (SQL Server) và model C#.
- 🌳 **Sơ đồ JSON/YAML** — định dạng, xem dạng cây, tìm kiếm, thống kê, chuyển đổi JSON ↔ YAML.
- 🖥️ **Khởi chạy không gian làm việc** — mở cùng lúc nhiều ứng dụng, tệp và trang web theo từng bộ.
- 📈 **Quản lý tài sản** — theo dõi dòng tiền, danh mục tài sản, biểu đồ; đồng bộ giá vàng/chứng khoán khi bạn bấm.
- 🎨 **Studio phối màu** — bánh xe màu, phối màu hài hoà, kiểm tra tương phản WCAG, trích màu từ ảnh.
- 📝 **Ghi chú** — soạn thảo Rich Text, thùng rác, xuất Markdown / văn bản thuần.
- 💻 **Thông tin & Dọn dẹp** — Xem cấu hình máy và dọn rác an toàn.
- 🌐 **Phân tích mạng** — Ping, quét cổng, tra cứu DNS, thông tin IP.
- ⏱️ **Pomodoro** — hẹn giờ tập trung kèm danh sách việc cần làm.
- 🔳 **Tạo mã QR** — tuỳ chỉnh màu, kiểu, logo; hỗ trợ URL, văn bản, Wi-Fi.

### Trạm trò chơi Arcade (10 game)
| Game | Chế độ |
|---|---|
| 💣 Dò mìn | Chơi đơn, đấu LAN |
| ❌ Cờ caro | Đấu máy (4 cấp độ), 2 người cùng máy, đấu LAN |
| 🔴 Cờ tướng | 2 người cùng máy, đấu LAN |
| ♟️ Cờ vua | 2 người cùng máy, đấu LAN |
| 🚢 Hải chiến | Đấu máy, đấu LAN |
| 🔢 Sudoku | 3 cấp độ, ghi chú bút chì |
| 🎯 2048 | Chơi đơn |
| 🧱 Xếp gạch | Chơi đơn |
| ⚪ Cờ lật (Othello) | Đấu máy, 2 người cùng máy |
| 🃏 Lật thẻ cặp đôi | Chơi đơn, 2 người cùng máy |

---

## Dữ liệu & bảo mật

- **Lưu cục bộ:** dữ liệu nằm trong thư mục `GnurTool_Data` do bạn chọn ở Cài đặt; bạn có thể tự sao lưu hoặc đồng bộ thư mục này.
- **Ghi tệp an toàn:** mọi lần lưu đều ghi ra tệp tạm rồi mới thay thế, giữ một bản `.bak`; tệp hỏng được đổi tên `.corrupt-<thời gian>` chứ không bị xoá.
- **Két mật khẩu:** khoá phái sinh từ mật khẩu chính bằng **Argon2id** (dự phòng PBKDF2-SHA256 600.000 vòng), mã hoá **AES-256-GCM**; sai mật khẩu nhiều lần sẽ tạm khoá.
- **Hồ sơ, Quản lý tài sản, cấu hình Bộ sinh API:** mã hoá AES-256-GCM bằng khoá riêng của máy, lưu trong kho bí mật của Windows.
- **Sao lưu:** bản có mật khẩu là tệp `.gtbackup` (Argon2id + AES-256-GCM), không ghi khoá bí mật ra đĩa ở dạng chưa mã hoá; bản không mật khẩu không chứa khoá bí mật.
- **LAN:** TLS 1.3 xác thực hai chiều, mỗi máy một chứng chỉ riêng; ghép cặp lần đầu bằng mã 6 số; chỉ máy đã ghép cặp mới gửi/nhận được.
- **WAN:** đi qua relay MQTT công cộng, chỉ kết nối TLS; nội dung mã hoá đầu-cuối (X25519 + AES-256-GCM), relay không đọc được nội dung. Relay vẫn thấy siêu dữ liệu kết nối (địa chỉ IP, thời điểm). Nên dùng mã phòng ngẫu nhiên (nút xúc xắc) thay vì mã dễ đoán.

### Khi nào app dùng mạng
- Chat **WAN** (khi bạn tạo hoặc vào phòng).
- **Đồng bộ giá** vàng/chứng khoán trong Quản lý tài sản (khi bạn bấm).
- **Kiểm tra cập nhật** tự động — mặc định **tắt**, bật trong Cài đặt.
- Công cụ **Phân tích mạng** khi bạn chạy Ping / DNS / tra IP.

Các chức năng còn lại chạy hoàn toàn offline.

---

## Tải & cài đặt

1. Vào mục [Releases](https://github.com/Gnurt3900/gnurt-tool-releases/releases).
2. Tải tệp `.zip` của bản mới nhất.
3. Giải nén vào một thư mục, ví dụ `D:\GnurTool`.
4. Chạy **`GnurTool.exe`**. Không cần cài đặt.

**Cập nhật:** đóng app, giải nén bản mới đè lên thư mục cũ (dữ liệu nằm ở `GnurTool_Data` nên không mất). Nên tạo bản sao lưu trong Cài đặt trước khi cập nhật.

---

## Hỗ trợ

Gặp lỗi hoặc muốn đề xuất tính năng, hãy tạo **Issue** tại [đây](https://github.com/Gnurt3900/gnurt-tool-releases/issues).
