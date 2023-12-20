# De 1
-  thư mục 
    - xóa thư mục
        + $ rm -r [name]
    - thêm thư mục 
        + $ mkdir [name]

- check user (root)
    + $ who
    + $ w

- Taọ user 
    + $ useradd -m -s /bin/sh U1
        - -m : tạo home cho user
        - -s /bin/sh : cho shell là mặc định của user
            --> dùng /bin/bash nhìn ok hơn 
    + $ useradd -d /home/U1 -m -s /bin/sh U1
        - -d : taọ chỉ mục /home/U1
    + $ sudo passwd [username]
        

- User
    + $ su [username]
    + $ exit

- Xóa user
    + $ userdel -r [username]
        - -r : để xóa hết cả thư mục ( thư mục /home/[username])

- Tạo nhóm G1 gán vào U1
    + Tạo group 
        - $ sudo groupadd [groupname]
    + Xóa group 
        - $ sudo groupdel [groupname]
    + gán User vào Group 
        - $ sudo usermod -aG [groupname] [username]
            + -a : thêm vào 
            + -G : chỉ định nhóm 
    + xóa User ra Group 
        - $ sudo gpasswd -d [username] [groupname]
    + thông tin User có trong group 
        - $ id [username]

- Thư mục 
    + Tạo thư mục
        - $ mkdir [newFolder]
    + Đổi tên thư mục
        - $ rename [currentFolder] [newFolder]
    + Xóa thư mục 
        - $ rm -rf [nameFolder]
    + Di chuyên file từ folder 
        - $ mv [path_current] [path_new]
    + 

- file
    + viết file 
        - $ nano 
    + tạo file 
        - $ mkdir [namefile]
        - $ mkdir [nameFolder]/[nameFile]
        - $ mkdir -p [nameFolder]/[nameFile]
            + -p : dùng khi chưa có folder
    + Copy
        - $ cp [nguon.txt] [dich.txt]
        - $ cp -r [nguon_folder] [dich_folder]
            + -r : lấy cả folder
        -




# Có thể tìm hiểu thêm 

- ls : xem file trong tệp 
    + $ ls -l : xem chi tiết các quyền trong file 
        ++ rw-r--r-- : quyền truy cập của chủ sở hữu 
                ++ rw : quyền đọc - ghi (own)
                ++ rw : quyền đọc - ghi (group - nếu có)
                ++ r  : quyền đọc ( All)
    + ex : -rw-rw-r-- 1 U1 U1 27 Dec 13 21:39 vanban1.txt
        ++  1 : số liên kết với thư mục hiện tại
        ++ U1 : chủ sở hữu 
        ++ U1 : Group user 
        ++ 27 : data (bit)
        ++ Dec : date ( ngày ) 