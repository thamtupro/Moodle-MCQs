// Chapter 1: Getting Started with Knative

// question: 1.1  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Mục tiêu chính của Knative khi khởi tạo là gì?</p>{
	~[moodle]Cung cấp một nền tảng trên Kubernetes để quản lý các distributed databases và messaging queues một cách hiệu quả.#<p>Mặc dù Knative có thể tích hợp với các hệ thống database và messaging, nhưng đó không phải là mục tiêu chính khi nó được khởi tạo. Knative tập trung vào các workload serverless trên Kubernetes.</p>
	=[moodle]Xây dựng, triển khai và quản lý các workload serverless một cách native trên Kubernetes, đơn giản hóa các tác vụ triển khai phức tạp.
	~[moodle]Tối ưu hóa hiệu suất phần cứng và ảo hóa toàn hệ thống cho các ứng dụng đám mây chạy trên Kubernetes.#<p>Knative không tập trung vào việc tối ưu hóa hiệu suất phần cứng hoặc ảo hóa toàn hệ thống; đó là vai trò của Kubernetes và các công nghệ ảo hóa cơ bản. Knative cung cấp một lớp trừu tượng để quản lý các ứng dụng.</p>
	~[moodle]Cung cấp một bộ công cụ hoàn chỉnh để phát triển ứng dụng di động và web trên môi trường đám mây Kubernetes.#<p>Knative là một nền tảng cho các ứng dụng serverless trên Kubernetes, không phải là một bộ công cụ phát triển ứng dụng di động hoặc web cụ thể.</p>
	####<p><strong>Giải thích</strong>\: Knative được khởi tạo với mục tiêu đơn giản là cung cấp một nền tảng native trên Kubernetes để xây dựng, triển khai và quản lý các workload serverless. Nó giúp giải quyết sự phức tạp của Kubernetes trong việc triển khai dịch vụ bằng cách cung cấp các nguyên mẫu middleware cần thiết thông qua một mô hình triển khai đơn giản hơn.</p>
}

// question: 1.2  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Hai khối xây dựng chính của Knative được nhắc đến trong sách là gì?</p>{
	~[moodle]Knative Pipelines và Knative Functions.#<p>Knative Pipelines và Knative Functions không phải là hai khối xây dựng chính được đề cập rõ ràng trong bối cảnh giới thiệu về Knative trong sách.</p>
	~[moodle]Knative Build và Knative Eventing.#<p>Knative Build là một thành phần cũ hơn của Knative, đã được thay thế hoặc phát triển thành các giải pháp khác. Knative Eventing là một khối xây dựng chính.</p>
	=[moodle]Knative Serving và Knative Eventing.
	~[moodle]Knative Gateway và Knative Autoscaler.#<p>Knative Gateway và Knative Autoscaler là các thành phần hoặc khả năng bên trong Knative Serving, không phải là hai khối xây dựng chính của toàn bộ Knative.</p>
	####<p><strong>Giải thích</strong>\: Knative có hai khối xây dựng chính: Knative Serving (dùng để chạy các dịch vụ bên trong Kubernetes với cú pháp triển khai đơn giản, tự động điều chỉnh quy mô từ 0 và mở rộng theo tải HTTP) và Knative Eventing (dùng để kết nối các dịch vụ Knative Serving với các luồng sự kiện ngoài HTTP, ví dụ như Apache Kafka).</p>
}

// question: 1.3  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Để thiết lập một cụm Kubernetes cho môi trường phát triển cục bộ, giải pháp nào được đề xuất trong sách?</p>{
	~[moodle]Sử dụng Google Kubernetes Engine (GKE) hoặc Amazon EKS.#<p>GKE hoặc EKS là các dịch vụ Kubernetes trên đám mây, không phải giải pháp cho môi trường phát triển cục bộ như minikube.</p>
	=[moodle]Sử dụng minikube vì nó cung cấp một cụm Kubernetes một nút phù hợp nhất cho phát triển cục bộ.
	~[moodle]Cài đặt một cụm Kubernetes đa nút hoàn chỉnh với kubeadm trên máy cục bộ.#<p>Cài đặt một cụm Kubernetes đa nút hoàn chỉnh với kubeadm quá phức tạp và tốn tài nguyên cho mục đích phát triển cục bộ được mô tả trong sách.</p>
	~[moodle]Sử dụng OpenShift, nền tảng Kubernetes phân phối của Red Hat, làm cụm cục bộ.#<p>OpenShift là một lựa chọn cho Knative (Chương 7), nhưng minikube được đề xuất cụ thể cho thiết lập cụm Kubernetes cục bộ ban đầu để chạy các công thức trong sách.</p>
	####<p><strong>Giải thích</strong>\: Đối với môi trường phát triển cục bộ, sách đề xuất sử dụng minikube vì nó cung cấp một cụm Kubernetes một nút, rất phù hợp cho phát triển cục bộ.</p>
}

// question: 1.4  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Thành phần cổng vào (ingress gateway) nào được Knative Serving yêu cầu để định tuyến các yêu cầu đến các dịch vụ của nó, và thành phần nào được sử dụng trong các công thức của sách?</p>{
	~[moodle]Ambassador; sách sử dụng Gloo.#<p>Các lựa chọn này sai về cổng vào được sử dụng trong sách hoặc về việc Knative Serving yêu cầu cổng vào.</p>
	~[moodle]Gloo; sách sử dụng Ambassador.#<p>Các lựa chọn này sai về cổng vào được sử dụng trong sách hoặc về việc Knative Serving yêu cầu cổng vào.</p>
	=[moodle]Istio; sách sử dụng Istio.
	~[moodle]Contour; sách sử dụng Contour.#<p>Các lựa chọn này sai về cổng vào được sử dụng trong sách hoặc về việc Knative Serving yêu cầu cổng vào.</p>
	####<p><strong>Giải thích</strong>\: Knative Serving yêu cầu một cổng vào (ingress gateway) để định tuyến các yêu cầu đến các dịch vụ Knative Serving. Sách đề cập rằng nó hỗ trợ các cổng vào dựa trên Envoy như Ambassador, Contour, Gloo và Istio. Trong các công thức của sách, Istio được sử dụng để cài đặt cổng vào.</p>
}

// question: 1.5  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Để cài đặt Registry Container Kubernetes nội bộ trong minikube, lệnh nào được sử dụng?</p>{
	~[moodle]minikube install registry.#<p>Lệnh minikube install registry không được đề cập trong nguồn cho việc cài đặt registry.</p>
	~[moodle]kubectl enable registry -n kube-system.#<p>Lệnh kubectl enable không phải là cách chính xác để bật một addon minikube hoặc cài đặt registry.</p>
	=[moodle]minikube addons enable registry.
	~[moodle]helm install registry.#<p>helm có thể được dùng để triển khai các ứng dụng Kubernetes phức tạp, nhưng đối với registry nội bộ của minikube, addon được ưu tiên hơn.</p>
	####<p><strong>Giải thích</strong>\: Để thiết lập một registry container nội bộ bên trong minikube, bạn cần chạy lệnh: minikube addons enable registry.</p>
}

// question: 1.6  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Các tài nguyên Knative Serving sẽ thuộc nhóm API nào?</p>{
	~[moodle]eventing.knative.dev.#<p>Các nhóm API này thuộc về Knative Eventing, không phải Knative Serving.</p>
	~[moodle]messaging.knative.dev.#<p>Các nhóm API này thuộc về Knative Eventing, không phải Knative Serving.</p>
	~[moodle]sources.eventing.knative.dev.#<p>Các nhóm API này thuộc về Knative Eventing, không phải Knative Serving.</p>
	=[moodle]serving.knative.dev.
	####<p><strong>Giải thích</strong>\: Tất cả các tài nguyên Knative Serving sẽ thuộc nhóm API được gọi là serving.knative.dev.</p>
}

// question: 1.7  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Các tài nguyên Knative Eventing sẽ thuộc những nhóm API nào?</p>{
	~[moodle]serving.knative.dev, build.knative.dev.#<p>serving.knative.dev là nhóm API của Knative Serving. build.knative.dev không phải là nhóm API chính của Eventing được nhắc đến.</p>
	=[moodle]messaging.knative.dev, eventing.knative.dev, sources.eventing.knative.dev, sources.knative.dev.
	~[moodle]networking.knative.dev, flow.knative.dev.#<p>networking.knative.dev là một phần của Serving liên quan đến mạng lưới. flow.knative.dev không được nhắc đến là nhóm API chính.</p>
	~[moodle]traffic.knative.dev, autoscaling.knative.dev.#<p>traffic.knative.dev và autoscaling.knative.dev không phải là các nhóm API chính mà là các khái niệm hoặc annotation liên quan đến Serving.</p>
	####<p><strong>Giải thích</strong>\: Tất cả các tài nguyên Knative Eventing sẽ thuộc một trong các nhóm API sau: messaging.knative.dev, eventing.knative.dev, sources.eventing.knative.dev, và sources.knative.dev.</p>
}

// question: 1.8  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Hai thành phần cơ sở hạ tầng chính của Knative, giúp dịch các CRD của Knative thành các đối tượng Kubernetes như Deployment và Service, là gì?</p>{
	~[moodle]Router và Activator.#<p>Router (Knative Route) và Activator là các thành phần chức năng của Knative Serving.</p>
	=[moodle]Controller và Webhook.
	~[moodle]Autoscaler và Ingress Gateway.#<p>Autoscaler là một thành phần chức năng của Knative Serving, còn Ingress Gateway (ví dụ: Istio) là một dependency bên ngoài.</p>
	~[moodle]Broker và Trigger.#<p>Broker và Trigger là các khái niệm chính trong Knative Eventing.</p>
	####<p><strong>Giải thích</strong>\: Knative có hai thành phần cơ sở hạ tầng chính: controller và webhook. Chúng giúp dịch các Knative CRD, thường được viết trong các tệp YAML, thành các đối tượng Kubernetes như Deployment và Service.</p>
}

// question: 1.9  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Để xác minh môi trường container và cấu hình docker sử dụng minikube, lệnh nào cần được chạy sau khi thiết lập profile?</p>{
	~[moodle]docker info.#<p>docker info hiển thị thông tin chung về Docker daemon nhưng không cấu hình môi trường để sử dụng minikube.</p>
	~[moodle]minikube docker-env && docker images.#<p>Lệnh này thiếu eval để thực thi việc thiết lập biến môi trường trước khi chạy docker images. docker images sau khi eval là bước tiếp theo để kiểm tra.</p>
	=[moodle]eval $(minikube docker-env).
	~[moodle]kubectl get nodes -o wide.#<p>Lệnh này hiển thị thông tin về các node Kubernetes nhưng không liên quan trực tiếp đến việc cấu hình môi trường docker cục bộ để sử dụng minikube.</p>
	####<p><strong>Giải thích</strong>\: Sau khi thiết lập profile minikube (ví dụ: minikube profile knativecookbook), bạn cần chạy lệnh eval $(minikube docker-env) để cấu hình môi trường docker của bạn sử dụng docker daemon của minikube.</p>
}

// question: 1.10  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Tại sao việc sử dụng watch &lt;kubectl command&gt; được ưu tiên hơn trong sách khi theo dõi tài nguyên Kubernetes?</p>{
	~[moodle]Lệnh watch cung cấp output chi tiết hơn và nhiều cột hơn.#<p>Lệnh watch không nhất thiết cung cấp output chi tiết hơn hoặc nhiều cột hơn; nó chỉ thay đổi cách trình bày output của lệnh kubectl get.</p>
	~[moodle]Lệnh watch chỉ hiển thị các thay đổi trạng thái, trong khi kubectl get -w hiển thị toàn bộ output mỗi lần.#<p>watch hiển thị toàn bộ output được làm mới, không chỉ các thay đổi. kubectl get -w cũng hiển thị các thay đổi được nối thêm.</p>
	=[moodle]Lệnh watch có output đơn giản và rõ ràng hơn, được làm mới định kỳ, thay vì nối thêm vào output.
	~[moodle]Lệnh watch sử dụng ít tài nguyên hệ thống hơn khi theo dõi liên tục.#<p>Không có thông tin trong nguồn cho thấy watch sử dụng ít tài nguyên hơn kubectl get -w; sự khác biệt chủ yếu là về định dạng hiển thị.</p>
	####<p><strong>Giải thích</strong>\: Sách giải thích rằng watch &lt;kubectl command&gt; cung cấp output đơn giản và rõ ràng hơn, được làm mới mỗi hai giây, cho phép người dùng theo dõi các thay đổi trạng thái một cách dễ dàng hơn. Ngược lại, kubectl get -w tiếp tục nối thêm vào output, có thể khó đọc hơn.</p>
}

// question: 1.11  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Khi cấu hình bí danh Registry Container, địa chỉ IP cho dev.local và example.com sẽ khớp với địa chỉ IP nào của registry nội bộ?</p>{
	~[moodle]Địa chỉ IP của Node (Node IP).#<p>Các lựa chọn này sai về loại địa chỉ IP mà bí danh sẽ khớp. Bí danh được liên kết với ClusterIP của dịch vụ registry.</p>
	=[moodle]Địa chỉ IP của Cluster (ClusterIP) của registry.
	~[moodle]Địa chỉ IP của Pod của registry.#<p>Các lựa chọn này sai về loại địa chỉ IP mà bí danh sẽ khớp. Bí danh được liên kết với ClusterIP của dịch vụ registry.</p>
	~[moodle]Địa chỉ IP của Service External (ExternalIP) của registry.#<p>Các lựa chọn này sai về loại địa chỉ IP mà bí danh sẽ khớp. Bí danh được liên kết với ClusterIP của dịch vụ registry.</p>
	####<p><strong>Giải thích</strong>\: Địa chỉ IP cho dev.local và example.com sẽ khớp với CLUSTER-IP của registry container nội bộ.</p>
}

// question: 1.12  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Để cập nhật các tên miền tùy chỉnh cho registry container nội bộ, bạn cần thực hiện những bước nào sau khi chỉnh sửa registry-aliases-config.yaml?</p>{
	~[moodle]Chỉ cần chạy lại patch-coredns.sh.#<p>Chỉ chạy patch-coredns.sh sẽ không làm cho daemonset cập nhật các bí danh mới từ ConfigMap.</p>
	=[moodle]Xóa pod daemonset trong namespace kube-system và chạy lại patch-coredns.sh.
	~[moodle]Khởi động lại toàn bộ cụm minikube.#<p>Khởi động lại toàn bộ cụm minikube là một giải pháp quá mức cần thiết và không hiệu quả.</p>
	~[moodle]Chạy kubectl apply -f registry-aliases-config.yaml một lần nữa.#<p>Lệnh này chỉ áp dụng lại ConfigMap, không đảm bảo daemonset sẽ đọc lại cấu hình hoặc CoreDNS được vá lại.</p>
	####<p><strong>Giải thích</strong>\: Sau khi cập nhật ConfigMap registry-aliases-config.yaml, bạn cần khởi động lại daemonset bằng cách xóa pod daemonset trong namespace kube-system. Khi daemonset khởi động lại, nó sẽ lấy các bí danh mới. Sau đó, bạn cần chạy lại script patch-coredns.sh để vá CoreDNS.</p>
}

// question: 1.13  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Phiên bản tối thiểu của Kubernetes mà Knative yêu cầu là gì?</p>{
	~[moodle]v1.13+.#<p>Các phiên bản này thấp hơn phiên bản tối thiểu được yêu cầu chính xác theo nguồn.</p>
	~[moodle]v1.14+.#<p>Các phiên bản này thấp hơn phiên bản tối thiểu được yêu cầu chính xác theo nguồn.</p>
	=[moodle]v1.15+.
	~[moodle]v1.16+.#<p>Các phiên bản này cao hơn phiên bản tối thiểu được yêu cầu chính xác theo nguồn.</p>
	####<p><strong>Giải thích</strong>\: Knative tối thiểu yêu cầu Kubernetes v1.15+; tuy nhiên, sách khuyến nghị sử dụng v1.15.0.</p>
}

// question: 1.14  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>Những loại workload ứng dụng hiện đại nào mà Knative có thể triển khai?</p>{
	~[moodle]Chỉ các ứng dụng Function as a Service (FaaS) nhỏ gọn.#<p>Các lựa chọn này giới hạn loại ứng dụng mà Knative có thể xử lý, không phản ánh khả năng đa dạng của Knative.</p>
	~[moodle]Chỉ các ứng dụng monolithic lớn.#<p>Các lựa chọn này giới hạn loại ứng dụng mà Knative có thể xử lý, không phản ánh khả năng đa dạng của Knative.</p>
	~[moodle]Chỉ các microservices.#<p>Các lựa chọn này giới hạn loại ứng dụng mà Knative có thể xử lý, không phản ánh khả năng đa dạng của Knative.</p>
	=[moodle]Bất kỳ workload ứng dụng hiện đại nào, bao gồm monolithic, microservices hoặc các function nhỏ gọn.
	####<p><strong>Giải thích</strong>\: Trên Knative, bạn có thể triển khai bất kỳ workload ứng dụng hiện đại nào, chẳng hạn như ứng dụng monolithic, microservices hoặc thậm chí các function nhỏ gọn.</p>
}

// question: 1.15  name: Chapter 1: Getting Started with Knative
::Chapter 1\: Getting Started with Knative::[html]<p>"Cookbook" này cấu trúc các ví dụ dưới dạng gì, và tại sao?</p>{
	~[moodle]Dưới dạng các bài tập lý thuyết để cung cấp hiểu biết sâu sắc về các nguyên tắc.#<p>Các lựa chọn này mô tả các cách tiếp cận khác không được sử dụng trong sách này.</p>
	=[moodle]Dưới dạng các "công thức" (recipes), mỗi công thức có một Vấn đề, Giải pháp và Thảo luận với các giải thích chi tiết.
	~[moodle]Dưới dạng các dự án mini, mỗi dự án xây dựng một ứng dụng hoàn chỉnh từ đầu.#<p>Các lựa chọn này mô tả các cách tiếp cận khác không được sử dụng trong sách này.</p>
	~[moodle]Dưới dạng các trường hợp nghiên cứu phức tạp, tập trung vào các triển khai quy mô lớn trong doanh nghiệp.#<p>Các lựa chọn này mô tả các cách tiếp cận khác không được sử dụng trong sách này.</p>
	####<p><strong>Giải thích</strong>\: Cuốn sách này được gọi là "cookbook" vì các ví dụ được cấu trúc dưới dạng "công thức" (recipes), mỗi công thức có một Vấn đề (Problem), Giải pháp (Solution) và Thảo luận (Discussion) với các giải thích chi tiết có thể.</p>
}

// Chapter 2: Understanding Knative Serving

// question: 2.1  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Knative Serving được mô tả là lý tưởng để làm gì trong Kubernetes?</p>{
	~[moodle]Chỉ để chạy các ứng dụng Function as a Service (FaaS) với tính năng scale-to-zero.#<p>Knative Serving không chỉ dành riêng cho FaaS mà còn cho bất kỳ dịch vụ ứng dụng nào.</p>
	=[moodle]Để chạy các dịch vụ ứng dụng bằng cách cung cấp cú pháp triển khai đơn giản, với khả năng tự động điều chỉnh quy mô từ 0 và mở rộng dựa trên tải HTTP.
	~[moodle]Để quản lý các distributed databases và cung cấp giải pháp lưu trữ dữ liệu bền vững.#<p>Knative Serving tập trung vào triển khai và quản lý dịch vụ, không phải quản lý database hoặc lưu trữ dữ liệu bền vững.</p>
	~[moodle]Để thực hiện các tác vụ tích hợp phức tạp giữa các hệ thống kế thừa và hiện đại.#<p>Các tác vụ tích hợp thường được xử lý bởi Knative Eventing hoặc Apache Camel-K (Chương 4, 6), không phải là chức năng chính của Serving.</p>
	####<p><strong>Giải thích</strong>\: Knative Serving lý tưởng để chạy các dịch vụ ứng dụng của bạn bên trong Kubernetes bằng cách cung cấp một cú pháp triển khai đơn giản hơn với khả năng tự động điều chỉnh quy mô từ 0 và mở rộng dựa trên tải HTTP.</p>
}

// question: 2.2  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Khi triển khai một dịch vụ Knative Serving (ksvc), Knative Serving controller tạo ra những tài nguyên Kubernetes nào?</p>{
	~[moodle]Một Pod, một Service và một Ingress.#<p>Mặc dù các tài nguyên này có liên quan, chúng không phải là ba tài nguyên chính mà Knative Serving controller trực tiếp tạo ra từ một ksvc duy nhất.</p>
	=[moodle]Một Configuration, một Revision và một Route.
	~[moodle]Một Deployment, một ReplicaSet và một Endpoint.#<p>Configuration sẽ tạo ra Deployment, Revision và Route, nhưng ba tài nguyên chính được tạo trực tiếp từ ksvc là Configuration, Revision và Route.</p>
	~[moodle]Một StatefulSet, một PersistentVolume và một Gateway.#<p>Các tài nguyên này không liên quan trực tiếp đến mô hình triển khai của Knative Serving.</p>
	####<p><strong>Giải thích</strong>\: Khi triển khai một dịch vụ Knative Serving (ksvc), Knative Serving controller tạo ra một Configuration, một Revision và một Route.</p>
}

// question: 2.3  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Knative Configuration có vai trò gì trong mô hình triển khai Knative Serving?</p>{
	~[moodle]Cung cấp URL mà dịch vụ Knative có thể được truy cập.#<p>Đây là vai trò của Knative Route.</p>
	=[moodle]Duy trì trạng thái mong muốn của triển khai và tạo một Kubernetes Deployment mới cho ứng dụng dựa trên trạng thái đó.
	~[moodle]Tương tự như một thẻ phiên bản kiểm soát và không thể thay đổi.#<p>Đây là mô tả của Knative Revision.</p>
	~[moodle]Chịu trách nhiệm về việc tự động điều chỉnh quy mô (autoscaling) của các pod dịch vụ.#<p>Autoscaling là một khả năng của Knative Serving, được quản lý bởi các thành phần như KPA và HPA, nhưng Configuration không trực tiếp chịu trách nhiệm về cơ chế autoscaling.</p>
	####<p><strong>Giải thích</strong>\: Knative Configuration duy trì trạng thái mong muốn của triển khai của bạn, cung cấp sự tách biệt rõ ràng giữa mã và cấu hình. Dựa trên trạng thái mong muốn, Knative Configuration controller tạo ra một Kubernetes Deployment mới cho ứng dụng của bạn.</p>
}

// question: 2.4  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Knative Revision được mô tả như thế nào và điều gì xảy ra khi Knative Configuration thay đổi?</p>{
	~[moodle]Revision là URL duy nhất để truy cập dịch vụ, sẽ thay đổi mỗi khi cấu hình được cập nhật.#<p>Đây là vai trò của Knative Route.</p>
	=[moodle]Revision là một thẻ hoặc nhãn kiểm soát phiên bản và là bất biến. Mọi thay đổi đối với Knative Configuration sẽ tạo ra một Revision mới.
	~[moodle]Revision là một Kubernetes Deployment có thể được cập nhật tại chỗ mà không tạo ra tài nguyên mới.#<p>Knative Revision có một Kubernetes Deployment tương ứng, nhưng Revision tự nó là bất biến và mọi thay đổi cấu hình sẽ tạo ra một Revision mới.</p>
	~[moodle]Revision là một thành phần mạng định tuyến lưu lượng truy cập giữa các phiên bản dịch vụ.#<p>Việc định tuyến lưu lượng truy cập là nhiệm vụ của Knative Route.</p>
	####<p><strong>Giải thích</strong>\: Knative Revision tương tự như một thẻ hoặc nhãn kiểm soát phiên bản và nó là bất biến (immutable). Mọi thay đổi đối với Knative Configuration sẽ tạo ra một Knative Revision mới.</p>
}

// question: 2.5  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Knative Route có chức năng chính là gì trong mô hình triển khai Knative Serving?</p>{
	~[moodle]Định nghĩa các quy tắc bảo mật và xác thực cho dịch vụ.#<p>Bảo mật và xác thực được xử lý bởi các thành phần khác như Istio (nếu có) hoặc cấu hình ứng dụng.</p>
	~[moodle]Cấu hình tự động điều chỉnh quy mô cho các pod ứng dụng.#<p>Cấu hình autoscaling được quản lý bởi Knative Serving và các ConfigMap liên quan.</p>
	=[moodle]Cung cấp URL mà dịch vụ Knative có thể được truy cập hoặc gọi.
	~[moodle]Quản lý việc lưu trữ và duy trì dữ liệu cho ứng dụng.#<p>Knative không trực tiếp quản lý lưu trữ dữ liệu bền vững cho ứng dụng; đó là nhiệm vụ của Kubernetes Volumes hoặc các dịch vụ bên ngoài.</p>
	####<p><strong>Giải thích</strong>\: Knative Route là URL mà dịch vụ Knative có thể được truy cập hoặc gọi.</p>
}

// question: 2.6  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Khi triển khai một Knative Service lần đầu, mất bao lâu để container image được tải xuống cụm Kubernetes của bạn, và điều này ảnh hưởng đến thời gian triển khai như thế nào?</p>{
	~[moodle]Việc triển khai diễn ra tức thì vì các image container luôn được lưu trữ cục bộ.#<p>Container image không phải lúc nào cũng được lưu trữ cục bộ, đặc biệt là trong lần triển khai đầu tiên.</p>
	=[moodle]Việc triển khai dịch vụ lần đầu tiên sẽ mất thêm thời gian vì container image cần được tải xuống cụm Kubernetes của bạn.
	~[moodle]Việc triển khai chỉ mất thời gian nếu container image không hợp lệ.#<p>Mặc dù image không hợp lệ có thể gây lỗi, nhưng việc tải xuống lần đầu là một yếu tố độc lập gây mất thời gian.</p>
	~[moodle]Không mất thêm thời gian vì Knative tự động nén image để tăng tốc quá trình tải xuống.#<p>Knative không tự động nén image; thời gian tải xuống phụ thuộc vào kích thước image và tốc độ mạng.</p>
	####<p><strong>Giải thích</strong>\: Việc triển khai dịch vụ lần đầu tiên sẽ mất thêm thời gian vì container image cần được tải xuống cụm Kubernetes của bạn.</p>
}

// question: 2.7  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Tại sao Knative Service tự động scale-to-zero (giảm về 0 pod) nếu không được tương tác trong khoảng 60 giây?</p>{
	~[moodle]Để giải phóng tài nguyên CPU cho các dịch vụ khác đang hoạt động trong cụm.#<p>Mặc dù có giải phóng tài nguyên, mục tiêu chính là tiết kiệm chi phí bằng cách không duy trì các tài nguyên không cần thiết.</p>
	~[moodle]Để tự động kiểm tra lỗi và khởi động lại dịch vụ nếu cần.#<p>Scale-to-zero không phải là cơ chế kiểm tra lỗi hoặc khởi động lại; đó là một tính năng quản lý tài nguyên.</p>
	=[moodle]Để tiết kiệm tài nguyên đám mây đắt đỏ bằng cách chấm dứt các pod không hoạt động.
	~[moodle]Để chuẩn bị cho việc cập nhật phiên bản mới của dịch vụ.#<p>Việc chuẩn bị cho cập nhật phiên bản mới là một quy trình riêng biệt, không phải là mục đích của scale-to-zero.</p>
	####<p><strong>Giải thích</strong>\: Knative Serving sẽ tự động scale-to-zero bất kỳ pod Knative Service nào không được sử dụng tích cực. Đây là chìa khóa giúp Knative Serving tiết kiệm tài nguyên đám mây đắt đỏ bằng cách sử dụng các dịch vụ serverless.</p>
}

// question: 2.8  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Theo nguyên tắc của ứng dụng Twelve-Factor, điều gì xảy ra khi có bất kỳ thay đổi nào đối với cấu hình ứng dụng trong Knative?</p>{
	~[moodle]Các thay đổi được áp dụng trực tiếp vào cấu hình hiện có mà không tạo ra phiên bản mới.#<p>Các thay đổi sẽ không được áp dụng trực tiếp mà sẽ tạo ra một Revision mới.</p>
	=[moodle]Một Revision mới được tạo, là trạng thái ứng dụng và cấu hình bất biến.
	~[moodle]Dịch vụ cần được triển khai lại hoàn toàn từ đầu, bao gồm cả việc tạo Route mới.#<p>Việc tạo một Revision mới không nhất thiết yêu cầu triển khai lại toàn bộ dịch vụ hoặc tạo Route mới.</p>
	~[moodle]Chỉ Knative Route được cập nhật để định tuyến lưu lượng đến cấu hình mới.#<p>Route sẽ định tuyến đến Revision mới nhất hoặc Revision được chỉ định, nhưng sự thay đổi cấu hình dẫn đến một Revision mới.</p>
	####<p><strong>Giải thích</strong>\: Nguyên tắc của ứng dụng Twelve-factor phát biểu rằng bất kỳ thay đổi nào đối với cấu hình ứng dụng đều được coi là một revision mới. Một revision là trạng thái ứng dụng và cấu hình bất biến, giúp bạn có khả năng khôi phục về bất kỳ trạng thái tốt đã biết nào trước đó.</p>
}

// question: 2.9  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Khi cập nhật một Knative Service bằng cách thêm một biến môi trường mới, điều gì sẽ xảy ra về mặt Kubernetes Deployment?</p>{
	~[moodle]Knative sẽ cập nhật Deployment hiện có mà không tạo ra cái mới.#<p>Knative sẽ tạo một Deployment mới thay vì cập nhật cái hiện có để đảm bảo tính bất biến của Revision.</p>
	=[moodle]Knative sẽ tạo ra một Kubernetes Deployment mới tương ứng với Revision mới.
	~[moodle]Knative sẽ tạm dừng Deployment cũ và chạy Deployment mới song song.#<p>Knative thường chỉ chạy Deployment mới và scale down cái cũ theo mặc định, không chạy song song trừ khi được cấu hình rõ ràng cho các mô hình phân phối lưu lượng.</p>
	~[moodle]Việc này không ảnh hưởng đến Kubernetes Deployment mà chỉ cập nhật cấu hình nội bộ của Knative.#<p>Thay đổi biến môi trường là một thay đổi cấu hình dẫn đến một Revision mới và một Kubernetes Deployment mới.</p>
	####<p><strong>Giải thích</strong>\: Bất kỳ cập nhật nào cho ứng dụng, chẳng hạn như image container mới, liveness probe được điều chỉnh, hoặc thay đổi biến môi trường, sẽ khiến Knative tạo ra một revision mới. Mọi lần rollout revision mới sẽ tạo ra một Kubernetes Deployment mới.</p>
}

// question: 2.10  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Theo mặc định, Knative Route định tuyến 100% lưu lượng truy cập của người dùng cuối đến phiên bản dịch vụ nào khi có một revision mới được tạo?</p>{
	~[moodle]Định tuyến 100% lưu lượng truy cập đến revision cũ nhất đang hoạt động.#<p>Các lựa chọn này mô tả các hành vi không mặc định hoặc không chính xác của Knative Route khi có revision mới.</p>
	~[moodle]Chia đều lưu lượng truy cập giữa revision cũ và revision mới.#<p>Các lựa chọn này mô tả các hành vi không mặc định hoặc không chính xác của Knative Route khi có revision mới.</p>
	=[moodle]Định tuyến 100% lưu lượng truy cập đến revision mới được tạo.
	~[moodle]Không định tuyến lưu lượng truy cập cho đến khi được cấu hình thủ công.#<p>Các lựa chọn này mô tả các hành vi không mặc định hoặc không chính xác của Knative Route khi có revision mới.</p>
	####<p><strong>Giải thích</strong>\: Knative Route sử dụng Knative Configuration để giữ trạng thái của một Knative Service – tức là cách phân phối lưu lượng truy cập giữa các revision khác nhau. Theo mặc định, nó định tuyến 100% lưu lượng truy cập đến bất kỳ revision mới được tạo nào.</p>
}

// question: 2.11  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Khối traffic trong YAML tài nguyên Knative Service được sử dụng để làm gì?</p>{
	~[moodle]Để xác định các ràng buộc về tài nguyên CPU và bộ nhớ cho dịch vụ.#<p>Các ràng buộc tài nguyên được đặt trong phần spec.template.spec.containers.</p>
	=[moodle]Để kiểm soát việc phân phối lưu lượng truy cập giữa nhiều revision của dịch vụ.
	~[moodle]Để cấu hình thời gian chờ (timeout) cho các yêu cầu HTTP.#<p>Thời gian chờ không được cấu hình trực tiếp trong khối traffic.</p>
	~[moodle]Để chỉ định các biến môi trường cho tất cả các revision của dịch vụ.#<p>Biến môi trường được cấu hình trong phần spec.template.spec.containers.env.</p>
	####<p><strong>Giải thích</strong>\: Khối traffic của YAML tài nguyên Knative Service kiểm soát việc phân phối lưu lượng truy cập giữa nhiều revision của dịch vụ.</p>
}

// question: 2.12  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Khi áp dụng mô hình triển khai Blue-Green với Knative, cách Knative xử lý việc chuyển đổi 100% lưu lượng truy cập từ một Revision (blue) sang một Revision mới (green) như thế nào?</p>{
	~[moodle]Nó yêu cầu triển khai lại toàn bộ dịch vụ để chuyển đổi.#<p>Không cần triển khai lại toàn bộ dịch vụ. Việc cập nhật khối traffic sẽ thực hiện việc chuyển đổi.</p>
	=[moodle]Nó sử dụng khối traffic trong cấu hình Knative Service để chỉ định 100% lưu lượng đến Revision mục tiêu.
	~[moodle]Nó tự động chuyển đổi sau một thời gian chờ đã đặt.#<p>Việc chuyển đổi là do cấu hình, không phải tự động sau thời gian chờ.</p>
	~[moodle]Nó tạo một Knative Route mới cho mỗi Revision (blue và green) để chuyển đổi lưu lượng.#<p>Không tạo Route mới cho mỗi Revision mà Route hiện có sẽ được cập nhật để định tuyến.</p>
	####<p><strong>Giải thích</strong>\: Knative cung cấp một cách đơn giản để chuyển đổi 100% lưu lượng truy cập từ một Knative Service Revision (blue) sang một Revision mới được triển khai (green) bằng cách sử dụng khối traffic trong cấu hình Knative Service để chỉ định 100% lưu lượng đến Revision mong muốn.</p>
}

// question: 2.13  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Mô hình phát hành Canary cho phép bạn làm gì khi triển khai thay đổi ứng dụng vào môi trường production?</p>{
	~[moodle]Chuyển đổi ngay lập tức 100% lưu lượng truy cập sang phiên bản mới để kiểm tra phản ứng.#<p>Điều này phù hợp hơn với Blue-Green deployment.</p>
	~[moodle]Chặn tất cả lưu lượng truy cập đến phiên bản mới cho đến khi được kiểm tra thủ công hoàn toàn.#<p>Chặn tất cả lưu lượng truy cập sẽ không giúp kiểm tra tính năng trong môi trường thực tế.</p>
	=[moodle]Chỉ cho phép một phần nhỏ lưu lượng truy cập của người dùng cuối chảy đến phiên bản đã thay đổi để giảm rủi ro.
	~[moodle]Yêu cầu tất cả người dùng cuối cập nhật ứng dụng của họ để nhận phiên bản mới nhất.#<p>Điều này không liên quan đến cách Canary release hoạt động.</p>
	####<p><strong>Giải thích</strong>\: Một phát hành Canary hiệu quả hơn khi bạn muốn giảm rủi ro khi giới thiệu các tính năng mới. Nó cung cấp một vòng lặp phản hồi tính năng tốt hơn trước khi triển khai thay đổi cho toàn bộ cơ sở người dùng của bạn, bằng cách chỉ cho phép một phần nhỏ lưu lượng truy cập.</p>
}

// question: 2.14  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Giá trị mặc định của livenessProbe và readinessProbe trong Knative Service có gì khác biệt so với các probe Kubernetes tiêu chuẩn?</p>{
	=[moodle]Chúng không có cổng (port) được định nghĩa như một phần của định nghĩa probe.
	~[moodle]Chúng yêu cầu một path khác so với probe Kubernetes tiêu chuẩn.#<p>path có thể tương tự hoặc giống với probe Kubernetes tiêu chuẩn.</p>
	~[moodle]Chúng không hỗ trợ các giao thức HTTP Get.#<p>Chúng vẫn hỗ trợ httpGet.</p>
	~[moodle]Chúng yêu cầu cấu hình xác thực bổ sung.#<p>Không có thông tin trong nguồn cho thấy chúng yêu cầu cấu hình xác thực bổ sung theo cách khác biệt.</p>
	####<p><strong>Giải thích</strong>\: livenessProbe của Knative Service hơi khác so với các probe Kubernetes tiêu chuẩn. Nó không có cổng (port) được định nghĩa như một phần của định nghĩa probe; Knative Serving controller có thể tự động suy ra cổng và cập nhật nó trong giai đoạn triển khai dịch vụ. Quy tắc tương tự cũng áp dụng cho readinessProbe.</p>
}

// question: 2.15  name: Chapter 2: Understanding Knative Serving
::Chapter 2\: Understanding Knative Serving::[html]<p>Tại sao việc thêm tag latest vào khối traffic của Knative Service, khi 100% lưu lượng được định tuyến đến một revision cụ thể (ví dụ: greeter-v1), lại hữu ích?</p>{
	~[moodle]Để đảm bảo rằng revision greeter-v1 luôn được cập nhật với các tính năng mới nhất.#<p>Tag latest trong ngữ cảnh này không đảm bảo greeter-v1 được cập nhật mà là kiểm soát hành vi định tuyến mặc định.</p>
	=[moodle]Để tắt hành vi mặc định của Knative Service là định tuyến 100% lưu lượng đến revision mới nhất.
	~[moodle]Để ưu tiên revision greeter-v1 trong các quyết định tự động điều chỉnh quy mô.#<p>Tag này không trực tiếp ưu tiên autoscaling mà là hành vi định tuyến.</p>
	~[moodle]Để đơn giản hóa việc khôi phục về các phiên bản trước của dịch vụ.#<p>Mặc dù việc ghim traffic giúp khôi phục dễ dàng hơn, mục đích của tag latest trong trường hợp này là ghi đè hành vi mặc định.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn định nghĩa 100% lưu lượng cần đi đến greeter-v1, tag latest có thể được sử dụng để ngăn chặn hành vi mặc định của Knative Service là định tuyến 100% lưu lượng đến revision mới nhất.</p>
}

// Chapter 3: Autoscaling Knative Services

// question: 3.1  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Khả năng tự động điều chỉnh quy mô (autoscaling) của Knative được quản lý bởi những thành phần nào?</p>{
	~[moodle]Kubernetes Ingress và Service Load Balancer.#<p>Ingress và Service Load Balancer là các thành phần mạng chung của Kubernetes.</p>
	~[moodle]Knative Router và Knative Revision Controller.#<p>Knative Router và Revision Controller là các thành phần của Knative Serving nhưng không trực tiếp quản lý việc tự động điều chỉnh quy mô như KPA và HPA.</p>
	=[moodle]Knative Horizontal Pod Autoscaler (KPA) và Horizontal Pod Autoscaler (HPA) của Kubernetes.
	~[moodle]Knative Eventing Brokers và Triggers.#<p>Knative Eventing Brokers và Triggers thuộc về Eventing, không phải là thành phần quản lý autoscaling cho dịch vụ.</p>
	####<p><strong>Giải thích</strong>\: Tính năng tự động điều chỉnh quy mô của Knative được quản lý bởi Knative Horizontal Pod Autoscaler (KPA) và Horizontal Pod Autoscaler (HPA) mặc định được tích hợp trong Kubernetes.</p>
}

// question: 3.2  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>HPA (Horizontal Pod Autoscaler) và KPA (Knative Horizontal Pod Autoscaler) dựa vào ba số liệu quan trọng nào để điều chỉnh quy mô?</p>{
	~[moodle]Network latency, disk I/O, và request count.#<p>Các số liệu này không phải là ba số liệu chính mà HPA và KPA dựa vào theo nguồn.</p>
	=[moodle]Concurrency, requests per second (RPS), và CPU.
	~[moodle]Memory usage, pod startup time, và response time.#<p>Các số liệu này không phải là ba số liệu chính mà HPA và KPA dựa vào theo nguồn.</p>
	~[moodle]Pod uptime, active connections, và error rate.#<p>Các số liệu này không phải là ba số liệu chính mà HPA và KPA dựa vào theo nguồn.</p>
	####<p><strong>Giải thích</strong>\: HPA dựa vào ba số liệu quan trọng: concurrency, requests per second (RPS) và CPU. KPA được coi là phiên bản mở rộng của HPA với một số điều chỉnh để phù hợp hơn với các yêu cầu điều chỉnh quy mô động và dựa trên tải của Knative.</p>
}

// question: 3.3  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Điều gì xảy ra khi một Revision của Knative Serving Service được coi là không hoạt động sau một thời gian nhàn rỗi (idleness)?</p>{
	~[moodle]Knative sẽ di chuyển Revision đó sang một cụm Kubernetes khác để tiết kiệm tài nguyên.#<p>Knative không tự động di chuyển Revision sang cụm khác.</p>
	=[moodle]Knative sẽ chấm dứt tất cả các pod tương ứng với Revision không hoạt động đó (scale-to-zero).
	~[moodle]Knative sẽ tự động cập nhật Revision đó lên phiên bản mới nhất để duy trì hoạt động.#<p>Chấm dứt pod là một phần của scale-to-zero, không phải tự động cập nhật.</p>
	~[moodle]Knative sẽ chuyển tất cả lưu lượng truy cập của Revision đó sang một Revision dự phòng.#<p>Việc chuyển lưu lượng sang Revision dự phòng là một phần của các mô hình triển khai như Blue-Green hoặc Canary, không phải là kết quả mặc định của scale-to-zero.</p>
	####<p><strong>Giải thích</strong>\: Sau một thời gian nhàn rỗi, Revision của Knative Serving Service của bạn được coi là không hoạt động. Knative sẽ chấm dứt tất cả các pod tương ứng với Revision không hoạt động đó (scale-to-zero).</p>
}

// question: 3.4  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Khi một Revision không hoạt động được scale-to-zero, vai trò của dịch vụ activator của Knative Serving là gì?</p>{
	~[moodle]Activator sẽ giữ các pod không hoạt động ở trạng thái ngủ đông cho đến khi có yêu cầu mới.#<p>Activator không giữ các pod ở trạng thái ngủ đông, mà thay vào đó, các pod bị chấm dứt.</p>
	=[moodle]Activator trở thành điểm cuối để nhận và đệm (buffering) lưu lượng HTTP của người dùng cuối, cho phép autoscaler hoạt động.
	~[moodle]Activator sẽ xóa hoàn toàn Revision không hoạt động khỏi cụm Kubernetes.#<p>Activator không xóa Revision mà chỉ xử lý lưu lượng khi Revision đó không hoạt động.</p>
	~[moodle]Activator sẽ tự động tạo một Revision mới và chuyển đổi lưu lượng đến đó.#<p>Activator không tạo Revision mới. Vai trò của nó là xử lý các yêu cầu đến khi dịch vụ đang ở trạng thái scale-to-zero.</p>
	####<p><strong>Giải thích</strong>\: Khi một Revision không hoạt động, các Route cho Revision đó sẽ được ánh xạ đến dịch vụ activator của Knative Serving. activator trở thành điểm cuối để nhận và đệm lưu lượng HTTP của người dùng cuối, cho phép autoscaler (khả năng của Knative Service để điều chỉnh quy mô từ 0 lên n pod) thực hiện nhiệm vụ của mình.</p>
}

// question: 3.5  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Tham số container-concurrency-target-default trong config-autoscaler có chức năng gì?</p>{
	~[moodle]Xác định số lượng CPU mặc định cho mỗi pod dịch vụ.#<p>Số lượng CPU được cấu hình thông qua các thuộc tính khác, không phải container-concurrency-target-default.</p>
	~[moodle]Cấu hình độ trễ khởi động nguội (cold start latency) mặc định.#<p>Độ trễ khởi động nguội là một vấn đề được giải quyết bằng minScale, không phải container-concurrency-target-default.</p>
	=[moodle]Định nghĩa số lượng yêu cầu đồng thời mặc định mà mỗi pod dịch vụ có thể xử lý.
	~[moodle]Thiết lập khoảng thời gian mặc định để theo dõi các yêu cầu.#<p>Khoảng thời gian theo dõi yêu cầu là stable-window.</p>
	####<p><strong>Giải thích</strong>\: Thuộc tính container-concurrency-target-default của ConfigMap config-autoscaler được sử dụng để cấu hình số lượng yêu cầu đồng thời (concurrency) cho mỗi pod dịch vụ.</p>
}

// question: 3.6  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Để bật hoặc tắt tính năng scale-to-zero của Knative, thuộc tính nào trong config-autoscaler cần được cấu hình, và giá trị mặc định của nó là gì?</p>{
	~[moodle]scale-to-zero-grace-period với giá trị mặc định là "30s".#<p>scale-to-zero-grace-period xác định khoảng thời gian chấm dứt các pod không hoạt động.</p>
	~[moodle]stable-window với giá trị mặc định là "60s".#<p>stable-window là khoảng thời gian theo dõi yêu cầu trước khi pod bị coi là không hoạt động.</p>
	=[moodle]enable-scale-to-zero với giá trị mặc định là "true".
	~[moodle]container-concurrency-target-default với giá trị mặc định là "100".#<p>container-concurrency-target-default cấu hình số lượng yêu cầu đồng thời cho mỗi pod.</p>
	####<p><strong>Giải thích</strong>\: Cờ để bật hoặc tắt tính năng giảm quy mô về 0 (scale-to-zero) được kiểm soát bởi thuộc tính enable-scale-to-zero. Giá trị mặc định của nó là "true".</p>
}

// question: 3.7  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Thời gian chấm dứt (termination period) của một pod không được sử dụng là tổng của những khoảng thời gian nào?</p>{
	~[moodle]stable-window và cold start latency.#<p>cold start latency là vấn đề được giải quyết, không phải một khoảng thời gian cộng thêm vào termination period.</p>
	~[moodle]container-concurrency-target-default và scale-to-zero-grace-period.#<p>container-concurrency-target-default là số lượng yêu cầu đồng thời, không phải khoảng thời gian.</p>
	=[moodle]stable-window và scale-to-zero-grace-period.
	~[moodle]stable-window và minScale.#<p>minScale đặt số lượng pod tối thiểu, không phải khoảng thời gian cộng thêm vào termination period.</p>
	####<p><strong>Giải thích</strong>\: Thời gian thực tế mà autoscaler cần để chấm dứt pod không sử dụng (pod không nhận yêu cầu trong stable-window) được đặt là không hoạt động, và thời gian chấm dứt là tổng của stable-window cộng với scale-to-zero-grace-period.</p>
}

// question: 3.8  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Để cấu hình Knative Service xử lý các đợt tăng đột biến yêu cầu bằng cách thay đổi cài đặt đồng thời mặc định, annotation nào được sử dụng?</p>{
	~[moodle]autoscaling.knative.dev/minScale.#<p>minScale được sử dụng để đặt số lượng pod tối thiểu.</p>
	~[moodle]autoscaling.knative.dev/maxScale.#<p>maxScale được sử dụng để đặt số lượng pod tối đa.</p>
	=[moodle]autoscaling.knative.dev/target.
	~[moodle]autoscaling.knative.dev/stable-window.#<p>stable-window là một thuộc tính trong config-autoscaler nhưng không phải là annotation trực tiếp trên dịch vụ để thay đổi cài đặt đồng thời.</p>
	####<p><strong>Giải thích</strong>\: Trong YAML của Knative Serving Service, bạn có thể thêm các annotation sẽ ghi đè hành vi mặc định và các tham số tự động điều chỉnh quy mô. Annotation được sử dụng để cấu hình số lượng yêu cầu đồng thời mục tiêu là autoscaling.knative.dev/target.</p>
}

// question: 3.9  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Mặc định, mỗi pod của Knative Service được cấu hình để xử lý bao nhiêu yêu cầu đồng thời (concurrent requests)?</p>{
	~[moodle]1 yêu cầu.#<p>Các giá trị này không phải là mặc định mà là các giá trị có thể được ghi đè bằng annotation.</p>
	~[moodle]10 yêu cầu.#<p>Các giá trị này không phải là mặc định mà là các giá trị có thể được ghi đè bằng annotation.</p>
	~[moodle]50 yêu cầu.#<p>Các giá trị này không phải là mặc định mà là các giá trị có thể được ghi đè bằng annotation.</p>
	=[moodle]100 yêu cầu.
	####<p><strong>Giải thích</strong>\: Theo mặc định, mỗi pod của Knative Service được cấu hình để xử lý 100 yêu cầu đồng thời từ các client của nó. Thuộc tính container-concurrency-target-default của config-autoscaler ConfigMap được sử dụng để cấu hình độ đồng thời này.</p>
}

// question: 3.10  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Vấn đề chính mà minScale (số lượng pod tối thiểu) giải quyết là gì?</p>{
	~[moodle]Tăng cường bảo mật bằng cách giới hạn số lượng pod hoạt động.#<p>minScale không phải là một tính năng bảo mật mà là tính năng quản lý hiệu suất và độ phản hồi.</p>
	=[moodle]Tránh thời gian chờ liên quan đến việc điều chỉnh quy mô từ 0 lên n pod, còn được gọi là độ trễ khởi động nguội (cold start latency).
	~[moodle]Giảm chi phí tài nguyên bằng cách duy trì số lượng pod thấp nhất có thể.#<p>minScale có thể làm tăng chi phí vì nó giữ một số pod luôn hoạt động, ngược lại với mục tiêu giảm chi phí của scale-to-zero.</p>
	~[moodle]Đảm bảo dịch vụ luôn có đủ tài nguyên CPU để xử lý các yêu cầu.#<p>minScale đảm bảo số lượng pod, nhưng việc có đủ tài nguyên CPU được quản lý bởi các giới hạn tài nguyên và autoscaling nói chung.</p>
	####<p><strong>Giải thích</strong>\: minScale giúp bạn tránh thời gian chờ liên quan đến việc điều chỉnh quy mô từ 0 lên n pod dựa trên khối lượng yêu cầu. Việc khởi động từ 0 và thời gian chờ liên quan được gọi là độ trễ khởi động nguội (cold start latency).</p>
}

// question: 3.11  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Nếu một ứng dụng cần duy trì phản hồi đặc biệt hoặc có thời gian khởi động lâu, kỹ thuật nào được sử dụng để giữ một số lượng pod tối thiểu luôn hoạt động?</p>{
	~[moodle]Sử dụng maxScale để giới hạn số lượng pod tối đa.#<p>maxScale đặt giới hạn trên cho số lượng pod, không phải số lượng pod tối thiểu.</p>
	~[moodle]Tắt tính năng scale-to-zero hoàn toàn.#<p>Tắt scale-to-zero hoàn toàn sẽ giữ tất cả các pod hoạt động, có thể lãng phí tài nguyên hơn việc đặt minScale hợp lý.</p>
	=[moodle]Sử dụng annotation autoscaling.knative.dev/minScale.
	~[moodle]Tăng giá trị stable-window để giữ pod hoạt động lâu hơn.#<p>Tăng stable-window chỉ kéo dài thời gian trước khi pod bị coi là không hoạt động, không đảm bảo số lượng pod tối thiểu.</p>
	####<p><strong>Giải thích</strong>\: Nếu ứng dụng của bạn cần duy trì phản hồi đặc biệt và/hoặc có thời gian khởi động lâu, thì việc giữ một số lượng pod tối thiểu luôn hoạt động có thể có lợi. Kỹ thuật này còn được gọi là làm ấm pod (pod warming), được thực hiện bằng cách thêm annotation autoscaling.knative.dev/minScale vào Knative Service YAML.</p>
}

// question: 3.12  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>maxScale (số lượng pod tối đa) có chức năng gì trong Knative Serving?</p>{
	=[moodle]Đặt giới hạn trên cho số lượng pod mà dịch vụ có thể mở rộng lên để xử lý các yêu cầu.
	~[moodle]Cấu hình số lượng yêu cầu đồng thời tối đa mà mỗi pod có thể xử lý.#<p>Số lượng yêu cầu đồng thời tối đa cho mỗi pod được cấu hình bởi autoscaling.knative.dev/target.</p>
	~[moodle]Định nghĩa thời gian tối đa mà một pod có thể hoạt động trước khi bị chấm dứt.#<p>Thời gian hoạt động tối đa không được định nghĩa trực tiếp bởi maxScale.</p>
	~[moodle]Đảm bảo rằng dịch vụ luôn có đủ pod để xử lý tất cả các yêu cầu đến.#<p>maxScale là giới hạn trên, không phải để đảm bảo đủ pod trong mọi trường hợp, mà là để kiểm soát việc sử dụng tài nguyên.</p>
	####<p><strong>Giải thích</strong>\: Knative theo mặc định không đặt giới hạn trên cho số lượng pod. Để giảm thiểu rủi ro vượt quá giới hạn tài nguyên tính toán của bạn, Knative Serving cho phép bạn thêm annotation autoscaling.knative.dev/maxScale vào Knative Service YAML. Với maxScale, bạn có thể hạn chế giới hạn trên của autoscaler.</p>
}

// question: 3.13  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Công thức để tính toán số lượng pod mục tiêu khi có N yêu cầu đồng thời và C là container-concurrency là gì?</p>{
	~[moodle]số lượng pod = N * C.#<p>Các công thức này không đúng với công thức được cung cấp trong nguồn.</p>
	~[moodle]số lượng pod = C / N.#<p>Các công thức này không đúng với công thức được cung cấp trong nguồn.</p>
	=[moodle]số lượng pod = N / C.
	~[moodle]số lượng pod = N + C.#<p>Các công thức này không đúng với công thức được cung cấp trong nguồn.</p>
	####<p><strong>Giải thích</strong>\: Sách cung cấp công thức để tính số lượng pod mục tiêu là: số lượng pod = tổng số yêu cầu / độ đồng thời của container (container-concurrency).</p>
}

// question: 3.14  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Tại sao service prime-generator được sử dụng trong ví dụ về cấu hình xử lý đột biến yêu cầu lại được thiết kế chậm?</p>{
	~[moodle]Để mô phỏng một ứng dụng đơn giản và phản hồi nhanh chóng.#<p>Ngược lại, nó được thiết kế chậm để quan sát autoscaling.</p>
	=[moodle]Để dễ dàng quan sát hành vi autoscaling khi dịch vụ phản hồi chậm và tải yêu cầu tăng lên.
	~[moodle]Để chứng minh rằng Knative có thể xử lý các ứng dụng không hiệu quả mà không cần tối ưu hóa mã.#<p>Mục đích là để minh họa autoscaling, không phải để chứng minh Knative có thể xử lý các ứng dụng không hiệu quả.</p>
	~[moodle]Để kiểm tra tính ổn định của cụm Kubernetes khi dịch vụ bị treo.#<p>Việc này được thiết kế để kích hoạt autoscaling, không phải để làm treo cụm.</p>
	####<p><strong>Giải thích</strong>\: Vì cần mô phỏng sự chậm chạp trong phản hồi để quan sát việc tự động điều chỉnh quy mô, dịch vụ được sử dụng cho kiểm thử tải là một bộ tạo số nguyên tố sử dụng Sàng Eratosthenes, đây là một trong những cách chậm nhất để tính số nguyên tố. Ứng dụng này cố gắng tăng thêm sự chậm chạp bằng cách thêm tải bộ nhớ, khiến Knative Service phản hồi chậm, từ đó cho phép nó tự động điều chỉnh quy mô (autoscale).</p>
}

// question: 3.15  name: Chapter 3: Autoscaling Knative Services
::Chapter 3\: Autoscaling Knative Services::[html]<p>Sau khi triển khai Knative Service với autoscaling.knative.dev/minScale: "2", điều gì sẽ xảy ra với số lượng pod sau một thời gian không có yêu cầu?</p>{
	~[moodle]Pod sẽ scale-to-zero hoàn toàn.#<p>Scale-to-zero bị ghi đè bởi minScale.</p>
	=[moodle]Số lượng pod sẽ không bao giờ giảm xuống dưới 2, ngay cả khi không có yêu cầu.
	~[moodle]Số lượng pod sẽ giảm xuống 1 để tiết kiệm tài nguyên.#<p>minScale thiết lập sàn là 2, không phải 1.</p>
	~[moodle]Số lượng pod sẽ tăng lên 5 để chờ đợi các yêu cầu tiếp theo.#<p>Tăng lên 5 là maxScale hoặc hành vi mở rộng dựa trên tải, không phải hành vi mặc định khi không có yêu cầu.</p>
	####<p><strong>Giải thích</strong>\: Bạn sẽ nhận thấy rằng prime-generator đã được điều chỉnh quy mô lên 2 bản sao (replicas) như được mô tả bởi giá trị autoscaling.knative.dev/minScale và những pod đó sẽ không tự động giảm quy mô về 0 ngay cả sau thời gian chấm dứt.</p>
}

// Chapter 4: Knative Eventing

// question: 4.1  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Khả năng của Knative Eventing là gì so với Knative Serving?</p>{
	~[moodle]Knative Eventing chỉ cung cấp khả năng tự động điều chỉnh quy mô dựa trên tải HTTP.#<p>Đây là đặc điểm của Knative Serving.</p>
	=[moodle]Knative Eventing mở rộng khả năng tự động điều chỉnh quy mô tới các giao thức hoặc nguồn sự kiện ngoài HTTP, ví dụ như Apache Kafka.
	~[moodle]Knative Eventing chủ yếu được sử dụng để triển khai các ứng dụng web với một cổng vào (ingress gateway).#<p>Đây là đặc điểm của Knative Serving.</p>
	~[moodle]Knative Eventing cho phép Knative Service chạy ở trạng thái "idle" mà không bị scale-to-zero.#<p>Knative Eventing không ngăn Knative Service scale-to-zero; thay vào đó, nó kích hoạt dịch vụ khi có sự kiện.</p>
	####<p><strong>Giải thích</strong>\: Với Knative Serving, bạn có tính năng tự động điều chỉnh quy mô động, bao gồm giảm về 0 pod, dựa trên việc không có tải lưu lượng HTTP. Với Knative Eventing, bạn có cùng khả năng tự động điều chỉnh quy mô đó nhưng được kết nối với các giao thức hoặc từ các nguồn khác ngoài HTTP (ví dụ: một loạt tin nhắn chảy qua một topic Apache Kafka có thể khiến dịch vụ dựa trên Kubernetes của bạn tự động điều chỉnh quy mô để xử lý các tin nhắn đó).</p>
}

// question: 4.2  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>CloudEvents là gì trong ngữ cảnh của Knative Eventing?</p>{
	~[moodle]Một dịch vụ lưu trữ đám mây cho các sự kiện dữ liệu.#<p>Các lựa chọn này sai về bản chất của CloudEvents, đó là một đặc tả, không phải dịch vụ, giao thức hoặc framework phát triển.</p>
	=[moodle]Một đặc tả để mô tả dữ liệu sự kiện theo một cách chung.
	~[moodle]Một giao thức mạng để truyền tải sự kiện giữa các thành phần.#<p>Các lựa chọn này sai về bản chất của CloudEvents, đó là một đặc tả, không phải dịch vụ, giao thức hoặc framework phát triển.</p>
	~[moodle]Một framework phát triển ứng dụng đám mây không máy chủ.#<p>Các lựa chọn này sai về bản chất của CloudEvents, đó là một đặc tả, không phải dịch vụ, giao thức hoặc framework phát triển.</p>
	####<p><strong>Giải thích</strong>\: CloudEvents là một đặc tả để mô tả dữ liệu sự kiện theo một cách chung. Một sự kiện có thể được tạo ra bởi bất kỳ số lượng nguồn nào (ví dụ: Kafka, S3, GCP PubSub, MQTT), và với tư cách là một nhà phát triển phần mềm, bạn muốn một sự trừu tượng hóa chung cho tất cả các đầu vào sự kiện.</p>
}

// question: 4.3  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Mô hình sử dụng Source to Sink trong Knative Eventing có đặc điểm gì?</p>{
	~[moodle]Cung cấp hàng đợi, áp lực ngược (backpressure) và khả năng lọc sự kiện mạnh mẽ.#<p>Các đặc điểm này không có trong mô hình Source to Sink.</p>
	=[moodle]Cung cấp trải nghiệm bắt đầu đơn giản nhất với một Sink duy nhất, không có hàng đợi, áp lực ngược và lọc.
	~[moodle]Hỗ trợ trả lời (replies) từ Sink Service và đảm bảo phản hồi được xử lý.#<p>Source to Sink không hỗ trợ trả lời.</p>
	~[moodle]Được thiết kế để định tuyến sự kiện phức tạp giữa nhiều nguồn và nhiều đích.#<p>Định tuyến sự kiện phức tạp thường được xử lý bởi Channels và Subscriptions, hoặc Brokers và Triggers.</p>
	####<p><strong>Giải thích</strong>\: Source to Sink cung cấp trải nghiệm bắt đầu đơn giản nhất với Knative Eventing. Nó cung cấp một Sink duy nhất (dịch vụ nhận sự kiện) mà không có hàng đợi, áp lực ngược (backpressure) và lọc. Source to Sink không hỗ trợ trả lời (replies), có nghĩa là phản hồi từ Sink Service bị bỏ qua.</p>
}

// question: 4.4  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Mô hình sử dụng Channels and Subscriptions trong Knative Eventing có đặc điểm gì?</p>{
	~[moodle]Nó cho phép lọc sự kiện dựa trên các thuộc tính của CloudEvent.#<p>Mô hình này không có khả năng lọc tin nhắn.</p>
	~[moodle]Mỗi Channel chỉ có thể có một Subscriber duy nhất.#<p>Mỗi Channel có thể có một hoặc nhiều Subscribers.</p>
	=[moodle]Hệ thống Knative Eventing định nghĩa một Channel có thể kết nối với các backend khác nhau, và mỗi Channel có thể có một hoặc nhiều Subscribers.
	~[moodle]Nó là mô hình "fire and forget" không cần chờ phản hồi từ Sink.#<p>Đây là mô tả của mô hình Source to Sink.</p>
	####<p><strong>Giải thích</strong>\: Với Channels and Subscriptions, hệ thống Knative Eventing định nghĩa một Channel, có thể kết nối với các backend khác nhau như In-Memory, Kafka và GCP PubSub để lấy sự kiện. Mỗi Channel có thể có một hoặc nhiều Subscribers dưới dạng Sink Services.</p>
}

// question: 4.5  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Sự khác biệt chính giữa mô hình Brokers and Triggers so với Channels and Subscriptions là gì?</p>{
	~[moodle]Brokers and Triggers không hỗ trợ nhiều Subscribers cho một nguồn sự kiện.#<p>Brokers và Triggers vẫn có thể hỗ trợ nhiều Subscribers thông qua Triggers.</p>
	=[moodle]Brokers and Triggers hỗ trợ lọc sự kiện dựa trên các thuộc tính của CloudEvent.
	~[moodle]Channels and Subscriptions cung cấp khả năng lưu trữ sự kiện bền vững, trong khi Brokers and Triggers thì không.#<p>Channels có thể kết nối với các backend bền vững như Kafka. Brokers cũng ngầm tạo một Channel.</p>
	~[moodle]Brokers and Triggers chỉ làm việc với các nguồn sự kiện nội bộ của Kubernetes.#<p>Brokers và Triggers có thể làm việc với nhiều loại nguồn sự kiện.</p>
	####<p><strong>Giải thích</strong>\: Brokers and Triggers tương tự như Channels and Subscriptions, ngoại trừ việc chúng hỗ trợ lọc sự kiện. Lọc sự kiện là một phương pháp cho phép Subscribers thể hiện sự quan tâm đến một tập hợp tin nhắn nhất định chảy vào Broker.</p>
}

// question: 4.6  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Knative Eventing Sinks có chức năng gì?</p>{
	~[moodle]Tạo sự kiện và gửi chúng đến các nguồn sự kiện bên ngoài.#<p>Việc tạo sự kiện là chức năng của Event Sources.</p>
	=[moodle]Xác định người nhận sự kiện – tức là người tiêu thụ sự kiện.
	~[moodle]Cung cấp một lớp trừu tượng để mô tả dữ liệu sự kiện.#<p>Mô tả dữ liệu sự kiện là chức năng của CloudEvents.</p>
	~[moodle]Quản lý việc tự động điều chỉnh quy mô của các pod sự kiện.#<p>Quản lý autoscaling là chức năng của Knative Serving và autoscaler.</p>
	####<p><strong>Giải thích</strong>\: Knative Eventing Sink là cách bạn chỉ định người nhận sự kiện – tức là người tiêu thụ sự kiện. Sinks có thể được gọi trực tiếp theo kiểu point-to-point bằng cách tham chiếu chúng thông qua sink của Event Source.</p>
}

// question: 4.7  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Bốn loại nguồn Knative Eventing (Sources) được cài đặt sẵn là gì?</p>{
	~[moodle]KafkaSource, GitHubSource, S3Source, CronJobSource.#<p>Các nguồn này có thể là các loại nguồn khác có thể được cài đặt, nhưng không phải là bốn nguồn được cài đặt sẵn mặc định theo nguồn.</p>
	=[moodle]ApiServerSource, ContainerSource, CronJobSource, SinkBinding.
	~[moodle]PrometheusSource, AzureEventHubSource, GoogleCloudStorageSource, RabbitMQSource.#<p>Các nguồn này có thể là các loại nguồn khác có thể được cài đặt, nhưng không phải là bốn nguồn được cài đặt sẵn mặc định theo nguồn.</p>
	~[moodle]HTTPSource, TCPSource, FileSource, DatabaseSource.#<p>Các nguồn này có thể là các loại nguồn khác có thể được cài đặt, nhưng không phải là bốn nguồn được cài đặt sẵn mặc định theo nguồn.</p>
	####<p><strong>Giải thích</strong>\: Knative Eventing Sources cài đặt sẵn bốn nguồn sau: ApiServerSource, ContainerSource, CronJobSource và SinkBinding.</p>
}

// question: 4.8  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>CronJobSource trong Knative Eventing có chức năng chính là gì?</p>{
	~[moodle]Cho phép bạn lắng nghe các sự kiện API của Kubernetes.#<p>Đây là chức năng của ApiServerSource.</p>
	~[moodle]Cho phép bạn tạo container riêng phát ra sự kiện.#<p>Đây là chức năng của ContainerSource.</p>
	=[moodle]Cho phép bạn chỉ định một bộ hẹn giờ cron để phát ra sự kiện định kỳ.
	~[moodle]Cho phép bạn liên kết bất kỳ tài nguyên Kubernetes nào để nhận sự kiện.#<p>Đây là chức năng của SinkBinding.</p>
	####<p><strong>Giải thích</strong>\: CronJobSource cho phép bạn chỉ định một bộ hẹn giờ cron, một tác vụ lặp lại sẽ phát ra một sự kiện đến Sink của bạn một cách định kỳ. CronJobSource thường là cách dễ nhất để xác minh rằng Knative Eventing đang hoạt động đúng cách.</p>
}

// question: 4.9  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Để triển khai một cụm Apache Kafka, giải pháp nào được đề xuất trong sách?</p>{
	~[moodle]Cài đặt Apache Kafka thủ công bằng các binary được tải xuống.#<p>Việc cài đặt thủ công phức tạp hơn và không phải là giải pháp được đề xuất trong sách.</p>
	=[moodle]Sử dụng Strimzi, một operator và tập hợp các CRD để triển khai Apache Kafka bên trong cụm Kubernetes.
	~[moodle]Sử dụng một dịch vụ Kafka được quản lý trên đám mây như Amazon MSK.#<p>Các dịch vụ Kafka trên đám mây là các giải pháp bên ngoài, trong khi sách tập trung vào việc triển khai Kafka bên trong Kubernetes.</p>
	~[moodle]Sử dụng một trình mô phỏng Kafka cục bộ để kiểm thử.#<p>Trình mô phỏng có thể dùng để kiểm thử, nhưng Strimzi được đề xuất để triển khai cụm Kafka thực tế.</p>
	####<p><strong>Giải thích</strong>\: Một trong những cách dễ nhất để triển khai một cụm Apache Kafka là sử dụng Strimzi, một operator và tập hợp các CRD triển khai Apache Kafka bên trong cụm Kubernetes.</p>
}

// question: 4.10  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Knative Eventing events thông qua KafkaSource phải được định dạng theo kiểu gì?</p>{
	~[moodle]XML-formatted.#<p>Các định dạng này không phải là bắt buộc cho các sự kiện từ KafkaSource theo nguồn.</p>
	~[moodle]CSV-formatted.#<p>Các định dạng này không phải là bắt buộc cho các sự kiện từ KafkaSource theo nguồn.</p>
	=[moodle]JSON-formatted.
	~[moodle]YAML-formatted.#<p>Các định dạng này không phải là bắt buộc cho các sự kiện từ KafkaSource theo nguồn.</p>
	####<p><strong>Giải thích</strong>\: Các sự kiện của Knative Eventing thông qua KafkaSource phải được định dạng JSON.</p>
}

// question: 4.11  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Tại sao việc sử dụng Apache Kafka làm backend Channel mặc định cho Knative Eventing lại quan trọng đối với khả năng bền vững (durability) của tin nhắn?</p>{
	~[moodle]InMemoryChannel cung cấp khả năng bền vững tốt hơn Kafka.#<p>InMemoryChannel không có khả năng bền vững tin nhắn.</p>
	=[moodle]Apache Kafka cung cấp khả năng giữ bền vững và duy trì tin nhắn, điều mà InMemoryChannel mặc định không có.
	~[moodle]Nó đơn giản hóa việc triển khai các Knative Service mới.#<p>Việc này phức tạp hơn vì yêu cầu cài đặt Kafka.</p>
	~[moodle]Nó giảm độ trễ cho các sự kiện đi qua Knative Channels.#<p>Việc này có thể ảnh hưởng đến độ trễ nhưng mục đích chính là bền vững.</p>
	####<p><strong>Giải thích</strong>\: Khả năng bền vững (Durability) và tính kiên trì (Persistence) là hai tính năng rất quan trọng của bất kỳ kiến trúc dựa trên tin nhắn nào. Mặc định, tất cả các Knative Channels được tạo bởi Knative Eventing API sử dụng InMemoryChannel (IMC), vốn không có khả năng duy trì tin nhắn. Để bật tính kiên trì, chúng ta cần sử dụng một trong các Channels được hỗ trợ như GCP PubSub, Kafka hoặc NATS làm backend Knative Channel mặc định.</p>
}

// question: 4.12  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Khi Knative Eventing Channel được tạo trong một namespace (ví dụ: chapter-4) đã được cấu hình để sử dụng KafkaChannel làm mặc định, điều gì sẽ xảy ra?</p>{
	~[moodle]Một InMemoryChannel sẽ được tạo để xử lý các sự kiện.#<p>Điều này sẽ không xảy ra nếu KafkaChannel được đặt làm mặc định.</p>
	=[moodle]Một Kafka Topic tương ứng sẽ được tạo.
	~[moodle]Channel sẽ không được tạo cho đến khi một Broker được triển khai.#<p>Channel sẽ được tạo và liên kết với Kafka Topic.</p>
	~[moodle]Knative sẽ từ chối tạo Channel do cấu hình không nhất quán.#<p>Cấu hình là hợp lệ và sẽ hoạt động như mong đợi.</p>
	####<p><strong>Giải thích</strong>\: Vì bạn đã cấu hình tất cả Knative Eventing Channels của chapter-4 là KafkaChannel, việc tạo một Knative Eventing Channel trong namespace chapter-4 sẽ dẫn đến việc một Kafka Topic tương ứng được tạo.</p>
}

// question: 4.13  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Cấu trúc của tên topic Kafka được tạo tự động cho mỗi Knative Eventing Channel theo quy ước nào?</p>{
	~[moodle]&lt;your-channel-name&gt;.&lt;your-channel-namespace&gt;.knative-messaging-kafka.#<p>Các cấu trúc tên topic này không đúng với quy ước được mô tả trong nguồn.</p>
	=[moodle]knative-messaging-kafka.&lt;your-channel-namespace&gt;.&lt;your-channel-name&gt;.
	~[moodle]kafka-topic.&lt;your-channel-namespace&gt;.&lt;your-channel-name&gt;.#<p>Các cấu trúc tên topic này không đúng với quy ước được mô tả trong nguồn.</p>
	~[moodle]default-channel.&lt;your-channel-namespace&gt;.&lt;your-channel-name&gt;.#<p>Các cấu trúc tên topic này không đúng với quy ước được mô tả trong nguồn.</p>
	####<p><strong>Giải thích</strong>\: Đối với mỗi Knative Eventing Channel mà bạn tạo, một Kafka Topic sẽ được tạo. Tên topic sẽ tuân theo quy ước như sau: knative-messaging-kafka.&lt;your-channel-namespace&gt;.&lt;your-channel-name&gt;.</p>
}

// question: 4.14  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Để bật Broker mặc định của Knative Eventing trong một namespace (ví dụ: chapter-4), lệnh nào được sử dụng?</p>{
	~[moodle]kubectl create broker default -n chapter-4.#<p>Các lệnh này không phải là cách chính xác để bật Broker mặc định theo cách được mô tả trong nguồn.</p>
	=[moodle]kubectl label namespace chapter-4 knative-eventing-injection=enabled.
	~[moodle]kubectl apply -f default-broker.yaml -n chapter-4.#<p>Các lệnh này không phải là cách chính xác để bật Broker mặc định theo cách được mô tả trong nguồn.</p>
	~[moodle]minikube addons enable eventing-broker -n chapter-4.#<p>Các lệnh này không phải là cách chính xác để bật Broker mặc định theo cách được mô tả trong nguồn.</p>
	####<p><strong>Giải thích</strong>\: Việc gán nhãn cho namespace chapter-4 với knative-eventing-injection=enabled sẽ khiến Knative Eventing triển khai một Broker mặc định và ingress liên quan của nó.</p>
}

// question: 4.15  name: Chapter 4: Knative Eventing
::Chapter 4\: Knative Eventing::[html]<p>Khi sử dụng Brokers và Triggers, việc lọc sự kiện được áp dụng dựa trên yếu tố nào của tin nhắn?</p>{
	~[moodle]Kích thước (size) của tin nhắn.#<p>Mặc dù các yếu tố này có thể có trong CloudEvent, nhưng bộ lọc được mô tả là áp dụng trên "CloudEvent attributes" nói chung, không chỉ giới hạn ở kích thước, thời gian hoặc tên nguồn.</p>
	~[moodle]Thời gian (timestamp) mà tin nhắn được tạo.#<p>Mặc dù các yếu tố này có thể có trong CloudEvent, nhưng bộ lọc được mô tả là áp dụng trên "CloudEvent attributes" nói chung, không chỉ giới hạn ở kích thước, thời gian hoặc tên nguồn.</p>
	=[moodle]Các thuộc tính của CloudEvent (CloudEvent attributes) của tin nhắn.
	~[moodle]Tên (name) của nguồn tạo ra tin nhắn.#<p>Mặc dù các yếu tố này có thể có trong CloudEvent, nhưng bộ lọc được mô tả là áp dụng trên "CloudEvent attributes" nói chung, không chỉ giới hạn ở kích thước, thời gian hoặc tên nguồn.</p>
	####<p><strong>Giải thích</strong>\: Trigger tự đăng ký vào Broker và áp dụng bộ lọc trên các tin nhắn trong Broker đã đăng ký. Các bộ lọc được áp dụng trên các thuộc tính của CloudEvent (CloudEvent attributes) của tin nhắn, trước khi gửi tin nhắn đến các Sink Services (Subscribers) quan tâm.</p>
}

// Chapter 5: Khả năng quan sát (Observability)

// question: 5.1  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Khả năng quan sát trong Knative được xây dựng dựa trên việc tận dụng Istio như một trong các triển khai cổng vào và gateway của nó, cùng với việc cài đặt thêm những thành phần nào?</p>{
	~[moodle]Nginx, Fluentd và Kibana.#<p>Các lựa chọn này đề cập đến các công cụ khả năng quan sát khác hoặc các công cụ không phải là bộ ba được sử dụng trực tiếp để đạt được khả năng quan sát trong Knative theo nguồn.</p>
	=[moodle]Prometheus, Grafana và Jaeger.
	~[moodle]Elasticsearch, Logstash và Filebeat.#<p>Các lựa chọn này đề cập đến các công cụ khả năng quan sát khác hoặc các công cụ không phải là bộ ba được sử dụng trực tiếp để đạt được khả năng quan sát trong Knative theo nguồn.</p>
	~[moodle]OpenTracing, Zipkin và Kafka.#<p>Các lựa chọn này đề cập đến các công cụ khả năng quan sát khác hoặc các công cụ không phải là bộ ba được sử dụng trực tiếp để đạt được khả năng quan sát trong Knative theo nguồn.</p>
	####<p><strong>Giải thích</strong>\: Knative tận dụng Istio như một trong các triển khai cổng vào và gateway của nó. Nếu một vài thành phần bổ sung – Prometheus, Grafana và Jaeger – được cài đặt trong cụm, thì Istio sẽ được cấu hình để tự động gửi thông tin cho chúng. Do đó, khả năng quan sát trong Knative có thể đạt được bằng cách đơn giản triển khai Prometheus, Grafana và Jaeger vào cụm Kubernetes của bạn.</p>
}

// question: 5.2  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Prometheus được sử dụng để làm gì trong khả năng quan sát của Knative?</p>{
	~[moodle]Thu thập và hiển thị các dấu vết phân tán (distributed traces) của dịch vụ.#<p>Đây là chức năng của Jaeger.</p>
	~[moodle]Phân tích nhật ký (logs) của ứng dụng và các thành phần hệ thống.#<p>Việc phân tích nhật ký là một phần của khả năng quan sát nhưng không phải chức năng chính của Prometheus theo nguồn.</p>
	=[moodle]Thu thập các số liệu (metrics) như mức sử dụng bộ nhớ và CPU từ các pod và dịch vụ.
	~[moodle]Cung cấp một giao diện người dùng để quản lý các dịch vụ Knative.#<p>Giao diện người dùng cho Knative được cung cấp bởi các bảng điều khiển Kubernetes hoặc các công cụ khác, không phải Prometheus.</p>
	####<p><strong>Giải thích</strong>\: Prometheus được sử dụng để thu thập các số liệu (metrics) như mức sử dụng bộ nhớ và CPU từ các pod và dịch vụ của bạn. Dữ liệu đã thu thập sau đó có thể được trực quan hóa bằng cách sử dụng các bảng điều khiển Grafana.</p>
}

// question: 5.3  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Grafana được sử dụng để làm gì trong khả năng quan sát của Knative?</p>{
	~[moodle]Thu thập số liệu và theo dõi hiệu suất của dịch vụ.#<p>Thu thập số liệu là chức năng của Prometheus.</p>
	=[moodle]Trực quan hóa dữ liệu số liệu đã thu thập từ Prometheus bằng cách sử dụng các bảng điều khiển (dashboards).
	~[moodle]Tạo và quản lý các sự kiện trong Knative Eventing.#<p>Knative Eventing quản lý sự kiện, không liên quan trực tiếp đến Grafana.</p>
	~[moodle]Phân tích các dấu vết (traces) phân tán để xác định nút thắt cổ chai.#<p>Phân tích dấu vết là chức năng của Jaeger.</p>
	####<p><strong>Giải thích</strong>\: Prometheus được sử dụng để thu thập các số liệu. Dữ liệu đã thu thập sau đó có thể được trực quan hóa bằng cách sử dụng các bảng điều khiển Grafana.</p>
}

// question: 5.4  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Để hiển thị dịch vụ Prometheus ra bên ngoài cụm Kubernetes bằng NodePort, lệnh nào được sử dụng?</p>{
	~[moodle]kubectl get service -n knative-monitoring prometheus-system-discovery.#<p>Lệnh này chỉ lấy thông tin dịch vụ, không hiển thị nó ra bên ngoài.</p>
	=[moodle]kubectl expose svc -n knative-monitoring prometheus-system-discovery --type=NodePort --name=prometheus-external.
	~[moodle]minikube service -n knative-monitoring prometheus-system-discovery.#<p>Lệnh này sẽ mở trình duyệt đến dịch vụ đã được hiển thị, không phải hiển thị nó.</p>
	~[moodle]kubectl port-forward -n knative-monitoring service/prometheus-system-discovery 9090:9090.#<p>port-forward tạo một kết nối cục bộ tạm thời, không hiển thị dịch vụ bằng NodePort.</p>
	####<p><strong>Giải thích</strong>\: Một trong những cách để truy cập bảng điều khiển Prometheus là sử dụng Kubernetes NodePort. Vì dịch vụ Prometheus theo mặc định chỉ có thể truy cập được bên trong cụm, bạn cần chạy lệnh sau để hiển thị dịch vụ Prometheus bằng NodePort: kubectl expose svc -n knative-monitoring prometheus-system-discovery --type=NodePort --name=prometheus-external.</p>
}

// question: 5.5  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Để cấu hình Knative sử dụng Prometheus cho việc thu thập số liệu, bạn cần vá (patch) nào trong namespace?</p>{
	~[moodle]config-network.#<p>Các ConfigMap này có các chức năng khác (mạng, mặc định, autoscaling) và không phải là nơi cấu hình việc thu thập số liệu của Prometheus.</p>
	~[moodle]config-defaults.#<p>Các ConfigMap này có các chức năng khác (mạng, mặc định, autoscaling) và không phải là nơi cấu hình việc thu thập số liệu của Prometheus.</p>
	=[moodle]config-observability.
	~[moodle]config-autoscaler.#<p>Các ConfigMap này có các chức năng khác (mạng, mặc định, autoscaling) và không phải là nơi cấu hình việc thu thập số liệu của Prometheus.</p>
	####<p><strong>Giải thích</strong>\: Các cấu hình liên quan đến số liệu được lưu trữ trong một ConfigMap có tên là config-observability trong namespace knative-serving. Bạn cần vá ConfigMap này để thu thập số liệu từ các pod Knative của bạn.</p>
}

// question: 5.6  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Jaeger được sử dụng để làm gì trong khả năng quan sát của Knative?</p>{
	~[moodle]Thu thập và trực quan hóa các số liệu về hiệu suất HTTP.#<p>Thu thập và trực quan hóa số liệu là chức năng của Prometheus và Grafana.</p>
	=[moodle]Thực hiện việc theo dõi phân tán (distributed tracing) đầu cuối (end-to-end) bằng cách truyền các header x-b3.
	~[moodle]Quản lý nhật ký và cảnh báo cho các sự kiện hệ thống.#<p>Quản lý nhật ký là một khía cạnh khác của khả năng quan sát.</p>
	~[moodle]Cung cấp một bảng điều khiển tổng quan về trạng thái của cụm Kubernetes.#<p>Các bảng điều khiển tổng quan được cung cấp bởi Grafana hoặc Kubernetes dashboard.</p>
	####<p><strong>Giải thích</strong>\: Jaeger có thể được sử dụng để thực hiện việc theo dõi phân tán (distributed tracing) đầu cuối (end-to-end) bằng cách truyền các header x-b3 như một phần của các yêu cầu HTTP.</p>
}

// question: 5.7  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Để xóa các dấu vết Jaeger hiện có và đưa Jaeger về trạng thái sạch, giải pháp đơn giản nào được đề xuất?</p>{
	~[moodle]Chạy lệnh jaeger clean để xóa dữ liệu.#<p>Lệnh jaeger clean không được đề cập trong nguồn.</p>
	=[moodle]Xóa pod Jaeger trong namespace istio-system và để một pod mới khởi động lại.
	~[moodle]Thay đổi cấu hình Jaeger để lưu trữ dữ liệu vào đĩa thay vì trong bộ nhớ.#<p>Thay đổi cấu hình lưu trữ là một giải pháp phức tạp hơn và không phải là cách được đề xuất để làm sạch nhanh dữ liệu trong bộ nhớ.</p>
	~[moodle]Khởi động lại toàn bộ cụm Kubernetes.#<p>Khởi động lại toàn bộ cụm là quá mức cần thiết.</p>
	####<p><strong>Giải thích</strong>\: Để rõ ràng hơn, việc dọn dẹp các dấu vết Jaeger hiện có được tạo ra từ các lần chạy kiểm thử tải trước đó là tốt. Một giải pháp đơn giản để trở lại trạng thái sạch đã biết là chỉ cần xóa pod Jaeger trong istio-system và để một pod mới khởi động lại vì Jaeger lưu trữ dữ liệu đã cache của nó trong bộ nhớ.</p>
}

// question: 5.8  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Trong ví dụ về các dịch vụ kiểm tra khả năng quan sát, dịch vụ customer được cấu hình là một dịch vụ luôn hoạt động (always-on service) bằng cách nào?</p>{
	~[moodle]Đặt maxScale thành một giá trị lớn.#<p>maxScale đặt giới hạn trên, không phải làm cho dịch vụ luôn hoạt động.</p>
	=[moodle]Cấu hình minScale của nó là 1.
	~[moodle]Gắn nhãn (label) serving.knative.dev/visibility: "public".#<p>Gắn nhãn này liên quan đến khả năng hiển thị, không phải duy trì pod hoạt động.</p>
	~[moodle]Vô hiệu hóa scale-to-zero.#<p>Vô hiệu hóa scale-to-zero sẽ giữ tất cả các pod hoạt động, nhưng minScale: 1 là cách cụ thể để chỉ giữ một pod hoạt động.</p>
	####<p><strong>Giải thích</strong>\: Dịch vụ customer là một dịch vụ luôn hoạt động (always-on service), vì vậy minScale của nó được cấu hình là 1.</p>
}

// question: 5.9  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Mục đích của nhãn serving.knative.dev/visibility trên một Knative Service là gì?</p>{
	~[moodle]Để làm cho dịch vụ chỉ hiển thị công khai bên ngoài cụm.#<p>Ngược lại, nhãn này hạn chế hiển thị công khai.</p>
	=[moodle]Để tạo một route cục bộ (cluster.local) cho dịch vụ, chỉ cho phép truy cập từ bên trong cụm.
	~[moodle]Để tắt hoàn toàn khả năng hiển thị mạng của dịch vụ.#<p>Nhãn này tạo ra một route cluster-local, không tắt hoàn toàn khả năng hiển thị mạng.</p>
	~[moodle]Để định cấu hình dịch vụ sử dụng một cổng (port) ngẫu nhiên.#<p>Nhãn này không liên quan đến cấu hình cổng ngẫu nhiên.</p>
	####<p><strong>Giải thích</strong>\: Mặc định, các Knative Services được hiển thị như các route công khai. Tuy nhiên, nhãn serving.knative.dev/visibility có thể được áp dụng vào YAML dịch vụ và kết quả là một route cluster.local được tạo ra, giới hạn khả năng truy cập dịch vụ chỉ từ bên trong cụm.</p>
}

// question: 5.10  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Ba bảng điều khiển (panels) chính mà dashboard của Grafana cung cấp là gì?</p>{
	~[moodle]Revision Pod Counts, Resource Usage, Autoscaler Metrics.#<p>Đây là các bảng điều khiển của Knative Serving - Scale Debugging dashboard.</p>
	=[moodle]Overview, Request Volume, Response Volume.
	~[moodle]Activator Metrics, Cold Start Latency, Error Rate.#<p>Đây là các số liệu riêng lẻ hoặc các khía cạnh không phải là tên bảng điều khiển chính.</p>
	~[moodle]CPU Usage, Memory Usage, Disk I/O.#<p>Đây là các số liệu riêng lẻ hoặc các khía cạnh không phải là tên bảng điều khiển chính.</p>
	####<p><strong>Giải thích</strong>\: Bảng điều khiển Knative Serving - Revision HTTP Requests có ba bảng: Overview (cung cấp tổng quan về yêu cầu và phản hồi HTTP), Request Volume (cung cấp các số liệu tập trung vào yêu cầu HTTP được phân loại theo revision và mã phản hồi), và Response Volume (cung cấp dữ liệu tập trung vào phản hồi HTTP theo thời gian phản hồi và mã phản hồi).</p>
}

// question: 5.11  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Khi theo dõi dịch vụ trong Grafana, nếu autoscaling.knative.dev/target là 10 và có 50 yêu cầu đồng thời, số lượng pod được điều chỉnh quy mô sẽ là bao nhiêu?</p>{
	~[moodle]2 đến 3 pod.#<p>Các giá trị này không đúng với kết quả dự kiến được cung cấp trong nguồn khi target concurrency là 10 và 50 yêu cầu.</p>
	=[moodle]6 đến 7 pod.
	~[moodle]10 pod.#<p>Các giá trị này không đúng với kết quả dự kiến được cung cấp trong nguồn khi target concurrency là 10 và 50 yêu cầu.</p>
	~[moodle]50 pod.#<p>Các giá trị này không đúng với kết quả dự kiến được cung cấp trong nguồn khi target concurrency là 10 và 50 yêu cầu.</p>
	####<p><strong>Giải thích</strong>\: Sách nêu rõ rằng preference service có thể xử lý tối đa 10 yêu cầu đồng thời (autoscaling.knative.dev/target: "10"). Để mô phỏng việc thu thập số liệu, bạn sẽ chạy một kiểm thử tải với 50 yêu cầu đồng thời. Vì dịch vụ preference chỉ có thể xử lý 10 yêu cầu đồng thời, bạn sẽ thấy preference điều chỉnh quy mô lên khoảng 6 đến 7 pod để xử lý các yêu cầu bổ sung.</p>
}

// question: 5.12  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Bảng điều khiển Autoscaler Metrics trong dashboard cung cấp những số liệu nào?</p>{
	~[moodle]CPU và bộ nhớ sử dụng của Knative Service.#<p>Đây là số liệu được cung cấp bởi bảng Resource Usage.</p>
	=[moodle]Các số liệu xung quanh việc tự động điều chỉnh quy mô của Knative Service, bao gồm số lượng pod, độ đồng thời và Requests Per Second (RPS).
	~[moodle]Số lượng yêu cầu được nhận để kích hoạt dịch vụ Knative.#<p>Đây là số liệu được cung cấp bởi bảng Activator Metrics.</p>
	~[moodle]Các số liệu về yêu cầu và phản hồi HTTP của dịch vụ.#<p>Các số liệu về yêu cầu và phản hồi HTTP được cung cấp bởi Knative Serving - Revision HTTP Requests dashboard.</p>
	####<p><strong>Giải thích</strong>\: Bảng điều khiển Autoscaler Metrics cung cấp các số liệu xung quanh việc tự động điều chỉnh quy mô của một Knative Service, bao gồm các điểm dữ liệu liên quan đến số lượng pod, độ đồng thời và Requests Per Second (RPS) của một Knative Service.</p>
}

// question: 5.13  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Khi sử dụng Jaeger để theo dõi Knative Services, yêu cầu ban đầu đến Knative Service được định tuyến qua thành phần nào?</p>{
	~[moodle]Trực tiếp đến Knative Service.#<p>Không trực tiếp đến Knative Service mà thông qua gateway.</p>
	~[moodle]Thông qua cluster-local-gateway.#<p>cluster-local-gateway được sử dụng cho các cuộc gọi nội bộ giữa các dịch vụ (ví dụ: customer gọi preference).</p>
	=[moodle]Thông qua istio-ingressgateway.
	~[moodle]Thông qua một load balancer nội bộ của Kubernetes.#<p>istio-ingressgateway là một loại load balancer nhưng cụ thể hơn là cổng vào Istio.</p>
	####<p><strong>Giải thích</strong>\: Bạn sẽ nhận thấy rằng cuộc gọi ban đầu đến Knative Service được định tuyến qua istio-ingressgateway.</p>
}

// question: 5.14  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>Giá trị ce-id và ce-source trong CloudEvent logs từ pod (do CronJobSource tạo ra) đại diện cho điều gì?</p>{
	~[moodle]ce-id là tên của pod, ce-source là tên của dịch vụ Knative.#<p>Các lựa chọn này sai về ý nghĩa của ce-id và ce-source trong logs CloudEvent.</p>
	=[moodle]ce-id là một định danh duy nhất của sự kiện, ce-source là nguồn tạo ra sự kiện.
	~[moodle]ce-id là thời gian sự kiện được tạo, ce-source là loại sự kiện.#<p>Các lựa chọn này sai về ý nghĩa của ce-id và ce-source trong logs CloudEvent.</p>
	~[moodle]ce-id là địa chỉ IP của nguồn, ce-source là cổng (port) của nguồn.#<p>Các lựa chọn này sai về ý nghĩa của ce-id và ce-source trong logs CloudEvent.</p>
	####<p><strong>Giải thích</strong>\: Khi theo dõi logs của eventinghello pod, bạn sẽ thấy các thông tin như ce-id=a1e0cbea-8f66-4fa6-8f3c-e5590c4ee147 và ce-source=/apis/v1/namespaces/chapter-5/cronjobsources/eventinghello-cronjob-source. ce-id là ID duy nhất của sự kiện, và ce-source là nguồn tạo ra sự kiện.</p>
}

// question: 5.15  name: Chapter 5: Khả năng quan sát (Observability)
::Chapter 5\: Khả năng quan sát (Observability)::[html]<p>PromQL query được sử dụng để làm gì trong Prometheus dashboard?</p>{
	~[moodle]Để giám sát tổng số yêu cầu HTTP đến các container.#<p>Tổng số yêu cầu HTTP thường được giám sát bằng các số liệu khác như http_requests_total.</p>
	=[moodle]Để kiểm tra dung lượng bộ nhớ RAM mà mỗi container ứng dụng tiêu thụ (Resident Set Size).
	~[moodle]Để theo dõi số lượng lỗi trong các container.#<p>Số lượng lỗi cũng là một số liệu riêng biệt.</p>
	~[moodle]Để xác định số lượng pod đang chạy trong namespace chapter-5.#<p>Số lượng pod đang chạy được kiểm tra bằng lệnh kubectl get pods hoặc qua các bảng điều khiển Grafana khác.</p>
	####<p><strong>Giải thích</strong>\: Bạn có thể chạy PromQL query: container_memory_rss{namespace="chapter-5",container_name="user-container"} trong Prometheus dashboard để xem dung lượng resident set size (RSS) – tức là bộ nhớ không phải đĩa như heap, stack, v.v. – mà mỗi container ứng dụng kiểm thử tiêu thụ.</p>
}

// Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K (Serverless Integration Patterns Using Apache Camel-K)

// question: 6.1  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Apache Camel-K hướng tới mục tiêu chính là gì?</p>{
	~[moodle]Đơn giản hóa việc quản lý cơ sở dữ liệu phân tán trong Kubernetes.#<p>Camel-K tập trung vào tích hợp, không phải quản lý cơ sở dữ liệu phân tán.</p>
	=[moodle]Đơn giản hóa mô hình lập trình và triển khai cho các tích hợp Apache Camel.
	~[moodle]Cung cấp một nền tảng đầy đủ để phát triển giao diện người dùng reactive.#<p>Camel-K không phải là nền tảng phát triển giao diện người dùng.</p>
	~[moodle]Tối ưu hóa hiệu suất của các ứng dụng Java truyền thống trên Kubernetes.#<p>Mặc dù có thể cải thiện việc triển khai các ứng dụng Java, mục tiêu chính là đơn giản hóa tích hợp serverless.</p>
	####<p><strong>Giải thích</strong>\: Apache Camel-K nhằm mục đích đơn giản hóa mô hình lập trình và triển khai cho các tích hợp Apache Camel. Bằng cách làm việc với Apache Camel-K, các nhà phát triển tích hợp giờ đây có thể tập trung vào việc viết các tích hợp của họ bằng Camel DSL mà không cần lo lắng về cách đóng gói và triển khai chúng.</p>
}

// question: 6.2  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Khi cài đặt Camel-K, lệnh command-line tool được sử dụng là gì và cần xác minh phiên bản nào?</p>{
	~[moodle]camelk install, phiên bản 1.0.0-RC2 trở lên.#<p>Tên lệnh không chính xác, phải là kamel.</p>
	=[moodle]kamel install, phiên bản 1.0.0-RC2 trở lên.
	~[moodle]kubectl install camel-k, phiên bản 1.0.0 trở lên.#<p>Không sử dụng kubectl install trực tiếp cho Camel-K.</p>
	~[moodle]minikube addons enable camel-k, phiên bản 0.12.0 trở lên.#<p>minikube addons không phải là cách cài đặt Camel-K.</p>
	####<p><strong>Giải thích</strong>\: Tải xuống phiên bản kamel chính xác cho hệ điều hành của bạn, giải nén binary và thêm nó vào $PATH. Sách đề cập đến việc sử dụng kamel và phiên bản 1.0.0-RC2 hoặc cao hơn. Để cài đặt Camel-K trong cụm của bạn, chạy lệnh kamel install --wait.</p>
}

// question: 6.3  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Trách nhiệm chính của camel-k-operator là gì?</p>{
	~[moodle]Tự động triển khai các dịch vụ Knative Serving khi có yêu cầu.#<p>camel-k-operator triển khai tích hợp dưới dạng Knative Service, không tự động triển khai các dịch vụ Knative Serving theo cách chung chung.</p>
	=[moodle]Tìm kiếm các tích hợp Camel-K được triển khai bằng kamel, và xây dựng, triển khai chúng dưới dạng các ứng dụng Kubernetes.
	~[moodle]Cung cấp một giao diện người dùng đồ họa để quản lý các ứng dụng serverless.#<p>Không có thông tin trong nguồn cho thấy camel-k-operator cung cấp giao diện người dùng.</p>
	~[moodle]Thu thập số liệu và dấu vết (traces) cho các tích hợp Camel-K.#<p>Thu thập số liệu và dấu vết là chức năng của các công cụ khả năng quan sát như Prometheus và Jaeger (Chương 5).</p>
	####<p><strong>Giải thích</strong>\: Trách nhiệm chính của camel-k-operator là tìm kiếm các tích hợp Camel-K được triển khai bằng kamel, và xây dựng, triển khai chúng dưới dạng các ứng dụng Kubernetes.</p>
}

// question: 6.4  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Để làm cho việc xây dựng và triển khai Camel-K nhanh hơn, giải pháp nào được đề xuất liên quan đến cài đặt Maven?</p>{
	~[moodle]Tăng số lượng CPU được cấp phát cho camel-k-operator.#<p>Tăng CPU có thể giúp nhưng không phải là giải pháp trực tiếp để tăng tốc quá trình xây dựng Maven.</p>
	=[moodle]Sử dụng một trình quản lý kho lưu trữ Maven như Sonatype Nexus để lưu vào bộ nhớ cache các artifact Maven.
	~[moodle]Vô hiệu hóa tính năng xây dựng image container trong Camel-K.#<p>Vô hiệu hóa tính năng xây dựng image sẽ làm mất chức năng chính của Camel-K.</p>
	~[moodle]Chuyển sang sử dụng Maven cục bộ trên host thay vì trong cụm.#<p>Việc này không phải là giải pháp được đề xuất để tăng tốc xây dựng trong cụm.</p>
	####<p><strong>Giải thích</strong>\: Một trong những cách để làm cho việc xây dựng nhanh hơn là sử dụng một trình quản lý kho lưu trữ Maven như Sonatype Nexus, giúp lưu vào bộ nhớ cache các artifact Maven từ các kho lưu trữ từ xa và phục vụ chúng từ các kho lưu trữ cục bộ trong những lần tải xuống tiếp theo.</p>
}

// question: 6.5  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Camel-K integration có thể được định nghĩa bằng Camel DSL trong những ngôn ngữ nào?</p>{
	~[moodle]Chỉ Java và XML.#<p>Các lựa chọn này chỉ bao gồm một phần các ngôn ngữ được hỗ trợ hoặc bao gồm các ngôn ngữ không được đề cập.</p>
	=[moodle]Java, JavaScript, Groovy, XML hoặc YAML.
	~[moodle]Chỉ Python và Go.#<p>Các lựa chọn này chỉ bao gồm một phần các ngôn ngữ được hỗ trợ hoặc bao gồm các ngôn ngữ không được đề cập.</p>
	~[moodle]Java, C#, và Ruby.#<p>Các lựa chọn này chỉ bao gồm một phần các ngôn ngữ được hỗ trợ hoặc bao gồm các ngôn ngữ không được đề cập.</p>
	####<p><strong>Giải thích</strong>\: Với Apache Camel-K, các nhà phát triển tích hợp có thể tập trung vào việc viết các tích hợp của họ bằng Camel DSL trong Java, JavaScript, Groovy, XML hoặc YAML.</p>
}

// question: 6.6  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Khi chạy một tích hợp Camel-K với tùy chọn --dev, tính năng nào được cung cấp?</p>{
	~[moodle]Tự động triển khai tích hợp dưới dạng Knative Service.#<p>Triển khai dưới dạng Knative Service là một khả năng của Camel-K, nhưng --dev tập trung vào trải nghiệm phát triển.</p>
	=[moodle]Tail nhật ký từ pod Kubernetes của tích hợp và hỗ trợ đồng bộ hóa các thay đổi nguồn để tự động tải lại Camel context.
	~[moodle]Cấu hình tích hợp để sử dụng một cơ sở dữ liệu phân tán.#<p>--dev không liên quan đến cấu hình cơ sở dữ liệu.</p>
	~[moodle]Giảm kích thước của image container bằng cách loại bỏ các phụ thuộc không cần thiết.#<p>--dev không liên quan trực tiếp đến việc giảm kích thước image.</p>
	####<p><strong>Giải thích</strong>\: Lệnh kamel khởi động tích hợp Camel-K ở chế độ phát triển với tùy chọn --dev. Chế độ phát triển thêm tùy chọn để tail nhật ký từ pod Kubernetes của tích hợp và thêm hỗ trợ để đồng bộ hóa các thay đổi nguồn và tự động tải lại Camel context.</p>
}

// question: 6.7  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Để chạy một tích hợp Camel-K dưới dạng dịch vụ serverless của Knative, Camel-K cần sử dụng thành phần Knative nào?</p>{
	~[moodle]knative:event.#<p>Các lựa chọn này không phải là consumer Knative của Camel-K được sử dụng để triển khai tích hợp dưới dạng Knative Service hoặc xử lý sự kiện Knative Channel.</p>
	~[moodle]knative:broker.#<p>Các lựa chọn này không phải là consumer Knative của Camel-K được sử dụng để triển khai tích hợp dưới dạng Knative Service hoặc xử lý sự kiện Knative Channel.</p>
	=[moodle]knative:endpoint hoặc knative:channel.
	~[moodle]knative:source.#<p>Các lựa chọn này không phải là consumer Knative của Camel-K được sử dụng để triển khai tích hợp dưới dạng Knative Service hoặc xử lý sự kiện Knative Channel.</p>
	####<p><strong>Giải thích</strong>\: Bất kỳ tích hợp Camel-K nào cũng có thể được chuyển đổi thành dịch vụ serverless bằng cách sử dụng Knative. Để một tích hợp được triển khai dưới dạng Knative Service, bạn cần sử dụng thành phần Knative của Camel-K. Thành phần Knative của Camel-K cung cấp hai consumer: knative:endpoint và knative:channel.</p>
}

// question: 6.8  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Khi được sử dụng làm consumer trong tích hợp Camel-K, tên của Knative Service được tạo ra sẽ là gì?</p>{
	~[moodle]knative-endpoint.#<p>Các lựa chọn này không đúng với cách đặt tên dịch vụ dựa trên URI knative:endpoint.</p>
	=[moodle]echoer.
	~[moodle]knative-channel.#<p>Các lựa chọn này không đúng với cách đặt tên dịch vụ dựa trên URI knative:endpoint.</p>
	~[moodle]camel-k-integration.#<p>Các lựa chọn này không đúng với cách đặt tên dịch vụ dựa trên URI knative:endpoint.</p>
	####<p><strong>Giải thích</strong>\: Consumer cần là một URI Knative endpoint có dạng knative:endpoint/&lt;tên endpoint của bạn&gt;. Tên của Knative Service sẽ là phân đoạn đường dẫn cuối cùng của URI; trong trường hợp này, Knative Service của bạn sẽ được gọi là echoer.</p>
}

// question: 6.9  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>CamelSource event source cho phép bạn làm gì trong kiến trúc Knative Eventing?</p>{
	~[moodle]Cho phép tích hợp Camel-K hoạt động như một Knative Event Sink.#<p>CamelSource là một Event Source, không phải Event Sink.</p>
	=[moodle]Cho phép tích hợp Camel-K hoạt động như một Knative Event Source và gửi các exchange Camel (OUT) thông qua Knative Event Sink.
	~[moodle]Cho phép Knative Service gọi một tích hợp Camel-K bằng HTTP POST.#<p>Đó là cách Knative Serving Service được gọi, không phải chức năng của CamelSource.</p>
	~[moodle]Cho phép Camel-K trực tiếp điều chỉnh quy mô các dịch vụ Knative Eventing.#<p>CamelSource không trực tiếp điều chỉnh quy mô các dịch vụ.</p>
	####<p><strong>Giải thích</strong>\: Nguồn sự kiện CamelSource cho phép bạn sử dụng một tích hợp Camel-K như một phần của kiến trúc Knative Eventing. Nói cách đơn giản, bạn có thể làm cho tích hợp Camel-K hoạt động như một Knative Event Source và gửi các exchange Camel (OUT) thông qua một Knative Event Sink.</p>
}

// question: 6.10  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Dịch vụ tiện ích event-display được triển khai để làm gì?</p>{
	~[moodle]Để mô phỏng một nguồn sự kiện và tạo ra các sự kiện mẫu.#<p>Nó là một sink, không phải một nguồn sự kiện.</p>
	=[moodle]Để theo dõi các tin nhắn CloudEvents thô được trao đổi giữa Knative Eventing Channels và Subscribers.
	~[moodle]Để cung cấp một giao diện người dùng cho việc quản lý các tích hợp Camel-K.#<p>Nó không cung cấp giao diện quản lý Camel-K.</p>
	~[moodle]Để thực hiện các phép biến đổi dữ liệu phức tạp trên các sự kiện đến.#<p>Nó chỉ ghi nhật ký các sự kiện, không thực hiện các phép biến đổi phức tạp.</p>
	####<p><strong>Giải thích</strong>\: Để xem các sự kiện được lấy từ CamelSource timed-greeter, bạn cần triển khai một dịch vụ tiện ích có tên là event-display. event-display là một Knative Service, khi được cấu hình làm event sink sẽ đơn giản là ghi nhật ký các CloudEvents thô được tạo từ Knative Event Source của nó.</p>
}

// question: 6.11  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Khi triển khai cùng một tích hợp timed-greeter nhưng lần này là một CamelSource, nó được cấu hình để gửi các sự kiện đến đâu?</p>{
	~[moodle]Một Kafka Topic trực tiếp.#<p>Các lựa chọn này không đúng với cấu hình sink của CamelSource trong ví dụ.</p>
	~[moodle]Một Knative Service khác trong cùng namespace.#<p>Các lựa chọn này không đúng với cấu hình sink của CamelSource trong ví dụ.</p>
	~[moodle]Một Knative Event Channel.#<p>Các lựa chọn này không đúng với cấu hình sink của CamelSource trong ví dụ.</p>
	=[moodle]Dịch vụ event-display như một Sink.
	####<p><strong>Giải thích</strong>\: Trong công thức này, bạn sẽ triển khai cùng một tích hợp timed-greeter mà bạn đã triển khai trước đó, nhưng lần này là một CamelSource. Nguồn sự kiện (CamelSource) được cấu hình để đưa các sự kiện đến sink event-display.</p>
}

// question: 6.12  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Trong mô hình Content Based Router được triển khai với Camel-K, các loại trái cây được phân loại thành "low-sugar", "medium-sugar", và "high-sugar" dựa trên yếu tố nào trong dữ liệu dinh dưỡng của chúng?</p>{
	~[moodle]Lượng carbohydrate.#<p>Các lựa chọn này không phải là yếu tố được sử dụng để phân loại trái cây trong ví dụ.</p>
	~[moodle]Lượng protein.#<p>Các lựa chọn này không phải là yếu tố được sử dụng để phân loại trái cây trong ví dụ.</p>
	=[moodle]Mức đường (sugar level).
	~[moodle]Lượng chất béo (fat).#<p>Các lựa chọn này không phải là yếu tố được sử dụng để phân loại trái cây trong ví dụ.</p>
	####<p><strong>Giải thích</strong>\: Mô hình Content Based Router sử dụng Choice EIP. Trong quá trình xử lý dữ liệu, bạn phân loại các loại trái cây là thấp (đường <= 5), trung bình (đường từ 5 đến 10), và cao (đường > 10) dựa trên mức đường (sugar level) có trong dữ liệu dinh dưỡng của chúng.</p>
}

// question: 6.13  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Header ce-type trong CloudEvents được sử dụng như một thuộc tính bộ lọc (filter attribute) trong thành phần Knative Eventing nào?</p>{
	~[moodle]Knative Channel.#<p>Knative Channel và Subscription không có khả năng lọc sự kiện trực tiếp như Trigger. Broker nhận tất cả các sự kiện, Trigger mới áp dụng bộ lọc.</p>
	~[moodle]Knative Subscription.#<p>Knative Channel và Subscription không có khả năng lọc sự kiện trực tiếp như Trigger. Broker nhận tất cả các sự kiện, Trigger mới áp dụng bộ lọc.</p>
	~[moodle]Knative Broker.#<p>Knative Channel và Subscription không có khả năng lọc sự kiện trực tiếp như Trigger. Broker nhận tất cả các sự kiện, Trigger mới áp dụng bộ lọc.</p>
	=[moodle]Knative Trigger.
	####<p><strong>Giải thích</strong>\: Dựa trên việc phân loại dữ liệu, bạn sẽ đặt CloudEvents type header là low-sugar, medium-sugar và high-sugar. Header này được sử dụng làm một trong các thuộc tính bộ lọc trong Knative Eventing Trigger.</p>
}

// question: 6.14  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Khi triển khai CamelSource, nó được cấu hình để gửi dữ liệu đã xử lý đến đâu?</p>{
	~[moodle]Dịch vụ fruit-events-display trực tiếp.#<p>fruit-events-display là Subscriber, nhận dữ liệu thông qua Trigger.</p>
	~[moodle]Một Kafka Topic khác.#<p>Dữ liệu được lấy từ Kafka Topic fruits, nhưng được gửi đến Broker sau khi xử lý.</p>
	~[moodle]Một dịch vụ Knative Serving riêng biệt.#<p>Nó gửi đến Broker, không phải một dịch vụ Knative Serving riêng biệt theo cách trực tiếp.</p>
	=[moodle]Knative Eventing Broker mặc định.
	####<p><strong>Giải thích</strong>\: Bước cuối cùng là gửi dữ liệu đã xử lý đến Knative Eventing Broker mặc định.</p>
}

// question: 6.15  name: Chapter 6: Các mô hình tích hợp Serverless sử dụng Apache Camel-K
::Chapter 6\: Các mô hình tích hợp Serverless sử dụng Apache Camel-K::[html]<p>Trong ví dụ về Data Producer (fruits-producer), nó sử dụng EIP (Enterprise Integration Pattern) nào để chia mảng JSON từ API trái cây thành các bản ghi riêng lẻ?</p>{
	~[moodle]Content Based Router EIP.#<p>Content Based Router EIP được sử dụng trong Data Processor (fruits-processor).</p>
	~[moodle]Aggregator EIP.#<p>Các EIP này không được đề cập trong ngữ cảnh của fruits-producer.</p>
	=[moodle]Split EIP.
	~[moodle]Message Filter EIP.#<p>Các EIP này không được đề cập trong ngữ cảnh của fruits-producer.</p>
	####<p><strong>Giải thích</strong>\: Dịch vụ fruits-producer sẽ sử dụng một API trái cây công khai để truy xuất thông tin về trái cây và truyền dữ liệu đến Apache Kafka. Dịch vụ fruits-producer truy xuất dữ liệu từ API trái cây, chia nó bằng cách sử dụng Split EIP, sau đó gửi dữ liệu đến một Kafka Topic có tên fruits.</p>
}

// Chapter 7: Knative trên OpenShift

// question: 7.1  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>OpenShift được mô tả là gì?</p>{
	~[moodle]Một hệ điều hành độc lập cho các ứng dụng đám mây.#<p>OpenShift không phải là một hệ điều hành độc lập.</p>
	~[moodle]Một trình ảo hóa (hypervisor) cho các máy ảo hiệu suất cao.#<p>OpenShift dựa trên Kubernetes, không phải một trình ảo hóa.</p>
	=[moodle]Bản phân phối Kubernetes của Red Hat để xây dựng và lưu trữ các ứng dụng đám mây cấp doanh nghiệp.
	~[moodle]Một bộ công cụ phát triển phần mềm độc quyền của Red Hat.#<p>OpenShift là một nền tảng dựa trên Kubernetes, không phải một bộ công cụ phát triển phần mềm độc quyền.</p>
	####<p><strong>Giải thích</strong>\: OpenShift là bản phân phối Kubernetes của Red Hat để xây dựng và lưu trữ các ứng dụng đám mây cấp doanh nghiệp.</p>
}

// question: 7.2  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Knative hỗ trợ cho OpenShift (còn gọi là OpenShift Serverless) chỉ khả dụng từ phiên bản OpenShift nào?</p>{
	~[moodle]OpenShift v3.#<p>Các phiên bản này thấp hơn phiên bản yêu cầu.</p>
	=[moodle]OpenShift v4.
	~[moodle]OpenShift Container Platform v2.#<p>Các phiên bản này thấp hơn phiên bản yêu cầu.</p>
	~[moodle]OpenShift Origin v1.#<p>Các phiên bản này thấp hơn phiên bản yêu cầu.</p>
	####<p><strong>Giải thích</strong>\: Hỗ trợ Knative cho OpenShift (còn gọi là OpenShift Serverless) chỉ khả dụng từ OpenShift v4.</p>
}

// question: 7.3  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Kubernetes Operators có vai trò gì?</p>{
	~[moodle]Cung cấp một giao diện người dùng dựa trên web để quản lý các cụm Kubernetes.#<p>Mặc dù có thể có giao diện người dùng, đây không phải là vai trò chính của Operator.</p>
	=[moodle]Là các tiện ích mở rộng phần mềm cho phép bạn quản lý việc triển khai các ứng dụng và dịch vụ Kubernetes.
	~[moodle]Cung cấp một kho lưu trữ trung tâm cho các image container.#<p>Container registry giải quyết vấn đề này.</p>
	~[moodle]Tự động tối ưu hóa hiệu suất của các ứng dụng đang chạy trong cụm.#<p>Operator quản lý vòng đời ứng dụng, không phải tự động tối ưu hóa hiệu suất.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes Operators là các tiện ích mở rộng phần mềm cho phép bạn quản lý việc triển khai các ứng dụng và dịch vụ Kubernetes. Các Operator không chỉ cung cấp cài đặt tự động mà còn có thể quản lý toàn bộ vòng đời của phần mềm, bao gồm nâng cấp và giám sát.</p>
}

// question: 7.4  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Công cụ command-line trong OpenShift tương tự như công cụ nào trong Kubernetes thuần túy?</p>{
	~[moodle]helm.#<p>helm là một trình quản lý gói cho Kubernetes.</p>
	~[moodle]minikube.#<p>minikube là một công cụ để chạy Kubernetes cục bộ.</p>
	~[moodle]docker.#<p>docker là một client để chạy container Linux.</p>
	=[moodle]kubectl.
	####<p><strong>Giải thích</strong>\: Bạn cũng cần tải xuống phiên bản OpenShift CLI (oc) mới nhất. oc tương tự như kubectl, và nó cho phép bạn tương tác và thực hiện các hoạt động khác nhau trên một cụm OpenShift.</p>
}

// question: 7.5  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Hai cách để cài đặt Knative Operators trên OpenShift là gì?</p>{
	~[moodle]Sử dụng Developer Console và CLI method.#<p>Developer Console là một cách để triển khai Knative Service (Chương 7.2), không phải cài đặt Operator.</p>
	=[moodle]Sử dụng OperatorHub UI qua OpenShift Administrator Console, hoặc sử dụng công cụ command-line oc.
	~[moodle]Chỉ bằng cách tải xuống và chạy các script cài đặt thủ công.#<p>Các lựa chọn này không phải là hai cách chính được đề cập rõ ràng để cài đặt Operator theo nguồn.</p>
	~[moodle]Sử dụng Helm charts hoặc Kustomize.#<p>Các lựa chọn này không phải là hai cách chính được đề cập rõ ràng để cài đặt Operator theo nguồn.</p>
	####<p><strong>Giải thích</strong>\: Có hai cách để cài đặt Knative Operators: sử dụng OperatorHub UI qua OpenShift Administrator Console hoặc sử dụng công cụ command-line oc.</p>
}

// question: 7.6  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>OpenShift Serverless Operator (hay còn gọi là Knative Serving component) cài đặt những gì trước khi cài đặt các thành phần cốt lõi của Knative Serving?</p>{
	~[moodle]Một Kafka Cluster và một Registry Container nội bộ.#<p>Kafka và Registry Container là các phụ thuộc khác được cài đặt riêng (Chương 1, 4).</p>
	=[moodle]Một Istio ingress gateway và Istio pilot trong một namespace gọi là knative-serving-ingress.
	~[moodle]Prometheus và Grafana để giám sát.#<p>Prometheus, Grafana, Elasticsearch và Jaeger là các thành phần khả năng quan sát (Chương 5).</p>
	~[moodle]Một Elasticsearch cluster và Jaeger để tracing.#<p>Prometheus, Grafana, Elasticsearch và Jaeger là các thành phần khả năng quan sát (Chương 5).</p>
	####<p><strong>Giải thích</strong>\: OpenShift Serverless Operator (tức là thành phần Knative Serving) cài đặt một Istio ingress gateway và Istio pilot trong một namespace gọi là knative-serving-ingress, trước khi cài đặt các thành phần cốt lõi của Knative Serving.</p>
}

// question: 7.7  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Theo nguồn, OpenShift Serverless Operator cài đặt những phụ thuộc nào cùng với nó?</p>{
	~[moodle]Chỉ Istio (servicemesh operator).#<p>Các lựa chọn này không đầy đủ hoặc không chính xác về các phụ thuộc được cài đặt.</p>
	=[moodle]Istio (servicemesh operator) và các phụ thuộc của Istio như Jaeger, Kiali và Elasticsearch operators.
	~[moodle]Chỉ Jaeger và Kiali operators.#<p>Các lựa chọn này không đầy đủ hoặc không chính xác về các phụ thuộc được cài đặt.</p>
	~[moodle]Không cài đặt bất kỳ phụ thuộc nào, người dùng phải tự cài đặt.#<p>Các lựa chọn này không đầy đủ hoặc không chính xác về các phụ thuộc được cài đặt.</p>
	####<p><strong>Giải thích</strong>\: Serverless Operator (serverless-operator) không chỉ tự cài đặt mà còn cài đặt các phụ thuộc của nó. Trong trường hợp này, Knative có phụ thuộc vào Istio (servicemesh operator) và Istio có phụ thuộc vào các operator Jaeger, Kiali và Elasticsearch.</p>
}

// question: 7.8  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Hai cách để triển khai một Knative Service trên OpenShift là gì?</p>{
	~[moodle]Chỉ bằng cách sử dụng giao diện người dùng Developer Console.#<p>Không chỉ có Developer Console.</p>
	=[moodle]Phương pháp CLI bằng oc apply -f service.yaml và phương pháp Developer Console.
	~[moodle]Bằng cách sử dụng Helm charts hoặc Operator.#<p>Helm charts không phải là một trong hai phương pháp chính được nêu rõ để triển khai một Knative Service ở đây. Operator được dùng để cài đặt Knative, không phải triển khai dịch vụ.</p>
	~[moodle]Phương pháp CLI và phương pháp API trực tiếp.#<p>Phương pháp API trực tiếp không phải là một trong hai phương pháp được nêu rõ.</p>
	####<p><strong>Giải thích</strong>\: Có hai cách để triển khai một Knative Service trên OpenShift: phương pháp CLI (sử dụng oc apply -f service.yaml) và phương pháp Developer Console.</p>
}

// question: 7.9  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Khi kiểm tra trạng thái của một Knative Route trên OpenShift bằng lệnh oc -n chapter-7 get rt greeter, nếu bạn thấy IngressNotConfigured dưới cột REASON, điều đó có nghĩa là gì?</p>{
	~[moodle]Dịch vụ Knative đã triển khai thành công và sẵn sàng để sử dụng.#<p>Ngược lại, nó có nghĩa là chưa sẵn sàng.</p>
	=[moodle]Knative ingress cho route vẫn đang được tạo và cấu hình.
	~[moodle]Route đã bị xóa và không còn hoạt động.#<p>Nó không có nghĩa là route đã bị xóa.</p>
	~[moodle]Có một lỗi cấu hình trong YAML của Knative Service.#<p>Nó có thể là một lỗi cấu hình tiềm ẩn nhưng trong ngữ cảnh này, nó cho thấy quá trình cấu hình đang diễn ra.</p>
	####<p><strong>Giải thích</strong>\: Khi dịch vụ được triển khai, lệnh oc -n chapter-7 get rt greeter sẽ trả về một phản hồi với IngressNotConfigured dưới REASON, có nghĩa là Knative ingress cho route vẫn đang được tạo và cấu hình.</p>
}

// question: 7.10  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Nếu bạn nhận được thông báo "Application is not available" khi gọi Knative Service trên OpenShift, và oc get ksvc trả về RevisionMissing, lỗi đó có thể là do đâu?</p>{
	~[moodle]Tên miền của dịch vụ (Service domain name) không chính xác.#<p>Mặc dù tên miền không chính xác có thể gây lỗi, RevisionMissing chỉ ra vấn đề với pod, không phải chỉ riêng tên miền.</p>
	=[moodle]Pod không thể được lập lịch (schedule) trong cụm do thiếu tài nguyên.
	~[moodle]Cổng (port) của dịch vụ không được hiển thị ra bên ngoài.#<p>Lỗi này không trực tiếp liên quan đến cổng bị ẩn.</p>
	~[moodle]Knative Serving đã bị gỡ cài đặt khỏi cụm.#<p>Nếu Knative Serving bị gỡ cài đặt, sẽ có các lỗi khác rõ ràng hơn.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn nhận được thông báo "Application is not available", đó là dấu hiệu cho thấy Knative Serving Service của bạn không triển khai thành công. RevisionMissing có thể có nghĩa là pod không thể lập lịch (schedule) trong cụm. Bạn có thể kiểm tra luồng sự kiện của cụm bằng lệnh oc get events --sort-by=.metadata.creationTimestamp và tìm dấu hiệu FailedScheduling.</p>
}

// question: 7.11  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Giải pháp nhanh chóng được đề xuất cho lỗi do tài nguyên CPU không đủ trên OpenShift, đặc biệt trên AWS với kích thước node worker mặc định nhỏ, là gì?</p>{
	~[moodle]Giảm yêu cầu tài nguyên CPU của Knative Service.#<p>Đây là một giải pháp khả thi nhưng không phải là giải pháp "nhanh chóng" hoặc được đề xuất trực tiếp cho vấn đề Insufficient cpu của cluster.</p>
	~[moodle]Xóa và triển khai lại Knative Service nhiều lần.#<p>Việc này không giải quyết nguyên nhân gốc rễ của việc thiếu tài nguyên.</p>
	=[moodle]Tăng pool node worker của bạn thông qua OpenShift Administrator Console.
	~[moodle]Chuyển sang một cluster OpenShift khác có nhiều tài nguyên hơn.#<p>Đây là một giải pháp tốn kém hơn và không phải là giải pháp được đề xuất nhanh chóng.</p>
	####<p><strong>Giải thích</strong>\: Lỗi FailedScheduling cho thấy Insufficient cpu. Giải pháp nhanh chóng là tăng pool node worker của bạn thông qua OpenShift Administrator Console. Quá trình này có thể mất vài phút, nhưng một khi node tham gia cụm, bạn có thể xóa và thêm lại Knative Service.</p>
}

// question: 7.12  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Khi triển khai một Knative Service trên OpenShift bằng Developer Console, sau khi nhập tên image container, bạn cần đảm bảo những tùy chọn nào được chọn?</p>{
	~[moodle]"Create a route to the application" và "Deploy with Git".#<p>"Deploy with Git" là một tùy chọn triển khai khác, không phải luôn cần thiết cho Knative Service.</p>
	=[moodle]"Enable scaling to zero when idle" và "Create a route to the application".
	~[moodle]"Add health checks" và "Enable auto-updates".#<p>Các tùy chọn này không phải là hai tùy chọn chính được nhấn mạnh trong quy trình triển khai Knative Service qua Developer Console.</p>
	~[moodle]"Use a custom build strategy" và "Expose an external port".#<p>Các tùy chọn này không phải là hai tùy chọn chính được nhấn mạnh trong quy trình triển khai Knative Service qua Developer Console.</p>
	####<p><strong>Giải thích</strong>\: Khi triển khai bằng Developer Console, bạn cần chọn hộp kiểm "Enable scaling to zero when idle" và chọn hộp kiểm cho "Create a route to the application", sau đó nhấp vào nút Create.</p>
}

// question: 7.13  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Mục đích của OperatorHub.io là gì?</p>{
	~[moodle]Cung cấp một cổng để mua các giải pháp Operator thương mại.#<p>Mặc dù có thể có các giải pháp thương mại, mục đích chính là chia sẻ và khám phá Operator của cộng đồng.</p>
	=[moodle]Cung cấp một nơi để chia sẻ và khám phá các Operator đã được cộng đồng Kubernetes đóng góp.
	~[moodle]Là một nền tảng để tự động hóa việc tạo các Operator mới.#<p>Các lựa chọn này không phải là mục đích chính của OperatorHub.io.</p>
	~[moodle]Cung cấp tài liệu kỹ thuật chuyên sâu về cách xây dựng Operator.#<p>Các lựa chọn này không phải là mục đích chính của OperatorHub.io.</p>
	####<p><strong>Giải thích</strong>\: OperatorHub.io cung cấp một nơi để chia sẻ và khám phá các Operator đã được cộng đồng Kubernetes đóng góp, chẳng hạn như Apache Kafka, Redis, Jenkins và nhiều loại khác.</p>
}

// question: 7.14  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Kiến trúc cốt lõi của OpenShift tự nó được triển khai dưới dạng gì?</p>{
	~[moodle]Một tập hợp các máy ảo và dịch vụ.#<p>OpenShift chạy trên các máy ảo hoặc bare metal nhưng kiến trúc cốt lõi của nó được định nghĩa bằng CRD và Operator.</p>
	~[moodle]Một tập hợp các Docker Compose files.#<p>Docker Compose được dùng cho quản lý container trên một máy, không phải kiến trúc OpenShift.</p>
	=[moodle]Một chuỗi các Kubernetes Custom Resource Definitions (CRDs) và Operators.
	~[moodle]Một framework phát triển ứng dụng độc lập.#<p>OpenShift là một nền tảng, không phải một framework phát triển ứng dụng độc lập.</p>
	####<p><strong>Giải thích</strong>\: Ở cốt lõi của nó, OpenShift tự nó được triển khai dưới dạng một chuỗi các Kubernetes Custom Resource Definitions (CRDs) và Operators.</p>
}

// question: 7.15  name: Chapter 7: Knative trên OpenShift
::Chapter 7\: Knative trên OpenShift::[html]<p>Sau khi cài đặt OpenShift Serverless Operator, để cài đặt Knative Serving thực tế, bạn cần tạo một project mới có tên là gì?</p>{
	~[moodle]default.#<p>default là namespace mặc định của Kubernetes.</p>
	~[moodle]knative-eventing.#<p>knative-eventing là namespace cho Knative Eventing.</p>
	=[moodle]knative-serving.
	~[moodle]openshift-serverless.#<p>openshift-serverless là tên chung của giải pháp, không phải tên project cụ thể để cài đặt Knative Serving.</p>
	####<p><strong>Giải thích</strong>\: Bây giờ bạn đã cài đặt Serverless Operator, bạn vẫn cần cài đặt Knative Serving thực tế. Tạo một project mới có tên là knative-serving.</p>
}