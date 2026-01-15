# � Dự đoán GDP Việt Nam bằng ARIMA, RNN và LSTM

## 1. Mục tiêu

Xây dựng và so sánh các mô hình dự đoán GDP Việt Nam dựa trên dữ liệu chuỗi thời gian nhằm đánh giá hiệu quả của các phương pháp truyền thống và học sâu.

## 2. Dữ liệu

**Nguồn:** World Bank

**Biến mục tiêu:** GDP (current US$)

**Dữ liệu được tiền xử lý:**

- Chuẩn hóa giá trị thiếu
- Ép kiểu dữ liệu sang số
- Loại bỏ các năm thiếu thông tin
- Điền giá trị thiếu bằng backfill & forward fill
- Sắp xếp theo thời gian

## 3. Các mô hình sử dụng

- **ARIMA:** mô hình thống kê truyền thống, đơn biến
- **RNN:** mạng nơ-ron hồi tiếp, học được quan hệ theo thời gian
- **LSTM:** cải tiến từ RNN, xử lý tốt phụ thuộc dài hạn

## 4. Kết quả đánh giá

| Mô hình | MAE (USD) | RMSE (USD) | R² |
|--------|-----------|-----------|-----|
| ARIMA | 37,646,224,349 | 44,914,364,139 | 0.4719 |
| RNN | 14,511,524,207 | 18,753,470,089 | 0.8382 |
| LSTM | 12,541,306,440 | 14,592,228,635 | 0.9020 |

## 5. Nhận xét

- ARIMA cho kết quả thấp do không mô hình hóa được quan hệ phi tuyến
- RNN cải thiện đáng kể độ chính xác
- LSTM cho kết quả tốt nhất, phù hợp nhất với bài toán dự đoán GDP chuỗi thời gian

## 6. Kết luận

LSTM là mô hình hiệu quả nhất trong ba mô hình được thử nghiệm và có tiềm năng ứng dụng trong dự đoán GDP ngắn hạn và trung hạn.

➡️ Trong phạm vi nghiên cứu này, **LSTM** được xem là mô hình phù hợp nhất để dự đoán GDP Việt Nam.

## 6. Công nghệ sử dụng

- Python, Pandas, NumPy
- Scikit-learn
- Statsmodels
- TensorFlow / Keras
- Jupyter Notebook / Google Colab

---

📌 *By Đỗ Đức Cảnh*

