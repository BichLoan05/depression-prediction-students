# depression-prediction-students
## I. Giới thiệu
Dự án xây dựng mô hình Machine Learning nhằm dự đoán nguy cơ trầm cảm ở sinh viên dựa trên các yếu tố học tập, lối sống và tài chính

Trọng tâm của bài toán: Tối ưu hóa chỉ số Recall (Độ nhạy) để hạn chế tối đa việc bỏ sót các trường hợp sinh viên có nguy cơ cao, đảm bảo không ai bị bỏ lại phía sau trong công tác hỗ trợ tâm lý học đường

## II. Pipeline chính
### 1. Data Cleaning
- Loại bỏ outliers (sử dụng IQR và Rule-based)
- Xử lý missing values (sử dụng Median)
- Loại bỏ các features không có phương sai để tránh nhiễu
### 2. Feature Engineering
- Gom nhóm dữ liệu (City → Region, ...)
- Encoding: Kết hợp Ordinal Encoding và One-hot Encoding
- Scaling: Chuẩn hóa dữ liệu bằng StandardScaler
### 3. Handling Imbalance
- Sử dụng kỹ thuật SMOTE trên tập Train để cân bằng lớp dữ liệu
### 4. Modeling
- Logistic Regression (Final Model - Mô hình được chọn)
- Random Forest
- XGBoost
- SVM
### III. Result
| Metric    | Value   | Đánh giá |
|----------|--------|----------|
| Accuracy | 84.49% | Tốt |
| Precision| 86.15% | Rất tốt |
| Recall   | 87.59% | Xuất sắc (Mục tiêu cốt lõi) |
| F1-score | 86.87% | Cân bằng tốt |
| ROC-AUC  | 91.95% | Khả năng phân loại cực mạnh |
## IV. Dataset
Dataset sử dụng trong dự án:

[Student_depression_dataset (1).csv](./Student_depression_dataset%20(1).csv)

## V. Công nghệ sử dụng
- Ngôn ngữ: Python
- Thư viện xử lý dữ liệu: Pandas, NumPy
- Machine Learning: Scikit-learn, Imbalanced-learn (SMOTE)
- Trực quan hóa: Matplotlib, Seaborn
## VI. Hướng phát triển
- Tuning hyperparameters sâu hơn (GridSearch / Optuna)
- Thử nghiệm Deep Learning models
- Deploy mô hình (API / Web App)
