# Giới thiệu về XML

Ngoài cách lưu trữ dữ liệu trong các hệ quản trị CSDL ra thì bạn có thể lưu trữ dữ liệu trong file TXT, file JSON hay file XML đều được. Tuy nhiên với những hệ thống lớn thì bắt buộc ta phải lưu trữ trong hệ quản trị CSDL bởi vì nó cũng cấp những tính năng giúp quản lý dữ liệu tốt hơn. Còn đối với XML hay JSON thì ứng dụng lớn nhất của nó trong lập trình web đó là xây dựng các Service và API, nghĩa là các API đó sẽ trả kết quả về dạng JSON hoặc XML các hệ thống khác có thể hiểu được. Ví dụ để tạo một ứng dụng đặt phòng trên mobile thì bạn phải xây dựng một Service và nhiệm vụ của service đó là trả kết quả danh sách phòng về cho App Mobile, mà với ngôn ngữ lập trình Mobile khác hoàn toàn với PHP hay C# nên ta phải trao đổi dữ liệu thông qua XML hoặc JSON.

# XML là gì?

 
XML là viết tắt của từ eXtensible Markup Language, hay còn gọi là ngôn ngữ đánh dấu mở rộng do W3C đề nghị với mục đích tạo ra các ngôn ngữ đánh dấu khác. Đây là một tập hợp con đơn giản có thể mô tả nhiều loại dữ liệu khác nhau nên rất hữu ích trong việc chia sẻ dữ liệu giữa các hệ thống. Ví dụ khi bạn xây dựng một ứng dụng bằng C# và một ứng dụng bằng PHP thì hai ngôn ngữ này không thể hiểu nhau, vì vậy ta sẽ sử dụng XML để trao đổi dữ liệu.

Tất cả những đặc tả dữ liệu XML đều phải tuân theo quy luật và cú pháp của nó nên hầu như các file XML đều rất nghiêm khắc trong việc biên dịch. Tuy nhiên công nghệ này cần phải được xem xét bởi vì trong quá trình thao tác và truyền dữ liệu nó có tỉ lệ sai sót lên tới 5% - 7%. Con số này không cao nhưng cũng rất đáng để cân nhức khi sử dụng.

Điển hình nhất là ngôn ngữ đánh dấu siêu văn bản HTML sử dụng cú pháp của XML để tạo nên và nó có các bộ phần tử và thuộc tính không mềm dẻo nên chỉ có tác dụng trong việc trình bày dữ liệu trên trình duyệt Browser.

# Sử dụng XML để làm gì ?
XML có thể được sử dụng để:

- XML có thể núp phía sau để đơn giản hóa việc tạo các tài liệu HTML cho các Website lớn.

- XML có thể được sử dụng để trao đổi thông tin giữa các tổ chức và hệ thống.

- XML có thể được sử dụng để Offload và Reload các cơ sở dữ liệu.

- XML có thể được sử dụng để lưu trữ và sắp xếp dữ liệu, có thể tinh chế dữ liệu cần xử lý.

- XML có thể dễ dàng để được hợp nhất với Style Sheet để tạo ra hầu như bất kỳ kết quả mong muốn nào.

Nói chung, bất kỳ kiểu dữ liệu nào có thể được biểu diễn như là một tài liệu XML.

# Markup là gì?

XML là một ngôn ngữ đánh dấu (Markup Language), mà định nghĩa tập hợp các qui tắc để mã hóa các tài liệu trong một định dạng có thể đọc được bởi con người và máy tính. Vậy một Markup Language là gì? Markup là thông tin được bổ sung vào một tài liệu nhằm nâng cao ý nghĩa của nó theo các cách cụ thể, trong đó nó nhận diện các thành phần và cách chúng liên quan với nhau. Chính xác hơn, một Markup Language là một tập hợp các biểu tượng có thể được đặt trong text của một tài liệu để phân ranh giới và gán nhãn các phần của tài liệu đó.

Ví dụ sau minh họa cách XML đánh dấu trông như thế nào, khi được nhúng trong một phần của text:

```
<message>
   <text>Hello, world!</text>
</message>
```

Ví dụ trên bao gồm các biểu tượng đánh dấu, hoặc các thẻ như `<message>...</message>` và `<text>... </text>`. Các thẻ `<message>` và `</message>` đánh dấu phần bắt đầu và phần cuối của đoạn XML code. Các thẻ `<text>` và `</text>` bao quanh phần văn bản `Hello, world!`.

# XML có phải là một ngôn ngữ lập trình?

Một ngôn ngữ lập trình gồm các qui tắc về cú pháp và từ vựng của riêng nó mà được sử dụng để tạo các chương trình máy tính. Các chương trình này chỉ dẫn máy tính thực hiện các tác vụ cụ thể. XML không đủ tiêu chuẩn để là một ngôn ngữ lập trình khi nó không thực hiện bất kỳ thuật toán hay kỹ thuật tính toán nào. Nó thường được lưu trữ trong một text file đơn giản và được xử lý bởi phần mềm đặc biệt có khả năng thông dịch XML.

# Cú pháp của tài liệu XML

Nếu bạn đã học qua HTML rồi thì rất dễ dàng hiểu cú pháp của XML bởi vì HTML được xây dựng dựa trên cú pháp của XML.

File XML sẽ có phần mở rộng là .xml. Tuy nhiên bạn hoàn toàn có thể sử dụng ngôn ngữ lập trình để thay đổi phần mở rộng cho nó 

## Cú pháp của thẻ XML:

XML được xây dựng dựa vào cấu trúc NODE lồng nhau, mỗi node sẽ có một thẻ mở và một thẻ đóng như sau:

```
<nodename> content </nodename>
```
Trong đó:

- `<nodename>` là thẻ mở, tên của thẻ này do bạn tự định nghĩa.

- `</nodename>` là thẻ đóng, tên của thẻ này phải trùng với tên của thẻ mở.

- `content` là nội dung của thẻ này

Ví dụ mình lưu trữ domain của mình thì cấu trúc như sau:
```
<domain>imkifu.top</domain>
```

Bạn hoàn toàn có thể bổ sung các thuộc tính vào các thẻ XML bằng cách sử dụng cú pháp sau:

```
<nodename ten_thuoc_tinh="giá trị">content</nodename>

```
Ví dụ bạn lưu trữ thông tin domain và chủ sở hữu của nó thì có thể lưu như sau:
```
<domain owner="Nguyễn Kiều Hưng" email="somebodyisdaydreamer@gmail.com">imkifu.top</domain>
```

## Khai báo Header (Chỉ thị xử lý):

Trên đầu mỗi file XML bạn phải khai báo một thẻ để thông báo version XML đang sử dụng (`thường là version 1.0`), và còn có thể chứa các thông tin về mã hóa ký tự hoặc các phụ thuộc bên ngoài khác . Giá trị của encoding (kiểu mã hóa ký tự) thuộc một trong các định dạng sau: UTF-8, UTF-16, ISO-10646-UCS-2, ISO-10646-UCS-4, ISO-8859-1 to ISO-8859-9, ISO-2022-JP, Shift_JIS, EUC-JP.

Cú pháp của thẻ chỉ thị xử lý như sau:

```
<?xml version="1.0" encoding="UTF-8"?>
```
Như vậy với các ví dụ trên thì cấu trúc đúng sẽ phải là:

```
<?xml version="1.0" encoding="UTF-8"?>
<domain>imkifu.top</domain>
```

và

```
<?xml version="1.0" encoding="UTF-8"?>
<domain owner="Nguyễn Kiều Hưng" email="somebodyisdaydreamer@gmail.com">imkifu.top</domain>
```

## Root node:

Mỗi tài liệu XML `nên` có một thẻ ngoài cùng và ta gọi thẻ này là `root node`. Thẻ này sẽ khai báo `tên chính` của tài liệu XML.

Ví dụ mình cần lưu trữ danh sách domain thì có thể viết như sau:
```
<?xml version=```"1.0" encoding="UTF-8"?>
<domains>
    <domain owner="Nguyễn Kiều Hưng" email="somebodyisdaydreamer@gmail.com">imkifu.top</domain>
</domains>
```

Không có một quy tắc đặt tên nào cả mà quy tắt do lập trình viên đặt ra, tuy nhiên lời khuyên là bạn nên đặt tên sao cho ngữ nghĩa phù hợp với nội dung của file.

## Link tài liệu tham khảo

https://cuongquach.com/xml-la-gi-doc-file-xml-nhu-the-nao.html

https://vietjack.com/xml/xml_la_gi.jsp

https://freetuts.net/xml-la-gi-cu-phap-can-ban-cua-xml-513.html