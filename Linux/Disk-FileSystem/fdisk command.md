# Command fdisk
+ Dùng để xem và quản lý các phân vùng ổ cứng trên Linux. 
 + `sudo fdisk -l` để hiển thị danh sách các phân vùng có sẵn của hệ thống
 + để làm việc trên các phân vùng ổ đĩa cụ thể thì vào command mode : ` sudo fdisk /dev/sda`
 +  Xem bảng phân vùng sử dụng `p`, `d` để xóa 1 phân vùng. 
 + `n` để tạo mới 1 vân vùng với `l` là logical và `p` là primary. Sau đó xác định sector muốn bắt đầu phân vùng. enter để chấp nhận thiết lập mặc đinh sau đó xác định sector cuối của phân vùng. có thể chỉ định kích thước của ổ đĩa thay vì là sector
 + định dạng phân vùng vừa tạo với command `sudo mkfs`.ext4 /dev/sda6. Nếu là swap thì mà mkswap
