# connected-ocp-installation
connected guide TBD, by Phat Chau & Tin Nguyen


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
   Chọn SNO để cài đặt trên môi trường lab
   ![image](https://github.com/user-attachments/assets/7ee50c33-d486-4321-a367-9ba18fedef77)

9. Skips 2 oprator này
    ![image](https://github.com/user-attachments/assets/abe57f75-464e-42eb-8d10-1ab0e6b3c200)

11. Add Host
    ![image](https://github.com/user-attachments/assets/d39a15ac-863c-48fc-b717-b5caeafd629e)

13. Chọn Full image file
    ![image](https://github.com/user-attachments/assets/daceeff4-66e1-4944-8a16-d9e5a2eee106)

Và tiến hành Generate Discovery ISO, download về local disk.

15. Login vào Console của VMware vCenter
   
    a. Để upload ISO
    ![image](https://github.com/user-attachments/assets/62d1cc30-313b-432c-a9ee-104099e05fd3)
   b. Tạo 1 VM làm SNO (8vCPU/16G), và boot từ ISO lên. (One host is required with at least 8 CPU cores, 15.00 GiB RAM, and 100 GB disk size)
   Lưu ý: cần phải add Vsphere disk uuid enabled cho VM.
   "disk.EnableUUID TRUE"

![image](https://github.com/user-attachments/assets/b367fd0e-5e10-4a28-b7f2-64887dadb43d)

   ![image](https://github.com/user-attachments/assets/9d4e4faa-d9f6-4e46-9307-e5e0afdc7d39)
   Đợi SNO boot lên và trở lại Red Hat Hybrid Console.
![image](https://github.com/user-attachments/assets/59ac5026-c7ba-494e-8d81-ee365751f9a4)

17. Nhấn Next các bước tiếp theo để tiến hành cài đặt và đợi đến step cuối, Install Cluster 

    ![image](https://github.com/user-attachments/assets/9dd9bcc2-698c-4f84-8d6d-094af137b97a)

19. Cài đặt thành công OVE/OCP Clusters.

    ![image](https://github.com/user-attachments/assets/60c9005a-70b3-4694-8288-07b4ea115f5c)

21. Cấu hình các thông số cho cluster từ ban đầu.

    Tham khảo: https://github.com/vnlabs-ops/agent-based-ocp4-installation?tab=readme-ov-file#m%E1%BB%99t-s%E1%BB%91-thi%E1%BA%BFt-l%E1%BA%ADp-ban-%C4%91%E1%BA%A7u


















