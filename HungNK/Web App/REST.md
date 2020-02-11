# REST là gì

Những khái niệm đầu tiên về REST(REpresentational State Transfer) được đưa ra vào năm 2000 trong luận văn tiến sĩ của Roy Thomas Fielding (đồng sáng lập giao thức HTTP). Trong luận văn ông giới thiệu khá chi tiết về các ràng buộc, quy ước cũng như cách thức thực hiện với hệ thống để có được một hệ thống REST.

Hiểu đơn giản nó là một bộ các ràng buộc và quy ước , khi áp dụng đầy đủ vào hệ thống của bạn thì ta có 1 hệ thống REST.

## REST Contraints

- Hệ thống hoạt động theo mô hình client-server, trong đó server là tập hợp các service nhỏ lắng nghe các request từ client. Với từng request khác nhau thì có thể một hoặc nhiều service xử lý.

- Stateless (phi trạng thái). Đơn giản server và client không lưu trạng thái của nhau -> mỗi request lên server thì client phải đóng gói thông tin đầy đủ để thằng server hiểu được. Điều này giúp hệ thống của bạn dễ phát triển,bảo trì, mở rộng vì không cần tốn công CRUD trạng thái của client . Hệ thống phát triển theo hướng này có ưu điểm nhưng cũng có khuyết điểm là gia tăng lượng thông tin cần truyền tải giữa client và server.

- Khả năng caching : Các response có thể lấy ra từ cache. Bằng cách cache các response , server giảm tải việc xử lý request, còn client cũng nhận được thông tin nhanh hơn. Ở đây ta đặt 1 thằng cache vào giữa : client- cache- server.

- Chuẩn hóa các interface : Đây là một trong những đặc tính quan trọng của hệ thống REST. Bằng cách tạo ra các quy ước chuẩn để giao tiếp giữa các thành phần trong hệ thống, bạn đã đơn giản hóa việc client có thể tương tác với server. Các quy ước này áp dụng cho toàn bộ các service giúp cho người sử dụng hệ thống của bạn dễ dụng hơn. Dễ hiểu hơn trên hệ thống bạn đặt ra 1 chuẩn API để người dùng dù là mobile, web đều có thể kết nối vào được. Hệ thống REST có yếu điểm ở đây vì khi chuẩn hóa rồi ta không thế tối ưu từng kết nối.-

- Phân lớp hệ thống : trong hệ thống REST bạn chia tách các thành phần hệ thống theo từng lớp, mỗi lớp chỉ sử dụng lớp ở dưới nó và giao tiếp với lớp ở ngay trên nó mà thôi. Điều này giúp bạn giảm độ phức tạp của hệ thống,giúp các thành phần tách biệt nhau từ đó dễ dàng mở rộng từng thành phần :

![](Pictures/REST1.png)


Xem bài viết gốc tại [đây](https://techmaster.vn/posts/33627/co-gang-de-giai-thich-ve-rest)


# Ưu điểm

- Xu hướng thiết kế web service trước kia từng là SOAP, WSDL ... nhưng hiện nay đã có một phương pháp tốt hơn đó là: REST (Representation State Stranfer).

- REST làm cho ứng dụng trở nên rõ ràng hơn:

- Rõ ràng về URLs: REST URL đại diện cho resource chứ không phải là một hành động.

- Trả về với nhiều định dạng khác nhau: html, xml, rss …

- Code ngắn gọn hơn.

- Rõ ràng cho việc thiết kế ứng dụng.

- REST định nghĩa các quy tắc kiến trúc để bạn thiết kế Web services chú trọng vào tài nguyên hệ thống, bao gồm các trạng thái tài nguyên được định dạng như thế nào và được chuyển tải qua HTTP thông qua số lượng lớn người dùng và được viết bởi những ngôn ngữ khác nhau. Có một số nguyên tắc để thiết kế một ứng dụng Web Service REST:

- "thing" là ID

- Sử dụng các phương thức chuẩn

- Resource với nhiều đại diện

- Giao tiếp phi trạng thái (statelessly)

Giải thích rõ hơn tại [đây](https://viblo.asia/p/co-ban-ve-rest-l5y8Rro9Mob3)

Nguồn tham khảo :

https://www.infoq.com/articles/rest-introduction/

https://gist.github.com/khanhhd/6879483
