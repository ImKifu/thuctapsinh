# Logical Volume  
Trong LVM có 3 loại logical volume:  
  - linear volume.
- striped volume.
- mirrored volume.  
## 1. Linear Volume  
 Linear Volume gộp nhiều Physical Volume(PV) thành một Logical Volume(LV). Ví dụ nếu bạn có 2 ổ 60GB , ta có thể tạo một Logical Volume 120 GB  .  
 Tạo một linear volume sẽ gán một lượng Physical Extents (PE) vào Logical Volume.Ở ảnh dưới ta có thể thấy các Logical Extens(LE) từ 1 dến 99 có thể được gán từ PV thứ nhất và LE từ 100 đến 198 là từ PV thứ 2, tổng cộng trong LV  có 198 LE  .  

 <img src="https://i.imgur.com/9mHBYI8.png">  

 Các PV cấu thành nên các LV không nhất thiết phải cùng dung lượng .Tại hình dưới ta có thể thấy Volume Group (VG) VG1 với kích cỡ các PE là 4MB. VG này bao gồm 2 PV là PV1 và PV2.Ta có thể tạo Linear Volume với dung lượng từ 1 đến 300 LE (4MB-1200MB).    
 <img src="https://i.imgur.com/Wz9yrW2.png">  

Từ 1 VG ta có thể tạo ra nhiều Linear Logical volume khác nhau với các dung lượng khác nhau . 

Cách ghi dữ liệu:  
<img src="https://i.imgur.com/OIlVvsX.gif">  

## 2. Striped Logical Volumes 
Kiểu LV này giúp cải thiện khả năng ghi đọc của ổ cứng.Striping giúp chia đều dữ liệu vào các LE.  
Ở ảnh dưới ta thấy data bị chia ra lần lượt trong 3 PV.Dữ liệu đầu tiên viết vào PV1 , dữ liệu thứ 2 viết vào PV2 ,... lần lượt như vậy đến khi hết dữ liệu phải ghi. 
<img src="https://i.imgur.com/wrdfvI7.png">

Striped logical volume các size stripe không vượt quá dung lượng các PE .  
**Lưu ý : Khi muốn tăng dung lượng của striped logical volumes , cần cài đặt một bộ PV , vì nếu cấu hình 1 PV vào sẽ k thể chạy striped được**  

Cách ghi :  
<img src="https://i.imgur.com/acfgnbl.gif">  
## 3.Mirrored Logical Volumes :  
Kiểu ghi này copy data trên các thiết bị khác nhau .Khi dữ liệu được viết vào một PV , nó sẽ được viết luôn vào PV còn lại.Cung cấp sự an toàn nếu các thiết bị có hỏng hóc . Trong các LV chạy mirror , nếu một LV bị hỏng , LV còn lại sẽ chạy Linear Volume và vẫn có thể truy cập đến được.  

Khi tạo mirrored logical volume, LVM sẽ đảm bảo data được viết trên các PV riêng biệt .Với LVM ta có thể tạo nhiều mirrored logical volumes.  

Một bản sao (Mirror) của LVM thường có kích thước 512KB ,LVM có lưu trữ log để theo dõi các phân vùng đồng bộ của các data được ghi.  
<img src="https://i.imgur.com/2CIZbMF.png">  

## 4. Snapshot Volume  






