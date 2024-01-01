## Câu 1
## Câu 2
## Câu 3
    + nén thư mục KMA thành file 
        * nén
            - $ tar -czvf KMA.gz kma
                - c : tạo tệp tar 
                - z : dùng gzip 
                - v : hiển thị thực hiện
                - f : xác định tên tệp 
## Câu 4
    + Kiểm tra câus hình máy
        * CPU , Ram , Disk 
            - $ lscpu
            - $ free -h
            - $ df -h
        * Ip máy
            - $ ifconfig
        * Đổi Ip
            - $ ifconfig eth0 192.168.0.100 netmask 255.255.255.0
                --> đổi sao cho khác là được
    + Kiểm tra MTU và thay đổi MTU
        * kiểm tra MTU 
            - $ ip link show
        * đổi 
            - $ ip link set dev eth0 mtu 1400

            
        
            