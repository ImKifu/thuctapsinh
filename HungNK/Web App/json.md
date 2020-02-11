# JSON là gì?

JSON là viết tắt của JavaScript Object Notation, là một kiểu định dạng dữ liệu tuân theo một quy luật nhất định mà hầu hết các ngôn ngữ lập trình hiện nay đều có thể đọc được. JSON là một tiêu chuẩn mở để trao đổi dữ liệu trên web.


![](Pictures/json-vs-xml.png)


# Định nghĩa

Định dạng JSON sử dụng các cặp `key – value` để dữ liệu sử dụng. Nó hỗ trợ các cấu trúc dữ liệu như đối tượng và mảng. Ví dụ một tập tin có tên `imkifu_info.json` với nội dung như ở dưới đây sử dụng format kiểu JSON để lưu trữ thông tin:
```
{
    "name" : "ImKifu",
    "title" : "Thực tập sinh của Nhân Hòa",
    "description" : "nhà đăng ký tên miền domain Quốc gia Việt Nam `.VN` . Nhà đăng ký chính thức của ICAN tên miền quốc tế `.COM`."
}
```

Ta có thể thấy cú pháp của JSON có 2 phần đó là `key` và `value`:

- Chuỗi JSON được bao lại bởi dấu ngoặc nhọn {}

- Các `key`, `value` của JSON bắt buộc phải đặt trong dấu nháy kép `{“}`, nếu bạn đặt nó trong dấu nháy đơn thì đây không phải là một chuỗi JSON đúng chuẩn. Nếu trường hợp trong value của bạn có chứa dấu nháy kép `"` thì hãy dùng dấu `\` để đặt trước nó, ví dụ  `\"json là gì\"`.

- Nếu có nhiều dữ liệu thì dùng dấu phẩy `,` để ngăn cách.

- Các `key` của JSON bạn nên đặt chữ cái không dấu hoặc số, dấu `_` và không có khoảng trắng., ký tự đầu tiên không nên đặt là số.

File json có thể được lưu với bất kỳ phần mở rộng nào, tuy nhiên thông thường thì nó được lưu dưới phần mở rộng là .json hoặc .js.

JSON ban đầu được phát triển để dành phục vụ cho ứng dụng viết bằng JavaScript. Tuy nhiên vì JSON là một định dạng dữ liệu nên nó có thể được sử dụng bởi bất cứ ngôn ngữ nào mà không bị giới hạn.

Giá trị key trong JSON có thể là chuỗi (string), số (numner), rỗng (null), mảng (array), hoặc đối tượng (object).

# Cấu trúc chuỗi JSON

## Kiểu OBJECT

```
var Hưng = {
   "firstName" : "Hưng",
   "lastName" : "Nguyễn",
   "age" :  "20"
};
```

## Kiểu OBJECT IN ARRAY

```
var interns = [{
   "name" : "ImKifu",
   "age" :  "20",
   "gender" : "male"
 
},
{
   "name" : "Niệm",
   "age" : "20",
   "gender" : "male"
 
},
{
   "name" : "Hiền",
   "age" : "20",
   "gender" : "female"
}];
```

Kiểu NEST OBJECT

``` 
var interns = {
  "imkifu" : {
  "name" : "Hưng",
  "age" :  "20",
  "gender" : "male" 
},
 
"niemdt" : {
  "name" : "Niệm",
  "age" : "20",
  "gender" : "male"
},
 
"hiennt" : {
  "name" : "Hiền",
  "age" : "20",
  "gender" : "female"
}
}
```

# Nên sử dụng JSON trong những tình huống nào?

Lưu trữ dữ liệu đơn thuần. Đó là khi bạn muốn lưu trữ dữ liệu dưới dạng metadata ở phía server. Chuỗi JSON sẽ được lưu vào database và sau đó khi cần dữ liệu thì sẽ được giải mã. 

Ví dụ với PHP, cung cấp các hàm liên quan đến JSON để mã và giải mã là json_encode và json_decode. 

Chú ý: phương pháp này cũng tương tự như sử dụng tính năng serialize và unserialize của PHP. Nhưng trong khi serialize và unserialize sử dụng với cả dữ liệu và biến, tức là phụ thuộc vào ngôn ngữ lập trình là PHP và dĩ nhiên không thể transfer sang ngôn ngữ lập trình khác để unserialize được. Vì vậy, nếu dữ liệu của bạn chỉ đơn thuần là dữ liệu cơ bản (chuỗi kí tự, số…) thì bạn hoàn toàn không nên sử dụng serialize mà nên sử dụng JSON. Sử dụng JavaScript, ActionScript để xử lý thông tin trả về từ phía server. Rất nhanh và rất dễ dàng.

Link tham khảo thêm tại [đây](https://viblo.asia/p/tim-hieu-ve-chuoi-du-lieu-json-MJykjQMJePB) và [đây](https://topdev.vn/blog/json-la-gi/).

Ngoài ra còn một số nguồn tham khảo khác:

https://www.json.org/json-vi.html

https://www.codehub.vn/JSON-La-Gi-va-Su-Dung-JSON-Nhu-The-Nao

https://viblo.asia/p/tim-hieu-ve-chuoi-du-lieu-json-MJykjQMJePB

https://topdev.vn/blog/json-la-gi/

https://freetuts.net/json-la-gi-cau-truc-chuoi-json-236.html
