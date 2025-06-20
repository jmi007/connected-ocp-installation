# connected-ocp-installation
connected guide 

***prepararion guide***

1. Cài đặt GUI (Graphical Desktop Environment)
Nếu bạn cài RHEL 9 bản minimal hoặc server, bạn chưa có GUI, nên phải cài thêm:

#sudo dnf groupinstall "Server with GUI"

2. Bật GUI làm mặc định khi khởi động
Chuyển systemd default target sang graphical.target:

#sudo systemctl set-default graphical.target

3. Cài đặt VMware Remote Console trên Fedora
Link: https://iuware.iu.edu/api/file/3518/3826
Giả sử bạn đã tải file VMware-Remote-Console-xxxx.x.x.xxxxxxx.bundle về thư mục ~/Downloads

Mở terminal và chạy:

#cd ~/Downloads
#chmod +x VMware-Remote-Console-xxxx.x.x.xxxxxxx.bundle
#sudo ./VMware-Remote-Console-xxxx.x.x.xxxxxxx.bundle


***Start lab***


1. Thay đổi cấu hình của bastion để thao tác được nhanh hơn: 2vCPU/4GB RAM -> 4vCPU/8GB RAM
   ![image](https://github.com/user-attachments/assets/1d60a0c1-3a9b-44ec-b7ee-48d9e01f6478)

3. ádsada


