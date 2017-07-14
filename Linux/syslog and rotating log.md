## Syslogd and rotating Log
+ Syslog là 1 gói software trong linux nhằm để ghi log của hệ thống trong quá trình hđ như của kernel, deamon hoặc các ứng dụng chạy trên hệ thống như http, dns,dhcp, ntp,..
+ Ứng dụng của syslog : Phân tích nguyên nhân của 1 vấn đề, giúp cho việc khắc phục sự cố nhanh hơn khi hệ thống gặp vấn đề, giúp cho việc pháy hiện dự đoán 1 vấn đề có thể xảy ra đối với hệ thống.
+ Mặc định thì log đc lưu trong `/var/log` 
+ file cấu hình syslog nằm ở `/etc/rsyslog.conf` chứa các rule.

## Rotating Log
+ Phần lớn các distro sẽ cài đặt một cấu hình syslog mặc định cho bạn, bao gồm logging to messages và các log files khác trong /var/log. Để ngăn cản những files này ngày càng trở nên cồng kềnh và khó kiểm soát, một hệ thống quay vòng log file (a log file rotation scheme) nên được cài đặt. Hệ thống cron đưa ra các lệnh để thiết lập những log files mới, những file cũ được đổi tên bằng cách thay một con số ở hậu tố. Với loại quay vòng này, /var/log/messages của ngày hôm qua sẽ trở thành messages.1 của ngày hôm nay và một messages mới được tạo. Sự luân phiên này được cấu hình cho một số lượng lớn các file, và các log files cũ nhất sẽ được xoá khi sự luân phiên bắt đầu chạy. Ví dụ trong /var/log có các messages sau: messages, messages.1, messages-20141111, messages-20141118, ...

+ Tiện ích thi hành rotation là logrotate. Lệnh này được cấu hình sử dụng cho một hoặc nhiều files - được xác định bởi các tham số đi cùng. File cấu hình mặc định là /etc/logrotate.conf.
