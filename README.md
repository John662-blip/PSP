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
## 5. Ảnh minh họa
<img width="1460" height="500" alt="image" src="https://github.com/user-attachments/assets/4696adec-0d16-4d9c-abb9-664b6de00ba8" />
<img width="1459" height="505" alt="image" src="https://github.com/user-attachments/assets/c90faa8d-73e0-472e-b5c2-2ed51c7cab98" />
<img width="1452" height="503" alt="image" src="https://github.com/user-attachments/assets/588e5f9b-a262-48a5-bea5-cc6871d1a291" />
<img width="1449" height="499" alt="image" src="https://github.com/user-attachments/assets/7db265f1-1d2c-4ecf-ab74-6e48938a8f83" />
<img width="1459" height="506" alt="image" src="https://github.com/user-attachments/assets/2a977d3a-76e6-4461-b16d-5c3cc0bc5186" />






