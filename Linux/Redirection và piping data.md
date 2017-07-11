# Redirecting và piping
 + Để điều hướng dữ liêu vào hoặc ra, dùng các ký tự được quy định sẵn
 ##### ```>```  dữ liêu xuất ra vào file tạo mới, nếu đã có file thì nó sẽ ghi đè
### vd: 
 ```
   cat $PATH > fileB.txt
  ```
 `>>` dữ liệu sẽ xuất ra file tạo sẵn và không ghi đè, nếu ko có file đấy nó sẽ create
### vd :
```
   cat abcdef >> fileB.txt
```
  `2>` tạo file mới mang thông báo lỗi( seem like log file), nếu file đấy có sẵn nó sẽ ghi đè
### vd : 
```
   cat fileC.txt 2> error.txt
```
  `2>>` ghi lên file có sẵn và ko ghi đè, create new file khi chưa có file đấy
  `&>` tạo file mới và chứa cả output và , nếu đã có file đấy nó sẽ ghi đè
   `<` lấy dữ theo hướng mũi tên 
 + Piping data : sự dụng kết quả của câu lệnh trước, ghi vào pip buffer sau đó dùng kqua đấy làm đầu vào cho câu lệnh sau, sdung `|`
### vd: 
```ls | less```
