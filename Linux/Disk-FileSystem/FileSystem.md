## File system trong linux
+ file system là một kiểu lưu trữ và tổ chức các file và dữ liệu trong file. Hiện linux phổ biến 2 kiểu là `ext3` và `ext4`.
+ Trên mỗi partition chỉ có thể có một kiểu file system( đc tạo ra khi format : ext3,ext4, fat, ntfs,..). Nhưng 1 cây thư mục có thể đặt trên nhiều partition : vd thư mục gốc `/` đặt ở sd2, thư mục `/home` đặt ở sda5,... tùy ng dùng.
### Đơn vị lưu trữ trên ổ cứng 
+ Sector : là đơn vị lưu trữ vật lý nhỏ nhất trên ổ cứng. 512b -> 1,2 or 4KiB 
+ Cluster : 1-128 sector
### Đơn vị lưu trữ file logic
+ Block : là đơn vị lưu trữ logic nhỏ nhất được cấp khi lưu dữ liệu, dung lương 1 block tùy theo kiểu file system. VD: `ext3` 1 block có thể là 1,2 hoặc 4kB
+ Extent : là một nhóm block liên tục. vd `ext4` dùng 1nhoms block thay vì block. Dữ liệu được lưu đủ 1 extent trong bộ nhớ trước khi ghi vào ổ cứng do đó tốc độ đọc ghi nhanh hơn. vd như `ext4` ghép các block 4kb thành extent tới 128 Mb
### Superblock : 
+ gồm các thông tin chugn về 1 hệ thoogns file: dung lượng, dung lượng block, các block đã ghi và con trống
+ Nếu superblock bị hỏng thì hệ thoogns file không mount đc và do đó không truy cập đc.   
