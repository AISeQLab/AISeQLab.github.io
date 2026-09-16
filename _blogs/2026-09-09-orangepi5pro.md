---
layout: post
title: "Cách setup cluster Orange Pi 5 Pro"
categories: cryptography
---

Dụng cụ chuẩn bị:

- Orange Pi 5 Pro có emmC
- Cáp USB-B 3.0 to USB 3.0 (important!): cáp cùi hơn không nhận
- Host PC có cổng USB-B 3.0

B1. Nạp bitloader và tải img os
- Cài rkdeveloptool thông qua terminal
- Trên Pi, cắm sẵn vào USB-B 3.0, Ethernet, HDMI và bàn phím. Nhấn giữ nút MaskROM bên cạnh nút nguồn => Cắm nguồn => Nhấn giữ thêm 2-3 giây nút MaskROM để PC nhận diện được ngoại vi. Gõ lại rkdevelopertool -ld => Thấy có xuất hiện maskROM thì thành công
- Tải đúng loader cho chip RK, sau dó tải thêm image từ trang chủ orangepi.org, sau đó tải ver Desktop (nếu muốn có giao diện) hoặc ver Server (chỉ có terminal, nhưng nhẹ hơn)


B2. Cài tailscale

curl -fsSL https://tailscale.com/install.sh | sh

sudo tailscale up (Hiện lên link đăng nhập, gõ tay link đó vào PC khác, select cùng tailnet)

sudo systemctl enable tailscaled

sudo systemctl start tailscaled

B3. Add new user

User mặc định của PI sẽ là orangepi / orangepi

Add thêm user mới với full quyền

sudo adduser ten_user_full_quyen

sudo usermod -aG sudo ten_user_full_quyen


