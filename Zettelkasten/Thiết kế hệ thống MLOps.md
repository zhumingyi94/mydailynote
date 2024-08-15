**202408080723**
**Status:** #flashcards #mlops 
**Tags:** [[Reference notes/MLOps]]
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

# Thiết kế hệ thống MLOps
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

### Key note
#### Thiết kế
Ta cần phải xác định được: 
1. Added Value
	- Tiền 
	- Thời gian
2. Từ đó xác định yêu cầu (Business)
	- Tốc độ 
	- Độ chính xác
	- Giải thích được
	- Tuân thủ
	- Kinh phí 
	- Con người 
3. Độ đo
	-  Độ chính xác 
	- Doanh thu 
	- Sự hài lòng của khách hàng
4. Phân tích dữ liệu
	- Đúng (Acc)
	- Đầy đủ (Completeness)
	- Nhất quán (Consistency)
	- Cập nhật (Timely)
5. Pipeline thu thập dữ liệu (Quan trọng nhất)

#### Phát triển
- Kỹ thuật phân tích đặc trưng 
- Feature Store khi cùng lúc làm việc với nhiều thuật toán học máy khác nhau và có thể sử dụng chung một phần dữ liệu
- Kiểm soát & theo dõi thí nghiệm:
	- Giả thuyết: Tôi nghĩ rằng ... (Có thể đúng / sai nhưng **PHẢI KIỂM CHỨNG** được)
	- Thu thập dữ liệu 
	- Lựa chọn các tham số
- Công cụ lưu trữ kết quả thí nghiệm 
- Huấn luyện mô hình
- Kiểm tra trên tập kiểm thử 
- Tính toán độ đo $\to$ Lựa chọn mô hình tốt nhất
- Bảng biểu, đồ thị, báo cáo

#### Triển khai
- Môi trường chạy (runtime environment) $\to$ Container
- Microservices $\to$ API
- CI/CD:
	- Integration: Plan, Code, Build, Test 
	- Test success $\to$ Deployment: Release, operate   
	- *Đầu tư cho kỹ năng test (Unit test, module test, integration test, ...)*

#### Giám sát 
- Độ đo (Business)
- Độ đo (tính toán). Vd: CPU, RAM, storage, GPU, ...
$\implies$ Retraining khi: 
	- Data Drift: Input thay đổi
	- Concept Drift: Input-Output thay đổi (Quan hệ thay đổi)
#### Giới thiệu về các tools
- Feature Store: Feast, Hopsworks
- Container: Docker, K8s (Auto Scaling)
- CI/CD: Github Action, Gitlab CI/CD
- Monitoring: Fiddler
- Data Monitoring: Great Expectations
- Chứng chỉ: AWS SageMaker, Azure Machine Learning, Google Cloud AI Platform, ...
- Container riêng cho ML: Nvidia container (Deepstream $\to$ phân tích ảnh)
### Exercise

### References

