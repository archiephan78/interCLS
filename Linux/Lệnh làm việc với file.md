## Các lệnh làm việc với file

### Lệnh man <command> đề đọc định nghĩa và các option của các câu lệnh
### lệnh cat
 + xem nội dung file
###vd :
```
   root@chungpt:~# cat file.txt
   chungpt
```
### lệnh head and tail 
+ xem từ đầu hoặc đuôi file, mặc đinh là 10 dòng:
+ option : -n < số dòng
### lệnh wc
 + đếm số dòng, số từ ,dung lương file
 + option : 
    `-m` số ký tự ; `-l` " số dòng ; `-w` số từ ; `-c` dung lương 

### Lệnh join
 + kết hợp nội dung các file theo cột 
### Lệnh paste
 + kệt hợp nội dung các file theo hàng
### Lệnh tac
 + ngược lại của cat
### Lệnh sort
 + sắp xếp dòng trong file, theo thứ tự ACSII
 + option : `-k` sort với keyword ; `-c` check; 
### Lệnh split:
 + chia file theo dòng `-l` hoặc theo dung lượng với `-b`
### lệnh uniq,nl :
 + xóa các dòng trùng lặp
 + `nl` hiển thị number line
### lệnh cut :
 + cut theo các option và show ra console
 + ví dụ option `-f` là field, `-d "*"` dấu hiệu vị dụ như dấu cách,dấu * hay ;,....
### Lệnh grep:
 +  tìm 1 chuỗi cụ thể trong file, cho phép sd biểu thức chính quy
 + option : `-n` hiện số dòng ; `-i` không phân biệt hoa thường ; `-r` nếu đó là thư mục thì nó sẽ tìm trogn tất cả các file là con cuả thư mục đó; `-w` đúng chính xác từ khóa
### lệnh sed :
 + stream editor, chỉnh sửa thay thế 1 cụm từ  có trong file bằng 1 từ khác
 + vd : `/s/text/rewrite/`
### lệnh awk:
 + thường đc dùng hỗ trợ cho grep ( phải có option --line buffer), hỗ trợ với ngôn ngữ C để lọc dữ liệu 1 cách thông minh hơn.  
### lệnh vi/vim:
 + chỉnh sửa file, `:set nu` để hiện number line , ấn `i` để chỉnh sửa và `:wq` để save và quit,.....
 + vd: mở file và nhảy đến dòng 5
   `vi +5 file.txt` hay mở file và nhảy đếm dòng có chứa ký tự chỉ định `vi +chungpt text.txt`
