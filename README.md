# 🎮 Phân Tích Dữ Liệu Thăm Dò (EDA) - Doanh Số Bán Trò Chơi Điện Tử

## 📋 Giới Thiệu

Dự án này thực hiện phân tích dữ liệu thăm dò (Exploratory Data Analysis - EDA) trên bộ dữ liệu về doanh số bán trò chơi điện tử trên toàn cầu. Bộ dữ liệu bao gồm các trò chơi điện tử đã bán được hơn 100,000 bản, được thu thập từ trang vgchartz.com.

Phân tích tập trung vào các khía cạnh sau:

- Phân tích các chỉ số thống kê cơ bản của dữ liệu
- Xác định xu hướng doanh số bán theo khu vực địa lý (Bắc Mỹ, châu Âu, Nhật Bản và các khu vực khác)
- Đánh giá sự phân bố và mối tương quan giữa các biến doanh số
- Phân tích các yếu tố ảnh hưởng đến doanh số như nhà phát hành, nền tảng, thể loại và năm phát hành
- Xử lý dữ liệu thiếu, giá trị trùng lặp và giá trị ngoại lai
- Tạo các biểu đồ trực quan để hiểu rõ hơn về dữ liệu

## 📊 Dữ Liệu

Bộ dữ liệu `vgsales.csv` bao gồm thông tin về doanh số bán trò chơi điện tử trên toàn cầu với các trường thông tin sau:

- **Rank**: Xếp hạng dựa trên doanh số bán toàn cầu
- **Name**: Tên của trò chơi
- **Platform**: Nền tảng mà trò chơi được phát hành (ví dụ: PC, PS4, etc.)
- **Year**: Năm phát hành trò chơi
- **Genre**: Thể loại trò chơi
- **Publisher**: Nhà phát hành trò chơi
- **NA_Sales**: Doanh số bán tại Bắc Mỹ (tính bằng triệu bản)
- **EU_Sales**: Doanh số bán tại châu Âu (tính bằng triệu bản)
- **JP_Sales**: Doanh số bán tại Nhật Bản (tính bằng triệu bản)
- **Other_Sales**: Doanh số bán tại các khu vực khác trên thế giới (tính bằng triệu bản)
- **Global_Sales**: Tổng doanh số bán trên toàn cầu (tính bằng triệu bản)

## 📈 Nội Dung Phân Tích

### 1️⃣ Tổng Quan Dữ Liệu

- Khám phá cấu trúc và kích thước của bộ dữ liệu (16.598 bản ghi với 11 cột)
- Tính toán dung lượng bộ nhớ sử dụng
- Xem thông tin tổng quan về dữ liệu (dòng đầu, dòng cuối, số lượng dòng và cột)
- Kiểm tra kiểu dữ liệu và phạm vi giá trị của từng cột

### 2️⃣ Phân Tích Thống Kê Cơ Bản

- **🎯 Xu hướng trung tâm**:

  - Tính toán giá trị trung bình, trung vị và mode của doanh số bán theo từng khu vực
  - So sánh chênh lệch giữa các chỉ số này để đánh giá độ lệch của phân phối
  - Phân tích tác động của giá trị ngoại lai đến các chỉ số thống kê

- **📏 Độ phân tán**:

  - Phân tích phạm vi (range) của doanh số bán (từ giá trị thấp nhất đến cao nhất)
  - Tính phương sai và độ lệch chuẩn để đánh giá mức độ phân tán dữ liệu
  - Áp dụng quy tắc thực nghiệm (Empirical Rule) để xác định phân phối dữ liệu

- **📊 Biểu đồ phân phối**:

  - Tạo biểu đồ histogram để trực quan hóa phân phối doanh số bán
  - Phân tích biểu đồ hộp (boxplot) để xác định các giá trị ngoại lai
  - Nghiên cứu độ lệch (skewness) của phân phối doanh số

- **📦 Phân vị và IQR**:
  - Tính toán các tứ phân vị (Q1, Q2, Q3) và khoảng tứ phân vị (IQR)
  - Sử dụng IQR để xác định ngưỡng phát hiện giá trị ngoại lai

### 3️⃣ Phân Tích Doanh Số Bán Theo Khu Vực

- So sánh chi tiết doanh số giữa các khu vực: Bắc Mỹ, châu Âu, Nhật Bản và các khu vực khác
- Phân tích tỷ lệ đóng góp của từng khu vực vào doanh số toàn cầu
- Xác định khu vực có doanh số bán cao nhất (Bắc Mỹ chiếm tỷ trọng lớn nhất)
- Đánh giá sự chênh lệch doanh số giữa các khu vực thông qua biểu đồ

### 4️⃣ Phân Tích Theo Thời Gian 📅

- Phân tích xu hướng phát hành trò chơi qua các năm
- Đánh giá sự thay đổi về doanh số bán theo thời gian
- Xác định các năm có doanh số cao nhất và thấp nhất
- Phân tích chi tiết doanh số bán cho một số năm cụ thể (như năm 2009)

### 5️⃣ Phân Tích Theo Nền Tảng, Thể Loại và Nhà Phát Hành 🎲

- Xác định các nền tảng phổ biến nhất và doanh số tương ứng
- Phân tích thị phần của từng thể loại trò chơi
- Đánh giá hiệu suất của các nhà phát hành lớn như Nintendo, Electronic Arts...
- Xác định các tổ hợp nền tảng-thể loại-nhà phát hành có doanh số cao nhất

### 6️⃣ Xử Lý Dữ Liệu 🧹

- Xử lý giá trị thiếu (missing values) trong cột Year và Publisher
- Xử lý các bản ghi trùng lặp với nhiều phương pháp khác nhau
- Phát hiện và xử lý giá trị ngoại lai (outliers) bằng phương pháp IQR và phân vị

### 7️⃣ Phân Tích Đa Biến 🔍

- Phân tích tương quan giữa doanh số các khu vực (NA_Sales, EU_Sales, JP_Sales, Other_Sales)
- Sử dụng ma trận tương quan và biểu đồ scatter plot để đánh giá mối quan hệ
- Thực hiện kỹ thuật tạo đặc trưng để tạo biến Average_Sales_Region

## 🛠️ Cách Sử Dụng

### 📋 Yêu Cầu

- Python 3.x
- Các thư viện Python: pandas, plotly.express, seaborn, matplotlib, numpy

### 🔧 Cài Đặt Môi Trường

```bash
pip install pandas plotly seaborn matplotlib numpy
```

### ▶️ Chạy Notebook

1. Clone hoặc tải xuống repository này
2. Đảm bảo file `vgsales.csv` nằm trong cùng thư mục với notebook `EDA.ipynb`
3. Mở và chạy notebook `EDA.ipynb` bằng Jupyter Notebook hoặc VSCode
4. Chạy các cell theo thứ tự từ trên xuống để xem kết quả phân tích

## 📝 Kết Luận Chính

### 🌎 Doanh Số Bán Theo Khu Vực

1. Doanh số bán tại Bắc Mỹ thường cao nhất so với các khu vực khác, với giá trị trung bình gấp đôi châu Âu
2. Giá trị trung bình của doanh số tại Bắc Mỹ (NA_Sales) là khoảng 0.26 triệu đơn vị, trong khi giá trị trung vị chỉ là 0.08 triệu, cho thấy phân phối có độ lệch phải mạnh
3. Thị trường Nhật Bản có xu hướng tiêu thụ khác biệt so với các thị trường phương Tây, thể hiện qua sự khác biệt trong thể loại game phổ biến

### 📊 Phân Phối Dữ Liệu

4. Phân phối doanh số bán có độ lệch dương mạnh (right-skewed), với hầu hết các trò chơi có doanh số thấp và chỉ một số ít có doanh số rất cao
5. Khoảng 98.95% dữ liệu nằm trong phạm vi 3 độ lệch chuẩn từ giá trị trung bình, phù hợp với quy tắc thực nghiệm (Empirical Rule)
6. Có sự chênh lệch đáng kể giữa các giá trị trung bình, trung vị và mode trong tất cả các khu vực, cho thấy sự phân tán lớn trong dữ liệu

### 📅 Xu Hướng Theo Thời Gian

7. Số lượng trò chơi phát hành đã tăng đáng kể theo thời gian, với đỉnh điểm trong khoảng những năm 2000s và 2010s
8. Có một tương quan âm nhẹ giữa năm phát hành và doanh số bán, cho thấy các trò chơi cũ có xu hướng có doanh số cao hơn (có thể do thời gian bán lâu hơn)

### 🎮 Thể Loại và Nhà Phát Hành

9. Nintendo là nhà phát hành chiếm vị trí dẫn đầu với nhiều trò chơi có doanh số cao nhất
10. Thể loại Action, Sports và Platform là những thể loại phổ biến nhất với doanh số cao
11. Phân tích tương quan cho thấy mối liên hệ mạnh giữa doanh số tại Bắc Mỹ và châu Âu (r = 0.77), nhưng yếu hơn giữa các khu vực khác

### 🧹 Xử Lý Dữ Liệu

12. Bộ dữ liệu có một số giá trị thiếu trong cột Year và Publisher, đã được xử lý bằng cách điền giá trị phổ biến nhất
13. Có một số bản ghi trùng lặp dựa trên các tiêu chí khác nhau, đã được xử lý để đảm bảo tính chính xác của phân tích

## 📂 Cấu Trúc Dự Án

```
└── EDA/
    ├── EDA.ipynb         # Jupyter notebook chứa tất cả phân tích
    ├── vgsales.csv       # Dữ liệu gốc về doanh số bán game
    └── README.md         # Tài liệu mô tả dự án
```

## 🔬 Phương Pháp Phân Tích

### 🔍 Phương pháp xử lý dữ liệu thiếu

1. **Loại bỏ hoàn toàn**: Đối với các phân tích không chấp nhận giá trị null
2. **Thay thế bằng giá trị phổ biến nhất**: Sử dụng mode() để tìm giá trị phổ biến nhất và điền vào các ô trống
3. **Phân tích trước và sau khi xử lý**: So sánh kết quả để đảm bảo việc xử lý không làm sai lệch phân tích

### 📉 Phương pháp xử lý giá trị ngoại lai

1. **Phương pháp IQR**: Sử dụng công thức Q1 - 1.5*IQR và Q3 + 1.5*IQR để xác định ngưỡng
2. **Phương pháp phân vị**: Cắt giảm các giá trị cao hơn phân vị thứ 80
3. **Quy tắc thực nghiệm (Empirical Rule)**: Kiểm tra phần trăm dữ liệu nằm trong khoảng ±3 độ lệch chuẩn

## 📊 Công Cụ Trực Quan Hóa

- **📊 Histogram**: Phân tích phân phối của doanh số bán và năm phát hành
- **📦 Boxplot**: Phát hiện giá trị ngoại lai và so sánh phân phối giữa các khu vực
- **🔢 Scatter Plot**: Phân tích mối tương quan giữa doanh số ở các khu vực khác nhau
- **📊 Biểu đồ cột**: So sánh số lượng trò chơi theo thể loại và nhóm doanh số
- **🔄 Ma trận tương quan**: Đánh giá mức độ tương quan giữa các biến doanh số

## 🔗 Nguồn Dữ Liệu

Dữ liệu được lấy từ Kaggle: https://www.kaggle.com/code/upadorprofzs/eda-video-game-sales/data
Nguồn gốc: vgchartz.com - Trang web chuyên theo dõi và phân tích doanh số ngành công nghiệp game
