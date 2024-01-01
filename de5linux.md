## Câu 1
## Câu 2
## Câu 3
    + Tạo nhóm group 1 và gán vàoi user1
        * Tạo nhóm
            - $ groupadd group1
        * Gán vào User1 
            - $ usermod -aG group1 U1
        * Kiểm tra 
            - $ id U1
        * xem đường dẫn
            - $ pwd U1
## Câu 4
    + Gán quyền cho User123 và G123 với test2.txt
        * cấp quyền cho file
            - $ chmod +wrx test2.txt
        * cấp quyền cho User123 
            - $ chmod User123 test2.txt
    + Nén file test.txt thành file filenen.gz
        * nén
            - $ tar -czvf filenen.gz test.txt
                - c : tạo tệp tar 
                - z : dùng gzip 
                - v : hiển thị thực hiện
                - f : xác định tên tệp 
    + Hiển thị các tiến trình
        * hiển thị 
            - $ ps

