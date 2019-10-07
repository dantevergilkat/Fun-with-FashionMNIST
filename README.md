# Fun-with-FashionMNIST
Testing models on FashionMNIST dataset

1. 2 l?p convolution + 1 l?p pooling + Dropout(rate=0.25) cho l?p convolution th? 2. 
K?t qu? trên t?p test: 93.19%

2. 3 l?p convolution + 1 l?p pooling + Dropout(rate=0.25) cho l?p convolution th? 3. 
K?t qu? trên t?p test: 93.22%

3. WiderResnet(depth=28, widen factor=10). 
K?t qu? trên t?p test: 95.33%

4. WiderResnet(depth=28, widen factor=10) + Dropout=0.2 + Random Erasing cho data augmentation(probability=0.4).
K?t qu? trên t?p test:  

5. WiderResnet(depth=28, widen factor=10) + Dropout=0.2 + Random Erasing cho data augmentation(probability=0.4) + CGAN cho data augmentation.
K?t qu? trên t?p test:

