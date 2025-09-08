# Khai Thác Lỗ Hổng Cross-Site Scripting

> VulnLab: Cross-Site Scripting (XSS)

> Thực Hiện: Mai Anh

> Cập Nhật Lần Cuối: 8/9/2025


- các kiểu lỗi xss
- cách thức tìm kiếm và khai thác


## Cross-Site Scripting (XSS)

**Cross-Site Scripting (XSS)** là một lỗ hổng bảo mật cho phép kẻ tấn công chèn và thực thi mã **JavaScript** độc hại trên trình duyệt của người dùng.

### Nguy cơ từ XSS
- **Đánh cắp phiên làm việc (Session)**  : Lấy cắp cookie để chiếm đoạt tài khoản người dùng.  

- **Thực hiện hành động giả mạo**  : Thay mặt người dùng gửi form, thực hiện giao dịch.  

- **Thu thập thông tin nhạy cảm**  : Keylogging, đánh cắp dữ liệu nhập vào form.  

- **Thay đổi nội dung trang**  : Thực hiện phishing bằng cách chèn form giả mạo.  

- **Tạo cửa hậu (Backdoor)**  : Thiết lập kết nối liên tục đến trình duyệt nạn nhân.  

## Các loại XSS và cách nhận diện

### Reflected XSS

-  Payload XSS được gửi đến server (thường qua URL) và phản chiếu ngay lập tức trong phản hồi. Khi người dùng nhấp vào link độc hại, trình duyệt sẽ thực thi mã độc.

- Sau khi access vào bài lab, thấy 1 ô tìm kiếm
<img width="908" height="121" alt="image" src="https://github.com/user-attachments/assets/b6d53d4a-80de-4cb9-a644-95ac2ac4e402" />

- Theo hint của bài, để thực hiện cuộc tấn công XSS bằng cách gọi hàm alert() và nhấn search

<img width="878" height="95" alt="image" src="https://github.com/user-attachments/assets/0aa5fb76-d054-46fd-bc88-eefd3e7a46a1" />

- Sau khi nhấn search thì hiện ô cảnh báo với dòng chữ hello

> Dữ liệu độc hại được được phản xạ ngay lập  tức trong res


