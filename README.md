**Ứng dụng CNN và trích xuất điểm mốc khuôn mặt trong phát hiện deepfake**

**Giới thiệu**

Dự án này tập trung vào việc phát hiện hình ảnh **Deepfake** bằng cách kết hợp giữa **mạng nơ-ron tích chập (CNN)** và **thông tin điểm mốc khuôn mặt**. Việc kết hợp đặc trưng hình học (như vị trí mắt, mũi, miệng...) với đặc trưng ảnh giúp mô hình học hiệu quả hơn và tăng độ chính xác trong phát hiện khuôn mặt bị giả mạo.

**Lý do thực hiện**

Deepfake đang là mối đe dọa lớn đối với sự xác thực trong truyền thông và dữ liệu số. Các mô hình CNN truyền thống có thể gặp khó khăn khi phân biệt ảnh giả có chất lượng cao. Việc tích hợp điểm mốc khuôn mặt sẽ bổ sung thông tin cấu trúc, giúp cải thiện hiệu năng mô hình.

**Các công việc thực hiện**
- 📁 Huấn luyện trên bộ dữ liệu [140k Real and Fake Faces](https://www.kaggle.com/datasets/xhlulu/140k-real-and-fake-faces)
- Trích xuất điểm mốc khuôn mặt bằng `dlib` hoặc `MediaPipe`
- Kết hợp ảnh gốc với thông tin hình học từ điểm mốc làm đầu vào cho CNN
- Áp dụng với các mô hình CNN cơ bản, MobileNetV2, DenseNet121
- Đánh giá mô hình bằng các chỉ số: Accuracy, F1-score, ma trận nhầm lẫn, Precision, Recall

  
**Hướng phát triển**

- Áp dụng cho video Deepfake, không chỉ ảnh tĩnh
- Tối ưu hóa mô hình để chạy trên thiết bị di động
- Kết hợp thêm kỹ thuật Attention hoặc Transformer
