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

Lab guide: https://www.redhat.com/en/blog/how-to-use-the-openshift-assisted-installer

Steps guide help:

1. Thay đổi cấu hình của bastion để thao tác được nhanh hơn: 2vCPU/4GB RAM -> 4vCPU/8GB RAM
   ![image](https://github.com/user-attachments/assets/1d60a0c1-3a9b-44ec-b7ee-48d9e01f6478)

3. Login vào console của bastion, thao tác bằng GUI
   ![image](https://github.com/user-attachments/assets/b019dd97-78ae-4664-a7be-fe7ae39cfbf3)

5. Login vào RedHat Hybrid Console https://console.redhat.com/openshift/assisted-installer/clusters/~new
   ![image](https://github.com/user-attachments/assets/0ee20cbd-7374-469d-9674-44d3c243d854)

7. Bắt đầu tạo Cluster OVE/OCP
   
9. ádasdas




