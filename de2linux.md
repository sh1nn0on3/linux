## Câu 1 : 
    ?? Trong các tiêu chí của tổ chức OSI : Free Redistribution có nghĩa là gì 
+ phần mềm được phân phối theo cách mà người nhận có quyền tự do về việc sao    chép, phân phối và/hoặc sửa đổi chúng mà không phải chịu các hạn chế đặc biệt.
    * Sao chép tự do : (Freedom to Redistribute)
        Người nhận được quyền tự do sao chép (copy) phần mềm và phân phối nó cho người khác mà không bị hạn chế bởi các giới hạn quyền lợi riêng tư hoặc thương mại.
    * Sửa đổi tự do : (Freedom to Modify)
        : Người nhận cũng được quyền tự do sửa đổi mã nguồn và tạo ra các phiên bản sửa đổi của phần mềm để đáp ứng nhu cầu của họ mà không bị ràng buộc bởi các giới hạn đặc biệt


## Câu 2 : 
    ?? Có ít nhất bao nhiêu partition cần được tạo ra khi ta cài đặt hệ điều hành Linux 
+ Phân vùng
    * / (root)
    * swap 
    * /home (home)
    * /boot
    * /var

## Câu 3 : 
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
    + Tạo U3 , U4 có cùng password là U3_123
        * Tạo 2 thằng như nhau nên làm thử user U3 và làm U4 tương tự 
        * Tạo user U3 
            - $ useradd -m -s /bin/bash U3
                --> -m : add thêm vào home (/home/[user])
                --> -s /bin/bash : đặt lại shell (không dùng cũng được)
        * Thêm password
            - $ passwd U3
                --> nó hiện ra new password thì gõ vào thôi (kh hiện đâu)
    + Gán người dùng U3 , U4 vào nhóm root
        * Thêm vào group Root 
            - $ usermod -aG root U3
                --> -aG : thêm ng dùng vào nhóm mà không xóa trước đó -- xác định 
        * Kiểm tra
            - $ id U3
    + Tạo thư mục KMA2 trong thư mục gốc "/"
        * Ra thư mục "/"
            - $ cd /
                --> check : $pwd
        * tạo thư mục 
            - $ mkdir KMA2
    + Sao chép thư mục KMA2 vào thư mục U3
        * sao chép 
            - $ cp /KMA2 /home/U3
    + Đăng nhập với tài khoản U3 , xóa thư mục /kma2 , kiểm tra tồn tại /kma2
        * Đăng nhập 
            - $ su U3
        * Xóa thư mục 
            - $ cd / && rm -rf /kma2
        * kiểm tra
            - file vẫn tồn tại 
            - U3 không có quyền thực thi (cần phải cấp quyền cho U3 và đổi own cho /kma2)
            - (Gợi ý dùng chown và chmod)
    
## Câu 4
    + chuyển về root 
        - $ sudo su 
    + Tạo file script để lưu và chạy - Tên file là sinhvien_bai4
        * Tạo file 
            - $ nano sinhvien_bai3.sh
        * Viết các lệnh chạy (thêm bash ở dòng đâu)
            - ex : #/bin/bash
                    echo (bla bla :>>>)
        * Cấu hình thêm file thêm quyền thực thi
            - $ chmod +x sinhvien_bai4.sh
        * Thực thi (gọi file đấy là done)
            - $ ./sinhvien_bai4.sh
    + Kiểm tra cấu hình máy 
        * CPU
            - $ lscpu
        * Ram 
            - $ free -h
        * Disk
            - $ df -h
        * Card
            - $ ip a
        * Kernel
            - $ uname -a
        * Ip
            - $ ifconfig
    + Định dạng ổ đĩa với ext2 (đừng test đọc qua thôi :v)
        * Kiểm tra ổ có sẵn 
            - $ lsblk 
        * Định dạng
            - $ sudo mkfs.ext2 /dev/sdX
    + Tạo thư mục /THI/THUCHANH , gắn vào ổ đĩa 
         * Tạo thư mục 
            - $ mkdir TH1_HK
        * Gắn ổ đĩa với thư mục
            - $ sudo mount /dev/sd(X) /THI/THUCHANH
                --> mount : lệnh gắn ổ đĩa 
        * kiểm tra 
            - $ lsblk 
    + Sao chép file vào thư mục gốc vào /THI/THUCHANH
        * sao chép
            - $ cp /home /THI/THUCHANH
    + hủy bỏ gắn ổ đĩa 
        * Hủy gắn ổ đĩa với thư mục
            - $ sudo umount /THI/THUCHANH
                --> umount : lệnh hủy gắn ổ đĩa 
        * kiểm tra 
                - $ lsblk 
    + Gắn lại và không cho phép ghi và xóa 
        * Gắn ổ đĩa với thư mục
            - $ sudo mount /dev/sd(X) /THI/THUCHANH
                --> mount : lệnh gắn ổ đĩa 
        * Hạn chế quyền file lại 
            - $ chmod 444 /THUCHANH/*
                --> 444 : read ( chỉ đọc )