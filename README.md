[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574192&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** phung352100@gmail.com
**Name:** Đào Danh Đăng Phụng

---

## Mo ta

(Triển khai pipeline ETL: đọc `raw_data.json`, lọc bản ghi không hợp lệ (price <= 0 hoặc `category` trống), tính `discounted_price = price * 0.9`, chuẩn hóa `category` sang Title Case, thêm `processed_at` và lưu kết quả ra `processed_data.csv`. Có script `agent_simulation.py` để so sánh phản hồi khi dùng dữ liệu sạch và dữ liệu rác.)

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tóm tắt kết quả: 3 bản ghi đã được xử lý/giữ lại; 2 bản ghi bị loại. Kết quả đã được lưu vào `processed_data.csv`.)
