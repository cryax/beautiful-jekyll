---
layout: post
title: Neuro science part 2
image: /img/hello_world.jpeg
tags: [Neuro-science, exciting-stuff]
use_math: true
---
# Mechanistic Model (show how a neural system goes about accomplishing a particular func)
Các cell ở LGN khác với cell ở V1
và ta thắc mắc là làm sao các oriented RF có được từ các center-sourround RF 

![Crepe](/img/neuro-science-1/rf-1.jpg)

Một loạt các cell ở LGN hội tụ lại đến 1 cell ở V1.
1 cell ở V1 nhận input từ nhiều cell ở LGN câu hỏi tiếp theo là làm sao input của cell ở LGN đi đến RF ở V1
có hình dạng khác nhau như vậy.

![Crepe](/img/neuro-science-1/rf-2.jpg)

Câu trả lời khác đơn giản chỉ cần sắp xếp các RF theo 1 thứ tự sau đó feed-foward hoặc converge thì nó sẽ biểu hiện tương tự
1 cell ở V1 như hình. Mô hình này gây tranh cãi vì bản thân các V1 cell có các connect vòng cho nó và đến các V1 cell khác mà mô hình của 2 tác giả không xét đến. Ta sẽ bàn đến sau này vấn đề này.

# Interpeter Model (Giải thích cách hoạt động, tại sao chúng lại được tạo nên như vậy)
Ta đến với phần giải thích tạo sao RF ở V1 lại có hình dáng như vậy

![Crepe](/img/neuro-science-1/rf-3.jpg)

![Crepe](/img/neuro-science-1/rf-4.jpg)

Hay câu hỏi là hình dáng như vậy thì có lợi gì cho tính toán.
Theo giả thuyết hiệu quả tính toán thì mục tiêu là làm sao biểu diễn lại hình ảnh cách chân thật và hiệu quả nhất mà sử dụng các RF ở V1: RF1, RF2, RF3,...

Giả sử có ảnh I và ảnh biểu diễn lại là hat{I} với hat{I} = \sum_{i}RF_i r_i (với r_1 r_2 là neural responses - weights)
Vậy thì RF_i ở đây như thế nào để minimize lỗi từng pixel giữa I và hat{I}

Để kiểm tra ta sẽ dùng các RF_i random và chạy efficient coding algorithm trên các vùng nhỏ (các ô vuông) của ảnh tự nhiên.
Các kĩ thuật liệt kê bên dưới cùng tên của tác giả.

![Crepe](/img/neuro-science-1/rf-5.jpg)

và sau đây là RF sau khi được điều chỉnh bởi các thuật toán:

![Crepe](/img/neuro-science-1/rf-6.jpg)

Kết luận là não bộ đang có gắng biểu diễn lại hình ảnh 1 cách hiệu quả và chân thực nhất
