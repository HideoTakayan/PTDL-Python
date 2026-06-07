# Đề tài: Phân tích và Dự báo mức độ xâm nhập mặn tại Đồng bằng sông Cửu Long

Đây là dự án Bài Tập Lớn môn **Lập Trình Phân Tích Dữ Liệu Với Python**.

## Thành viên nhóm
1. Đỗ Như Minh Hiếu
2. Trần Tiến Đức
3. Lê Xuân Hoàng

## Quy trình 7 Bước thực hiện:
1. **Thu thập dữ liệu**: Sử dụng dữ liệu quan trắc độ mặn (File `CSDL_DSS1_20240109_1.csv`) và mực nước (File `tanChauwaterLevel2016.json`).
2. **Làm sạch dữ liệu**: Xử lý `NaN`, chuyển đổi kiểu dữ liệu `datetime`.
3. **Khai phá dữ liệu (EDA)**: Vẽ biểu đồ xu hướng độ mặn theo tháng.
4. **Lập mô hình Machine Learning**: Sử dụng Linear Regression, Random Forest và XGBoost.
5. **Lựa chọn features**: Thêm biến trễ (Lag) và biến chu kỳ (Sin/Cos).
6. **Đánh giá và So sánh**: Dùng `RMSE`, `MAE`, `R2 Score` để so sánh các mô hình.
7. **Báo cáo**: Kết quả được lưu tại thư mục `reports`.

## Cách chạy dự án
1. Mở terminal và cài đặt thư viện: `pip install -r requirements.txt`
2. Mở Jupyter Notebook: `jupyter notebook`
3. Lần lượt chạy các file trong thư mục `notebooks/`.
