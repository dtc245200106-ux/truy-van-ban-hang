# Bài thực hành: Truy vấn CSDL Quản Lý Bán Hàng

## 📋 Thông tin
- **Database:** QuanLyBanHang
- **Công cụ:** MySQL Workbench
- **Số lượng truy vấn:** 4

## 📝 Dữ liệu đã thêm

### Customer (3 bản ghi)
| cID | cName | cAge |
|-----|-------|------|
| 1 | Minh Quan | 10 |
| 2 | Ngoc Oanh | 20 |
| 3 | Hong Ha | 50 |

### Product (5 bản ghi)
| pID | pName | pPrice |
|-----|-------|--------|
| 1 | May Giat | 3 |
| 2 | Tu Lanh | 5 |
| 3 | Dieu Hoa | 7 |
| 4 | Quat | 1 |
| 5 | Bep Dien | 2 |

### Order (3 bản ghi)
| oID | cID | oDate | oTotalPrice |
|-----|-----|-------|-------------|
| 1 | 1 | 2006-03-21 | NULL |
| 2 | 2 | 2006-03-23 | NULL |
| 3 | 1 | 2006-03-16 | NULL |

### OrderDetail (7 bản ghi)
| oID | pID | odQTY |
|-----|-----|-------|
| 1 | 1 | 3 |
| 1 | 3 | 7 |
| 1 | 4 | 2 |
| 2 | 1 | 1 |
| 3 | 1 | 8 |
| 2 | 5 | 4 |
| 2 | 3 | 3 |

## 📊 Kết quả truy vấn

### Truy vấn 1: Tất cả hóa đơn
| oID | oDate | oTotalPrice |
|-----|-------|-------------|
| 1 | 2006-03-21 | NULL |
| 2 | 2006-03-23 | NULL |
| 3 | 2006-03-16 | NULL |

### Truy vấn 2: Khách hàng + sản phẩm
| cID | CustomerName | ProductName | Quantity |
|-----|--------------|-------------|----------|
| 1 | Minh Quan | May Giat | 3 |
| 1 | Minh Quan | Dieu Hoa | 7 |
| 1 | Minh Quan | Quat | 2 |
| 1 | Minh Quan | May Giat | 8 |
| 2 | Ngoc Oanh | May Giat | 1 |
| 2 | Ngoc Oanh | Bep Dien | 4 |
| 2 | Ngoc Oanh | Dieu Hoa | 3 |

### Truy vấn 3: Khách hàng không mua
| cID | cName |
|-----|-------|
| 3 | Hong Ha |

### Truy vấn 4: Giá tiền từng hóa đơn
| OrderID | OrderDate | TotalPrice |
|---------|-----------|------------|
| 1 | 2006-03-21 | 68 |
| 2 | 2006-03-23 | 36 |
| 3 | 2006-03-16 | 24 |

## 📸 Ảnh minh chứng
- query-1.png
- query-2.png
- query-3.png
- query-4.png