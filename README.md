# PSP: Person Sketch-to-Photo Synthesis

## 1. Giới thiệu

Đồ án này triển khai **Person Sketch-to-Photo Synthesis (PSP)**, tức là **chuyển phác thảo khuôn mặt sang ảnh thực**.  
- **Dataset**: Person Face Sketches  
- **Mục tiêu**: Sinh ảnh chân thực từ phác thảo, giữ được cấu trúc gương mặt và các đặc trưng nhận diện.

---

## 2. Dataset

- **Tên**: Person Face Sketches  
- **Đặc điểm**: Mỗi cá nhân có **phác thảo và ảnh thực** tương ứng.  
- **Tiền xử lý**: Resize về 128×128, normalize về [-1,1].

---

## 3. Mô hình

- **Kiến trúc**: PSP sử dụng Gen của StyleGAN + pixel2style2pixel encoder để map sketch sang không gian style.  
- **Input**: Sketch (phác thảo)  
- **Output**: Generated photo (ảnh tổng hợp)  
- **Optimizer**: Adam  
- **Learning rate**: 0.0001

---

## 4. Đánh giá chất lượng

Mô hình được đánh giá bằng các metric tiêu chuẩn:

| Metric      | Giá trị   |
|------------|----------|
| **FID**    | 51.2085 | 
| **SSIM**   | 0.4235  | 
| **LPIPS**  | 0.3160  | 


<img width="1162" height="6390" alt="tải xuống (1)" src="https://github.com/user-attachments/assets/4df48cf7-73d0-4ac9-bc0b-6764ade9c5fe" />

