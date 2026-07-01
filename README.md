🎟️ Hệ thống Đặt Vé (Rạp Chiếu Phim / Xe Khách)

## 📖 Giới thiệu

Đây là dự án môn **Cấu trúc Dữ liệu và Giải thuật** được xây dựng bằng **C++**.

Hệ thống mô phỏng quá trình đặt vé, hủy vé và quản lý danh sách chờ của rạp chiếu phim hoặc xe khách.

Dự án áp dụng nhiều cấu trúc dữ liệu để giải quyết các bài toán thực tế như tìm kiếm nhanh, quản lý hàng đợi ưu tiên và hoàn tác giao dịch.

---

## 🎯 Mục tiêu

- Quản lý ghế ngồi.
- Đặt vé cho khách hàng.
- Hủy vé.
- Quản lý danh sách chờ khi hết ghế.
- Tìm kiếm khách hàng nhanh.
- Thống kê doanh thu và số ghế còn trống.

---

# 🛠️ Công nghệ sử dụng

- Ngôn ngữ: C++
- IDE: Visual Studio 2022
- Chuẩn: C++17
- Console Application (CLI)

---

# 📂 Cấu trúc dữ liệu sử dụng

| Cấu trúc | Mục đích |
|----------|----------|
| BST | Lưu khách hàng và tìm kiếm nhanh theo mã hoặc tên |
| Priority Queue | Quản lý danh sách chờ (VIP, người cao tuổi,...) |
| Stack | Lưu lịch sử giao dịch để hỗ trợ hủy vé |
| Mảng 2 chiều | Quản lý sơ đồ ghế |

---

# ⚙️ Chức năng chính

## 1. Hiển thị sơ đồ ghế

- Hiển thị ghế trống.
- Hiển thị ghế đã đặt.

Ví dụ

```
      1  2  3  4  5

A    O  O  X  O  O
B    O  X  O  O  O
C    O  O  O  X  O
```

O : Ghế trống

X : Đã đặt

---

## 2. Đặt vé

Người dùng nhập:

- Mã khách hàng
- Họ tên
- Loại khách
- Ghế muốn đặt

Nếu còn ghế

→ Đặt thành công.

Nếu hết ghế

→ Tự động đưa vào Priority Queue.

---

## 3. Hủy vé

- Chọn khách cần hủy.
- Giao dịch được lưu trong Stack.
- Ghế được giải phóng.
- Nếu danh sách chờ không rỗng thì tự động cấp ghế cho người ưu tiên cao nhất.

---

## 4. Tìm kiếm khách hàng

Tìm theo:

- Mã khách
- Tên khách

Sử dụng BST.

---

## 5. Xuất danh sách khách đã đặt

Hiển thị:

- Mã khách
- Họ tên
- Ghế
- Loại khách

---

## 6. Thống kê

Hiển thị:

- Tổng số ghế
- Ghế đã đặt
- Ghế còn trống
- Doanh thu
- Số khách đang chờ

---

# 🧩 Cấu trúc chương trình

```
Project
│
├── main.cpp
├── Seat.h
├── Seat.cpp
├── Customer.h
├── Customer.cpp
├── BST.h
├── BST.cpp
├── PriorityQueue.h
├── PriorityQueue.cpp
├── Stack.h
├── Stack.cpp
├── BookingSystem.h
├── BookingSystem.cpp
└── README.md
```

---

# 🔄 Luồng hoạt động

```
Khởi động chương trình
        │
        ▼
 Hiển thị Menu
        │
        ├── Đặt vé
        │        │
        │        ├── Còn ghế → Đặt thành công
        │        │
        │        └── Hết ghế → Priority Queue
        │
        ├── Hủy vé
        │        │
        │        ├── Stack lưu lịch sử
        │        └── Cấp ghế cho người chờ
        │
        ├── Tìm khách (BST)
        │
        ├── Xuất danh sách
        │
        └── Thống kê
```

---

# 📊 Độ phức tạp

| Chức năng | Độ phức tạp |
|------------|------------|
| Đặt vé | O(log n) |
| Hủy vé | O(log n) |
| Tìm kiếm BST | O(log n) |
| Thêm Priority Queue | O(log n) |
| Pop Priority Queue | O(log n) |
| Push Stack | O(1) |
| Pop Stack | O(1) |

---

# ▶️ Cách chạy chương trình

Clone dự án

```bash
git clone https://github.com/yourusername/BookingSystem.git
```

Mở bằng Visual Studio.

Build Project.

Nhấn:

```
Ctrl + F5
```

---

# 📷 Giao diện chương trình

Ví dụ Menu

```
========== BOOKING SYSTEM ==========
1. Hien thi so do ghe
2. Dat ve
3. Huy ve
4. Tim kiem khach hang
5. Danh sach da dat
6. Thong ke
0. Thoat
====================================
```

---

# 🚀 Hướng phát triển

- Đăng nhập Admin.
- Lưu dữ liệu bằng File.
- Kết nối SQL Server.
- Giao diện WinForms.
- Thanh toán online.
- Đặt nhiều vé cùng lúc.
- Xuất hóa đơn PDF.
