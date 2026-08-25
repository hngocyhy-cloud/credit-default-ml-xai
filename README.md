# Dự báo rủi ro vỡ nợ khách hàng cá nhân — ML kết hợp Explainable AI

Khóa luận tốt nghiệp — Ngành Phân tích dữ liệu kinh doanh, Đại học Công nghiệp Hà Nội.

**Sinh viên:** Dương Thị Hồng Ngọc — 2022601391 — Lớp 2022DHDLKD01 - K17
**GVHD:** ThS. Trương Hoàng Giang

## Mô tả

Dự báo rủi ro vỡ nợ khách hàng thẻ tín dụng bằng Machine Learning (Logistic Regression,
Random Forest, XGBoost), xử lý mất cân bằng lớp bằng SMOTE, tối ưu ngưỡng phân loại
theo F2-score, và giải thích mô hình bằng SHAP (TreeSHAP).

Bộ dữ liệu: [Default of Credit Card Clients Dataset](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients) (Yeh & Lien, 2009), UCI Machine Learning Repository.

## Cấu trúc repo

```
.
├── notebooks/
│   └── KLTN_FILE_CODE.ipynb   # Notebook chính: EDA, feature engineering, mô hình, SHAP
├── docs/
│   └── KLTN_DuongThiHongNgoc_2022601391.pdf   # Toàn văn khóa luận
├── requirements.txt
└── README.md
```

## Cài đặt

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## Chạy notebook

```bash
jupyter notebook notebooks/KLTN_FILE_CODE.ipynb
```

Notebook tự động tìm file dữ liệu ở các vị trí phổ biến (local, Google Colab...).
Nếu chạy local, đặt file CSV gốc của bộ dữ liệu vào thư mục `data/` (không kèm trong repo).

## Kết quả chính

| Mô hình | ROC-AUC | PR-AUC | F2-score |
|---|---|---|---|
| Logistic Regression | 0.7436 | 0.5039 | 0.6034 |
| Random Forest | 0.7730 | 0.5491 | 0.6314 |
| XGBoost | 0.7727 | 0.5492 | 0.6330 |

Xem chi tiết trong khóa luận (`docs/`) hoặc notebook.

## License

Mục đích học thuật.
