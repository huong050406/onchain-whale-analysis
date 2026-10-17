
# PHÂN TÍCH MẠNG LƯỚI ON-CHAIN VÀ SỰ LAN TRUYỀN RỦI RO TỪ CÁC VÍ CÁ VOI

**Tên tiếng Anh:** On-chain Network & Whale Contagion Analysis

## 1. Giới thiệu dự án

Dự án nghiên cứu cấu trúc mạng lưới giao dịch blockchain, hoạt động của các ví cá voi (whales) và mối liên hệ giữa dòng tiền on-chain với biến động thị trường tiền mã hóa.

Nghiên cứu kết hợp phân tích mạng lưới (Graph Analytics), phương pháp kinh tế lượng, học máy (Machine Learning) và trực quan hóa dữ liệu nhằm nhận diện những đặc điểm quan trọng trong mạng lưới giao dịch và đánh giá khả năng dự báo rủi ro thị trường.

## 2. Mục tiêu nghiên cứu

- Xây dựng mạng lưới giao dịch blockchain theo thời gian.
- Phân tích cấu trúc mạng lưới, mức độ kết nối và vai trò của các địa chỉ ví.
- Nhận diện hoạt động của các ví cá voi và dòng tiền giao dịch lớn.
- Phân tích mối liên hệ giữa whale flows và biến động thị trường.
- Xây dựng, đánh giá và so sánh các mô hình thống kê, học máy.
- Phát triển dashboard trực quan hóa mạng lưới và các chỉ số liên quan.

## 3. Câu hỏi nghiên cứu

**RQ1:** Cấu trúc mạng lưới giao dịch thay đổi như thế nào giữa giai đoạn thị trường bình thường và giai đoạn căng thẳng?

**RQ2:** Các ví giữ vị trí trung tâm trong mạng lưới có vai trò nổi bật trong việc luân chuyển dòng tiền hay không?

**RQ3:** Các giao dịch giá trị lớn và dòng tiền chuyển vào sàn giao dịch có khả năng dự báo biến động thị trường trong ngắn hạn hay không?

**RQ4:** Mức độ tập trung trong mạng lưới có gia tăng trước những giai đoạn thị trường căng thẳng hay không?

**RQ5:** Các mô hình học máy dựa trên đồ thị có cải thiện khả năng phân loại địa chỉ ví so với mô hình học máy truyền thống hay không?

## 4. Dữ liệu nghiên cứu

### 4.1. Nguồn dữ liệu dự kiến

Dữ liệu blockchain:
- Google Blockchain Analytics / BigQuery
- Ethereum Public Datasets
- Etherscan và các nguồn nhãn địa chỉ công khai

Dữ liệu thị trường:
- Binance
- CoinGecko

### 4.2. Phạm vi dữ liệu

Các nội dung đang chờ nhóm thống nhất:
- Blockchain và token nghiên cứu
- Khoảng thời gian nghiên cứu
- Phương pháp lấy mẫu giao dịch
- Tần suất quan sát dữ liệu
- Danh sách nguồn dữ liệu chính thức

## 5. Cấu trúc dự án

```text
onchain-whale-analysis/
├── README.md
├── requirements.txt
├── .gitignore
├── config/
├── data/
│   ├── raw/
│   ├── interim/
│   └── processed/
├── src/
│   ├── data/
│   ├── features/
│   ├── models/
│   ├── evaluation/
│   └── utils/
├── notebooks/
├── dashboard/
├── tests/
├── outputs/
│   ├── tables/
│   └── figures/
└── paper/
```

### Chức năng các thư mục

- `config/`: Lưu các thông số cấu hình nghiên cứu.
- `data/raw/`: Lưu dữ liệu gốc.
- `data/interim/`: Lưu dữ liệu trung gian trong quá trình xử lý.
- `data/processed/`: Lưu dữ liệu đã xử lý.
- `src/data/`: Code thu thập và tiền xử lý dữ liệu.
- `src/features/`: Code xây dựng các chỉ số mạng lưới và whale features.
- `src/models/`: Code xây dựng mô hình kinh tế lượng và học máy.
- `src/evaluation/`: Code đánh giá mô hình và kiểm định độ vững.
- `src/utils/`: Các hàm hỗ trợ dùng chung.
- `notebooks/`: Phân tích và thử nghiệm dữ liệu.
- `dashboard/`: Xây dựng giao diện trực quan hóa.
- `tests/`: Kiểm thử chương trình.
- `outputs/tables/`: Lưu bảng kết quả nghiên cứu.
- `outputs/figures/`: Lưu biểu đồ và hình ảnh.
- `paper/`: Lưu nội dung báo cáo học thuật.

## 6. Hướng dẫn cài đặt

### 6.1. Yêu cầu

- Python
- Git
- Visual Studio Code (khuyến nghị)

### 6.2. Tải dự án

```bash
git clone https://github.com/huong050406/onchain-whale-analysis.git
cd onchain-whale-analysis
```

### 6.3. Tạo môi trường Python

```powershell
python -m venv .venv
```

Kích hoạt môi trường trên Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 6.4. Cài đặt thư viện

```powershell
python -m pip install -r requirements.txt
```

## 7. Quy trình nghiên cứu

**Giai đoạn 1: Thu thập và xử lý dữ liệu**

Thu thập dữ liệu giao dịch blockchain, dữ liệu thị trường và nhãn địa chỉ ví; làm sạch, chuẩn hóa và đồng bộ dữ liệu.

**Giai đoạn 2: Phân tích mạng lưới giao dịch**

Xây dựng đồ thị giao dịch, tính toán các chỉ số centrality, phân tích cộng đồng và nhận diện hoạt động của ví cá voi.

**Giai đoạn 3: Phân tích kinh tế lượng**

Kiểm định mối liên hệ giữa whale flows, cấu trúc mạng lưới và biến động thị trường bằng mô hình hồi quy và nghiên cứu sự kiện.

**Giai đoạn 4: Xây dựng mô hình học máy**

Phát triển các mô hình phân loại địa chỉ ví, đánh giá hiệu quả và so sánh giữa các phương pháp.

**Giai đoạn 5: Xây dựng dashboard**

Trực quan hóa mạng lưới giao dịch, các địa chỉ ví quan trọng, dòng tiền cá voi và các chỉ số biến động thị trường.

**Giai đoạn 6: Tổng hợp và báo cáo**

Tổng hợp kết quả thực nghiệm, thực hiện các kiểm định cần thiết và hoàn thiện báo cáo nghiên cứu.

## 8. Phân công công việc

Dự án được thực hiện bởi nhóm gồm 6 thành viên.

Nội dung công việc, người phụ trách, người hỗ trợ và các nhiệm vụ phụ thuộc được trình bày trong file `Phan_cong_Blueprint08.xlsx`.

Các thành viên thực hiện công việc theo nhiệm vụ được phân công và phối hợp thông qua GitHub.

## 9. Nguyên tắc làm việc nhóm

- Sử dụng cấu trúc thư mục thống nhất.
- Không tự ý thay đổi định dạng dữ liệu đầu vào dùng chung.
- Viết code có chú thích, tên biến rõ ràng.
- Lưu nguồn dữ liệu và thời điểm thu thập.
- Không đưa thông tin đăng nhập, API key hoặc dữ liệu nhạy cảm lên GitHub.
- Ưu tiên sử dụng nhánh Git riêng cho từng nhiệm vụ.
- Kiểm tra code trước khi hợp nhất vào nhánh chính.
- Đảm bảo kết quả có thể tái lập.

## 10. Tiến độ dự án

**Trạng thái hiện tại:** Khởi tạo repository và chuẩn bị môi trường nghiên cứu.

Các nội dung đang chờ hoàn thiện:
- Thống nhất dữ liệu và phạm vi nghiên cứu.
- Hoàn thiện cấu hình dự án.
- Thu thập và xử lý dữ liệu.
- Triển khai các mô hình phân tích.
- Xây dựng dashboard.
- Hoàn thiện báo cáo nghiên cứu.

## 11. Lưu ý

Dự án được thực hiện phục vụ mục đích học thuật và nghiên cứu.

Các kết quả phân tích, dự báo và trực quan hóa không được xem là khuyến nghị đầu tư.
