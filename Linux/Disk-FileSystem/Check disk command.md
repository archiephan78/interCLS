## Các lệnh kiểm tra file system
### Lệnh fsck
+ file system check: hđong theo 5 phase:
 ```
 Phase 1: check block and sizes: ktra các inode
 Phase 2: check path-names : ktra sự tương thích giữa inode và thư mục
 phase 3: Check connectivity: các thư mục có đc kết nối vào hệ thống file hay ko
  phase 4: check reference counts : sửa các sai lệch về số link ở 2 phase trên
  Phase 5 : check cylinder groups :  ktra các block chưa dùng có phù hợp với bảng inode hay không?
 ````
+ Option : `-A` check all ; `-C` check proc; `-c` ktra và đánh dấu trên các bad blocks 
+ Sau khoảng 25-30 lần khởi động, fsck sẽ tự động ktra nên quá trình boot sẽ lâu hơn

### Lệnh df 
+  Monitoring disk use by partition
+ Kiểm tra dung lượng trên các partition
+ Option `-a` hiện thị tất cả ; `-h` hthi dưới dạng Mb và Gb; `-T` hiện thị định dạng partition;...
### Lệnh `du` [Option]..[File]
+ ktra dung lương trên đĩa đc dùng bởi  các tập tin và thư mục
+ Option : `-a` ;`-c`; `-h`; `-s`..
