# Fun-with-FashionMNIST
Testing models on FashionMNIST dataset

1. 2 convolutional + 1 pooling + Dropout(rate=0.25) cho lớp convolution thứ 2 
Kết quả trên tập test: 93.19%

2. Thử tăng thêm 1 convolution layer: 3 convolutional + 1 pooling + Dropout(rate=0.25) cho lớp convolution thứ 3. 
Kết quả trên tập test: 93.22%

3. Thử với WiderResnet(depth=28, widen factor=10). Kết quả rất cao trên tập train nhưng khi test thì không cao => Dấu hiệu overfitting.
Kết quả trên tập test: 95.33%

4. Để tránh overfitting, sử dụng thêm Dropout và augment data bằng cách sử dụng Random Erasing (tự động gán random các giá trị màu cho vùng ảnh bị xóa) .WiderResnet(depth=28, widen factor=10) + Dropout=0.2 + Random Erasing for data augmentation(probability=0.4).
Kết quả trên tập test:  96.04%

5. Vẫn còn dấu hiệu overfitting, thử augment data thêm bằng CGAN. WiderResnet(depth=28, widen factor=10) + Dropout=0.2 + Random Erasing cho data augmentation(probability=0.4) + CGAN cho data augmentation.
Kết quả trên tập test:

- Sử dụng chương trình CNN: 

Để train và xuất kết quả cuối cùng trên tập test trên mô hình gồm 2 lớp convolution: python 2_conv_layer.py 

Để train và xuất kết quả cuối cùng trên tập test trên mô hình gồm 3 lớp convolution: python 3_conv_layer.py

- Sử dụng chương trình WideResnet + Random Erasing:

Để train và xuất kết quả test theo mô hình 3: python fashionmnist.py --dataset fashionmnist --arch wrn --depth 28 --widen-factor 10

Để train và xuất kết quả test theo mô hình 4: python fashionmnist.py --dataset fashionmnist --arch wrn --depth 28 --widen-factor 10 --drop 0.2 --p 0.4

Xem thêm trong link tham khảo

- Sử dụng chương trình GAN:

python main.py --dataset fashion-mnist --gan_type CGAN --epoch 50 --batch_size 64

Link tham khảo:

https://github.com/zhunzhong07/Random-Erasing

https://github.com/hwalsuklee/tensorflow-generative-model-collections
