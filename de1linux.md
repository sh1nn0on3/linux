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
    + Xem thông tin về người dùng - đường dẫn người dùng
        * xem thông tin 
            - $ id U1 
        * xem đường dẫn 
            - $ su U1 
                --> vào trong user
            - $ echo $HOME
                --> xem đường dẫn hiện tại của U1
    + Tạo thư mục KMA_U1 
        * tạo thư mục
            - $ su U1
                --> vào trong user U1
            - $ mkdir KMA_U1
                --> Tạo thư mục
    + Di chuyển thư mục KMA_U1 sang U2 
        * Ở ngòai root
            - $ mv /home/U1/KMA_U1 /home/U2
                --> mv [path_current] [path_new] : di chuyển file
        * Kiểm tra 
            - $ su U2
                --> vào U2 xem đã có chưa 

## Câu 4
    + chuyển về root 
        - $ sudo su 
    + Tạo file script để lưu và chạy - Tên file là sinhvien_bai4
        * Tạo file 
            - $ nano sinhvien_bai4.sh
        * Viết các lệnh chạy (thêm bash ở dòng đâu)
            - ex : #/bin/bash
                    echo (bla bla :>>>)
        * Cấu hình thêm file thêm quyền thực thi
            - $ chmod +x sinhvien_bai4.sh
        * Thực thi (gọi file đấy là done)
            - $ ./sinhvien_bai4.sh
    + Dùng lệnh định dang ổ đĩa với định dạng ext4 (đừng test đọc qua thôi :v)
        * Xác định địa chỉ ổ cứng
            - $ lsblk ( hoặc fdisk -l )
        * Định dạng ổ đĩa
            - $ sudo mkfs.ext4 /dev/sdX
                --> mkfs.ext4 : lệnh định dạng --- /dev/sd(X) : ổ đĩa cần định dạng
        * Kiểm tra 
            - $ lsblk ( hoặc fdisk -l )
    + Tạo thư mục /TH1_HK , gắn ổ đĩa với thư mục /TH1_HK
        * Tạo thư mục 
            - $ mkdir TH1_HK
        * Gắn ổ đĩa với thư mục
            - $ sudo mount /dev/sd(X) /TH1_HK
                --> mount : lệnh gắn ổ đĩa 
        * kiểm tra 
            - $ lsblk 
    + sao lưu file từ ổ địa vào /TH2_HK bằng lệnh rsync 
        * sao lưu 
            - $ sudo rsync -av --progress /dev/sd(X) /TH2_HK
                --> -av : giữ nguyên thuộc tính và hiển thị
                --> --progress : hiện thị tiến trình sao lưu
    + copy file bất kỳ (ổ đĩa gốc) vào thư mục /TH2_HK
        * copy
            - $ sudo cp /dev/sdc /TH2_HK
    + Hủy bỏ TH1_HK với ổ đĩa
        * hủy
            - $ sudo umount /TH1_HK
    + kiểm tra sự tồn tại của file vừa copy vào thư mục TH1_HK ; giải thích cơ chế ánh xạ mount/umount
        * kiểm tra sự tồn tại 
            - $ ls 
        * giaỉ thích 
            - Mount (Gắn kết):
                Khi bạn mount một ổ đĩa hoặc phân vùng, bạn thực hiện việc "gắn kết" nó vào hệ thống tệp.
                Hệ thống tệp sẽ tạo một liên kết từ thư mục mount point (điểm gắn kết) đến ổ đĩa hoặc phân vùng đó.
                Điểm gắn kết là nơi mà dữ liệu từ ổ đĩa hoặc phân vùng sẽ trở nên truy cập được trong cây thư mục hệ thống tệp của bạn.

            - Unmount (Gỡ kết nối):

                Khi bạn unmount một ổ đĩa hoặc phân vùng, bạn thực hiện việc "gỡ kết nối" nó khỏi hệ thống tệp.
                Liên kết từ thư mục mount point đến ổ đĩa hoặc phân vùng sẽ bị hủy bỏ, và dữ liệu trên ổ đĩa sẽ không còn truy cập được từ đường dẫn mount point đó.
                Khi bạn unmount, bạn cho phép hệ thống tệp đóng mọi kết nối đến ổ đĩa và chuẩn bị cho việc tháo nó ra khỏi hệ thống.