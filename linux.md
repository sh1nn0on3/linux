-d  : Tạo thư mục gốc 
-p  : Tạo cây thư mục 
-r  : xóa cả thư mục 
-rm : Xóa thư mục  

# Note

***
sudo su : vào root
su  : quyền user
exit : thoát user
***
lsblk    : hiển thị thông tin ổ đĩa 
fdisk -l : hiển thị chi tiết ổ đĩa và phân vùng 

***
mkdir : tạo thư mục
    ** $ mkdir [path]
cp : copy thư mục và chuyển sang thư mục khác 
    ** $ cp [path_current] [path_new]
mv : chuyển thư mục 
    ** $ mv [path_current] [path_new]
rm -rf : xóa thư mục
    ** $ rm -rf [path]

***
useradd : tạo user 
    ** $ useradd -d /home/[user] -m -s /bin/sh [user]
userdel : xóa user
    ** $ userdel -r [username]
groupadd
    ** $ sudo groupadd [groupname]
    ** $ sudo usermod -aG [groupname] [username]
kickUserGroup
    ** $ sudo deluser [username] [groupname]
groupdel
    ** $ sudo groupdel [groupname]
    ** 

***
usermod
chmod
    ** $ chmod 555 [file]
***
who
w
***
tree
***
nano 
vim 
cat

***
mount : gắn ổ đĩa
umount : gỡ gắn ổ đĩa 

#  Chi tiết 
*  
    ** Viết 
        - nano : đơn giản 
            -- $ nano
            -- ctrl + X
        - vim : phức tạp 
            -- $ vim [nameFile]
            -- i : viết thêm 
            -- esc : thoát 
            -- :wq! : lưu thay đổi và thoát 
    ** Đọc 
        - cat 

# Nén
*
    ** zip 
        - $ zip -r [ten_tep_zip] [ten_thu_muc]
    ** gz 
        - $ tar -czvf [ten_tep_tar].gz [ten_thu_muc]
            - c : tạo tệp tar 
            - z : dùng gzip 
            - v : hiển thị thực hiện
            - f : xác định tên tệp 

# card
*
    ** ip
        - ip addr add [ip] [name]
                ** $ ip addr add 192.168.1.2/24 dev eth0 
        - ip addr del [ip] [name]
        - ip addr show 
        - ip addr show [name]
            ** check 
            **$ ip addr show eth0
    ** network 
        - ip link set [name] up (mở)
            ** $ ip link set dev eth0 up
        - ip link set [name] down (ngắt)
    ** ifconfig

## SSH
*
    $ systemctl start ssh
    $ ssh [name]@[ip]