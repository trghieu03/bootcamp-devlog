# Session 01 - Blockchain Fundamentals

- Student: Vũ Trung Hiếu
- GitHub: [@trghieu03](https://github.com/trghieu03)
- Submitted: 2026-10-21
- Commit: [S01] add devlog - @trghieu03

## 1. Summary

Buổi này giúp mình hiểu blockchain là gì, vì sao nó ra đời, khác gì so với hệ thống tập trung, và Bitcoin/Ethereum đóng vai trò gì trong đó.

## 2. Topic notes

**Blockchain là gì?**
Là một sổ cái (ledger) kỹ thuật số phi tập trung. Dữ liệu được ghi thành các khối (block), mỗi khối liên kết với khối trước bằng mã hóa (hash), tạo thành một chuỗi. Sửa một khối cũ sẽ làm hỏng mọi khối phía sau, nên dữ liệu rất khó bị thay đổi.

**Tập trung vs Phi tập trung**
- Tập trung: một bên (ngân hàng, công ty) giữ dữ liệu và quyết định. Nhanh, dễ quản lý, nhưng phụ thuộc vào bên đó và có điểm lỗi duy nhất.
- Phi tập trung: dữ liệu nằm trên nhiều máy (node), không ai kiểm soát một mình. Minh bạch và khó bị chặn hơn, nhưng thường chậm hơn.

**Bitcoin ra đời để giải quyết vấn đề gì?**
Giải quyết bài toán chuyển tiền trực tiếp giữa hai người mà không cần ngân hàng làm trung gian, và không bị chi tiêu hai lần (double spending). Ưu điểm: không cần tin vào bên thứ ba, minh bạch. Nhược điểm: tốc độ giao dịch thấp, tốn điện (Proof of Work), giá biến động mạnh.

**Ethereum mở rộng blockchain thế nào?**
Bitcoin chủ yếu để chuyển giá trị. Ethereum thêm smart contract (chương trình chạy trên blockchain), cho phép xây ứng dụng phi tập trung (dApp) như DeFi, NFT.

**Lợi ích và ứng dụng**
- Lợi ích: minh bạch, bất biến, không cần trung gian.
- Ứng dụng: thanh toán, tài chính phi tập trung (DeFi), truy xuất nguồn gốc hàng hóa, NFT.

## 3. Work completed

- Tham gia buổi học trên Discord (14/10).
- Cài Git, clone repo mẫu dev-lock-bootcamp về máy.
- Đổi remote sang repo bootcamp-devlog của mình.
- Tạo file devlog theo template.

```
git clone https://github.com/vantuann205/dev-lock-bootcamp.git
git remote set-url origin https://github.com/trghieu03/bootcamp-devlog.git
```

## 4. Evidence

| Task | Evidence URL | What it proves |
|------|--------------|----------------|
| Repo nộp bài | https://github.com/trghieu03/bootcamp-devlog | Repo đã tạo và có devlog |
| Devlog buổi 1 | https://github.com/trghieu03/bootcamp-devlog/blob/main/submissions/trghieu03/session-01.md | Đã nộp devlog buổi 1 |

## 5. Blockers

Lúc đầu máy chưa cài Git nên báo lỗi `'git' is not recognized`. Mình đã cài Git và mở lại Command Prompt thì chạy được. Mình cũng gõ nhầm lệnh copy file (dùng `/` thay vì `\`), đã sửa lại.

## 6. Takeaway

Buổi 1 cho mình bức tranh tổng quan: blockchain là sổ cái phi tập trung. Buổi 2 sẽ đi sâu vào cách nó hoạt động: cấu trúc block, transaction, node và vòng đời một giao dịch.