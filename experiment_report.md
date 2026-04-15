# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-XXXX
**Name:** (Đào Danh Đăng Phụng)
**Date:** (2026-04-15)

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | (Agent: Based on my data, the best choice is Laptop at $1200.0.) | (9) | (Agent picks the expected high-priced electronics from clean data.) |
| Garbage Data (`garbage_data.csv`) | (Agent: Based on my data, the best choice is Nuclear Reactor at $999999.) | (2) | (Poisoned/outlier record (extreme price) causes wrong recommendation.) |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

(Agent trả lời sai khi dùng dữ liệu rác vì dữ liệu bị 'poisoned' có nhiều lỗi chất lượng. Các vấn đề chính gồm: outliers (giá cực lớn như 999999) làm thuật toán chọn theo giá bị lệch; kiểu dữ liệu không đúng (ví dụ 'ten dollars') gây lỗi khi chuyển sang số; giá trị null hoặc `category` rỗng làm mất khả năng phân loại; duplicate IDs gây sai lệch thống kê. Cần xử lý: loại bỏ/cắt tỉa outlier, chuyển đổi kiểu, loại bản ghi null, xử lý trùng lặp trước khi đưa vào agent.)

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

(Đồng ý. Nếu dữ liệu kém chất lượng thì prompt tốt cũng không đảm bảo kết quả đúng; chất lượng dữ liệu là yếu tố quyết định.)
