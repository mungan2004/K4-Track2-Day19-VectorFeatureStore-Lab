# Reflection — Lab 19

**Tên:** Nguyễn Thị Mừng
**Cohort:** A20-K4
**Path đã chạy:** lite

---

## Câu hỏi (≤ 200 chữ)

> Trên golden set 50 queries, mode nào thắng ở loại query nào (`exact` /
> `paraphrase` / `mixed`), và tại sao? Khi nào bạn **không** dùng hybrid
> (i.e. khi nào pure BM25 hoặc pure vector là lựa chọn đúng)?

- **Exact:** BM25 thắng vì keyword signal mạnh mẽ với các từ khóa kỹ thuật khớp chính xác nguyên văn.
- **Paraphrase:** Cả BM25 và Vector đều giảm hiệu quả vì câu hỏi dùng các từ không có verbatim trong doc, nhưng Vector có khả năng tìm theo cụm ngữ nghĩa.
- **Mixed:** Hybrid thắng áp đảo vì nó trung hòa được cả ý tưởng paraphrase và exact term của query.

**Không dùng hybrid khi:**
- Khi tìm kiếm mã lỗi, log code, thông số ID chính xác (Nên dùng pure BM25).
- Khi hệ thống bị giới hạn ngân sách tính toán quá eo hẹp hoặc không có nhu cầu keyword match (Nên dùng pure vector).

---

## Điều ngạc nhiên nhất khi làm lab này

_(Optional, 1–2 câu)_

---

## Bonus challenge

- [ ] Đã làm bonus (xem `bonus/`)
- [ ] Pair work với: _<tên đồng đội nếu có>_
