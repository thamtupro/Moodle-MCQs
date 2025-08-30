// Chapter 1: Why Kubernetes exists
// question: 1 name: Switch category to $module$/top/Chapter 1: Why Kubernetes exists
$CATEGORY: $module$/top/Chapter 1: Why Kubernetes exists

// question: 1.1  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Kubernetes được định nghĩa là một nền tảng mã nguồn mở với mục đích chính nào?</p>{
	~[moodle]Để thực hiện ảo hóa toàn hệ thống cho các máy chủ vật lý, tạo ra các máy ảo độc lập và nặng nề.#<p>Kubernetes không thực hiện ảo hóa toàn hệ thống; đó là vai trò của máy ảo và hypervisor. Kubernetes tập trung vào việc quản lý container.</p>
	~[moodle]Để quản lý cơ sở dữ liệu phân tán phức tạp và tối ưu hóa hiệu suất I/O của chúng.#<p>Mặc dù Kubernetes có thể quản lý cơ sở dữ liệu chạy trong container, mục đích chính của nó không phải là quản lý cơ sở dữ liệu phân tán hoặc tối ưu hóa hiệu suất I/O của chúng.</p>
	=[moodle]Để triển khai và điều phối các ứng dụng đóng gói dưới dạng container, định nghĩa API tập trung vào ứng dụng để quản lý tài nguyên đám mây.
	~[moodle]Để biên dịch mã nguồn đa ngôn ngữ thành một định dạng chung, giúp đơn giản hóa quá trình phát triển phần mềm.#<p>Kubernetes không phải là công cụ biên dịch mã nguồn đa ngôn ngữ. Nó tập trung vào việc triển khai và quản lý các ứng dụng đã được biên dịch.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes là một nền tảng mã nguồn mở để lưu trữ container và định nghĩa các API tập trung vào ứng dụng để quản lý ngữ nghĩa đám mây xung quanh cách các container này được cung cấp tài nguyên lưu trữ, mạng, bảo mật và các tài nguyên khác.</p>
}

// question: 1.2  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Vấn đề "Infrastructure drift" (lệch cấu hình hạ tầng) được Kubernetes giải quyết như thế nào?</p>{
	~[moodle]Bằng cách yêu cầu quản trị viên thực hiện các thay đổi thủ công đồng bộ trên tất cả các thành phần.#<p>Kubernetes nhằm mục đích giảm thiểu các thay đổi thủ công, không yêu cầu chúng.</p>
	=[moodle]Bằng cách tự động hóa quá trình quản lý hạ tầng theo cách có thể tái sản xuất, đảm bảo các thành phần được sao chép khi cần thiết.
	~[moodle]Bằng cách sử dụng các công cụ cấu hình cũ như Puppet hoặc Chef để quản lý từng máy chủ riêng lẻ.#<p>Kubernetes mượn ý tưởng từ các công cụ như Puppet và Chef nhưng cung cấp một cách tiếp cận mới để quản lý trạng thái phức tạp, không phải là sử dụng lại chúng một cách trực tiếp.</p>
	~[moodle]Bằng cách chỉ cho phép các ứng dụng chạy trên các máy chủ có cấu hình tĩnh và không thay đổi.#<p>Kubernetes được thiết kế để quản lý các ứng dụng và hạ tầng động, không phải giới hạn vào cấu hình tĩnh.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes cung cấp một cách để quản lý trạng thái toàn bộ của tất cả các ứng dụng một cách tập trung, giúp tự động hóa và đảm bảo tính tái sản xuất của hạ tầng, qua đó giải quyết vấn đề "infrastructure drift".</p>
}

// question: 1.3  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Trong Kubernetes, Pod được mô tả là gì?</p>{
	~[moodle]Một máy ảo đầy đủ với hệ điều hành riêng, chạy một hoặc nhiều container.#<p>Pod không phải là một máy ảo đầy đủ, mà là một trừu tượng hóa để chạy container, nhẹ hơn nhiều so với VM.</p>
	=[moodle]Đơn vị nhỏ nhất, nguyên tử có thể được triển khai tới một cluster Kubernetes, đóng gói một hoặc nhiều container đang chạy.
	~[moodle]Một dịch vụ mạng chịu trách nhiệm định tuyến lưu lượng giữa các node trong cluster.#<p>Dịch vụ mạng (Services) và kube-proxy chịu trách nhiệm định tuyến, không phải bản thân Pod.</p>
	~[moodle]Một công cụ quản lý tài nguyên phần cứng cho các node trong cluster.#<p>Control plane và kubelet quản lý tài nguyên, không phải Pod.</p>
	####<p><strong>Giải thích</strong>\: Pod là đối tượng Kubernetes đóng gói một container đang chạy và là đơn vị nguyên tử nhỏ nhất có thể được triển khai tới một cluster Kubernetes.</p>
}

// question: 1.4  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Mục đích chính của việc sử dụng container (như Docker hoặc OCI images) trong một môi trường Kubernetes là gì?</p>{
	~[moodle]Tách biệt hoàn toàn các ứng dụng khỏi hệ điều hành host bằng cách tạo các máy ảo riêng biệt.#<p>Container sử dụng các tính năng kernel Linux để tạo sự tách biệt nhẹ nhàng, không phải tách biệt hoàn toàn như máy ảo.</p>
	=[moodle]Đóng gói ứng dụng và tất cả các phụ thuộc của nó vào một đơn vị độc lập và có thể di chuyển, tạo ra các máy chủ bất biến.
	~[moodle]Chỉ để chạy các ứng dụng web đơn giản, không yêu cầu tài nguyên phức tạp.#<p>Container có thể chạy nhiều loại ứng dụng khác nhau, không chỉ giới hạn ở ứng dụng web đơn giản.</p>
	~[moodle]Cung cấp một giao diện đồ họa người dùng (GUI) đơn giản để quản lý phần mềm.#<p>Container không cung cấp GUI để quản lý phần mềm.</p>
	####<p><strong>Giải thích</strong>\: Container (hình ảnh Docker hoặc OCI) đóng gói ứng dụng và các phụ thuộc của nó, cho phép chạy các máy chủ bất biến và đơn giản hóa việc triển khai phần mềm.</p>
}

// question: 1.5  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Thành phần nào của Kubernetes chịu trách nhiệm cho các thao tác CRUD (Create, Read, Update, Delete) trên tất cả các đối tượng API và cung cấp giao diện RESTful?</p>{
	~[moodle]Kubelet.#<p>Kubelet là tác nhân chạy trên các node, thực hiện các chỉ thị từ control plane.</p>
	~[moodle]Kube-scheduler.#<p>Kube-scheduler chịu trách nhiệm lập lịch Pod lên các node.</p>
	=[moodle]Kubernetes API server (kube-apiserver).
	~[moodle]Etcd.#<p>Etcd là nơi lưu trữ dữ liệu nhất quán cho trạng thái của cluster, nhưng API server là giao diện để tương tác với dữ liệu đó.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes API server (kube-apiserver) là một máy chủ REST dựa trên HTTP, phơi bày các đối tượng API khác nhau cho một cluster Kubernetes; các đối tượng này bao gồm từ Pod đến node đến Horizontal Pod Autoscaler. API server xác thực và cung cấp giao diện web để thực hiện các dịch vụ CRUD trên trạng thái chia sẻ của cluster.</p>
}

// question: 1.6  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Theo nguồn, đâu là một trong những tính năng cốt lõi mà Kubernetes cung cấp?</p>{
	~[moodle]Tích hợp chặt chẽ với các hypervisor phổ biến để tạo máy ảo.#<p>Kubernetes tích hợp với các nền tảng đám mây và hypervisor lớn, nhưng không phải là tính năng cốt lõi để tạo máy ảo. Nó tập trung vào container.</p>
	=[moodle]Cung cấp một nền tảng chịu lỗi để lưu trữ và định nghĩa trạng thái của tất cả các Services, ứng dụng và cấu hình trung tâm dữ liệu.
	~[moodle]Giảm thiểu yêu cầu về tài nguyên CPU và bộ nhớ cho các ứng dụng chạy trong container.#<p>Mặc dù Kubernetes cho phép quản lý tài nguyên hiệu quả, mục đích chính của nó không phải là giảm thiểu CPU và bộ nhớ cho ứng dụng.</p>
	~[moodle]Tự động biên dịch mã nguồn ứng dụng mỗi khi có thay đổi.#<p>Kubernetes quản lý triển khai các ứng dụng đã được đóng gói, không phải tự động biên dịch mã nguồn.</p>
	####<p><strong>Giải thích</strong>\: Một trong những tính năng cốt lõi của Kubernetes là cung cấp một khuôn khổ chịu lỗi để lưu trữ và định nghĩa trạng thái của tất cả các Services, ứng dụng và cấu hình trung tâm dữ liệu hoặc các hạ tầng được Kubernetes hỗ trợ khác.</p>
}

// question: 1.7  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Các đối tượng API trong Kubernetes, như Pods hoặc Deployments, được định nghĩa chủ yếu bằng định dạng nào?</p>{
	~[moodle]Các tệp nhị phân đã biên dịch.#<p>Các tệp nhị phân không phải là cách định nghĩa các đối tượng API trong Kubernetes.</p>
	~[moodle]Các tập lệnh shell phức tạp.#<p>Các tập lệnh shell có thể được sử dụng để tương tác với Kubernetes, nhưng không phải để định nghĩa các đối tượng API.</p>
	=[moodle]Các tệp văn bản thuần túy được định nghĩa thông qua YAML hoặc JSON.
	~[moodle]Các cơ sở dữ liệu quan hệ chuyên dụng.#<p>Etcd là một key/value store được sử dụng để lưu trữ trạng thái, nhưng không phải là nơi định nghĩa trực tiếp các đối tượng API.</p>
	####<p><strong>Giải thích</strong>\: Tại cốt lõi, chúng ta định nghĩa mọi thứ trong Kubernetes là các tệp văn bản thuần túy, được định nghĩa thông qua YAML hoặc JSON.</p>
}

// question: 1.8  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Thành phần nào của Kubernetes được gọi là "bộ não" của cluster, nơi diễn ra việc lập lịch container và quản lý tất cả các đối tượng Kubernetes?</p>{
	~[moodle]Kubelet.#<p>Kubelet là tác nhân trên các node.</p>
	~[moodle]Worker Nodes.#<p>Worker Nodes là đơn vị tính toán cơ bản, nơi các Pod chạy.</p>
	=[moodle]Control Plane.
	~[moodle]Container Runtime.#<p>Container Runtime là phần mềm thực thi container trên một node.</p>
	####<p><strong>Giải thích</strong>\: Control plane là bộ não của một cluster Kubernetes, nơi diễn ra việc lập lịch container và quản lý tất cả các đối tượng Kubernetes (đôi khi được gọi là Masters).</p>
}

// question: 1.9  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Công cụ dòng lệnh (CLI) được sử dụng để giao tiếp với Kubernetes control plane là gì?</p>{
	~[moodle]Docker Compose.#<p>Docker Compose là công cụ để quản lý nhiều container trên một máy đơn.</p>
	=[moodle]kubectl.
	~[moodle]Helm.#<p>Helm là công cụ quản lý package cho Kubernetes.</p>
	~[moodle]Ansible.#<p>Ansible là công cụ quản lý cấu hình.</p>
	####<p><strong>Giải thích</strong>\: kubectl là công cụ dòng lệnh để giao tiếp với Kubernetes control plane.</p>
}

// question: 1.10  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Khi nào thì không nên sử dụng Kubernetes theo khuyến nghị của nguồn?</p>{
	~[moodle]Khi cần triển khai hàng trăm hoặc hàng nghìn container trong môi trường sản xuất.#<p>Đây là một trong những trường hợp sử dụng chính của Kubernetes.</p>
	=[moodle]Đối với các ứng dụng tính toán hiệu năng cao (HPC) yêu cầu độ trễ cực thấp.
	~[moodle]Để xây dựng các ứng dụng microservice mới hoàn toàn từ đầu.#<p>Kubernetes rất phù hợp cho việc triển khai microservices.</p>
	~[moodle]Để tự động hóa quy trình DevOps và duy trì tính nhất quán của môi trường.#<p>Đây là một lợi ích cốt lõi của việc sử dụng Kubernetes.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes có thể không phù hợp cho các trường hợp sử dụng tính toán hiệu năng cao (HPC) vì việc sử dụng container có thể thêm một lớp phức tạp và ảnh hưởng đến hiệu suất, đặc biệt nếu ứng dụng bị ảnh hưởng bởi độ trễ nano hoặc micro giây.</p>
}

// question: 1.11  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Khái niệm "Namespace" trong Kubernetes được sử dụng để làm gì?</p>{
	~[moodle]Để tạo một mạng vật lý riêng biệt cho các Pod.#<p>Namespaces không tạo mạng vật lý, mà là nhóm logic.</p>
	~[moodle]Để cho phép các Pod truy cập trực tiếp vào tài nguyên hệ thống của host.#<p>Host network cho phép truy cập tài nguyên host, không phải Namespace.</p>
	=[moodle]Để cung cấp một hình thức nhóm phân cấp đơn giản cho các đối tượng Kubernetes, chẳng hạn như Pods và Services.
	~[moodle]Để định nghĩa các giới hạn tài nguyên CPU và bộ nhớ cho các container.#<p>Giới hạn tài nguyên được định nghĩa trong spec của Pod thông qua cgroups.</p>
	####<p><strong>Giải thích</strong>\: Trong Kubernetes, Namespaces cho phép một số đối tượng tồn tại bên trong một Namespace cụ thể, cung cấp cho các nhà phát triển một hình thức nhóm phân cấp đơn giản.</p>
}

// question: 1.12  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Đâu là đơn vị tính toán cơ bản trong một cluster Kubernetes, chịu trách nhiệm chạy quá trình kubelet?</p>{
	~[moodle]Pod.#<p>Pod là đơn vị triển khai nhỏ nhất, chạy trên một Node.</p>
	~[moodle]Control Plane.#<p>Control Plane là "bộ não" của cluster, không phải đơn vị tính toán.</p>
	=[moodle]Node.
	~[moodle]Container.#<p>Container chạy bên trong Pod, không phải đơn vị tính toán cơ bản của cluster.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes worker nodes là đơn vị tính toán cơ bản trong một cluster Kubernetes. Node là một máy chạy quá trình kubelet.</p>
}

// question: 1.13  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Theo nguồn, Kubernetes mượn khả năng quản lý trạng thái từ công cụ nào?</p>{
	~[moodle]Chef.#<p>Chef là một công cụ quản lý cấu hình khác.</p>
	~[moodle]Ansible.#<p>Ansible là một công cụ quản lý cấu hình khác.</p>
	=[moodle]Puppet.
	~[moodle]Mesos.#<p>Mesos cung cấp các nguyên thủy ứng dụng và lập lịch.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes mượn các khả năng quản lý trạng thái từ các công cụ như Puppet.</p>
}

// question: 1.14  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Thành phần nào trong kiến trúc Kubernetes chịu trách nhiệm tự động hóa việc mở rộng (scaling) các host và ứng dụng được lưu trữ với nhận thức về cập nhật cuốn chiếu (rolling update awareness)?</p>{
	~[moodle]Kubelet.#<p>Kubelet quản lý Pod trên một node, không trực tiếp quản lý scaling toàn cục.</p>
	~[moodle]Kube-proxy.#<p>Kube-proxy lo về mạng dịch vụ.</p>
	=[moodle]Kubernetes control plane thông qua các tính năng của nó.
	~[moodle]Etcd.#<p>Etcd lưu trữ trạng thái, không trực tiếp thực hiện scaling.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes tự động hóa việc mở rộng cho các host và các ứng dụng được lưu trữ với nhận thức về cập nhật cuốn chiếu. Đây là một tính năng tổng thể của Kubernetes, được điều phối bởi control plane.</p>
}

// question: 1.15  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Điều gì không phải là một trong những tính năng của Kubernetes được liệt kê trong nguồn?</p>{
	~[moodle]Tích hợp với tất cả các nền tảng đám mây và hypervisor chính.#<p>Đây là một tính năng được liệt kê trong nguồn.</p>
	~[moodle]Cung cấp API trung lập với đám mây cho tất cả chức năng.#<p>Đây là một tính năng được liệt kê trong nguồn.</p>
	=[moodle]Cung cấp khả năng truy cập trực tiếp và đầy đủ vào phần cứng máy chủ.
	~[moodle]Tự động hóa việc mở rộng (scaling) và quản lý triển khai với thời gian ngừng hoạt động tối thiểu.#<p>Đây là một tính năng được liệt kê trong nguồn.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes không cung cấp khả năng truy cập trực tiếp và đầy đủ vào phần cứng máy chủ; nó trừu tượng hóa tài nguyên. Đây không phải là một tính năng được liệt kê.</p>
}

// question: 1.16  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>DaemonSet trong Kubernetes có vai trò gì?</p>{
	~[moodle]Chạy một bản sao (replica) của Pod trên một node cụ thể.#<p>Một bản sao trên một node cụ thể có thể là một Pod đơn lẻ hoặc một phần của Deployment.</p>
	=[moodle]Đảm bảo một bản sao của Pod chạy trên MỌI node trong một cluster.
	~[moodle]Quản lý việc mở rộng và cập nhật các ứng dụng không trạng thái.#<p>Deployment quản lý scaling và cập nhật ứng dụng không trạng thái.</p>
	~[moodle]Cung cấp bộ nhớ tạm thời cho các Pod.#<p>emptyDir cung cấp bộ nhớ tạm thời.</p>
	####<p><strong>Giải thích</strong>\: DaemonSet giống như một deployment, nhưng nó chạy trên mọi node của một cluster.</p>
}

// question: 1.17  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Khái niệm "OCI" trong bối cảnh Kubernetes và container đề cập đến điều gì?</p>{
	~[moodle]Một giao diện mạng container cho phép kết nối giữa các Pod.#<p>CNI là giao diện mạng container.</p>
	=[moodle]Định dạng hình ảnh phổ biến để xây dựng các ứng dụng độc lập, có thể thực thi.
	~[moodle]Một giao diện lưu trữ container để quản lý các volume.#<p>CSI là giao diện lưu trữ container.</p>
	~[moodle]Tên của một công cụ dòng lệnh được sử dụng để quản lý Kubernetes.#<p>kubectl là công cụ dòng lệnh chính.</p>
	####<p><strong>Giải thích</strong>\: OCI là định dạng hình ảnh phổ biến để xây dựng các ứng dụng độc lập, có thể thực thi. Cũng được gọi là hình ảnh Docker.</p>
}

// question: 1.18  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Tại sao việc chạy Kubernetes trên các hệ điều hành bất biến (immutable operating systems) lại tự nhiên?</p>{
	~[moodle]Vì các hệ điều hành bất biến cho phép cài đặt thủ công các bản vá bảo mật thường xuyên hơn.#<p>Hệ điều hành bất biến giảm thiểu cài đặt thủ công.</p>
	=[moodle]Vì chúng chỉ cập nhật khi toàn bộ hệ điều hành được cập nhật, giúp duy trì tính nhất quán và tránh "drift".
	~[moodle]Vì chúng cung cấp quyền truy cập trực tiếp vào các tài nguyên phần cứng, tối ưu hóa hiệu suất.#<p>Hệ điều hành bất biến không thay đổi cách Kubernetes truy cập phần cứng.</p>
	~[moodle]Vì chúng loại bỏ hoàn toàn nhu cầu về container và hình ảnh OCI.#<p>Kubernetes vẫn chạy container và hình ảnh OCI trên các hệ điều hành này.</p>
	####<p><strong>Giải thích</strong>\: Việc chạy Kubernetes trên các hệ điều hành bất biến là tự nhiên vì chúng chỉ cập nhật khi toàn bộ hệ điều hành được cập nhật, giúp duy trì tính nhất quán và tránh "drift", nơi một số máy hoạt động hơi khác nhau vì các bản vá bị bỏ lỡ hoặc áp dụng không đúng cách.</p>
}

// question: 1.19  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Hai khái niệm CNI và CSI trong Kubernetes đại diện cho điều gì?</p>{
	~[moodle]CNI là Container Network Interface, còn CSI là Container System Interface.#<p>CSI không phải là Container System Interface.</p>
	~[moodle]CNI là Container Native Integration, còn CSI là Container Security Interface.#<p>Các lựa chọn này không chính xác.</p>
	=[moodle]CNI là Container Network Interface, còn CSI là Container Storage Interface.
	~[moodle]CNI là Cloud Native Infrastructure, còn CSI là Cloud Security Integration.#<p>Các lựa chọn này không chính xác.</p>
	####<p><strong>Giải thích</strong>\: CNI và CSI là Container Networking và Storage Interfaces, tương ứng, cho phép mạng và lưu trữ có thể cắm được cho Pods (container) chạy trong Kubernetes.</p>
}

// question: 1.20  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Nếu bạn có một ứng dụng chạy 10 microservice khác nhau, giải pháp phổ biến và trực quan nhất để tách biệt tất cả các đối tượng API Kubernetes liên quan đến ứng dụng đó là gì?</p>{
	~[moodle]Tạo một PersistentVolumeClaim (PVC) riêng cho mỗi microservice.#<p>PVCs chỉ giải quyết vấn đề lưu trữ, không phải nhóm logic toàn bộ ứng dụng.</p>
	~[moodle]Gán nhãn duy nhất cho mỗi Pod và Service liên quan.#<p>Nhãn giúp tổ chức nhưng không cung cấp ranh giới tách biệt mạnh mẽ như Namespace.</p>
	=[moodle]Tạo một Namespace riêng biệt cho tất cả các Pods, Services và PVCs của ứng dụng.
	~[moodle]Sử dụng một công cụ quản lý cấu hình bên ngoài để theo dõi từng đối tượng.#<p>Đây là một cách quản lý nhưng không phải giải pháp tích hợp sẵn trong Kubernetes để tách biệt logic.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn có một ứng dụng chạy 10 microservice khác nhau, bạn thường tạo tất cả các Pods, Services và PersistentVolumeClaims (còn gọi là PVCs) này trong cùng một Namespace. Bằng cách đó, khi đến lúc bạn muốn xóa ứng dụng, bạn chỉ cần xóa Namespace.</p>
}

// question: 1.21  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Theo nguồn, việc quản lý hạ tầng một cách có thể tái sản xuất (reproducible way) là gì?</p>{
	~[moodle]Chỉ đơn giản là việc sao chép các tệp cấu hình bằng tay.#<p>Sao chép thủ công không phải là cách có thể tái sản xuất hiệu quả.</p>
	=[moodle]Cách quản lý "drift" (lệch cấu hình) của hạ tầng khi các yêu cầu về phần cứng, tuân thủ thay đổi.
	~[moodle]Việc tự động cài đặt hệ điều hành trên mọi máy chủ mới.#<p>Đây có thể là một phần của quản lý hạ tầng nhưng không phải định nghĩa đầy đủ về tính tái sản xuất.</p>
	~[moodle]Việc loại bỏ hoàn toàn nhu cầu về bất kỳ cấu hình nào.#<p>Không thể loại bỏ hoàn toàn cấu hình; mục tiêu là quản lý nó một cách hiệu quả.</p>
	####<p><strong>Giải thích</strong>\: Quản lý hạ tầng là một cách có thể tái sản xuất để quản lý "drift" của cấu hình hạ tầng đó khi các yêu cầu về phần cứng, tuân thủ và các yêu cầu trung tâm dữ liệu khác thay đổi theo thời gian.</p>
}

// question: 1.22  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Khi đề cập đến "API objects" trong Kubernetes, điều gì là KHÔNG phải là một trong các thuộc tính chính của chúng?</p>{
	~[moodle]Một phiên bản API được đặt tên (ví dụ: v1).#<p>Đây là một thuộc tính chính của đối tượng API.</p>
	~[moodle]Một loại (kind) đối tượng (ví dụ: Deployment).#<p>Đây là một thuộc tính chính của đối tượng API.</p>
	~[moodle]Một phần metadata.#<p>Đây là một thuộc tính chính của đối tượng API.</p>
	=[moodle]Một giao diện đồ họa người dùng tích hợp.
	####<p><strong>Giải thích</strong>\: Các đối tượng API Kubernetes có phiên bản API được đặt tên, loại và phần metadata. Chúng không có giao diện đồ họa người dùng tích hợp; giao diện này thường được cung cấp bởi các công cụ bên thứ ba hoặc CLI.</p>
}

// question: 1.23  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Kubernetes tích hợp với các nền tảng đám mây và hypervisor chính thông qua thành phần nào?</p>{
	~[moodle]Kubelet.#<p>Kubelet chạy trên các node.</p>
	=[moodle]Kubernetes controller manager (KCM).
	~[moodle]Etcd.#<p>Etcd là nơi lưu trữ trạng thái.</p>
	~[moodle]Kube-proxy.#<p>Kube-proxy lo về mạng dịch vụ.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes tích hợp với tất cả các nền tảng đám mây và hypervisor chính trong Kubernetes controller manager (còn được gọi là KCM).</p>
}

// question: 1.24  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Một trong những lợi ích quan trọng nhất của việc chuyển sang Kubernetes là gì, đặc biệt trong các trường hợp thất bại nghiêm trọng?</p>{
	~[moodle]Thời gian phục hồi trở nên không thể đoán trước và phức tạp hơn để quản lý.#<p>Ngược lại, thời gian phục hồi trở nên dễ đoán hơn.</p>
	~[moodle]Loại bỏ hoàn toàn nhu cầu về bất kỳ sự can thiệp thủ công nào.#<p>Kubernetes giảm thiểu sự can thiệp thủ công nhưng không loại bỏ hoàn toàn.</p>
	=[moodle]Thời gian phục hồi trong các trường hợp thất bại nghiêm trọng trở nên dễ đoán hơn để quản lý.
	~[moodle]Tăng cường sự phụ thuộc vào các công cụ quản lý cấu hình legacy.#<p>Kubernetes giảm sự phụ thuộc vào các công cụ legacy.</p>
	####<p><strong>Giải thích</strong>\: Việc chuyển đổi sang Kubernetes cho công ty này đã giải quyết toàn bộ các vấn đề quản lý máy ảo, gánh nặng DNS cho việc xuất bản dịch vụ phức tạp và nhiều hơn nữa. Ngoài ra, thời gian phục hồi trong các trường hợp thất bại nghiêm trọng trở nên dễ đoán hơn để quản lý từ góc độ hạ tầng.</p>
}

// question: 1.25  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Điều nào sau đây là KHÔNG phải là một thành phần chính của kiến trúc Kubernetes ở cấp độ cao?</p>{
	~[moodle]Hạ tầng phần cứng.#<p>Đây là một thành phần chính được liệt kê.</p>
	~[moodle]Các worker node của Kubernetes.#<p>Đây là một thành phần chính được liệt kê.</p>
	~[moodle]Control plane của Kubernetes.#<p>Đây là một thành phần chính được liệt kê.</p>
	=[moodle]Một cơ sở dữ liệu SQL truyền thống để lưu trữ trạng thái ứng dụng.
	####<p><strong>Giải thích</strong>\: Kiến trúc Kubernetes ở cấp độ cao bao gồm hạ tầng phần cứng, các worker node và control plane. Kubernetes sử dụng etcd, một key/value store, để lưu trữ trạng thái, không phải cơ sở dữ liệu SQL truyền thống.</p>
}

// question: 1.26  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Mục đích của "node labeling" trong Kubernetes là gì?</p>{
	~[moodle]Để gán tên duy nhất cho mỗi node.#<p>Node có tên riêng, nhãn là để thêm metadata.</p>
	~[moodle]Để xác định các giới hạn tài nguyên vật lý của một node.#<p>Giới hạn tài nguyên được quản lý bởi cgroups và kubelet, không phải nhãn node.</p>
	=[moodle]Để cho phép lập lịch ứng dụng chạy trên phần cứng ảo hóa cụ thể, dựa trên metadata của nó.
	~[moodle]Để tự động cấu hình địa chỉ IP cho các Pod trên một node.#<p>CNI provider cấu hình IP cho Pod.</p>
	####<p><strong>Giải thích</strong>\: Node labeling cho phép lập lịch ứng dụng chạy trên phần cứng ảo hóa cụ thể, dựa trên metadata của nó, thông qua bộ lập lịch Kubernetes.</p>
}

// question: 1.27  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Công cụ nào được sử dụng bởi các container có đặc quyền (privileged containers) trên môi trường Linux để quản lý các quy tắc iptables cho việc định tuyến lưu lượng đến các ứng dụng?</p>{
	~[moodle]Docker Compose.#<p>Docker Compose dùng để quản lý multi-container trên một máy.</p>
	=[moodle]Kube-proxy.
	~[moodle]Helm.#<p>Helm là công cụ quản lý package.</p>
	~[moodle]Terraform.#<p>Terraform là công cụ hạ tầng dưới dạng mã.</p>
	####<p><strong>Giải thích</strong>\: Ví dụ, một container có đặc quyền trong hệ thống Linux có thể quản lý các quy tắc iptables để định tuyến lưu lượng đến các ứng dụng, và thực tế, đây chính xác là những gì proxy dịch vụ Kubernetes (được gọi là kube-proxy) thực hiện.</p>
}

// question: 1.28  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Trong một luồng làm việc Kubernetes được đơn giản hóa, hình ảnh Dockerfile dùng để làm gì?</p>{
	~[moodle]Để chạy các lệnh shell trực tiếp trên máy chủ vật lý.#<p>Dockerfile là file cấu hình, không trực tiếp chạy lệnh shell trên host.</p>
	=[moodle]Để xây dựng một hình ảnh (image) có khả năng chạy MySQL hoặc một ứng dụng khác.
	~[moodle]Để định nghĩa các quy tắc bảo mật cho toàn bộ cluster.#<p>Quy tắc bảo mật được định nghĩa bằng YAML/JSON, không phải Dockerfile.</p>
	~[moodle]Để quản lý các volume lưu trữ dữ liệu liên tục.#<p>Dockerfile không trực tiếp quản lý volume lưu trữ.</p>
	####<p><strong>Giải thích</strong>\: Để bắt đầu với một ví dụ cụ thể về microservice, đoạn mã sau tạo ra một Dockerfile để xây dựng một hình ảnh có khả năng chạy MySQL.</p>
}

// question: 1.29  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Điều gì làm cho việc quản lý các bản ghi DNS trở nên khó khăn ở quy mô lớn trong môi trường microservice mà không có Kubernetes?</p>{
	~[moodle]Số lượng máy chủ vật lý cố định.#<p>Số lượng máy chủ vật lý không phải là nguyên nhân chính.</p>
	=[moodle]Sự bùng nổ trong việc sử dụng tên miền trên một trung tâm dữ liệu nội bộ do microservice.
	~[moodle]Việc thiếu các giao thức mạng tiêu chuẩn.#<p>Giao thức mạng tiêu chuẩn tồn tại.</p>
	~[moodle]Sự cần thiết của cấu hình DNS thủ công cho mỗi ứng dụng.#<p>Kubernetes giải quyết việc này bằng cách tự động hóa.</p>
	####<p><strong>Giải thích</strong>\: Microservices làm cho việc quản lý các bản ghi DNS ở quy mô lớn trở nên khó khăn vì chúng yêu cầu sự bùng nổ trong việc sử dụng tên miền trên một trung tâm dữ liệu nội bộ.</p>
}

// question: 1.30  name: Chapter 1: Why Kubernetes exists
::Chapter 1\: Why Kubernetes exists::[html]<p>Mục đích của việc sử dụng etcd trong control plane của Kubernetes là gì?</p>{
	~[moodle]Để cung cấp giao diện người dùng cho các nhà phát triển.#<p>API server cung cấp giao diện API, không phải etcd.</p>
	=[moodle]Để lưu trữ trạng thái mong muốn của toàn bộ cluster một cách nhất quán mạnh mẽ (strictly consistent).
	~[moodle]Để chạy các container ứng dụng trên các worker node.#<p>Kubelet và container runtime chạy container trên worker node.</p>
	~[moodle]Để định tuyến lưu lượng mạng giữa các Pod.#<p>Kube-proxy và CNI provider định tuyến lưu lượng mạng.</p>
	####<p><strong>Giải thích</strong>\: Etcd là một key/value store với các đảm bảo nhất quán mạnh mẽ. Kubernetes đã áp dụng etcd làm backend cho API server, cung cấp một key/value store nhất quán mạnh mẽ nơi Kubernetes có thể lưu trữ tất cả các trạng thái mong muốn của cluster.</p>
}

// Chapter 2: Why the Pod?
// question: 2 name: Switch category to $module$/top/Chapter 2: Why the Pod?
$CATEGORY: $module$/top/Chapter 2: Why the Pod?

// question: 2.1  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Điều gì mô tả chính xác nhất một Pod trong Kubernetes?</p>{
	~[moodle]Một máy chủ vật lý có thể chạy nhiều ứng dụng ảo hóa độc lập.#<p>Pod không phải là một máy chủ vật lý; nó là một trừu tượng hóa trên một node.</p>
	=[moodle]Một đối tượng API Kubernetes có thể chứa một hoặc nhiều container chia sẻ cùng tài nguyên mạng và lưu trữ.
	~[moodle]Một dịch vụ mạng chịu trách nhiệm cân bằng tải lưu lượng giữa các node.#<p>Service là đối tượng API để cân bằng tải, không phải Pod.</p>
	~[moodle]Một kho lưu trữ hình ảnh Docker toàn cầu cho các ứng dụng.#<p>Container Registry lưu trữ hình ảnh Docker.</p>
	####<p><strong>Giải thích</strong>\: Pod là một đối tượng được định nghĩa trong Kubernetes API. Pod (hình 2.1) cho phép chúng ta định nghĩa một đối tượng có thể bao gồm nhiều container, điều này cho phép Kubernetes tạo ra một hoặc nhiều container được lưu trữ trên một node. Một Pod là một hoặc nhiều hình ảnh OCI chạy dưới dạng container trên một node cluster Kubernetes.</p>
}

// question: 2.2  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Một Pod được tạo thành từ tập hợp các tính năng kernel Linux nào?</p>{
	~[moodle]Swap space và temporary file systems.#<p>Đây là các khái niệm liên quan đến kernel Linux nhưng không phải là hai tính năng cốt lõi được Pod sử dụng để tạo ảo hóa nhẹ.</p>
	~[moodle]Kernel modules và system calls.#<p>Đây là các khái niệm liên quan đến kernel Linux nhưng không phải là hai tính năng cốt lõi được Pod sử dụng để tạo ảo hóa nhẹ.</p>
	=[moodle]Control groups (cgroups) và namespaces.
	~[moodle]Interrupt handlers và device drivers.#<p>Đây là các khái niệm liên quan đến kernel Linux nhưng không phải là hai tính năng cốt lõi được Pod sử dụng để tạo ảo hóa nhẹ.</p>
	####<p><strong>Giải thích</strong>\: Pods, ở cấp độ cơ bản, là một tập hợp các namespaces Linux trong một cấu hình cụ thể. Các namespaces Linux là các thành phần kernel Linux cung cấp chức năng cơ bản để lấy một hình ảnh và tạo một container đang chạy. Các container kết hợp cgroups và namespaces – hai tính năng kernel Linux – để tạo ra các thể hiện hệ điều hành ảo nhẹ.</p>
}

// question: 2.3  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Vai trò chính của kubelet trong một cluster Kubernetes là gì?</p>{
	~[moodle]Đóng vai trò là bộ lập lịch chính, quyết định Pod nào chạy trên node nào.#<p>Bộ lập lịch (kube-scheduler) là bộ lập lịch chính.</p>
	=[moodle]Giao tiếp với API server để thực hiện các yêu cầu của control plane trên node và quản lý vòng đời của Pod.
	~[moodle]Cung cấp giao diện người dùng đồ họa để quản lý các ứng dụng.#<p>Kubelet không cung cấp GUI.</p>
	~[moodle]Tạo và quản lý các dịch vụ mạng bên ngoài cho các ứng dụng.#<p>Kube-proxy xử lý các dịch vụ mạng.</p>
	####<p><strong>Giải thích</strong>\: Kubelet là tác nhân Kubernetes chạy trên các node của bạn. Nó làm những gì control plane cần nó làm. Kubelet sử dụng CRI và CNI để điều hòa trạng thái của một node với trạng thái của control plane.</p>
}

// question: 2.4  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Thành phần nào của Kubernetes chịu trách nhiệm tạo ra các dịch vụ mạng ClusterIP và NodePort trên mỗi node?</p>{
	~[moodle]Kubelet.#<p>Kubelet quản lý vòng đời của Pod.</p>
	=[moodle]Kubernetes network proxy (kube-proxy).
	~[moodle]Kubernetes API server (kube-apiserver).#<p>API server là giao diện trung tâm cho các hoạt động CRUD.</p>
	~[moodle]CNI provider.#<p>CNI provider cung cấp địa chỉ IP cho Pods.</p>
	####<p><strong>Giải thích</strong>\: Binary proxy mạng Kubernetes (kube-proxy) xử lý việc tạo các dịch vụ ClusterIP và NodePort trên mỗi node.</p>
}

// question: 2.5  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Điều gì xảy ra với thông tin ứng dụng khi một node trong control plane bị gián đoạn, nhưng control plane vẫn còn hoạt động?</p>{
	~[moodle]Thông tin ứng dụng bị mất hoàn toàn và không thể phục hồi.#<p>Thông tin ứng dụng không bị mất nếu node đi xuống nhưng control plane vẫn hoạt động.</p>
	=[moodle]Không có gì mới có thể được triển khai, nhưng trang web hoặc ứng dụng vẫn hoạt động.
	~[moodle]Tất cả các Pod trên cluster đều bị dừng ngay lập tức.#<p>Các Pod hiện có tiếp tục chạy.</p>
	~[moodle]Dữ liệu đính kèm vào các ứng dụng tự động di chuyển sang node khác.#<p>Dữ liệu di chuyển khi control plane hoạt động lại và có thể lập lịch Pod mới.</p>
	####<p><strong>Giải thích</strong>\: Ngay cả khi control plane bị gián đoạn, Zeus Zap sẽ không mất bất kỳ thông tin ứng dụng nào nếu một node gặp sự cố. Trong trường hợp control plane bị gián đoạn, không có gì mới có thể được triển khai, nhưng trang web vẫn hoạt động.</p>
}

// question: 2.6  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Đâu là một trong những loại namespace Linux được Pod sử dụng?</p>{
	~[moodle]Filesystem namespace.#<p>Đây không phải là tên namespace Linux chính thức được liệt kê trong nguồn cho Pod. mnt là cho filesystem.</p>
	~[moodle]Processor namespace.#<p>Đây không phải là tên namespace Linux chính thức được liệt kê trong nguồn cho Pod.</p>
	=[moodle]Inter-Process Communication (IPC) namespace.
	~[moodle]Memory namespace.#<p>Đây không phải là tên namespace Linux chính thức được liệt kê trong nguồn cho Pod. cgroup là cho tài nguyên.</p>
	####<p><strong>Giải thích</strong>\: Một Pod có các namespace Linux sau: Một hoặc nhiều namespace PID, một namespace mạng duy nhất, namespace IPC, namespace cgroup (nhóm kiểm soát), namespace mnt (mount), namespace user (ID người dùng).</p>
}

// question: 2.7  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Để một kubelet thực hiện công việc thực sự của mình (ví dụ: chạy container), nó cần những thành phần nào?</p>{
	~[moodle]Chỉ cần một hệ điều hành đã cài đặt và systemd.#<p>Hệ điều hành và systemd là các thành phần của node, nhưng không đủ cho kubelet chạy container.</p>
	=[moodle]Cả một CNI provider và một container runtime có thể truy cập qua CRI.
	~[moodle]Chỉ cần kube-proxy và kubectl.#<p>kubectl là công cụ dòng lệnh, không phải thành phần node.</p>
	~[moodle]Chỉ cần kết nối với Kubernetes API server.#<p>Kubelet kết nối với API server, nhưng vẫn cần CNI/CRI để thực thi.</p>
	####<p><strong>Giải thích</strong>\: Tuy nhiên, kubelet không thể làm bất kỳ công việc thực sự nào nếu không có cả CNI provider và container runtime có thể truy cập qua Container Runtime Interface (CRI).</p>
}

// question: 2.8  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Thành phần nào trong control plane của Kubernetes chịu trách nhiệm cho việc lập lịch phân tán, xem xét các yếu tố như tài nguyên CPU và bộ nhớ có sẵn trên một node?</p>{
	~[moodle]Kube-apiserver.#<p>API server là giao diện cho các đối tượng API.</p>
	=[moodle]Kube-scheduler.
	~[moodle]Kubelet.#<p>Kubelet quản lý Pod trên node sau khi được lập lịch.</p>
	~[moodle]Controller manager.#<p>Controller manager quản lý các vòng lặp điều khiển khác, chẳng hạn như tạo PV/PVC.</p>
	####<p><strong>Giải thích</strong>\: Bộ lập lịch Kubernetes (kube-scheduler) cung cấp một triển khai lập lịch sạch, đơn giản—hoàn hảo cho một hệ thống phức tạp như Kubernetes. Bộ lập lịch xem xét nhiều yếu tố trong việc lập lịch Pod. Chúng bao gồm các thành phần phần cứng trên một node, tài nguyên CPU và bộ nhớ có sẵn, các ràng buộc lập lịch chính sách và các yếu tố trọng số khác.</p>
}

// question: 2.9  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>"Pod density" (mật độ Pod) cao hơn trong Kubernetes có lợi ích gì?</p>{
	~[moodle]Tăng cường khả năng chịu lỗi bằng cách phân tán Pod trên nhiều node hơn.#<p>Mật độ Pod cao hơn có thể có nghĩa là ít node hơn, có thể ảnh hưởng đến khả năng chịu lỗi nếu một node bị lỗi.</p>
	=[moodle]Giảm chi phí bằng cách chạy nhiều Pod hơn trên ít máy chủ hơn.
	~[moodle]Tăng cường bảo mật bằng cách giới hạn số lượng Pod trên mỗi node.#<p>Mật độ cao không trực tiếp liên quan đến bảo mật theo cách này.</p>
	~[moodle]Đơn giản hóa việc quản lý cấu hình mạng cho các Pod.#<p>Quản lý mạng vẫn phức tạp ở mật độ cao.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes cho phép mật độ Pod cao hơn, đó là khả năng chạy các node được cấp phát quá mức và đóng gói dày đặc. Mật độ Pod được kiểm soát thông qua các bước như điều chỉnh cài đặt tài nguyên. Điều này giúp giảm chi phí đám mây.</p>
}

// question: 2.10  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Khi đề cập đến "Control Plane" trong Kubernetes, điều gì KHÔNG phải là một trong những khía cạnh mà nó điều khiển?</p>{
	~[moodle]Gắn lưu trữ vào các tiến trình.#<p>Đây là một khía cạnh mà Control Plane điều khiển.</p>
	~[moodle]Tạo và mở rộng số lượng container.#<p>Đây là một khía cạnh mà Control Plane điều khiển.</p>
	=[moodle]Tùy chỉnh trực tiếp cấu hình kernel Linux của mỗi node.
	~[moodle]Tạo các tuyến IP đến các cổng.#<p>Đây là một khía cạnh mà Control Plane điều khiển.</p>
	####<p><strong>Giải thích</strong>\: Control Plane kiểm soát nhiều khía cạnh của quản lý ứng dụng phân tán, bao gồm gắn lưu trữ, tạo và mở rộng container, tiêu diệt và di chuyển container không lành mạnh, tạo tuyến IP và cập nhật các điểm cuối cân bằng tải. Nó không trực tiếp tùy chỉnh cấu hình kernel Linux.</p>
}

// question: 2.11  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>"Operational requirements" (yêu cầu vận hành) của một ứng dụng web ví dụ trong Kubernetes bao gồm những gì?</p>{
	~[moodle]Chỉ yêu cầu một máy ảo duy nhất cho toàn bộ ứng dụng.#<p>Ứng dụng web phức tạp cần nhiều thành phần và có thể là nhiều VM hoặc server.</p>
	=[moodle]Tính năng cân bằng tải, khả năng mở rộng (scaling), và tính sẵn sàng cao (high availability).
	~[moodle]Chỉ lưu trữ dữ liệu trên một đĩa cục bộ, không có bất kỳ khả năng sao lưu nào.#<p>Ứng dụng web yêu cầu lưu trữ ổn định hơn, chẳng hạn như cho cơ sở dữ liệu.</p>
	~[moodle]Yêu cầu truy cập root đầy đủ cho mọi microservice.#<p>Quyền root đầy đủ là một rủi ro bảo mật và không phải là yêu cầu mặc định.</p>
	####<p><strong>Giải thích</strong>\: Yêu cầu vận hành của ứng dụng web ví dụ bao gồm: cân bằng tải, scaling, high availability.</p>
}

// question: 2.12  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Điều gì xảy ra khi kubelet được API server báo cho biết nó không lành mạnh (unhealthy) trong Kubernetes 1.17 trở lên?</p>{
	~[moodle]kubelet tự động tắt.#<p>Đây không phải là phản ứng trực tiếp của kubelet khi không lành mạnh.</p>
	=[moodle]kubelet cập nhật một đối tượng Lease nhỏ trong etcd để báo hiệu trạng thái của nó.
	~[moodle]kubelet khởi động lại tất cả các Pod trên node.#<p>Đây không phải là phản ứng trực tiếp của kubelet khi không lành mạnh.</p>
	~[moodle]API server ngay lập tức gỡ bỏ node khỏi cluster.#<p>Đây không phải là phản ứng trực tiếp của kubelet khi không lành mạnh.</p>
	####<p><strong>Giải thích</strong>\: Để tối ưu hóa hiệu suất của các cluster lớn và giảm độ "ồn ào" của mạng, Kubernetes phiên bản 1.17 trở lên triển khai một điểm cuối API server cụ thể để quản lý các kubelet thông qua cơ chế leasing của etcd. Kubelet cập nhật một đối tượng Lease (rất nhỏ) cứ sau 10 giây.</p>
}

// question: 2.13  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Mục đích chính của "Operator pattern" trong Kubernetes là gì?</p>{
	~[moodle]Để thay thế hoàn toàn các container runtime như Docker.#<p>Operator quản lý ứng dụng, không thay thế container runtime.</p>
	=[moodle]Để quản lý các ứng dụng phức tạp, có trạng thái (stateful applications) trên Kubernetes bằng cách tự động hóa các tác vụ vận hành.
	~[moodle]Để tạo các bản sao lưu (backups) tự động của dữ liệu cluster vào bộ nhớ tạm thời.#<p>Operator có thể quản lý backup nhưng đó không phải mục đích chính.</p>
	~[moodle]Để cung cấp một giao diện mạng ảo cho các Pod giao tiếp với nhau.#<p>CNI provider và kube-proxy cung cấp mạng ảo.</p>
	####<p><strong>Giải thích</strong>\: Vì mô hình Operator nhanh chóng trở thành cơ chế tiêu chuẩn để triển khai các ứng dụng phức tạp trên Kubernetes, lời khuyên của chúng tôi là chuyển từ việc sử dụng YAML thuần túy sang cài đặt và sử dụng Operator.</p>
}

// question: 2.14  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Khi một Pod được lập lịch trên một node, Container Runtime Interface (CRI) có trách nhiệm gì?</p>{
	~[moodle]Đặt tên duy nhất cho Pod.#<p>Tên Pod được định nghĩa trong YAML.</p>
	=[moodle]Kéo hình ảnh container từ registry và chạy container.
	~[moodle]Quản lý các PersistentVolume.#<p>CSI quản lý PersistentVolume.</p>
	~[moodle]Xác định trạng thái của node.#<p>Kubelet theo dõi trạng thái node.</p>
	####<p><strong>Giải thích</strong>\: Kubelet sử dụng CRI và CNI để điều hòa trạng thái của một node với trạng thái của control plane. Ví dụ, khi control plane quyết định rằng NGINX sẽ chạy trên các node hai, ba và bốn của một cluster năm node, nhiệm vụ của kubelet là đảm bảo CNI provider kéo container này từ một registry hình ảnh và chạy với địa chỉ IP trong phạm vi podCIDR. CRI là interface mà kubelet sử dụng để tương tác với các container runtime.</p>
}

// question: 2.15  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Điều gì KHÔNG phải là một thành phần điển hình của một Kubernetes Node chạy trên Linux?</p>{
	~[moodle]Hệ điều hành đã cài đặt (OS).#<p>Đây là một thành phần của một Kubernetes Node.</p>
	~[moodle]systemd (trình quản lý hệ thống và dịch vụ Linux).#<p>Đây là một thành phần của một Kubernetes Node.</p>
	=[moodle]Kubernetes API server.
	~[moodle]Kubelet (tác nhân node).#<p>Đây là một thành phần của một Kubernetes Node.</p>
	####<p><strong>Giải thích</strong>\: Một node có thể chạy trên Raspberry Pi, một máy ảo trong đám mây hoặc vô số nền tảng khác. Hình 2.4 hiển thị các thành phần tạo nên một node chạy trên Linux, bao gồm: một máy chủ, một hệ điều hành đã cài đặt, systemd, kubelet, container runtime, network proxy (kube-proxy), CNI provider. Kubernetes API server là thành phần của control plane, không phải của worker node.</p>
}

// question: 2.16  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>"Container Runtime Interface (CRI)" và "Container Network Interface (CNI)" là ví dụ về các giao diện đang phát triển trong Kubernetes để hỗ trợ mục tiêu nào?</p>{
	~[moodle]Tạo ra một hệ thống được tích hợp chặt chẽ, phụ thuộc vào nhà cung cấp.#<p>Mục tiêu là ngược lại, phân tách khỏi sự phụ thuộc vào nhà cung cấp.</p>
	=[moodle]Phân tách chức năng cụ thể của nhà cung cấp thành các thành phần có thể cắm được, mô-đun hóa.
	~[moodle]Đơn giản hóa quá trình lập lịch của Kubernetes bằng cách loại bỏ các tùy chọn phức tạp.#<p>Mục tiêu là tính mô-đun, không phải đơn giản hóa lập lịch bằng cách loại bỏ các tùy chọn.</p>
	~[moodle]Giảm thiểu khả năng tương thích của Kubernetes với các hệ điều hành khác ngoài Linux.#<p>Tính mô-đun hóa giúp tăng cường khả năng tương thích.</p>
	####<p><strong>Giải thích</strong>\: Các giao diện khác đang phát triển để hỗ trợ một tương lai mô-đun hóa, trung lập với nhà cung cấp hơn cho Kubernetes là Container Networking Interface (CNI), Container Runtime Interface (CRI), và Container Storage Interface (CSI).</p>
}

// question: 2.17  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Một "ClusterIP Service" trong Kubernetes có đặc điểm gì?</p>{
	~[moodle]Cung cấp một cổng mở trên một node Kubernetes để cân bằng tải.#<p>NodePort làm điều này.</p>
	~[moodle]Tạo một bộ cân bằng tải bên ngoài cluster, có thể truy cập từ internet.#<p>LoadBalancer làm điều này.</p>
	=[moodle]Là một dịch vụ nội bộ cân bằng tải các Pod Kubernetes, chỉ có thể truy cập được từ bên trong cluster.
	~[moodle]Gán một địa chỉ IP duy nhất và cố định cho mỗi Pod.#<p>Pods có địa chỉ IP riêng của chúng, nhưng ClusterIP là cho dịch vụ.</p>
	####<p><strong>Giải thích</strong>\: ClusterIP là một dịch vụ nội bộ cân bằng tải các Pod Kubernetes.</p>
}

// question: 2.18  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>"Autoscaling" (tự động mở rộng) trong Kubernetes mang lại lợi ích gì liên quan đến chi phí?</p>{
	~[moodle]Tăng chi phí đám mây do luôn có nhiều node hơn mức cần thiết.#<p>Mục tiêu của autoscaling là tối ưu hóa, không phải tăng chi phí không cần thiết.</p>
	=[moodle]Cho phép điều chỉnh số lượng node trong cluster, giúp tiết kiệm chi phí bằng cách giảm node khi không cần.
	~[moodle]Chỉ tối ưu hóa hiệu suất, không có ảnh hưởng đến chi phí.#<p>Autoscaling ảnh hưởng trực tiếp đến chi phí.</p>
	~[moodle]Yêu cầu quản lý thủ công liên tục để tối ưu hóa chi phí.#<p>Autoscaling là tự động, giảm quản lý thủ công.</p>
	####<p><strong>Giải thích</strong>\: Khi một cluster tự động mở rộng, nó tự động thêm nhiều node hơn vào cluster, điều đó có nghĩa là nhiều node hơn sẽ bằng chi phí sử dụng đám mây cao hơn. Nhiều node hơn cho phép ứng dụng của bạn có nhiều bản sao hơn và xử lý nhiều tải hơn, nhưng sau đó sếp của bạn nhận hóa đơn và muốn có một giải pháp để tiết kiệm tiền. Nguồn cũng nói về việc giảm số lượng worker node xuống 0 để tiết kiệm chi phí.</p>
}

// question: 2.19  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Khi sử dụng kubectl apply -f deployment.yaml để tạo một Deployment NGINX, thành phần đầu tiên trong control plane mà kubectl giao tiếp là gì?</p>{
	~[moodle]Kube-scheduler.#<p>Scheduler được API server gọi để lập lịch.</p>
	=[moodle]Kubernetes API server.
	~[moodle]Kubelet.#<p>Kubelet chạy trên node, nhận chỉ thị từ API server.</p>
	~[moodle]Etcd.#<p>Etcd là nơi lưu trữ dữ liệu cho API server.</p>
	####<p><strong>Giải thích</strong>\: Khi bạn thực thi kubectl apply, kubectl giao tiếp với thành phần đầu tiên trong control plane. Đó là API server.</p>
}

// question: 2.20  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Node API object trong Kubernetes cung cấp thông tin gì?</p>{
	~[moodle]Danh sách các container đang chạy trên tất cả các node.#<p>kubectl get pods hiển thị danh sách container chạy.</p>
	=[moodle]Thông tin về node, bao gồm địa chỉ IP nội bộ, CIDR của Pod, và trạng thái sức khỏe của kubelet.
	~[moodle]Chỉ định các quy tắc bảo mật mạng cho các Pod.#<p>NetworkPolicy định nghĩa quy tắc bảo mật mạng.</p>
	~[moodle]Thông tin chi tiết về các ứng dụng được triển khai trên node.#<p>Thông tin ứng dụng được lấy từ Deployment, Pod.</p>
	####<p><strong>Giải thích</strong>\: Node API object mô tả node lưu trữ control plane Kubernetes, bao gồm các annotations như kubeadm.alpha.kubernetes.io/cri-socket và các nhãn (labels). Nó cũng cung cấp thông tin về trạng thái node, bao gồm địa chỉ IP nội bộ (InternalIP), tên host (Hostname), và các điều kiện sức khỏe của kubelet (MemoryPressure, DiskPressure, PIDPressure, Ready).</p>
}

// question: 2.21  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>"Infrastructure controllers" (bộ điều khiển hạ tầng) trong Kubernetes chủ yếu dùng để làm gì?</p>{
	~[moodle]Để giám sát hiệu suất CPU và bộ nhớ của các node.#<p>Giám sát hiệu suất thuộc về Prometheus và cAdvisor.</p>
	~[moodle]Để quản lý các ứng dụng không trạng thái (stateless applications) như NGINX.#<p>Deployments quản lý ứng dụng không trạng thái.</p>
	=[moodle]Để xử lý các yêu cầu phức tạp về hạ tầng cho các ứng dụng có trạng thái (stateful applications) như cơ sở dữ liệu.
	~[moodle]Để cung cấp giao diện dòng lệnh cho người dùng tương tác với cluster.#<p>kubectl cung cấp giao diện dòng lệnh.</p>
	####<p><strong>Giải thích</strong>\: Ứng dụng có trạng thái, giống như cơ sở dữ liệu, thường có các yêu cầu vận hành cụ thể. Điều này dẫn đến việc yêu cầu một bộ điều khiển hoặc một Operator để quản lý ứng dụng.</p>
}

// question: 2.22  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>"Cloud Controller Manager (CCM)" được thiết kế để giải quyết vấn đề gì trong Kubernetes?</p>{
	~[moodle]Đảm bảo tất cả các Pod đều có địa chỉ IP duy nhất.#<p>CNI cung cấp địa chỉ IP cho Pods.</p>
	=[moodle]Cho phép phát triển nhà cung cấp đám mây nhanh hơn bằng cách phân tách chức năng cụ thể của nhà cung cấp ra khỏi codebase chính của Kubernetes.
	~[moodle]Cung cấp một cơ sở dữ liệu nhất quán cho toàn bộ cluster.#<p>Etcd cung cấp cơ sở dữ liệu nhất quán.</p>
	~[moodle]Quản lý việc lập lịch các Pod trên các node dựa trên tài nguyên có sẵn.#<p>Scheduler quản lý việc lập lịch Pod.</p>
	####<p><strong>Giải thích</strong>\: CCM được thiết kế để cho phép phát triển nhà cung cấp đám mây nhanh hơn và tạo các nhà cung cấp đám mây. Việc tái cấu trúc repository này cho phép các chủ sở hữu nhà cung cấp đám mây quản lý mã và cho phép các nhà cung cấp di chuyển với tốc độ cao hơn.</p>
}

// question: 2.23  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Khi một ứng dụng được định nghĩa là có "High Availability" (HA) với "five 9s" (99.999% uptime), nó có nghĩa là gì?</p>{
	~[moodle]Ứng dụng có thể có hơn 5 phút ngừng hoạt động mỗi tháng.#<p>5 phút 15 giây là tổng thời gian cho cả năm, không phải mỗi tháng.</p>
	~[moodle]Ứng dụng không bao giờ bị ngừng hoạt động.#<p>Không có ứng dụng nào có thể đảm bảo 100% uptime.</p>
	=[moodle]Ứng dụng chỉ có thể có 5 phút và 15 giây ngừng hoạt động có thể xảy ra trong một năm.
	~[moodle]Ứng dụng được thiết kế để chạy trên năm node khác nhau.#<p>"Five 9s" là về uptime, không phải số node.</p>
	####<p><strong>Giải thích</strong>\: Bốn 9 cho chúng ta 52 phút và 36 giây ngừng hoạt động mỗi năm; năm 9 (99.999% uptime) cho chúng ta 5 phút và 15 giây ngừng hoạt động có thể xảy ra.</p>
}

// question: 2.24  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Pod có thể duy trì bất kỳ trạng thái nào mà không cần một PersistentVolume không?</p>{
	~[moodle]Có, thông qua việc ghi dữ liệu vào lớp trên cùng của hệ thống tệp container.#<p>Dữ liệu trên lớp ghi tạm thời sẽ biến mất khi Pod khởi động lại.</p>
	=[moodle]Không, tất cả dữ liệu sẽ biến mất khi Pod khởi động lại.
	~[moodle]Có, nhưng chỉ khi dữ liệu được lưu trữ trong Secrets.#<p>Secrets được dùng cho dữ liệu nhạy cảm nhỏ, không phải lưu trữ dữ liệu ứng dụng lớn.</p>
	~[moodle]Có, bằng cách sử dụng PersistentVolumeClaims được định nghĩa trước.#<p>PVC là để duy trì trạng thái, nhưng câu hỏi là "không cần một volume".</p>
	####<p><strong>Giải thích</strong>\: Khả năng ghi dữ liệu vào lớp trên cùng của hệ thống tệp container nói chung là chậm và không được khuyến nghị cho lưu lượng ghi lớn. Và, trong mọi trường hợp, điều này đơn giản là không hoạt động: dữ liệu này biến mất ngay khi Pod được khởi động lại.</p>
}

// question: 2.25  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Điều gì KHÔNG phải là một trong những loại Services trong Kubernetes?</p>{
	~[moodle]ClusterIP.#<p>Đây là một loại Service được liệt kê.</p>
	~[moodle]NodePort.#<p>Đây là một loại Service được liệt kê.</p>
	=[moodle]ExternalService.
	~[moodle]LoadBalancer.#<p>Đây là một loại Service được liệt kê.</p>
	####<p><strong>Giải thích</strong>\: Các loại Services bao gồm: ClusterIP, NodePort, LoadBalancer. ExternalService không phải là một loại Service được liệt kê trực tiếp.</p>
}

// question: 2.26  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>"Infrastructure for our web application" bao gồm những gì?</p>{
	=[moodle]Các máy ảo (VMs) trên đám mây hoặc máy tính vật lý làm máy chủ.
	~[moodle]Các công cụ tích hợp liên tục (CI) như Jenkins hoặc CircleCI.#<p>Đây là các công cụ mà hạ tầng cần hỗ trợ, không phải bản thân hạ tầng.</p>
	~[moodle]Chỉ một máy chủ duy nhất để chạy ứng dụng.#<p>Ứng dụng web cần nhiều thành phần và có thể là nhiều server.</p>
	~[moodle]Các ứng dụng cơ sở dữ liệu như MySQL hoặc Postgres.#<p>Đây là các loại ứng dụng mà hạ tầng cần hỗ trợ, không phải bản thân hạ tầng.</p>
	####<p><strong>Giải thích</strong>\: Nếu không có phần mềm điều phối container như Kubernetes, các tổ chức cần nhiều thành phần trong hạ tầng của họ. Để chạy một ứng dụng, bạn cần nhiều máy ảo (VMs) trên đám mây hoặc máy tính vật lý làm máy chủ của bạn.</p>
}

// question: 2.27  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Các control loops trong Kubernetes hoạt động như thế nào, giống như một máy điều hòa nhiệt độ?</p>{
	~[moodle]Điều chỉnh nhiệt độ bên trong container.#<p>Máy điều hòa nhiệt độ điều chỉnh nhiệt độ, nhưng Kubernetes điều hòa trạng thái cluster.</p>
	=[moodle]Kiểm soát và điều hòa trạng thái của cluster theo trạng thái mong muốn.
	~[moodle]Cung cấp năng lượng cho các worker node.#<p>Cung cấp năng lượng là chức năng vật lý, không phải control loop.</p>
	~[moodle]Quản lý việc cấp phát địa chỉ IP vật lý cho mỗi Pod.#<p>CNI cung cấp địa chỉ IP.</p>
	####<p><strong>Giải thích</strong>\: Tại cốt lõi, Kubernetes là một cỗ máy điều hòa trạng thái với các vòng lặp điều khiển khác nhau, giống như một máy điều hòa nhiệt độ. Thay vì điều chỉnh nhiệt độ, Kubernetes kiểm soát việc gắn lưu trữ, tạo/mở rộng container, tiêu diệt/di chuyển container, tạo tuyến IP và cập nhật các điểm cuối cân bằng tải.</p>
}

// question: 2.28  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Trong ngữ cảnh "Pod density" và tối ưu hóa chi phí, điều gì có thể được thực hiện với số lượng worker node trong control plane vào cuối tuần nếu không cần môi trường phát triển?</p>{
	~[moodle]Tăng số lượng worker node để xử lý tải cao hơn.#<p>Tăng số node sẽ làm tăng chi phí.</p>
	=[moodle]Giảm số lượng worker node xuống 0 để tiết kiệm chi phí.
	~[moodle]Giữ nguyên số lượng worker node và chỉ dừng các Pod không cần thiết.#<p>Giữ nguyên số node vẫn tốn kém hơn so với việc tắt chúng.</p>
	~[moodle]Chuyển tất cả các Pod sang một cluster khác.#<p>Chuyển Pod sang cluster khác không phải là giải pháp tiết kiệm chi phí cho chính cluster đó.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn không cần môi trường phát triển của mình chạy vào cuối tuần, thì tại sao nó lại hoạt động? Đơn giản là giảm số lượng worker node trong control plane xuống 0, và khi bạn cần cluster hoạt động trở lại, tăng số lượng worker node.</p>
}

// question: 2.29  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>Điều gì là lý do chính khiến các container kube-apiserver, kube-controller-manager và kube-scheduler được tìm thấy trong phần images của Node API object?</p>{
	~[moodle]Chúng là các ứng dụng mà người dùng triển khai trên node.#<p>Đây là các thành phần hệ thống của Kubernetes, không phải ứng dụng người dùng điển hình.</p>
	=[moodle]Chúng là các thành phần của control plane được Docker hoặc containerd chạy trên node đó.
	~[moodle]Chúng là các hình ảnh chỉ được tải xuống nhưng không chạy.#<p>Chúng được liệt kê vì chúng đang chạy.</p>
	~[moodle]Chúng là các thành phần tùy chọn có thể được cài đặt trên node.#<p>Chúng là các thành phần cốt lõi của control plane.</p>
	####<p><strong>Giải thích</strong>\: Phần images trong Node API object liệt kê các hình ảnh container đang chạy trên node đó. Trong một cluster kind, các thành phần control plane như kube-apiserver, kube-controller-manager và kube-scheduler được chạy dưới dạng container.</p>
}

// question: 2.30  name: Chapter 2: Why the Pod?
::Chapter 2\: Why the Pod?::[html]<p>StatefulSets khác với Deployments như thế nào trong ngữ cảnh DNS?</p>{
	~[moodle]StatefulSets không hỗ trợ bất kỳ loại DNS nào, chỉ dựa vào địa chỉ IP.#<p>StatefulSets hỗ trợ DNS.</p>
	=[moodle]StatefulSets cung cấp các bản ghi DNS liên tục cho các Pod của chúng, cho phép các Pod giữ cùng một tên host khi khởi động lại hoặc di chuyển.
	~[moodle]Deployments cung cấp DNS nhất quán hơn StatefulSets.#<p>StatefulSets thường cung cấp DNS nhất quán hơn cho các Pod cá nhân.</p>
	~[moodle]StatefulSets yêu cầu cấu hình DNS thủ công cho mỗi Pod.#<p>DNS được quản lý tự động, không phải thủ công.</p>
	####<p><strong>Giải thích</strong>\: StatefulSets có các bản ghi DNS liên tục cho các Pod của chúng, cho phép các Pod giữ cùng một tên host khi khởi động lại hoặc di chuyển. DNS with headless services là một tính năng chính của StatefulSets.</p>
}

// Chapter 3: Let’s build a Pod
// question: 3 name: Switch category to $module$/top/Chapter 3: Let’s build a Pod
$CATEGORY: $module$/top/Chapter 3: Let’s build a Pod

// question: 3.1  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều gì xảy ra trong khoảng thời gian giữa khi một Pod được tạo lần đầu tiên và khi nó được khai báo ở trạng thái "Running"?</p>{
	~[moodle]Kubelet đợi cho đến khi một lệnh thủ công được phát ra để khởi động Pod.#<p>Quá trình này tự động.</p>
	=[moodle]Một loạt các nguyên thủy Linux được gọi để tạo ra một container, bao gồm thiết lập mạng và PID namespace.
	~[moodle]Pod được tự động di chuyển đến một node khác để tìm tài nguyên.#<p>Di chuyển Pod xảy ra nếu có vấn đề, không phải trong quá trình khởi động ban đầu.</p>
	~[moodle]Container runtime tải xuống tất cả các phụ thuộc của ứng dụng từ internet.#<p>Tải hình ảnh là một phần của quá trình này, nhưng không phải là tất cả những gì xảy ra.</p>
	####<p><strong>Giải thích</strong>\: Có một khoảng thời gian dài giữa khi một Pod được tạo lần đầu tiên và khi nó được khai báo ở trạng thái running. Điều gì đang diễn ra trong khoảng thời gian này? Một loạt các nguyên thủy Linux mà bạn có thể không sử dụng trong cuộc sống hàng ngày đang được triệu tập để tạo ra thứ được gọi là container. Kubelet khởi chạy một container tạm dừng (pause container) để cấp cho hệ điều hành Linux thời gian tạo mạng cho container.</p>
}

// question: 3.2  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Công cụ chroot trong Linux được sử dụng để làm gì khi xây dựng một container từ đầu?</p>{
	~[moodle]Để thực thi một ứng dụng trong một thư mục đã tạo.#<p>Thực thi ứng dụng là bước cuối cùng sau khi mọi thứ đã được thiết lập.</p>
	~[moodle]Để tạo các namespaces người dùng.#<p>Namespaces người dùng được tạo bằng lệnh unshare.</p>
	=[moodle]Để thiết lập thư mục đã tạo làm hệ thống tệp giả cho ứng dụng, giúp cô lập nó khỏi hệ thống tệp thật của host.
	~[moodle]Để giới hạn lượng tài nguyên CPU và bộ nhớ mà ứng dụng có thể sử dụng.#<p>Giới hạn tài nguyên là chức năng của các nhóm kiểm soát (cgroups).</p>
	####<p><strong>Giải thích</strong>\: chroot tạo ra một "hộp" nơi chúng ta có thể chạy một tập lệnh Bash hoặc chương trình Linux khác. Điều này không có khả năng hiển thị nào khác vào hệ thống rộng lớn hơn và không có xung đột, có nghĩa là nếu chúng ta muốn chạy rm -rf / bên trong hộp, chúng ta có thể làm như vậy mà không phá hủy tất cả các tệp trong hệ điều hành thực tế của chúng ta. Lệnh chroot được sử dụng để đặt thư mục đã tạo làm hệ thống tệp giả cho ứng dụng.</p>
}

// question: 3.3  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều gì mô tả khái niệm "Everything is a file" (Mọi thứ là một tệp) trong Linux?</p>{
	~[moodle]Tất cả dữ liệu trên hệ thống được lưu trữ dưới dạng một tệp duy nhất.#<p>Không phải dữ liệu được lưu trữ trong một tệp duy nhất.</p>
	=[moodle]Kernel Linux xử lý mọi tài nguyên hệ thống, bao gồm thư mục, thiết bị, socket và pipe, như các tệp hoặc bộ mô tả tệp.
	~[moodle]Mọi ứng dụng đều phải lưu trữ đầu ra của nó vào một tệp vật lý.#<p>Đầu ra có thể được chuyển hướng đến "standard out" (thiết bị đầu cuối), cũng được coi là một tệp.</p>
	~[moodle]Chỉ các tệp văn bản mới có thể được truy cập trong hệ điều hành Linux.#<p>Tất cả các loại tệp đều có thể truy cập được.</p>
	####<p><strong>Giải thích</strong>\: Các nguyên thủy Linux, theo một nghĩa nào đó, hầu như luôn thực hiện một cái gì đó để thao tác, di chuyển hoặc cung cấp một trừu tượng hóa trên một loại tệp nào đó. Điều này là do mọi thứ bạn cần xây dựng với Kubernetes ban đầu được xây dựng để hoạt động trên Linux, và Linux được thiết kế hoàn toàn để sử dụng trừu tượng hóa tệp làm một nguyên thủy kiểm soát. Một thư mục là một tệp, nhưng nó chứa tên của các tệp khác. Các thiết bị cũng được biểu diễn dưới dạng các tệp đối với kernel Linux. Socket và pipe cũng là các tệp, mà các tiến trình có thể sử dụng cục bộ để giao tiếp.</p>
}

// question: 3.4  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Công cụ kind được mô tả như thế nào trong bối cảnh Kubernetes?</p>{
	~[moodle]Một công cụ triển khai Kubernetes cấp độ sản xuất cho các trung tâm dữ liệu lớn.#<p>Kind không phải là nhà cung cấp Kubernetes sản xuất và chỉ được sử dụng cho mục đích phát triển hoặc nghiên cứu.</p>
	=[moodle]Một công cụ phát triển cho phép chạy các cluster Kubernetes bên trong các container Docker cục bộ.
	~[moodle]Một dịch vụ giám sát hiệu suất cho các Pod trong Kubernetes.#<p>Prometheus là một dịch vụ giám sát.</p>
	~[moodle]Một phương pháp để tạo ra các hình ảnh container bất biến.#<p>Dockerfile và các công cụ xây dựng hình ảnh tạo ra hình ảnh container.</p>
	####<p><strong>Giải thích</strong>\: Kind[](https://kind.sigs.k8s.io) là một công cụ phát triển cho Kubernetes. Điều này sẽ là cơ sở cho nhiều thí nghiệm chúng ta thực hiện trong cuốn sách này. Kind cho phép bạn chạy các cluster Kubernetes (đơn node hoặc đa node) bên trong một container runtime, chẳng hạn như Docker Engine.</p>
}

// question: 3.5  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Khi một Pod khởi động, "pause container" có vai trò gì?</p>{
	~[moodle]Thực thi ứng dụng chính ngay lập tức.#<p>Ứng dụng chính chỉ bắt đầu sau khi pause container đã thiết lập môi trường.</p>
	=[moodle]Cung cấp một môi trường tạm thời để khởi tạo mạng và PID namespace cho Pod.
	~[moodle]Tải xuống hình ảnh ứng dụng từ registry.#<p>Container runtime kéo hình ảnh, nhưng pause container là để thiết lập namespace.</p>
	~[moodle]Giám sát tình trạng sức khỏe của các container khác trong Pod.#<p>Kubelet giám sát tình trạng.</p>
	####<p><strong>Giải thích</strong>\: Kubelet (bằng cách nói chuyện với một container runtime) sau đó khởi chạy một pause container, cấp cho hệ điều hành Linux thời gian để tạo một mạng cho container. Pause container này là tiền thân của ứng dụng thực tế mà chúng ta sẽ chạy. Nó tồn tại với mục đích tạo một "ngôi nhà" ban đầu để khởi động quá trình mạng container mới và ID tiến trình (PID) của nó.</p>
}

// question: 3.6  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều gì là rủi ro bảo mật chính khi sử dụng chức năng hostPath của Kubernetes volumes?</p>{
	~[moodle]Nó chỉ cho phép truy cập chỉ đọc vào các tệp của host.#<p>hostPath có thể cho phép ghi, không chỉ đọc.</p>
	=[moodle]Nó có thể cho phép container thao túng hoặc đọc nội dung của các thư mục quan trọng trên host.
	~[moodle]Nó làm chậm hiệu suất I/O của container.#<p>hostPath không nhất thiết làm chậm hiệu suất I/O.</p>
	~[moodle]Nó đòi hỏi cấu hình mạng phức tạp.#<p>hostPath là về lưu trữ, không phải mạng.</p>
	####<p><strong>Giải thích</strong>\: Hãy lưu ý rằng điều này mở ra một lỗ hổng bảo mật! Sau khi chúng ta mount nội dung của /tmp vào các container, bất kỳ ai cũng có thể thao túng hoặc đọc nội dung của nó. Đây thực sự là lý do tại sao chức năng hostPath của Kubernetes volumes thường bị tắt trong các cluster sản xuất.</p>
}

// question: 3.7  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>cgroups (control groups) trong Linux có chức năng chính là gì đối với các Pod trong Kubernetes?</p>{
	~[moodle]Quản lý việc định tuyến lưu lượng mạng giữa các Pod.#<p>Định tuyến mạng do CNI và kube-proxy xử lý.</p>
	=[moodle]Cô lập và phân bổ tài nguyên hệ điều hành như CPU và bộ nhớ cho các tiến trình.
	~[moodle]Tạo ra một hệ thống tệp riêng biệt cho mỗi container.#<p>Hệ thống tệp riêng biệt được tạo bởi các namespace và OverlayFS.</p>
	~[moodle]Cung cấp một giao diện API cho các ứng dụng để giao tiếp với kernel Linux.#<p>Kernel Linux cung cấp API, cgroups là để quản lý tài nguyên.</p>
	####<p><strong>Giải thích</strong>\: Các nhóm kiểm soát (viết tắt là cgroups) là những nút điều khiển mà tất cả chúng ta đều biết và yêu thích. Chúng cho phép chúng ta cấp nhiều hoặc ít CPU và bộ nhớ hơn cho các ứng dụng chạy trong các cluster của chúng ta. Cgroups cho phép chúng ta định nghĩa các "bin" (thùng) được phân tách theo phân cấp cho bộ nhớ, CPU và các tài nguyên hệ điều hành khác.</p>
}

// question: 3.8  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Khi bạn chạy kubectl exec -t -i core-k8s ip a trong một Pod BusyBox đang chạy, điều gì bạn sẽ mong đợi được thấy mà không có trong một tiến trình chroot đơn giản?</p>{
	~[moodle]Một danh sách các tiến trình hệ thống đang chạy trên host.#<p>Một tiến trình chroot có thể nhìn thấy tiến trình host trừ khi unshare được sử dụng.</p>
	=[moodle]Một thiết bị eth0 hoạt động với một địa chỉ IP có thể sử dụng được trong Pod.
	~[moodle]Các tùy chọn cấu hình cgroup của Pod.#<p>cgroup được thiết lập bên ngoài Pod, mặc dù Pod sử dụng chúng.</p>
	~[moodle]Nội dung của /etc/resolv.conf được Pod sử dụng.#<p>/etc/resolv.conf là một tệp được mount vào Pod, không phải thiết bị mạng.</p>
	####<p><strong>Giải thích</strong>\: Nếu chúng ta so sánh Pod này với một Pod thực đang chạy trong một cluster Kubernetes thông thường, chúng ta sẽ thấy một điểm khác biệt quan trọng hơn: thiếu một thiết bị eth0 hoạt động. Nếu chúng ta chạy Pod BusyBox của chúng ta trước đó với ip a (mà chúng ta sẽ làm trong phần tiếp theo), chúng ta sẽ thấy một mạng sống động hơn nhiều với một thiết bị eth0 có thể sử dụng được.</p>
}

// question: 3.9  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>kube-proxy trong Kubernetes chủ yếu sử dụng công cụ Linux nào để thực hiện định tuyến mạng cấp thấp cho các dịch vụ?</p>{
	~[moodle]chroot.#<p>chroot để cô lập hệ thống tệp.</p>
	~[moodle]mount.#<p>mount để gắn kết dữ liệu.</p>
	=[moodle]iptables.
	~[moodle]unshare.#<p>unshare để tạo namespaces.</p>
	####<p><strong>Giải thích</strong>\: Trong hầu hết các cluster, các quy tắc mạng này được triển khai hoàn toàn bởi kube-proxy, thường được cấu hình để sử dụng chương trình iptables để thực hiện định tuyến mạng cấp thấp.</p>
}

// question: 3.10  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Khi xây dựng một Pod từ đầu, mục đích của việc sử dụng lệnh unshare là gì?</p>{
	~[moodle]Để sao chép các tệp từ hệ thống host vào thư mục làm việc của tiến trình.#<p>cp hoặc mount thực hiện sao chép tệp.</p>
	=[moodle]Để tạo các tiến trình con chạy trong sự cô lập từ các namespaces mạng, mount, hoặc PID.
	~[moodle]Để cấp cho tiến trình quyền truy cập root vào tất cả các tài nguyên hệ thống.#<p>unshare tạo sự cô lập, không cấp quyền root.</p>
	~[moodle]Để giám sát hiệu suất CPU và bộ nhớ của tiến trình.#<p>cgroups giám sát hiệu suất.</p>
	####<p><strong>Giải thích</strong>\: Lệnh unshare cho phép một tiến trình tạo các tiến trình con chạy trong sự cô lập từ một mạng, mount hoặc PID. Chúng ta sẽ sử dụng nó kỹ lưỡng trong chương này để khám phá hiện tượng Pid 1 nổi tiếng trong các container, nơi mọi container trong một cluster Kubernetes đều nghĩ nó là chương trình duy nhất trên toàn thế giới.</p>
}

// question: 3.11  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Khái niệm "mount propagation" (truyền bá mount) trong Linux quan trọng như thế nào đối với các CSI driver?</p>{
	~[moodle]Nó cho phép các CSI driver chạy trên các hệ điều hành không phải Linux.#<p>Mount propagation là một yêu cầu của Linux, không phải là một cách để chạy trên các OS khác.</p>
	=[moodle]Nó cho phép kubelet chấp nhận rằng các mount có thể được tạo từ bên trong một container.
	~[moodle]Nó cung cấp một cách để mã nguồn của CSI driver được biên dịch vào kubelet.#<p>CSI được thiết kế để tách biệt mã nguồn của nhà cung cấp khỏi kubelet.</p>
	~[moodle]Nó tăng cường hiệu suất của các hoạt động đọc/ghi vào volume.#<p>Mount propagation giải quyết vấn đề tương thích, không phải hiệu suất.</p>
	####<p><strong>Giải thích</strong>\: Vì các CSI driver là một tập hợp các container thường được duy trì bởi các nhà cung cấp, kubelet tự nó cần có khả năng chấp nhận rằng các mount có thể được tạo từ bên trong một container. Điều này được gọi là mount propagation và là một phần quan trọng của các yêu cầu Linux cấp thấp để một số khía cạnh của Kubernetes hoạt động đúng cách.</p>
}

// question: 3.12  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều gì là lý do chính khiến các container BusyBox thường được sử dụng trong các ví dụ hướng dẫn Kubernetes?</p>{
	~[moodle]Vì chúng rất lớn và chứa nhiều tiện ích để thử nghiệm.#<p>Ngược lại, chúng rất nhỏ.</p>
	=[moodle]Vì chúng là hình ảnh Linux tối thiểu, đi kèm với các tiện ích cơ bản như ip a, thích hợp để điều tra hành vi container mặc định.
	~[moodle]Vì chúng cung cấp hiệu suất mạng cao nhất cho các ứng dụng.#<p>BusyBox không tập trung vào hiệu suất mạng.</p>
	~[moodle]Vì chúng tự động cấu hình DNS và lưu trữ cho Pod.#<p>Nó không tự động cấu hình DNS hoặc lưu trữ theo cách toàn diện.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn đang thắc mắc về hình ảnh BusyBox, Pod BusyBox chỉ là một hình ảnh Linux tối thiểu mà bạn có thể chạy để điều tra hành vi container mặc định. Mặc dù các ví dụ thường sử dụng Pod NGINX làm tiêu chuẩn, chúng tôi chọn BusyBox vì nó đi kèm với lệnh ip a và đóng gói các tiện ích cơ bản khác.</p>
}

// question: 3.13  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Trong quá trình khởi động Pod của Kubernetes, đâu là một trong những hành động mà kubelet thực hiện?</p>{
	~[moodle]Trực tiếp chạy các container mà không thông qua bất kỳ giao diện nào.#<p>Kubelet không chạy container trực tiếp; nó chuyển sang CRI.</p>
	=[moodle]Phải tìm ra rằng nó phải chạy một container, sau đó khởi chạy một pause container.
	~[moodle]Tự động cấp quyền truy cập root cho tất cả các container.#<p>Quyền root là một rủi ro bảo mật và không được tự động cấp.</p>
	~[moodle]Tự động tạo các PersistentVolume mới cho mỗi Pod.#<p>Dynamic provisioner tạo PVs, không phải kubelet trực tiếp.</p>
	####<p><strong>Giải thích</strong>\: Kubelet phải tìm ra rằng nó phải chạy một container. Kubelet (bằng cách nói chuyện với một container runtime) sau đó khởi chạy một pause container.</p>
}

// question: 3.14  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Khi một Pod được Kubernetes tạo, default-token volume cung cấp cho Pod điều gì?</p>{
	~[moodle]Một giao diện mạng ảo để giao tiếp giữa các Pod.#<p>CNI cung cấp giao diện mạng ảo.</p>
	=[moodle]Một chứng chỉ cho phép Pod giao tiếp với API server.
	~[moodle]Một thư mục tạm thời để lưu trữ dữ liệu không liên tục.#<p>emptyDir cung cấp thư mục tạm thời.</p>
	~[moodle]Một bản ghi DNS để tìm kiếm các dịch vụ bên ngoài.#<p>CoreDNS cung cấp bản ghi DNS.</p>
	####<p><strong>Giải thích</strong>\: Một trường như vậy mà Kubernetes hào phóng cung cấp cho tất cả các Pod của nó là default-token volume. Điều này cung cấp cho các Pod của chúng ta một chứng chỉ cho phép chúng giao tiếp với API server và để "gọi về nhà".</p>
}

// question: 3.15  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều gì KHÔNG phải là một trong các nguyên thủy Linux mà Kubernetes dựa vào hàng ngày?</p>{
	~[moodle]swapoff (tắt bộ nhớ swap).#<p>Đây là một nguyên thủy Linux mà Kubernetes dựa vào.</p>
	=[moodle]chkdsk (kiểm tra đĩa trên Windows).
	~[moodle]iptables (quy tắc tường lửa).#<p>Đây là một nguyên thủy Linux mà Kubernetes dựa vào.</p>
	~[moodle]mount (gắn tài nguyên vào một vị trí cụ thể).#<p>Đây là một nguyên thủy Linux mà Kubernetes dựa vào.</p>
	####<p><strong>Giải thích</strong>\: Các chương trình (hoặc nguyên thủy) mà chúng ta dựa vào hàng ngày trong các cluster Kubernetes của chúng ta bao gồm swapoff, iptables, mount, systemd, socat, unshare, ps. chkdsk là một công cụ trên Windows, không phải nguyên thủy Linux mà Kubernetes sử dụng.</p>
}

// question: 3.16  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Theo nguồn, containerd đóng vai trò gì trong kiến trúc container runtime của Kubernetes?</p>{
	~[moodle]Nó là công cụ dòng lệnh chính để tương tác với Kubernetes.#<p>kubectl là công cụ dòng lệnh chính.</p>
	=[moodle]Nó là một triển khai phổ biến của CRI, được kubelet sử dụng để khởi động và dừng Pods.
	~[moodle]Nó là một loại hình ảnh container tối thiểu được sử dụng làm cơ sở.#<p>BusyBox là một hình ảnh container tối thiểu.</p>
	~[moodle]Nó quản lý PersistentVolumes và PersistentVolumeClaims.#<p>CSI quản lý PersistentVolumes và PersistentVolumeClaims.</p>
	####<p><strong>Giải thích</strong>\: Triển khai phổ biến nhất của CRI là containerd, và trên thực tế, Docker tự nó sử dụng containerd bên dưới. CRI đại diện cho một số (nhưng không phải tất cả) chức năng của containerd trong một giao diện tối thiểu, giúp mọi người dễ dàng triển khai các container runtime của riêng họ cho Kubernetes.</p>
}

// question: 3.17  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều gì là lý do chính khiến Docker đã bị phản đối (deprecated) trong Kubernetes 1.20?</p>{
	~[moodle]Docker không còn được sử dụng để phát triển ứng dụng.#<p>Docker vẫn được sử dụng rộng rãi để phát triển.</p>
	=[moodle]Kubernetes đang chuyển sang một giao diện trung lập với container runtime (CRI), và Docker không tích hợp tốt với mô hình này.
	~[moodle]Docker là một container runtime nặng nề và không phù hợp cho môi trường sản xuất.#<p>Mặc dù có những cân nhắc về trọng lượng, lý do chính là sự chuyển đổi sang CRI.</p>
	~[moodle]Các lý do bảo mật đã buộc Kubernetes phải ngừng hỗ trợ Docker.#<p>Lý do chính là kiến trúc, không phải trực tiếp là vấn đề bảo mật.</p>
	####<p><strong>Giải thích</strong>\: Mặc dù Kubernetes đã hỗ trợ Docker gốc trong nhiều năm, kể từ Kubernetes 1.20, quá trình phản đối hỗ trợ Docker một cách rõ ràng đang diễn ra mạnh mẽ, và cuối cùng, bản thân Kubernetes sẽ không có bất kỳ kiến thức nào về bất kỳ container runtime nào. Thay vào đó, nó dựa vào CRI.</p>
}

// question: 3.18  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Khi một Pod được Kubernetes tạo, tệp /etc/resolv.conf được sử dụng để làm gì?</p>{
	~[moodle]Để lưu trữ nhật ký (logs) của Pod.#<p>Nhật ký thường được ghi vào stdout/stderr hoặc các volume chuyên dụng.</p>
	~[moodle]Để định cấu hình cài đặt tường lửa của Pod.#<p>iptables cấu hình tường lửa.</p>
	=[moodle]Để thực hiện tra cứu DNS cho Pod bằng cách định nghĩa các máy chủ DNS.
	~[moodle]Để xác định các giới hạn tài nguyên CPU và bộ nhớ của Pod.#<p>cgroups và resources stanza định nghĩa giới hạn tài nguyên.</p>
	####<p><strong>Giải thích</strong>\: Khi một Pod được tạo, nhiều tệp cũng được tạo động. Một trong những tệp đó là /etc/resolv.conf. Nó được ngăn xếp mạng Linux sử dụng để thực hiện tra cứu DNS vì tệp này định nghĩa các máy chủ DNS.</p>
}

// question: 3.19  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều gì là lý do chính khiến việc quản lý hàng trăm hoặc hàng nghìn tiến trình mà không có công cụ hạ tầng bổ sung (extra infrastructure tooling) trở nên không bền vững?</p>{
	~[moodle]Các tiến trình sẽ tự động xung đột với nhau và ngừng hoạt động.#<p>Xung đột có thể xảy ra nhưng công cụ là để quản lý việc cấu hình và theo dõi.</p>
	=[moodle]Khó khăn trong việc xác định các loại lưu trữ và báo cáo lỗi đính kèm.
	~[moodle]Tiêu thụ CPU và bộ nhớ quá mức của các tiến trình cá nhân.#<p>Mặc dù tiêu thụ tài nguyên là một vấn đề, việc quản lý cấu hình và lỗi là một thách thức lớn hơn ở quy mô lớn.</p>
	~[moodle]Không thể sao lưu dữ liệu cho các tiến trình đó.#<p>Sao lưu là một phần của lưu trữ, nhưng việc quản lý các loại lưu trữ khác nhau là thách thức chính.</p>
	####<p><strong>Giải thích</strong>\: Nếu chúng ta muốn định kỳ thay đổi cách NAS này được mount? Trong ví dụ trước của chúng ta, điều này có nghĩa là sửa đổi các lệnh shell của chúng ta và thay đổi cách chúng ta mount các volume, từng cái một. Làm điều này cho hàng trăm hoặc hàng nghìn tiến trình mà không có công cụ hạ tầng bổ sung để tự động hóa quá trình sẽ không bền vững vì những lý do rõ ràng. Tuy nhiên, ngay cả với các công cụ như vậy, chúng ta sẽ cần một cách để định nghĩa các loại lưu trữ này và báo cáo nếu các đính kèm vào các volume lưu trữ được mount này đang thất bại.</p>
}

// question: 3.20  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Khi một Pod chuyển từ trạng thái Pending sang ContainerCreating, điều gì đang xảy ra?</p>{
	~[moodle]Pod đang chờ được gán một địa chỉ IP.#<p>Địa chỉ IP được gán trong quá trình ContainerCreating thông qua CNI.</p>
	=[moodle]Kubelet đang thiết lập các cgroups và mounts cho Pod.
	~[moodle]Pod đang chờ các container runtime kéo hình ảnh ứng dụng.#<p>Kéo hình ảnh cũng là một phần của quá trình này, nhưng ContainerCreating tập trung vào thiết lập tài nguyên.</p>
	~[moodle]Scheduler đang tìm một node thích hợp để đặt Pod.#<p>Scheduler làm điều này trong trạng thái Pending trước đó.</p>
	####<p><strong>Giải thích</strong>\: Như bạn đã biết, trạng thái ContainerCreating chỉ đơn giản là trạng thái trong đó cgroups và mount được kubelet thiết lập cho một Pod trước khi nó vào trạng thái Running.</p>
}

// question: 3.21  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Làm thế nào để các tệp Linux trở nên "composable" (có thể kết hợp được)?</p>{
	~[moodle]Bằng cách luôn yêu cầu quyền root để thao tác với chúng.#<p>Quyền root là về đặc quyền, không phải tính kết hợp.</p>
	=[moodle]Bằng cách sử dụng các lệnh như pipe (|) để chuyển đầu ra từ một lệnh sang lệnh khác làm đầu vào.
	~[moodle]Bằng cách lưu trữ chúng ở một vị trí tập trung trên mạng.#<p>Vị trí lưu trữ không liên quan đến tính kết hợp của lệnh.</p>
	~[moodle]Bằng cách giới hạn kích thước của mỗi tệp.#<p>Kích thước tệp không ảnh hưởng đến tính kết hợp.</p>
	####<p><strong>Giải thích</strong>\: Kết hợp các khái niệm trước đây về tệp và quản lý tài nguyên, chúng ta đến với điểm quan trọng nhất về các nguyên thủy Linux: chúng có thể kết hợp thành các hành động cấp cao hơn. Sử dụng một pipe (|), chúng ta có thể lấy đầu ra từ một lệnh và xử lý nó trong một lệnh khác.</p>
}

// question: 3.22  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Để chạy kubectl trên một máy Windows, bạn có thể thực hiện điều này như thế nào?</p>{
	~[moodle]Chỉ có thể chạy kubectl trên các cluster từ xa trong đám mây.#<p>Đây là một mô tả không đầy đủ về khả năng của kubectl trên Windows.</p>
	~[moodle]Cần phải cài đặt một máy ảo Linux đầy đủ trên Windows.#<p>Đây là một mô tả không đầy đủ về khả năng của kubectl trên Windows.</p>
	=[moodle]Có thể chạy kubectl như một tệp thực thi Windows hoặc bên trong Windows Subsystem for Linux (WSL 2).
	~[moodle]kubectl không hỗ trợ hệ điều hành Windows.#<p>Đây là một mô tả không chính xác về khả năng của kubectl trên Windows.</p>
	####<p><strong>Giải thích</strong>\: kind có thể cài đặt dưới dạng tệp thực thi Windows. Chúng tôi khuyến khích bạn xem https://kind.sigs.k8s.io/docs/user/quick-start/. Nó thậm chí còn có các lệnh cài đặt Choco mà bạn có thể chạy. Nếu bạn là người dùng Windows, bạn có thể chạy tất cả các lệnh trong cuốn sách này bên trong Windows Subsystem for Linux (WSL 2), đó là một máy ảo Linux nhẹ có thể chạy dễ dàng trên bất kỳ máy Windows nào. Bạn cũng có thể chạy kubectl dưới dạng tệp thực thi Windows để kết nối với một cluster từ xa trên bất kỳ đám mây nào.</p>
}

// question: 3.23  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Khi một ứng dụng Pod được triển khai, những điều gì thường được xuất bản (published) để các thành phần khác của Kubernetes có thể sử dụng?</p>{
	~[moodle]Chỉ địa chỉ IP của Pod.#<p>Chỉ địa chỉ IP là không đủ.</p>
	=[moodle]Metadata về Pods (chẳng hạn như nhãn), logic khởi động lại, và đảm bảo về khả năng tiếp cận địa chỉ IP.
	~[moodle]Mã nguồn đầy đủ của ứng dụng bên trong Pod.#<p>Mã nguồn không được xuất bản như metadata.</p>
	~[moodle]Các tài nguyên phần cứng vật lý mà Pod đang sử dụng.#<p>Tài nguyên vật lý là trên node, không phải của Pod.</p>
	####<p><strong>Giải thích</strong>\: Để cho phép các hoạt động này, chúng ta cần metadata về Pods được xuất bản đến các phần khác của Kubernetes (đây là công việc của API Server), và chúng ta cần liên tục giám sát trạng thái của chúng (công việc của kubelet) để trạng thái này được cập nhật và điền vào theo thời gian. Pods, do đó, có nhiều hơn một lệnh container và một hình ảnh Docker. Chúng có nhãn và các thông số kỹ thuật được xác định rõ ràng về cách trạng thái của chúng được xuất bản, để chúng có thể được tạo lại nhanh chóng cùng với một dàn các chức năng do kubelet cung cấp. Điều này đảm bảo rằng các địa chỉ IP và quy tắc DNS luôn được cập nhật.</p>
}

// question: 3.24  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>kube-dns Pod điển hình gửi lưu lượng truy cập đến cổng nào?</p>{
	~[moodle]Cổng 80 (HTTP).#<p>Các cổng này dùng cho các dịch vụ khác.</p>
	~[moodle]Cổng 443 (HTTPS).#<p>Các cổng này dùng cho các dịch vụ khác.</p>
	=[moodle]Cổng 53 (DNS).
	~[moodle]Cổng 22 (SSH).#<p>Các cổng này dùng cho các dịch vụ khác.</p>
	####<p><strong>Giải thích</strong>\: kube-dns Pod gửi lưu lượng truy cập đến cổng 53, cổng này được biết đến rộng rãi là tiêu chuẩn cổng DNS.</p>
}

// question: 3.25  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều gì không phải là một trong những loại vấn đề mà "extra infrastructure tooling" sẽ giải quyết cho hàng trăm hoặc hàng nghìn tiến trình trong môi trường sản xuất?</p>{
	~[moodle]Các vấn đề về lưu trữ (StorageClasses, PersistentVolumes, PersistentVolumeClaims).#<p>Đây là một vấn đề mà các công cụ hạ tầng giải quyết.</p>
	~[moodle]Các vấn đề về lập lịch (matching cgroup requirements).#<p>Đây là một vấn đề mà các công cụ hạ tầng giải quyết.</p>
	~[moodle]Các vấn đề về khởi động lại (graceful upgrades).#<p>Đây là một vấn đề mà các công cụ hạ tầng giải quyết.</p>
	=[moodle]Các vấn đề về hiệu suất của một ứng dụng duy nhất do mã lỗi (buggy code).
	####<p><strong>Giải thích</strong>\: Các công cụ hạ tầng giải quyết các vấn đề liên quan đến quản lý quy mô lớn của lưu trữ, lập lịch và khởi động lại. Chúng không trực tiếp giải quyết các vấn đề về hiệu suất do mã lỗi của một ứng dụng duy nhất.</p>
}

// question: 3.26  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Trong luồng làm việc của iptables và kube-proxy, KUBE-SEP rules (quy tắc) được sử dụng để làm gì?</p>{
	~[moodle]Để tạo các bản ghi DNS cho Pod.#<p>kube-dns và CoreDNS tạo bản ghi DNS.</p>
	=[moodle]Để định tuyến lưu lượng truy cập từ một dịch vụ đến các điểm cuối Pod cụ thể.
	~[moodle]Để mã hóa lưu lượng mạng giữa các node.#<p>Mã hóa thường được thực hiện ở lớp cao hơn.</p>
	~[moodle]Để giám sát trạng thái sức khỏe của các container.#<p>Kubelet giám sát trạng thái sức khỏe.</p>
	####<p><strong>Giải thích</strong>\: Khi lưu lượng truy cập từ một dịch vụ được nhận, nó được định tuyến bằng cách sử dụng các quy tắc KUBE-SEP. Các Pod này truy cập internet bên ngoài hoặc nhận lưu lượng truy cập. Nếu một trong những Pod này trở nên không lành mạnh, thì quy tắc cụ thể cho KUBE-SEP-IT2Z sẽ được proxy mạng, kube-proxy, điều hòa để lưu lượng truy cập chỉ chuyển tiếp đến các bản sao lành mạnh của Pod DNS của chúng ta.</p>
}

// question: 3.27  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều nào sau đây KHÔNG đúng về Docker trong ngữ cảnh Kubernetes hiện tại?</p>{
	~[moodle]containerd là một triển khai phổ biến của CRI mà Docker sử dụng bên dưới.#<p>Đây là một tuyên bố đúng về Docker và Kubernetes.</p>
	~[moodle]Kubernetes đã chuyển sang sử dụng CRI để trừu tượng hóa container runtime.#<p>Đây là một tuyên bố đúng về Docker và Kubernetes.</p>
	=[moodle]Docker được khuyến nghị là container runtime mặc định cho các cluster Kubernetes sản xuất.
	~[moodle]Kubernetes 1.20 đã bắt đầu quá trình phản đối hỗ trợ Docker một cách rõ ràng.#<p>Đây là một tuyên bố đúng về Docker và Kubernetes.</p>
	####<p><strong>Giải thích</strong>\: Mặc dù Kubernetes đã hỗ trợ Docker gốc trong nhiều năm, kể từ Kubernetes 1.20, quá trình phản đối hỗ trợ Docker một cách rõ ràng đang diễn ra mạnh mẽ, và cuối cùng, bản thân Kubernetes sẽ không có bất kỳ kiến thức nào về bất kỳ container runtime nào. Modern Kubernetes clusters không thường chạy Docker làm container runtime cho Linux vì nhiều lý do. Docker rất tốt cho các nhà phát triển để chạy Kubernetes, nhưng các trung tâm dữ liệu yêu cầu một giải pháp container runtime nhẹ hơn, tích hợp sâu hơn với OS.</p>
}

// question: 3.28  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Khi tạo một Pod đơn giản bằng kubectl create -f pod.yaml, trường kind trong định nghĩa Pod dùng để làm gì?</p>{
	~[moodle]Để đặt tên cho Pod.#<p>metadata.name đặt tên cho Pod.</p>
	=[moodle]Để cho API server biết loại đối tượng API mà nó là.
	~[moodle]Để chỉ định hình ảnh container mà Pod sẽ sử dụng.#<p>spec.containers[].image chỉ định hình ảnh.</p>
	~[moodle]Để định nghĩa các nhãn (labels) cho Pod.#<p>metadata.labels định nghĩa nhãn.</p>
	####<p><strong>Giải thích</strong>\: Không nên nhầm lẫn với công cụ kind mà chúng ta đã sử dụng để tạo cluster này, trường kind API trong định nghĩa Pod của chúng ta cho API server biết loại đối tượng API mà nó là khi chúng ta tạo Pod này.</p>
}

// question: 3.29  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>Điều nào sau đây KHÔNG phải là một trạng thái trong vòng đời của Pod được nhắc đến trong nguồn?</p>{
	~[moodle]Pending.#<p>Đây là một trạng thái của Pod được nhắc đến.</p>
	=[moodle]Starting.
	~[moodle]ContainerCreating.#<p>Đây là một trạng thái của Pod được nhắc đến.</p>
	~[moodle]Running.#<p>Đây là một trạng thái của Pod được nhắc đến.</p>
	####<p><strong>Giải thích</strong>\: Các trạng thái của Pod bao gồm Pending, ContainerCreating, và Running. Starting không phải là một trạng thái riêng biệt mà là một phần của quá trình ContainerCreating.</p>
}

// question: 3.30  name: Chapter 3: Let’s build a Pod
::Chapter 3\: Let’s build a Pod::[html]<p>socat command có vai trò gì trong các nguyên thủy Linux mà Kubernetes dựa vào?</p>{
	~[moodle]Tắt bộ nhớ swap.#<p>swapoff tắt bộ nhớ swap.</p>
	=[moodle]Thiết lập một luồng thông tin hai chiều giữa các tiến trình.
	~[moodle]Giới hạn tài nguyên CPU của một tiến trình.#<p>cgroups giới hạn tài nguyên CPU.</p>
	~[moodle]Liệt kê các tiến trình đang chạy.#<p>ps liệt kê các tiến trình đang chạy.</p>
	####<p><strong>Giải thích</strong>\: socat là một lệnh cho phép bạn thiết lập một luồng thông tin hai chiều giữa các tiến trình; socat là một phần thiết yếu của cách lệnh kubectl port-forward hoạt động.</p>
}