![image](https://github.com/user-attachments/assets/21fc4dbb-fcf6-4a99-a663-3399b2eb0852)
![image](https://github.com/user-attachments/assets/9c59f37a-8ffa-4ce2-99bd-92d755bc8a1f)
1. Giới thiệu
Ứng dụng “Truyền File Có Ký Số” là một công cụ hỗ trợ gửi và nhận tệp tin kèm chữ ký số nhằm đảm bảo an toàn và toàn vẹn dữ liệu trong quá trình trao đổi thông tin. Ứng dụng mô phỏng mô hình Client - Server, trong đó phía gửi (Client) thực hiện ký số tệp tin trước khi truyền đi, còn phía nhận (Server) sẽ kiểm tra xác thực chữ ký nhằm đảm bảo tệp tin không bị giả mạo hay chỉnh sửa.

Mục tiêu chính của ứng dụng là:

Xác thực nguồn gốc tệp tin (Authenticity),

Bảo đảm tính toàn vẹn dữ liệu (Integrity),

Ngăn chặn hành vi chối bỏ trách nhiệm (Non-repudiation).

2. Chức năng cơ bản
Ứng dụng bao gồm hai phần chính: Gửi File (Client) và Nhận File (Server), với các chức năng cụ thể:

Phía Gửi File (Client):

Cho phép người dùng chọn tệp cần gửi.

Lựa chọn thuật toán ký số (RSA 2048/4096-bit).

Tạo cặp khóa mới (khóa riêng & khóa công khai).

Ký số tệp tin bằng khóa riêng và gửi kèm tệp.

Phía Nhận File (Server):

Cho phép người dùng tải khóa công khai từ phía client.

Nhận tệp tin đã ký và thực hiện xác thực chữ ký.

Hiển thị trạng thái xác thực (Hợp lệ hoặc Không hợp lệ).

3. Kỹ thuật và công nghệ sử dụng
Ứng dụng được xây dựng với các công nghệ và kỹ thuật hiện đại, đảm bảo tính bảo mật và trải nghiệm người dùng tốt:

Frontend:

HTML5, CSS3, JavaScript: Giao diện người dùng trực quan, dễ sử dụng.

Bootstrap (hoặc tương đương): Giúp tối ưu giao diện trên nhiều kích thước màn hình.

Bảo mật và mã hóa:

Thuật toán RSA: Dùng để tạo cặp khóa và ký số dữ liệu, hỗ trợ RSA 2048-bit và RSA 4096-bit.

WebCrypto API (trong trình duyệt): Thực hiện các thao tác mã hóa, ký số và xác thực.

Kiến trúc ứng dụng:

Mô hình Client - Server giả lập ngay trong trình duyệt, giúp người học nắm bắt nhanh cơ chế ký và xác thực.

Không yêu cầu backend (có thể chạy offline thông qua file .html).
