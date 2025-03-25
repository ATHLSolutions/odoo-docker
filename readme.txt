odoo18/
│
├── data/
│   └── pgdata/
    └── odoo/
    └── nginx/
│
├── nginx/
│   ├── default.conf      # file config nginx
│   
│
├── odoo/
│   ├── Dockerfile
│   ├── odoo.conf
│   ├── entrypoint.sh
│   └── wait-for-pssql.py
├── docker-compose-build.yml # build odoo image
├── docker-compose.yml # dùng image từ docker hub

===================================

docker-compose.yml  : file này sử dụng image chuẩn odoo:18 từ docker hub
docker-compose-build.y,l : file này sử dụng dockerfile từ https://github.com/odoo/docker/blob/master/18.0/Dockerfile và build image

# thực hiện lệnh như sau

docker compose -f "docker-compose-build.yml" up -d --build




Để tạo Git cho project của bạn và upload lên GitHub, bạn có thể làm theo các bước sau:

1. Khởi tạo Git trong thư mục dự án
Mở terminal trong Visual Studio Code (hoặc sử dụng Command Prompt/PowerShell) và chạy lệnh sau:

Lệnh này sẽ khởi tạo một repository Git trong thư mục dự án của bạn.

2. Thêm các file vào Git
Thêm tất cả các file trong thư mục vào Git bằng lệnh:

3. Commit các thay đổi
Tạo một commit đầu tiên với thông điệp:

4. Tạo repository trên GitHub
Truy cập GitHub và đăng nhập.
Nhấn vào nút New (hoặc + > New repository).
Điền tên repository, chọn chế độ Public hoặc Private, sau đó nhấn Create repository.
5. Kết nối repository GitHub với dự án
Sao chép URL của repository vừa tạo (ví dụ: https://github.com/username/repository.git) và chạy lệnh sau trong terminal:

6. Đẩy code lên GitHub
Đẩy code từ máy tính lên GitHub bằng lệnh:

7. Kiểm tra trên GitHub
Truy cập repository trên GitHub để kiểm tra xem code đã được upload thành công chưa.


======================

Khi bạn xóa file trong thư mục dự án và muốn cập nhật thay đổi đó lên GitHub, Git yêu cầu bạn phải thực hiện một commit để ghi nhận sự thay đổi (xóa file) này. Dưới đây là cách xử lý:

1. Kiểm tra trạng thái Git
Chạy lệnh sau để kiểm tra trạng thái của repository:

git status

Bạn sẽ thấy các file bị xóa được liệt kê trong trạng thái "deleted".


2. Thêm thay đổi vào staging
Để thêm các thay đổi (bao gồm việc xóa file) vào staging, chạy lệnh:

git add -u

Lệnh -u sẽ cập nhật tất cả các thay đổi (bao gồm xóa, sửa đổi, hoặc thêm file).

3. Commit thay đổi
Tạo một commit để ghi nhận việc xóa file:

git commit -m "Remove unnecessary files"

4. Đẩy thay đổi lên GitHub
Đẩy commit mới lên GitHub:

git push