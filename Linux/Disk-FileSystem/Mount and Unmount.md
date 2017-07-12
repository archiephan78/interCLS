## Mount và UnMount trong linux
+ Để có thể truy cập dữ liệu đc lưu trữ trong các phân vùng thì trong linux trước hết các thiết bị này phải được gắn kết (mount) vào 1 thư mục trống (gọi là mount point) đã tồn tại sẵn trong cây thư mục. Và unmount ( ngắt kết nối)
+ Có thể sử dụng lệnh mount để mount filesystem hoặc mount tự động thông qua file cấu hình `/etc/fstab`
#### ví dụ để mount ổ CD `/dev/cdrom là đường dẫn tớ ổ cd cần mount và /media/cdrom là mount point. truy cập đến `/media/cdrom thì mới thực sự truy cập đc nd trong CD :
```
   $ mount /dev/cdrom /media/cdrom
```
+ tương tự viws unmount 
