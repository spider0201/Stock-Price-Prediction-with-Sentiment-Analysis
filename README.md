# Stock Price Prediction with Sentiment Analysis

## Mô tả
Dự án này dự báo giá cổ phiếu sử dụng các mô hình LSTM, TimesNet, ARIMA kết hợp với dữ liệu cảm xúc (sentiment) từ tin tức và bình luận.

## Yêu cầu hệ thống

- Python >= 3.8
- pip (Python package manager)
- Trình duyệt Chrome (nếu crawl dữ liệu với Selenium)
- ChromeDriver phù hợp với phiên bản Chrome

## Cài đặt

1. **Clone hoặc tải mã nguồn về máy:**

   ```
   git clone https://github.com/spider0201/Stock-Price-Prediction-with-Sentiment-Analysis.git
   cd <thư-mục-dự-án>
   ```

2. **Tạo môi trường ảo (khuyến nghị):**

   ```
   python -m venv venv
   venv\Scripts\activate
   ```

3. **Cài đặt các thư viện cần thiết:**

   ```
   pip install -r requirements.txt
   ```

4. **Cài đặt ChromeDriver (nếu crawl dữ liệu):**
   - Tải về tại: https://chromedriver.chromium.org/downloads
   - Đảm bảo chromedriver.exe nằm trong PATH hoặc cùng thư mục với mã nguồn.

## Hướng dẫn chạy chương trình
Note:
- Thư mục crawl_data (Dùng để crawl dữ liệu nếu bạn muốn crawl mới và chạy thử yêu cần có Selenium và Chromedriver)
- Thư mục model (gồm 2 file bao gồm model - dự báo đơn biến và model + SA - là dự báo đa biến gồm cả biến sentiment_score)
- Thư mục sentiment_analysis (file data_processing.ipynb dùng để tiền xử lý dữ liệu văn bản, bài báo đưa qua mô hình phoBert để chấm điểm score)

### 1. Crawl dữ liệu tin tức

- Mở file `crawl_data_news.ipynb`.
- Chạy từng cell để thu thập dữ liệu tin tức từ CafeF. (có thể dẫn đến treo vì mỗi lần chạy nó load lại trang để lấy tin tức)

### 2. Tiền xử lý dữ liệu

- Mở file `data_preprocess.ipynb` bằng Jupyter Notebook hoặc VSCode.
- Chạy tuần tự các cell để xử lý dữ liệu đầu vào.

### 3. Huấn luyện và đánh giá mô hình

- Mở các file:
  - `model.ipynb` (dự báo giá cổ phiếu với LSTM, TimesNet, ARIMA)
  - `model+SA.ipynb` (dự báo kết hợp điểm sentiment)
- Chạy tuần tự các cell để huấn luyện và đánh giá mô hình.
- Lưu ý sau khi chạy data_process.ipynb thì sẽ sinh ra file dữ liệu gộp để chạy mô hình và dùng nó để chạy model.
### 4. Kết quả

- Kết quả dự báo, các chỉ số đánh giá và biểu đồ sẽ được hiển thị trực tiếp trong notebook.

## Lưu ý

- Đảm bảo các file dữ liệu `sentiment_score.csv` đã có sẵn trong thư mục dự án hoặc cập nhật đường dẫn phù hợp.
- Nếu gặp lỗi thiếu thư viện, hãy kiểm tra lại file `requirements.txt` và cài đặt bổ sung nếu cần.

## Liên hệ

- Tác giả: Nguyễn Đình Lập
- Email: lapthptym0201@gmail.com