## Câu 1 : 
    ?? Phân biệt CopyLeft và Copyright ?
+ CopyLeft : dùng chùa >< Copyright : bản quyền
+ copyright tập trung vào việc bảo vệ quyền lợi của tác giả, copyleft tập trung vào việc đảm bảo tự do sử dụng và phân phối tác phẩm trong cộng đồng
....

## Câu 2 
    ?? Tập tin /etc/shadow chứa thông tin gì của user sys 
+ Liên quan đến mật khẩu của user trong sys (env)
+ vd : 
 ``username:password:last_change:min_change:max_change:warning_days:inactive_days:expire_date:reserved

## Câu 3 
    + chuyển về root 
        - $ sudo su 
    + Tạo file script để lưu và chạy - Tên file là sinhvien_bai3
        * Tạo file 
            - $ nano sinhvien_bai3.sh
        * Viết các lệnh chạy (thêm bash ở dòng đâu)
            - ex : #/bin/bash
                    echo (bla bla :>>>)
        * Cấu hình thêm file thêm quyền thực thi
            - $ chmod +x sinhvien_bai3.sh
        * Thực thi (gọi file đấy là done)
            - $ ./sinhvien_bai3.sh
    + Tạo U1 , U2 có cùng password là sv123456
        * Tạo 2 thằng như nhau nên làm thử user U1 và làm U2 tương tự 
        * Tạo user U1 
            - $ useradd -m -s /bin/bash U1
                --> -m : add thêm vào home (/home/[user])
                --> -s /bin/bash : đặt lại shell (không dùng cũng được)
        * Thêm password
            - $ passwd U1
                --> nó hiện ra new password thì gõ vào thôi (kh hiện đâu)
    + Xem thông tin về người dùng 
        
