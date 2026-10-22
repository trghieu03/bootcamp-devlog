# Session 02 - How Blockchain Works

- Student: Vũ Trung Hiếu
- GitHub: [@trghieu03](https://github.com/trghieu03)
- Submitted: 2026-10-21
- Commit: [S02] add devlog - @trghieu03

## 1. Summary

Buổi này giúp mình hiểu blockchain vận hành bên trong như thế nào: cấu trúc block, giao dịch, sổ cái và trạng thái, mạng node ngang hàng, và đường đi của một giao dịch từ lúc tạo đến lúc được xác nhận.

## 2. Topic notes

**Block và cấu trúc chuỗi**
Mỗi block gồm phần header (hash của block trước, thời gian, các giá trị phục vụ xác thực) và phần body (danh sách giao dịch). Vì mỗi block chứa hash của block liền trước nên chúng nối thành chuỗi. Sửa một block cũ sẽ làm đổi hash và phá vỡ cả chuỗi phía sau.

**Transaction là gì?**
Là một lệnh chuyển giá trị hoặc dữ liệu: người gửi, người nhận, số lượng và phí. Giao dịch được ký bằng private key của người gửi để chứng minh quyền sở hữu.

**Ledger và State**
- Ledger: toàn bộ lịch sử giao dịch, chỉ ghi thêm, không sửa.
- State: trạng thái hiện tại (ví dụ số dư từng địa chỉ), được tính ra từ ledger.

**Node và mạng P2P**
Node là máy tham gia mạng. Các node nối trực tiếp với nhau (peer-to-peer), không có máy chủ trung tâm. Mỗi full node giữ một bản sao dữ liệu và tự kiểm tra giao dịch, block mới.

**Vòng đời một giao dịch**
1. Người dùng tạo giao dịch và ký bằng private key.
2. Giao dịch được gửi lên mạng và nằm chờ trong mempool.
3. Miner/validator chọn giao dịch đưa vào block mới.
4. Các node kiểm tra block, thêm vào chuỗi.
5. Càng nhiều block được thêm phía sau thì giao dịch càng chắc chắn.

**Blockchain Explorer**
Là website tra cứu công khai block, giao dịch và địa chỉ trên blockchain (ví dụ Etherscan cho Ethereum). Dùng để kiểm chứng giao dịch đã được xác nhận chưa.

## 3. Work completed

- Tham gia buổi học trên Discord (21/10).

## 4. Evidence

https://drive.google.com/file/d/1wWnwPLqqpKX4B4pdZflRoHaKvPW-7bpA/view?usp=sharing

## 5. Blockers

## 6. Takeaway
*Mã hash (hash)
Hash là kết quả của một hàm băm: đưa dữ liệu bất kỳ vào, nhận về một chuỗi có độ dài cố định (SHA-256 luôn ra 256 bit). Đặc điểm:
- Cùng dữ liệu thì luôn ra cùng một hash.
- Đổi một ký tự nhỏ thì hash đổi hoàn toàn.
- Một chiều: từ hash không suy ngược ra được dữ liệu gốc.
MD5 và SHA-1 không còn an toàn, blockchain dùng SHA-256.

*Hash trong blockchain
- Nối block: mỗi block chứa hash của block trước, sửa block cũ thì chuỗi phía sau đứt.
- Proof of Work: thợ đào thử nonce cho đến khi hash của block có đủ số số 0 ở đầu theo độ khó.
- Địa chỉ ví: tạo từ public key qua các hàm băm, nên không suy ngược ra khóa được.
- Merkle tree: băm các giao dịch theo cặp thành cây, chỉ cần lưu Root Hash trong header để kiểm tra nhanh.


