# kubernets-lý thuyết

Kubernetes (K8s) là một nền tảng mã nguồn mở để tự động hóa việc triển khai, mở rộng và quản lý các ứng dụng containerized. Nó hoạt động dựa trên một cụm máy chủ (cluster) và tự động hóa việc quản lý các ứng dụng, tối ưu hóa tài nguyên, theo dõi và tự phục hồi khi có sự cố. Kubernetes giúp giảm thiểu các tác vụ thủ công phức tạp, quản lý kết nối mạng ổn định và mở rộng quy mô theo nhu cầu. 
Cơ chế hoạt động của Kubernetes:

**1. Cụm (Cluster):**

Kubernetes hoạt động trên một cụm gồm các máy chủ (nodes) được chia thành hai loại chính:
Master Node (Node chủ): Chứa các thành phần điều khiển (Control Plane) như API Server, Etcd, Controller Manager và Scheduler. Các thành phần này quản lý và điều phối hoạt động của toàn bộ cụm Kubernetes. 
Worker Nodes (Node worker): Chạy các ứng dụng containerized, còn được gọi là Pod. Mỗi node worker có các thành phần như Kubelet, Kube-proxy và Container Runtime. 

**2. Pod:**

Pod là đơn vị nhỏ nhất trong Kubernetes, chứa một hoặc nhiều container (ví dụ: Docker containers). Pod được quản lý và triển khai trên các node worker. 

**3. Deployment:**

Deployment định nghĩa cách triển khai và cập nhật các ứng dụng. Nó quản lý việc tạo và cập nhật các Pod, đảm bảo ứng dụng luôn hoạt động ở trạng thái mong muốn. 

**4. Service:**

Service định nghĩa cách truy cập các Pod. Nó cung cấp một địa chỉ IP duy nhất và một tập hợp các quy tắc để truy cập các Pod, giúp cân bằng tải và phân phối lưu lượng truy cập.

**5. Controller:**

Kubernetes sử dụng các controller để quản lý các tài nguyên và đảm bảo trạng thái mong muốn của hệ thống. Ví dụ, ReplicaSet controller đảm bảo số lượng Pod luôn đúng như cấu hình, và Deployment controller quản lý việc triển khai và cập nhật ứng dụng. 

**6. API Server:**

API Server là trung tâm giao tiếp của Kubernetes. Nó cho phép người dùng, các thành phần khác và các công cụ quản lý như kubectl tương tác với cụm Kubernetes. 

**7. etcd:**

Etcd là một kho lưu trữ dữ liệu phân tán, lưu trữ trạng thái của cụm Kubernetes, bao gồm thông tin về các Pod, Service, Deployment, v.v. 

**8. Scheduler:**

Scheduler chịu trách nhiệm lên lịch cho các Pod mới trên các node worker, tối ưu hóa việc sử dụng tài nguyên và đáp ứng các yêu cầu của Pod. 

**9. Kubelet:**

Kubelet là một agent chạy trên mỗi node worker, giao tiếp với API Server và quản lý vòng đời của các Pod trên node đó. 

**10. Kube-proxy:**

Kube-proxy là một network proxy chạy trên mỗi node worker, quản lý các kết nối mạng và phân phối lưu lượng truy cập đến các Pod. 

**Tóm lại, Kubernetes hoạt động bằng cách:**

*Tổ chức:*

Phân chia các ứng dụng thành các Pod và triển khai chúng trên các node worker.

*Quản lý:*

Sử dụng Deployment, Service và các Controller để quản lý vòng đời, cập nhật và cân bằng tải cho các ứng dụng.

*Tự động hóa:*

Tự động khởi động lại Pod khi gặp sự cố, mở rộng quy mô ứng dụng theo nhu cầu, và thực hiện các cập nhật an toàn. 

*Tối ưu hóa:*

Tối ưu hóa việc sử dụng tài nguyên và quản lý kết nối mạng. 

<img width="881" height="552" alt="image" src="https://github.com/user-attachments/assets/f588bb32-aebe-4c83-bab0-36aae6373595" />
