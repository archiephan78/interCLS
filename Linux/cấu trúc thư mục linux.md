# Linux phân chia các thư mục từ thư mục gốc /root
Gồm các thư mục 
\ -/root :
tất cả các file thư mục bắt đầu từ root, chỉ có root user mới có quyền viết trogn thư mục này
#/bin:
  chứa các file thực thi nhị phân
  Linux command sử dụng bởi tất cả users của hệ thống được đặt ở đây vd như ps,ls,grep,ping,cp....
#/sbin
  giống /bin nhưng linux command nằm trong thư mục này thường đươc sd bởi sysadmin cho mục đích bảo trì hệ thống vd như iptables, fdisk,ifconfig,...
#/boot
 khởi động
#/dev
  chứa device files bao gồm terminal device,usb hoặc bất cứ device nào gắn với system
#/etc
  chứa file cấu hình yêu cầu bởi tất cả các programs,hệ thống vd như resolv.conf, iptables.conf, interface,...
#/home
   thư mục người dùng 
#/lib
  chứa library file hỗ trợ thwucj thi các lệnh trong bin và sb
#/lib64
  giống lib nhưng chwuas file dành riêng cho system x64
#/lost+found
  dùng để lưu các tập tin ko có thư mục mẹ mà được tìm thấy dưới thư mục gốc sau khi dùng lệnh fsck
#/media
  thư mục này được dùng để tạo ra các tập tin gắn (loaded) tạm thời được hệ thống tạo ra khi một thiết bị lưu động (removable media) được cắm vào như đĩa CDs, máy ảnh kỹ thuật số… các file *.iso
#/mnt
  thư mục tạm chứa các file hệ thống được mounted
#/opt
  chứa các ứng dụng đc thêm vào từ các nhà cung cấp độc lập khác chưa có trong hệ thống soucerlist 
#/proc
  chứa thông tin về process hệ thống 
   đây là filesystem chứa thông tin về các process đang chạy 
#/run
  thư mục song song với /var/run . tức là 2 bên có dữ liệu giống nhau
#/srv
  chứa dữ liệu các dịch vụ chạy trên hệ thống như ssh, mysql,...
#/sys
  thư mục chứa các file hệ thống 
#/tmp
  thư mục chứa các file tạm thời tạo ra bởi system và users, sẽ bị xóa sau khi reboot 
#/usr
  chứa các tập tin của những ứng dụng chính đc cài đặt cho mọi , chứa thư viện, file thực thi, hướng dẫn và mã nguồn.
