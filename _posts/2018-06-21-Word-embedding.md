---
layout: post
title: Word embedding
image: /img/hello_world.jpeg
tags: [computer science, exciting-stuff]
---


Biểu diễn word embedding theo mô hình skip gram (bài giảng của standford) mỗi từ đầu vào là one-hot vec sau khi nhân với ma trận (gọi là center word matrix) - hay lấy dòng của matrix này ra
ta có Vc = W*Wb sau đó nhân với 1 dòng của ouput word representation matrix rồi lấy softmax trên col vector và so sánh với groundtruth

![Crepe](/img/word-embedding/model-draw.png)

Để tính gradient descent ta chỉ cần đạo hàm (dùng chain rule) để tính

![Crepe](/img/word-embedding/gradient_1.jpg)


![Crepe](/img/word-embedding/gradient_2.jpg)

