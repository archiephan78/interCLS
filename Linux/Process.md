### Fork() trong linux:
 +  Là 1 system call của linux, khi 1 chương trinh gọi fork thì OS sẽ copy ra 1 chương trình nữa có process ID khác với chương trình hiện tại và 2 chương trình sẽ chạy song song. Chương trình đầu gọi là Process Cha, chương trình sau gọi là Process Con. Cả 2 process này đều có mọi thông tin trên stack giống nhau chỉ có PID khác nhau.
### Lệnh ps
  + biết thông tin các process hiện đang sử dụng
  + option : `-a`: hiện thị tất cả các tiến trình ; `-f` hiện thị thông tin tiến trình cha; `-aux` liệt kê danh sahcs các process đang chạy cùng owner, pid, %cpu,...
### Lệnh top
  + hiển thị thông tin sử dụng tài nguyên
theo thống kê thời gian thực
  + option : `-d time` khoảng tgian trễ time giữa 2 lần update status ( mặc đinh 5s) ; `-p [pid]` theo dõi process với pid cụ thể; `-a` all; 
### dừng 1 process
 + `Kill` [signal] [PID]
 + mặc định signal là 15 : TERM : kết thúc ctrinh
 + `1` gọi lại proc ; `9` hủy proc ; `17,19,23` dùng proc; 
### Background : tiến trình ngầm
 + `bg` chuyển từ proc foreground -> bg
 + `fg %[pid]` chuyển từ bg -> fg
