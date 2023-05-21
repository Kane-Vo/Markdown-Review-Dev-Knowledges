# Review-Fudamentals
## Cấu trúc dữ liệu và giải thuật
  ### 1. Độ phức tạp thuật toán (Big O)

  ### 2. Sắp xếp và tìm kiếm nhị phân
    a. Sort
      * Bubble sort
      * Selection sort
      * Insertion sort
      * Quick sort
      * Heap sort

    b. Tìm kiếm nhị phân

  ### 3. Các phương pháp sinh
    * Sinh nhị phân
    * Sinh hoán vị
    * Sinh tổ hợp
    * Sinh chỉnh hợp
  ### 4. Đệ quy, quay lui

  ### 5. Cấu trúc dữ liệu stack, queue, dequeue

  ### 6. Quy hoạch động

  ### 7. Đồ thị.

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
  ### 1. MVC

    * Model
      Đây là thành phần quản lý toàn bộ các cơ sở dữ liệu (database) của ứng dụng. Đồng thời Model cũng chứa các lớp mô tả business logic và định nghĩa business rules cho dữ liệu (cách mà dữ liệu sẽ được thay đổi và sử dụng).

    * View
      View là giao diện hiển thị dành cho người dùng. Bộ phận này đại diện cho các thành phần UI (ví dụ như: XML, HTML,…) mà người dùng sẽ tương tác. View tương tác với Model thông qua Observer pattern.

    * Controller
      Controller là bộ phận có chức năng ghi nhận và điều hướng các yêu cầu (request) mà người dùng đưa ra tại View. Sau khi tiếp nhận, Controller sẽ xử lý các dữ liệu thông qua Model và cuối cùng trả kết quả, phản hồi tại View.

    ~Mô hình MVC có rất nhiều ưu điểm, cụ thể như:~

      - Nhẹ, tiết kiệm băng thông: MVC không tiêu tốn nhiều viewstate nên rất tiết kiệm băng thông. Các thao tác gửi, nhận dữ liệu được diễn ra liên tục. Vì vậy, website/ứng dụng hoạt động ổn định hơn.
      - Có thể kiểm tra, phát hiện lỗi phần mềm dễ dàng.
      - Rất tốt trong việc phân tách các phần Model và View.
      - Mô hình có kết cấu đơn giản. Dù bạn không quá am hiểu về kỹ thuật cũng có thể sử dụng được.

    ~Bên cạnh ưu điểm, MVC cũng tồn tại một số nhược điểm sau:~

      - Khó thực hiện unit test do Controller và Android API có sự liên hệ chặt chẽ với nhau.
      - Controller và View có liên quan với nhau. Do đó, khi thay đổi ở View thì đồng nghĩa bạn sẽ phải thay đổi ở Controller.
      - Theo thời gian, Controller sẽ trở nên khó kiểm soát vì càng ngày càng có nhiều code được viết thêm vào.
      - MVC chỉ thích hợp với các dự án lớn. Với các dự án nhỏ, mô hình này khá cồng kềnh và tốn nhiều thời gian trong việc trung chuyển dữ liệu.

  ### 1. MVP

  ### 1. MVVM
------------

## Cơ chế hoạt động của web
------------

## Design pattern

  ### 1. Observer pattern
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

## Bạn có thể tự hỏi, mình học gì khi học 1 ngôn ngữ mới? Đây là câu trả lời:

  * Cách khai báo hàm, biến
  * Cách khai báo vòng lặp, điều kiện if/else
  * Các kiểu cấu trúc dữ liệu: list, set, tuple, …
  * IO, multi-thread, delegate, event
  * IDE phù hợp, cách build, debug
  * Các framework, cách sử dụng, ….