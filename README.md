# Review-Fudamentals
## Cấu trúc dữ liệu và giải thuật

------------
## OOP
  ### 1. Các tính chất
    1. Tính trừu tượng
    2. Tính đa hình
    3. Tính đóng gói
    4. Tính kế thừa
## Vòng lặp
------------

## Đệ quy
------------

## Callback
------------

## 1 số mô hình phát triển ứng dụng
------------

## Cơ chế hoạt động của web
------------

## Design pattern
------------

## Các principle cần lưu ý
------------

### 1. SOLID

* Single responsibility principle

Mỗi một class chỉ xử lí 1 vấn đề. Dễ debug và maintain hệ thống.
Dễ triển khai hơn khi có auto check.
Áp dụng cho class, function, components và micro services

* Open-Closed principle

không sửa code của 1 class khi class đã hoàn thiện, nếu cần mở rộng tính năng thì thông qua kế thừa hoặc interface

* Liskov Substitution Principle

không được thay đổi tính đúng đắn của 1 class cha khi kế thừa

* Interface Segregation Principle

không nên xây dựng 1 interface lớn, nên tách ra thành nhiều interface nhỏ

* Dependency Inversion Principle

cấp cha không phụ thuộc cấp con, 
các class giao tiếp với nhau thông qua interface


### 2. ACID

* Atomicity

Atomicity có thể hiểu là tính nguyên tử. Điều này có nghĩa là mọi thay đổi về dữ liệu phải đảm bảo trọn vẹn, nếu các tiến trình thực hiện thành công hoặc là sẽ không có bất kỳ sự thay đổi nào về dữ liệu nếu có sự cố tiến trình xảy ra.


* Consistency

Thuộc tính Consistency yêu cầu tính nhất quán dữ liệu cho database. Khi có một Transaction được hoàn thành, tất cả dữ liệu phải được bảo toàn các mối liên kết dù cho tiến trình thao tác thành công hay thất bại.


* Isolation

Isolation là thuộc tính nói về tính độc lập của các Transaction khi thực thi đồng thời trên hệ thống. Nếu cùng một lúc, có nhiều tiến trình cùng diễn ra thì cần một cơ chế đưa ra để bảo đảm rằng các tiến trình này có thể hoạt động song song mà không ảnh hưởng đến nhau. 

* Durability

Thuộc tính này đưa ra để đảm bảo rằng khi các Transaction diễn ra thành công thì tác dụng nó tạo ra với cơ sở dữ liệu phải bền vững. Dù hệ thống có xảy ra bất kỳ lỗi gì thì dữ liệu luôn được khôi phục lại nguyên trạng.

Ví dụ, đối với các tiến trình giao dịch tiền qua ngân hàng. Khi các Transaction hoàn tất, dữ liệu sẽ được ghi lại dưới dạng đĩa cứng, các giao dịch cũng được ghi chép lại. Nếu có bất kỳ sự cố nào xảy ra đều có thể dễ dàng backup lại data.


