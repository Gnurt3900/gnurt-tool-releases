# Gnurt Tool - Premium Utility & Arcade Station

**GNURT Tool** là một siêu ứng dụng tiện ích đa năng cao cấp chạy Native trên Windows. Ứng dụng kết hợp hoàn hảo giữa các công cụ hỗ trợ công việc hàng ngày, lập trình viên và **Trạm Trò Chơi Arcade** giải trí Neon bắt mắt, mang lại trải nghiệm mượt mà bám sát tần số quét màn hình cùng triết lý bảo mật dữ liệu tuyệt đối.

<img width="1457" height="898" alt="image" src="https://github.com/user-attachments/assets/6ce593df-c61c-4707-97ef-31f391f8c929" />

---

## 🔒 Cam Kết Bảo Mật An Toàn Tuyệt Đối (Local-First Philosophy)

*   **Không Cloud / Không Internet**: Ứng dụng hoạt động theo triết lý Local-First. Toàn bộ dữ liệu của bạn chỉ được lưu trữ trực tiếp trên chính ổ cứng máy tính cá nhân của bạn.
*   **Mã Hóa AES-256 Quân Sự**: Dữ liệu két sắt mật khẩu được bảo vệ bằng thuật toán mã hóa đối xứng AES-256 an toàn nhất hiện nay. Không một ai (kể cả nhà phát triển) có thể tiếp cận dữ liệu của bạn nếu không có mật khẩu chủ (Master Password).

---

## 🚀 Các Tính Năng Nổi Bật

### 1. Bộ Siêu Tiện Ích Cao Cấp (Premium Utilities)
*   🔑 **Password Vault**: Két sắt lưu trữ mật khẩu mã hóa AES-256 cục bộ, tích hợp trình sinh mật khẩu ngẫu nhiên bảo mật và tự động khóa két sắt khi cửa sổ thu nhỏ hoặc mất focus.
*   💻 **C# API Generator (CodeGen)**: Sinh tự động toàn bộ cấu hình API và logic dữ liệu (Controller, CQRS Command/Query, Validator, DTO, Repository, Service) đồng bộ 100% với cấu trúc dự án ASP.NET Core Web API bằng cách nhập tên bảng SQL hoặc nạp từ file Excel cấu hình.
*   🖥️ **Workspace Launcher**: Quản lý và khởi chạy đồng loạt các tệp tin, ứng dụng Windows và địa chỉ URL theo từng không gian làm việc tùy chỉnh chỉ với một cú click chuột.
*   📈 **Wealth Tracker**: Theo dõi biến động tài sản cá nhân, quản lý dòng tiền thu chi kèm biểu đồ thống kê trực quan.
*   🚀 **LAN File Transfer**: Chia sẻ tệp tin dung lượng lớn giữa các máy tính trong mạng nội bộ siêu tốc không cần internet.
*   🌳 **JSON Visualizer**: Trình phân tích, định dạng và hiển thị cấu trúc dữ liệu JSON dạng cây tương tác.
*   📊 **SQL Generator**: Biên dịch tự động bảng dữ liệu Excel thành mã truy vấn SQL Server / MySQL nhanh chóng.
*   🎨 **Color Studio**: Công cụ phối màu và kiểm tra độ tương phản UI chuẩn WCAG cho Designer/Developer.
*   📝 **Notes Studio**: Trình ghi chú nhanh Rich Text hỗ trợ định dạng văn bản nâng cao.
*   🌐 **Network Tools**: Công cụ đo độ trễ mạng (Ping) nội bộ và internet chuyên dụng.
*   ⏱️ **Pomodoro Timer**: Đồng hồ quản lý thời gian tập trung làm việc hiệu quả.
*   🔳 **QR Decorator**: Tạo và tùy biến phong cách, màu sắc, logo cho mã QR.

### 2. Trạm Trò Chơi Arcade (Arcade Station)
Tích hợp 9 tựa game kinh điển được khoác lên mình lớp áo đồ họa Neon hiện đại:
*   Dò mìn (Minesweeper), Cờ caro (Gomoku), Sudoku.
*   Cờ tướng, Cờ vua, Hải chiến (Battleship).
*   Bóng bàn Neon (Pong), Pac-Man Neon, Bomber Champion.

---

## 🛡️ Thiết Kế Mật Mã & Bảo Mật (Cryptography & Security Design)

GNURT Tool được thiết kế bảo mật theo mô hình **Zero-Knowledge** (Nhà phát triển hoàn toàn không có thông tin hay cách thức truy cập dữ liệu của bạn):

1.  **Két sắt mật khẩu (Password Vault)**:
    *   **Phái sinh khóa**: Sử dụng giải thuật **PBKDF2-HMAC-SHA256** chạy ngoài luồng UI để sinh khóa từ Master Password.
    *   **Mã hóa liên hợp**: Triển khai cơ chế mã hóa **AES-256-CBC** kết hợp ký xác thực **HMAC-SHA-256 (Encrypt-then-MAC)** chống tấn công sửa đổi Bit-flipping và Padding Oracle.
    *   **Chống Timing Attack**: So khớp chữ ký HMAC bằng thuật toán XOR thời gian hằng số (Constant-Time Comparison).
    *   **Dọn dẹp RAM vật lý**: Thực hiện ghi đè giá trị `0` (Zeroing-out) lên các khóa thô trong bộ nhớ RAM ngay khi kết thúc tác vụ mã hóa/giải mã.
2.  **Truyền tin LAN/WAN (E2EE Chat & File)**:
    *   **Khóa phiên động**: Thỏa thuận khóa đối xứng qua giao thức **Diffie-Hellman 2048-bit (Safe Prime MODP Group 14)** cho từng phiên kết nối.
    *   **Chống active MitM**: Gói tin bắt tay DH được mã hóa trước bằng mã phòng 10 ký tự làm khóa bí mật tạm thời để kháng kẻ đứng giữa chủ động trên MQTT Broker công cộng.
    *   **Kháng Replay Attack**: Gói tin được đính kèm nhãn thời gian `__ts__` kết hợp cache so khớp chữ ký HMAC nhận được trong vòng 120 giây.

---

## ⚡ Tối Ưu Hóa Hiệu Năng (Performance Engineering)

Mã nguồn được tối ưu hóa sâu để chạy Native siêu nhẹ, siêu mượt trên Windows Desktop:

1.  **Cách ly vẽ Canvas (`RepaintBoundary`)**: Tách biệt hoàn toàn phần Render vẽ game đồ họa động khỏi giao diện hệ thống tĩnh, duy trì tốc độ phản hồi 60fps - 120fps mà không hao phí tài nguyên CPU/GPU.
2.  **Không gây đơ giật UI (Non-blocking I/O)**: 100% các thao tác kiểm tra, đọc ghi tệp dữ liệu đều chạy bất đồng bộ.
3.  **Xử lý đa luồng (Isolates)**: Đẩy các tác vụ nặng (mật mã PBKDF2, nén/giải nén ZIP sao lưu, phân tích excel sinh mã SQL) sang các luồng phụ `Isolate` riêng biệt để bảo vệ luồng UI chính.
4.  **Triệt tiêu Garbage Collection (GC) overhead**: Gom nhóm và khai báo tất cả các biểu thức RegExp phức tạp thành hằng số tĩnh `static final` khởi tạo một lần duy nhất.

---

## 📥 Hướng Dẫn Tải & Cài Đặt (Download & Installation)

Ứng dụng hỗ trợ chạy Native mượt mà trên hệ điều hành **Windows 10 / 11** (64-bit).

1.  Truy cập vào mục [Releases](https://github.com/Gnurt3900/gnurt_tool/releases) của Repository này.
2.  Tải xuống bản phát hành mới nhất (`.rar`).
3.  **Giải nén** thư mục ra ổ đĩa của bạn (ví dụ: ổ `C:\` hoặc `D:\`).
4.  Nhấp đúp chuột vào tệp tin **`gnurt_tool.exe`** để mở ứng dụng và sử dụng ngay lập tức mà không cần cấu hình phức tạp.

---

## 📧 Hỗ Trợ & Liên Hệ
Nếu bạn gặp bất kỳ sự cố nào hoặc có đề xuất tính năng mới, vui lòng tạo một **Issue** trực tiếp tại repo này để được hỗ trợ nhanh nhất.
