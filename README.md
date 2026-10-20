# Bài tập môn An toàn và Bảo mật Thông tin

## Yêu cầu đề bài
- **Bài 1: Mã hóa đối xứng AES**
  - Sinh khóa AES, lưu khóa ra file, nạp khóa từ file.
  - Mã hóa chuỗi văn bản -> kết quả Base64 ra màn hình.
  - Mã hóa & giải mã file kích thước lớn (hàng GB) bằng kỹ thuật luồng CryptoStream.
  - Đo lường thời gian mã hóa/giải mã, tính tốc độ (MB/s).
  - So sánh từng byte (`byte-by-byte comparison`) giữa file nguồn và file giải mã -> Rút ra kết luận.
- **Bài 2: Mã hóa bất đối xứng RSA & Chữ ký số**
  - Sinh cặp khóa RSA, xuất định dạng chuẩn PEM.
  - Phân tích ý nghĩa các byte trong cấu trúc ASN.1 DER của file PEM (trích xuất Modulus $n$, Public Exponent $e$, Private Exponent $d$, các số nguyên tố $p, q$, hệ số CRT).
  - Mã hóa mảng bytes $\le 190$ bytes (khóa phiên AES 256-bit 32 bytes) bằng Public Key (OAEP-SHA256) -> lưu file Base64.
  - Giải mã bằng Private Key và đối chiếu dữ liệu gốc.
  - Đo và đánh giá tốc độ xử lý giữa Public Key ($e = 65537$ nhỏ) và Private Key ($d$ lớn).
  - Sinh chuỗi băm SHA-256 và khảo sát hiệu ứng tuyết lở (Avalanche Effect).
  - Nghiên cứu cơ chế chữ ký số: Đề xuất phương pháp để cùng 1 dữ liệu, cùng 1 Private Key nhưng mỗi lần ký cho ra chữ ký số hoàn toàn khác nhau (Chuẩn RSA-PSS RFC 8017).

## Deadline
25/10/2026 23:59

## Người thực hiện
- **Họ và tên:** Hoàng Đình Hiệu
- **GitHub:** [HoangDinhHieu](https://github.com/HoangDinhHieu)
- **Lớp / Khóa:** K59KMT

## Kết quả dự kiến
- Ứng dụng Windows Forms (.NET 8.0) hoàn chỉnh với giao diện trực quan.
- Chạy thử nghiệm thành công với file dung lượng lớn và kiểm thử tính toàn vẹn 100%.
- Thư mục `images/` lưu trữ đầy đủ ảnh chụp minh chứng kết quả chạy thực tế.
