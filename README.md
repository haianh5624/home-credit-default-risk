# Phân tích và Dự báo Rủi ro Tín dụng (Home Credit Default Risk)

## Mục tiêu dự án
Dự án này tập trung xây dựng một hệ thống phân loại rủi ro tín dụng cho khách hàng cá nhân dựa trên bộ dữ liệu của Home Credit. Mục tiêu là phát triển mô hình học máy để dự đoán khả năng vỡ nợ của khách hàng, từ đó hỗ trợ các tổ chức tài chính ra quyết định phê duyệt khoản vay một cách chính xác và tự động hóa.

## Các tính năng chính
-   **Xử lý dữ liệu đa nguồn:** Tích hợp và tiền xử lý dữ liệu từ nhiều bảng khác nhau của Home Credit.
-   **Kỹ thuật đặc trưng (Feature Engineering):** Tạo ra các biến số mới dựa trên kiến thức nghiệp vụ để tăng cường sức mạnh dự báo của mô hình.
-   **Mô hình học máy tiên tiến:** Sử dụng các thuật toán mạnh mẽ như XGBoost, LightGBM và Random Forest.
-   **Tối ưu hóa hiệu suất:** Áp dụng kỹ thuật Lựa chọn đặc trưng (Feature Selection) và Tinh chỉnh siêu tham số tự động (Hyperparameter Tuning) với **Optuna**.
-   **Mô hình kết hợp (Ensemble Learning):** Kết hợp các mô hình đơn lẻ để đạt độ chính xác và tính ổn định cao nhất.
-   **Hệ thống hỗ trợ ra quyết định (Dashboard):** Ứng dụng web trực quan giúp nhân viên tín dụng tra cứu hồ sơ và phân tầng rủi ro (An toàn - Cảnh báo - Nguy hiểm).

## Công nghệ sử dụng
-   **Ngôn ngữ:** Python
-   **Thư viện chính:** Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Optuna, Streamlit.

## Kết quả đạt được
-   Mô hình Ensemble đạt hiệu suất phân loại ấn tượng với **ROC-AUC = 0.7905** và **hệ số Gini = 0.5811** trên tập kiểm thử (Validation Set).
-   Khả năng phân tách nhóm rủi ro (KS Statistic) đạt **44.15%**.
-   Mô hình có khả năng phát hiện **hơn 42%** số trường hợp nợ xấu tiềm ẩn.

## Hướng dẫn chạy dự án
1.  **Clone repository:**
    ```bash
    git clone []
    cd home-credit-default-risk
    ```
2.  **Cài đặt các thư viện cần thiết:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Tải dữ liệu:** Tải bộ dữ liệu gốc từ cuộc thi Kaggle Home Credit Default Risk và đặt vào thư mục `data/` (hoặc thư mục bạn đã dùng).
4.  **Chạy Notebook tiền xử lý và huấn luyện:** Mở và chạy file `Tiền xử lý dữ liệu.ipynb` và các Notebook liên quan để xử lý dữ liệu và huấn luyện mô hình. Sau khi chạy, các file mô hình (`.pkl`) và dữ liệu mẫu (`file_demo_chuan.csv`) sẽ được tạo ra.
6.  **Khởi động Dashboard:**
    ```bash
    streamlit run dashboard_final.py
    ```
    Sau đó truy cập `http://localhost:8501` trên trình duyệt của bạn.
   
