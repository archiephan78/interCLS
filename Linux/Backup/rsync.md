# Rsync
+ Sao lưu hoặc đồng bộ dữ liệu 1 cách an toàn.
+ sao lưu 

   ```
  rsync -vbar --delete-before /thư mục A /thưmục B
   ```
 Backup sẽ tạo 1 bản dl hoàn chỉnh giống nhau,A thay đổi thì B thay đổi

+ đồng bộ

  ```
   rsync -av --numeric-ids /folderA /folderB
  ```
synchronize là chức năng đồng bộ dl. A và B dữ liệu sẽ đồng bộ với nhau, bên nào có bất kỳ thay đổi gì thì bên kia cũng vậy
