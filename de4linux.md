## Câu 1 
    ?? Trình bày định nghĩa :
        + phần mềm mã nguồn mở (OSS)
        + Freeware
        + ShareWare
        + Charityware
    
    ++ Mã nguồn mở :
        - là loại phần mềm mà nguồn mã nguồn của nó được công bố cùng với mã nguồn để mọi người đều có thể sử dụng và truy cập vào 
    ++ Freeware :
        - Là phần mềm miễn phí và có mã nguồn mở
    ++ Shareware :
        - Là phần mềm miễn phí 1 thời gian :v (nửa mùa)
    ++ Charityware :
        - Là phần mềm mất phí

## Câu 2 
    ?? Cho biết các thư mục sau 
        + /sbin/
        + /tmp/
        + /var/
    
    ** /Sbin/ :
        - Thư mục chưa các lệnh hệ thống
        - ex : ifconfig , fdisk , reboot
    ** /tmp/ :
        - Thư mục tạm thời thường được xóa khi khởi động lại (hiểu như ram )
    ** /var/ :
        - Là thư mục lưu trữ biến môi trường , dữ liệu biến đổi trong quá trình hoạt động
        - ex : /var/log  , /var/lib , ...

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
            - $ chmod +x sinhvien_bai4.sh
        * Thực thi (gọi file đấy là done)
            - $ ./sinhvien_bai3.sh  
    + Tạo U1 và mật khẩu abc@123
        * Tạo User và password
            - $ useradd U1
            - $ passwd U1 
        * Tạo file F1.txt trong U1
            - $ nano /home/U1/F1.txt
        * Tạo file f1.txt trong U1
            - $ nano /home/U1/f1.txt
        * Xem thuộc tính của tệp tin 
            - $ ls -la F1.txt f1.txt

## Câu 4
    + chuyển về root 
        - $ sudo su 
    + Tạo file script để lưu và chạy - Tên file là sinhvien_bai3
        * Tạo file 
            - $ nano sinhvien_bai4.sh
        * Viết các lệnh chạy (thêm bash ở dòng đâu)
            - ex : #/bin/bash
                    echo (bla bla :>>>)
        * Cấu hình thêm file thêm quyền thực thi
            - $ chmod +x sinhvien_bai4.sh
        * Thực thi (gọi file đấy là done)
            - $ ./sinhvien_bai4.sh
    + Tạo cây thư mục /KMA/Baitap trong file vanban2.txt và xem thuộc tính
        * Tạo cây thư mục
            - $ mkdir /KMA/Baitap
        * Tạo file thư mục 
            - $ nano /KMA/Baitap/vanban2.txt
        * Gán quyền 
            - $ chmod 744 /KMA/Baitap/vanban2.txt
        * Xem thuộc tính
            - $ ls -la /KMA/Baitap/vanban2.txt
    + Tạo người dùng U25 và cấp quyền để U25 sửa được
        * Tạo U25 và passwd
            - $ useradd U25
            - $ passwd U25 
        * Cấp quyền 
            - $ chmod U25 /KMA/Baitap/vanban2.txt
        * 
    + Kiểm tra địa chỉ quảng bá 
        - $ ifconfig 