 + Trong `bash shell` giá trị của mỗi biến là chuỗi, có nhiều biến được sử dụng bởi môi trường shell và môi trường hệ điều hành để lưu trữ các giá trị mặc đinh được gọi là biến môi trường 
 + Các biến được đặt tên với cấu trúc đặt tên thông thường. khi 1 ứng dụng được thực thi, nó sẽ  truyền 1 tập các biến gọi là biến môi trường. Để xem tất cả các biến môi trường dùng `env`
 + tạo biến môi trường của mình 
  ` export VCC="VcCloud"`
 + Kiểm tra
   ` env | grep 'VCC'`
 + Gỡ biến môi trường
   ` unset VCC` 
