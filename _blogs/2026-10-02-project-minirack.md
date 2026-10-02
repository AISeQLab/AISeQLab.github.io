---
layout: post
title: "Project mini-rack"
categories: hardware
---

Từ lúc hết hè đến nay cũng rảnh rỗi, tôi ở nhà lướt video YTB thì thấy được video này.

<!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/y1GCIwLm3is?si=3t2HB9zN72ONhW-c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> -->

Thế là bị sa vào cơn nghiện chế tạo minirack, vừa hay trên khoa đang có một đống thiết bị để ngổn ngang, bắt tay vào làm thôi :v

<img src="..//images/blogs/Rack/r7.jpg" alt="Introduction" style="width:100%;" />

Ý định ban đầu là làm quả 10-inch mini-rack như thế này, chỉ tầm 10-12U.

<img src="..//images/blogs/Rack/refer.jpg" alt="Introduction" style="width:100%;" />

Nhưng sau khi tham khảo nguyên liệu thì nguyên quả khung đã làm tôi khóc thét. Có hai option, một là in 3D toàn bộ (nhưng tôi nghĩ là nó không gánh nổi tải), hai là mua đồ có sẵn của Deskpi Rackmate, nhưng nhìn quả này xem.

<img src="..//images/blogs/Rack/deskpi.png" alt="Introduction" style="width:100%;" />

Nguyên khung lỏ 6U đã có giá 100$, không những thế ở VN không có phân phối chính hãng, phải thông qua xách tay nên giá có thể bị đội lên 20-30%, option này quá là không kinh tế.

Do đó, tôi đã lên kế hoạch để biến từ một đống sắt vụn thành khung rack. Tất cả nguyên vật liệu đều được mua trên sàn cam.

### 1. Khung

Để chế mini-rack tiết kiệm nhất thì mình chọn loại open-rack, nôm na là không có thêm lớp bên ngoài để chống bụi, mà chỉ trơ chọi khung.

Tôi thích phương án này: sử dụng nhôm định hình 2020 để làm khung (12 thanh), sau đó bắt thanh V lỗ để làm khung phụ bên trong, tuy nhiên giá nhôm khá đắt, nên để cắt giảm thêm nữa tôi chỉ dùng 4 thanh V lỗ (vì lần đầu làm nên tôi chọn kích thước vừa vừa là 12U, project kế thì có thể chọn dài hơn).

<img src="..//images/blogs/Rack/vlo.jpg" alt="Introduction" style="width:100%;" />

Thanh V lỗ này (2 x 2) sẽ có một mặt full lỗ vuông để bắt ecu M6 và một mặt lỗ tròn M6 nhưng thưa hơn, chúng ta sẽ có mặt lỗ vuông hướng chính diện và lỗ tròn cạnh bên.

Để cố định thì có nhiều option, tôi sử dụng mâm trên dưới. Mâm tôi mua có D400 mm, cái này hơi thiếu kinh nghiệm vì xài mâm cùng Depth thì tầng trên sẽ không liên thông tới tầng dưới được. Tốt hơn thì nên xài thanh ngang trước.

Ngoài ra tôi mua thêm ở shop này mấy panel để giằng trước sau.

<img src="..//images/blogs/Rack/mam.jpg" alt="Introduction" style="width:100%;" />

Sau khi sử dụng 4 thanh V, 3 mâm và một số panel thành quả sẽ như thế này. Hình này là tôi đang ướm thử các thiết bị lên xem để hkông gian chứa không.

<img src="..//images/blogs/Rack/r6.jpg" alt="Introduction" style="width:100%;" />

### 2. Nguồn

Phần kế là nguồn, sau khi tìm hiểu một thời gian thì tôi chọn thanh PDU này, giá thành và công năng vừa phải, các bác lưu ý phần công suất và CB. 

<img src="..//images/blogs/Rack/PDU.jpg" alt="Introduction" style="width:100%;" />

Tuy nhiên PDU này khá ít ổ cắm nên tôi độ thêm 3 cái ổ điện 6 lỗ DELI. Tổng dây out chỉ có 1, dĩ nhiên là các bác có thể mua PDU có số ổ cắm nhiều hơn, tuy nhiên P/P sẽ thấp hơn so với kiểu này.

<img src="..//images/blogs/Rack/r5.jpg" alt="Introduction" style="width:100%;" />

PDU có tai bắt nên sẽ được gắn vào mặt sau (hoặc hông cũng được), còn 3 ổ cắm thì tôi quyết định để vào mặt hông để dễ đi dây, nhưng lúc sau đổi lại thành mặt sau luôn.

Để dây không bị cong khi gấp đoạn thì các bác có thể mua mấy connector như thế này. Vì đầu con Pi của tôi vuông góc, nên nếu cứ đấu dây nguồn vào thì không xếp gọn gần nhau được (xếp chồng thì quạt top trên pi lại bị che).

<img src="..//images/blogs/Rack/op.jpg" alt="Introduction" style="width:100%;" />

<img src="..//images/blogs/Rack/r1.jpg" alt="Introduction" style="width:100%;" />

Đi dây nguồn (+ dây mạng) là một nghệ thuật, lý tưởng nhất là ta đi dây dọc theo khung (khung sẽ giấu dây dùm), dây đi vào không gian trong tủ rack sẽ phải là minimum về length

<img src="..//images/blogs/Rack/r4.jpg" alt="Introduction" style="width:100%;" />