# Session 06 - DApps & Web3 Ecosystem

- **Sinh viên:** Vũ Trung Hiếu (GitHub @trghieu03)
- **Ngày nộp:** 12/11/2026
- **Commit:** `[S06] add devlog`

## 1. Summary

Buổi học về kiến trúc của một ứng dụng phi tập trung (dApp), luồng tương tác Frontend → Wallet → Smart Contract → Blockchain, các nhóm ứng dụng chính trong hệ sinh thái Web3 (DeFi, Payment, NFT, Gaming, DAO), vai trò của Oracle và một mini demo trên testnet.

## 2. Topic notes

### dApp Architecture
- dApp = giao diện web/app thông thường + smart contract chạy trên blockchain làm phần logic và lưu trạng thái quan trọng.
- Khác ứng dụng truyền thống: không có một máy chủ backend duy nhất kiểm soát dữ liệu; ai cũng có thể kiểm tra mã contract và giao dịch.
- Dữ liệu lớn (ảnh, file) thường lưu ngoài chuỗi (ví dụ IPFS), trên chuỗi chỉ lưu tham chiếu/hash.

### Frontend → Wallet → Smart Contract → Blockchain
1. **Frontend:** người dùng bấm thao tác trên giao diện.
2. **Wallet:** ví hiển thị giao dịch để người dùng xem và ký bằng private key (ứng dụng không giữ khóa của người dùng).
3. **Smart Contract:** giao dịch đã ký gọi hàm của contract.
4. **Blockchain:** node xác thực, đưa vào block, cập nhật state; frontend đọc lại kết quả để hiển thị.

### Các nhóm ứng dụng
- **DeFi:** dịch vụ tài chính không qua trung gian (sàn phi tập trung, cho vay, staking) chạy bằng smart contract.
- **Payment:** chuyển giá trị nhanh, xuyên biên giới, thường dùng stablecoin.
- **NFT:** token đại diện quyền sở hữu tài sản số duy nhất (nghệ thuật, vé, vật phẩm).
- **Gaming:** vật phẩm trong game là tài sản người chơi thực sự sở hữu và có thể chuyển nhượng.
- **DAO:** tổ chức tự vận hành, thành viên bỏ phiếu quản trị theo quy tắc ghi trong smart contract.

### Oracle (mức giới thiệu)
- Smart contract không tự lấy được dữ liệu ngoài chuỗi (giá, thời tiết, kết quả sự kiện).
- Oracle là cầu nối đưa dữ liệu bên ngoài vào blockchain; cần đáng tin cậy vì dữ liệu sai sẽ làm contract chạy sai.

### Mini Demo trên Testnet
- Testnet là mạng thử nghiệm, token không có giá trị thật, dùng để thử giao dịch an toàn.
- Các bước minh họa: kết nối ví vào dApp, thực hiện một thao tác, ký giao dịch trong ví, theo dõi kết quả trên explorer.

## 3. Work completed
- Tham gia buổi học trên Discord.
- Ghi chú theo các mục của đề cương.
- Viết devlog và đẩy lên repo bootcamp-devlog.

## 4. Evidence
- (bổ sung sau)

## 5. Blockers
- (để trống nếu không có)

## 6. Takeaway
dApp khác ứng dụng thường ở chỗ logic nằm trong smart contract công khai và người dùng tự nắm khóa qua ví, nên cần hiểu rõ luồng ký giao dịch trước khi dùng.
