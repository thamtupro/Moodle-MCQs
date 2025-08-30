// Chapter 3: Pods: Running Containers in Kubernetes
// Switch category to $module$/top/Chapter 3: Pods: Running Containers in Kubernetes
$CATEGORY: $module$/top/Chapter 3: Pods: Running Containers in Kubernetes

// Question 1
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Đơn vị triển khai cơ bản nhất trong Kubernetes là gì?</p>{
	~[moodle]Container riêng lẻ.#<p>Kubernetes không quản lý các container riêng lẻ trực tiếp; chúng luôn được chạy bên trong một Pod.</p>
	=[moodle]Một nhóm container được đóng gói vào một Pod.
	~[moodle]Một tập hợp các máy ảo chạy ứng dụng.#<p>Pod là một lớp trừu tượng cao hơn các máy ảo; một Pod chạy các container, có thể chạy trên một máy ảo hoặc máy vật lý.</p>
	~[moodle]Một dịch vụ quản lý tài nguyên máy chủ.#<p>Dịch vụ quản lý tài nguyên máy chủ là một chức năng rộng hơn, không phải là đơn vị triển khai cơ bản của ứng dụng.</p>
	####<p><strong>Giải thích</strong>: Pod là một nhóm các container được đặt cùng vị trí (co-located) và đại diện cho khối xây dựng cơ bản nhất trong Kubernetes. Thay vì triển khai từng container riêng lẻ, bạn luôn triển khai và vận hành một Pod.</p>
}

// Question 2
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Điều nào sau đây là ĐÚNG về việc chạy nhiều container trong một Pod?</p>{
	~[moodle]Các container trong cùng một Pod có thể chạy trên các Node khác nhau để phân phối tải.#<p>Các container trong cùng một Pod được thiết kế để đặt cùng vị trí trên cùng một Node và không được phân phối trên các Node khác nhau.</p>
	~[moodle]Mỗi container trong một Pod được cách ly hoàn toàn với các container khác về tài nguyên mạng.#<p>Các container trong cùng một Pod chia sẻ cùng không gian mạng (network namespace) và có thể giao tiếp qua localhost.</p>
	=[moodle]Khi một Pod chứa nhiều container, tất cả chúng phải luôn chạy trên một Node Worker duy nhất.
	~[moodle]Một Pod có thể chứa nhiều container nhưng chúng không thể chia sẻ cùng hệ thống tệp.#<p>Các container trong cùng một Pod có thể chia sẻ các Volume để cùng truy cập dữ liệu.</p>
	####<p><strong>Giải thích</strong>: Khi một Pod chứa nhiều container, tất cả chúng phải luôn chạy trên một Node Worker duy nhất và không bao giờ trải rộng trên nhiều Node Worker.</p>
}

// Question 3
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Vai trò chính của trường spec trong định nghĩa Pod YAML/JSON là gì?</p>{
	~[moodle]Mô tả trạng thái hiện tại của Pod sau khi nó được triển khai và chạy.#<p>Trường status mô tả trạng thái hiện tại của Pod, được Kubernetes cập nhật.</p>
	~[moodle]Chứa thông tin siêu dữ liệu của Pod như tên, nhãn và chú thích.#<p>Trường metadata chứa thông tin siêu dữ liệu như tên, nhãn và chú thích.</p>
	=[moodle]Xác định các thuộc tính mong muốn của Pod, bao gồm danh sách các container và Volume.
	~[moodle]Liệt kê phiên bản API Kubernetes được sử dụng cho tài nguyên này.#<p>Trường apiVersion chỉ ra phiên bản API Kubernetes được sử dụng.</p>
	####<p><strong>Giải thích</strong>: Trường spec (specification) định nghĩa trạng thái mong muốn của Pod, bao gồm danh sách các container, Volume và các thuộc tính khác của Pod.</p>
}

// Question 4
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Nếu một Pod có nhiều container, làm thế nào để bạn xem log của một container cụ thể bằng kubectl logs?</p>{
	~[moodle]Chạy kubectl logs &lt;pod-name&gt; và nó sẽ hiển thị log của tất cả các container.#<p>Nếu không có -c, kubectl logs có thể báo lỗi hoặc hiển thị log của container đầu tiên nếu có nhiều container và không rõ ràng.</p>
	=[moodle]Sử dụng tùy chọn -c &lt;container-name&gt; sau tên Pod: kubectl logs &lt;pod-name&gt; -c &lt;container-name&gt;.
	~[moodle]Log của các container trong Pod không thể xem riêng lẻ mà phải thông qua một công cụ log tập trung.#<p>Mặc dù log tập trung được khuyến nghị, bạn vẫn có thể xem log của từng container bằng kubectl logs.</p>
	~[moodle]Bạn cần kết nối SSH vào Node và truy cập trực tiếp các tệp log của container.#<p>kubectl logs là cách tiêu chuẩn để xem log mà không cần truy cập trực tiếp vào Node, giúp trừu tượng hóa hạ tầng.</p>
	####<p><strong>Giải thích</strong>: Nếu Pod của bạn bao gồm nhiều container, bạn phải chỉ định rõ ràng tên container bằng cách thêm tùy chọn -c &lt;container name&gt; khi chạy kubectl logs.</p>
}

// Question 5
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Vai trò của kubectl port-forward là gì?</p>{
	~[moodle]Triển khai một Pod mới lên cluster Kubernetes.#<p>kubectl run hoặc kubectl create -f được sử dụng để triển khai Pod.</p>
	=[moodle]Cho phép bạn truy cập một dịch vụ chạy bên trong một Pod từ máy cục bộ của bạn.
	~[moodle]Thay đổi IP nội bộ của một Pod thành một địa chỉ IP công khai.#<p>kubectl port-forward tạo một đường hầm tạm thời, không thay đổi địa chỉ IP thực của Pod.</p>
	~[moodle]Xem trạng thái và thông tin chi tiết về các Node trong cluster.#<p>kubectl get nodes hoặc kubectl describe node được sử dụng để xem thông tin Node.</p>
	####<p><strong>Giải thích</strong>: Lệnh kubectl port-forward cho phép bạn chuyển tiếp các yêu cầu từ một cổng cục bộ trên máy của bạn đến một cổng trên Pod đang chạy trong cluster, giúp truy cập các dịch vụ nội bộ từ máy cục bộ.</p>
}

// Question 6
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Ưu điểm chính của việc sử dụng các tệp YAML để định nghĩa tài nguyên Kubernetes là gì?</p>{
	~[moodle]Chúng cho phép cấu hình các tài nguyên Kubernetes nhanh hơn nhiều so với việc sử dụng giao diện web.#<p>kubectl run hoặc Management Console có thể nhanh hơn cho các tác vụ đơn giản, nhưng YAML cung cấp khả năng kiểm soát và tái sử dụng tốt hơn cho cấu hình phức tạp.</p>
	=[moodle]Việc định nghĩa tất cả các đối tượng Kubernetes từ tệp YAML giúp lưu trữ chúng trong hệ thống kiểm soát phiên bản (version control system).
	~[moodle]Tệp YAML chỉ cho phép cấu hình một tập hợp giới hạn các thuộc tính, làm cho các định nghĩa đơn giản hơn.#<p>Ngược lại, tệp YAML cho phép bạn cấu hình tất cả các thuộc tính của tài nguyên Kubernetes, không chỉ một tập hợp giới hạn.</p>
	~[moodle]Tệp YAML cho phép Kubernetes tự động điều chỉnh cấu hình nếu có lỗi xảy ra trong quá trình triển khai.#<p>Tệp YAML định nghĩa trạng thái mong muốn; việc tự động điều chỉnh là chức năng của các controller Kubernetes, không phải bản thân tệp YAML.</p>
	####<p><strong>Giải thích</strong>: Việc định nghĩa tất cả các đối tượng Kubernetes từ tệp YAML giúp bạn có thể lưu trữ chúng trong một hệ thống kiểm soát phiên bản, với tất cả các lợi ích mà nó mang lại.</p>
}

// Question 7
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Nhãn (Labels) trong Kubernetes được sử dụng với mục đích chính là gì?</p>{
	~[moodle]Để lưu trữ các khối dữ liệu lớn, không xác định (unstructured data) gắn liền với Pod.#<p>Chú thích (Annotations) được sử dụng để gắn các khối dữ liệu lớn hơn, không xác định.</p>
	~[moodle]Để định nghĩa cấu hình mạng cho các Pods trong cùng một Namespace.#<p>Cấu hình mạng được định nghĩa bởi các tài nguyên như Services, NetworkPolicies, và VPC.</p>
	=[moodle]Để tổ chức và chọn các tài nguyên Kubernetes thành các nhóm dựa trên các cặp khóa-giá trị.
	~[moodle]Để chỉ định các hạn chế bảo mật cho từng container riêng lẻ trong một Pod.#<p>Các hạn chế bảo mật được định nghĩa bởi Security Contexts hoặc Pod Security Policies.</p>
	####<p><strong>Giải thích</strong>: Nhãn (Labels) là các cặp khóa-giá trị gắn vào các tài nguyên Kubernetes, được sử dụng để tổ chức, nhóm và chọn các tài nguyên thành các tập hợp.</p>
}

// Question 8
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Khi muốn chọn các Pods thuộc ứng dụng frontend và đang trong trạng thái beta release, bạn sẽ sử dụng bộ chọn nhãn (label selector) nào?</p>{
	~[moodle]app=frontend OR rel=beta.#<p>Bộ chọn nhãn Kubernetes sử dụng dấu phẩy làm toán tử AND, không phải OR.</p>
	=[moodle]app=frontend,rel=beta.
	~[moodle]app IN (frontend, beta).#<p>Toán tử IN được sử dụng với các giá trị trong ngoặc đơn, ví dụ: env in (prod, staging).</p>
	~[moodle]app=frontend AND rel=beta (trong cú pháp Kubernetes selector, dấu phẩy là AND).#<p>Trong cú pháp của kubectl, dấu phẩy (,) đã được hiểu là toán tử logic AND.</p>
	####<p><strong>Giải thích</strong>: Bộ chọn có thể bao gồm nhiều tiêu chí được phân tách bằng dấu phẩy. Các tài nguyên cần khớp với tất cả các tiêu chí để khớp với bộ chọn. Vì vậy, app=frontend,rel=beta sẽ chọn các Pods chạy bản beta của microservice frontend.</p>
}

// Question 9
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Điều nào sau đây mô tả đúng nhất về Annotation trong Kubernetes?</p>{
	~[moodle]Các cặp khóa-giá trị được sử dụng để chọn các Pods cho một Service.#<p>Nhãn (Labels) được sử dụng để chọn các Pods cho một Service.</p>
	~[moodle]Các trường bắt buộc phải có để một Pod có thể được lập lịch trình thành công.#<p>Các trường bắt buộc thường bao gồm apiVersion, kind, metadata.name và spec.containers.</p>
	=[moodle]Các cặp khóa-giá trị được sử dụng để đính kèm các khối dữ liệu lớn, không xác định vào tài nguyên, thường được các công cụ hoặc thư viện sử dụng.
	~[moodle]Một thuộc tính trong Pod Spec để chỉ định Node cụ thể mà Pod sẽ chạy.#<p>nodeSelector là thuộc tính dùng để chỉ định Node cụ thể.</p>
	####<p><strong>Giải thích</strong>: Annotation cho phép đính kèm các khối dữ liệu lớn hơn vào các Pod hoặc các tài nguyên khác, thường được sử dụng bởi con người hoặc các công cụ và thư viện.</p>
}

// Question 10
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Mục đích chính của Namespace trong Kubernetes là gì?</p>{
	~[moodle]Để giới hạn số lượng CPU và Memory mà một Pod có thể tiêu thụ.#<p>Resource Quotas và Limit Ranges được sử dụng để giới hạn tài nguyên.</p>
	=[moodle]Để tạo các cụm Kubernetes ảo riêng biệt cho các nhóm hoặc dự án khác nhau trên cùng một cụm vật lý.
	~[moodle]Để đảm bảo rằng tất cả các Pods trong cùng một Node đều có thể truy cập lẫn nhau.#<p>Khả năng truy cập giữa các Pods trong cùng Node được quản lý bởi mạng Pod, không phải Namespace.</p>
	~[moodle]Để định nghĩa các chính sách bảo mật cho việc truy cập vào API server.#<p>RBAC (Role-Based Access Control) được sử dụng để định nghĩa các chính sách bảo mật cho việc truy cập API server.</p>
	####<p><strong>Giải thích</strong>: Namespaces có thể được sử dụng để cho phép các nhóm khác nhau sử dụng cùng một cluster như thể chúng đang sử dụng các cluster Kubernetes riêng biệt và không chồng chéo.</p>
}

// Question 11
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Khi bạn xóa một Namespace, điều gì sẽ xảy ra với tất cả các tài nguyên bên trong nó?</p>{
	~[moodle]Các tài nguyên sẽ được chuyển sang Namespace default.#<p>Kubernetes không tự động di chuyển tài nguyên giữa các Namespace.</p>
	=[moodle]Các tài nguyên sẽ bị xóa ngay lập tức cùng với Namespace đó.
	~[moodle]Các tài nguyên sẽ trở thành "orphaned" và tiếp tục chạy mà không có Namespace.#<p>Các tài nguyên được gắn với một Namespace và không thể tồn tại bên ngoài nó khi Namespace bị xóa.</p>
	~[moodle]Các tài nguyên sẽ được tự động sao lưu và lưu trữ bên ngoài cluster.#<p>Cần cấu hình riêng biệt các giải pháp sao lưu nếu bạn muốn bảo vệ dữ liệu khi xóa Namespace.</p>
	####<p><strong>Giải thích</strong>: Việc xóa một Namespace sẽ xóa tất cả các tài nguyên nằm trong Namespace đó.</p>
}

// Question 12
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Lệnh nào cho phép bạn liệt kê các Pods trong một Namespace cụ thể khác với Namespace default?</p>{
	~[moodle]kubectl get pods --all-namespaces.#<p>kubectl get pods --all-namespaces liệt kê Pods từ tất cả các Namespace, không chỉ một Namespace cụ thể.</p>
	=[moodle]kubectl get pods --namespace &lt;tên-namespace&gt; hoặc kubectl get pods -n &lt;tên-namespace&gt;.
	~[moodle]kubectl list pods &lt;tên-namespace&gt;.#<p>Không có lệnh kubectl list pods.</p>
	~[moodle]kubectl get pods --context &lt;tên-namespace&gt;.#<p>context được sử dụng để quản lý cấu hình kết nối tới các cluster khác nhau.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể sử dụng tùy chọn --namespace &lt;name&gt; hoặc -n &lt;name&gt; để chỉ định Namespace mà bạn muốn liệt kê Pods từ đó.</p>
}

// Question 13
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Khi bạn xóa một Pod bằng kubectl delete pod &lt;tên-pod&gt;, điều gì xảy ra đầu tiên với các container bên trong Pod?</p>{
	~[moodle]Kubernetes gửi tín hiệu SIGKILL đến các tiến trình trong container ngay lập tức.#<p>Nếu tiến trình không tắt kịp thời sau tín hiệu SIGTERM, sau khoảng thời gian chờ, nó mới bị tiêu diệt bằng SIGKILL.</p>
	=[moodle]Kubernetes gửi tín hiệu SIGTERM đến tiến trình chính của container để cho phép nó tắt một cách duyên dáng (gracefully).
	~[moodle]Pod được chuyển sang trạng thái "Paused" và tất cả các tiến trình bị đóng băng.#<p>Không có trạng thái "Paused" theo cách này khi xóa Pod.</p>
	~[moodle]Pod ngay lập tức bị loại bỏ khỏi Node mà không có bất kỳ tín hiệu nào.#<p>Một quy trình tắt máy được thực hiện để đảm bảo tài nguyên được giải phóng đúng cách và ứng dụng có thể hoàn thành các yêu cầu đang thực hiện.</p>
	####<p><strong>Giải thích</strong>: Khi xóa một Pod, Kubernetes sẽ gửi tín hiệu SIGTERM đến tiến trình chính của container và đợi một số giây nhất định (mặc định là 30 giây) để nó tắt một cách duyên dáng.</p>
}

// Question 14
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Điều nào sau đây là ĐÚNG về việc chỉ định cổng (ports) trong định nghĩa Pod?</p>{
	~[moodle]Việc chỉ định cổng là bắt buộc để các client có thể kết nối đến Pod.#<p>Các client kết nối thông qua địa chỉ IP của Pod và cổng mà ứng dụng thực sự lắng nghe, không phải là thông tin cổng được khai báo trong Pod definition.</p>
	=[moodle]Việc chỉ định cổng chỉ mang tính thông tin và không ảnh hưởng đến việc client có thể kết nối hay không.
	~[moodle]Kubernetes sử dụng các cổng này để tự động tạo Services cho Pod.#<p>Services được tạo ra bởi các tài nguyên Service riêng biệt và sử dụng bộ chọn nhãn để tìm Pods.</p>
	~[moodle]Nếu không chỉ định cổng, Pod sẽ không thể giao tiếp với bất kỳ Service nào.#<p>Pod có thể giao tiếp thông qua mạng Pod ngay cả khi cổng không được chỉ định, miễn là ứng dụng bên trong container lắng nghe trên cổng đó.</p>
	####<p><strong>Giải thích</strong>: Việc chỉ định cổng trong định nghĩa Pod chỉ mang tính thông tin. Việc bỏ qua chúng không ảnh hưởng đến việc client có thể kết nối đến Pod thông qua cổng đó hay không.</p>
}

// Question 15
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Nếu bạn muốn chạy một Pod mà không có bất kỳ ReplicationController hoặc Deployment nào quản lý nó, bạn sẽ sử dụng lệnh kubectl run với tùy chọn nào?</p>{
	~[moodle]kubectl run &lt;tên-pod&gt; --image=&lt;image&gt; --restart=Always.#<p>--restart=Always là mặc định cho các controller như Deployment hoặc ReplicationController, không cho phép Pod độc lập.</p>
	=[moodle]kubectl run &lt;tên-pod&gt; --image=&lt;image&gt; --generator=run-pod/v1.
	~[moodle]kubectl run &lt;tên-pod&gt; --image=&lt;image&gt; --replicas=1.#<p>--replicas=1 sẽ tạo một ReplicationController hoặc Deployment với một bản sao Pod.</p>
	~[moodle]kubectl run &lt;tên-pod&gt; --image=&lt;image&gt; --expose.#<p>--expose được dùng để tạo Service để lộ Pod ra bên ngoài.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể chạy một Pod trực tiếp, không có bất kỳ loại ReplicationController hoặc tương tự nào đằng sau nó, bằng cách sử dụng tùy chọn --generator=run-pod/v1.</p>
}

// Question 16
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Khi tạo một Pod từ một tệp YAML, các phần chính mà hầu hết các tài nguyên Kubernetes đều có là gì?</p>{
	~[moodle]status, events, logs.#<p>Đây là các thuộc tính liên quan đến trạng thái và hoạt động của Pod, không phải là các phần cấu trúc chính trong định nghĩa YAML.</p>
	=[moodle]apiVersion, kind, metadata, spec.
	~[moodle]controller, scheduler, kubelet.#<p>Đây là các thành phần của Control Plane Kubernetes, không phải các phần trong định nghĩa tài nguyên.</p>
	~[moodle]image, containerID, imageID.#<p>Đây là các thuộc tính của container, nằm trong phần spec của Pod.</p>
	####<p><strong>Giải thích</strong>: Hầu hết các tài nguyên Kubernetes đều có ba phần quan trọng: apiVersion (phiên bản API), kind (loại tài nguyên), metadata (siêu dữ liệu), và spec (đặc tả).</p>
}

// Question 17
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Điều nào sau đây KHÔNG phải là một lý do phổ biến để nhóm nhiều container vào cùng một Pod?</p>{
	~[moodle]Các container cần chia sẻ tài nguyên mạng giống nhau để giao tiếp hiệu quả.#<p>Các container trong một Pod chia sẻ network namespace, cho phép chúng giao tiếp qua localhost.</p>
	~[moodle]Các container cần chia sẻ cùng hệ thống tệp để truy cập dữ liệu chung.#<p>Các container có thể chia sẻ các Volume để truy cập cùng hệ thống tệp hoặc dữ liệu tạm thời.</p>
	=[moodle]Các container có các chu kỳ sống độc lập và có thể được triển khai riêng biệt.
	~[moodle]Các container thực hiện các chức năng phụ trợ (sidecar) hỗ trợ cho container chính.#<p>Mô hình sidecar (container phụ trợ) là một trường hợp sử dụng phổ biến cho nhiều container trong một Pod, nơi sidecar cung cấp chức năng bổ sung cho container chính (ví dụ: logging, monitoring).</p>
	####<p><strong>Giải thích</strong>: Nếu các container có các chu kỳ sống độc lập và có thể được triển khai riêng biệt, thì nên đặt chúng trong các Pod riêng biệt để tối đa hóa khả năng độc lập và linh hoạt.</p>
}

// Question 18
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Khi một Pod bị xóa, log của các container bên trong nó sẽ được xử lý như thế nào theo mặc định?</p>{
	~[moodle]Log sẽ được lưu trữ tự động trên một Volume bền vững (Persistent Volume).#<p>Log không tự động được lưu trữ trên Persistent Volume; cần cấu hình hệ thống log riêng biệt cho điều đó.</p>
	~[moodle]Log sẽ được chuyển đến một dịch vụ log tập trung trong vòng vài phút.#<p>Log tập trung cần được cấu hình riêng (ví dụ: với FluentD, ElasticSearch, Kibana - EFK stack) và không phải là hành vi mặc định khi xóa Pod.</p>
	=[moodle]Log sẽ bị xóa cùng với Pod và không thể truy xuất được nữa.
	~[moodle]Log được nén và lưu trữ tạm thời trên Node mà Pod đã chạy.#<p>Log có thể được giữ lại trên Node trong một khoảng thời gian nhất định bởi runtime container, nhưng sẽ không còn truy cập được thông qua API Kubernetes một khi Pod bị xóa.</p>
	####<p><strong>Giải thích</strong>: Khi một Pod bị xóa, log của nó cũng bị xóa. Để giữ log ngay cả sau khi Pod bị xóa, bạn cần thiết lập hệ thống log tập trung, cluster-wide.</p>
}

// Question 19
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Điều gì xảy ra khi bạn cố gắng tạo một Pod mà không có bất kỳ container nào được định nghĩa trong trường spec của nó?</p>{
	~[moodle]Kubernetes sẽ tự động tạo một container default rỗng để Pod có thể chạy.#<p>Kubernetes không tự động thêm container vào Pod nếu người dùng không định nghĩa.</p>
	=[moodle]API server sẽ từ chối Pod đó vì nó không hợp lệ.
	~[moodle]Pod sẽ được tạo nhưng sẽ luôn ở trạng thái Pending vì không có gì để chạy.#<p>Vì Pod không hợp lệ, nó sẽ không được tạo thành công để đạt trạng thái Pending.</p>
	~[moodle]Kubelet sẽ tạo một Pod pause và đợi bạn thêm container sau.#<p>Container pause được tạo bởi Kubelet cho mục đích hạ tầng của Pod, không phải để làm Pod trống rỗng.</p>
	####<p><strong>Giải thích</strong>: API server thực hiện xác thực các đối tượng. Nếu bạn cố gắng lưu trữ một đối tượng được cấu hình không đúng cách (ví dụ: một Pod không có container), API server sẽ từ chối nó.</p>
}

// Question 20
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Khi sử dụng kubectl explain pod.spec.containers.ports, bạn đang tìm kiếm thông tin gì?</p>{
	~[moodle]Cách khai báo các Volume cho Pod.#<p>Volume được định nghĩa trong pod.spec.volumes và pod.spec.containers.volumeMounts.</p>
	~[moodle]Cách cấu hình liveness probes cho container.#<p>Liveness probes được định nghĩa trong pod.spec.containers.livenessProbe.</p>
	=[moodle]Cách định nghĩa các cổng mạng mà container lắng nghe.
	~[moodle]Cách thiết lập các biến môi trường cho container.#<p>Biến môi trường được định nghĩa trong pod.spec.containers.env.</p>
	####<p><strong>Giải thích</strong>: Lệnh kubectl explain cung cấp tài liệu về các trường của một tài nguyên Kubernetes. Cụ thể, pod.spec.containers.ports sẽ giải thích cách định nghĩa các cổng mạng mà một container bên trong Pod mong muốn hiển thị.</p>
}

// Question 21
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Điều nào sau đây là một hạn chế của việc sử dụng kubectl run để tạo tài nguyên Kubernetes so với việc sử dụng tệp YAML?</p>{
	~[moodle]kubectl run không thể được sử dụng để tạo Pods, chỉ có thể tạo Deployments.#<p>kubectl run có thể tạo Pods trực tiếp (với --generator=run-pod/v1), Deployments hoặc ReplicationControllers.</p>
	=[moodle]kubectl run thường chỉ cho phép bạn cấu hình một tập hợp giới hạn các thuộc tính của tài nguyên.
	~[moodle]kubectl run chỉ hoạt động với các container Docker, không hỗ trợ các runtime container khác.#<p>kubectl run làm việc với bất kỳ container runtime nào được cấu hình với Kubernetes (Docker, rkt, CRI-O, v.v.).</p>
	~[moodle]kubectl run tự động thêm các nhãn ngẫu nhiên vào Pod, làm cho việc quản lý trở nên khó khăn.#<p>kubectl run có thể thêm nhãn, nhưng chúng thường không ngẫu nhiên mà tuân theo các quy ước nhất định, và người dùng có thể kiểm soát chúng.</p>
	####<p><strong>Giải thích</strong>: Các cách đơn giản hơn để tạo tài nguyên, như lệnh kubectl run, thường chỉ cho phép bạn cấu hình một tập hợp giới hạn các thuộc tính, không phải tất cả.</p>
}

// Question 22
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Nếu bạn muốn tất cả các Pods của một ứng dụng backend được lập lịch trên các Node có nhãn disk: ssd, bạn sẽ sử dụng thuộc tính nào trong Pod Spec?</p>{
	~[moodle]affinity.nodeAffinity.requiredDuringSchedulingIgnoredDuringExecution.#<p>nodeAffinity là một tính năng lập lịch nâng cao hơn cho phép các quy tắc lập lịch phức tạp hơn so với nodeSelector.</p>
	=[moodle]nodeSelector.
	~[moodle]tolerations.#<p>tolerations được sử dụng để cho phép Pod chạy trên các Node có taints (ô nhiễm) cụ thể.</p>
	~[moodle]priorityClassName.#<p>priorityClassName được sử dụng để chỉ định ưu tiên của Pod trong quá trình lập lịch.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể sử dụng thuộc tính nodeSelector trong Pod Spec để chỉ định rằng Pod chỉ nên chạy trên các Node có nhãn cụ thể. Ví dụ: nodeSelector: disk: ssd.</p>
}

// Question 23
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Khi một container bên trong Pod bị khởi động lại (ví dụ: do lỗi ứng dụng hoặc liveness probe thất bại), điều gì xảy ra với container đó?</p>{
	~[moodle]Container cũ được khôi phục và tiếp tục chạy từ trạng thái cuối cùng.#<p>Nội dung của hệ thống tệp bên trong container sẽ bị mất, trừ khi được lưu trữ trên một Volume.</p>
	=[moodle]Một container hoàn toàn mới được tạo và chạy, thay thế container cũ.
	~[moodle]Pod bị xóa và một Pod hoàn toàn mới được tạo để thay thế.#<p>Pod vẫn giữ nguyên; chỉ có container bên trong nó được khởi động lại.</p>
	~[moodle]Kubelet sẽ cố gắng sửa chữa container cũ mà không khởi tạo lại.#<p>Kubelet không sửa chữa container; nó sẽ khởi động lại (tạo mới) container theo chính sách restartPolicy của Pod.</p>
	####<p><strong>Giải thích</strong>: Khi một container bị tiêu diệt, một container hoàn toàn mới được tạo - đó không phải là cùng một container được khởi động lại.</p>
}

// Question 24
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Bạn có thể thêm hoặc thay đổi nhãn của một Pod đã tồn tại bằng lệnh nào?</p>{
	~[moodle]kubectl edit pod &lt;tên-pod&gt;.#<p>kubectl edit mở toàn bộ định nghĩa Pod để chỉnh sửa, có thể dùng để thay đổi nhãn nhưng không phải cách trực tiếp nhất.</p>
	~[moodle]kubectl annotate pod &lt;tên-pod&gt; &lt;khóa&gt;=&lt;giá-trị&gt;.#<p>kubectl annotate được dùng để thêm hoặc sửa đổi chú thích (annotations), không phải nhãn (labels).</p>
	=[moodle]kubectl label pod &lt;tên-pod&gt; &lt;khóa&gt;=&lt;giá-trị&gt; --overwrite.
	~[moodle]kubectl update pod &lt;tên-pod&gt; --labels &lt;khóa&gt;=&lt;giá-trị&gt;.#<p>Không có lệnh kubectl update pod --labels.</p>
	####<p><strong>Giải thích</strong>: Nhãn có thể được thêm vào và sửa đổi trên các Pod đã tồn tại bằng lệnh kubectl label pod &lt;tên-pod&gt; &lt;khóa&gt;=&lt;giá-trị&gt; --overwrite.</p>
}

// Question 25
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Nếu bạn muốn xóa tất cả các Pods trong một Namespace cụ thể mà không xóa chính Namespace đó, bạn sẽ sử dụng lệnh nào?</p>{
	~[moodle]kubectl delete namespace &lt;tên-namespace&gt;.#<p>kubectl delete namespace sẽ xóa toàn bộ Namespace và tất cả tài nguyên bên trong.</p>
	~[moodle]kubectl delete pod --all-namespaces.#<p>kubectl delete pod --all-namespaces sẽ cố gắng xóa tất cả Pods trong tất cả các Namespace, bao gồm cả các Pods hệ thống.</p>
	=[moodle]kubectl delete pod --all -n &lt;tên-namespace&gt;.
	~[moodle]kubectl delete pods &lt;tên-namespace&gt;.#<p>Lệnh này không hợp lệ, bạn cần chỉ định một bộ chọn hoặc --all.</p>
	####<p><strong>Giải thích</strong>: Để xóa tất cả các Pods trong một Namespace cụ thể mà không xóa Namespace đó, bạn có thể sử dụng lệnh kubectl delete pod --all -n &lt;tên-namespace&gt;.</p>
}

// Question 26
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Tại sao việc sử dụng nhãn đa chiều (multi-dimensional labels) lại được khuyến nghị cho các tài nguyên Kubernetes?</p>{
	~[moodle]Để giảm số lượng nhãn cần thiết cho mỗi tài nguyên, làm cho các định nghĩa đơn giản hơn.#<p>Nhãn đa chiều có thể tăng số lượng nhãn trên mỗi tài nguyên, nhưng bù lại bằng khả năng tổ chức mạnh mẽ hơn.</p>
	=[moodle]Để cho phép lựa chọn linh hoạt hơn và phân loại tài nguyên theo nhiều tiêu chí khác nhau.
	~[moodle]Để chỉ định quyền truy cập duy nhất cho từng tài nguyên thông qua RBAC.#<p>Nhãn được sử dụng để chọn tài nguyên mà một vai trò RBAC có thể tác động, nhưng bản thân chúng không định nghĩa quyền truy cập.</p>
	~[moodle]Để lưu trữ các tệp cấu hình lớn trực tiếp trên tài nguyên Kubernetes.#<p>Chú thích (Annotations) được sử dụng cho việc lưu trữ các tệp cấu hình lớn hoặc dữ liệu không cấu trúc.</p>
	####<p><strong>Giải thích</strong>: Việc sử dụng nhãn đa chiều thay vì nhãn đơn chiều (multi-dimensional instead of single-dimensional labels) là một phương pháp hay được khuyến nghị để cho phép lựa chọn linh hoạt hơn và phân loại tài nguyên theo nhiều tiêu chí khác nhau (ví dụ: app: frontend, tier: web, env: prod).</p>
}

// Question 27
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Khi bạn tạo một Pod bằng kubectl create -f kubia-manual.yaml, trạng thái ban đầu của Pod thường là gì trước khi chuyển sang Running?</p>{
	~[moodle]Completed.#<p>Completed là trạng thái cho các Pods hoàn thành một tác vụ và dừng lại.</p>
	~[moodle]CrashLoopBackOff.#<p>CrashLoopBackOff cho biết container trong Pod liên tục gặp lỗi và khởi động lại.</p>
	=[moodle]Pending.
	~[moodle]Terminating.#<p>Terminating là trạng thái khi một Pod đang trong quá trình bị xóa.</p>
	####<p><strong>Giải thích</strong>: Khi một Pod được tạo, trạng thái ban đầu của nó thường là Pending, cho thấy Pod đã được API server chấp nhận nhưng chưa được lập lịch trình hoặc các container chưa được tạo.</p>
}

// Question 28
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Nếu bạn muốn khám phá tất cả các tùy chọn cấu hình có sẵn cho một tài nguyên Kubernetes cụ thể (ví dụ: Pod) mà không cần tra cứu tài liệu trực tuyến, bạn sẽ sử dụng lệnh nào?</p>{
	~[moodle]kubectl get --help.#<p>kubectl get --help chỉ hiển thị các tùy chọn trợ giúp cho lệnh get.</p>
	~[moodle]kubectl describe pod.#<p>kubectl describe pod hiển thị trạng thái và thông tin của một Pod đang chạy.</p>
	=[moodle]kubectl explain pod.
	~[moodle]kubectl info pod.#<p>Không có lệnh kubectl info pod.</p>
	####<p><strong>Giải thích</strong>: Lệnh kubectl explain &lt;resource-type&gt; cho phép bạn nhanh chóng tra cứu thông tin chi tiết về bất kỳ tài nguyên Kubernetes nào, bao gồm các trường và tùy chọn cấu hình của nó.</p>
}

// Question 29
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Điều nào sau đây là ĐÚNG về địa chỉ IP của Pod trong Kubernetes?</p>{
	=[moodle]Mỗi Pod có một địa chỉ IP duy nhất trong cluster.
	~[moodle]Địa chỉ IP của Pod có thể thay đổi mỗi khi container bên trong nó khởi động lại.#<p>Địa chỉ IP của Pod duy trì ổn định trong suốt chu kỳ sống của Pod, nhưng sẽ thay đổi nếu Pod bị xóa và tạo lại.</p>
	~[moodle]Các Pods trong cùng một Node chia sẻ cùng một địa chỉ IP.#<p>Mỗi Pod có địa chỉ IP riêng của mình, ngay cả khi chúng chạy trên cùng một Node.</p>
	~[moodle]Địa chỉ IP của Pod được quản lý bởi Service, không phải Pod trực tiếp.#<p>Service sử dụng bộ chọn nhãn để tìm các Pods và chuyển tiếp lưu lượng truy cập đến chúng; Service cung cấp một IP ổn định cho các client, trong khi Pod vẫn có IP riêng.</p>
	####<p><strong>Giải thích</strong>: Mỗi Pod có địa chỉ IP riêng và duy nhất của nó, cho phép nó giao tiếp với các Pod khác và dịch vụ bên ngoài.</p>
}

// Question 30
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Bạn có thể sử dụng biểu tượng app=kubia làm nhãn trên Pod để làm gì?</p>{
	~[moodle]Định nghĩa phiên bản cụ thể của ứng dụng kubia.#<p>Để định nghĩa phiên bản, bạn thường sử dụng một nhãn khác như version: v1 hoặc rel: stable.</p>
	=[moodle]Đánh dấu Pod là một phần của ứng dụng kubia, cho phép Services và các Controller khác nhóm và quản lý nó.
	~[moodle]Chỉ định rằng Pod này chỉ có thể chạy trên các Node được gắn nhãn app=kubia.#<p>nodeSelector hoặc nodeAffinity được sử dụng để lập lịch Pods trên các Node cụ thể.</p>
	~[moodle]Bật tính năng tự động mở rộng quy mô cho ứng dụng kubia.#<p>Tự động mở rộng quy mô được thực hiện bởi HorizontalPodAutoscaler, nhắm mục tiêu vào Deployment hoặc ReplicaSet, dựa trên các nhãn của Pod.</p>
	####<p><strong>Giải thích</strong>: Nhãn như app=kubia được sử dụng để đánh dấu Pod là một phần của ứng dụng kubia, giúp các Services, ReplicationControllers và các tài nguyên khác có thể chọn và quản lý tập hợp các Pods đó một cách hiệu quả.</p>
}

// Question 31
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Điều nào sau đây KHÔNG thể được khai báo trực tiếp trong một định nghĩa Pod YAML?</p>{
	~[moodle]Tên của container (name).#<p>Tên của container được khai báo trong spec.containers.name.</p>
	~[moodle]Ảnh container (image).#<p>Ảnh container được khai báo trong spec.containers.image.</p>
	=[moodle]Số lượng replicas mong muốn của Pod.
	~[moodle]Các biến môi trường cho container.#<p>Biến môi trường được khai báo trong spec.containers.env.</p>
	####<p><strong>Giải thích</strong>: Số lượng replicas mong muốn của Pod (replicas) không được khai báo trực tiếp trong định nghĩa Pod mà được khai báo trong các tài nguyên quản lý Pod như ReplicationController, ReplicaSet hoặc Deployment.</p>
}

// Question 32
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Khi một Pod được tạo từ tệp YAML, sau khi được API server chấp nhận, thành phần nào của Kubernetes chịu trách nhiệm gán Node Worker cho Pod đó?</p>{
	~[moodle]Kubelet.#<p>Kubelet chạy trên Node Worker và quản lý các container trên Node đó sau khi Pod đã được Scheduler gán.</p>
	~[moodle]Controller Manager.#<p>Controller Manager chạy các Controller cấp cluster, nhưng không trực tiếp gán Node cho Pods.</p>
	=[moodle]Scheduler.
	~[moodle]kube-proxy.#<p>kube-proxy chịu trách nhiệm cân bằng tải mạng cho các Service.</p>
	####<p><strong>Giải thích</strong>: Scheduler chịu trách nhiệm gán một Node Worker cho mỗi Pod mới được tạo mà chưa có Node được đặt.</p>
}

// Question 33
::Chapter 3\: Pods: Running Containers in Kubernetes::[html]<p>Điều gì xảy ra khi bạn cố gắng tạo một Pod với một nhãn (label) không hợp lệ (ví dụ: khóa chứa ký tự đặc biệt)?</p>{
	~[moodle]Kubernetes sẽ tự động sửa lỗi nhãn thành định dạng hợp lệ.#<p>API server không tự động sửa lỗi cấu hình của người dùng.</p>
	~[moodle]Pod sẽ được tạo nhưng nhãn không hợp lệ sẽ bị bỏ qua.#<p>Nếu nhãn không hợp lệ, việc tạo tài nguyên sẽ thất bại.</p>
	=[moodle]API server sẽ từ chối tạo Pod đó và trả về lỗi xác thực.
	~[moodle]Pod sẽ được lập lịch trình thành công nhưng sẽ không thể được quản lý bởi các Controller.#<p>Lỗi xác thực sẽ ngăn cản Pod được tạo, chứ không chỉ là không được quản lý.</p>
	####<p><strong>Giải thích</strong>: API server Kubernetes thực hiện xác thực các đối tượng. Nếu bạn cố gắng lưu trữ một đối tượng có cấu hình không hợp lệ, chẳng hạn như một nhãn không tuân thủ định dạng cho phép, API server sẽ từ chối yêu cầu và trả về lỗi xác thực.</p>
}

// Chapter 4: Replication and Other Controllers: Deploying Managed Pods
// Switch category to $module$/top/Chapter 4: Replication and Other Controllers: Deploying Managed Pods
$CATEGORY: $module$/top/Chapter 4: Replication and Other Controllers: Deploying Managed Pods

// Question 1
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Trong Kubernetes, điều gì được khuyến nghị để quản lý Pods trong các trường hợp sử dụng thực tế, thay vì tạo Pods trực tiếp?</p>{
	~[moodle]Tự quản lý Pods thủ công bằng kubectl create và kubectl delete.#<p>Quản lý Pods thủ công là công việc khó khăn và dễ mắc lỗi, không phù hợp cho các triển khai tự động và có khả năng phục hồi.</p>
	=[moodle]Sử dụng các tài nguyên cấp cao hơn như ReplicationControllers hoặc Deployments.
	~[moodle]Viết script shell để giám sát và khởi động lại Pods khi cần.#<p>Kubernetes cung cấp các Controller tích hợp sẵn để tự động giám sát và quản lý Pods, loại bỏ nhu cầu viết script tùy chỉnh cho các tác vụ cơ bản này.</p>
	~[moodle]Chỉ sử dụng các Pods không được quản lý (unmanaged pods) cho tất cả các ứng dụng.#<p>Pods không được quản lý không có khả năng tự phục hồi hoặc tự động lập lịch trình lại khi Node bị lỗi, không phù hợp cho các ứng dụng yêu cầu tính bền vững.</p>
	####<p><strong>Giải thích</strong>: Trong các trường hợp sử dụng thực tế, bạn hầu như không bao giờ tạo Pods trực tiếp. Thay vào đó, bạn tạo các loại tài nguyên khác, chẳng hạn như ReplicationControllers hoặc Deployments, sau đó chúng sẽ tạo và quản lý các Pods thực tế.</p>
}

// Question 2
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Chức năng chính của liveness probe trong Kubernetes là gì?</p>{
	~[moodle]Kiểm tra xem ứng dụng có sẵn sàng nhận lưu lượng truy cập mạng hay không.#<p>Chức năng này thuộc về readiness probe, đảm bảo Pod sẵn sàng nhận lưu lượng truy cập.</p>
	=[moodle]Kiểm tra xem tiến trình chính của container có bị treo hoặc ngừng hoạt động hay không, và khởi động lại nếu cần.
	~[moodle]Thu thập các chỉ số hiệu suất từ container và gửi chúng đến một hệ thống giám sát.#<p>Thu thập chỉ số là nhiệm vụ của cAdvisor và Heapster, không phải liveness probe.</p>
	~[moodle]Đảm bảo rằng container có đủ tài nguyên CPU và bộ nhớ để hoạt động.#<p>Quản lý tài nguyên là nhiệm vụ của Scheduler và Limit Range, không phải liveness probe.</p>
	####<p><strong>Giải thích</strong>: Liveness probe được Kubelet sử dụng để kiểm tra định kỳ xem ứng dụng bên trong container có hoạt động đúng cách hay không. Nếu probe thất bại, Kubelet sẽ khởi động lại container.</p>
}

// Question 3
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Khi một liveness probe của container thất bại nhiều lần liên tiếp, hành động mặc định của Kubernetes là gì?</p>{
	~[moodle]Đánh dấu Pod là Failed và ngăn không cho nó được lập lịch lại.#<p>Pod chỉ được đánh dấu Failed nếu không thể khởi động container hoặc nếu restartPolicy không cho phép khởi động lại.</p>
	~[moodle]Loại bỏ Pod khỏi tất cả các Service và đợi quản trị viên can thiệp.#<p>Readiness probe có thể loại bỏ Pod khỏi Service, nhưng thất bại của liveness probe dẫn đến khởi động lại container.</p>
	=[moodle]Khởi động lại container bên trong Pod.
	~[moodle]Chuyển Pod sang một Node khác có tài nguyên tốt hơn.#<p>Kubelet thực hiện việc khởi động lại container trên cùng một Node; việc chuyển Pod sang Node khác xảy ra khi Node bị lỗi và được quản lý bởi Control Plane.</p>
	####<p><strong>Giải thích</strong>: Nếu liveness probe của container thất bại failureThreshold lần liên tiếp, container sẽ được khởi động lại.</p>
}

// Question 4
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Ba phần thiết yếu của một ReplicationController là gì?</p>{
	~[moodle]apiVersion, kind, metadata.#<p>Đây là các phần cấu trúc cơ bản của một tài nguyên Kubernetes nói chung.</p>
	=[moodle]Bộ chọn nhãn (label selector), số lượng bản sao mong muốn (replica count), và mẫu Pod (pod template).
	~[moodle]livenessProbe, readinessProbe, startupProbe.#<p>Đây là các loại probe sức khỏe cho container.</p>
	~[moodle]kubelet, scheduler, controller-manager.#<p>Đây là các thành phần của Control Plane Kubernetes.</p>
	####<p><strong>Giải thích</strong>: Một ReplicationController có ba phần thiết yếu: bộ chọn nhãn (label selector), xác định Pods nào nằm trong phạm vi của nó; số lượng bản sao mong muốn (replica count), chỉ định số lượng Pods phải chạy; và mẫu Pod (pod template), được sử dụng khi tạo các bản sao Pod mới.</p>
}

// Question 5
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Nếu bạn thay đổi mẫu Pod (pod template) của một ReplicationController đã tồn tại, điều gì sẽ xảy ra?</p>{
	~[moodle]Tất cả các Pods đang chạy sẽ được tự động khởi động lại với mẫu Pod mới.#<p>Để cập nhật tất cả Pods, cần thực hiện Rolling dn Pods mới được tạo sau đó mới sử dụng mẫu Pod đã cập nhật.
	~[moodle]ReplicationController sẽ bị lỗi và cần được tạo lại.#<p>ReplicationController vẫn tiếp tục hoạt động với các Pods hiện có và tạo Pods mới theo mẫu mới.</p>
	~[moodle]Không có gì xảy ra, mẫu Pod không thể thay đổi sau khi tạo.#<p>Mẫu Pod có thể được thay đổi, nhưng chỉ áp dụng cho Pods mới.</p>
	####<p><strong>Giải thích</strong>: Việc thay đổi mẫu Pod của một ReplicationController chỉ ảnh hưởng đến các Pods được tạo ra sau đó và không có tác động đến các Pods hiện có.</p>
}

// Question 6
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Khi một Node Worker bị lỗi, điều gì sẽ xảy ra với các Pods không được quản lý (unmanaged pods) đang chạy trên Node đó?</p>{
	~[moodle]Kubelet trên Node bị lỗi sẽ tự động khởi động lại các Pods đó.#<p>Kubelet chạy trên Node đó, nếu Node lỗi, Kubelet cũng sẽ không hoạt động.</p>
	~[moodle]Control Plane sẽ tạo các Pods thay thế trên các Node khác.#<p>Control Plane chỉ tạo Pods thay thế cho các Pods được quản lý bởi các Controller (như ReplicationController, Deployment).</p>
	=[moodle]Các Pods sẽ bị mất và không được phục hồi tự động.
	~[moodle]Các Pods sẽ được chuyển sang trạng thái "Paused" cho đến khi Node được sửa chữa.#<p>Không có trạng thái "Paused" tự động cho Pods khi Node bị lỗi.</p>
	####<p><strong>Giải thích</strong>: Đối với các Pods mà bạn tạo trực tiếp (unmanaged pods), chúng không được quản lý bởi bất kỳ thứ gì ngoại trừ Kubelet. Nếu Node bị lỗi, Kubelet không thể làm gì, và các Pods đó sẽ bị mất và không được phục hồi tự động.</p>
}

// Question 7
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Điều nào sau đây là ví dụ về một Exec probe trong liveness probe?</p>{
	~[moodle]Gửi một yêu cầu HTTP GET đến đường dẫn /healthz trên cổng 8080.#<p>Đây là ví dụ về HTTP GET probe.</p>
	~[moodle]Mở một kết nối TCP đến cổng 8080.#<p>Đây là ví dụ về TCP Socket probe.</p>
	=[moodle]Chạy lệnh cat /tmp/healthy trong container và kiểm tra mã thoát.
	~[moodle]Kiểm tra việc sử dụng CPU của container để xác định tình trạng hoạt động.#<p>Liveness probe kiểm tra sức khỏe của ứng dụng, không phải việc sử dụng tài nguyên CPU.</p>
	####<p><strong>Giải thích</strong>: Một Exec probe thực thi một lệnh bên trong container và xem xét mã thoát của lệnh đó. Mã thoát 0 cho biết thành công, mã khác 0 cho biết thất bại. Ví dụ: command: ["cat", "/tmp/healthy"].</p>
}

// Question 8
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Làm thế nào để bạn scale up (tăng số lượng bản sao) của một ReplicationController một cách khai báo (declaratively)?</p>{
	~[moodle]Sử dụng lệnh kubectl run --replicas=&lt;số-lượng-mới&gt;.#<p>kubectl run được dùng để tạo tài nguyên, không phải để scale tài nguyên đã tồn tại.</p>
	=[moodle]Chỉnh sửa trường spec.replicas trong định nghĩa ReplicationController bằng kubectl edit rc &lt;tên-rc&gt;.
	~[moodle]Xóa ReplicationController cũ và tạo một cái mới với số lượng bản sao cao hơn.#<p>Cách này không phải là khai báo mà là phá hủy và tạo lại, gây gián đoạn dịch vụ.</p>
	~[moodle]Tăng thủ công số lượng Pods bằng kubectl create pod.#<p>Tạo Pods thủ công không được quản lý bởi ReplicationController.</p>
	####<p><strong>Giải thích</strong>: Để scale một ReplicationController một cách khai báo, bạn chỉnh sửa trường spec.replicas trong định nghĩa của nó, ví dụ bằng kubectl edit rc &lt;tên-rc&gt;, và Kubernetes sẽ tự động điều chỉnh số lượng Pods.</p>
}

// Question 9
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Sự khác biệt chính giữa ReplicationController (RC) và ReplicaSet (RS) là gì?</p>{
	~[moodle]RC chỉ có thể quản lý Pods trong một Namespace duy nhất, trong khi RS có thể quản lý Pods trên toàn cluster.#<p>Cả RC và RS đều là tài nguyên có Namespace.</p>
	~[moodle]RC có khả năng tự phục hồi mạnh mẽ hơn RS khi Node bị lỗi.#<p>Cả RC và RS đều cung cấp khả năng tự phục hồi tương tự bằng cách đảm bảo số lượng bản sao mong muốn.</p>
	=[moodle]RS sử dụng các bộ chọn nhãn biểu cảm hơn (set-based selectors) so với RC.
	~[moodle]RC có thể quản lý các tác vụ một lần (one-off tasks), trong khi RS không thể.#<p>Jobs được sử dụng để quản lý các tác vụ một lần hoàn thành.</p>
	####<p><strong>Giải thích</strong>: ReplicaSet so với ReplicationController, có khả năng sử dụng các bộ chọn nhãn biểu cảm hơn (set-based selectors) như in, notin, exists thay vì chỉ các bộ chọn dựa trên đẳng thức (equality-based selectors).</p>
}

// Question 10
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>DaemonSet được sử dụng với mục đích gì?</p>{
	=[moodle]Đảm bảo rằng mỗi Node trong cluster (hoặc một tập hợp các Node đã chọn) chạy đúng một bản sao của một Pod cụ thể.
	~[moodle]Chạy một tác vụ có thể hoàn thành một lần (one-time completable task) theo lịch trình định sẵn.#<p>Đây là mục đích của CronJob.</p>
	~[moodle]Triển khai các ứng dụng stateful (có trạng thái) được sao chép với định danh ổn định.#<p>Đây là mục đích của StatefulSet.</p>
	~[moodle]Cân bằng tải lưu lượng truy cập giữa nhiều bản sao của một ứng dụng.#<p>Đây là mục đích của Service và Load Balancer.</p>
	####<p><strong>Giải thích</strong>: DaemonSet đảm bảo rằng một bản sao của Pod cụ thể chạy chính xác trên mỗi Node hoặc trên một tập hợp các Node đã chọn trong cluster.</p>
}

// Question 11
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Ví dụ phổ biến về việc sử dụng DaemonSet là gì?</p>{
	~[moodle]Triển khai một ứng dụng web không trạng thái (stateless web application).#<p>Deployment hoặc ReplicationController được sử dụng cho các ứng dụng web không trạng thái.</p>
	~[moodle]Chạy các tác vụ phân tích dữ liệu hàng loạt định kỳ.#<p>CronJob được sử dụng cho các tác vụ hàng loạt định kỳ.</p>
	=[moodle]Triển khai các tác nhân giám sát (monitoring agents) hoặc bộ thu thập log (log collectors) trên mỗi Node.
	~[moodle]Chạy một cơ sở dữ liệu quan hệ được sao chép (replicated relational database).#<p>StatefulSet được sử dụng cho các ứng dụng stateful như cơ sở dữ liệu.</p>
	####<p><strong>Giải thích</strong>: DaemonSet thường được sử dụng cho các Pods cấp hệ thống như các tác nhân giám sát (monitoring agents), bộ thu thập log (log collectors), hoặc các thành phần mạng (như kube-proxy) cần chạy trên mỗi Node.</p>
}

// Question 12
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Resource Job trong Kubernetes được sử dụng khi nào?</p>{
	~[moodle]Khi bạn cần chạy một ứng dụng liên tục, không bao giờ dừng.#<p>ReplicationController hoặc Deployment được sử dụng cho các ứng dụng liên tục.</p>
	=[moodle]Khi bạn cần chạy một Pod thực hiện một tác vụ duy nhất có thể hoàn thành.
	~[moodle]Khi bạn muốn đảm bảo một số lượng Pods nhất định luôn chạy trên mỗi Node.#<p>DaemonSet được sử dụng cho mục đích này.</p>
	~[moodle]Khi bạn muốn tạo ra một Service với một địa chỉ IP ổn định.#<p>Service được sử dụng để tạo địa chỉ IP ổn định.</p>
	####<p><strong>Giải thích</strong>: Resource Job được giới thiệu để chạy các Pods thực hiện một tác vụ duy nhất, có thể hoàn thành.</p>
}

// Question 13
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Làm thế nào để đảm bảo rằng một tác vụ Job chạy nhiều Pods tuần tự và phải hoàn thành 5 lần thành công?</p>{
	~[moodle]Đặt trường spec.parallelism thành 5.#<p>spec.parallelism được dùng để chạy nhiều Pods Job song song.</p>
	=[moodle]Đặt trường spec.completions thành 5.
	~[moodle]Sử dụng một CronJob với lịch trình 5 lần.#<p>CronJob được dùng để lập lịch Job chạy định kỳ.</p>
	~[moodle]Tạo 5 Pods Job riêng biệt thủ công.#<p>Job resource được thiết kế để tự động quản lý việc này.</p>
	####<p><strong>Giải thích</strong>: Để một Job chạy nhiều Pods tuần tự và phải hoàn thành một số lần cụ thể (ví dụ: 5 lần), bạn đặt trường spec.completions thành giá trị mong muốn.</p>
}

// Question 14
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Điều nào sau đây là ĐÚNG về cơ chế hoạt động của ReplicationController?</p>{
	~[moodle]Nó giao tiếp trực tiếp với Kubelet để khởi động và dừng container.#<p>Các Controller Kubernetes giao tiếp với API server, không giao tiếp trực tiếp với Kubelet.</p>
	=[moodle]Nó liên tục giám sát API server để tìm Pods khớp với bộ chọn nhãn và điều chỉnh số lượng.
	~[moodle]Nó thay đổi định nghĩa Pod của các Pods đang chạy để cập nhật chúng.#<p>Thay đổi mẫu Pod của RC chỉ ảnh hưởng đến các Pods mới; không thay đổi các Pods đang chạy.</p>
	~[moodle]Nó chỉ được kích hoạt một lần khi tạo và không theo dõi trạng thái sau đó.#<p>RC hoạt động theo cơ chế vòng lặp điều hòa (reconciliation loop), liên tục giám sát và điều chỉnh trạng thái.</p>
	####<p><strong>Giải thích</strong>: ReplicationController liên tục giám sát API server để tìm các Pods khớp với bộ chọn nhãn của nó. Nếu số lượng Pods hiện có không khớp với số lượng mong muốn, nó sẽ thực hiện hành động thích hợp để điều chỉnh.</p>
}

// Question 15
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Một CronJob trong Kubernetes được sử dụng để làm gì?</p>{
	~[moodle]Cung cấp một giao diện web để quản lý các Pods.#<p>Dashboard Kubernetes cung cấp giao diện web để quản lý Pods.</p>
	=[moodle]Lập lịch một Job resource để chạy định kỳ hoặc vào một thời điểm cụ thể trong tương lai.
	~[moodle]Đảm bảo rằng một số lượng Pods nhất định luôn được sao chép và chạy.#<p>ReplicationController, ReplicaSet, hoặc Deployment được sử dụng cho mục đích này.</p>
	~[moodle]Giám sát tình trạng sức khỏe của các container và khởi động lại chúng nếu cần.#<p>Liveness probe và Kubelet được sử dụng cho mục đích này.</p>
	####<p><strong>Giải thích</strong>: CronJob được sử dụng để lập lịch một Job resource theo một lịch trình định kỳ (sử dụng định dạng cron) hoặc vào một thời điểm cụ thể trong tương lai.</p>
}

// Question 16
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Điều nào sau đây KHÔNG phải là một loại probe sức khỏe được Kubernetes hỗ trợ cho container?</p>{
	~[moodle]HTTP GET probe.#<p>HTTP GET probe gửi yêu cầu HTTP và kiểm tra mã trạng thái.</p>
	~[moodle]TCP Socket probe.#<p>TCP Socket probe cố gắng mở kết nối TCP.</p>
	=[moodle]DNS lookup probe.
	~[moodle]Exec probe.#<p>Exec probe thực thi một lệnh bên trong container.</p>
	####<p><strong>Giải thích</strong>: Kubernetes hỗ trợ ba loại probe sức khỏe chính: HTTP GET probe, TCP Socket probe và Exec probe. Không có loại DNS lookup probe được đề cập trong các nguồn cung cấp.</p>
}

// Question 17
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Khi sử dụng kubectl delete rc &lt;tên-rc&gt; --cascade=false, điều gì sẽ xảy ra?</p>{
	~[moodle]ReplicationController và tất cả các Pods liên quan sẽ bị xóa.#<p>Đây là hành vi mặc định khi không sử dụng --cascade=false.</p>
	=[moodle]Chỉ ReplicationController bị xóa, các Pods do nó quản lý sẽ tiếp tục chạy và trở thành Pods không được quản lý.
	~[moodle]Lệnh sẽ thất bại vì cascade=false không phải là một tùy chọn hợp lệ cho ReplicationController.#<p>--cascade=false là một tùy chọn hợp lệ.</p>
	~[moodle]ReplicationController được đánh dấu là Terminating nhưng không có gì bị xóa cho đến khi tất cả các Pods dừng lại.#<p>RC bị xóa ngay lập tức, trong khi các Pods tiếp tục chạy.</p>
	####<p><strong>Giải thích</strong>: Khi bạn xóa một ReplicationController bằng kubectl delete rc &lt;tên-rc&gt; --cascade=false, chỉ ReplicationController bị xóa, và các Pods do nó quản lý sẽ tiếp tục chạy nhưng không còn được quản lý bởi Controller nào nữa.</p>
}

// Question 18
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Liveness probe sử dụng thuộc tính initialDelaySeconds với mục đích gì?</p>{
	~[moodle]Xác định khoảng thời gian tối đa mà probe được phép chạy.#<p>timeoutSeconds xác định thời gian chờ tối đa cho một probe.</p>
	~[moodle]Định nghĩa khoảng thời gian tối thiểu giữa các lần kiểm tra probe.#<p>periodSeconds định nghĩa khoảng thời gian giữa các lần kiểm tra probe.</p>
	=[moodle]Chỉ định số giây mà Kubernetes sẽ đợi trước khi thực hiện lần kiểm tra liveness đầu tiên sau khi container khởi động.
	~[moodle]Đặt ngưỡng số lần probe thất bại liên tiếp trước khi container được khởi động lại.#<p>failureThreshold là ngưỡng số lần probe thất bại liên tiếp.</p>
	####<p><strong>Giải thích</strong>: Thuộc tính initialDelaySeconds trong liveness probe chỉ định số giây mà Kubernetes sẽ đợi trước khi thực hiện lần kiểm tra liveness đầu tiên sau khi container được khởi động.</p>
}

// Question 19
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Điều nào sau đây là ĐÚNG về mô hình khai báo (declarative approach) của Kubernetes khi quản lý tài nguyên?</p>{
	~[moodle]Bạn chỉ cần đưa ra các lệnh từng bước để Kubernetes thực hiện các hành động cụ thể.#<p>Cách này mô tả mô hình mệnh lệnh (imperative approach), không phải khai báo.</p>
	=[moodle]Bạn chỉ định trạng thái cuối cùng mong muốn của hệ thống, và Kubernetes sẽ tự mình thực hiện các hành động cần thiết để đạt được trạng thái đó.
	~[moodle]Bạn phải liên tục theo dõi và điều chỉnh trạng thái hiện tại của hệ thống để khớp với mong muốn của mình.#<p>Các Controller Kubernetes thực hiện việc giám sát và điều chỉnh tự động.</p>
	~[moodle]Kubernetes yêu cầu bạn tự động hóa tất cả các tác vụ quản lý thông qua các script tùy chỉnh.#<p>Kubernetes cung cấp các Controller tích hợp sẵn để tự động hóa nhiều tác vụ, giảm nhu cầu script tùy chỉnh.</p>
	####<p><strong>Giải thích</strong>: Mô hình khai báo (declarative approach) là một nguyên tắc cơ bản của Kubernetes. Thay vì chỉ thị Kubernetes chính xác phải làm gì, bạn chỉ thay đổi một cách khai báo trạng thái mong muốn của hệ thống và để Kubernetes tự mình kiểm tra trạng thái thực tế hiện tại và điều hòa nó với trạng thái mong muốn.</p>
}

// Question 20
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>DaemonSet sử dụng thuộc tính nodeSelector với mục đích gì?</p>{
	~[moodle]Để chỉ định Node Master mà DaemonSet sẽ chạy.#<p>DaemonSet chạy trên Node Worker, không phải Node Master, trừ khi Node Master được cấu hình để cho phép.</p>
	=[moodle]Để đảm bảo rằng các Pods chỉ chạy trên một số Node cụ thể có nhãn khớp với bộ chọn.
	~[moodle]Để phân bổ tài nguyên CPU và bộ nhớ cho Pods của DaemonSet.#<p>Tài nguyên được phân bổ bằng resources.requests và resources.limits.</p>
	~[moodle]Để kích hoạt tính năng tự động mở rộng quy mô (autoscaling) cho DaemonSet.#<p>DaemonSet không hỗ trợ autoscaling theo cách thông thường, vì nó phải chạy trên một tập hợp Node cố định.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể sử dụng thuộc tính nodeSelector trong Pod template của DaemonSet để đảm bảo rằng các Pods chỉ chạy trên một số Node cụ thể có nhãn khớp với bộ chọn (ví dụ: chỉ trên các Node có nhãn disk: ssd).</p>
}

// Question 21
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Điều nào sau đây KHÔNG phải là một tham số cấu hình của liveness probe?</p>{
	~[moodle]periodSeconds.#<p>periodSeconds là khoảng thời gian giữa các lần kiểm tra probe.</p>
	~[moodle]timeoutSeconds.#<p>timeoutSeconds là thời gian tối đa mà probe được phép chờ phản hồi.</p>
	=[moodle]replicaCount.
	~[moodle]failureThreshold.#<p>failureThreshold là số lần probe thất bại liên tiếp trước khi hành động được thực hiện.</p>
	####<p><strong>Giải thích</strong>: replicaCount là một thuộc tính của ReplicationController hoặc Deployment, không phải là tham số cấu hình của liveness probe.</p>
}

// Question 22
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Khi một Job resource tạo ra nhiều Pods chạy song song, điều gì xảy ra nếu một trong các Pods đó thất bại?</p>{
	~[moodle]Toàn bộ Job sẽ bị đánh dấu là Failed và dừng lại.#<p>Job được thiết kế để chịu lỗi và tiếp tục cho đến khi hoàn thành.</p>
	=[moodle]Job sẽ tạo một Pod mới để thay thế Pod bị lỗi và tiếp tục chạy cho đến khi đạt được số lượng hoàn thành mong muốn.
	~[moodle]Các Pods khác đang chạy song song cũng sẽ bị dừng để đồng bộ hóa.#<p>Các Pods khác tiếp tục chạy mà không bị ảnh hưởng bởi thất bại của một Pod khác.</p>
	~[moodle]Job sẽ cố gắng khởi động lại Pod bị lỗi một số lần giới hạn trước khi dừng lại.#<p>Hành vi khởi động lại Pods bên trong Job được quản lý bởi Job controller để đảm bảo hoàn thành tổng thể.</p>
	####<p><strong>Giải thích</strong>: Nếu một trong các Pods của Job thất bại (ví dụ: container thoát với mã lỗi khác 0), Job sẽ tạo một Pod mới để thay thế và tiếp tục chạy cho đến khi đạt được số lượng hoàn thành mong muốn (spec.completions).</p>
}

// Question 23
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Bạn có thể thấy lịch sử triển khai (rollout history) của một Deployment bằng lệnh nào?</p>{
	~[moodle]kubectl get deployment &lt;tên-deployment&gt; --history.#<p>Không có tùy chọn --history cho kubectl get.</p>
	=[moodle]kubectl rollout history deployment &lt;tên-deployment&gt;.
	~[moodle]kubectl describe deployment &lt;tên-deployment&gt;.#<p>kubectl describe cung cấp thông tin chi tiết về trạng thái hiện tại của Deployment, nhưng không phải lịch sử triển khai dạng bảng.</p>
	~[moodle]kubectl logs deployment &lt;tên-deployment&gt;.#<p>kubectl logs hiển thị log của Pods, không phải lịch sử triển khai của Deployment.</p>
	####<p><strong>Giải thích</strong>: Lệnh kubectl rollout history deployment &lt;tên-deployment&gt; được sử dụng để hiển thị lịch sử triển khai của một Deployment, bao gồm các revision và nguyên nhân thay đổi (nếu được ghi lại bằng --record).</p>
}

// Question 24
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Khi một ReplicationController phản ứng với việc một Pod bị xóa thủ công, nó sẽ làm gì?</p>{
	~[moodle]Nó sẽ không làm gì, vì việc xóa thủ công nằm ngoài phạm vi quản lý của nó.#<p>Việc giám sát và điều chỉnh số lượng Pods là nhiệm vụ chính của ReplicationController.</p>
	=[moodle]Nó sẽ tạo một Pod mới ngay lập tức để duy trì số lượng bản sao mong muốn.
	~[moodle]Nó sẽ đánh dấu ReplicationController là Failed cho đến khi Pod bị xóa được phục hồi.#<p>ReplicationController không đánh dấu Failed trong trường hợp này; nó thực hiện hành động điều hòa.</p>
	~[moodle]Nó sẽ đợi 5 phút trước khi thực hiện bất kỳ hành động nào.#<p>RC phản ứng rất nhanh chóng với sự thay đổi số lượng Pods.</p>
	####<p><strong>Giải thích</strong>: ReplicationController phản ứng với việc một Pod bị xóa thủ công bằng cách tạo một Pod mới ngay lập tức để đảm bảo số lượng bản sao khớp với số lượng mong muốn (replica count).</p>
}

// Question 25
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Lệnh kubeadm init trên Node Master được sử dụng để làm gì?</p>{
	~[moodle]Để tạo một Node Worker mới và thêm nó vào cluster.#<p>kubeadm join được dùng để thêm Node Worker.</p>
	=[moodle]Để triển khai tất cả các thành phần của Kubernetes Control Plane và khởi tạo Node Master.
	~[moodle]Để xóa tất cả các tài nguyên Kubernetes khỏi Node Master.#<p>kubeadm reset được dùng để xóa các tài nguyên.</p>
	~[moodle]Để cài đặt Docker và Kubelet trên Node Master.#<p>Docker và Kubelet phải được cài đặt trước khi chạy kubeadm init.</p>
	####<p><strong>Giải thích</strong>: Lệnh kubeadm init được chạy trên Node Master để triển khai tất cả các thành phần cần thiết của Kubernetes Control Plane (etcd, API server, Scheduler, Controller Manager) và khởi tạo Node Master.</p>
}

// Question 26
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Điều nào sau đây là ĐÚNG về các loại Pods chạy trên Node Master khi sử dụng kubeadm để thiết lập cluster?</p>{
	~[moodle]Kubelet chạy như một Pod trên Node Master, quản lý các thành phần Control Plane khác.#<p>Kubelet là thành phần hệ thống, không phải Pod.</p>
	=[moodle]Kubelet luôn chạy như một thành phần hệ thống thông thường, và nó sẽ chạy tất cả các thành phần khác dưới dạng Pods.
	~[moodle]API server là thành phần duy nhất chạy như một Pod trên Node Master.#<p>Các thành phần Control Plane khác cũng chạy dưới dạng Pods, do Kubelet quản lý.</p>
	~[moodle]Tất cả các thành phần Control Plane đều chạy như các tiến trình hệ thống thông thường, không phải Pods.#<p>kubeadm triển khai các thành phần Control Plane dưới dạng Pods được quản lý bởi Kubelet.</p>
	####<p><strong>Giải thích</strong>: Kubelet là thành phần duy nhất luôn chạy như một thành phần hệ thống thông thường, và chính Kubelet sau đó sẽ chạy tất cả các thành phần khác (bao gồm các thành phần Control Plane như API server, Scheduler, Controller Manager, etcd) dưới dạng Pods.</p>
}

// Question 27
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Khi một Pod được lập lịch trên một Node, thành phần nào của Kubernetes chịu trách nhiệm chạy các container của Pod đó?</p>{
	~[moodle]Scheduler.#<p>Scheduler chỉ gán Node cho Pod.</p>
	~[moodle]Controller Manager.#<p>Controller Manager quản lý các tài nguyên cấp cluster.</p>
	=[moodle]Kubelet.
	~[moodle]kube-proxy.#<p>kube-proxy quản lý cân bằng tải mạng.</p>
	####<p><strong>Giải thích</strong>: Ngay sau khi Kubelet trên Node mục tiêu nhận thấy Pod đã được lập lịch cho Node của nó, nó sẽ hướng dẫn Container Runtime (ví dụ: Docker) kéo các ảnh container cần thiết và chạy các container.</p>
}

// Question 28
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Nếu bạn muốn chạy một ứng dụng batch job định kỳ (ví dụ: mỗi đêm lúc 3 giờ sáng), bạn nên sử dụng tài nguyên Kubernetes nào?</p>{
	~[moodle]Deployment.#<p>Deployment dùng cho các ứng dụng chạy liên tục.</p>
	~[moodle]DaemonSet.#<p>DaemonSet dùng để chạy một Pod trên mỗi Node.</p>
	=[moodle]CronJob.
	~[moodle]ReplicationController.#<p>ReplicationController dùng để duy trì số lượng Pods chạy liên tục.</p>
	####<p><strong>Giải thích</strong>: Để chạy một ứng dụng batch job định kỳ, bạn nên sử dụng tài nguyên CronJob, cho phép lập lịch các Jobs theo một biểu thức cron.</p>
}

// Question 29
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Điều nào sau đây là sai về liveness probe?</p>{
	~[moodle]Nó được cấu hình để kiểm tra định kỳ tình trạng sức khỏe của ứng dụng trong container.#<p>Liveness probe kiểm tra sức khỏe của ứng dụng.</p>
	~[moodle]Khi probe thất bại liên tiếp, container sẽ bị khởi động lại.#<p>Hành động mặc định khi liveness probe thất bại failureThreshold lần là khởi động lại container.</p>
	~[moodle]Các tham số như initialDelaySeconds có thể được dùng để trì hoãn lần kiểm tra đầu tiên.#<p>initialDelaySeconds được dùng để trì hoãn việc bắt đầu các lần kiểm tra probe.</p>
	=[moodle]Nó giúp tự động loại bỏ Pod khỏi Service nếu ứng dụng không hoạt động.
	####<p><strong>Giải thích</strong>: Liveness probe giúp khởi động lại container nếu ứng dụng gặp lỗi. Việc tự động loại bỏ Pod khỏi Service nếu ứng dụng không hoạt động hoặc không sẵn sàng để nhận yêu cầu là chức năng của readiness probe.</p>
}

// Question 30
::Chapter 4: Replication and Other Controllers: Deploying Managed Pods::[html]<p>Bạn có thể làm gì nếu muốn một Node Master trong cluster kubeadm cho phép các Pods không phải của Control Plane chạy trên đó?</p>{
	~[moodle]Kích hoạt nodeSelector trên Node Master.#<p>nodeSelector được dùng trong định nghĩa Pod để chọn Node, không phải cấu hình Node.</p>
	=[moodle]Loại bỏ taint (taint) khỏi Node Master.
	~[moodle]Thêm một readinessProbe vào Pods của Control Plane.#<p>readinessProbe kiểm tra khả năng sẵn sàng của ứng dụng, không liên quan đến việc cho phép lập lịch trên Node Master.</p>
	~[moodle]Cấu hình lại kube-proxy trên Node Master.#<p>kube-proxy chịu trách nhiệm cân bằng tải, không liên quan đến việc lập lịch Pods trên Node Master.</p>
	####<p><strong>Giải thích</strong>: Theo mặc định, Node Master trong cluster kubeadm được gắn một taint (ví dụ: node-role.kubernetes.io/master:NoSchedule) để ngăn các Pods không thuộc Control Plane lập lịch trên đó. Để cho phép các Pods khác chạy, bạn cần loại bỏ taint khỏi Node Master.</p>
}

// Chapter 5: Services: Allowing Clients to Discover and Talk to Pods
// Switch category to $module$/top/Chapter 5: Services: Allowing Clients to Discover and Talk to Pods
$CATEGORY: $module$/top/Chapter 5: Services: Allowing Clients to Discover and Talk to Pods

// Question 1
::Chapter 5: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Mục đích chính của Service trong Kubernetes là gì?</p>{
	~[moodle]Để lưu trữ dữ liệu bền vững cho các ứng dụng.#<p>Volumes và PersistentVolumes được sử dụng để lưu trữ dữ liệu bền vững.</p>
	~[moodle]Để quản lý vòng đời của các container bên trong Pods.#<p>Kubelet và các Controller như ReplicationController/Deployment quản lý vòng đời của container/Pod.</p>
	=[moodle]Để cho phép các client khám phá và giao tiếp với một hoặc nhiều Pods thông qua một địa chỉ IP và cổng ổn định.
	~[moodle]Để tự động mở rộng quy mô số lượng Pods dựa trên tải.#<p>HorizontalPodAutoscaler được sử dụng để tự động mở rộng quy mô Pods.</p>
	####<p><strong>Giải thích</strong>: Service cho phép các client khám phá và giao tiếp với một hoặc nhiều Pods thông qua một địa chỉ IP và cặp cổng duy nhất và ổn định.</p>
}

// Question 2
::Chapter 5: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Loại Service nào tạo ra một địa chỉ IP ảo (ClusterIP) chỉ có thể truy cập được từ bên trong cluster Kubernetes?</p>{
	~[moodle]NodePort.#<p>NodePort lộ Service thông qua một cổng tĩnh trên mỗi Node của cluster, có thể truy cập từ bên ngoài.</p>
	~[moodle]LoadBalancer.#<p>LoadBalancer tạo một bộ cân bằng tải bên ngoài từ nhà cung cấp đám mây, lộ Service ra bên ngoài.</p>
	=[moodle]ClusterIP.
	~[moodle]ExternalName.#<p>ExternalName ánh xạ Service đến một tên DNS bên ngoài, không phải một địa chỉ IP nội bộ.</p>
	####<p><strong>Giải thích</strong>: ClusterIP là loại Service mặc định, nó tạo ra một địa chỉ IP ảo (ClusterIP) chỉ có thể truy cập được từ bên trong cluster Kubernetes.</p>
}

// Question 3
::Chapter 5: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Khi bạn muốn lộ Service ra bên ngoài cluster thông qua một cổng tĩnh trên mỗi Node của cluster, bạn sẽ sử dụng loại Service nào?</p>{
	~[moodle]ClusterIP.#<p>ClusterIP chỉ truy cập được từ bên trong cluster.</p>
	=[moodle]NodePort.
	~[moodle]LoadBalancer.#<p>LoadBalancer tạo một bộ cân bằng tải bên ngoài và lộ Service qua đó.</p>
	~[moodle]Ingress.#<p>Ingress là tài nguyên cấp cao hơn để quản lý truy cập HTTP/HTTPS bên ngoài đến nhiều Services.</p>
	####<p><strong>Giải thích</strong>: Loại Service NodePort lộ Service thông qua một cổng tĩnh trên mỗi địa chỉ IP của Node trong cluster. Điều này cho phép client truy cập Service từ bên ngoài cluster thông qua NodeIP:NodePort.</p>
}

// Question 4
::Chapter 5: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Nếu bạn đang chạy Kubernetes trên nhà cung cấp đám mây (ví dụ: GKE, AWS), loại Service nào sẽ tự động tạo một bộ cân bằng tải bên ngoài?</p>{
	~[moodle]NodePort.#<p>NodePort lộ Service qua cổng Node, không phải bộ cân bằng tải bên ngoài.</p>
	~[moodle]ClusterIP.#<p>ClusterIP chỉ cho phép truy cập nội bộ.</p>
	=[moodle]LoadBalancer.
	~[moodle]ExternalName.#<p>ExternalName ánh xạ đến tên DNS bên ngoài, không tạo bộ cân bằng tải.</p>
	####<p><strong>Giải thích</strong>: Loại Service LoadBalancer sẽ tự động yêu cầu nhà cung cấp đám mây tạo ra một bộ cân bằng tải bên ngoài và lộ Service ra bên ngoài thông qua bộ cân bằng tải đó.</p>
}

// Question 5
::Chapter 5: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Vai trò của Endpoints resource trong Kubernetes là gì?</p>{
	~[moodle]Định nghĩa các quy tắc lập lịch trình cho Pods.#<p>Scheduler định nghĩa các quy tắc lập lịch trình cho Pods.</p>
	=[moodle]Xác định Pods (hoặc các server khác) nào được lộ thông qua một Service.
	~[moodle]Quản lý việc xác thực và ủy quyền cho API server.#<p>RBAC và các phương thức xác thực/ủy quyền khác quản lý quyền truy cập API server.</p>
	~[moodle]Lưu trữ cấu hình của cluster một cách bền vững.#<p>etcd lưu trữ cấu hình cluster một cách bền vững.</p>
	####<p><strong>Giải thích</strong>: Resource Endpoints định nghĩa các Pods (hoặc các server khác) nào được lộ thông qua một Service. Kubernetes tự động tạo và cập nhật Endpoints cho Services có bộ chọn nhãn.</p>
}

// Question 6
::Chapter 5: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Làm thế nào để các Pods khám phá các Services khác trong cùng một cluster thông qua biến môi trường?</p>{
	~[moodle]Các biến môi trường được đặt thủ công trong định nghĩa Pod trước khi tạo Service.#<p>Các biến môi trường Service được Kubernetes tự động tiêm, không phải đặt thủ công.</p>
	=[moodle]Kubernetes tự động tiêm các biến môi trường vào Pods, nhưng chỉ cho các Service đã tồn tại trước khi Pod được tạo.
	~[moodle]Các Pods phải thực hiện yêu cầu HTTP đến API server để lấy danh sách Services.#<p>Mặc dù có thể giao tiếp với API server, biến môi trường và DNS là các cơ chế khám phá Service phổ biến hơn và hiệu quả hơn.</p>
	~[moodle]Biến môi trường chỉ chứa thông tin về Node mà Pod đang chạy.#<p>Biến môi trường bao gồm cả thông tin Service host và port.</p>
	####<p><strong>Giải thích</strong>: Kubernetes tự động tiêm các biến môi trường cho các Services vào các Pods. Tuy nhiên, điều này chỉ xảy ra cho các Services đã tồn tại trước khi Pod được tạo. Nếu Service được tạo sau Pod, Pod sẽ không nhận được các biến môi trường đó.</p>
}

// Question 7
::Chapter 5: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Địa chỉ IP và cổng của Service kubia-http được lưu trữ trong những biến môi trường nào theo quy ước của Kubernetes?</p>{
	~[moodle]KUBIA_HTTP_IP và KUBIA_HTTP_PORT.#<p>Đây không phải là quy ước chuẩn của Kubernetes.</p>
	=[moodle]KUBIA_SERVICE_HOST và KUBIA_SERVICE_PORT.
	~[moodle]SERVICE_KUBIA_HTTP_HOST và SERVICE_KUBIA_HTTP_PORT.#<p>Thứ tự tên Service và SERVICE_HOST không đúng với quy ước.</p>
	~[moodle]KUBERNETES_SERVICE_HOST và KUBERNETES_SERVICE_PORT.#<p>KUBERNETES_SERVICE_HOST và KUBERNETES_SERVICE_PORT chỉ đến API server của Kubernetes, không phải các Service của người dùng.</p>
	####<p><strong>Giải thích</strong>: Địa chỉ IP của Service được lưu trữ trong biến môi trường &lt;UPPERCASE_SERVICE_NAME&gt;_SERVICE_HOST, và cổng của Service được lưu trữ trong &lt;UPPERCASE_SERVICE_NAME&gt;_SERVICE_PORT. Ví dụ: KUBIA_SERVICE_HOST và KUBIA_SERVICE_PORT cho Service tên kubia.</p>
}

// Question 8
::Chapter 5: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Làm thế nào để các Pods khám phá các Services khác trong cùng một cluster thông qua DNS?</p>{
	~[moodle]Các Pods phải gửi một yêu cầu HTTP đến kube-dns để nhận ánh xạ.#<p>kube-dns xử lý các truy vấn DNS tiêu chuẩn, không phải yêu cầu HTTP.</p>
	=[moodle]Kubernetes DNS service (kube-dns) giải quyết tên Service thành địa chỉ IP của Service hoặc IP của Pods.
	~[moodle]Các Pods phải đọc một ConfigMap được cập nhật tự động chứa tất cả các ánh xạ DNS.#<p>ConfigMaps được sử dụng để truyền cấu hình, không phải là cơ chế khám phá Service chính.</p>
	~[moodle]DNS chỉ được sử dụng để khám phá các Services bên ngoài cluster.#<p>DNS là cơ chế khám phá Service chính cho cả Services nội bộ và bên ngoài (thông qua Ingress).</p>
	####<p><strong>Giải thích</strong>: Kubernetes DNS service (kube-dns) là một Pod chạy trong cluster có nhiệm vụ giải quyết tên Service thành địa chỉ IP của Service hoặc (đối với headless service) các địa chỉ IP của các Pods backend.</p>
}

// Question 9
::Chapter 5: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Loại Service nào không có ClusterIP và thay vào đó trả về các bản ghi DNS với địa chỉ IP của các Pods backend trực tiếp?</p>{
	~[moodle]NodePort.#<p>NodePort có ClusterIP và thêm một cổng Node.</p>
	~[moodle]LoadBalancer.#<p>LoadBalancer có ClusterIP và sử dụng bộ cân bằng tải bên ngoài.</p>
	=[moodle]Headless Service.
	~[moodle]ExternalName.#<p>ExternalName ánh xạ đến tên DNS bên ngoài, không phải IP của Pod nội bộ.</p>
	####<p><strong>Giải thích</strong>: Một Headless Service được định nghĩa bằng cách đặt trường clusterIP thành None. Nó không có ClusterIP và thay vào đó, Kubernetes DNS service sẽ trả về các bản ghi DNS chứa địa chỉ IP của tất cả các Pods backend.</p>
}

// Question 10
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Ingress trong Kubernetes được sử dụng với mục đích chính là gì?</p>{
	~[moodle]Cung cấp một giao diện cho việc triển khai các ứng dụng từ mã nguồn.#<p>Các công cụ như Deployment hoặc Helm được dùng để triển khai ứng dụng.</p>
	~[moodle]Kiểm soát lưu lượng mạng giữa các Pods trong cluster.#<p>NetworkPolicy được dùng để kiểm soát lưu lượng mạng giữa các Pods.</p>
	=[moodle]Lộ một hoặc nhiều Services HTTP/HTTPS ra bên ngoài cluster thông qua một địa chỉ IP có thể truy cập bên ngoài duy nhất.
	~[moodle]Đảm bảo rằng mỗi Pod có một Volume lưu trữ dữ liệu bền vững.#<p>PersistentVolumes và PersistentVolumeClaims được dùng cho lưu trữ dữ liệu bền vững.</p>
	####<p><strong>Giải thích</strong>: Ingress được sử dụng để lộ một hoặc nhiều Services ra bên ngoài cluster thông qua một địa chỉ IP có thể truy cập bên ngoài duy nhất, thường là cho lưu lượng HTTP và HTTPS.</p>
}

// Question 11
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Để Ingress Controller có thể xử lý lưu lượng TLS (HTTPS), nó cần được cung cấp loại tài nguyên nào chứa chứng chỉ và khóa riêng?</p>{
	~[moodle]ConfigMap.#<p>ConfigMap dùng để lưu trữ dữ liệu cấu hình không nhạy cảm.</p>
	=[moodle]Secret.
	~[moodle]PersistentVolume.#<p>PersistentVolume là tài nguyên lưu trữ bền vững.</p>
	~[moodle]ServiceAccount.#<p>ServiceAccount cung cấp định danh cho các ứng dụng chạy trong Pods để tương tác với API server.</p>
	####<p><strong>Giải thích</strong>: Để Ingress Controller có thể xử lý lưu lượng TLS, nó cần được cung cấp một tài nguyên Secret chứa chứng chỉ và khóa riêng tư cho miền đó. Ingress sẽ tham chiếu đến Secret này để sử dụng.</p>
}

// Question 12
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Readiness probe khác với liveness probe ở điểm nào?</p>{
	~[moodle]Readiness probe kiểm tra sức khỏe của ứng dụng, còn liveness probe kiểm tra khả năng sẵn sàng nhận yêu cầu.#<p>Ngược lại, liveness probe kiểm tra sức khỏe, readiness probe kiểm tra khả năng sẵn sàng.</p>
	=[moodle]Readiness probe loại bỏ Pod khỏi Service nếu ứng dụng không sẵn sàng, còn liveness probe khởi động lại container nếu ứng dụng không hoạt động.
	~[moodle]Liveness probe chỉ được chạy một lần khi Pod khởi động, còn readiness probe chạy liên tục.#<p>Cả hai loại probe đều chạy định kỳ.</p>
	~[moodle]Readiness probe chỉ hoạt động với các ứng dụng web, còn liveness probe hoạt động với mọi loại ứng dụng.#<p>Cả hai loại probe đều có thể được cấu hình cho nhiều loại ứng dụng, không chỉ ứng dụng web.</p>
	####<p><strong>Giải thích</strong>: Readiness probe kiểm tra xem container có sẵn sàng để nhận yêu cầu hay không; nếu nó báo không sẵn sàng, Pod sẽ bị loại bỏ khỏi Service. Liveness probe kiểm tra xem ứng dụng có đang chạy hay không; nếu nó thất bại, container sẽ được khởi động lại.</p>
}

// Question 13
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Khi một Pod được đánh dấu là "Not Ready" bởi readiness probe, điều gì xảy ra?</p>{
	~[moodle]Kubernetes sẽ tự động xóa Pod đó.#<p>Pod sẽ không bị xóa ngay lập tức mà vẫn tiếp tục chạy.</p>
	=[moodle]Pod đó sẽ bị loại bỏ khỏi danh sách các Endpoint của Service và không nhận được lưu lượng truy cập nữa.
	~[moodle]Container bên trong Pod sẽ được khởi động lại ngay lập tức.#<p>Khởi động lại container là hành động của liveness probe khi thất bại.</p>
	~[moodle]Kubernetes sẽ chuyển Pod đó sang một Node khác.#<p>Chuyển Pod sang Node khác xảy ra khi Node bị lỗi, không phải khi Pod không sẵn sàng.</p>
	####<p><strong>Giải thích</strong>: Khi một Pod báo rằng nó không sẵn sàng ("Not Ready") thông qua readiness probe, nó sẽ bị loại bỏ khỏi danh sách các Endpoint của Service. Nếu sau đó Pod trở nên sẵn sàng trở lại, nó sẽ được thêm lại.</p>
}

// Question 14
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Thuộc tính sessionAffinity: ClientIP trong định nghĩa Service có tác dụng gì?</p>{
	=[moodle]Đảm bảo rằng tất cả các yêu cầu từ cùng một địa chỉ IP client sẽ được chuyển đến cùng một Pod.
	~[moodle]Chỉ cho phép các client có địa chỉ IP cụ thể truy cập Service.#<p>SecurityGroup hoặc NetworkPolicy được dùng để kiểm soát quyền truy cập dựa trên IP.</p>
	~[moodle]Ưu tiên các Pods trên cùng một Node để xử lý các yêu cầu của client.#<p>Có các quy tắc lập lịch trình để ưu tiên Pods trên cùng Node (ví dụ: podAntiAffinity với topologyKey: kubernetes.io/hostname).</p>
	~[moodle]Đảm bảo rằng Service chỉ được tạo trong một Vùng sẵn sàng (Availability Zone) duy nhất.#<p>Tính sẵn sàng cao thường được đảm bảo bằng cách phân phối tài nguyên trên nhiều Availability Zones.</p>
	####<p><strong>Giải thích</strong>: Thuộc tính sessionAffinity: ClientIP được sử dụng để cấu hình Service nhằm đảm bảo rằng tất cả các yêu cầu từ cùng một địa chỉ IP client sẽ được chuyển đến cùng một Pod.</p>
}

// Question 15
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Nếu bạn muốn cấu hình một Service mà không cần Kubernetes tự động tìm kiếm các Pods backend (ví dụ: để trỏ đến một cơ sở dữ liệu bên ngoài cluster), bạn sẽ định nghĩa Service đó như thế nào?</p>{
	=[moodle]Bằng cách không chỉ định bất kỳ label selector nào trong spec.selector và định nghĩa Endpoints resource thủ công.
	~[moodle]Bằng cách đặt clusterIP: None và để Kubernetes tự tìm kiếm các IP bên ngoài.#<p>clusterIP: None tạo một headless service cho các Pods nội bộ.</p>
	~[moodle]Bằng cách sử dụng loại Service ExternalName và cung cấp một tên miền.#<p>Loại ExternalName ánh xạ đến một tên DNS, không phải địa chỉ IP cụ thể mà bạn muốn quản lý thông qua Endpoints.</p>
	~[moodle]Bằng cách đặt type: LoadBalancer và cung cấp một địa chỉ IP bên ngoài.#<p>type: LoadBalancer tự động tạo bộ cân bằng tải cho các Pods nội bộ.</p>
	####<p><strong>Giải thích</strong>: Để tạo một Service không có bộ chọn nhãn và trỏ đến các backend không phải Pod Kubernetes (hoặc các Pods không được quản lý bởi Controller), bạn không chỉ định trường spec.selector và sau đó tạo một Endpoints resource thủ công để liệt kê các địa chỉ IP và cổng của các backend đó.</p>
}

// Question 16
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Điều nào sau đây KHÔNG phải là một cách để lộ một Service HTTP/HTTPS ra bên ngoài cluster?</p>{
	~[moodle]Sử dụng Service loại NodePort.#<p>NodePort lộ Service qua cổng Node.</p>
	~[moodle]Sử dụng Service loại LoadBalancer.#<p>LoadBalancer tạo bộ cân bằng tải bên ngoài.</p>
	~[moodle]Sử dụng tài nguyên Ingress.#<p>Ingress quản lý truy cập HTTP/HTTPS bên ngoài đến nhiều Services.</p>
	=[moodle]Sử dụng Service loại ClusterIP trực tiếp.
	####<p><strong>Giải thích</strong>: Service loại ClusterIP chỉ cung cấp địa chỉ IP ảo có thể truy cập được từ bên trong cluster và không trực tiếp lộ Service ra bên ngoài.</p>
}

// Question 17
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Khi cấu hình Ingress, bạn có thể định nghĩa các quy tắc để ánh xạ các Service khác nhau tới các đường dẫn (paths) khác nhau của cùng một tên miền (host) như thế nào?</p>{
	~[moodle]Ingress không hỗ trợ việc ánh xạ nhiều đường dẫn trên cùng một tên miền.#<p>Ingress được thiết kế để hỗ trợ việc này.</p>
	=[moodle]Bằng cách định nghĩa nhiều path trong một rule.http.paths của Ingress resource.
	~[moodle]Bằng cách tạo một Ingress resource riêng biệt cho mỗi đường dẫn.#<p>Mặc dù có thể tạo nhiều Ingress, việc định nghĩa nhiều đường dẫn trong một Ingress là cách hiệu quả hơn cho cùng một tên miền.</p>
	~[moodle]Bằng cách sử dụng sessionAffinity: ClientIP trong Service.#<p>sessionAffinity là thuộc tính của Service, không liên quan đến cấu hình ánh xạ đường dẫn của Ingress.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể ánh xạ các Service khác nhau đến các đường dẫn khác nhau của cùng một tên miền bằng cách định nghĩa nhiều path trong một rule.http.paths của Ingress resource, mỗi path trỏ đến một backend.serviceName và backend.servicePort khác nhau.</p>
}

// Question 18
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Khi một Service đã được tạo trước một Pod, làm thế nào Pod đó có thể khám phá địa chỉ IP và cổng của Service thông qua biến môi trường?</p>{
	~[moodle]Pod tự động nhận các biến môi trường khi nó được lập lịch trên Node.#<p>Pod nhận các biến môi trường của Service khi container được tạo, không phải khi Pod được lập lịch.</p>
	=[moodle]Các biến môi trường được tiêm vào container của Pod khi Kubelet khởi động container.
	~[moodle]Pod phải thực hiện yêu cầu DNS để lấy các biến môi trường.#<p>DNS là một cơ chế khám phá khác, không phải cách lấy biến môi trường.</p>
	~[moodle]Các biến môi trường được đọc từ một tệp cấu hình trên Node.#<p>Các biến môi trường được tiêm vào môi trường runtime của container.</p>
	####<p><strong>Giải thích</strong>: Khi một Service được tạo trước một Pod, các biến môi trường chứa thông tin của Service sẽ được tiêm vào các container của Pod khi Kubelet khởi động container.</p>
}

// Question 19
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Nguyên tắc nào được sử dụng bởi kube-proxy trong chế độ iptables để chuyển tiếp lưu lượng đến Pods backend của Service?</p>{
	~[moodle]kube-proxy mở một kết nối TCP đến mỗi Pod và chuyển tiếp các gói tin.#<p>Chế độ userspace sử dụng một proxy thực sự, nhưng chế độ iptables trực tiếp sửa đổi gói tin.</p>
	=[moodle]kube-proxy ghi lại các quy tắc iptables trên Node để sửa đổi gói tin và định tuyến chúng đến một Pod backend được chọn ngẫu nhiên.
	~[moodle]kube-proxy tạo một giao diện mạng ảo cho mỗi Pod và định tuyến trực tiếp các gói tin.#<p>kube-proxy không tạo giao diện mạng ảo cho mỗi Pod; Pods có giao diện mạng riêng.</p>
	~[moodle]kube-proxy chạy một máy chủ proxy HTTP để quản lý lưu lượng truy cập.#<p>kube-proxy không chạy máy chủ proxy HTTP; đó là chức năng của Ingress controller hoặc Load Balancer.</p>
	####<p><strong>Giải thích</strong>: Trong chế độ iptables, kube-proxy ghi lại các quy tắc iptables trên Node. Khi một gói tin đến với địa chỉ IP/cổng của Service, các quy tắc này sẽ sửa đổi địa chỉ IP và cổng đích của gói tin, chuyển hướng nó đến một Pod backend được chọn ngẫu nhiên.</p>
}

// Question 20
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Khi một Service không có bộ chọn nhãn, bạn phải làm gì để Kubernetes biết Pods nào thuộc Service đó?</p>{
	~[moodle]Kubernetes sẽ tự động gán tất cả Pods trong cùng Namespace cho Service đó.#<p>Kubernetes không tự động gán Pods cho Service không có bộ chọn.</p>
	=[moodle]Bạn phải tạo thủ công một tài nguyên Endpoints và liệt kê các địa chỉ IP của Pods.
	~[moodle]Service đó sẽ không bao giờ có Pods backend.#<p>Service không có bộ chọn có thể có Pods backend nếu bạn tạo Endpoints thủ công.</p>
	~[moodle]Service sẽ chỉ hoạt động với các Pods có cùng tên với Service.#<p>Tên Pod không liên quan trực tiếp đến việc Service tìm kiếm backend nếu không có bộ chọn nhãn.</p>
	####<p><strong>Giải thích</strong>: Khi một Service không có bộ chọn nhãn (spec.selector), Kubernetes không thể tự động tìm kiếm các Pods backend. Trong trường hợp này, bạn phải tạo thủ công một tài nguyên Endpoints và liệt kê các địa chỉ IP của Pods (hoặc các điểm cuối mạng khác) mà bạn muốn Service chuyển tiếp lưu lượng đến.</p>
}

// Question 21
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Nếu bạn muốn kết nối từ máy cục bộ của mình đến một Service chạy bên trong cluster Kubernetes, nhưng Service đó không có External IP, bạn có thể sử dụng lệnh nào?</p>{
	~[moodle]kubectl exec &lt;pod-name&gt; -- &lt;lệnh&gt;.#<p>kubectl exec chạy lệnh bên trong container của Pod.</p>
	~[moodle]kubectl logs &lt;pod-name&gt;.#<p>kubectl logs hiển thị log của container.</p>
	=[moodle]kubectl port-forward svc/&lt;service-name&gt; &lt;cổng-cục-bộ&gt;:&lt;cổng-dịch-vụ&gt;.
	~[moodle]kubectl proxy.#<p>kubectl proxy tạo một proxy cục bộ đến Kubernetes API server, không phải trực tiếp đến một Service cụ thể của ứng dụng.</p>
	####<p><strong>Giải thích</strong>: Nếu Service của bạn không có External IP (ví dụ: là ClusterIP hoặc NodePort không được lộ ra ngoài), bạn có thể sử dụng lệnh kubectl port-forward svc/&lt;service-name&gt; &lt;cổng-cục-bộ&gt;:&lt;cổng-dịch-vụ&gt; để tạo một đường hầm tạm thời và truy cập Service từ máy cục bộ.</p>
}

// Question 22
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Điều nào sau đây là ĐÚNG về việc lộ nhiều cổng trong cùng một Service?</p>{
	~[moodle]Một Service chỉ có thể lộ một cổng duy nhất cho tất cả các Pods backend.#<p>Điều này là sai, Service có thể lộ nhiều cổng.</p>
	=[moodle]Một Service có thể lộ nhiều cổng, nhưng mỗi cổng phải có một tên duy nhất và được ánh xạ đến một containerPort khác.
	~[moodle]Để lộ nhiều cổng, bạn phải tạo một Service riêng biệt cho mỗi cổng.#<p>Bạn có thể lộ nhiều cổng trong một Service duy nhất.</p>
	~[moodle]Việc lộ nhiều cổng chỉ có thể thực hiện được với Service loại LoadBalancer.#<p>Tất cả các loại Service (ClusterIP, NodePort, LoadBalancer) đều có thể lộ nhiều cổng.</p>
	####<p><strong>Giải thích</strong>: Một Service có thể lộ nhiều cổng. Trong trường hợp này, mỗi mục cổng trong spec.ports phải có một tên duy nhất và được ánh xạ đến containerPort thích hợp trên Pods backend.</p>
}

// Question 23
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Làm thế nào để bạn đảm bảo rằng một ứng dụng web không nhận lưu lượng truy cập từ Service trong khi nó đang khởi động hoặc thực hiện các tác vụ khởi tạo mất thời gian?</p>{
	~[moodle]Cấu hình một liveness probe để khởi động lại container nếu ứng dụng chưa sẵn sàng.#<p>Liveness probe khởi động lại container, không phải điều khiển lưu lượng từ Service.</p>
	=[moodle]Sử dụng một readiness probe để báo hiệu cho Service khi ứng dụng đã sẵn sàng nhận yêu cầu.
	~[moodle]Đặt initialDelaySeconds rất dài cho Pod.#<p>initialDelaySeconds trì hoãn việc bắt đầu probe, không điều khiển việc nhận lưu lượng khi chưa sẵn sàng.</p>
	~[moodle]Tắt hoàn toàn Service cho đến khi ứng dụng khởi động xong.#<p>Tắt hoàn toàn Service sẽ khiến ứng dụng không thể truy cập được, không phải giải pháp quản lý lưu lượng thông minh.</p>
	####<p><strong>Giải thích</strong>: Bằng cách sử dụng một readiness probe, ứng dụng có thể báo hiệu cho Kubernetes khi nó đã sẵn sàng nhận lưu lượng truy cập. Nếu ứng dụng chưa sẵn sàng, Pod sẽ bị loại bỏ khỏi Service và không nhận yêu cầu.</p>
}

// Question 24
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Khi sử dụng Ingress để lộ Services, điều nào sau đây là ĐÚNG về host trong rule?</p>{
	~[moodle]host là tên miền bên trong cluster, ví dụ my-service.default.svc.cluster.local.#<p>Đó là tên miền FQDN của Service nội bộ, không phải host trong Ingress.</p>
	=[moodle]host là tên miền công khai mà client sẽ sử dụng để truy cập Services.
	~[moodle]host là địa chỉ IP của Node Worker mà Ingress Controller chạy trên đó.#<p>Ingress Controller chạy như một Pod trên Node Worker, nhưng host không phải là địa chỉ IP của Node.</p>
	~[moodle]host là tên của Service được lộ ra.#<p>Tên Service được chỉ định trong backend.serviceName của rule.</p>
	####<p><strong>Giải thích</strong>: Trong định nghĩa Ingress, host trong rule là tên miền công khai mà client sẽ sử dụng để truy cập Services (ví dụ: kubia.example.com).</p>
}

// Question 25
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Thành phần nào chịu trách nhiệm cài đặt các quy tắc iptables trên các Node để thực hiện cân bằng tải cho Services trong chế độ iptables?</p>{
	~[moodle]Kubelet.#<p>Kubelet quản lý container và Pods trên Node.</p>
	~[moodle]Scheduler.#<p>Scheduler gán Pods cho Node.</p>
	=[moodle]kube-proxy.
	~[moodle]Controller Manager.#<p>Controller Manager quản lý các Controller cấp cluster.</p>
	####<p><strong>Giải thích</strong>: kube-proxy là thành phần chịu trách nhiệm cài đặt các quy tắc iptables trên các Node để thực hiện cân bằng tải và định tuyến lưu lượng mạng đến các Pods backend của Service trong chế độ iptables.</p>
}

// Question 26
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Điều nào sau đây là SAI về kubectl exec?</p>{
	~[moodle]Nó cho phép bạn chạy các lệnh tùy ý bên trong một container đang chạy của một Pod.#<p>kubectl exec được thiết kế để chạy các lệnh tùy ý trong container.</p>
	=[moodle]Nó là cách tốt nhất để thay đổi cấu hình ứng dụng một cách vĩnh viễn trong container.
	~[moodle]Nó hữu ích khi bạn muốn kiểm tra môi trường hoặc trạng thái của một container.#<p>kubectl exec rất hữu ích để gỡ lỗi và kiểm tra môi trường bên trong container.</p>
	~[moodle]Nó có thể được sử dụng để chạy shell tương tác bên trong container (với -it).#<p>Với tùy chọn -it, bạn có thể chạy một shell tương tác bên trong container.</p>
	####<p><strong>Giải thích</strong>: kubectl exec chỉ chạy lệnh bên trong container, không phải là cách tốt nhất để thay đổi cấu hình một cách vĩnh viễn vì các thay đổi trong container thường bị mất khi nó khởi động lại. Cấu hình nên được quản lý bằng ConfigMaps hoặc Secrets.</p>
}

// Question 27
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Tại sao việc sử dụng Headless Service lại quan trọng đối với StatefulSet?</p>{
	~[moodle]Để StatefulSet có thể sử dụng địa chỉ IP ổn định cho toàn bộ Service.#<p>Headless Service không có ClusterIP; nó cung cấp IP của từng Pod.</p>
	=[moodle]Để cho phép mỗi Pod trong StatefulSet có một danh tính mạng ổn định và có thể khám phá các Pods ngang hàng khác.
	~[moodle]Để Headless Service có thể cung cấp khả năng cân bằng tải cho StatefulSet.#<p>Headless Service không cung cấp cân bằng tải trực tiếp qua ClusterIP; client phải tự xử lý việc cân bằng tải dựa trên các IP Pod được trả về.</p>
	~[moodle]Để đảm bảo rằng StatefulSet luôn được triển khai trên cùng một Node.#<p>StatefulSet đảm bảo danh tính ổn định, nhưng Pod vẫn có thể được lập lịch lại trên các Node khác.</p>
	####<p><strong>Giải thích</strong>: Headless Service được sử dụng với StatefulSet để cung cấp danh tính mạng ổn định cho mỗi Pod trong StatefulSet. Thay vì một ClusterIP duy nhất, Headless Service cung cấp các bản ghi DNS trỏ trực tiếp đến địa chỉ IP của từng Pod, cho phép các Pods trong StatefulSet khám phá và giao tiếp với các Pods ngang hàng.</p>
}

// Question 28
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Nếu bạn muốn chạy một Service chỉ có thể truy cập được qua tên DNS của nó và không qua một địa chỉ IP ảo (ClusterIP) nào, bạn sẽ cấu hình trường clusterIP như thế nào trong Service Spec?</p>{
	~[moodle]Bỏ qua trường clusterIP.#<p>Nếu clusterIP bị bỏ qua, Kubernetes sẽ tự động gán một ClusterIP.</p>
	~[moodle]Đặt clusterIP: 0.0.0.0.#<p>0.0.0.0 thường được dùng để chỉ lắng nghe trên tất cả các giao diện, không phải để tạo headless service.</p>
	=[moodle]Đặt clusterIP: None.
	~[moodle]Đặt clusterIP: localhost.#<p>localhost là địa chỉ loopback, không thích hợp cho Service.</p>
	####<p><strong>Giải thích</strong>: Để tạo một Headless Service (không có ClusterIP), bạn phải đặt trường clusterIP thành None trong Service Spec.</p>
}

// Question 29
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Điều nào sau đây là SAI về việc sử dụng sessionAffinity trong Service?</p>{
	~[moodle]Nó cố gắng chuyển các yêu cầu từ cùng một client IP đến cùng một Pod backend.#<p>Đây là mục đích chính của sessionAffinity: ClientIP.</p>
	~[moodle]Nó chỉ hoạt động với các giao thức TCP hoặc UDP.#<p>sessionAffinity hoạt động với cả TCP và UDP.</p>
	=[moodle]Nó đảm bảo rằng tất cả các yêu cầu từ một client sẽ luôn được xử lý bởi cùng một Pod, ngay cả khi Pod đó bị khởi động lại.
	~[moodle]sessionAffinity chỉ có thể được đặt thành ClientIP hoặc None.#<p>Các giá trị hợp lệ cho sessionAffinity là ClientIP hoặc None.</p>
	####<p><strong>Giải thích</strong>: sessionAffinity cố gắng đảm bảo các yêu cầu từ cùng một client IP đi đến cùng một Pod. Tuy nhiên, nếu Pod bị khởi động lại hoặc bị xóa, phiên (session) sẽ bị phá vỡ và các yêu cầu tiếp theo từ client đó có thể được chuyển đến một Pod khác. Nó không đảm bảo duy trì liên tục qua các lần khởi động lại Pod.</p>
}

// Question 30
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Để Ingress Controller trong Minikube có thể xử lý các yêu cầu từ bên ngoài, bạn cần cài đặt add-on nào?</p>{
	~[moodle]kube-dns.#<p>kube-dns cung cấp dịch vụ DNS nội bộ.</p>
	~[moodle]kubernetes-dashboard.#<p>kubernetes-dashboard cung cấp giao diện web cho cluster.</p>
	=[moodle]nginx-ingress-controller.
	~[moodle]heapster.#<p>heapster thu thập chỉ số tài nguyên.</p>
	####<p><strong>Giải thích</strong>: Ingress là một API resource, nhưng nó không thực hiện proxying trực tiếp. Để Ingress hoạt động, bạn cần một Ingress Controller đang chạy trong cluster (ví dụ: nginx-ingress-controller). Minikube cung cấp nó dưới dạng một add-on.</p>
}

// Question 31
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Khi Service loại LoadBalancer được tạo, nó sẽ tự động tạo ra những Service loại nào khác đi kèm?</p>{
	~[moodle]Chỉ ClusterIP.#<p>Nó tạo ra cả ClusterIP và NodePort.</p>
	~[moodle]Chỉ NodePort.#<p>Nó tạo ra cả ClusterIP và NodePort.</p>
	=[moodle]Cả ClusterIP và NodePort.
	~[moodle]Không tạo thêm loại Service nào khác.#<p>Các Service LoadBalancer được xây dựng dựa trên NodePort và ClusterIP.</p>
	####<p><strong>Giải thích</strong>: Khi bạn tạo một Service loại LoadBalancer, Kubernetes không chỉ tạo ra một bộ cân bằng tải bên ngoài mà còn tự động tạo ra một Service loại NodePort và một Service loại ClusterIP đi kèm. Cả ba cấp độ này hoạt động cùng nhau để lộ ứng dụng ra bên ngoài.</p>
}

// Question 32
::Chapter 5\: Services: Allowing Clients to Discover and Talk to Pods::[html]<p>Giả sử bạn có một ứng dụng backend được lộ thông qua Service với tên backend-service. Các Pods khác trong cùng Namespace có thể truy cập backend-service bằng tên miền nào?</p>{
	~[moodle]backend-service.default.svc.cluster.local.#<p>Đây là tên miền đầy đủ (FQDN) nếu Service nằm trong Namespace default.</p>
	~[moodle]backend-service.svc.cluster.local.#<p>Đây là tên miền FQDN không đầy đủ, bỏ qua Namespace.</p>
	~[moodle]backend-service.cluster.local.#<p>Đây là tên miền FQDN không đầy đủ, bỏ qua Namespace và svc.</p>
	=[moodle]backend-service.
	####<p><strong>Giải thích</strong>: Các Pods trong cùng một Namespace có thể truy cập một Service khác trong cùng Namespace đó bằng cách sử dụng tên ngắn của Service (ví dụ: backend-service). Tên miền đầy đủ (FQDN) là backend-service.namespace.svc.cluster.local.</p>
}

// Chapter 6: Volumes: Attaching Disk Storage to Containers
// Switch category to $module$/top/Chapter 6: Volumes: Attaching Disk Storage to Containers
$CATEGORY: $module$/top/Chapter 6: Volumes: Attaching Disk Storage to Containers

// Question 1
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Mục đích chính của Volumes trong Kubernetes là gì?</p>{
	~[moodle]Để cung cấp bộ nhớ RAM cho các container.#<p>RAM được quản lý thông qua yêu cầu và giới hạn tài nguyên (resource requests/limits).</p>
	=[moodle]Để gắn bộ nhớ đĩa vào các container và cho phép chia sẻ dữ liệu giữa các container trong cùng một Pod.
	~[moodle]Để định nghĩa cấu hình mạng cho các Pods.#<p>Cấu hình mạng được quản lý bởi Service, NetworkPolicy, v.v..</p>
	~[moodle]Để tạo các bản sao lưu tự động của dữ liệu ứng dụng.#<p>Volumes cung cấp khả năng lưu trữ bền vững, nhưng việc sao lưu tự động thường cần các giải pháp cụ thể hơn (ví dụ: snapshot của PersistentVolume).</p>
	####<p><strong>Giải thích</strong>: Volumes được sử dụng để cung cấp bộ nhớ đĩa cho các container của Pod và cho phép chia sẻ dữ liệu giữa các container trong cùng một Pod.</p>
}

// Question 2
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Điều nào sau đây là ĐÚNG về chu kỳ sống của một Volume trong Kubernetes?</p>{
	=[moodle]Volume được tạo khi Pod khởi động và bị hủy khi Pod bị xóa.
	~[moodle]Volume được tạo một lần và tồn tại vĩnh viễn, ngay cả khi Pod bị xóa.#<p>PersistentVolumes có thể tồn tại độc lập với Pod, nhưng một Volume của Pod thì không.</p>
	~[moodle]Volume được tạo và hủy cùng với mỗi container bên trong Pod.#<p>Nội dung của Volume sẽ tồn tại qua các lần khởi động lại container.</p>
	~[moodle]Volume có thể được gắn vào nhiều Pods chạy trên các Node khác nhau cùng một lúc.#<p>Khả năng này phụ thuộc vào accessModes của PersistentVolume và loại lưu trữ cơ bản (ReadWriteMany là hiếm).</p>
	####<p><strong>Giải thích</strong>: Volume là một thành phần của Pod và chia sẻ cùng chu kỳ sống với Pod. Điều này có nghĩa là một Volume được tạo khi Pod được khởi động và bị hủy khi Pod bị xóa.</p>
}

// Question 3
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Volume loại emptyDir có đặc điểm chính là gì?</p>{
	~[moodle]Nó cung cấp bộ nhớ bền vững được gắn từ đĩa vật lý của Node.#<p>hostPath hoặc gcePersistentDisk/awsElasticBlockStore cung cấp bộ nhớ bền vững.</p>
	=[moodle]Nó được tạo rỗng khi Pod khởi động và bị xóa khi Pod kết thúc.
	~[moodle]Nó clone một Git repository vào Pod khi khởi động.#<p>gitRepo Volume clone một Git repository.</p>
	~[moodle]Nó là một loại Volume chỉ có thể đọc được (read-only).#<p>emptyDir là Volume có thể đọc-ghi.</p>
	####<p><strong>Giải thích</strong>: Volume emptyDir được tạo rỗng khi Pod được khởi động và bị xóa khi Pod kết thúc (bị xóa khỏi Node). Nó là một không gian làm việc tạm thời.</p>
}

// Question 4
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Để cải thiện hiệu suất của Volume emptyDir cho dữ liệu tạm thời rất nhạy cảm với độ trễ (latency), bạn có thể cấu hình nó để sử dụng phương tiện lưu trữ nào?</p>{
	~[moodle]Đĩa cứng (HDD).#<p>Đĩa cứng chậm hơn RAM.</p>
	=[moodle]Bộ nhớ RAM (Memory).
	~[moodle]Persistent Disk (ví dụ: GCE Persistent Disk).#<p>Persistent Disk là lưu trữ bền vững, không phải tạm thời hiệu suất cao cho emptyDir.</p>
	~[moodle]NFS share.#<p>NFS share là lưu trữ mạng, không được dùng cho emptyDir.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể cấu hình Volume emptyDir để sử dụng bộ nhớ RAM (medium: Memory). Điều này sẽ làm cho dữ liệu được lưu trữ trong tmpfs (hệ thống tệp tạm thời dựa trên RAM), cung cấp hiệu suất cao hơn cho dữ liệu tạm thời.</p>
}

// Question 5
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Hạn chế chính của Volume loại hostPath là gì khi Pod có thể được lập lịch trên bất kỳ Node nào trong cluster?</p>{
	~[moodle]Dữ liệu trên hostPath không tồn tại khi Pod bị xóa.#<p>Dữ liệu trên hostPath tồn tại ngay cả khi Pod bị xóa, miễn là Node vẫn hoạt động.</p>
	~[moodle]hostPath không thể chia sẻ dữ liệu giữa các container trong cùng một Pod.#<p>hostPath có thể chia sẻ dữ liệu giữa các container trong cùng một Pod, giống như bất kỳ Volume nào khác.</p>
	=[moodle]hostPath gắn Pod vào một Node cụ thể, làm giảm tính linh hoạt và khả năng phục hồi của Pod khi Node bị lỗi.
	~[moodle]hostPath chỉ hỗ trợ các tệp đọc-ghi, không hỗ trợ các tệp thực thi.#<p>hostPath hỗ trợ cả tệp đọc-ghi và tệp thực thi.</p>
	####<p><strong>Giải thích</strong>: Hạn chế chính của hostPath là nó gắn Pod vào một Node cụ thể (nếu Pod cần truy cập một đường dẫn cụ thể trên Node đó). Nếu Pod được lập lịch lại trên một Node khác, nó sẽ không thể truy cập dữ liệu cũ. Điều này làm giảm tính linh hoạt và khả năng phục hồi của Pod khi Node bị lỗi.</p>
}

// Question 6
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Volume loại gitRepo được sử dụng với mục đích gì?</p>{
	~[moodle]Để gắn một ổ đĩa cứng vật lý từ Node vào Pod.#<p>hostPath gắn ổ đĩa vật lý.</p>
	=[moodle]Để clone một Git repository vào một thư mục bên trong Pod khi Pod khởi động.
	~[moodle]Để cung cấp một không gian lưu trữ tạm thời cho các Pods cần dữ liệu tốc độ cao.#<p>emptyDir với medium: Memory cung cấp không gian tạm thời tốc độ cao.</p>
	~[moodle]Để truy cập các tệp cấu hình không thay đổi được từ API server.#<p>ConfigMap hoặc Secret Volumes được sử dụng cho cấu hình.</p>
	####<p><strong>Giải thích</strong>: Volume gitRepo được sử dụng để clone một Git repository vào một thư mục bên trong Pod khi Pod khởi động.</p>
}

// Question 7
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Điều nào sau đây KHÔNG phải là một trong những loại Volume cụ thể của nhà cung cấp đám mây (Cloud Provider Specific Volumes) được đề cập?</p>{
	~[moodle]gcePersistentDisk (Google Compute Engine Persistent Disk).#<p>gcePersistentDisk là của Google Cloud.</p>
	~[moodle]awsElasticBlockStore (AWS Elastic Block Store).#<p>awsElasticBlockStore là của AWS.</p>
	~[moodle]azureDisk (Azure Disk).#<p>azureDisk là của Microsoft Azure (không được đề cập chi tiết trong các nguồn nhưng là một loại tương tự).</p>
	=[moodle]nfs (Network File System).
	####<p><strong>Giải thích</strong>: nfs (Network File System) là một loại Volume được hỗ trợ rộng rãi nhưng không phải là loại Volume cụ thể của một nhà cung cấp đám mây; nó là một loại lưu trữ mạng chung.</p>
}

// Question 8
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Mục đích của PersistentVolume (PV) trong Kubernetes là gì?</p>{
	~[moodle]Là một yêu cầu lưu trữ của người dùng/Pod.#<p>PersistentVolumeClaim (PVC) là yêu cầu lưu trữ của người dùng.</p>
	=[moodle]Trừu tượng hóa việc cung cấp lưu trữ vật lý thực tế từ nhà cung cấp đám mây hoặc on-premises.
	~[moodle]Là một loại Volume tạm thời được tạo cùng Pod.#<p>emptyDir là loại Volume tạm thời được tạo cùng Pod.</p>
	~[moodle]Là một thư mục trên Node Worker được gắn vào Pod.#<p>hostPath là một thư mục trên Node Worker.</p>
	####<p><strong>Giải thích</strong>: PersistentVolume (PV) là một tài nguyên cấp cluster được quản trị viên cluster cung cấp, trừu tượng hóa việc cung cấp lưu trữ vật lý thực tế (ví dụ: một GCE Persistent Disk, NFS share, EBS) và đăng ký nó trong Kubernetes.</p>
}

// Question 9
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>PersistentVolumeClaim (PVC) được sử dụng để làm gì?</p>{
	~[moodle]Để định nghĩa loại lưu trữ động (dynamically-provisioned storage).#<p>StorageClass định nghĩa loại lưu trữ động.</p>
	=[moodle]Là một yêu cầu của Pod về một loại lưu trữ cụ thể với dung lượng và chế độ truy cập mong muốn.
	~[moodle]Để cung cấp lưu trữ vật lý cho cluster.#<p>PersistentVolume cung cấp lưu trữ vật lý.</p>
	~[moodle]Để quản lý việc sao lưu tự động cho PersistentVolume.#<p>Việc sao lưu tự động thường là một tính năng của nhà cung cấp lưu trữ hoặc một giải pháp bên ngoài.</p>
	####<p><strong>Giải thích</strong>: PersistentVolumeClaim (PVC) là một tài nguyên có Namespace, đại diện cho yêu cầu của người dùng/Pod về một loại lưu trữ cụ thể, chỉ định dung lượng tối thiểu và chế độ truy cập mong muốn.</p>
}

// Question 10
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Chế độ truy cập ReadWriteOnce (RWO) cho PersistentVolume có nghĩa là gì?</p>{
	~[moodle]Volume có thể được gắn bởi nhiều Node để đọc và ghi.#<p>ReadWriteMany (RWX) là chế độ truy cập cho phép nhiều Node đọc và ghi, nhưng không phải tất cả các loại lưu trữ đều hỗ trợ.</p>
	=[moodle]Volume có thể được gắn bởi một Node duy nhất để đọc và ghi.
	~[moodle]Volume có thể được gắn bởi nhiều Node để chỉ đọc.#<p>ReadOnlyMany (ROX) là chế độ truy cập cho phép nhiều Node chỉ đọc.</p>
	~[moodle]Volume chỉ có thể được gắn bởi một Pod duy nhất, không phải Node.#<p>Chế độ truy cập liên quan đến Node, không phải Pod, vì Pod chạy trên một Node.</p>
	####<p><strong>Giải thích</strong>: ReadWriteOnce (RWO) có nghĩa là Volume chỉ có thể được gắn bởi một Node duy nhất để đọc và ghi.</p>
}

// Question 11
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Chính sách thu hồi (reclaim policy) nào cho PersistentVolume đảm bảo rằng Volume và dữ liệu của nó sẽ không bị xóa sau khi PersistentVolumeClaim của nó được giải phóng?</p>{
	=[moodle]Retain.
	~[moodle]Delete.#<p>Delete sẽ xóa PersistentVolume và lưu trữ vật lý cơ bản khi PersistentVolumeClaim được giải phóng.</p>
	~[moodle]Recycle.#<p>Recycle xóa dữ liệu trên Volume và làm cho nó có sẵn cho một PersistentVolumeClaim mới.</p>
	~[moodle]Wipe.#<p>Wipe không phải là một chính sách thu hồi tiêu chuẩn của Kubernetes.</p>
	####<p><strong>Giải thích</strong>: Chính sách thu hồi Retain đảm bảo rằng PersistentVolume và dữ liệu của nó không bị xóa sau khi PersistentVolumeClaim được giải phóng, mà thay vào đó chuyển sang trạng thái Released để quản trị viên xử lý thủ công.</p>
}

// Question 12
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>StorageClass trong Kubernetes được sử dụng với mục đích gì?</p>{
	=[moodle]Định nghĩa loại lưu trữ động (dynamically-provisioned storage) có sẵn trong cluster.
	~[moodle]Chỉ định dung lượng lưu trữ tối thiểu mà một Pod yêu cầu.#<p>Dung lượng lưu trữ tối thiểu được chỉ định trong PersistentVolumeClaim.</p>
	~[moodle]Cấu hình quyền truy cập vào các tệp trên Volume.#<p>Quyền truy cập tệp được quản lý thông qua volumeMounts trong Pod Spec và các quyền hệ thống tệp.</p>
	~[moodle]Là một yêu cầu lưu trữ của Pod cho một PersistentVolume cụ thể.#<p>PersistentVolumeClaim là yêu cầu lưu trữ của Pod.</p>
	####<p><strong>Giải thích</strong>: StorageClass là một tài nguyên cấp cluster được quản trị viên sử dụng để định nghĩa các loại lưu trữ động có sẵn trong cluster và cách chúng được cung cấp (provisioner).</p>
}

// Question 13
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Điều nào sau đây là lợi ích chính của việc sử dụng PersistentVolumes và PersistentVolumeClaims?</p>{
	~[moodle]Nó cho phép các Pods được gắn trực tiếp vào lưu trữ vật lý của Node mà không cần cấu hình.#<p>PV/PVC không gắn trực tiếp vào lưu trữ vật lý của Node, mà trừu tượng hóa nó.</p>
	=[moodle]Nó tách biệt yêu cầu lưu trữ của ứng dụng khỏi công nghệ lưu trữ cơ bản, tăng tính di động và trừu tượng hóa hạ tầng.
	~[moodle]Nó đảm bảo rằng dữ liệu trên Volume sẽ bị xóa hoàn toàn khi Pod bị xóa.#<p>Chính sách thu hồi Retain hoặc Delete quyết định việc xóa dữ liệu; Retain giữ lại dữ liệu.</p>
	~[moodle]Nó chỉ có thể được sử dụng với các Volume tạm thời như emptyDir.#<p>PV/PVC được thiết kế cho lưu trữ bền vững, không phải emptyDir.</p>
	####<p><strong>Giải thích</strong>: Lợi ích chính của việc sử dụng PersistentVolumes và PersistentVolumeClaims là nó tách biệt yêu cầu lưu trữ của ứng dụng khỏi công nghệ lưu trữ cơ bản. Điều này giúp ứng dụng không cần quan tâm đến chi tiết hạ tầng lưu trữ và tăng tính di động.</p>
}

// Question 14
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Khi một PersistentVolumeClaim được tạo và không có PersistentVolume nào được cung cấp thủ công khớp với yêu cầu của nó, làm thế nào để Kubernetes có thể cung cấp lưu trữ động (dynamic provisioning)?</p>{
	~[moodle]Kubernetes sẽ tạo một PersistentVolume trống và đợi quản trị viên gắn lưu trữ vào.#<p>Kubernetes không tạo PV trống mà dựa vào provisioner để tạo cả PV và lưu trữ cơ bản.</p>
	~[moodle]PersistentVolumeClaim sẽ ở trạng thái Pending cho đến khi một PersistentVolume được cung cấp thủ công.#<p>Nếu có StorageClass và provisioner, Kubernetes sẽ cung cấp động, không chờ cung cấp thủ công.</p>
	=[moodle]Kubernetes sẽ sử dụng một StorageClass và một provisioner để tự động tạo một PersistentVolume và lưu trữ cơ bản.
	~[moodle]Kubernetes sẽ tự động gán một Volume emptyDir cho PersistentVolumeClaim.#<p>emptyDir là lưu trữ tạm thời, không phải lưu trữ bền vững cho PVC.</p>
	####<p><strong>Giải thích</strong>: Để thực hiện cung cấp lưu trữ động, quản trị viên cluster triển khai một PersistentVolume provisioner và định nghĩa một hoặc nhiều đối tượng StorageClass. Khi người dùng tạo một PersistentVolumeClaim tham chiếu đến một StorageClass, provisioner sẽ tự động tạo một PersistentVolume và lưu trữ cơ bản.</p>
}

// Question 15
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Điều nào sau đây là ĐÚNG về StorageClass?</p>{
	=[moodle]StorageClass định nghĩa loại lưu trữ động và chỉ ra provisioner nào sẽ được sử dụng để tự động cung cấp PersistentVolume khi có yêu cầu từ PersistentVolumeClaim.
	~[moodle]StorageClass là một tài nguyên có Namespace và chỉ được sử dụng trong Namespace mà nó được tạo ra.#<p>StorageClass là một tài nguyên cấp cluster, không phải tài nguyên có Namespace.</p>
	~[moodle]StorageClass chỉ được sử dụng để ràng buộc PersistentVolumeClaims với các PersistentVolumes đã tồn tại.#<p>StorageClass định nghĩa cách PV được tạo động, không phải cách ràng buộc với PV đã tồn tại.</p>
	~[moodle]StorageClass chỉ được sử dụng khi bạn muốn cung cấp lưu trữ thủ công.#<p>StorageClass được sử dụng cho cung cấp động, trong khi cung cấp thủ công là tạo PV trực tiếp.</p>
	####<p><strong>Giải thích</strong>: StorageClass định nghĩa loại lưu trữ động và chỉ ra provisioner nào sẽ được sử dụng để tự động cung cấp PersistentVolume khi có yêu cầu từ PersistentVolumeClaim.</p>
}

// Question 16
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Nếu một PersistentVolumeClaim được tạo và có nhiều PersistentVolumes có sẵn khớp với yêu cầu của nó, Kubernetes sẽ làm gì?</p>{
	=[moodle]Sẽ ràng buộc PVC với PV đầu tiên trong danh sách các PV có sẵn.
	~[moodle]Sẽ ràng buộc PVC với PV có dung lượng lớn nhất.#<p>Nó ưu tiên PV nhỏ nhất có thể khớp, để tối ưu hóa việc sử dụng tài nguyên.</p>
	~[moodle]Sẽ để PVC ở trạng thái Pending cho đến khi quản trị viên chọn PV.#<p>Nếu có PV khớp, PVC sẽ được ràng buộc ngay lập tức.</p>
	~[moodle]Sẽ tạo một PV mới để đảm bảo khớp chính xác.#<p>Cung cấp động (dynamic provisioning) chỉ xảy ra nếu không có PV nào khớp và có StorageClass được chỉ định.</p>
	####<p><strong>Giải thích</strong>: Scheduler PersistentVolume tìm kiếm một PersistentVolume có sẵn khớp với PersistentVolumeClaim về dung lượng và chế độ truy cập. Nó duy trì một danh sách các PVs được sắp xếp cho mỗi chế độ truy cập theo dung lượng tăng dần và sẽ trả về Volume đầu tiên từ danh sách.</p>
}

// Question 17
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Sau khi một PersistentVolumeClaim được giải phóng (ví dụ: do Pod sử dụng nó bị xóa), nếu chính sách thu hồi của PersistentVolume là Retain, trạng thái của PersistentVolume sẽ là gì?</p>{
	~[moodle]Available.#<p>Available là trạng thái ban đầu của một PV sẵn sàng được yêu cầu.</p>
	~[moodle]Bound.#<p>Bound là trạng thái khi PV đã được ràng buộc với một PVC.</p>
	=[moodle]Released.
	~[moodle]Failed.#<p>Failed là trạng thái nếu có lỗi xảy ra trong quá trình PV.</p>
	####<p><strong>Giải thích</strong>: Khi một PersistentVolumeClaim được giải phóng, nếu chính sách thu hồi của PersistentVolume là Retain, PersistentVolume sẽ chuyển sang trạng thái Released. Nó không thể được yêu cầu lại cho đến khi quản trị viên xử lý thủ công.</p>
}

// Question 18
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Điều nào sau đây là ĐÚNG về việc chia sẻ dữ liệu giữa các container trong cùng một Pod bằng Volume?</p>{
	~[moodle]Chỉ có Volume loại emptyDir mới có thể chia sẻ giữa các container.#<p>Nhiều loại Volume khác cũng có thể chia sẻ dữ liệu (ví dụ: gitRepo, ConfigMap, Secret).</p>
	=[moodle]Bất kỳ loại Volume nào cũng có thể được chia sẻ giữa các container trong cùng một Pod.
	~[moodle]Việc chia sẻ Volume yêu cầu cấu hình securityContext cụ thể trên Pod.#<p>securityContext có thể ảnh hưởng đến quyền truy cập tệp, nhưng không phải là điều kiện tiên quyết để chia sẻ Volume.</p>
	~[moodle]Volume chỉ có thể được chia sẻ nếu nó được cấu hình là read-only.#<p>Volume có thể là đọc-ghi hoặc chỉ đọc, tùy thuộc vào cách nó được mount và loại Volume.</p>
	####<p><strong>Giải thích</strong>: Bất kỳ loại Volume nào cũng có thể được chia sẻ giữa các container trong cùng một Pod, miễn là chúng được gắn vào các container thông qua volumeMounts trong Pod Spec.</p>
}

// Question 19
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Khi sử dụng gcePersistentDisk làm Volume cho Pod, điều gì cần được thực hiện trước khi tạo Pod?</p>{
	~[moodle]Kubernetes sẽ tự động tạo một GCE Persistent Disk mới khi Pod được tạo.#<p>gcePersistentDisk trực tiếp không tự động tạo đĩa; đó là chức năng của dynamic provisioning qua PV/PVC.</p>
	=[moodle]Bạn phải tạo thủ công GCE Persistent Disk trong cùng Availability Zone với cluster của bạn.
	~[moodle]Bạn phải định nghĩa một StorageClass để GCE Persistent Disk có thể được cung cấp động.#<p>StorageClass là cho dynamic provisioning, không phải cho việc tham chiếu trực tiếp Persistent Disk trong Pod.</p>
	~[moodle]Bạn phải đăng ký GCE Persistent Disk với kube-controller-manager thủ công.#<p>Việc đăng ký được thực hiện thông qua PersistentVolume hoặc dynamic provisioning, không phải trực tiếp với kube-controller-manager.</p>
	####<p><strong>Giải thích</strong>: Để sử dụng gcePersistentDisk làm Volume trực tiếp trong Pod (không qua PV/PVC động), bạn phải tạo thủ công GCE Persistent Disk trước đó, đảm bảo nó nằm trong cùng khu vực (zone) với cluster Kubernetes của bạn.</p>
}

// Question 20
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Khi một Pod sử dụng một gcePersistentDisk trực tiếp làm Volume (không qua PersistentVolume), trường nào trong Pod Spec được sử dụng để tham chiếu đến GCE Persistent Disk?</p>{
	=[moodle]gcePersistentDisk.
	~[moodle]volumeName.#<p>volumeName được dùng để tham chiếu một PersistentVolume đã tồn tại.</p>
	~[moodle]claimRef.#<p>claimRef không phải là thuộc tính chuẩn.</p>
	~[moodle]pvcName.#<p>pvcName không phải là thuộc tính chuẩn.</p>
	####<p><strong>Giải thích</strong>: Khi sử dụng gcePersistentDisk trực tiếp trong Pod Spec (không qua PersistentVolume), trường gcePersistentDisk trong phần volumes của Pod Spec được sử dụng để tham chiếu đến GCE Persistent Disk, với các thuộc tính như pdName và fsType.</p>
}

// Question 21
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Nếu bạn muốn một PersistentVolumeClaim (PVC) được ràng buộc với một PersistentVolume (PV) đã được cung cấp thủ công (pre-provisioned) thay vì kích hoạt cung cấp động (dynamic provisioning), bạn nên cấu hình trường storageClassName trong PVC như thế nào?</p>{
	~[moodle]Bỏ qua trường storageClassName.#<p>Bỏ qua trường storageClassName thường sẽ kích hoạt cung cấp động nếu có một StorageClass mặc định.</p>
	~[moodle]Đặt storageClassName thành tên của PV mong muốn.#<p>storageClassName tham chiếu đến một StorageClass, không phải tên của PV.</p>
	=[moodle]Đặt storageClassName thành một chuỗi rỗng ("").
	~[moodle]Đặt storageClassName thành manual.#<p>manual không phải là giá trị đặc biệt cho storageClassName.</p>
	####<p><strong>Giải thích</strong>: Nếu bạn muốn PVC ràng buộc với một PV đã được cung cấp thủ công, bạn phải đặt trường storageClassName thành một chuỗi rỗng ("") trong PVC. Nếu bạn bỏ qua trường này hoặc chỉ định một tên StorageClass, Kubernetes sẽ cố gắng cung cấp động PV.</p>
}

// Question 22
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Điều nào sau đây là ĐÚNG về chính sách thu hồi Delete cho PersistentVolume?</p>{
	~[moodle]Dữ liệu trên Volume sẽ bị xóa nhưng PV sẽ được giữ lại.#<p>Chính sách Delete sẽ xóa cả PV và lưu trữ vật lý cơ bản.</p>
	=[moodle]PV và lưu trữ vật lý cơ bản sẽ bị xóa khi PersistentVolumeClaim được giải phóng.
	~[moodle]Nó tái chế dữ liệu trên Volume để được sử dụng bởi một PersistentVolumeClaim mới.#<p>Đó là hành vi của Recycle.</p>
	~[moodle]Nó chỉ áp dụng cho các Volume tạm thời như emptyDir.#<p>Chính sách thu hồi chỉ áp dụng cho PersistentVolumes.</p>
	####<p><strong>Giải thích</strong>: Chính sách thu hồi Delete sẽ xóa cả PersistentVolume và lưu trữ vật lý cơ bản khi PersistentVolumeClaim được giải phóng.</p>
}

// Question 23
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Khi bạn tạo một ConfigMap hoặc Secret và mount nó như một Volume trong Pod, các entries của ConfigMap/Secret sẽ được lộ ra cho container dưới dạng gì?</p>{
	~[moodle]Các biến môi trường.#<p>ConfigMap và Secret cũng có thể được lộ ra dưới dạng biến môi trường, nhưng đó là một cơ chế khác.</p>
	=[moodle]Các tệp trong thư mục Volume.
	~[moodle]Các đối tượng trong bộ nhớ.#<p>Mặc dù Secret có thể được lưu trữ trong tmpfs (RAM-backed), chúng vẫn được truy cập dưới dạng tệp.</p>
	~[moodle]Các luồng dữ liệu (data streams).#<p>Chúng là các tệp tĩnh được tạo bởi Kubernetes.</p>
	####<p><strong>Giải thích</strong>: Khi ConfigMap hoặc Secret được mount như một Volume, các entries của chúng sẽ được lộ ra cho container dưới dạng các tệp trong thư mục Volume được mount. Mỗi key của ConfigMap/Secret sẽ trở thành một tệp, và value của key đó là nội dung của tệp.</p>
}

// Question 24
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Khi một ConfigMap được sử dụng làm Volume và được cập nhật, điều gì sẽ xảy ra với các tệp trong Volume?</p>{
	~[moodle]Các tệp được ghi trực tiếp vào thư mục và có thể gây ra sự không nhất quán nếu nhiều tệp thay đổi.#<p>Ghi trực tiếp và lock file không đảm bảo tính nguyên tử cho nhiều tệp.</p>
	=[moodle]Các tệp được cập nhật nguyên tử (atomically) thông qua các liên kết tượng trưng (symbolic links).
	~[moodle]Pod cần được khởi động lại để các thay đổi có hiệu lực.#<p>Mặc dù ứng dụng có thể cần tín hiệu để tải lại cấu hình, việc cập nhật tệp không yêu cầu khởi động lại Pod.</p>
	~[moodle]Chỉ Secret Volumes mới có thể được cập nhật tự động, không phải ConfigMap Volumes.#<p>Cơ chế cập nhật tự động này cũng hoạt động với Secret Volumes.</p>
	####<p><strong>Giải thích</strong>: Khi ConfigMap được cập nhật, các tệp trong tất cả các Volume tham chiếu đến nó cũng được cập nhật. Kubernetes thực hiện điều này một cách nguyên tử (atomically) bằng cách sử dụng các liên kết tượng trưng (symbolic links) để đảm bảo tất cả các tệp thay đổi cùng một lúc.</p>
}

// Question 25
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Khi một PersistentVolumeClaim được tạo và không có StorageClass nào được chỉ định (hoặc storageClassName: "" được đặt), Kubernetes sẽ làm gì để ràng buộc nó?</p>{
	~[moodle]Sẽ luôn cung cấp động một PV mới.#<p>Cung cấp động chỉ xảy ra khi có một StorageClass được chỉ định hoặc một StorageClass mặc định được thiết lập.</p>
	=[moodle]Sẽ cố gắng ràng buộc PVC đó với một PersistentVolume đã được cung cấp thủ công (pre-provisioned).
	~[moodle]Sẽ để PVC ở trạng thái Pending mãi mãi.#<p>PVC có thể ở trạng thái Pending nếu không tìm thấy PV khớp hoặc không có cách nào để cung cấp động.</p>
	~[moodle]Sẽ gán một StorageClass mặc định và cung cấp động một PV.#<p>StorageClass mặc định chỉ được gán khi trường storageClassName bị bỏ qua hoàn toàn và có một StorageClass được đánh dấu là mặc định.</p>
	####<p><strong>Giải thích</strong>: Nếu không có StorageClass được chỉ định hoặc storageClassName được đặt thành chuỗi rỗng (""), Kubernetes sẽ cố gắng ràng buộc PVC với một PersistentVolume đã được cung cấp thủ công (pre-provisioned) khớp với yêu cầu của nó.</p>
}

// Question 26
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Chế độ truy cập ReadWriteMany (RWX) cho PersistentVolume có nghĩa là gì?</p>{
	~[moodle]Volume có thể được gắn bởi một Node duy nhất để đọc và ghi.#<p>ReadWriteOnce (RWO) là chế độ truy cập cho phép một Node duy nhất đọc và ghi.</p>
	=[moodle]Volume có thể được gắn bởi nhiều Node để đọc và ghi.
	~[moodle]Volume chỉ có thể được gắn bởi một Pod duy nhất để đọc và ghi.#<p>Chế độ truy cập liên quan đến Node, không phải Pod.</p>
	~[moodle]Volume có thể được gắn bởi nhiều Node để chỉ đọc.#<p>ReadOnlyMany (ROX) là chế độ truy cập cho phép nhiều Node chỉ đọc.</p>
	####<p><strong>Giải thích</strong>: ReadWriteMany (RWX) có nghĩa là Volume có thể được gắn bởi nhiều Node để đọc và ghi, nhưng không phải tất cả các công nghệ lưu trữ cơ bản đều hỗ trợ chế độ này.</p>
}

// Question 27
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Điều nào sau đây là SAI về PersistentVolume và PersistentVolumeClaim?</p>{
	~[moodle]PersistentVolume là tài nguyên cấp cluster, trong khi PersistentVolumeClaim là tài nguyên có Namespace.#<p>Đây là đúng; PV là cấp cluster, PVC là có Namespace.</p>
	~[moodle]PersistentVolume định nghĩa loại lưu trữ và khả năng của nó, trong khi PersistentVolumeClaim là yêu cầu của người dùng.#<p>PV mô tả "phần cứng" lưu trữ, PVC là yêu cầu của "người dùng" về lưu trữ.</p>
	=[moodle]PersistentVolume được tạo tự động bởi StorageClass, trong khi PersistentVolumeClaim được tạo thủ công.
	~[moodle]PersistentVolumeClaim bị xóa sẽ tự động khiến PersistentVolume tương ứng bị xóa nếu chính sách thu hồi là Delete.#<p>Đây là hành vi đúng khi chính sách thu hồi là Delete.</p>
	####<p><strong>Giải thích</strong>: PersistentVolume có thể được tạo thủ công bởi quản trị viên hoặc tự động thông qua dynamic provisioning bởi StorageClass, không phải luôn được tạo tự động bởi StorageClass. PersistentVolumeClaim thường được tạo thủ công bởi người dùng, nhưng câu nói rằng PV luôn được tạo tự động là sai.</p>
}

// Question 28
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Khi bạn muốn lưu trữ dữ liệu bền vững cho một Pod trong GKE, và không muốn lộ chi tiết về loại đĩa (gcePersistentDisk) trong Pod spec, bạn nên làm gì?</p>{
	~[moodle]Sử dụng emptyDir với medium: Memory.#<p>emptyDir là lưu trữ tạm thời, không phải lưu trữ bền vững.</p>
	=[moodle]Tạo một PersistentVolume trỏ đến gcePersistentDisk, sau đó một PersistentVolumeClaim tham chiếu đến PV đó.
	~[moodle]Gắn trực tiếp gcePersistentDisk vào Pod bằng tên của nó.#<p>Gắn trực tiếp gcePersistentDisk lộ chi tiết lưu trữ trong Pod spec, điều bạn muốn tránh.</p>
	~[moodle]Sử dụng hostPath và trỏ đến một thư mục trên Node.#<p>hostPath gắn vào thư mục trên Node, không phải lưu trữ bền vững từ GKE.</p>
	####<p><strong>Giải thích</strong>: Để trừu tượng hóa chi tiết lưu trữ, bạn nên tạo một PersistentVolume (do quản trị viên tạo) trỏ đến gcePersistentDisk, sau đó người dùng tạo một PersistentVolumeClaim để yêu cầu lưu trữ mà không cần chỉ định chi tiết gcePersistentDisk trong Pod spec.</p>
}

// Question 29
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Điều nào sau đây KHÔNG phải là một trạng thái (STATUS) của PersistentVolume?</p>{
	~[moodle]Available.#<p>Available là trạng thái ban đầu của một PV sẵn sàng được yêu cầu.</p>
	~[moodle]Bound.#<p>Bound là trạng thái khi PV đã được ràng buộc với một PVC.</p>
	~[moodle]Released.#<p>Released là trạng thái khi PV được giải phóng khỏi PVC nhưng dữ liệu vẫn còn.</p>
	=[moodle]Detached.
	####<p><strong>Giải thích</strong>: Các trạng thái của PersistentVolume là Available, Bound, Released và Failed. Detached không phải là một trạng thái tiêu chuẩn của PersistentVolume.</p>
}

// Question 30
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Loại Volume nào thích hợp nhất để lưu trữ các tệp cấu hình không nhạy cảm (non-sensitive config files) được cập nhật tự động và có thể chia sẻ giữa các container trong Pod?</p>{
	~[moodle]Secret Volume.#<p>Secret Volume được dùng cho dữ liệu nhạy cảm.</p>
	~[moodle]PersistentVolumeClaim Volume.#<p>PersistentVolumeClaim Volume được dùng cho lưu trữ dữ liệu bền vững.</p>
	=[moodle]ConfigMap Volume.
	~[moodle]emptyDir Volume.#<p>emptyDir Volume là lưu trữ tạm thời, không dùng để lưu cấu hình được cập nhật tự động từ một nguồn khác.</p>
	####<p><strong>Giải thích</strong>: ConfigMap Volume được sử dụng để lộ các entries của ConfigMap dưới dạng các tệp trong Volume, rất phù hợp cho các tệp cấu hình không nhạy cảm và có thể cập nhật tự động khi ConfigMap nguồn thay đổi. Volume này cũng có thể chia sẻ giữa các container trong Pod.</p>
}

// Question 31
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Khi sử dụng ConfigMap Volume, làm thế nào để Kubernetes đảm bảo rằng các tệp được cập nhật một cách nguyên tử (atomically)?</p>{
	~[moodle]Bằng cách ghi trực tiếp vào các tệp và sử dụng lock file để ngăn chặn các thay đổi không nhất quán.#<p>Ghi trực tiếp và lock file không đảm bảo tính nguyên tử cho nhiều tệp.</p>
	=[moodle]Bằng cách sử dụng các liên kết tượng trưng (symbolic links) để thay thế thư mục cũ bằng thư mục mới chứa các tệp đã cập nhật.
	~[moodle]Bằng cách khởi động lại container để áp dụng các thay đổi cấu hình.#<p>Khởi động lại container là nhiệm vụ của ứng dụng để nhận thay đổi, không phải cơ chế cập nhật tệp của Kubernetes.</p>
	~[moodle]Bằng cách sử dụng một giao thức NFS để đồng bộ hóa các tệp giữa các container.#<p>Cơ chế này được Kubernetes thực hiện nội bộ bằng symbolic links, không liên quan đến NFS.</p>
	####<p><strong>Giải thích</strong>: Kubernetes đạt được việc cập nhật các tệp ConfigMap một cách nguyên tử bằng cách sử dụng các liên kết tượng trưng (symbolic links). Nó tạo một thư mục mới với các tệp đã cập nhật, sau đó thay thế liên kết tượng trưng ..data trỏ đến thư mục cũ bằng một liên kết mới trỏ đến thư mục chứa các tệp cập nhật. Điều này đảm bảo rằng tất cả các tệp thay đổi cùng một lúc.</p>
}

// Question 32
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Chính sách thu hồi Delete cho PersistentVolume có nghĩa là gì?</p>{
	~[moodle]Dữ liệu trên Volume sẽ bị xóa nhưng PV sẽ được giữ lại.#<p>Chính sách Delete sẽ xóa cả PV và lưu trữ vật lý cơ bản.</p>
	=[moodle]PV và lưu trữ vật lý cơ bản sẽ bị xóa khi PersistentVolumeClaim được giải phóng.
	~[moodle]Nó tái chế dữ liệu trên Volume để được sử dụng bởi một PersistentVolumeClaim mới.#<p>Đó là hành vi của Recycle.</p>
	~[moodle]Nó chỉ áp dụng cho các Volume tạm thời như emptyDir.#<p>Chính sách thu hồi chỉ áp dụng cho PersistentVolumes.</p>
	####<p><strong>Giải thích</strong>: Chính sách thu hồi Delete sẽ xóa cả PersistentVolume và lưu trữ vật lý cơ bản khi PersistentVolumeClaim được giải phóng.</p>
}

// Question 33
::Chapter 6\: Volumes: Attaching Disk Storage to Containers::[html]<p>Điều nào sau đây là ví dụ của một ConfigMap được lộ ra dưới dạng tệp trong Volume?</p>{
	~[moodle]Passing command-line arguments to containers.#<p>Command-line arguments được truyền qua Pod spec (command/args).</p>
	~[moodle]Setting environment variables for a container.#<p>ConfigMap có thể được dùng để đặt biến môi trường, nhưng đó là một cơ chế khác.</p>
	=[moodle]Using a ConfigMap volume to expose ConfigMap entries as files.
	~[moodle]Accessing pod metadata and other resources from applications.#<p>Accessing pod metadata and other resources thường dùng Downward API.</p>
	####<p><strong>Giải thích</strong>: Một ví dụ của ConfigMap được lộ ra dưới dạng tệp là khi sử dụng ConfigMap Volume để mount các entries của ConfigMap dưới dạng các tệp trong thư mục Volume của Pod.</p>
}