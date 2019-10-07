# Fun-with-FashionMNIST
Testing models on FashionMNIST dataset

1. 2 convolutional + 1 pooling + Dropout(rate=0.25) cho lop convolution thu 2 
Ket qua trên tap test: 93.19%

2. 3 convolutional + 1 lop pooling + Dropout(rate=0.25) cho lop convolution thu 3. 
Ket qua trên tap test: 93.22%

3. WiderResnet(depth=28, widen factor=10). 
Ket qua trên tap test: 95.33%

4. WiderResnet(depth=28, widen factor=10) + Dropout=0.2 + Random Erasing cho data augmentation(probability=0.4).
Ket qua trên tap test:  96.04%

5. WiderResnet(depth=28, widen factor=10) + Dropout=0.2 + Random Erasing cho data augmentation(probability=0.4) + CGAN cho data augmentation.
Ket qua trên tap test:

