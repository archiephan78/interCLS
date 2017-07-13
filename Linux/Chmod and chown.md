
## Chmod 

+ chmod cho phép thay đổi permission của một file hay folder. 
+ option : 4= read ; 2= write ; 1= execute ; 0= no permission
### vd:
  ```
     chmod 755 test.sh
  ```
 Nghĩa là user khởi tạo `test.sh` sẽ có quyền read,write,execute(4+2+1), group chứa user đấy sẽ chỉ có quyền read, write ; other cũng chỉ có quyền read và write(4+1). Hoặc có thể dugnf chữ cái tương đương `r,w,x` 
## Chown

+ thay đổi quyền sở hữu của file hoặc folder
+ ví dụ : `chown -R chungpt:admin /var/www`

## chgrp 

+ thay đổi group cho user
