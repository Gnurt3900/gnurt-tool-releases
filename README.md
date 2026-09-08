# Gnurt Tool - Premium Utility & Arcade Station

**GNURT Tool** (hay **GnurTool**) là một siêu ứng dụng tiện ích đa năng cao cấp chạy Native trên Windows Desktop. Ứng dụng kết hợp hoàn hảo giữa các công cụ hỗ trợ công việc hàng ngày, lập trình viên và **Trạm Trò Chơi Arcade** E-Ink thanh lịch, mang lại trải nghiệm mượt mà bám sát tần số quét màn hình cùng triết lý bảo mật dữ liệu tuyệt đối (Local-First).

<img width="1241" height="806" alt="image" src="https://github.com/user-attachments/assets/e37f7110-2c21-46ea-a7f2-8e4815efbd86" />


---

## 🔒 Cam Kết Bảo Mật An Toàn Tuyệt Đối (Local-First Philosophy)

*   **Lưu trữ Cục bộ (Local-First)**: Toàn bộ dữ liệu của bạn (ghi chú, lịch & sự kiện, công việc Pomodoro, tài sản tích lũy...) đều được lưu trữ hoàn toàn dưới dạng tệp tin cục bộ có cấu trúc nằm trong một thư mục tập trung duy nhất (`GnurTool_Data`). Bạn có toàn quyền sao lưu hoặc đồng bộ qua Google Drive/OneDrive.
*   **Mã Hóa AES-256 Quân Sự**: Dữ liệu két sắt mật khẩu và cấu hình offline được bảo vệ bằng thuật toán mã hóa đối xứng **AES-256-CBC** kết hợp xác thực **HMAC-SHA-256**. Mật khẩu CSDL được cô lập bằng cơ chế **Windows DPAPI** (Credential Manager) an toàn tuyệt đối.

---

## 🚀 Các Tính Năng Nổi Bật

### 1. Bộ Siêu Tiện Ích Cao Cấp (Premium Utilities)
*   📅 **Lịch âm dương (Lunisolar Calendar)**: Tra cứu lịch Âm - Dương song hành, tự động tính toán Can Chi (Ngày/Tháng/Năm) và 24 Tiết khí thiên văn học, quản lý sự kiện kỷ niệm và đếm ngược thông minh.
*   🔑 **Password Vault**: Két sắt lưu trữ mật khẩu mã hóa AES-256 cục bộ, tích hợp trình sinh mật khẩu ngẫu nhiên bảo mật chuẩn Entropy cao và tự động khóa két sắt khi cửa sổ thu nhỏ hoặc mất focus.
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
Tích hợp **10 tựa game kinh điển** theo phong cách thiết kế **E-Ink Minimalist** thanh lịch, dịu mắt, tối ưu tài nguyên siêu nhẹ RAM (< 30MB) và CPU (0% khi người chơi đang suy nghĩ), tự động thích ứng mượt mà theo chủ đề Sáng / Tối:
*   💣 **Dò mìn (Minesweeper)**: Chơi đơn hoặc thi đấu tốc độ quét mìn qua mạng LAN.
*   ❌ **Cờ caro (Gomoku)**: Đấu trí với bot AI 4 cấp độ, 2 người tại chỗ hoặc đối kháng qua mạng LAN.
*   🔢 **Sudoku**: 4 cấp độ câu đố số học, chế độ bút chì nháp và kiểm tra logic offline.
*   🔴 **Cờ tướng (Xiangqi)**: Bàn cờ chữ Hán vector phẳng sắc nét, hỗ trợ AI và kết nối LAN thời gian thực.
*   ♟️ **Cờ vua (Chess)**: Quân cờ Unicode thanh lịch, kiểm soát lượt đi và chiếu tướng chuẩn quốc tế.
*   🚢 **Hải chiến (Battleship)**: Bày binh bố trận hạm đội, tích hợp bot AI săn tàu tự động và đấu mạng LAN.
*   🎯 **2048**: Trượt gộp số mượt mà bằng phím mũi tên bàn phím.
*   🧱 **Xếp gạch (Tetris)**: Game rơi khối gạch kinh điển, tính điểm combo và tăng dần tốc độ.
*   ⚪ **Cờ lật (Othello / Reversi)**: Thuật toán AI tính toán lật quân, hỗ trợ chơi đơn hoặc 2 người tại chỗ.
*   🃏 **Lật thẻ cặp đôi (Memory Cards)**: Trò chơi trí nhớ E-Ink tối giản, hỗ trợ chơi đơn và đối kháng 2 người tại chỗ.

---

## 🛡️ Thiết Kế Mật Mã & Bảo Mật (Cryptography & Security Design)

GNURT Tool được thiết kế bảo mật theo mô hình **Zero-Knowledge** (Nhà phát triển hoàn toàn không có quyền truy cập dữ liệu của bạn):

1.  **Két sắt mật khẩu (Password Vault)**:
    *   **Phái sinh khóa**: Sử dụng giải thuật **PBKDF2-HMAC-SHA256** chạy ngoài luồng UI (`Isolate`) để sinh khóa từ Master Password.
    *   **Mã hóa liên hợp**: Triển khai cơ chế mã hóa **AES-256-CBC** kết hợp ký xác thực **HMAC-SHA-256 (Encrypt-then-MAC)** chống tấn công sửa đổi Bit-flipping và Padding Oracle.
    *   **Chống Timing Attack**: So khớp chữ ký HMAC bằng thuật toán XOR thời gian hằng số (Constant-Time Comparison).
    *   **Dọn dẹp RAM vật lý**: Ghi đè giá trị `0` (Zeroing-out) lên các khóa thô trong bộ nhớ RAM ngay khi kết thúc tác vụ mã hóa/giải mã.
2.  **Truyền tin LAN/WAN (E2EE Chat & File)**:
    *   **Khóa phiên động**: Thỏa thuận khóa đối xứng qua giao thức **Diffie-Hellman 2048-bit (Safe Prime MODP Group 14)** cho từng phiên kết nối.
    *   **Chống active MitM**: Gói tin bắt tay DH được mã hóa trước bằng mã phòng 10 ký tự làm khóa bí mật tạm thời để kháng kẻ đứng giữa chủ động trên MQTT Broker công cộng.
    *   **Kháng Replay Attack**: Gói tin được đính kèm nhãn thời gian `__ts__` kết hợp cache so khớp chữ ký HMAC nhận được trong vòng 120 giây.
3.  **Bảo mật cấu hình CodeGen offline**:
    *   Các thông số kết nối CSDL được mã hóa AES-256-CBC trước khi lưu đĩa. Mật khẩu nhạy cảm được quản lý độc quyền qua **Windows Credential Manager (DPAPI)**.

---

## ⚡ Tối Ưu Hóa Hiệu Năng (Performance Engineering)

Mã nguồn được tối ưu hóa sâu để chạy Native siêu nhẹ, siêu mượt trên Windows Desktop:

1.  **Cách ly vẽ Canvas (`RepaintBoundary`)**: Tách biệt hoàn toàn phần Render vẽ game đồ họa động khỏi giao diện hệ thống tĩnh, duy trì tốc độ phản hồi 60fps - 120fps mà không hao phí tài nguyên CPU/GPU.
2.  **Không gây đơ giật UI (Non-blocking I/O)**: 100% các thao tác kiểm tra, đọc ghi tệp dữ liệu đều chạy bất đồng bộ.
3.  **Xử lý đa luồng (Isolates)**: Đẩy các tác vụ nặng (mật mã PBKDF2, nén/giải nén ZIP sao lưu, phân tích excel sinh mã SQL) sang các luồng phụ `Isolate` riêng biệt để bảo vệ luồng UI chính.
4.  **Triệt tiêu Garbage Collection (GC) overhead**: Gom nhóm và khai báo tất cả các biểu thức RegExp phức tạp thành hằng số tĩnh `static final` khởi tạo một lần duy nhất.

---

## 📥 Hướng Dẫn Tải & Cài Đặt (Download & Installation)

Hướng dẫn cài đặt và sử dụng trên **Windows 10 / 11** (64-bit):

1.  Truy cập vào mục [Releases](https://github.com/Gnurt3900/gnurt-tool-releases/releases) của Repository.
2.  Tải xuống bản phát hành mới nhất (`.zip`).
3.  **Giải nén** thư mục ra ổ đĩa của bạn (ví dụ: `C:\GnurTool` hoặc `D:\GnurTool`).
4.  Nhấp đúp chuột vào tệp tin **`GnurTool.exe`** để mở ứng dụng và sử dụng ngay lập tức mà không cần cài đặt thêm.

---

## 📧 Hỗ Trợ & Đóng Góp
Nếu bạn gặp bất kỳ sự cố nào hoặc có đề xuất tính năng mới, vui lòng tạo một **Issue** trực tiếp tại [Repository chính](https://github.com/Gnurt3900/gnurt-tool-releases/issues) để được hỗ trợ nhanh nhất.
