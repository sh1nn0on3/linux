## Câu 1
    ?? Mã nguồn NukeViet3.0 được cung cấp bởi loại giấy phép nào 
    
    Tính đến thời điểm kiến thức của tôi được cập nhật lần cuối vào tháng 1 năm 2022, NukeViet 3.0 (hoặc NukeViet CMS) sử dụng giấy phép GNU General Public License (GPL), phiên bản 2. Điều này có nghĩa là mã nguồn của NukeViet 3.0 là mã nguồn mở, và bạn có quyền sử dụng, sửa đổi và phân phối mã nguồn này dưới điều kiện của GPL.

    GPL là một giấy phép phổ biến trong cộng đồng mã nguồn mở và đặt ra một số điều kiện để bảo vệ quyền tự do của người sử dụng. Một số điều quan trọng của GPL bao gồm:

    1. Tự do sử dụng: Bạn có quyền tự do sử dụng phần mềm cho bất kỳ mục đích nào.

    2. Tự do nghiên cứu: Bạn có quyền nghiên cứu cách hoạt động của phần mềm và sửa đổi nó theo ý muốn.

    3. Tự do phân phối: Bạn có quyền sao chép và phân phối lại phần mềm.

    4. Tự do cải tiến: Nếu bạn sửa đổi phần mềm, bạn có quyền phân phối lại phiên bản sửa đổi của mình.

## Câu 2 
    ?? Cho biết các thư mục sau gồm những gì : /bin/ ; /dev/ ; /home/

        + /bin/ : Đây là nơi chứa các tập tin thực thi (cung cấp các lệnh hệ thống)
            * ex : cp  , mv , rm , etc
        + /dev/ : Thư mục chứa các tệp tin thiết bị ( đại diện cho phần cứng) 
            * ex : thiết bị như ổ đĩa , bàn phím , các thiết bị thông qua hệ thống
        + /home/ : Đây là thư mục chính của các user trong hệ thống
            * ex : /home/user1

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
    + Xem danh sách ổ địa có trên linux
        * xem ổ đĩa (1 số lệnh - t dùng mỗi các đầu mấy cái dưới tham khảo cũng được )
            - $ lsblk
                -- xem khối lưu trữ , bao gồm ổ đĩa và các vùng
            - $ fdisk -l 
                -- xem chi tiết hơn (-l liệt kê thông tin các ổ đĩa ) 
            - $ df -h 
                -- hiển thi thông tin về không gian đĩa sử dụng và còn trống trong sys (-h xem kích thước của mỗi ổ (gb , mb , kb ,..) )
    + Tạo thư mục /KMA/Security
        * Tạo file
            - $ mkdir /KMA/Security
    + Thực hiện ánh xạ ổ đĩa cdrom vào thư mục /KMA/Security 
        * Gắn ổ đĩa với thư mục
            - $ sudo mount /dev/sd(X) /KMA/Security 
                --> mount : lệnh gắn ổ đĩa 
        * kiểm tra 
            - $ lsblk 
    + Copy file bất kỳ trong /KMA/Security tới ổ đĩa gốc "/THI"
        * đ hiểu đề đ làm :v

## Câu 4
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
            - $ ./sinhvien_bai4.sh
    + Đặt IP tĩnh trên máy chủ Linux 192.168.0.100/255.255.255.0
        * Dùng lệnh cmd
            - $ ifconfig eth0 192.168.0.100 netmask 255.255.255.0
                --> nếu lỗi thì do chưa cho eth0 tạo mới là được
        * kiểm tra 
            - $ ifconfig eth0
    + download từ 1 trang nào đấy
        * 2 cách (cmt lại cho như theo đề bài)
            - $ curl -o [name_file] [url]
            - $ wget -o [name_file] [url]
                --> -o : để đặt tên file url khi tải về 
        