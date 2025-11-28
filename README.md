Các thông số về số lượng ảnh đã dược trình bày trong code.
Gồm có 134 ảnh biến Cấm rẽ trái và 64 ảnh biển Bắt buộc rẽ phải trước augmentation.



Resize: (128,128)
Normalize: rescale=1./255
RGB màu chuẩn
Augmentation: xoay, flip, brightness, shift, zoom, shear.

- Xây dựng theo mô hình CNN.
Cấu trúc: 2 Conv2D + MaxPooling → Flatten → Dense → Dropout → Output
Activation: ReLU cho hidden, Softmax cho output
Optimizer: Adam
Learning rate: mặc định 0.001
Batch size: 32
Số epoch: 20 (thử nghiệm)

Đánh giá tổng quan: Train loss giảm đều và gần về 0 → mô hình học tốt trên dữ liệu huấn luyện.
                    Val loss dao động nhiều, có vài spike lớn (ví dụ epoch 7, 9…) → mô hình chưa ổn định trên dữ liệu validation.
                    Khoảng cách giữa train loss và val loss khá lớn → có khả năng overfitting.

link gọi API: https://1a2c372f4df3ed810b.gradio.live
