# Đồ Án Lập Trình Phân Tích Dữ Liệu: Hồi quy Không-Thời gian Độ Mặn ĐBSCL

Đây là một bài phân tích Machine Learning cơ bản (Spatiotemporal Regression), sử dụng dữ liệu độ mặn ĐBSCL và mực nước Châu Đốc.

## Mục tiêu
Dùng thông tin vị trí (Kinh độ, Vĩ độ), thời gian (Tháng) và biến proxy (Mực nước Châu Đốc) để ước lượng độ mặn tại các quan trắc năm 2022 bằng Random Forest/XGBoost.

## Quy trình 7 Bước thực hiện:
1. **Thu thập dữ liệu**: Sử dụng dữ liệu quan trắc độ mặn ĐBSCL và Mực nước Châu Đốc.
2. **Làm sạch dữ liệu**: Ghép nối dữ liệu quá khứ gần nhất bằng `merge_asof(direction='backward')` (tối đa 3 ngày).
3. **Khai phá dữ liệu (EDA)**: Vẽ bản đồ phân bố mặn (Scatter map) và Boxplot khảo sát sự khác biệt theo tháng.
4. **Lập mô hình học máy**: Sử dụng các thuật toán Machine Learning (Random Forest, XGBoost) để xây dựng bài toán Hồi quy Không-Thời gian.
5. **Chia tập Train/Test**: Sử dụng Temporal Split (Train < 2022, Test == 2022). Đảm bảo không có rò rỉ dữ liệu.
6. **Đánh giá và So sánh**: So sánh RMSE, MAE, R2 giữa các mô hình và Baseline (Trung bình trạm).
7. **Báo cáo**: Hiển thị biểu đồ phân tán (Scatter plot) so sánh thực tế và ước lượng năm 2022 tại Trạm QL1.

## Cách chạy dự án
1. Mở terminal và cài đặt thư viện: `pip install -r requirements.txt`
2. Đảm bảo dữ liệu nằm đúng trong thư mục `data/raw/`
3. Chạy file `notebooks/BTL.ipynb`.
