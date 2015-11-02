#Cài đặt và cấu hình DNS MASTER

- Cài đặt BIND bằng lệnh:
**yum -y install bind**
- vào file cấu hình named.conf chỉ ra những file zone nằm ở vị trí nào và kiểu của file zone, 
**vi /etc/named.conf**
DNS lắng nghe trên cổng 53, thêm địa chỉ mạng mà bạn muốn DNS lắng nghe, các địa chỉ cách nhau dấu ;
allow-query cho phép những địa chỉ ip nào đc truy vấn vào DNS
"." IN tên của 13 Server DNS nằm trong file name.ca
- thêm zone hunter.com kiểu zone là master zone(primary) file chứa những tên phân giải đi hunter.db(có chứa các bản ghi) allow-update là kiểu update cho phép update tự động không? none: không
- thêm zone 0.0.10.in-addr.arpa zone về ip cấu trúc viết ngược của ip kiểu master zone

- Cấu hình file phân giải thuận(phân giải tên thành Ip)


- Cấu hình file phân giải nghịch(phân giải ip thành tên)


- Tắt SELinux chuyển enforcing thành permit hoặc disable
- Sau đó Reboot lại máy
