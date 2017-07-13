# Logical Volume Manager (LVM)

+ Là phương phép cho phép ấn định không gian đĩa cứng thành những logical volume khiến cho việc thay đổi kích thước trở nên dễ dàng hơn so với partition. Với LVM có thể thay đổi kích thước mà không cần phải sửa lại table của OS. 
+ LVM là kỹ thuật quản lý việc thay đổi kích thước lưu trữ của ổ cứng. Ưu điểm là không để hệ thống bị gián đoạn hoạt động, ko làm học dịch vụ,..
### Các thành phần trong LVM

<img src="http://i.imgur.com/RxUmap1.png" >
+ Hard drives : thiệt bị lưu trữ dl,  trong linux là sda
+ Partition : phân vùng
+ Physical Volumes : là cách gọi khác của partition trong kỹ thuật LVM. Nhiều physical volumes tạo thành volume group. mount point của boot ko đc nằm trong group.
+ Logical volume : volume group đc chia nhỏ thành nhiều logical volume.  mỗi Logical volume có ý nghĩa tương tự như partition. Nó đc dùng cho mount point và đc format với những định dạng khác nhau nhiw ext2,3,4

### các bước tạo Logical Volume LVM :
 + Tạo các partition với fdisk trên hardisk (`lsblk` để check hardisk)

```
   #fdisk dev/sdb
   #Command : n
   #Partition type:
       p primary
       e extended
   #Select :p
   #Partition number :1
   #Command : w (save and quit)
   #fdisk dev/sdb
   #Command :t
   #hexcode :8e (change to LVM)
   #command : w
````
 + Tạo Physical Volume 
```
  #pvcreate /dev/sdb1/
  #pvdisplay
```
 + Tạo Volume Group :
```
  #vgcreate vg-aaa1 /dev/sdb1 /dev/sdc1
  #vgdisplay
```
 + Taok Logical Volume:
```
  # lvcreate -L 1G -n lv-aaa1 vg-aaa1
  # lvdisplay
```
 + Định dạng logical volume với mkfs `mkfs -t ext4 /dev/vg-aaa1/lv-aaa1
 + mount lv-aaa1 vào folder aaa1 và sử dụng `mount /dev/vg-aaa1/lv-aaa1 aaa1
 + Để tăng kích thước Logical volume sdung câu lệnh
 ````
  # lvextend -L +50M /dev/vg-aaa1/lv-aaa1
 ````
  sau khi tăng kích thước thì logical volume đã đc tăng nhưng file system trên volume vẫn chưa thay đổi. resize nó :
 ```
  # resize2fs /dev/vg-aaa1/lv-aaa1
 ```
+ Tương tự để giảm kích thước thì dùng lệnh `lvreduce`. nhưng trc khi giảm thì phải unmount và format lại với `mkfs`
 + Tương tự với Volume group thì dùng lệnh `vgextend` và `vgreduce`, xóa thif dùng `vgremove`	
 
