# Session 03 - Cryptography & Wallet

- Student: Vũ Trung Hiếu
- GitHub: [@trghieu03](https://github.com/trghieu03)
- Submitted: 2026-10-28
- Commit: [S03] add devlog - @trghieu03

## 1. Summary

Buổi này giúp mình hiểu nền tảng mật mã đứng sau blockchain: hash, cặp khóa public/private, chữ ký số. Từ đó hiểu ví (wallet) thực chất là gì, seed phrase quan trọng ra sao và cách giữ ví an toàn.

## 2. Topic notes

**Hashing**

* Hash là hàm biến dữ liệu bất kỳ thành một chuỗi cố định (ví dụ SHA-256 ra 256 bit).
* Cùng đầu vào luôn ra cùng kết quả; đổi một ký tự nhỏ thì hash đổi hoàn toàn.
* Một chiều: không suy ngược được dữ liệu gốc từ hash.
* Dùng trong blockchain để liên kết các block và đảm bảo dữ liệu không bị sửa.

**Public key / Private key**

* Private key: số bí mật, chỉ mình giữ, dùng để ký giao dịch.
* Public key: sinh ra từ private key, có thể chia sẻ công khai.
* Từ private key tính ra public key rất dễ, ngược lại gần như không thể.

**Digital Signature**

* Người gửi dùng private key để ký giao dịch.
* Ai cũng dùng public key để kiểm tra chữ ký hợp lệ.
* Chứng minh được: giao dịch do chủ khóa tạo ra (xác thực) và không bị sửa sau khi ký (toàn vẹn).

**Wallet & Address**

* Ví không "chứa" coin. Coin nằm trên blockchain; ví giữ private key để chứng minh quyền chi tiêu.
* Address (địa chỉ) được tạo từ public key, giống số tài khoản dùng để nhận tiền.

**Seed Phrase**

* Chuỗi từ (thường 12 hoặc 24 từ) dùng để khôi phục toàn bộ ví và các private key.
* Ai có seed phrase là kiểm soát được ví. Mất seed phrase mà mất thiết bị thì mất ví.
* Chỉ ghi ra giấy, cất offline; không chụp ảnh, không lưu trong ghi chú điện thoại hay chat, không gửi cho bất kỳ ai.

**Custodial vs Non-custodial Wallet**

| | Custodial | Non-custodial |
| - | - | - |
| Ai giữ private key | Bên thứ ba (sàn, dịch vụ) | Chính mình |
| Ưu điểm | Dễ dùng, quên mật khẩu vẫn khôi phục được | Toàn quyền kiểm soát, không phụ thuộc ai |
| Nhược điểm | Phụ thuộc bên giữ, rủi ro sàn bị hack hoặc đóng băng | Tự chịu trách nhiệm, mất seed phrase là mất hết |

**Basic Wallet Security**

* Không chia sẻ private key và seed phrase.
* Cảnh giác link/trang web giả mạo và tin nhắn lừa đảo (phishing).
* Kiểm tra kỹ địa chỉ trước khi gửi, vì giao dịch không hoàn lại được.
* Cài ví từ nguồn chính thức; với số tiền lớn nên cân nhắc hardware wallet.

## 3. Work completed

* Tham gia buổi học trên Discord (28/10).
* Ghi chú lại kiến thức theo 7 mục của buổi.
* Viết devlog theo template và push lên repo bootcamp-devlog.

## 4. Evidence

https://drive.google.com/file/d/1Tm7IV0GKwssF3yhYto9sAZzQhRLMCEz7/view?usp=sharing

## 5. Blockers

## 6. Takeaway

Buổi 3 cho mình thấy quyền kiểm soát tài sản trên blockchain nằm ở private key: giữ được khóa là giữ được tiền, nên bảo mật seed phrase là việc quan trọng nhất.
