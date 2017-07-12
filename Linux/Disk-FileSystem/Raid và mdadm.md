# RAID và mdadm
 RAID ( Redundant Arrays of Inexpensive Disks) là hình thức ghép nhiều ổ đĩa cứng vật lý thành 1 hế thống ổ đĩa cứng có chức năng gia tăng tốc độ đọc ghi dữ liệu hoặc nhằm tăng thêm sự an toàn của dữ liệu chứa trên hệ thống đĩa hoặc kết hợp cả 2 yếu tố trên
 + Phân loại thì có nhiều loại RAID như raid 0,1,3,4,5,10,....
 
### RAID 0 :
 + cần tối thiểu 2 ổ đĩa (disk 0 , disk 1)
 + nó sẽ hđ như sau : giả sử file A dung lượng 100MB sẽ dc lữ trữ ở mỗi ổ đĩa 50MB.
 + Yêu cầu 2 ổ cứng cùng dung lượng, nếu kahcs thì lấy ổ thấp nhất. 
### RAID 1 :
 + đạt an toàn dữ liệu
 +  2 ổ địa lưu dữ liệu giống hệt nhau
### RAID 10:
 + cần tối thiếu 4 ổ.
 + dữ liệu lưu đồng thời vào 4 ổ .2 ổ dạng raid 0, 2 ổ dạng raid 1
 + chi phí cao
 <img src="http://i.imgur.com/ZNhGyqL.png" >

### RAID 01:
 + 4 ổ 
  <img src="http://i.imgur.com/RpS0muW.jpg" >
  
### RAID 5:
 + cần tối thiểu 4 ổ cứng  
 + file sẽ được split và lưu trong 3 ổ và 1 ổ để backup. Bản back up có thể ở bất kỳ trên disk nào trong cụm raid. 
<img src="blob:http://imgur.com/8087a271-5d3e-4abd-bb5c-d299587b0642">

## Quản lý chuẩn để tạo RAID với mdadm 


+ install :
  
  ```
  $apt-get install mdadm
  $yum install mdadm
  
 ```
 
+ mdadm có 7 chức năng . nhưng 3 chức năng chính là `create` - tao 1 thiết bị raid mới ; `assemble` - tập hợp các thiết bị để tạo raid ;  và `monitor` - theo dõi thiết bị raid .
+ Tạo ổ đĩa mềm RAID , ý là phần mềm, ko cần thiết bị RAID, dùng các phân vùng tham gia vào mảng đĩa thay vì sd toàn bộ ổ đĩa.
 
 
 ```
  $mdadm --create /dev/md0 <chế độ raid> <option> < danh sách các thiet bi tham gia>
 ```

