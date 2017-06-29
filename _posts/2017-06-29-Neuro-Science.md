---
layout: post
title: Neuro science part 1
image: /img/hello_world.jpeg
tags: [Neuro-science, exciting-stuff]
---


Mục tiêu giải thích cách não tạo ra hành vi.

Theo P.Dayan và L. Abbott: là công cụ và phương thức giúp mô tả những gì hệ thần kinh làm, đánh giá chức năng và hiểu cách tại sao nó hoạt động theo 1 cách cụ thể.
Descriptive Model(What) – Mechanistic Model (How) – Interpretive Model (Why).
Receptive Field (Vùng thụ cảm): đặc trưng cụ thể của 1 vùng giác quan kích thích mà tạo ra tín hiệu manh từ cell.
ví dụ: điểm sáng mà bật lên tại 1 vùng đặc trưng trên retina (võng mạc).
Thanh ánh sáng mà bật lên tại vùng đặc trưng có hướng trên võng mạc.

![Crepe](/img/neuro-science-1/retina-1.jpg)

Mô hình của RF: ví dụ như trên võng mạc con người ảnh cây bút sẽ lật ngc và in lên màng võng mạc ở đây các cell trên retinal sẽ convert và đưa về vùng xử lý khác từng cell này chỉ phản ứng khi có thông tin tại 1 vị trí cố đinh của nó (nếu nằm ngoài cell sẽ không phản ứng).

![Crepe](/img/neuro-science-1/retina-2.jpg)

LGN: vùng trung gian giữa đường truyền dữ liệu từ retina-> V1.
Primary Visual Cortex:1 vùng ở vỏ não.

![Crepe](/img/neuro-science-1/retina-3.jpg)
![Crepe](/img/neuro-science-1/retina-4.jpg)

Oriented RF:
![Crepe](/img/neuro-science-1/retina-5.jpg)

Khi di chuyển từ LGN -> V1 cell ở LGN có dạng center-surrounded và V1 có oriented RF.
Nhiều cell ở LGN là input cho 1 cell ở V1.

![Crepe](/img/neuro-science-1/retina-6.jpg)

và đây là cách RF ở V1 được tạo nên (nhiều cells ở LGN xếp thành 1 cell ở V1)

![Crepe](/img/neuro-science-1/retina-7.jpg)

Tại sao RF ở V1 lại form theo hình dạng như v:
Cách hình thành như vậy có lợi ích gì.
Giả sử mục tiêu là biểu diễn ảnh 1 cách chân thực và hiệu quả nhất sử dụng các RF của V1 như trên.  Cho ảnh I ta dựng lại I bằng các RF như sau : I’= sum(Rf(i) * w(i)). w(i) là weight của RF thứ i.

![Crepe](/img/neuro-science-1/retina-8.jpg)

vậy thì RF(i) phải như thế nào để tổng bình phương lỗi  giữa I và I’ minimized và càng độc lập nhất.
Ta sẽ test trên nhưng bức ảnh ngẫu nhiên và chọn RF(i) ngẫu nhiêu sau đó chay efficient coding(sparse coding, ICA, predictive coding) algo trên những phần của ảnh.
Kết quả:

![Crepe](/img/neuro-science-1/retina-9.jpg)

khớp với những gì ta dự đoán. Não bộ cố gắng tối ưu việc biễu diễn ảnh bằng cách tạo ra RF có hình dạng như ta đã thấy.