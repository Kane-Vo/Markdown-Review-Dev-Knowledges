## Design pattern
  ### 1. Observer pattern
  ### 2. MVC

  * Model
    Đây là thành phần quản lý toàn bộ các cơ sở dữ liệu (database) của ứng dụng. Đồng thời Model cũng chứa các lớp mô tả business logic và định nghĩa business rules cho dữ liệu (cách mà dữ liệu sẽ được thay đổi và sử dụng).

  * View
    View là giao diện hiển thị dành cho người dùng. Bộ phận này đại diện cho các thành phần UI (ví dụ như: XML, HTML,…) mà người dùng sẽ tương tác. View tương tác với Model thông qua Observer pattern.

  * Controller
    Controller là bộ phận có chức năng ghi nhận và điều hướng các yêu cầu (request) mà người dùng đưa ra tại View. Sau khi tiếp nhận, Controller sẽ xử lý các dữ liệu thông qua Model và cuối cùng trả kết quả, phản hồi tại View.

  **Mô hình MVC có rất nhiều ưu điểm, cụ thể như:**

  - Nhẹ, tiết kiệm băng thông: MVC không tiêu tốn nhiều viewstate nên rất tiết kiệm băng thông. Các thao tác gửi, nhận dữ liệu được diễn ra liên tục. Vì vậy, website/ứng dụng hoạt động ổn định hơn.
  - Có thể kiểm tra, phát hiện lỗi phần mềm dễ dàng.
  - Rất tốt trong việc phân tách các phần Model và View.
  - Mô hình có kết cấu đơn giản. Dù bạn không quá am hiểu về kỹ thuật cũng có thể sử dụng được.

  **Bên cạnh ưu điểm, MVC cũng tồn tại một số nhược điểm sau:**

  - Khó thực hiện unit test do Controller và Android API có sự liên hệ chặt chẽ với nhau.
  - Controller và View có liên quan với nhau. Do đó, khi thay đổi ở View thì đồng nghĩa bạn sẽ phải thay đổi ở Controller.
  - Theo thời gian, Controller sẽ trở nên khó kiểm soát vì càng ngày càng có nhiều code được viết thêm vào.
  - MVC chỉ thích hợp với các dự án lớn. Với các dự án nhỏ, mô hình này khá cồng kềnh và tốn nhiều thời gian trong việc trung chuyển dữ liệu.

  ### 1. MVP

  ### 1. MVVM
