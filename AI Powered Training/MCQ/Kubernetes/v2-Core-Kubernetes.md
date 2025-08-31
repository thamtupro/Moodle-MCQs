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

// Chapter 4: Using cgroups for processes in our Pods
// question: 4 name: Switch category to $module$/top/Chapter 4: Using cgroups for processes in our Pods
$CATEGORY: $module$/top/Chapter 4: Using cgroups for processes in our Pods

// question: 4.1 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Vai trò chính của cgroup trong Linux là gì?</p>{
	~[moodle]Tạo một bản sao đầy đủ của hệ điều hành cho mỗi ứng dụng.#<p>Tạo bản sao hệ điều hành là chức năng kết hợp của cgroup và namespace, không phải riêng cgroup.</p>
	~[moodle]Định nghĩa các tài nguyên mà một tiến trình có thể truy cập trên hệ thống.#<p>Chức năng này thuộc về namespace, không phải cgroup.</p>
	~[moodle]Đảm bảo giao tiếp mạng an toàn giữa các tiến trình.#<p>cgroup không trực tiếp liên quan đến bảo mật mạng.</p>
	=[moodle]Quản lý việc phân bổ và cô lập tài nguyên cho các tiến trình.
	####<p><strong>Giải thích</strong>\: cgroup (control group) cho phép hệ điều hành định nghĩa các nhóm tài nguyên được phân bổ và cô lập một cách phân cấp cho các tiến trình.</p>
}

// question: 4.2 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Điều gì xảy ra với một Pod của Kubernetes cho đến khi container pause được thêm vào namespace của nó?</p>{
	~[moodle]Ứng dụng trong Pod bắt đầu xử lý yêu cầu ngay lập tức.#<p>Ứng dụng chỉ bắt đầu sau khi container pause được thêm và các công việc chuẩn bị hoàn tất.</p>
	=[moodle]Pod vẫn ở trạng thái nhàn rỗi và chờ đợi công việc chuẩn bị hoàn tất.
	~[moodle]Hệ thống tự động gán một IP công cộng cho Pod.#<p>Việc gán IP diễn ra trong quá trình thiết lập mạng, sau khi container pause được tạo.</p>
	~[moodle]Kubelet không thực hiện bất kỳ công việc nào liên quan đến Pod.#<p>Kubelet chịu trách nhiệm thực hiện các bước chuẩn bị này.</p>
	####<p><strong>Giải thích</strong>\: Ứng dụng của chúng ta ở trạng thái nhàn rỗi cho đến khi container pause được thêm vào namespace của nó.</p>
}

// question: 4.3 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Tại sao các cgroup lại quan trọng đối với Pod trong một cụm Kubernetes quy mô lớn?</p>{
	~[moodle]Chúng giúp giảm số lượng node cần thiết trong cụm.#<p>Chúng giúp tăng mật độ Pod trên mỗi node, gián tiếp giảm số lượng node, nhưng mục đích chính là hiệu quả sử dụng tài nguyên.</p>
	~[moodle]Chúng đảm bảo mỗi Pod có toàn quyền truy cập vào tất cả tài nguyên hệ thống.#<p>Ngược lại, cgroup được dùng để giới hạn và phân chia tài nguyên, không phải cấp toàn quyền truy cập.</p>
	=[moodle]Chúng cho phép cô lập tài nguyên và tăng hiệu quả sử dụng trung tâm dữ liệu.
	~[moodle]Chúng đơn giản hóa việc quản lý cấu hình mạng cho các Pod.#<p>Việc đơn giản hóa quản lý mạng thuộc về CNI và kube-proxy.</p>
	####<p><strong>Giải thích</strong>\: cgroup cho phép định nghĩa các nhóm tài nguyên được cô lập, giúp cô lập CPU, bộ nhớ và các tài nguyên OS khác, từ đó tăng cường hiệu quả sử dụng trung tâm dữ liệu.</p>
}

// question: 4.4 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Thành phần nào của Kubernetes chịu trách nhiệm tạo namespace và cgroup cho một container?</p>{
	~[moodle]API server.#<p>API server lưu trữ trạng thái mong muốn của cụm.</p>
	~[moodle]kube-scheduler.#<p>kube-scheduler quyết định Pod sẽ chạy trên node nào.</p>
	=[moodle]container pause.
	~[moodle]kube-controller-manager.#<p>kube-controller-manager chạy các vòng điều khiển khác.</p>
	####<p><strong>Giải thích</strong>\: Container pause (container tạm dừng) là một trình giữ chỗ mà kubelet sử dụng để tạo namespace và cgroup cho một container.</p>
}

// question: 4.5 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Khi một Pod yêu cầu tài nguyên CPU hoặc bộ nhớ, cgroup tương ứng được định nghĩa ở đâu trong hệ thống Linux?</p>{
	~[moodle]/etc/kubernetes/manifests.#<p>Đây là nơi lưu trữ các manifest tĩnh cho các thành phần của mặt phẳng điều khiển.</p>
	~[moodle]/proc/<PID>/cgroup.#<p>Tệp này chứa thông tin về các cgroup mà một tiến trình cụ thể thuộc về.</p>
	=[moodle]/sys/fs/cgroup.
	~[moodle]/var/lib/kubelet/config.yaml.#<p>Đây là tệp cấu hình của kubelet.</p>
	####<p><strong>Giải thích</strong>\: Các cgroup được định nghĩa dưới thư mục /sys/fs/cgroup và kernel thực thi các quy tắc cgroup.</p>
}

// question: 4.6 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Thuật ngữ "Mirror Pod" trong Kubernetes có nghĩa là gì?</p>{
	~[moodle]Một Pod được chạy đồng thời trên nhiều node.#<p>Đây là chức năng của ReplicaSet hoặc DaemonSet.</p>
	=[moodle]Một Pod được tạo và quản lý bởi kubelet trên cơ sở độc lập.
	~[moodle]Một Pod phản chiếu cấu hình của một Pod khác để cân bằng tải.#<p>Không phải là Pod phản chiếu cấu hình để cân bằng tải.</p>
	~[moodle]Một Pod dùng để giám sát các Pod khác trong cụm.#<p>Pod dùng để giám sát thường là các công cụ như Prometheus.</p>
	####<p><strong>Giải thích</strong>\: Mirror Pod được tạo và quản lý bởi một kubelet trên cơ sở độc lập, cho phép kubelet tự khởi động toàn bộ cụm Kubernetes chạy bên trong Pod.</p>
}

// question: 4.7 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Loại QoS class nào được gán cho một Pod có cả CPU và memory requests, nhưng không có limits?</p>{
	~[moodle]Guaranteed (Đảm bảo).#<p>Guaranteed Pod có cả yêu cầu và giới hạn tài nguyên giống hệt nhau.</p>
	=[moodle]Burstable (Có thể tăng tốc).
	~[moodle]BestEffort (Nỗ lực tối đa).#<p>BestEffort Pod không có bất kỳ yêu cầu hoặc giới hạn tài nguyên nào.</p>
	~[moodle]Critical (Quan trọng).#<p>Critical không phải là một QoS class chính thức.</p>
	####<p><strong>Giải thích</strong>\: Pod Burstable là những Pod có cả yêu cầu CPU và bộ nhớ, nhưng không có giới hạn tài nguyên.</p>
}

// question: 4.8 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Tại sao Kubernetes không hỗ trợ sử dụng swap trong hầu hết các cấu hình?</p>{
	~[moodle]Để đơn giản hóa việc triển khai mạng.#<p>Không liên quan trực tiếp đến việc triển khai mạng.</p>
	=[moodle]Để đảm bảo hiệu suất truy cập bộ nhớ được đảm bảo.
	~[moodle]Vì swap chỉ hữu ích cho các ứng dụng chạy trên Windows.#<p>Swap là tính năng của hệ điều hành, không chỉ dành cho Windows.</p>
	~[moodle]Vì việc sử dụng swap làm tăng chi phí quản lý.#<p>Mặc dù có thể ảnh hưởng đến chi phí, lý do chính là để đảm bảo hiệu suất và độ tin cậy.</p>
	####<p><strong>Giải thích</strong>\: Việc vô hiệu hóa swap trong Kubernetes giúp đảm bảo hiệu suất truy cập bộ nhớ, đặc biệt đối với các QoS class Guaranteed.</p>
}

// question: 4.9 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Đơn vị đo lường CPU cơ bản mà Kubernetes sử dụng là gì?</p>{
	=[moodle]Một hyperthread trên phần cứng trần hoặc một core/vCPU trên đám mây.
	~[moodle]Một megahertz (MHz) của bộ xử lý.#<p>Megahertz là đơn vị đo tốc độ đồng hồ, không phải đơn vị phân bổ CPU của Kubernetes.</p>
	~[moodle]Một tỷ lệ phần trăm cố định của tổng CPU.#<p>Tỷ lệ phần trăm có thể được biểu thị (ví dụ: 0.25 CPU) nhưng đơn vị cơ bản là 1.</p>
	~[moodle]Một đơn vị riêng biệt được định nghĩa bởi CRI.#<p>CRI (Container Runtime Interface) không định nghĩa đơn vị CPU.</p>
	####<p><strong>Giải thích</strong>\: Đơn vị cơ bản mà Kubernetes sử dụng để đo CPU là 1, tương đương với một hyperthread trên phần cứng trần hoặc một core/vCPU trên đám mây.</p>
}

// question: 4.10 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Loại metrics nào trong Prometheus được sử dụng để theo dõi các giá trị thay đổi liên tục theo thời gian, như số lượng yêu cầu mỗi giây?</p>{
	~[moodle]Histograms (Biểu đồ tần suất).#<p>Histograms hiển thị các khoảng thời gian cho các loại sự kiện khác nhau.</p>
	=[moodle]Gauges (Đồng hồ đo).
	~[moodle]Counters (Bộ đếm).#<p>Counters chỉ định các số đếm sự kiện tăng liên tục.</p>
	~[moodle]Summaries (Tóm tắt).#<p>Summaries không phải là một loại metrics chính thức trong danh sách được cung cấp.</p>
	####<p><strong>Giải thích</strong>\: Gauges chỉ ra số lượng yêu cầu bạn nhận được mỗi giây tại bất kỳ thời điểm nào, nó tăng và giảm theo định kỳ.</p>
}

// question: 4.11 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Chức năng chính của cAdvisor trong hệ thống giám sát Kubernetes là gì?</p>{
	~[moodle]Cung cấp giao diện người dùng đồ họa cho Prometheus.#<p>Grafana thường cung cấp GUI cho Prometheus.</p>
	=[moodle]Thu thập dữ liệu định lượng về việc sử dụng cgroup.
	~[moodle]Quản lý việc triển khai và mở rộng quy mô của Prometheus.#<p>Prometheus quản lý việc thu thập và lưu trữ metrics.</p>
	~[moodle]Tạo các rule mạng cho giao tiếp giữa các Pod.#<p>Kube-proxy và CNI provider tạo rule mạng.</p>
	####<p><strong>Giải thích</strong>\: Kubelet sử dụng thư viện cAdvisor để giám sát cgroup và thu thập dữ liệu định lượng về chúng, ví dụ: lượng CPU và bộ nhớ mà một Pod cụ thể sử dụng.</p>
}

// question: 4.12 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Loại QoS class nào của Pod không có bất kỳ yêu cầu hoặc giới hạn tài nguyên nào?</p>{
	~[moodle]Guaranteed (Đảm bảo).#<p>Guaranteed Pod có yêu cầu và giới hạn CPU/bộ nhớ giống hệt nhau.</p>
	~[moodle]Burstable (Có thể tăng tốc).#<p>Burstable Pod có yêu cầu nhưng không có giới hạn, hoặc yêu cầu khác giới hạn.</p>
	=[moodle]BestEffort (Nỗ lực tối đa).
	~[moodle]Standard (Tiêu chuẩn).#<p>Standard không phải là một QoS class chính thức của Kubernetes.</p>
	####<p><strong>Giải thích</strong>\: BestEffort là lớp QoS mà các Pod không có bất kỳ yêu cầu hoặc giới hạn tài nguyên nào.</p>
}

// question: 4.13 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Mục đích chính của việc tắt Transparent HugePages là gì?</p>{
	~[moodle]Để tăng hiệu suất mạng cho các Pod.#<p>Tắt Transparent HugePages không liên quan trực tiếp đến hiệu suất mạng.</p>
	~[moodle]Để giảm mức tiêu thụ bộ nhớ tổng thể của node.#<p>HugePages được dùng để tối ưu hóa việc sử dụng bộ nhớ cho các ứng dụng lớn, không phải để giảm mức tiêu thụ tổng thể.</p>
	~[moodle]Để có thể thay đổi cấu hình HugePages thông qua Pod specification.#<p>Có thể cấu hình HugePages thông qua init containers, nhưng mục đích chính của việc tắt Transparent HugePages là hiệu suất.</p>
	=[moodle]Để cải thiện hiệu suất cho các hệ điều hành cụ thể.
	####<p><strong>Giải thích</strong>\: Việc tắt Transparent HugePages có thể tạo ra sự khác biệt về hiệu suất trên các hệ điều hành cụ thể.</p>
}

// question: 4.14 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Khi kiểm tra cgroup của một tiến trình, thư mục "burstable" trong đường dẫn cgroup của Kubernetes ám chỉ điều gì?</p>{
	~[moodle]Pod đó là một Pod quan trọng của hệ thống.#<p>Không phải là chỉ báo về Pod quan trọng của hệ thống.</p>
	=[moodle]Pod đó có thể sử dụng một lượng lớn CPU khi cần.
	~[moodle]Pod đó có giới hạn sử dụng tài nguyên cứng.#<p>Ngược lại, Burstable Pod thường không có giới hạn sử dụng cứng.</p>
	~[moodle]Pod đó đang chạy trên một node đặc biệt được tối ưu hóa.#<p>Nó liên quan đến cách tài nguyên được phân bổ, không phải loại node.</p>
	####<p><strong>Giải thích</strong>\: Thư mục "burstable" (có thể tăng tốc) định nghĩa một QoS class đặc biệt cho Kubernetes, nơi Pod có khả năng sử dụng các burst CPU lớn khi cần thiết (ví dụ: scheduler khi cần lên lịch cho nhiều Pod nhanh chóng).</p>
}

// question: 4.15 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Loại metrics nào của Prometheus thường được sử dụng để theo dõi các sự kiện tăng liên tục theo thời gian, như tổng số yêu cầu đã nhận?</p>{
	~[moodle]Gauges (Đồng hồ đo).#<p>Gauges biểu thị một giá trị có thể tăng hoặc giảm.</p>
	~[moodle]Histograms (Biểu đồ tần suất).#<p>Histograms hiển thị phân phối các giá trị theo các khoảng.</p>
	=[moodle]Counters (Bộ đếm).
	~[moodle]Logs (Nhật ký).#<p>Logs là nhật ký văn bản, không phải loại metrics của Prometheus.</p>
	####<p><strong>Giải thích</strong>\: Counters chỉ định các số đếm sự kiện tăng liên tục, ví dụ: tổng số yêu cầu bạn đã thấy.</p>
}

// question: 4.16 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Lệnh nào của Linux được sử dụng để hiển thị mối quan hệ cha-con của các tiến trình trong một hệ thống?</p>{
	~[moodle]ps -ax.#<p>ps -ax liệt kê tất cả các tiến trình.</p>
	~[moodle]grep.#<p>grep dùng để lọc kết quả.</p>
	=[moodle]pstree.
	~[moodle]systemctl status.#<p>systemctl status hiển thị trạng thái của các dịch vụ systemd.</p>
	####<p><strong>Giải thích</strong>\: Lệnh pstree được dùng để điều tra mối quan hệ cha-con của các tiến trình trong cụm kind.</p>
}

// question: 4.17 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Các tham số --system-reserved và --kubelet-reserved trong kubelet dùng để làm gì?</p>{
	~[moodle]Định nghĩa các yêu cầu tài nguyên tối thiểu cho các Pod ứng dụng.#<p>Các tham số này dành cho tài nguyên hệ thống và kubelet, không phải Pod ứng dụng.</p>
	=[moodle]Tính toán lượng tài nguyên cgroup khả dụng để phân bổ cho Pod.
	~[moodle]Chỉ định lượng tài nguyên mà Prometheus cần để giám sát.#<p>Không liên quan đến Prometheus.</p>
	~[moodle]Đặt giới hạn cứng cho số lượng Pod có thể chạy trên một node.#<p>Giới hạn số Pod được điều chỉnh bằng tham số khác.</p>
	####<p><strong>Giải thích</strong>\: Kubelet tính toán lượng tài nguyên cgroup khả dụng để phân bổ cho Pod bằng cách xác định tổng dung lượng trên node, sau đó trừ đi lượng băng thông CPU cần thiết cho chính nó và cho node bên dưới, được điều chỉnh bằng các tham số --system-reserved và --kubelet-reserved.</p>
}

// question: 4.18 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Khi nào một Pod được coi là "Guaranteed" (Đảm bảo) về QoS class?</p>{
	~[moodle]Khi nó chỉ có CPU requests.#<p>Đây là trường hợp của Burstable hoặc BestEffort.</p>
	~[moodle]Khi nó có cả CPU và memory requests.#<p>Đây là trường hợp của Burstable nếu không có limits.</p>
	~[moodle]Khi nó không có bất kỳ resource requests nào.#<p>Đây là trường hợp của BestEffort.</p>
	=[moodle]Khi nó có CPU và memory requests giống hệt với limits.
	####<p><strong>Giải thích</strong>\: Pod Guaranteed là những Pod có yêu cầu và giới hạn CPU và bộ nhớ giống hệt nhau.</p>
}

// question: 4.19 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Các HugePages là gì và mục đích của chúng trong Kubernetes?</p>{
	~[moodle]Một loại cgroup đặc biệt để quản lý tài nguyên mạng.#<p>HugePages liên quan đến bộ nhớ, không phải mạng.</p>
	=[moodle]Các trang bộ nhớ lớn hơn kích thước trang bộ nhớ mặc định của kernel Linux.
	~[moodle]Một cơ chế lưu trữ bền vững cho dữ liệu của Pod.#<p>Không phải cơ chế lưu trữ bền vững.</p>
	~[moodle]Một kỹ thuật để tăng cường bảo mật cho các container.#<p>Không phải tính năng bảo mật container.</p>
	####<p><strong>Giải thích</strong>\: HugePages là một khái niệm cho phép Pod truy cập các trang bộ nhớ lớn hơn kích thước trang bộ nhớ mặc định của kernel Linux (thường là 4 KB).</p>
}

// question: 4.20 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Điều gì sẽ xảy ra nếu một tiến trình vượt quá giới hạn bộ nhớ cứng (hard memory limits) của nó trong Kubernetes?</p>{
	~[moodle]Tiến trình sẽ được chuyển sang swap space.#<p>Kubernetes thường không cho phép sử dụng swap.</p>
	=[moodle]Tiến trình sẽ bị giết (killed).
	~[moodle]Tiến trình sẽ bị tạm dừng cho đến khi có đủ bộ nhớ.#<p>Tiến trình sẽ bị giết thay vì tạm dừng.</p>
	~[moodle]Tiến trình sẽ nhận được thêm bộ nhớ từ hệ thống.#<p>Giới hạn cứng sẽ ngăn điều này xảy ra.</p>
	####<p><strong>Giải thích</strong>\: Một tiến trình có giới hạn bộ nhớ cứng sẽ bị giết nếu nó vượt quá giới hạn bộ nhớ của mình trong một thời gian dài. Kubernetes sẽ trả về một exit code và trạng thái OOMKilled.</p>
}

// question: 4.21 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Trong kiến trúc Linux, đâu là thành phần là cha của tất cả các cgroup?</p>{
	~[moodle]/docker cgroup.#<p>Docker cgroup là con của / cgroup.</p>
	~[moodle]/systemd cgroup.#<p>systemd cgroup cũng là con của / cgroup.</p>
	=[moodle]/ cgroup.
	~[moodle]/kubepods cgroup.#<p>kubepods là một phần của phân vùng cgroup mà Kubernetes dành cho Pod của nó.</p>
	####<p><strong>Giải thích</strong>\: Trên một máy Linux tiêu chuẩn hoặc trong một node cụm kind, gốc của tất cả các cgroup là / cgroup được tạo khi khởi động.</p>
}

// question: 4.22 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Để cấu hình một init container chỉnh sửa HugePages, cần có những điều kiện nào?</p>{
	~[moodle]Init container phải chạy ở chế độ không đặc quyền (unprivileged mode).#<p>Cần chạy ở chế độ đặc quyền.</p>
	=[moodle]Init container phải mount thư mục /sys bằng kiểu volume hostPath.
	~[moodle]Init container phải chạy trước khi Pod chính bắt đầu.#<p>Init container luôn chạy trước Pod chính, nhưng đây không phải là điều kiện duy nhất để chỉnh sửa HugePages.</p>
	~[moodle]Init container không được phép thực thi các lệnh Linux.#<p>Init container cần thực thi các lệnh Linux để chỉnh sửa.</p>
	####<p><strong>Giải thích</strong>\: Cấu hình HugePages có thể được thực hiện trong init container nếu nó chạy ở chế độ đặc quyền và mount thư mục /sys bằng kiểu volume hostPath.</p>
}

// question: 4.23 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Metrics "etcd_request_duration_seconds_bucket" trong Prometheus được sử dụng để theo dõi điều gì?</p>{
	~[moodle]Tổng số yêu cầu etcd.#<p>Nó đo lường thời gian, không phải tổng số.</p>
	=[moodle]Thời gian thực hiện các yêu cầu etcd, được chia thành các bucket.
	~[moodle]Tần suất các yêu cầu etcd.#<p>Không phải tần suất.</p>
	~[moodle]Kích thước dữ liệu được ghi vào etcd.#<p>Không phải kích thước dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: Metrics này cho biết thời gian các lệnh ghi vào etcd (disk) đang diễn ra, được chia thành các bucket (là một histogram).</p>
}

// question: 4.24 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Trong ngữ cảnh của kubelet, cấu trúc dữ liệu "allocatable" biểu thị điều gì?</p>{
	~[moodle]Tổng dung lượng tài nguyên mà node có.#<p>"allocatable" là một phần của tổng dung lượng, sau khi đã trừ đi các tài nguyên dự trữ.</p>
	=[moodle]Lượng tài nguyên cgroup khả dụng để phân bổ cho các Pod.
	~[moodle]Lượng tài nguyên đang được các Pod sử dụng.#<p>Đây là trạng thái sử dụng thực tế, không phải giá trị "allocatable".</p>
	~[moodle]Lượng tài nguyên mà kubelet tự động dự trữ cho chính nó.#<p>Lượng dự trữ cho kubelet được trừ khỏi tổng dung lượng để ra "allocatable".</p>
	####<p><strong>Giải thích</strong>\: "allocatable" là lượng ngân sách cgroup có sẵn để phân bổ tài nguyên cho các Pod. Kubelet tính toán giá trị này bằng cách xác định tổng dung lượng trên node, sau đó trừ đi lượng băng thông CPU cần thiết cho chính nó và cho node bên dưới.</p>
}

// question: 4.25 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Điều gì không phải là một trong những lợi thế của việc sử dụng Prometheus để giám sát cụm Kubernetes?</p>{
	~[moodle]Có thể nhìn thấy các tiến trình ẩn không hiển thị với Kubernetes.#<p>Một lợi thế là có thể nhìn thấy các tiến trình ẩn có thể tràn cụm.</p>
	~[moodle]Trực tiếp ánh xạ tài nguyên Kubernetes với các công cụ cô lập kernel-level.#<p>Nó cho phép ánh xạ trực tiếp tài nguyên Kubernetes với các công cụ cô lập kernel-level.</p>
	=[moodle]Cung cấp khả năng tự động sửa lỗi (self-healing) cho các Pod không khỏe mạnh.
	~[moodle]Là một công cụ tuyệt vời để tìm hiểu về cách container được triển khai.#<p>Nó là một công cụ tuyệt vời để tìm hiểu thêm về cách container được triển khai ở quy mô lớn.</p>
	####<p><strong>Giải thích</strong>\: Prometheus là một hệ thống giám sát, nó thu thập và hiển thị metrics, nhưng không tự động sửa lỗi cho Pods. Kubelet và các controller khác chịu trách nhiệm tự sửa lỗi.</p>
}

// question: 4.26 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Loại metrics nào của Prometheus hiển thị các "bucket" thời gian cho các loại sự kiện khác nhau, ví dụ: bao nhiêu yêu cầu hoàn thành trong dưới 500ms?</p>{
	~[moodle]Gauges (Đồng hồ đo).#<p>Gauges hiển thị giá trị hiện tại.</p>
	=[moodle]Histograms (Biểu đồ tần suất).
	~[moodle]Counters (Bộ đếm).#<p>Counters hiển thị tổng số tăng dần.</p>
	~[moodle]Event logs (Nhật ký sự kiện).#<p>Event logs là dữ liệu thô, không phải loại metrics đã được tổng hợp.</p>
	####<p><strong>Giải thích</strong>\: Histograms hiển thị các bucket thời gian cho các loại sự kiện khác nhau (ví dụ: bao nhiêu yêu cầu hoàn thành dưới 500 ms).</p>
}

// question: 4.27 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Các init containers có thể được sử dụng để làm gì trong ngữ cảnh cấu hình tài nguyên của Pod?</p>{
	~[moodle]Chạy ứng dụng chính của Pod.#<p>Ứng dụng chính chạy trong các container chính.</p>
	=[moodle]Cấu hình các tính năng Linux cụ thể cần thiết cho Pod.
	~[moodle]Cung cấp giao diện mạng chính cho Pod.#<p>CNI cung cấp giao diện mạng.</p>
	~[moodle]Quản lý việc sao lưu dữ liệu của Pod.#<p>PV/PVC và các giải pháp lưu trữ khác quản lý sao lưu dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: init containers có thể được dùng để khởi động các tính năng Linux nhất định có thể cần thiết cho Pod chạy đúng cách.</p>
}

// question: 4.28 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Đâu không phải là một trong các QoS class được Kubernetes tự động tạo ra dựa trên cách định nghĩa một Pod?</p>{
	~[moodle]Burstable (Có thể tăng tốc).#<p>Đây là một QoS class chính thức của Kubernetes.</p>
	~[moodle]Guaranteed (Đảm bảo).#<p>Đây là một QoS class chính thức của Kubernetes.</p>
	~[moodle]BestEffort (Nỗ lực tối đa).#<p>Đây là một QoS class chính thức của Kubernetes.</p>
	=[moodle]Critical (Quan trọng).
	####<p><strong>Giải thích</strong>\: Burstable, Guaranteed, và BestEffort là ba QoS classes được Kubernetes tự động tạo tùy thuộc vào cách bạn định nghĩa một Pod. Critical không phải là một QoS class chính thức.</p>
}

// question: 4.29 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Điều gì là đúng về việc kubelet quản lý các tiến trình và luồng trong Linux?</p>{
	~[moodle]Kubelet trực tiếp tạo và quản lý tất cả các luồng của ứng dụng.#<p>Kubelet quản lý vòng đời Pod, nhưng Linux kernel quản lý các tiến trình và luồng.</p>
	=[moodle]Mọi tiến trình trong Linux có thể tạo một hoặc nhiều luồng.
	~[moodle]Kubelet bỏ qua cấu trúc luồng của Linux khi chạy Pod.#<p>Kubelet phụ thuộc vào các tính năng của Linux kernel, bao gồm cách quản lý luồng.</p>
	~[moodle]Mọi luồng trong Linux đều có PID riêng biệt và không chia sẻ tài nguyên.#<p>Các luồng chia sẻ cùng không gian bộ nhớ của tiến trình cha.</p>
	####<p><strong>Giải thích</strong>\: Mọi tiến trình trong Linux có thể tạo một hoặc nhiều luồng (thread). Một luồng thực thi là một sự trừu tượng mà các chương trình có thể sử dụng để tạo các tiến trình mới chia sẻ cùng bộ nhớ với các tiến trình khác.</p>
}

// question: 4.30 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Chức năng chính của systemd trong Linux là gì, liên quan đến các tiến trình Kubernetes?</p>{
	~[moodle]Quản lý cấu hình mạng cho các Pod.#<p>CNI và kube-proxy quản lý mạng.</p>
	~[moodle]Khởi động các container trong Pod.#<p>CRI/Container Runtime chịu trách nhiệm khởi động container.</p>
	=[moodle]Khởi động kubelet, là tiến trình cốt lõi quản lý các container.
	~[moodle]Theo dõi và ghi lại các metrics hiệu suất của cgroup.#<p>Prometheus và cAdvisor theo dõi metrics.</p>
	####<p><strong>Giải thích</strong>\: systemd (trình quản lý hệ thống và dịch vụ Linux) thường khởi động kubelet, là tiến trình cốt lõi chạy trong một cụm để quản lý tất cả các container của bạn.</p>
}

// question: 4.31 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Điều gì xảy ra khi một Pod có "soft memory limits"?</p>{
	~[moodle]Pod sẽ bị giết ngay lập tức khi vượt quá giới hạn.#<p>Đây là hành vi của "hard memory limits".</p>
	=[moodle]Pod có lượng RAM thay đổi theo thời gian tùy thuộc vào tải hệ thống.
	~[moodle]Pod sẽ được chuyển sang swap space khi cần.#<p>Kubernetes thường không sử dụng swap.</p>
	~[moodle]Giới hạn này không ảnh hưởng đến Pod.#<p>Giới hạn mềm vẫn ảnh hưởng đến việc phân bổ tài nguyên.</p>
	####<p><strong>Giải thích</strong>\: Một tiến trình có giới hạn bộ nhớ mềm (soft memory limits) có lượng RAM thay đổi theo thời gian, tùy thuộc vào tải hệ thống.</p>
}

// question: 4.32 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Các luồng trong Linux chia sẻ điều gì với tiến trình cha của chúng?</p>{
	~[moodle]Không gian PID riêng biệt.#<p>Các luồng có SPID (subprocess IDs) riêng biệt, nhưng không gian PID thường được chia sẻ trong Pod.</p>
	=[moodle]Cùng một pool tài nguyên ban đầu được cấp.
	~[moodle]Địa chỉ IP mạng riêng.#<p>Địa chỉ IP mạng thường được chia sẻ giữa các container trong cùng một Pod, không phải giữa các luồng riêng biệt.</p>
	~[moodle]Namespace file system riêng biệt.#<p>Namespaces cấp quyền truy cập tài nguyên.</p>
	####<p><strong>Giải thích</strong>\: Tất cả các luồng được tạo bởi một chương trình đều sử dụng cùng một pool tài nguyên ban đầu được cấp cho tiến trình cha.</p>
}

// question: 4.33 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Trong ngữ cảnh cgroup, tại sao thư mục docker lại đóng vai trò là thư mục cha của mọi thứ trong cụm kind?</p>{
	~[moodle]Vì kind sử dụng Docker làm container runtime chính.#<p>kind không sử dụng Docker làm container runtime chính; nó sử dụng containerd bên trong các node Docker.</p>
	=[moodle]Vì Docker tạo các node kind và chạy kubelet bên trong chúng.
	~[moodle]Vì Docker là tiến trình gốc của systemd trên cụm kind.#<p>Docker là con của systemd trong môi trường Linux thông thường, nhưng trong kind, Docker đóng vai trò là môi trường ảo.</p>
	~[moodle]Vì kubelet chỉ quản lý các cgroup do Docker tạo ra.#<p>kubelet tương tác với CRI để quản lý cgroup, không chỉ cgroup do Docker tạo.</p>
	####<p><strong>Giải thích</strong>\: Trong cụm kind, thư mục docker là cha của mọi thứ vì kind sử dụng Docker để tạo các node và sau đó cài đặt containerd làm container runtime bên trong các node đó. Vì vậy, nó giống như một "VM chạy kubelet của chúng ta".</p>
}

// question: 4.34 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Các QoS class trong Kubernetes giúp kiểm soát điều gì?</p>{
	~[moodle]Cách các Pod được tạo và xóa.#<p>Kubelet và các controller quản lý việc tạo và xóa Pod.</p>
	=[moodle]Khả năng truy cập tài nguyên của các ứng dụng.
	~[moodle]Tốc độ kéo image của container.#<p>ImageService của CRI quản lý việc kéo image.</p>
	~[moodle]Số lượng node trong một cụm.#<p>Quy mô của cụm là một vấn đề riêng biệt.</p>
	####<p><strong>Giải thích</strong>\: QoS (quality of service) đề cập đến khả năng sẵn sàng của tài nguyên ngay lập tức. Các QoS class như Guaranteed, Burstable, và BestEffort được tạo ra tùy thuộc vào cách bạn định nghĩa một Pod, ảnh hưởng đến khả năng truy cập tài nguyên của ứng dụng.</p>
}

// question: 4.35 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Tại sao kube-scheduler thường được cấu hình là một Burstable Pod?</p>{
	~[moodle]Để đảm bảo nó luôn có đủ tài nguyên.#<p>Guaranteed Pod sẽ đảm bảo tài nguyên, nhưng scheduler cần linh hoạt.</p>
	=[moodle]Vì nó cần khả năng sử dụng các burst CPU lớn khi cần.
	~[moodle]Để giới hạn nghiêm ngặt tài nguyên mà nó có thể tiêu thụ.#<p>Burstable Pod không có giới hạn cứng như vậy.</p>
	~[moodle]Vì nó không quan trọng và có thể bị đình chỉ bất cứ lúc nào.#<p>scheduler là một thành phần quan trọng của mặt phẳng điều khiển.</p>
	####<p><strong>Giải thích</strong>\: kube-scheduler là một ví dụ về Pod thường chạy với khả năng sử dụng các burst CPU lớn khi cần thiết (ví dụ: trong trường hợp cần lên lịch nhanh chóng cho 10 hoặc 20 Pod vào một node).</p>
}

// question: 4.36 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Khi tạo một cgroup, tại sao việc ghi "0" vào /sys/fs/cgroup/memory/chroot0/memory.swappiness lại quan trọng?</p>{
	~[moodle]Để đảm bảo container có thể sử dụng tất cả swap space có sẵn.#<p>Ngược lại, nó ngăn việc sử dụng swap.</p>
	=[moodle]Để ngăn container phân bổ swap space, phù hợp với cách Kubernetes thường chạy.
	~[moodle]Để tăng tốc độ truy cập bộ nhớ của container.#<p>swappiness không trực tiếp tăng tốc độ truy cập bộ nhớ.</p>
	~[moodle]Để kích hoạt Transparent HugePages.#<p>swappiness không liên quan đến Transparent HugePages.</p>
	####<p><strong>Giải thích</strong>\: Ghi "0" vào memory.swappiness đảm bảo container không phân bổ swap space, đây là cách Kubernetes hầu như luôn chạy.</p>
}

// question: 4.37 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Điều gì là đúng về sự khác biệt giữa etcd v2 và etcd v3?</p>{
	~[moodle]etcd v2 tốt hơn cho hiệu suất so với v3.#<p>etcd v3 có hiệu suất tốt hơn.</p>
	=[moodle]etcd v3 sử dụng gRPC cho các giao dịch nhanh hơn.
	~[moodle]etcd v3 có một không gian key phân cấp.#<p>etcd v3 có không gian key hoàn toàn phẳng, trái ngược với phân cấp.</p>
	~[moodle]etcd v2 hỗ trợ xem nhiều bản ghi trên một kết nối TCP.#<p>etcd v3 có khả năng xem nhiều bản ghi trên một kết nối TCP.</p>
	####<p><strong>Giải thích</strong>\: etcd v3 tốt hơn nhiều so với v2 về hiệu suất và sử dụng gRPC cho các giao dịch nhanh hơn.</p>
}

// question: 4.38 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Lệnh cat /proc/<PID>/cgroup dùng để làm gì?</p>{
	~[moodle]Liệt kê tất cả các tiến trình đang chạy trên hệ thống.#<p>ps -ax làm điều này.</p>
	=[moodle]Hỏi kernel Linux về các cgroup tồn tại cho một tiến trình cụ thể.
	~[moodle]Hiển thị thông tin CPU và bộ nhớ của một Pod.#<p>Đây là thông tin nằm trong các tệp con của đường dẫn cgroup, không phải lệnh cat này trực tiếp.</p>
	~[moodle]Thay đổi cấu hình cgroup của một tiến trình.#<p>cat chỉ dùng để đọc, không phải thay đổi.</p>
	####<p><strong>Giải thích</strong>\: Lệnh này được dùng để hỏi kernel Linux về các cgroup tồn tại cho tiến trình cụ thể đó.</p>
}

// question: 4.39 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Khi kiểm tra cgroup của một tiến trình, thư mục kubepods trong đường dẫn cgroup biểu thị điều gì?</p>{
	=[moodle]Một phân vùng của các cgroup mà Kubernetes dành riêng cho các Pod của nó.
	~[moodle]Cgroup cho Docker daemon đang chạy trên máy tính.#<p>docker là cgroup cho Docker daemon.</p>
	~[moodle]Tên của Docker kind container.#<p>b7a49b42... là tên của Docker kind container.</p>
	~[moodle]ID của Pod, được phản ánh trong Linux kernel.#<p>pod1557... là ID của Pod.</p>
	####<p><strong>Giải thích</strong>\: kubepods là một phân vùng của các cgroup mà Kubernetes dành riêng cho các Pod của nó.</p>
}

// question: 4.40 name: Chapter 4: Using cgroups for processes in our Pods
::Chapter 4\: Using cgroups for processes in our Pods::[html]<p>Loại cgroup nào được sử dụng để quản lý I/O?</p>{
	~[moodle]cpuacct.#<p>cpuacct được sử dụng để báo cáo việc sử dụng tài nguyên CPU.</p>
	=[moodle]blkio.
	~[moodle]memory.#<p>memory cgroup giới hạn việc sử dụng bộ nhớ.</p>
	~[moodle]freezer.#<p>freezer cgroup tạm dừng hoặc tiếp tục các tác vụ.</p>
	####<p><strong>Giải thích</strong>\: blkio cgroup là một tài nguyên ít được biết đến hơn được sử dụng để quản lý I/O.</p>
}

// Chapter 5: CNIs and providing the Pod with a network
// question: 5 name: Switch category to $module$/top/Chapter 5: CNIs and providing the Pod with a network
$CATEGORY: $module$/top/Chapter 5: CNIs and providing the Pod with a network

// question: 5.1 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Lý do chính tại sao Kubernetes cần các mạng được định nghĩa bằng phần mềm (SDN) là gì?</p>{
	~[moodle]Để cho phép quản trị viên cấu hình mạng thủ công hàng ngày.#<p>Ngược lại, SDN nhằm giảm gánh nặng cấu hình mạng thủ công.</p>
	=[moodle]Vì mạng thay đổi liên tục và cần được tự động hóa bằng phần mềm.
	~[moodle]Để giảm chi phí phần cứng mạng vật lý.#<p>Mặc dù có thể giảm chi phí phần cứng, đây không phải là lý do chính.</p>
	~[moodle]Để đơn giản hóa việc triển khai các ứng dụng độc lập.#<p>Nó giải quyết vấn đề mạng trong một môi trường container phức tạp, không phải ứng dụng độc lập.</p>
	####<p><strong>Giải thích</strong>\: Mạng Kubernetes hoàn toàn được định nghĩa bằng phần mềm và liên tục thay đổi do tính chất phù du và động của Pod và service endpoints. Do đó, nó phải được tự động hóa bằng phần mềm.</p>
}

// question: 5.2 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Hai công cụ mạng cơ bản mà Kubernetes cung cấp để giải quyết vấn đề mạng container là gì?</p>{
	~[moodle]Docker Compose và Docker Swarm.#<p>Đây là các công cụ quản lý container của Docker, không phải công cụ mạng cốt lõi của Kubernetes.</p>
	~[moodle]Kubelet và API Server.#<p>Kubelet và API Server là các thành phần cốt lõi của Kubernetes, nhưng không phải là công cụ mạng trực tiếp.</p>
	=[moodle]Kube-proxy và Container Network Interface (CNI).
	~[moodle]Virtual Machines (VMs) và Hypervisors.#<p>Đây là công nghệ ảo hóa, không phải công cụ mạng của Kubernetes.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes cung cấp hai công cụ mạng cơ bản là Kube-proxy và Container Network Interface (CNI) để giải quyết vấn đề định tuyến lưu lượng vào và ra khỏi cụm.</p>
}

// question: 5.3 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Điều gì là đúng về cách CNI specification định nghĩa chi tiết mạng container?</p>{
	~[moodle]Nó định nghĩa rất chi tiết các hoạt động mạng của container.#<p>Ngược lại, nó không chỉ định chi tiết.</p>
	=[moodle]Nó là một định nghĩa chung cho các hoạt động cấp cao để thêm container vào mạng.
	~[moodle]Nó chỉ có thể được triển khai bởi các plugin IPAM.#<p>Một số plugin CNI, như IPAM, chỉ chịu trách nhiệm tìm địa chỉ IP hợp lệ, nhưng CNI không giới hạn ở đó.</p>
	~[moodle]Nó yêu cầu mỗi plugin CNI phải gắn một Pod vào mạng.#<p>Một số plugin CNI không thực sự gắn Pod vào mạng, mà đóng vai trò nhỏ hơn.</p>
	####<p><strong>Giải thích</strong>\: CNI specification là một định nghĩa chung cho các hoạt động cấp cao để thêm một container vào mạng, không chỉ rõ chi tiết của mạng container.</p>
}

// question: 5.4 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Mục đích chính của kube-proxy trong Kubernetes là gì?</p>{
	~[moodle]Cấp phát địa chỉ IP cho các Pod.#<p>CNI provider cấp phát địa chỉ IP cho Pod.</p>
	=[moodle]Thực hiện các rule định tuyến cấp thấp để gửi lưu lượng từ service đến Pod.
	~[moodle]Quản lý vòng đời của các Pod.#<p>kubelet quản lý vòng đời của Pod.</p>
	~[moodle]Cung cấp lưu trữ persistent cho các Pod.#<p>CSI và PersistentVolumes cung cấp lưu trữ persistent.</p>
	####<p><strong>Giải thích</strong>\: kube-proxy sử dụng công nghệ định tuyến cấp thấp như iptables hoặc IPVS để gửi lưu lượng từ service vào và ra khỏi Pod.</p>
}

// question: 5.5 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Khi nào mặt phẳng điều khiển Kubernetes tạo một địa chỉ IP mới cho một ClusterIP Service?</p>{
	~[moodle]Khi một CNI provider yêu cầu một IP.#<p>CNI providers cấp phát IP cho Pod, không phải service.</p>
	=[moodle]Khi bạn tạo một ClusterIP Service mới từ CIDR được cung cấp khi khởi động.
	~[moodle]Khi kube-proxy khởi động.#<p>kube-proxy thực hiện định tuyến cho service, nhưng không tạo IP service.</p>
	~[moodle]Khi một Pod yêu cầu một địa chỉ IP nội bộ.#<p>Địa chỉ IP nội bộ cho Pod được cấp bởi CNI.</p>
	####<p><strong>Giải thích</strong>\: Khi bạn tạo một ClusterIP Service mới, mặt phẳng điều khiển Kubernetes tạo một IP mới từ CIDR bạn cung cấp khi khởi động như một tùy chọn dòng lệnh.</p>
}

// question: 5.6 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Cấu hình kube-proxy phổ biến nhất trên Linux là gì?</p>{
	~[moodle]userspace proxy.#<p>userspace proxy là một chế độ cũ hơn và kém hiệu quả hơn.</p>
	~[moodle]IPVS proxy.#<p>IPVS proxy là một chế độ thay thế, hiệu quả hơn, nhưng iptables vẫn phổ biến nhất.</p>
	=[moodle]iptables proxy.
	~[moodle]kernel proxy.#<p>kernel proxy không phải là một chế độ riêng biệt mà là cách iptables và IPVS tương tác với kernel.</p>
	####<p><strong>Giải thích</strong>\: Trường hợp phổ biến hơn là chúng ta chạy kube-proxy trên Linux, và trong trường hợp này, chúng ta thường chạy iptables proxy. Trong các cụm kind của bạn, kube-proxy chỉ chạy ở chế độ iptables mặc định.</p>
}

// question: 5.7 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Các NodePort được sử dụng để làm gì trong Kubernetes?</p>{
	~[moodle]Cung cấp các địa chỉ IP nội bộ cho các Pod.#<p>ClusterIP Services và CNI cấp IP nội bộ cho Pod.</p>
	=[moodle]Mở một cổng ngẫu nhiên trên tất cả các node của cụm để chuyển tiếp lưu lượng đến một Service.
	~[moodle]Tạo một địa chỉ IP bên ngoài ổn định cho LoadBalancer Services.#<p>LoadBalancer Service cung cấp IP bên ngoài.</p>
	~[moodle]Giới hạn lưu lượng mạng cho các Service nội bộ.#<p>NetworkPolicies giới hạn lưu lượng mạng.</p>
	####<p><strong>Giải thích</strong>\: Các cổng ngẫu nhiên được cấp phát cho các NodePort Service sẽ mở trên tất cả các node của cụm, chuyển tiếp lưu lượng đến các Pod của Service đó.</p>
}

// question: 5.8 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Calico là gì trong ngữ cảnh của các CNI provider?</p>{
	~[moodle]Một CNI provider dựa trên OVS sử dụng bridge để định tuyến.#<p>Antrea là CNI provider dựa trên OVS.</p>
	=[moodle]Một CNI provider dựa trên BGP tạo các rule định tuyến Layer 3.
	~[moodle]Một CNI provider đơn giản chỉ dành cho các cụm node đơn.#<p>KindNet là CNI đơn giản chỉ dùng cho cụm node đơn.</p>
	~[moodle]Một CNI provider độc quyền chỉ chạy trong hạ tầng của nhà cung cấp cụ thể.#<p>Calico cung cấp cả chức năng vendor-specific và vendor-neutral.</p>
	####<p><strong>Giải thích</strong>\: Calico là một CNI provider dựa trên BGP (Border Gateway Protocol) tạo các rule định tuyến Layer 3 mới để triển khai mặt phẳng dữ liệu.</p>
}

// question: 5.9 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Kiến trúc của một CNI plugin thường bao gồm những bước nào khi cài đặt trong các cụm Linux đơn giản?</p>{
	~[moodle]Chỉ cài đặt một chương trình CNI binary trên node.#<p>Đây chỉ là một trong các bước.</p>
	=[moodle]Triển khai một DaemonSet và một coordination container.
	~[moodle]Chỉ cài đặt kube-proxy.#<p>kube-proxy là một điều kiện tiên quyết, không phải là toàn bộ quá trình cài đặt CNI.</p>
	~[moodle]Không cần cài đặt gì vì Kubernetes tự động tích hợp CNI.#<p>CNI cần được cấu hình và cài đặt.</p>
	####<p><strong>Giải thích</strong>\: Việc cài đặt CNI bao gồm bốn bước: cài đặt kube-proxy, cài đặt chương trình CNI binary, triển khai một DaemonSet và triển khai một coordination container. DaemonSet và coordination container là các thành phần chính.</p>
}

// question: 5.10 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Khi một IP address được yêu cầu cho một Pod mới, kubelet sử dụng binary CNI nào?</p>{
	~[moodle]kube-proxy binary.#<p>kube-proxy chịu trách nhiệm định tuyến service.</p>
	=[moodle]CNI binary được cài đặt trên host qua hostPath volume.
	~[moodle]etcd binary.#<p>etcd là kho dữ liệu key/value của Kubernetes.</p>
	~[moodle]API server.#<p>API server quản lý các đối tượng API.</p>
	####<p><strong>Giải thích</strong>\: CNI binary cho tiến trình Calico-node truy cập hostPath, kết nối tới /etc/cni/net.d/ trên kubelet của bạn. Kubelet sử dụng binary này để gọi API CNI khi cần một địa chỉ IP cho một Pod mới.</p>
}

// question: 5.11 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Trong Antrea, điều gì là đúng về cách nó quản lý lưu lượng Pod?</p>{
	~[moodle]Nó sử dụng BGP để broadcast các rule IP.#<p>Calico sử dụng BGP.</p>
	=[moodle]Nó chạy một OVS switch trên mỗi node và định tuyến lưu lượng.
	~[moodle]Nó sử dụng iptables để tạo các rule network policy.#<p>Antrea sử dụng OVS để thực hiện các rule NetworkPolicy.</p>
	~[moodle]Nó gán một MAC address riêng cho mỗi Pod.#<p>macvlan gán MAC riêng, ipvlan thì không.</p>
	####<p><strong>Giải thích</strong>\: Antrea sử dụng OpenVSwitch (OVS) làm mặt phẳng dữ liệu, chạy một switch trên mỗi node để định tuyến lưu lượng khi nó đến.</p>
}

// question: 5.12 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Ba hoạt động CNI cơ bản mà chương trình binary được cài đặt bởi agent triển khai là gì?</p>{
	~[moodle]START, STOP, RESTART.#<p>Đây không phải là các hoạt động chính thức của CNI.</p>
	=[moodle]ADD, DELETE, CHECK.
	~[moodle]CREATE, READ, UPDATE.#<p>Đây không phải là các hoạt động chính thức của CNI.</p>
	~[moodle]BUILD, DEPLOY, MONITOR.#<p>Đây không phải là các hoạt động chính thức của CNI.</p>
	####<p><strong>Giải thích</strong>\: CNI specification được triển khai bởi chương trình binary được cài đặt bởi agent. Cụ thể, nó triển khai ba hoạt động CNI cơ bản: ADD, DELETE, và CHECK.</p>
}

// question: 5.13 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Tại sao các hostPath volume type thường được coi là một anti-pattern, trừ một số trường hợp cụ thể?</p>{
	~[moodle]Vì chúng luôn làm chậm hiệu suất của Pod.#<p>Không phải luôn làm chậm hiệu suất.</p>
	=[moodle]Vì chúng tạo ra một lỗ hổng bảo mật nếu bị lạm dụng.
	~[moodle]Vì chúng không thể được sử dụng để cài đặt CNI binary.#<p>hostPath được sử dụng để cài đặt CNI binary.</p>
	~[moodle]Vì chúng không tương thích với Kubernetes service discovery.#<p>hostPath không ảnh hưởng đến service discovery.</p>
	####<p><strong>Giải thích</strong>\: hostPath volume type thường là một anti-pattern, trừ khi bạn đang cấu hình một chức năng OS cấp thấp như CNI, vì nó có thể mở ra một lỗ hổng bảo mật nếu container có toàn quyền truy cập vào host.</p>
}

// question: 5.14 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Sự khác biệt chính giữa Calico và Antrea về mặt kiến trúc định tuyến là gì?</p>{
	~[moodle]Calico sử dụng bridge, còn Antrea sử dụng BGP.#<p>Antrea sử dụng bridge, còn Calico sử dụng BGP.</p>
	=[moodle]Calico sử dụng Layer 3 routing (BGP), còn Antrea sử dụng OVS data plane (bridge).
	~[moodle]Calico yêu cầu kube-proxy, còn Antrea thì không.#<p>Cả hai đều cần kube-proxy hoặc có thể thay thế nó.</p>
	~[moodle]Calico chỉ chạy trên Linux, còn Antrea hỗ trợ Windows.#<p>Cả hai đều hỗ trợ Linux và Windows.</p>
	####<p><strong>Giải thích</strong>\: Calico là một CNI provider dựa trên BGP (Layer 3 routing), còn Antrea là một CNI provider dựa trên OVS (Open vSwitch) data plane, sử dụng bridge.</p>
}

// question: 5.15 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Điều gì xảy ra với các CoreDNS Pod nếu CNI provider chưa được thiết lập trong cụm?</p>{
	~[moodle]Chúng sẽ chạy bình thường nhưng không thể phân giải DNS.#<p>CoreDNS yêu cầu mạng Pod để hoạt động.</p>
	=[moodle]Chúng sẽ không thể khởi động vì các node ở trạng thái NotReady.
	~[moodle]Chúng sẽ tự động cài đặt CNI provider.#<p>CoreDNS không tự cài đặt CNI.</p>
	~[moodle]Chúng sẽ được chuyển sang một node khác có CNI.#<p>scheduler sẽ không lên lịch cho các Pod nếu các node không sẵn sàng.</p>
	####<p><strong>Giải thích</strong>\: Tại thời điểm này, CoreDNS Pod sẽ không thể khởi động vì Kubernetes scheduler thấy rằng tất cả các node đều ở trạng thái NotReady, do CNI provider chưa được thiết lập.</p>
}

// question: 5.16 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Các veth pair (virtual Ethernet cable) trong Calico được dùng để làm gì?</p>{
	~[moodle]Kết nối các node với mạng internet bên ngoài.#<p>veth pair là cho kết nối nội bộ giữa Pod và node.</p>
	=[moodle]Kết nối các Pod trực tiếp với kubelet thông qua một cáp Ethernet ảo.
	~[moodle]Tạo một IP tunnel giữa các node.#<p>IP tunnel là một cơ chế khác để giao tiếp giữa các node.</p>
	~[moodle]Giám sát lưu lượng mạng của kube-proxy.#<p>veth pair không trực tiếp giám sát kube-proxy.</p>
	####<p><strong>Giải thích</strong>\: Thiết bị cali3831... được gắn trực tiếp (như bất kỳ thiết bị nào khác) qua một cáp Ethernet (một loại) vào node của chúng ta. Đây được gọi là veth pair, trong đó các container tự chúng có một đầu của cáp Ethernet ảo (tên là cali3831) được cắm trực tiếp vào chúng từ kubelet của chúng ta.</p>
}

// question: 5.17 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Các CNI provider và kube-proxy hoạt động khác nhau như thế nào trên các hệ điều hành non-Linux (ví dụ: Windows)?</p>{
	=[moodle]Chúng chạy như các Windows services thay vì Pods.
	~[moodle]Chúng sử dụng cùng một cách triển khai trên Windows như trên Linux.#<p>Cách triển khai khác nhau do đặc điểm của OS.</p>
	~[moodle]Windows Kubernetes nodes không cần CNI provider hoặc kube-proxy.#<p>Windows Kubernetes nodes vẫn cần CNI provider và kube-proxy.</p>
	~[moodle]Chúng chỉ hỗ trợ BGP trên Windows.#<p>Calico có thể chạy ở chế độ VXLAN trên Windows.</p>
	####<p><strong>Giải thích</strong>\: Trên các hệ điều hành khác (ví dụ: Windows Kubernetes nodes), CNI provider được cài đặt bằng trình quản lý dịch vụ và chạy như một host process.</p>
}

// question: 5.18 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>KindNet là gì trong ngữ cảnh CNI?</p>{
	~[moodle]Một CNI provider toàn diện cho các cụm lớn.#<p>KindNet không phải là toàn diện cho các cụm lớn.</p>
	=[moodle]Một CNI plugin đơn giản chỉ hoạt động cho các cụm một node.
	~[moodle]Một CNI plugin dựa trên VXLAN.#<p>KindNet không được chỉ rõ là dựa trên VXLAN.</p>
	~[moodle]Một CNI provider độc quyền của VMware.#<p>Antrea là CNI của VMware.</p>
	####<p><strong>Giải thích</strong>\: KindNet là một CNI plugin đơn giản được sử dụng trong các cụm kind mặc định, nhưng nó chỉ được thiết kế để hoạt động trong các cụm đơn giản với một subnet duy nhất.</p>
}

// question: 5.19 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>IP tunnel là gì và tại sao các CNI provider sử dụng chúng?</p>{
	~[moodle]Một loại giao diện mạng vật lý để kết nối các node.#<p>IP tunnel là ảo, không phải vật lý.</p>
	=[moodle]Một cấu trúc cho phép mạng phẳng giữa các Pod trong một cụm.
	~[moodle]Một công cụ để giám sát lưu lượng mạng giữa các Pod.#<p>IP tunnel là cơ chế định tuyến, không phải công cụ giám sát.</p>
	~[moodle]Một cơ chế bảo mật để mã hóa lưu lượng Pod.#<p>IP tunnel không cung cấp mã hóa.</p>
	####<p><strong>Giải thích</strong>\: IP tunnel là một cấu trúc cho phép mạng phẳng giữa các Pod trong một cụm. Các thiết bị như antrea-gw0 hoặc tunl0 tương ứng với các gateway OVS hoặc IPIP tunnel để quản lý lưu lượng.</p>
}

// question: 5.20 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Lệnh route -n trong một cụm Calico hiển thị gì khác biệt so với một cụm Antrea?</p>{
	~[moodle]Calico có một routing table entry cho mỗi node.#<p>Ngược lại với phát biểu.</p>
	=[moodle]Calico có một routing table entry cho mỗi Pod.
	~[moodle]Antrea có một routing table entry cho mỗi Pod.#<p>Ngược lại với phát biểu.</p>
	~[moodle]Antrea không có routing table entry nào.#<p>Antrea có một routing table entry cho mỗi node.</p>
	####<p><strong>Giải thích</strong>\: Antrea có một routing table entry cho mỗi node, trong khi Calico có một routing table entry cho mỗi Pod.</p>
}

// question: 5.21 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Trong Calico, giao thức định tuyến Layer 3 nào thường được sử dụng?</p>{
	~[moodle]VXLAN.#<p>VXLAN là một tùy chọn định tuyến khác mà Calico hỗ trợ.</p>
	~[moodle]NAND.#<p>NAND là một tùy chọn định tuyến khác mà Calico hỗ trợ.</p>
	=[moodle]BGP (Border Gateway Protocol).
	~[moodle]OVS (Open vSwitch).#<p>OVS được Antrea sử dụng.</p>
	####<p><strong>Giải thích</strong>\: Calico là một CNI provider dựa trên BGP (Border Gateway Protocol) tạo các rule định tuyến Layer 3 mới để triển khai mặt phẳng dữ liệu.</p>
}

// question: 5.22 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Mục đích của tunl0 interface trong một cụm Calico là gì?</p>{
	~[moodle]Để kết nối Pod với mạng host.#<p>tunl0 là cho IP tunnel, không phải mạng host.</p>
	=[moodle]Để định tuyến lưu lượng thông qua IPIP tunnel trong cụm.
	~[moodle]Để giám sát lưu lượng OVS.#<p>tunl0 không phải để giám sát OVS.</p>
	~[moodle]Để cung cấp giao diện quản lý Calico.#<p>tunl0 là một giao diện mạng.</p>
	####<p><strong>Giải thích</strong>\: Trong cụm Calico của chúng ta, chạy ip a cho thấy chúng ta có một tunl0 interface. Điều này được tạo bởi container calico_node thông qua brd service, chịu trách nhiệm định tuyến lưu lượng thông qua IPIP tunnel trong cụm.</p>
}

// question: 5.23 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Điều gì là đúng khi so sánh CNI providers và kube-proxy trên các OS khác nhau?</p>{
	=[moodle]Linux có tiện ích mạng native tốt hơn cho Pod so với các OS khác.
	~[moodle]Windows Kubernetes nodes thường chạy CNI provider dưới dạng Pod.#<p>Windows Kubernetes nodes thường cài đặt CNI provider bằng service manager và chạy nó như một host process.</p>
	~[moodle]Các CNI provider chỉ có thể được cài đặt trên Linux.#<p>CNI providers hỗ trợ cả Linux và Windows.</p>
	~[moodle]Windows HostProcess containers đã được triển khai đầy đủ và phổ biến.#<p>Windows HostProcess containers đang nổi lên, nhưng vẫn chưa phổ biến như Linux DaemonSets.</p>
	####<p><strong>Giải thích</strong>\: Linux networking stack rất phù hợp với mô hình mạng của Kubernetes, chủ yếu do kiến trúc của cgroups, namespaces, và khái niệm Linux root user.</p>
}

// question: 5.24 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Lệnh nào có thể được sử dụng để kiểm tra CNI routing trên các provider khác nhau?</p>{
	~[moodle]ls và grep.#<p>Các lệnh này được sử dụng cho các tác vụ filesystem.</p>
	=[moodle]arp và ip.
	~[moodle]cat và find.#<p>Các lệnh này được sử dụng cho các tác vụ filesystem.</p>
	~[moodle]kubectl get pods.#<p>kubectl get pods hiển thị trạng thái Pod, không phải thông tin định tuyến cấp thấp.</p>
	####<p><strong>Giải thích</strong>\: Chúng ta sẽ kiểm tra CNI routing trên các provider khác nhau bằng các lệnh arp và ip.</p>
}

// question: 5.25 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Điều gì sẽ xảy ra với lưu lượng mạng của Pod khi kube-proxy được cấu hình để sử dụng chế độ iptables?</p>{
	~[moodle]Kube-proxy bỏ qua iptables và sử dụng một proxy userspace.#<p>userspace proxy là một chế độ riêng biệt, không phải là cách iptables hoạt động.</p>
	=[moodle]Kube-proxy tạo các rule iptables để gửi lưu lượng từ service đến Pod.
	~[moodle]Kube-proxy chuyển đổi tất cả lưu lượng sang IPVS.#<p>IPVS là một chế độ khác, không phải là kết quả của việc sử dụng iptables.</p>
	~[moodle]Kube-proxy chỉ định tuyến lưu lượng Layer 7.#<p>kube-proxy hoạt động ở Layer 4.</p>
	####<p><strong>Giải thích</strong>\: Trong chế độ iptables, kube-proxy tạo các rule iptables để gửi lưu lượng từ service đến Pod. Đây là nơi sự thay đổi động của service và Pod tác động lớn đến các cụm lớn.</p>
}

// question: 5.26 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Làm thế nào để Antrea và Calico thường quản lý các Network Policy?</p>{
	~[moodle]Cả hai đều sử dụng iptables để thực thi Network Policy.#<p>Calico sử dụng iptables, nhưng Antrea sử dụng OVS flows.</p>
	=[moodle]Antrea sử dụng OVS flows, còn Calico sử dụng iptables.
	~[moodle]Antrea sử dụng BGP, còn Calico sử dụng OVS.#<p>Antrea dùng OVS, Calico dùng BGP.</p>
	~[moodle]Cả hai đều không thực hiện các Network Policy mà dựa vào Kubernetes.#<p>Cả hai đều triển khai Network Policy.</p>
	####<p><strong>Giải thích</strong>\: Antrea thực hiện Network Policy bằng cách sử dụng OVS flows và ghi các flow này vào table 90. Calico sử dụng các rule iptables.</p>
}

// question: 5.27 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Điều gì là đúng về OverlayFS khi so sánh với các filesystem gốc về hiệu suất ghi?</p>{
	~[moodle]OverlayFS luôn nhanh hơn các filesystem gốc.#<p>Ngược lại, nó thường chậm hơn.</p>
	=[moodle]OverlayFS có thể chậm và tốn CPU hơn do các hoạt động copy-on-write.
	~[moodle]OverlayFS không hỗ trợ các hoạt động ghi.#<p>OverlayFS hỗ trợ ghi.</p>
	~[moodle]OverlayFS không ảnh hưởng đến hiệu suất ghi.#<p>OverlayFS ảnh hưởng đến hiệu suất ghi.</p>
	####<p><strong>Giải thích</strong>\: Các lớp container thường có các filesystem copy-on-write, cho phép một tiến trình ghi dữ liệu vào lớp trên cùng của filesystem mà không ảnh hưởng đến image container bên dưới, nhưng điều này đi kèm với chi phí hiệu suất. Copy-on-write filesystems thường chậm (và có thể tốn CPU) so với các hoạt động filesystem gốc.</p>
}

// question: 5.28 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Trong Docker, Overlay2 storage driver quản lý các lớp image container như thế nào?</p>{
	~[moodle]Nó nén tất cả các lớp thành một tar file lớn.#<p>Image layers được nén dưới dạng tar files, nhưng storage driver giải nén chúng thành các thư mục.</p>
	=[moodle]Nó giải nén mỗi lớp image thành một thư mục riêng biệt và sử dụng OverlayFS để kết hợp chúng.
	~[moodle]Nó lưu trữ các lớp image dưới dạng các đối tượng riêng lẻ trong một cơ sở dữ liệu.#<p>Overlay2 không lưu trữ trong cơ sở dữ liệu.</p>
	~[moodle]Nó giải nén tất cả các lớp vào một thư mục tạm thời duy nhất cho mỗi container.#<p>Overlay2 giải nén mỗi lớp vào một thư mục riêng biệt, không phải một thư mục duy nhất.</p>
	####<p><strong>Giải thích</strong>\: Overlay2 giải nén mỗi lớp trong image container vào thư mục cấu hình của container runtime (thường là /var/lib/docker/overlay2) và sử dụng OverlayFS để kết hợp chúng thành một thư mục duy nhất để container sử dụng.</p>
}

// question: 5.29 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Hiện tượng "copy-up" trong OverlayFS xảy ra khi nào?</p>{
	~[moodle]Khi một container tạo một tệp mới từ đầu.#<p>Tạo tệp mới chỉ là ghi vào upperdir.</p>
	~[moodle]Khi một tệp bị xóa khỏi lớp upperdir.#<p>Xóa tệp từ upperdir thường liên quan đến "whiteout".</p>
	=[moodle]Khi một container muốn sửa đổi hoặc xóa một tệp tồn tại ở lớp lowerdir.
	~[moodle]Khi một container được khởi động từ một image mới.#<p>Copy-up không liên quan trực tiếp đến việc khởi động một container, mà là hành vi ghi vào filesystem.</p>
	####<p><strong>Giải thích</strong>\: Copy-up xảy ra khi một container muốn sửa đổi hoặc xóa một tệp tồn tại trong một trong các lớp lowerdir nhưng không có trong upperdir. Để làm điều này, OverlayFS sẽ sao chép tệp bị thiếu từ thư mục lowerdir sang upperdir để container có thể tương tác với nó.</p>
}

// question: 5.30 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Nhược điểm chính của việc lưu trữ dữ liệu trong OverlayFS của Docker container là gì?</p>{
	~[moodle]Dữ liệu chỉ có thể được truy cập bởi một container duy nhất.#<p>Dữ liệu trong OverlayFS có thể được truy cập bởi container, nhưng nó không phải là giải pháp lưu trữ dữ liệu bền vững.</p>
	~[moodle]Hiệu suất đọc/ghi bị giảm đáng kể.#<p>Mặc dù copy-ups có thể làm chậm hiệu suất I/O, nhược điểm chính được nhấn mạnh là mất dữ liệu.</p>
	=[moodle]Dữ liệu sẽ bị xóa sau khi container bị xóa.
	~[moodle]Dữ liệu không thể được sao lưu hoặc khôi phục.#<p>Có nhiều cách để sao lưu và khôi phục dữ liệu từ container thông qua Volumes hoặc Bind Mounts.</p>
	####<p><strong>Giải thích</strong>\: Một nhược điểm lớn của overlay file system là bất kỳ dữ liệu nào được lưu trữ bên trong nó sẽ bị xóa khi container bị xóa.</p>
}

// question: 5.31 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Hai cách dễ nhất để khắc phục nhược điểm mất dữ liệu của OverlayFS khi một container bị xóa là gì?</p>{
	~[moodle]Sử dụng các công cụ quản lý cấu hình như Chef hoặc Ansible.#<p>Các công cụ quản lý cấu hình không giải quyết vấn đề mất dữ liệu bền vững từ container.</p>
	~[moodle]Sử dụng Dockerfile để tạo các lớp image mới cho mỗi thay đổi.#<p>Tạo các lớp image mới cho mỗi thay đổi sẽ làm tăng kích thước image và không phải là cách để lưu trữ dữ liệu sau khi container bị xóa.</p>
	=[moodle]Sử dụng Volumes hoặc Bind Mounts.
	~[moodle]Tăng kích thước của upperdir để lưu trữ nhiều dữ liệu hơn.#<p>Tăng kích thước upperdir chỉ tăng dung lượng lưu trữ tạm thời, nó không giải quyết vấn đề mất dữ liệu khi container bị xóa.</p>
	####<p><strong>Giải thích</strong>\: Các cách dễ nhất để khắc phục những hạn chế này là sử dụng Volumes hoặc Bind Mounts. Volumes có hiệu suất tốt hơn bind mounts, nhưng bind mounts dễ sử dụng hơn.</p>
}

// question: 5.32 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Điều gì là đúng về OverlayFS trong Docker?</p>{
	~[moodle]Nó là một loại filesystem chỉ đọc.#<p>OverlayFS có một lớp đọc/ghi.</p>
	=[moodle]Nó sử dụng một lớp upperdir để lưu trữ các thay đổi của container.
	~[moodle]Nó được sử dụng để lưu trữ dữ liệu lâu dài.#<p>OverlayFS không phải là giải pháp lưu trữ dữ liệu lâu dài; dữ liệu sẽ bị xóa khi container bị xóa.</p>
	~[moodle]Nó không cho phép container tạo tệp mới.#<p>Container có thể tạo tệp mới bằng cách ghi vào upperdir.</p>
	####<p><strong>Giải thích</strong>\: OverlayFS sử dụng một lớp đọc/ghi được gọi là upperdir để lưu trữ các thay đổi được thực hiện bởi container.</p>
}

// question: 5.33 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Theo mặc định, Docker sử dụng driver volume nào?</p>{
	~[moodle]json-file.#<p>json-file là logging driver mặc định.</p>
	~[moodle]bridge.#<p>bridge là network driver mặc định.</p>
	=[moodle]local.
	~[moodle]overlay2.#<p>overlay2 là storage driver mặc định cho các lớp image.</p>
	####<p><strong>Giải thích</strong>\: Theo mặc định, Docker sử dụng local volume driver. Local driver đơn giản tạo một thư mục trong thư mục hệ thống của Docker và mount nó vào container như một loại virtual disk.</p>
}

// question: 5.34 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Mục đích chính của Bind Mounts trong Docker là gì?</p>{
	~[moodle]Tạo bản sao dữ liệu từ container sang host.#<p>Bind Mounts tạo liên kết trực tiếp, không phải bản sao.</p>
	=[moodle]Ánh xạ các thư mục trên host trực tiếp vào các thư mục bên trong container.
	~[moodle]Duy trì dữ liệu ứng dụng sau khi container bị xóa.#<p>Volumes hoặc Persistent Volumes làm điều này hiệu quả hơn.</p>
	~[moodle]Tải xuống các tệp tar và giải nén chúng vào container.#<p>ADD instruction trong Dockerfile làm điều này.</p>
	####<p><strong>Giải thích</strong>\: Bind Mounts ánh xạ các thư mục trên host trực tiếp vào các thư mục bên trong container.</p>
}

// question: 5.35 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Một trong những lợi thế của Bind Mounts so với việc sao chép source code vào một volume để kiểm thử ứng dụng là gì?</p>{
	~[moodle]Bind Mounts tự động nén dữ liệu để tiết kiệm không gian.#<p>Bind Mounts không nén dữ liệu.</p>
	=[moodle]Không cần quản lý volumes và không có container tạm thời nào bị bỏ lại.
	~[moodle]Đảm bảo rằng ứng dụng luôn chạy với quyền root.#<p>Bind Mounts không liên quan đến việc chạy ứng dụng với quyền root.</p>
	~[moodle]Cải thiện đáng kể hiệu suất I/O trên các hệ thống non-Linux.#<p>Ngược lại, bind mounts có thể gây giảm hiệu suất trên các hệ thống non-Linux.</p>
	####<p><strong>Giải thích</strong>\: Với bind mounts, bạn chỉ cần ánh xạ thư mục source code của mình vào một thư mục trong container và chạy các bài kiểm thử. Không cần quản lý volume và không cần dọn dẹp các container tạm thời sau khi hoàn thành.</p>
}

// question: 5.36 name: Chapter 5: CNIs and providing the Pod with a network
::Chapter 5\: CNIs and providing the Pod with a network::[html]<p>Khi chạy Docker trên các hệ điều hành non-Linux (ví dụ: macOS, Windows), Bind Mounts có thể gặp phải vấn đề gì?</p>{
	~[moodle]Không thể truy cập các tệp lớn hơn 1GB.#<p>Không có giới hạn kích thước tệp cụ thể như vậy.</p>
	=[moodle]Hiệu suất đọc/ghi có thể chậm đáng kể.
	~[moodle]Dữ liệu sẽ không được duy trì sau khi container bị dừng.#<p>Bind Mounts vẫn duy trì dữ liệu trên host; vấn đề là hiệu suất.</p>
	~[moodle]Chỉ các thư mục hệ thống mới có thể được mount, không phải các thư mục người dùng.#<p>Cả thư mục hệ thống và người dùng đều có thể được mount.</p>
	####<p><strong>Giải thích</strong>\: Khi chạy Docker bên ngoài Linux (chẳng hạn trên macOS hoặc Windows), Bind Mounts có thể gặp vấn đề về hiệu suất. Các thư mục làm việc thường được chia sẻ với một virtual machine, và mỗi hoạt động đọc/ghi vào bind mount cần phải thông qua một driver, gây ra sự chậm đáng kể khi làm việc với các tệp lớn hoặc nhiều tệp nhỏ.</p>
}

// Chapter 6: Troubleshooting large-scale network error
// question: 6 name: Switch category to $module$/top/Chapter 6: Troubleshooting large-scale network error
$CATEGORY: $module$/top/Chapter 6: Troubleshooting large-scale network error

// question: 6.1 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Sonobuoy được sử dụng cho mục đích gì trong Kubernetes?</p>{
	~[moodle]Chỉ để triển khai các ứng dụng vào cụm.#<p>Sonobuoy không phải là công cụ triển khai ứng dụng.</p>
	=[moodle]Để chứng nhận, chẩn đoán và kiểm tra chức năng của các cụm Kubernetes đang hoạt động.
	~[moodle]Chỉ để giám sát hiệu suất mạng.#<p>Sonobuoy kiểm tra chức năng tổng thể, không chỉ hiệu suất mạng.</p>
	~[moodle]Để tạo ra các lỗi mạng quy mô lớn để kiểm tra cụm.#<p>Sonobuoy dùng để kiểm tra, không phải tạo lỗi.</p>
	####<p><strong>Giải thích</strong>\: Sonobuoy là một công cụ đa năng để chứng nhận, chẩn đoán và kiểm tra chức năng của các cụm Kubernetes đang hoạt động.</p>
}

// question: 6.2 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Sonobuoy dựa trên thư viện kiểm thử nào của Kubernetes?</p>{
	~[moodle]Unit testing library.#<p>Các thư viện khác không phải là cơ sở của Sonobuoy.</p>
	~[moodle]Integration testing library.#<p>Các thư viện khác không phải là cơ sở của Sonobuoy.</p>
	=[moodle]e2e (end-to-end) testing library.
	~[moodle]Stress testing library.#<p>Các thư viện khác không phải là cơ sở của Sonobuoy.</p>
	####<p><strong>Giải thích</strong>\: Sonobuoy dựa trên thư viện kiểm thử e2e (end-to-end) của Kubernetes.</p>
}

// question: 6.3 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Điều gì là đúng về Antrea CNI provider so với Calico về cách nó thực hiện các NetworkPolicy?</p>{
	~[moodle]Antrea sử dụng iptables, còn Calico sử dụng OVS.#<p>Calico sử dụng iptables.</p>
	=[moodle]Antrea sử dụng OVS router để tạo các rule.
	~[moodle]Antrea không hỗ trợ NetworkPolicy.#<p>Antrea hỗ trợ NetworkPolicy.</p>
	~[moodle]Calico và Antrea đều sử dụng cùng một công nghệ để thực hiện NetworkPolicy.#<p>Antrea sử dụng OVS, Calico sử dụng iptables.</p>
	####<p><strong>Giải thích</strong>\: Antrea CNI provider sử dụng OpenVSwitch (OVS) làm mặt phẳng dữ liệu. OVS router tạo các rule để triển khai Kubernetes NetworkPolicy API.</p>
}

// question: 6.4 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Lệnh arp -na trong Linux được sử dụng để làm gì khi kiểm tra CNI routing?</p>{
	~[moodle]Liệt kê các địa chỉ IP của Pod.#<p>ip a hoặc kubectl get pods -o wide hiển thị IP của Pod.</p>
	=[moodle]Hiển thị bảng ARP để ánh xạ địa chỉ IP thành địa chỉ MAC.
	~[moodle]Kiểm tra trạng thái của kube-proxy.#<p>kube-proxy được kiểm tra bằng các lệnh kubectl hoặc iptables.</p>
	~[moodle]Hiển thị các routing rule Layer 3.#<p>route -n hiển thị routing rule Layer 3.</p>
	####<p><strong>Giải thích</strong>\: Lệnh arp -na hiển thị bảng ARP (Address Resolution Protocol), giúp ánh xạ địa chỉ IP thành địa chỉ MAC trên mạng cục bộ.</p>
}

// question: 6.5 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Khi kiểm tra CNI routing, tại sao cần tracing data paths cho Pod trong một cụm thực?</p>{
	~[moodle]Để xác nhận IP address của Pod.#<p>IP address có thể được kiểm tra bằng lệnh ip a.</p>
	~[moodle]Để kiểm tra các rule cgroup.#<p>cgroup là cho quản lý tài nguyên, không phải data path.</p>
	=[moodle]Để xác nhận rằng CNI provider đang hoạt động bình thường.
	~[moodle]Để xác định tốc độ truyền dữ liệu của container.#<p>tcpdump có thể đo tốc độ truyền.</p>
	####<p><strong>Giải thích</strong>\: Tracing data paths cho Pod trong một cụm thực là một trong các cách để xác nhận rằng CNI provider đang hoạt động bình thường. Nếu không có lưu lượng vào giao diện Calico hoặc Antrea, CNI có thể bị lỗi.</p>
}

// question: 6.6 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Lệnh iptables-save | grep SEP-QI được sử dụng để tìm kiếm điều gì trong một cụm Kubernetes?</p>{
	~[moodle]Tất cả các rule iptables.#<p>iptables-save hiển thị tất cả các rule.</p>
	=[moodle]Các rule liên quan đến một Service Endpoint cụ thể.
	~[moodle]Các rule của NetworkPolicy.#<p>NetworkPolicy có các rule phức tạp hơn.</p>
	~[moodle]Các rule cho LoadBalancer Service.#<p>LoadBalancer Service cũng có rule riêng.</p>
	####<p><strong>Giải thích</strong>\: Chúng ta có thể sử dụng grep để tìm tất cả các rule liên quan đến một service cụ thể. Trong trường hợp này, SEP-QI... tương ứng với container CoreDNS trong cụm.</p>
}

// question: 6.7 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Ingress controllers cung cấp chức năng mạng Layer nào trong Kubernetes?</p>{
	~[moodle]Layer 3 (IP routing).#<p>CNI cung cấp Layer 3.</p>
	~[moodle]Layer 4 (TCP/UDP load balancing).#<p>kube-proxy cung cấp Layer 4.</p>
	=[moodle]Layer 7 (HTTP/HTTPS routing).
	~[moodle]Layer 2 (Ethernet switching).#<p>OVS hoặc physical switch cung cấp Layer 2.</p>
	####<p><strong>Giải thích</strong>\: Ingress controllers cung cấp chức năng mạng Layer 7 (HTTP/HTTPS routing). Ví dụ, Contour là một ingress controller xử lý lưu lượng Layer 7.</p>
}

// question: 6.8 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Gateway API là gì và vai trò của nó trong tương lai của mạng Kubernetes?</p>{
	~[moodle]Một API cũ đang bị thay thế.#<p>Ingress API là cái cũ.</p>
	=[moodle]Một API mới, linh hoạt hơn sẽ thay thế Ingress API.
	~[moodle]Một giao thức giao tiếp giữa các CNI provider.#<p>Gateway API là cho định nghĩa route, không phải giao tiếp giữa các CNI.</p>
	~[moodle]Một công cụ để giám sát lưu lượng mạng Layer 4.#<p>Gateway API tập trung vào Layer 7.</p>
	####<p><strong>Giải thích</strong>\: Gateway API đang nổi lên như một cách thay thế để cung cấp giải pháp multi-tenant tốt hơn cho vấn đề lộ route từ một cụm Kubernetes. Nó mô tả các loại tài nguyên Layer 7 cho nhà phát triển một cách linh hoạt hơn và sẽ thay thế Ingress API.</p>
}

// question: 6.9 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Cyclonus là một công cụ dùng để làm gì trong Kubernetes?</p>{
	~[moodle]Triển khai các CNI provider.#<p>Cyclonus là một công cụ kiểm thử, không phải triển khai.</p>
	=[moodle]Kiểm tra sự phù hợp của CNI provider với NetworkPolicy API.
	~[moodle]Giám sát hiệu suất của OVS.#<p>Prometheus giám sát OVS.</p>
	~[moodle]Khắc phục lỗi kube-proxy.#<p>Sonobuoy hoặc iptables-save được dùng để khắc phục lỗi kube-proxy.</p>
	####<p><strong>Giải thích</strong>\: Cyclonus tạo ra hàng trăm kịch bản Network Policy và thăm dò xem CNI provider của bạn có triển khai chúng đúng cách hay không. Nó là một công cụ mạnh mẽ để điều tra các tính năng NetworkPolicy của CNI provider của bạn.</p>
}

// question: 6.10 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Khi sử dụng tcpdump để tracing data path của các container đang hoạt động, điều gì được quan sát để xác nhận rằng CNI provider đang khỏe mạnh?</p>{
	~[moodle]CPU usage của node.#<p>CPU usage được giám sát bằng cgroups và Prometheus.</p>
	=[moodle]Traffic đang chảy vào giao diện liên quan đến Calico hoặc Antrea.
	~[moodle]Số lượng Pods đang chạy trên node.#<p>kubectl get pods hiển thị số lượng Pods.</p>
	~[moodle]Disk I/O của container.#<p>Disk I/O không liên quan trực tiếp đến network data path.</p>
	####<p><strong>Giải thích</strong>\: Nếu không có lưu lượng vào một giao diện liên quan đến Calico hoặc Antrea, CNI của chúng ta rõ ràng đã bị lỗi vì hầu hết các cụm Kubernetes sẽ có ít nhất một số lưu lượng chảy giữa các Pod trong các hoạt động ổn định.</p>
}

// question: 6.11 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Mục đích của ovs-vsctl tool là gì khi được chạy bên trong Antrea container?</p>{
	~[moodle]Để chỉnh sửa NetworkPolicy của Antrea.#<p>ovs-ofctl được dùng để hiển thị các OVS flows thực hiện NetworkPolicy.</p>
	=[moodle]Để lấy thông tin chi tiết về các giao diện OVS.
	~[moodle]Để khởi động lại Antrea agent.#<p>kubectl được dùng để khởi động lại Pod.</p>
	~[moodle]Để giám sát CPU và memory usage của Antrea.#<p>Prometheus dùng để giám sát CPU/memory.</p>
	####<p><strong>Giải thích</strong>\: Chúng ta có thể hỏi OVS cung cấp thêm thông tin về giao diện này thông qua ovs-vsctl tool.</p>
}

// question: 6.12 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Điều gì là đúng về Antrea khi nó quản lý các routing table entry trên mỗi node?</p>{
	~[moodle]Antrea có một routing table entry cho mỗi Pod.#<p>Calico có một routing table entry cho mỗi Pod.</p>
	=[moodle]Antrea có một routing table entry cho mỗi node.
	~[moodle]Antrea không có routing table entry nào được kernel quản lý.#<p>kernel vẫn quản lý các route cho Antrea gateway.</p>
	~[moodle]Antrea sử dụng blackhole route.#<p>Antrea không có blackhole route vì nó được xử lý bởi OVS.</p>
	####<p><strong>Giải thích</strong>\: Antrea có một routing table entry cho mỗi node. Tất cả lưu lượng của Pod này đi trực tiếp đến thiết bị Antrea-gw0.</p>
}

// question: 6.13 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Mục đích của lệnh tcpdump là gì khi khắc phục sự cố mạng container?</p>{
	~[moodle]Để hiển thị bảng routing của container.#<p>ip route hiển thị bảng routing.</p>
	~[moodle]Để kiểm tra CPU usage của container.#<p>top hoặc cgroups kiểm tra CPU usage.</p>
	=[moodle]Để trace data path của các container đang hoạt động và sniff packets.
	~[moodle]Để khởi động lại network interface của container.#<p>tcpdump là công cụ giám sát, không phải điều khiển.</p>
	####<p><strong>Giải thích</strong>\: Tcpdump là một công cụ chẩn đoán mạng phổ biến được dùng để trace data path của các container đang hoạt động. Nó cho phép bạn sniff packets trực tiếp trên các thiết bị CNI.</p>
}

// question: 6.14 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Khi kiểm tra kube-proxy và iptables, công cụ iptables-save được sử dụng để làm gì?</p>{
	~[moodle]Chỉ để xóa các rule iptables cũ.#<p>iptables-save là để hiển thị, không phải xóa.</p>
	~[moodle]Để lưu trữ các rule iptables vào một tệp.#<p>Nó có thể lưu vào tệp, nhưng mục đích chính là hiển thị.</p>
	=[moodle]Để hiển thị tất cả các rule iptables đang hoạt động.
	~[moodle]Để thêm các rule iptables mới.#<p>iptables được dùng để thêm rule.</p>
	####<p><strong>Giải thích</strong>\: iptables-save cho thấy tất cả glue đang được sử dụng để giữ cho mạng của chúng ta hoạt động cùng nhau.</p>
}

// question: 6.15 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Điều gì không phải là một trong những cách mà NetworkPolicy có thể kiểm soát lưu lượng mạng?</p>{
	~[moodle]Áp dụng cho các Pods.#<p>NetworkPolicy được áp dụng cho các Pods.</p>
	=[moodle]Chỉ kiểm soát lưu lượng ingress.
	~[moodle]Được thiết kế để xử lý lưu lượng TCP, UDP, và SCTP.#<p>NetworkPolicy được thiết kế để xử lý lưu lượng TCP, UDP, và SCTP.</p>
	~[moodle]Có thể kiểm soát lưu lượng được định nghĩa bởi một CIDR range.#<p>NetworkPolicy có thể kiểm soát lưu lượng được định nghĩa bởi một CIDR range.</p>
	####<p><strong>Giải thích</strong>\: NetworkPolicy kiểm soát cả lưu lượng ingress và egress.</p>
}

// question: 6.16 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Contour là gì trong ngữ cảnh Kubernetes?</p>{
	~[moodle]Một CNI provider.#<p>Contour là ingress controller, không phải CNI provider.</p>
	~[moodle]Một load balancer cho các service Layer 4.#<p>Contour xử lý Layer 7.</p>
	=[moodle]Một ingress controller của CNCF.
	~[moodle]Một công cụ để kiểm thử NetworkPolicy.#<p>Cyclonus là công cụ kiểm thử NetworkPolicy.</p>
	####<p><strong>Giải thích</strong>\: Contour là một ingress controller của CNCF (Cloud Native Computing Foundation) nổi lên như một giải pháp thay thế.</p>
}

// question: 6.17 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Các Load Balancers do Kubernetes tạo có thể làm gì mà quản trị viên cần lưu ý về bảo mật?</p>{
	~[moodle]Chúng chỉ hoạt động nội bộ trong cụm.#<p>Load Balancers có thể là internal hoặc external.</p>
	=[moodle]Chúng có thể tự động expose các ứng dụng ra thế giới bên ngoài.
	~[moodle]Chúng luôn yêu cầu cấu hình DNS thủ công.#<p>Kubernetes tự động cấu hình DNS cho các service.</p>
	~[moodle]Chúng không thể bị tấn công.#<p>Mọi thành phần đều có thể bị tấn công.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes có thể tạo các load balancer bên ngoài để expose ứng dụng của bạn ra thế giới, và nó làm điều đó tự động. Điều này có thể gây rủi ro nếu một service nhạy cảm bị expose ra bên ngoài.</p>
}

// question: 6.18 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Open Policy Agent (OPA) hoạt động như thế nào trong Kubernetes?</p>{
	~[moodle]Nó tự động tạo các NetworkPolicy.#<p>OPA thực thi policy, không tự động tạo NetworkPolicy.</p>
	=[moodle]Nó đánh giá các policy và dữ liệu để tạo ra kết quả query.
	~[moodle]Nó thay thế kube-proxy để quản lý lưu lượng.#<p>OPA là policy engine, không phải proxy.</p>
	~[moodle]Nó chỉ được sử dụng để giám sát các audit log.#<p>OPA có audit functionality, nhưng đó không phải là chức năng duy nhất.</p>
	####<p><strong>Giải thích</strong>\: OPA đánh giá các policy và dữ liệu để tạo ra kết quả query (được gửi lại cho client). Các policy được viết bằng ngôn ngữ declarative cấp cao.</p>
}

// question: 6.19 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Gatekeeper của OPA có những tính năng nào?</p>{
	~[moodle]Sử dụng sidecar và không extensible.#<p>Ngược lại, nó không dùng sidecar và extensible.</p>
	=[moodle]Sử dụng CRDs, extensible, và thực hiện chức năng audit.
	~[moodle]Chỉ hoạt động với iptables.#<p>Gatekeeper hoạt động ở cấp độ API của Kubernetes.</p>
	~[moodle]Chỉ kiểm soát Layer 4 networking.#<p>Gatekeeper kiểm soát các policy ở nhiều cấp độ, không chỉ Layer 4.</p>
	####<p><strong>Giải thích</strong>\: Gatekeeper không sử dụng sidecar, sử dụng CRDs (custom resource definitions), có thể mở rộng (extensible), và thực hiện chức năng audit.</p>
}

// question: 6.20 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Khi cấu hình self-signed certificates cho một local registry được bảo mật bằng reverse proxy, bạn cần thêm chứng chỉ CA (ví dụ: cert.pem) vào đâu trên VM/host chạy Docker?</p>{
	~[moodle]Thư mục /var/lib/docker/volumes.#<p>Thư mục này lưu trữ Docker volumes.</p>
	~[moodle]Thư mục /usr/local/bin.#<p>Thư mục này thường chứa các binary executable.</p>
	=[moodle]Thư mục /usr/local/share/ca-certificates và sau đó cập nhật root certificates.
	~[moodle]Tệp /etc/docker/daemon.json.#<p>daemon.json là tệp cấu hình của Docker daemon, không phải nơi lưu trữ chứng chỉ CA.</p>
	####<p><strong>Giải thích</strong>\: Để cấu hình self-signed certificates cho local registry, bạn cần thêm chứng chỉ CA vào thư mục /usr/local/share/ca-certificates và sau đó cập nhật root certificates.</p>
}

// question: 6.21 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Các Enterprise registries là lựa chọn tuyệt vời cho các công ty cần gì?</p>{
	~[moodle]Một registry công khai cho dữ liệu nhạy cảm.#<p>Docker Hub là public registry mặc định.</p>
	~[moodle]Một registry tích hợp với các nền tảng source-code hosting.#<p>Source-code hosting registries tập trung vào tích hợp với các nền tảng lưu trữ source code.</p>
	=[moodle]Một registry hoạt động trong mạng nội bộ và môi trường của họ, tuân thủ tiêu chuẩn ngành.
	~[moodle]Một insecure local registry cho môi trường sản xuất.#<p>Insecure local registries không phù hợp cho môi trường enterprise.</p>
	####<p><strong>Giải thích</strong>\: Enterprise registries là một lựa chọn tuyệt vời cho các công ty cần một registry hoạt động trong mạng nội bộ và môi trường của họ. Chúng được xây dựng để tuân thủ nhiều tiêu chuẩn và quy định của ngành, giúp chúng dễ dàng được phê duyệt bởi các bộ phận security và compliance.</p>
}

// question: 6.22 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Lệnh docker exec -t -i <your kind node> /bin/bash được dùng để làm gì?</p>{
	~[moodle]Khởi động một kind cluster.#<p>kind create cluster làm điều này.</p>
	~[moodle]Xóa một kind cluster.#<p>kind delete cluster làm điều này.</p>
	=[moodle]SSH vào một node Kubernetes bằng cách thực thi vào Docker container của nó.
	~[moodle]Kiểm tra trạng thái của các Pod.#<p>kubectl get pods kiểm tra trạng thái Pod.</p>
	####<p><strong>Giải thích</strong>\: Lệnh này cho phép chúng ta exec vào Docker container đang chạy kind cluster để khám phá các route đã được tạo. Nó tương đương với việc ssh vào một node Kubernetes thực.</p>
}

// question: 6.23 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Linux Capabilities trong ngữ cảnh Docker có mục đích chính là gì?</p>{
	~[moodle]Kiểm soát cách các lớp image được lưu trữ trên disk.#<p>Storage drivers quản lý cách các lớp image được lưu trữ.</p>
	=[moodle]Hạn chế tập hợp các system calls mà các tiến trình bên trong container có thể thực hiện.
	~[moodle]Ánh xạ các network port của container tới host.#<p>--publish flag làm điều này.</p>
	~[moodle]Giám sát CPU và memory usage của container.#<p>Control groups và các công cụ giám sát làm điều này.</p>
	####<p><strong>Giải thích</strong>\: Linux Capabilities là các nhóm đặc quyền có thể được cấp cho một ứng dụng, cho phép quản trị viên hạn chế tập hợp các system calls mà các tiến trình bên trong một namespace có thể thực hiện.</p>
}

// question: 6.24 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Lệnh docker run với --privileged flag có tác dụng gì đối với container?</p>{
	~[moodle]Tự động cài đặt tất cả các gói phần mềm cần thiết vào container.#<p>--privileged không cài đặt phần mềm.</p>
	=[moodle]Khiến container hoạt động như một tiến trình thực trên hệ thống, có quyền truy cập vào mọi thứ bao gồm các thiết bị của host.
	~[moodle]Giới hạn container chỉ chạy một ứng dụng duy nhất để tăng cường bảo mật.#<p>--privileged cho phép truy cập sâu hơn, không phải giới hạn ứng dụng.</p>
	~[moodle]Vô hiệu hóa tất cả các giới hạn tài nguyên CPU và memory cho container.#<p>--privileged không vô hiệu hóa giới hạn tài nguyên; nó bỏ qua các biện pháp bảo mật liên quan đến quyền truy cập thiết bị/tệp.</p>
	####<p><strong>Giải thích</strong>\: --privileged flag về cơ bản nói với Docker: "hãy coi container này như một tiến trình thực trên hệ thống của bạn." Nó có thể làm bất cứ điều gì và truy cập mọi thứ, bao gồm cả các thiết bị trên hệ thống của bạn như ổ cứng. Điều này cực kỳ nguy hiểm.</p>
}

// question: 6.25 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Phương pháp được khuyến nghị để chạy "Docker in Docker" là gì?</p>{
	~[moodle]Cài đặt toàn bộ Docker Engine bên trong container.#<p>Cài đặt toàn bộ Docker Engine bên trong container có nhiều vấn đề và không được khuyến nghị.</p>
	=[moodle]Bind mounting Unix socket của Docker Engine vào container và chỉ cài đặt Docker client.
	~[moodle]Sử dụng virtualized hypervisor bên trong container.#<p>Cách tiếp cận này không phải là "Docker in Docker" mà là nested virtualization, và không được khuyến nghị.</p>
	~[moodle]Xây dựng lại Docker Engine từ source code bên trong container.#<p>Xây dựng lại từ source code là không thực tế và không cần thiết.</p>
	####<p><strong>Giải thích</strong>\: Phương pháp được khuyến nghị và đơn giản hơn nhiều là cấu hình container của bạn để giao tiếp với một Docker Engine hiện có bằng cách bind mounting Unix socket của Docker Engine (thường là /var/run/docker.sock) vào container, và chỉ cài đặt Docker client bên trong container.</p>
}

// question: 6.26 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Nhược điểm chính của việc chạy "Docker in Docker" bằng cách bind mounting Unix socket của Docker Engine là gì?</p>{
	~[moodle]Các child container sẽ không thể truy cập internet.#<p>Child container vẫn có thể truy cập internet nếu mạng được cấu hình đúng.</p>
	~[moodle]Các child container sẽ không được duy trì sau khi parent container bị xóa.#<p>Child container được tạo trực tiếp bởi Docker Engine của host, vì vậy chúng sẽ tồn tại độc lập với parent container trừ khi —rm được sử dụng.</p>
	=[moodle]Parent container sẽ có thể nhìn thấy và tương tác với tất cả các tài nguyên Docker Engine trên host.
	~[moodle]Parent container sẽ yêu cầu quá nhiều tài nguyên CPU và memory.#<p>Mặc dù nó có thể tiêu thụ tài nguyên, đây không phải là nhược điểm chính được nhấn mạnh trong ngữ cảnh này.</p>
	####<p><strong>Giải thích</strong>\: Một nhược điểm của cách tiếp cận này là parent container có thể nhìn thấy các container, volumes, networks, và các tài nguyên khác được quản lý bởi Docker Engine mà bạn đang chia sẻ. Điều này có thể gây ra các vấn đề bảo mật nếu có thông tin nhạy cảm.</p>
}

// question: 6.27 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Tại sao việc chạy nhiều ứng dụng trong một container duy nhất thường không được khuyến nghị?</p>{
	~[moodle]Container sẽ không thể giao tiếp với các external services.#<p>Khả năng giao tiếp không bị ảnh hưởng bởi số lượng ứng dụng trong một container.</p>
	=[moodle]Việc khôi phục khỏi lỗi khó khăn hơn, và có thể dẫn đến thời gian ngừng hoạt động kéo dài.
	~[moodle]Làm tăng đáng kể kích thước của image container.#<p>Tăng kích thước image không phải là lý do chính, mà là sự phức tạp trong quản lý và khôi phục.</p>
	~[moodle]Container sẽ luôn chạy với quyền root, gây ra rủi ro bảo mật.#<p>Root privileges là mặc định, nhưng không phải do chạy nhiều ứng dụng.</p>
	####<p><strong>Giải thích</strong>\: Containers được thiết kế để khởi động và dừng theo ý muốn. Containers có nhiều ứng dụng thường có quy trình khởi động phức tạp hơn các container ứng dụng đơn lẻ. Điều này làm cho việc khôi phục khó khăn hơn, có thể dẫn đến thời gian ngừng hoạt động kéo dài.</p>
}

// question: 6.28 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Giải pháp nào được Docker cung cấp để dễ dàng quản lý nhiều container liên quan trên một máy duy nhất?</p>{
	~[moodle]Kubernetes.#<p>Đây là container orchestrator được sử dụng để quản lý container trên nhiều máy.</p>
	~[moodle]Docker Swarm.#<p>Đây là container orchestrator được sử dụng để quản lý container trên nhiều máy.</p>
	=[moodle]Docker Compose.
	~[moodle]HashiCorp Nomad.#<p>Đây là container orchestrator được sử dụng để quản lý container trên nhiều máy.</p>
	####<p><strong>Giải thích</strong>\: Docker Compose là một công cụ được Docker cung cấp giúp dễ dàng chạy và kết nối nhiều container trên một máy duy nhất. Nó sử dụng một tệp manifest duy nhất để định nghĩa tất cả các container và mối quan hệ của chúng.</p>
}

// question: 6.29 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Khi một ứng dụng bên trong container gửi tin nhắn đến các standard streams (stdout hoặc stderr), Docker sử dụng thành phần nào để thu thập và chuyển tiếp dữ liệu đó?</p>{
	~[moodle]Container runtimes.#<p>Container runtimes tạo, quản lý và xóa container.</p>
	=[moodle]Logging drivers.
	~[moodle]Control groups.#<p>Control groups giới hạn mức tiêu thụ tài nguyên.</p>
	~[moodle]Unix sockets.#<p>Unix sockets được sử dụng để giao tiếp giữa các ứng dụng trên cùng một máy.</p>
	####<p><strong>Giải thích</strong>\: Khi một ứng dụng chạy bên trong container, Docker sử dụng logging drivers để thu thập dữ liệu được gửi đến các stdout hoặc stderr streams. Các driver này chuyển tiếp dữ liệu đến nơi khác, chẳng hạn như một thư mục trên disk hoặc một nền tảng log aggregation trực tuyến.</p>
}

// question: 6.30 name: Chapter 6: Troubleshooting large-scale network error
::Chapter 6\: Troubleshooting large-scale network error::[html]<p>Khi nào bạn nên xem xét sử dụng một container orchestrator như Kubernetes?</p>{
	~[moodle]Khi bạn chỉ cần chạy một ứng dụng duy nhất trên một host.#<p>Docker Compose phù hợp hơn cho các trường hợp sử dụng này.</p>
	~[moodle]Khi bạn muốn đơn giản hóa việc triển khai các ứng dụng chỉ chạy cục bộ.#<p>Docker Compose phù hợp hơn cho các trường hợp sử dụng này.</p>
	=[moodle]Khi bạn đang chạy hàng trăm hoặc hàng nghìn container trong môi trường sản xuất và cần mở rộng, di chuyển và định tuyến lưu lượng.
	~[moodle]Khi bạn muốn giảm thiểu việc sử dụng tài nguyên CPU và memory của container.#<p>Giảm thiểu tài nguyên được thực hiện bằng cách cấu hình giới hạn tài nguyên (control groups) hoặc tối ưu hóa Dockerfiles (multi-stage builds), không phải bằng cách sử dụng orchestrator.</p>
	####<p><strong>Giải thích</strong>\: Trong khi Docker hoạt động tốt cho các ứng dụng đơn lẻ, mọi thứ trở nên rất phức tạp nhanh chóng khi bạn đang chạy hàng trăm hoặc hàng nghìn container trong môi trường sản xuất. Container orchestrator giải quyết những vấn đề này bằng cách sử dụng các công cụ lập lịch, mạng và service discovery để giúp việc mở rộng, di chuyển và định tuyến lưu lượng đến container rất dễ dàng.</p>
}

// Chapter 7: Pod storage and the CSI
// question: 7 name: Switch category to $module$/top/Chapter 7: Pod storage and the CSI
$CATEGORY: $module$/top/Chapter 7: Pod storage and the CSI

// question: 7.1 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Phát biểu nào sau đây mô tả đúng nhất lý do Kubernetes cần các giải pháp lưu trữ ứng dụng bền vững bên ngoài hostPath hoặc emptyDir?</p>{
	~[moodle]hostPath không thể gắn kết với các thiết bị lưu trữ từ xa, và emptyDir quá phức tạp cho các ứng dụng cơ sở dữ liệu.#<p>hostPath có thể gắn kết các thiết bị lưu trữ nhưng có hạn chế về tính bền vững. emptyDir đơn giản và không được thiết kế cho các ứng dụng cơ sở dữ liệu bền vững.</p>
	=[moodle]hostPath không đảm bảo tính khả dụng cao, và emptyDir không bảo toàn dữ liệu khi Pod bị xóa.
	~[moodle]hostPath chỉ hoạt động trên Linux, còn emptyDir không hỗ trợ sao lưu dữ liệu sang bộ nhớ lạnh.#<p>hostPath hoạt động trên Linux và Windows, còn emptyDir không được thiết kế cho các kịch bản sao lưu dài hạn.</p>
	~[moodle]hostPath có hiệu suất thấp, và emptyDir yêu cầu nhiều tài nguyên CPU hơn so với lưu trữ bên ngoài.#<p>Hiệu suất của hostPath và emptyDir thường tốt cho các trường hợp sử dụng cụ thể, nhưng vấn đề chính là tính bền vững và bảo toàn dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: hostPath có thể không có thư mục ghi duy nhất trên đĩa máy chủ và emptyDir là một volume tạm thời mà dữ liệu sẽ biến mất khi Pod bị khởi động lại.</p>
}

// question: 7.2 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Ba khái niệm chính mà Kubernetes sử dụng để biểu diễn mô hình dữ liệu lưu trữ, đặc biệt cho các yêu cầu lưu trữ cấp ứng dụng, là gì?</p>{
	~[moodle]Namespace, Service và Ingress.#<p>Các khái niệm này liên quan đến mạng và phân vùng tài nguyên trong Kubernetes.</p>
	~[moodle]Pod, Container và Image.#<p>Các khái niệm này liên quan đến việc triển khai ứng dụng cơ bản trong Kubernetes.</p>
	=[moodle]PersistentVolume (PV), PersistentVolumeClaim (PVC) và StorageClass.
	~[moodle]Node, Kubelet và API Server.#<p>Các khái niệm này liên quan đến kiến trúc cơ bản của Kubernetes và cách các thành phần tương tác.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes biểu diễn mô hình dữ liệu lưu trữ cấp ứng dụng bằng cách sử dụng các khái niệm PersistentVolume (PV), PersistentVolumeClaim (PVC) và StorageClass.</p>
}

// question: 7.3 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>PersistentVolume (PV) đóng vai trò gì trong mô hình lưu trữ của Kubernetes?</p>{
	~[moodle]PV là yêu cầu của ứng dụng về một khối lượng lưu trữ cụ thể.#<p>Đây là định nghĩa của PersistentVolumeClaim (PVC).</p>
	~[moodle]PV cho phép các nhà cung cấp lưu trữ cắm giải pháp của họ vào Kubernetes.#<p>Đây là chức năng của Container Storage Interface (CSI).</p>
	=[moodle]PV cung cấp cho quản trị viên một cách để quản lý các khối đĩa trong môi trường Kubernetes.
	~[moodle]PV tự động cung cấp lưu trữ cho Pod mà không cần cấu hình thủ công.#<p>Việc tự động cung cấp lưu trữ được gọi là Dynamic Provisioning, thường được thực hiện thông qua StorageClass và CSI.</p>
	####<p><strong>Giải thích</strong>\: PV cung cấp cho quản trị viên một cách để quản lý các khối đĩa trong môi trường Kubernetes.</p>
}

// question: 7.4 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Mục đích chính của PersistentVolumeClaim (PVC) trong Kubernetes là gì?</p>{
	~[moodle]PVC là một giao diện để định nghĩa các loại lưu trữ khác nhau.#<p>Đây là vai trò của StorageClass.</p>
	=[moodle]PVC cho phép ứng dụng yêu cầu quyền truy cập vào một khối lượng lưu trữ.
	~[moodle]PVC là một khối lượng lưu trữ vật lý được quản lý bởi quản trị viên.#<p>Đây là PersistentVolume (PV).</p>
	~[moodle]PVC là một công cụ để giám sát hiệu suất lưu trữ trong cluster.#<p>Việc giám sát thường được thực hiện bởi các công cụ như Prometheus và cAdvisor.</p>
	####<p><strong>Giải thích</strong>\: PVC định nghĩa một yêu cầu đối với các khối lượng lưu trữ (claim to these volumes) có thể được một ứng dụng (bởi một Pod) yêu cầu và được API Kubernetes thực hiện.</p>
}

// question: 7.5 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Chức năng chính của StorageClass trong Kubernetes là gì?</p>{
	~[moodle]StorageClass cho phép quản trị viên cấp phát các khối lượng lưu trữ cụ thể.#<p>Việc cấp phát cụ thể là nhiệm vụ của Dynamic Provisioner và Controller dựa trên yêu cầu từ StorageClass.</p>
	=[moodle]StorageClass cung cấp một cách để nhà phát triển yêu cầu volume mà không cần biết chi tiết triển khai.
	~[moodle]StorageClass tự động sao lưu dữ liệu từ Pod ra bên ngoài cluster.#<p>Sao lưu dữ liệu là một chức năng bên ngoài StorageClass, thường được thực hiện bởi các nhà cung cấp lưu trữ hoặc Snapshot API.</p>
	~[moodle]StorageClass định nghĩa các chính sách bảo mật cho quyền truy cập lưu trữ.#<p>Các chính sách bảo mật thường được định nghĩa ở các cấp độ khác nhau như NetworkPolicy, RBAC hoặc thông qua các công cụ như OPA.</p>
	####<p><strong>Giải thích</strong>\: StorageClass cung cấp cho các nhà phát triển ứng dụng một cách để có được một volume mà không cần biết chính xác cách nó được triển khai.</p>
}

// question: 7.6 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Ba yêu cầu lưu trữ chính thường gây ra vấn đề trong môi trường Kubernetes là gì?</p>{
	~[moodle]Lưu trữ mã nguồn, lưu trữ cấu hình ứng dụng, và lưu trữ nhật ký.#<p>Đây là các loại dữ liệu, không phải ba loại yêu cầu lưu trữ chính theo phân loại của nguồn.</p>
	=[moodle]Lưu trữ Docker/containerd/CRI, lưu trữ hạ tầng Kubernetes, và lưu trữ ứng dụng.
	~[moodle]Lưu trữ CPU, lưu trữ bộ nhớ, và lưu trữ mạng.#<p>CPU, bộ nhớ và mạng là tài nguyên tính toán, không phải loại lưu trữ.</p>
	~[moodle]Lưu trữ tạm thời, lưu trữ bán bền vững, và lưu trữ cực kỳ bền vững.#<p>Đây là phân loại dựa trên tính bền vững, không phải phân loại các yêu cầu lưu trữ gây vấn đề trong Kubernetes.</p>
	####<p><strong>Giải thích</strong>\: Ba loại yêu cầu lưu trữ thường gây ra vấn đề trong môi trường Kubernetes là: lưu trữ Docker/containerd/CRI, lưu trữ hạ tầng Kubernetes và lưu trữ ứng dụng.</p>
}

// question: 7.7 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Lợi ích chính của việc sử dụng StorageClass standard (mặc định) trong Kubernetes là gì khi tạo PVC?</p>{
	~[moodle]Nó cung cấp các tính năng lưu trữ độc quyền không có sẵn trong các StorageClass khác.#<p>StorageClass standard thường là một triển khai cơ bản và không nhất thiết phải cung cấp các tính năng độc quyền.</p>
	=[moodle]Nó tự động gán một lớp lưu trữ cho PVC nếu không được chỉ định rõ ràng.
	~[moodle]Nó đảm bảo hiệu suất I/O cao nhất cho tất cả các volume.#<p>Hiệu suất cao nhất tùy thuộc vào nhà cung cấp lưu trữ và cấu hình cụ thể, không phải mặc định của standard.</p>
	~[moodle]Nó cho phép các Pod truy cập vào lưu trữ mà không cần PersistentVolume.#<p>Pod vẫn cần PersistentVolume (được tự động tạo bởi provisioner) để truy cập lưu trữ.</p>
	####<p><strong>Giải thích</strong>\: Khi một StorageClass standard hoặc mặc định được định nghĩa, một PVC không có StorageClass sẽ tự động được cấu hình để nhận PVC mặc định đó thông qua một admission controller.</p>
}

// question: 7.8 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Container Storage Interface (CSI) giải quyết vấn đề "in-tree provider problem" bằng cách nào?</p>{
	~[moodle]CSI yêu cầu các nhà cung cấp lưu trữ biên dịch mã của họ vào nhân Kubernetes.#<p>CSI ra đời để tránh việc các nhà cung cấp phải đưa mã của họ vào core của Kubernetes.</p>
	=[moodle]CSI cung cấp một giao diện trừu tượng, cho phép các nhà cung cấp tạo giải pháp lưu trữ bên ngoài codebase của Kubernetes.
	~[moodle]CSI loại bỏ hoàn toàn nhu cầu về các trình điều khiển lưu trữ.#<p>CSI không loại bỏ trình điều khiển lưu trữ, mà thay vào đó cung cấp một cách tiêu chuẩn hóa để các trình điều khiển này hoạt động.</p>
	~[moodle]CSI tích hợp sâu hơn với Docker Engine để quản lý lưu trữ.#<p>Kubernetes đang loại bỏ sự phụ thuộc vào Docker Engine, và CSI tập trung vào việc tách rời logic lưu trữ khỏi kubelet.</p>
	####<p><strong>Giải thích</strong>\: CSI định nghĩa một giao diện để các nhà cung cấp giải pháp lưu trữ có thể dễ dàng cắm giải pháp của họ vào bất kỳ cụm Kubernetes nào và cung cấp nhiều giải pháp lưu trữ. Điều này giải quyết vấn đề "in-tree provider problem" khi mã của nhà cung cấp phải nằm trong core của Kubernetes.</p>
}

// question: 7.9 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Theo CSI, ba loại dịch vụ chung (general categories) mà một plugin lưu trữ định nghĩa là gì?</p>{
	~[moodle]Dịch vụ Docker, dịch vụ CNI, và dịch vụ CRI.#<p>Đây là các thành phần và giao diện khác của Kubernetes, không phải các loại dịch vụ của CSI.</p>
	=[moodle]Dịch vụ Identity, dịch vụ Controller, và dịch vụ Node.
	~[moodle]Dịch vụ Read, dịch vụ Write, và dịch vụ Mount.#<p>Đây là các thao tác cơ bản trên file system, không phải các loại dịch vụ CSI.</p>
	~[moodle]Dịch vụ Provision, dịch vụ Attach, và dịch vụ Detach.#<p>Đây là các thao tác được thực hiện bởi các dịch vụ Controller và Node của CSI.</p>
	####<p><strong>Giải thích</strong>\: CSI định nghĩa một tập hợp các chức năng chung bao gồm: dịch vụ Identity, dịch vụ Controller và dịch vụ Node.</p>
}

// question: 7.10 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Chức năng chính của "Identity services" trong đặc tả CSI là gì?</p>{
	~[moodle]Identity services tạo ra các volume mới dựa trên yêu cầu của Pod.#<p>Đây là chức năng của Controller service.</p>
	=[moodle]Identity services cho phép một plugin tự xác định (cung cấp metadata về chính nó).
	~[moodle]Identity services gắn kết một volume vào Pod trên một node cụ thể.#<p>Đây là chức năng của Node service.</p>
	~[moodle]Identity services giám sát các thay đổi trong API server để điều phối lưu trữ.#<p>Việc giám sát API server là nhiệm vụ của các bộ điều khiển (controllers) nói chung.</p>
	####<p><strong>Giải thích</strong>\: Các dịch vụ Identity cho phép một plugin tự xác định (cung cấp metadata về chính nó), giúp control plane của Kubernetes xác nhận rằng một loại plugin lưu trữ cụ thể đang chạy và có sẵn cho một loại volume.</p>
}

// question: 7.11 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Trong quy trình hoạt động của CSI, "Controller service" chịu trách nhiệm gì?</p>{
	~[moodle]Controller service khởi động Pod và đảm bảo nó có quyền truy cập lưu trữ.#<p>Kubelet chịu trách nhiệm khởi động Pod và quản lý vòng đời của nó, bao gồm gắn kết lưu trữ được chuẩn bị bởi CSI.</p>
	=[moodle]Controller service kết nối các yêu cầu lưu trữ với các nhà cung cấp lưu trữ backend.
	~[moodle]Controller service ghi dữ liệu vào volume vật lý trên node.#<p>Việc ghi dữ liệu được thực hiện bởi ứng dụng bên trong Pod, thông qua VFS và volume đã được gắn.</p>
	~[moodle]Controller service đăng ký driver CSI với kubelet trên mỗi node.#<p>Việc đăng ký driver với kubelet là một phần của quy trình Node service và driver registration.</p>
	####<p><strong>Giải thích</strong>\: Controller là bộ não của bất kỳ driver CSI nào, kết nối các yêu cầu lưu trữ với các nhà cung cấp lưu trữ backend. Nó thực hiện các chức năng như CreateVolume, DeleteVolume, ControllerPublishVolume.</p>
}

// question: 7.12 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Khi một Pod được tạo và yêu cầu lưu trữ qua CSI, thành phần nào chịu trách nhiệm thực hiện các hoạt động gắn kết (mounting operations) cấp thấp trên hệ thống tệp?</p>{
	~[moodle]API server.#<p>API server lưu trữ trạng thái mong muốn và là điểm giao tiếp chính.</p>
	~[moodle]Scheduler.#<p>Scheduler chọn node mà Pod sẽ chạy trên đó, dựa trên các thuộc tính lưu trữ.</p>
	=[moodle]Kubelet, thông qua Node service của CSI driver.
	~[moodle]Container runtime.#<p>Container runtime (như containerd) tạo container, nhưng các thao tác gắn kết volume phức tạp được xử lý bởi kubelet và CSI.</p>
	####<p><strong>Giải thích</strong>\: Node service là phần của CSI chạy trên kubelet, gắn kết volume được tạo trước đó vào một Pod cụ thể theo yêu cầu. Kubelet chịu trách nhiệm đảm bảo container của Pod được khởi chạy với các namespace mount chính xác để truy cập thư mục này.</p>
}

// question: 7.13 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Mục đích của bind mount trong bối cảnh CSI là gì?</p>{
	~[moodle]bind mount tạo một bản sao độc lập của dữ liệu cho mỗi container.#<p>bind mount chia sẻ cùng một thư mục, không tạo bản sao độc lập.</p>
	=[moodle]bind mount là thao tác cụ thể trong Linux để làm cho một thư mục có sẵn cho Pod.
	~[moodle]bind mount cho phép gắn kết các volume mà không cần CSI driver.#<p>bind mount là một khái niệm Linux cơ bản, nhưng trong CSI, nó là một phần của "hợp đồng" giữa attacher và kubelet để gắn kết lưu trữ được cấp phát bởi CSI driver.</p>
	~[moodle]bind mount chỉ được sử dụng để chia sẻ tệp cấu hình giữa các container.#<p>bind mount có thể được sử dụng cho nhiều mục đích khác nhau, không chỉ tệp cấu hình.</p>
	####<p><strong>Giải thích</strong>\: Trong Linux, thao tác cụ thể mà chúng ta đề cập khi làm cho một thư mục có sẵn cho Pod (hoặc bất kỳ tiến trình nào khác thông qua việc nhân bản một thư mục) được gọi là bind mount.</p>
}

// question: 7.14 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Tại sao mount propagation lại quan trọng đối với CSI trong Linux?</p>{
	~[moodle]Nó cho phép các container tự động sao chép dữ liệu của volume.#<p>mount propagation liên quan đến việc chia sẻ các mount, không phải tự động sao chép dữ liệu.</p>
	=[moodle]Nó là một phần quan trọng của các yêu cầu cấp thấp của Linux để các mount được tạo từ bên trong container có thể được kubelet chấp nhận.
	~[moodle]Nó đảm bảo rằng các volume được gắn kết luôn ở chế độ chỉ đọc.#<p>mount propagation không liên quan đến chế độ chỉ đọc hay đọc-ghi.</p>
	~[moodle]Nó tăng cường bảo mật bằng cách ngăn các container truy cập vào các mount của máy chủ.#<p>mount propagation thực tế có thể mở rộng khả năng truy cập vào các mount của máy chủ cho container đặc quyền, do đó cần được quản lý cẩn thận về bảo mật.</p>
	####<p><strong>Giải thích</strong>\: Vì các driver CSI là một tập hợp các container thường do nhà cung cấp duy trì, kubelet tự nó cần có khả năng chấp nhận rằng các mount có thể được tạo từ bên trong một container. Điều này được gọi là mount propagation và là một phần quan trọng của các yêu cầu Linux cấp thấp để một số khía cạnh của Kubernetes hoạt động đúng.</p>
}

// question: 7.15 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Các loại filesystem như btrfs, overlay, hoặc overlay2 thường được sử dụng cho mục đích lưu trữ nào trong Kubernetes?</p>{
	~[moodle]Lưu trữ ứng dụng (Application storage) cho các Pod.#<p>Lưu trữ ứng dụng thường là PersistentVolume gắn từ bên ngoài hoặc đĩa cục bộ bền vững.</p>
	~[moodle]Lưu trữ hạ tầng Kubernetes (Kubernetes infrastructure storage) cho các Secret.#<p>Lưu trữ hạ tầng Kubernetes có thể bao gồm hostPath hoặc Secret volumes được sử dụng trên các kubelet riêng lẻ để chia sẻ thông tin cục bộ.</p>
	=[moodle]Lưu trữ Docker/containerd/CRI (copy-on-write filesystem) cho các container.
	~[moodle]Lưu trữ cục bộ (Local storage) trên mỗi node.#<p>Lưu trữ cục bộ thường chỉ một thư mục trên đĩa của node, có thể được dùng cho volume local.</p>
	####<p><strong>Giải thích</strong>\: Các container yêu cầu các filesystem đặc biệt trên runtime của chúng vì chúng cần ghi vào một lớp VFS (đây là lý do tại sao, ví dụ, bạn có thể chạy rm -rf /tmp trên một container mà không thực sự xóa bất cứ thứ gì khỏi host của bạn). Thông thường, môi trường Kubernetes sử dụng một filesystem như btrfs, overlay, hoặc overlay2.</p>
}

// question: 7.16 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Tại sao việc ghi dữ liệu vào lớp trên cùng của filesystem của container (OverlayFS) thường không được khuyến nghị cho lưu lượng ghi cao?</p>{
	~[moodle]Nó tiêu tốn quá nhiều tài nguyên CPU của host.#<p>Mặc dù copy-on-write có thể tốn CPU, vấn đề chính là tính bền vững của dữ liệu.</p>
	=[moodle]Dữ liệu sẽ biến mất ngay khi Pod được khởi động lại.
	~[moodle]Nó tạo ra quá nhiều Network I/O trên cluster.#<p>Việc ghi vào OverlayFS là hoạt động cục bộ trên node, không phải network I/O.</p>
	~[moodle]Nó làm tăng kích thước của image container.#<p>Ghi vào OverlayFS tạo ra một lớp tạm thời, không làm tăng kích thước của image gốc.</p>
	####<p><strong>Giải thích</strong>\: Việc ghi dữ liệu vào lớp trên cùng của filesystem của container (OverlayFS) không được khuyến nghị cho lưu lượng ghi cao vì dữ liệu này biến mất ngay khi Pod được khởi động lại.</p>
}

// question: 7.17 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Các hoạt động như read(), write(), open(), stat(), chmod() được gọi thông qua thành phần nào trong Linux?</p>{
	~[moodle]Kernel module.#<p>Kernel module là các thành phần của nhân Linux, VFS sử dụng chúng nhưng không phải là nơi các hoạt động được gọi trực tiếp.</p>
	=[moodle]Virtual Filesystem (VFS).
	~[moodle]BIOS.#<p>BIOS là phần mềm cấp thấp khởi động hệ thống, VFS hoạt động phía trên nó.</p>
	~[moodle]Device driver.#<p>Device driver là phần mềm giao tiếp với thiết bị phần cứng, VFS sử dụng driver nhưng VFS là lớp trừu tượng phía trên.</p>
	####<p><strong>Giải thích</strong>\: Tất cả các hoạt động này đều được gọi chống lại cái được gọi là Virtual Filesystem (VFS).</p>
}

// question: 7.18 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[ sondole]<p>Tại sao tính năng lưu trữ emptyDir có thể hoạt động như một công cụ tăng hiệu suất cho việc ghi dữ liệu vào đĩa trong container?</p>{
	~[moodle]emptyDir tự động nén dữ liệu để tiết kiệm không gian.#<p>emptyDir không tự động nén dữ liệu.</p>
	=[moodle]emptyDir có thể ghi vào bộ nhớ tạm thời (tmpfs) hoặc được ánh xạ bộ nhớ thuần túy, nhanh như RAM.
	~[moodle]emptyDir yêu cầu ít tài nguyên CPU hơn so với việc ghi vào lớp OverlayFS.#<p>emptyDir có thể nhanh hơn OverlayFS, nhưng không nhất thiết là do ít CPU hơn mà là do bản chất của tmpfs hoặc ánh xạ bộ nhớ.</p>
	~[moodle]emptyDir cho phép ghi trực tiếp vào đĩa vật lý của host.#<p>emptyDir mặc định ghi vào đĩa của node, nhưng thông thường vào một thư mục tạm thời, không phải trực tiếp vào đĩa vật lý mà bỏ qua hệ thống file.</p>
	####<p><strong>Giải thích</strong>\: Volume emptyDir có thể ghi vào bộ nhớ tạm thời (tmpfs) hoặc thậm chí là các volume ánh xạ bộ nhớ thuần túy, nhanh như RAM theo định nghĩa.</p>
}

// question: 7.19 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Khi một Pod yêu cầu lưu trữ bền vững, quy trình chung mà Kubernetes thực hiện để cấp phát PersistentVolumeClaim (PVC) bao gồm những bước nào?</p>{
	=[moodle]Pod yêu cầu PVC, Scheduler tìm node phù hợp, PVC được fulfillment bởi control plane, Pod được khởi động.
	~[moodle]Kubelet tạo PVC, API server phê duyệt, Container runtime gắn volume, Pod bắt đầu chạy.#<p>Kubelet không tạo PVC, API server không trực tiếp phê duyệt mà controller manager xử lý.</p>
	~[moodle]Scheduler tạo PV, Kubelet yêu cầu PVC, Controller Manager xác thực, Pod được triển khai.#<p>Scheduler không tạo PV, Dynamic storage controller mới làm.</p>
	~[moodle]API server trực tiếp cung cấp lưu trữ từ Docker Hub, sau đó Scheduler gắn kết volume.#<p>API server không cung cấp lưu trữ từ Docker Hub.</p>
	####<p><strong>Giải thích</strong>\: Quy trình điển hình bao gồm: Người dùng yêu cầu tạo Pod cần PVC, Scheduler bắt đầu tìm kiếm node phù hợp, PVC được fulfillment bởi Kubernetes control plane (thông qua PV và dynamic storage controller), sau đó Pod được lên lịch và khởi động.</p>
}

// question: 7.20 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Điều gì sẽ xảy ra nếu một PersistentVolumeClaim (PVC) không chỉ định storageClassName và có một StorageClass mặc định đã được định nghĩa trong cluster?</p>{
	~[moodle]PVC sẽ ở trạng thái Pending vô thời hạn.#<p>Nó sẽ không ở trạng thái Pending nếu có StorageClass mặc định.</p>
	=[moodle]PVC sẽ tự động được gán StorageClass mặc định.
	~[moodle]API server sẽ từ chối tạo PVC.#<p>API server sẽ chấp nhận và thêm default StorageClass.</p>
	~[moodle]Kubelet sẽ tạo một emptyDir volume thay thế.#<p>emptyDir không phải là thay thế cho PersistentVolume và PVC.</p>
	####<p><strong>Giải thích</strong>\: Khi một standard hoặc default StorageClass được định nghĩa, một PVC không có storage class sẽ tự động được cấu hình để nhận default PVC đó.</p>
}

// question: 7.21 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Tại sao CSI và dynamic provisioning được coi là hai công nghệ hiệp lực (synergistic) trong Kubernetes?</p>{
	=[moodle]CSI là một giao diện, còn dynamic provisioning là một tính năng, cả hai cùng cho phép các nhà phát triển sử dụng cùng một khai báo qua StorageClass để gắn kết các loại lưu trữ khác nhau.
	~[moodle]CSI chỉ hoạt động với dynamic provisioning để tạo volume.#<p>CSI có thể hoạt động với cả static và dynamic provisioning.</p>
	~[moodle]Dynamic provisioning là một phần của CSI specification.#<p>Dynamic provisioning là một tính năng của nhiều giải pháp cluster, không phải là một phần của CSI specification.</p>
	~[moodle]CSI thay thế hoàn toàn dynamic provisioning cho việc quản lý lưu trữ.#<p>CSI là giao diện để tích hợp driver, dynamic provisioning là khả năng tự động tạo volume. Chúng bổ trợ cho nhau.</p>
	####<p><strong>Giải thích</strong>\: Hai công nghệ này khá hiệp lực. Bằng cách kết hợp chúng, bạn cho phép các nhà phát triển tiếp tục sử dụng cùng một khai báo thông qua StorageClasses để gắn kết các loại lưu trữ có khả năng khác nhau nhưng hiển thị cùng một ngữ nghĩa cấp cao.</p>
}

// question: 7.22 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Lợi ích chính của dynamic provisioning so với việc cấp phát PersistentVolume thủ công là gì?</p>{
	~[moodle]Dynamic provisioning cho phép ứng dụng tự động chọn StorageClass.#<p>StorageClass được chỉ định trong PVC, không phải do ứng dụng tự chọn.</p>
	=[moodle]Dynamic provisioning tự động tạo PersistentVolume khi PVC được yêu cầu, giảm gánh nặng quản lý thủ công.
	~[moodle]Dynamic provisioning đảm bảo rằng dữ liệu luôn được lưu trữ trên local disk của node.#<p>Dynamic provisioning có thể tạo volume trên nhiều loại lưu trữ khác nhau, không chỉ local disk.</p>
	~[moodle]Dynamic provisioning chỉ hoạt động với các volume types cụ thể không được hỗ trợ thủ công.#<p>Dynamic provisioning hỗ trợ nhiều loại volume types thông qua CSI.</p>
	####<p><strong>Giải thích</strong>\: Khả năng quản lý lưu trữ "on the fly" trong một cluster có nghĩa là chúng ta cần có khả năng cung cấp volume "on the fly". Điều này được gọi là dynamic provisioning. Dynamic provisioning trong Kubernetes nổi bật vì tính cắm ghép (PVCs, CSI) và khai báo cao.</p>
}

// question: 7.23 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Sự khác biệt chính giữa local storage (PersistentVolume loại Local) và emptyDir volume là gì?</p>{
	~[moodle]local storage được gắn kết tự động, trong khi emptyDir yêu cầu cấu hình thủ công.#<p>Cả hai đều được gắn kết theo định nghĩa của Pod.</p>
	=[moodle]local storage có tuổi thọ gắn với đĩa cục bộ, có khả năng phục hồi dữ liệu, trong khi emptyDir chỉ tồn tại cùng với vòng đời của Pod trên cùng một node.
	~[moodle]local storage chỉ có thể được truy cập bởi một container duy nhất, còn emptyDir có thể chia sẻ giữa nhiều container.#<p>Cả hai đều có thể được chia sẻ giữa nhiều container trong cùng một Pod.</p>
	~[moodle]local storage luôn yêu cầu một CSI driver, còn emptyDir thì không.#<p>local storage không nhất thiết phải dùng CSI driver; emptyDir không cần.</p>
	####<p><strong>Giải thích</strong>\: local storage có tuổi thọ gắn với đĩa cục bộ, cho phép phục hồi dữ liệu trong trường hợp thảm họa, trong khi emptyDir không hỗ trợ trường hợp sử dụng này.</p>
}

// question: 7.24 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Tại sao emptyDir volume thường được sử dụng làm "scratchpad" để ghi dữ liệu tạm thời giữa hai container trong cùng một Pod?</p>{
	~[moodle]Vì emptyDir là loại volume duy nhất cho phép chia sẻ dữ liệu trong Pod.#<p>Có nhiều cách khác để chia sẻ dữ liệu như thông qua shared volume hoặc mạng.</p>
	=[moodle]Vì emptyDir rẻ hơn và có thể nhanh hơn PersistentVolume nếu dữ liệu không cần được duy trì.
	~[moodle]Vì emptyDir tự động mã hóa dữ liệu, đảm bảo bảo mật.#<p>emptyDir không tự động mã hóa dữ liệu.</p>
	~[moodle]Vì emptyDir cho phép truy cập dữ liệu từ bên ngoài cluster.#<p>emptyDir là lưu trữ cục bộ trên node và không được thiết kế để truy cập từ bên ngoài cluster.</p>
	####<p><strong>Giải thích</strong>\: PersistentVolume thường đắt tiền và chậm hơn đáng kể so với emptyDir volume. Nếu bạn không cần giữ dữ liệu cho một Pod, việc lãng phí tài nguyên lưu trữ là không cần thiết. emptyDir có thể ghi vào bộ nhớ tạm thời (tmpfs) hoặc các volume ánh xạ bộ nhớ thuần túy, nhanh như RAM.</p>
}

// question: 7.25 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Cơ chế nào trong Kubernetes giúp xác định xem một Pod có sẵn sàng để bắt đầu trên một node hay không, liên quan đến các yêu cầu lưu trữ?</p>{
	~[moodle]Kubelet kiểm tra trực tiếp khả năng gắn kết volume.#<p>Kubelet sẽ gắn volume sau khi Pod được lên lịch và đang trong quá trình khởi động.</p>
	=[moodle]Scheduler kiểm tra các thuộc tính cấu trúc liên kết lưu trữ, CPU và bộ nhớ của node.
	~[moodle]API server ủy quyền cho Container runtime để xác minh volume.#<p>Container runtime không chịu trách nhiệm xác minh volume.</p>
	~[moodle]Volume provisioner tự động gắn volume trước khi Pod được lên lịch.#<p>Volume provisioner tạo volume, nhưng Scheduler là người quyết định thời điểm gắn kết.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes scheduler chịu trách nhiệm đảm bảo rằng một Pod được đặt trên một node có khả năng chạy nó, bao gồm cả các thuộc tính cấu trúc liên kết lưu trữ, CPU và bộ nhớ phù hợp.</p>
}

// question: 7.26 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Tại sao Secret trong Kubernetes được coi là một loại lưu trữ, mặc dù không phải là volume truyền thống cho ứng dụng?</p>{
	~[moodle]Secret lưu trữ dữ liệu lớn như các tệp cơ sở dữ liệu.#<p>Secret không dùng để lưu trữ dữ liệu lớn; nó có giới hạn kích thước khoảng 1MB.</p>
	=[moodle]Secret có thể được gắn (mount) vào Pod dưới dạng các tệp hoặc biến môi trường.
	~[moodle]Secret yêu cầu CSI driver để hoạt động.#<p>Secret là một API object gốc của Kubernetes, không yêu cầu CSI driver.</p>
	~[moodle]Secret được thiết kế để chia sẻ dữ liệu bền vững giữa các node.#<p>Secret được dùng để chia sẻ thông tin nhạy cảm một cách an toàn cho Pod, không phải dữ liệu bền vững giữa các node như một volume thông thường.</p>
	####<p><strong>Giải thích</strong>\: Secret được gắn vào Pod dưới dạng các tệp (files) hoặc biến môi trường, cung cấp dữ liệu như chứng chỉ hoặc mật khẩu.</p>
}

// question: 7.27 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Mối quan hệ giữa việc mã hóa Secret trong Kubernetes và Base64 encoding là gì?</p>{
	~[moodle]Base64 encoding là phương pháp chính để bảo mật Secret trong Kubernetes.#<p>Base64 không phải là cơ chế bảo mật.</p>
	=[moodle]Base64 encoding chỉ là một hình thức biểu diễn, không cung cấp bảo mật cho Secret.
	~[moodle]Kubernetes tự động mã hóa Base64 cho Secret để tránh truy cập trái phép.#<p>Kubernetes sử dụng mã hóa khi nghỉ (encryption at rest) cho Secret trong etcd, không phải Base64.</p>
	~[moodle]Base64 encoding được sử dụng để nén Secret trước khi lưu trữ vào etcd.#<p>Base64 không dùng để nén.</p>
	####<p><strong>Giải thích</strong>\: Một quan niệm sai lầm phổ biến là dữ liệu Secret trong Kubernetes được bảo mật thông qua mã hóa Base64. Điều này không đúng, vì mã hóa Base64 không bảo mật bất cứ điều gì cả.</p>
}

// question: 7.28 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Tại sao việc sử dụng hostPath volume thường được coi là một "anti-pattern" (chống mẫu) trong các ứng dụng microservice trên Kubernetes?</p>{
	~[moodle]hostPath không thể cung cấp đủ hiệu suất I/O cho các ứng dụng thực tế.#<p>hostPath có thể cung cấp hiệu suất tốt vì nó truy cập trực tiếp vào đĩa host.</p>
	=[moodle]hostPath làm cho ứng dụng kém linh hoạt hơn vì dữ liệu gắn chặt với một node cụ thể, gây khó khăn khi Pod bị di chuyển.
	~[moodle]hostPath yêu cầu cấu hình phức tạp và không thể tự động hóa.#<p>hostPath đơn giản để cấu hình nhưng hạn chế về tính di động.</p>
	~[moodle]hostPath luôn làm tăng nguy cơ bảo mật bằng cách cho phép truy cập root vào host.#<p>Mặc dù hostPath có thể gây rủi ro bảo mật nếu không được sử dụng cẩn thận, vấn đề chính được đề cập là nó làm dữ liệu gắn chặt với node.</p>
	####<p><strong>Giải thích</strong>\: hostPath thường là một chống mẫu vì nó có nghĩa là các ứng dụng sẽ hoạt động khác nhau khi một Pod chết và sau đó được lên lịch lại trên một node mới. Điều này ảnh hưởng đến tính di động của Pod.</p>
}

// question: 7.29 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Khi nào việc sử dụng hostPath volume được coi là một trường hợp sử dụng "chuẩn mực" (canonical use case) trong Kubernetes?</p>{
	~[moodle]Để lưu trữ dữ liệu của các cơ sở dữ liệu lớn, phân tán.#<p>Cơ sở dữ liệu thường sử dụng PersistentVolumes được điều phối để đảm bảo tính bền vững và di động.</p>
	~[moodle]Để triển khai các ứng dụng web với yêu cầu lưu trữ tạm thời.#<p>Ứng dụng web tạm thời có thể dùng emptyDir hoặc lưu trữ lớp container.</p>
	=[moodle]Cho các chức năng tiện ích hoặc hành động quản trị yêu cầu truy cập tài nguyên tệp host.
	~[moodle]Để chia sẻ ảnh container giữa các node trong cluster.#<p>Ảnh container được lưu trữ trong Container Registry và bộ nhớ cache cục bộ trên node.</p>
	####<p><strong>Giải thích</strong>\: CSI và CNI, là xương sống cho mạng và lưu trữ của Kubernetes, đều phụ thuộc rất nhiều vào việc sử dụng hostPath. Kubelet tự nó chạy trên mỗi node gắn và hủy gắn các volume lưu trữ, thực hiện các cuộc gọi này thông qua CSI driver và UNIX domain socket được chia sẻ trên host bằng hostPath volume.</p>
}

// question: 7.30 name: Chapter 7: Pod storage and the CSI
::Chapter 7\: Pod storage and the CSI::[html]<p>Chức năng chính của VolumeClaimTemplate trong StatefulSet là gì, đặc biệt trong trường hợp các ứng dụng như Cassandra?</p>{
	~[moodle]VolumeClaimTemplate định nghĩa các chính sách bảo mật cho các volume được gắn vào StatefulSet.#<p>VolumeClaimTemplate định nghĩa yêu cầu lưu trữ, không phải chính sách bảo mật.</p>
	=[moodle]VolumeClaimTemplate cho phép StatefulSet tự động khai báo PersistentVolume với tên dự đoán được cho mỗi bản sao.
	~[moodle]VolumeClaimTemplate cho phép một StatefulSet chia sẻ một PersistentVolume duy nhất giữa tất cả các Pod của nó.#<p>Mỗi bản sao StatefulSet thường có PersistentVolume riêng.</p>
	~[moodle]VolumeClaimTemplate chỉ được sử dụng để cung cấp lưu trữ tạm thời cho các Pod trong StatefulSet.#<p>VolumeClaimTemplate dùng cho lưu trữ bền vững.</p>
	####<p><strong>Giải thích</strong>\: VolumeClaimTemplates là một cấu trúc trong API Kubernetes cho biết Kubernetes cách khai báo PersistentVolume cho StatefulSet. Điều này giúp chúng có thể được tạo tự động, dựa trên kích thước của StatefulSet, bởi một operator cài đặt StatefulSet lần đầu tiên hoặc mở rộng nó.</p>
}

// Chapter 8: Storage implementation and modeling
// question: 8 name: Switch category to $module$/top/Chapter 8: Storage implementation and modeling
$CATEGORY: $module$/top/Chapter 8: Storage implementation and modeling

// question: 8.1 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Khi mô hình hóa lưu trữ trong Kubernetes, câu hỏi quan trọng nhất cần tự hỏi đối với bất kỳ ứng dụng nào cần lưu trữ bền vững là gì?</p>{
	~[moodle]Ứng dụng có thể chạy trên máy ảo hay container?#<p>Đây là câu hỏi về môi trường chạy, không phải yêu cầu lưu trữ.</p>
	=[moodle]Lưu trữ có cần bền vững (durable) hay chỉ là nỗ lực tốt nhất (best effort)?
	~[moodle]Ứng dụng cần bao nhiêu CPU và RAM?#<p>Đây là yêu cầu về tài nguyên tính toán, không phải lưu trữ.</p>
	~[moodle]Lưu trữ cần có giao diện đồ họa người dùng để quản lý không?#<p>Giao diện quản lý lưu trữ không phải là yêu cầu cốt lõi.</p>
	####<p><strong>Giải thích</strong>\: Một trong những câu hỏi quan trọng nhất là "Lưu trữ có cần bền vững (durable) hay chỉ là nỗ lực tốt nhất (best effort)?".</p>
}

// question: 8.2 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Tại sao PersistentVolume (PV) có thể đắt tiền và thường chậm hơn emptyDir volume?</p>{
	~[moodle]PV yêu cầu CSI driver phức tạp và luôn sử dụng SSD.#<p>CSI driver không nhất thiết làm PV đắt, và PV không luôn dùng SSD.</p>
	=[moodle]PV thường yêu cầu một distributed storage controller và có thể liên quan đến network traffic và ghi vào đĩa vật lý.
	~[moodle]PV cần nhiều tài nguyên CPU và bộ nhớ của node hơn emptyDir.#<p>emptyDir có thể dùng tmpfs (RAM) nên rất nhanh, còn PV dùng đĩa nên thường chậm hơn.</p>
	~[moodle]PV chỉ có thể được tạo thủ công, không hỗ trợ dynamic provisioning.#<p>Dynamic provisioning là một tính năng mạnh mẽ của PV.</p>
	####<p><strong>Giải thích</strong>\: PersistentVolume thường đắt tiền. Chúng yêu cầu một distributed storage controller để cấp phát một volume với lượng lưu trữ cụ thể, và dung lượng lưu trữ này có thể bị giới hạn. PersistentVolume có thể chậm hơn emptyDir volume đáng kể vì chúng thường yêu cầu network traffic và ghi vào một loại đĩa nào đó.</p>
}

// question: 8.3 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Dynamic provisioning trong Kubernetes mang lại lợi ích gì cho việc quản lý lưu trữ?</p>{
	~[moodle]Nó cho phép người dùng cấu hình thủ công mọi chi tiết của PersistentVolume.#<p>Dynamic provisioning giảm nhu cầu cấu hình thủ công.</p>
	=[moodle]Nó tự động tạo PersistentVolume khi PersistentVolumeClaim được yêu cầu, dựa trên StorageClass và CSI driver.
	~[moodle]Nó giới hạn các loại lưu trữ có thể được sử dụng trong Kubernetes.#<p>Dynamic provisioning mở rộng các loại lưu trữ có thể sử dụng thông qua CSI.</p>
	~[moodle]Nó loại bỏ hoàn toàn nhu cầu về PersistentVolumeClaim.#<p>Dynamic provisioning hoạt động với PVC để thực hiện yêu cầu lưu trữ.</p>
	####<p><strong>Giải thích</strong>\: Dynamic provisioning, khả năng tự động tạo PersistentVolume khi PVC được tạo, là một tính năng mạnh mẽ.</p>
}

// question: 8.4 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Mục đích của việc sử dụng emptyDir volume với tmpfs (temporary file storage) là gì?</p>{
	~[moodle]Để lưu trữ dữ liệu bền vững mà không bị xóa khi Pod khởi động lại.#<p>emptyDir là tạm thời, dữ liệu bị xóa khi Pod biến mất.</p>
	=[moodle]Để cung cấp bộ nhớ cache hiệu suất cao hoặc không gian làm việc tạm thời nhanh như RAM.
	~[moodle]Để chia sẻ dữ liệu giữa các Pod chạy trên các node khác nhau.#<p>emptyDir là cục bộ trên node, không chia sẻ giữa các node.</p>
	~[moodle]Để bảo vệ dữ liệu nhạy cảm khỏi bị truy cập trái phép.#<p>emptyDir không cung cấp cơ chế bảo mật cho dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: Một volume emptyDir có thể ghi vào bộ nhớ tệp tạm thời (tmpfs) hoặc thậm chí là các volume được ánh xạ bộ nhớ thuần túy, nhanh như RAM theo định nghĩa.</p>
}

// question: 8.5 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Tại sao PersistentVolumeClaim (PVC) ReadWriteOnce lại quan trọng trong việc quản lý truy cập lưu trữ?</p>{
	~[moodle]Nó cho phép nhiều Pod đọc và ghi đồng thời vào cùng một volume.#<p>ReadWriteMany mới cho phép nhiều Pod đọc/ghi đồng thời.</p>
	=[moodle]Nó đảm bảo rằng một volume chỉ được gắn vào một node duy nhất dưới dạng đọc-ghi.
	~[moodle]Nó cho phép volume chỉ được truy cập ở chế độ chỉ đọc.#<p>ReadOnlyMany cho phép chỉ đọc.</p>
	~[moodle]Nó là một volume type chỉ hỗ trợ dynamic provisioning.#<p>ReadWriteOnce là một access mode, không phải volume type, và hoạt động với cả static và dynamic provisioning.</p>
	####<p><strong>Giải thích</strong>\: PersistentVolumeClaim (PVC) là một tham chiếu được đặt tên đến PersistentVolume. Yêu cầu này ràng buộc một volume nếu volume đó thuộc loại RWO (ReadWriteOnce) để các Pod khác không thể sử dụng lại nó cho đến khi volume đó không còn được gắn kết.</p>
}

// question: 8.6 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Vai trò của CSI (Container Storage Interface) trong việc gắn kết các loại lưu trữ tùy ý cho Pod là gì?</p>{
	~[moodle]CSI loại bỏ nhu cầu về các NFS client hoặc GlusterFS client trên các hệ điều hành.#<p>CSI không loại bỏ nhu cầu client, mà là một cách để client được triển khai và tương tác với kubelet.</p>
	=[moodle]CSI cung cấp một giao diện tiêu chuẩn để các driver lưu trữ có thể giao tiếp với kubelet và thực hiện các hoạt động gắn kết hệ thống tệp cấp thấp.
	~[moodle]CSI cho phép kubelet tự động phát hiện và gắn kết bất kỳ loại lưu trữ nào.#<p>CSI cung cấp giao diện, không phải phép màu để kubelet tự động gắn mọi thứ.</p>
	~[moodle]CSI là một storage type mới trong Kubernetes để lưu trữ dữ liệu container.#<p>CSI là một giao diện, không phải loại lưu trữ.</p>
	####<p><strong>Giải thích</strong>\: CSI đã thay đổi điều này, và kubelet ngày càng không còn nhận biết về các filesystem dành riêng cho nền tảng. Thay vào đó, người dùng quan tâm đến việc gắn một loại lưu trữ cụ thể thường chạy một CSI driver dưới dạng DaemonSet trên cluster của họ. Các driver này sử dụng một socket để giao tiếp với kubelet và thực hiện các hoạt động gắn kết filesystem cấp thấp cần thiết.</p>
}

// question: 8.7 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>StorageClass có thể giúp quản trị viên Kubernetes đáp ứng các nhu cầu khác nhau của nhà phát triển như thế nào?</p>{
	=[moodle]StorageClass cho phép quản trị viên định nghĩa các chính sách và loại lưu trữ khác nhau một cách khai báo.
	~[moodle]StorageClass tự động di chuyển dữ liệu giữa các loại lưu trữ khác nhau để tối ưu hóa chi phí.#<p>StorageClass định nghĩa loại lưu trữ, không phải di chuyển dữ liệu.</p>
	~[moodle]StorageClass chỉ được sử dụng để giới hạn số lượng PersistentVolume mà một nhà phát triển có thể yêu cầu.#<p>StorageClass dùng để định nghĩa loại, không phải giới hạn số lượng.</p>
	~[moodle]StorageClass là một phương tiện để sao lưu dữ liệu của ứng dụng vào cloud storage.#<p>StorageClass định nghĩa cách volume được cung cấp, không phải sao lưu.</p>
	####<p><strong>Giải thích</strong>\: StorageClass cho phép bạn thiết kế StorageClasses cho trung tâm dữ liệu của mình để đáp ứng các nhu cầu khác nhau, chẳng hạn như SLA dữ liệu phức tạp, yêu cầu hiệu suất, và ngữ nghĩa bảo mật/đa người thuê.</p>
}

// question: 8.8 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Khi nào Secrets được gắn vào Pod và chúng có thể được sử dụng để làm gì?</p>{
	~[moodle]Secrets được gắn vào Pod sau khi ứng dụng khởi động và được dùng để lưu nhật ký.#<p>Secrets không dùng để lưu nhật ký.</p>
	=[moodle]Secrets được gắn vào Pod khi nó bắt đầu và được dùng để truy cập API server hoặc database credentials.
	~[moodle]Secrets được gắn vào Pod chỉ khi có sự cố và được dùng để khôi phục cấu hình.#<p>Secrets là một phần của cấu hình Pod bình thường, không chỉ khi có sự cố.</p>
	~[moodle]Secrets được gắn vào Pod để lưu trữ container images.#<p>Container images được kéo từ image registries.</p>
	####<p><strong>Giải thích</strong>\: Secrets thường được gắn vào Pod để cấp quyền truy cập vào các dịch vụ như cơ sở dữ liệu hoặc API server. Khi Pod được khởi động, API access token được gắn vào Pod.</p>
}

// question: 8.9 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Tại sao nên disable automountServiceAccountToken thành false nếu Pod không cần ServiceAccount token?</p>{
	~[moodle]Để tăng hiệu suất mạng của Pod.#<p>automountServiceAccountToken không ảnh hưởng trực tiếp đến hiệu suất mạng.</p>
	=[moodle]Để giảm thiểu nguy cơ bảo mật nếu Pod bị xâm nhập.
	~[moodle]Để cho phép Pod sử dụng ServiceAccount khác.#<p>ServiceAccount khác được chỉ định thông qua trường serviceAccountName, không phải tắt automount.</p>
	~[moodle]Để kích hoạt host network cho Pod.#<p>host network được kích hoạt bằng cách đặt hostNetwork: true trong Pod spec.</p>
	####<p><strong>Giải thích</strong>\: Nếu một Pod không cần ServiceAccount token, hãy tắt tính năng gắn token tự động bằng cách đặt automountServiceAccountToken thành false. Điều này làm giảm blast radius (phạm vi thiệt hại) nếu Pod bị tấn công.</p>
}

// question: 8.10 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Tại sao các CNI providers và CSI drivers thường sử dụng hostPath volume?</p>{
	~[moodle]Để lưu trữ các tệp nhật ký của các ứng dụng quản lý mạng.#<p>hostPath có thể dùng cho nhật ký, nhưng đây không phải lý do chính cho CNI/CSI.</p>
	=[moodle]Để tự cài đặt các binary của chúng lên node hoặc gắn các utility dành riêng cho nhà cung cấp.
	~[moodle]Để cung cấp bộ nhớ cache hiệu suất cao cho các dịch vụ mạng.#<p>hostPath không phải là bộ nhớ cache chuyên dụng cho dịch vụ mạng.</p>
	~[moodle]Để đảm bảo rằng các Pod của chúng có địa chỉ IP độc lập.#<p>hostPath không trực tiếp liên quan đến việc cấp phát IP, đó là việc của CNI.</p>
	####<p><strong>Giải thích</strong>\: CNI providers cài đặt chúng vào kubelet bằng cách ghi các binary của chúng từ bên trong container vào chính node. CSI providers cũng sử dụng hostPath để gắn các utility dành riêng cho nhà cung cấp để lưu trữ.</p>
}

// question: 8.11 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Trong trường hợp Cassandra trên Kubernetes, StatefulSet sử dụng VolumeClaimTemplate để làm gì?</p>{
	~[moodle]Để đảm bảo tất cả các Pod Cassandra sử dụng cùng một volume.#<p>StatefulSet thường cung cấp một volume riêng cho mỗi bản sao.</p>
	=[moodle]Để tự động tạo các PersistentVolume với tên dự đoán được cho mỗi bản sao của StatefulSet.
	~[moodle]Để di chuyển volume giữa các node khi Pod bị rescheduled.#<p>VolumeClaimTemplate định nghĩa cách tạo volume, việc di chuyển volume là chức năng của hệ thống lưu trữ và scheduler.</p>
	~[moodle]Để cấp phát lưu trữ tạm thời cho Cassandra khi khởi động.#<p>VolumeClaimTemplate dùng cho lưu trữ bền vững, không phải tạm thời.</p>
	####<p><strong>Giải thích</strong>\: VolumeClaimTemplates là một cấu trúc trong API Kubernetes cho biết Kubernetes cách khai báo PersistentVolume cho StatefulSet. Điều này giúp chúng có thể được tạo tự động, dựa trên kích thước của StatefulSet.</p>
}

// question: 8.12 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Tính năng snapshots và cloning cho volume được triển khai trong Kubernetes thông qua cơ chế nào?</p>{
	~[moodle]Thông qua việc trực tiếp tích hợp logic snapshot của nhà cung cấp vào Kubernetes client.#<p>CSI loại bỏ nhu cầu tích hợp trực tiếp với Kubernetes client.</p>
	=[moodle]Thông qua việc nhà cung cấp lưu trữ triển khai các CSI API calls cụ thể như CreateSnapshot và DeleteSnapshot.
	~[moodle]Thông qua việc sử dụng hostPath volume để sao chép dữ liệu.#<p>hostPath không phải là cơ chế snapshot cho volume.</p>
	~[moodle]Thông qua việc tự động sao lưu dữ liệu vào etcd.#<p>etcd lưu trữ metadata, không phải dữ liệu snapshot.</p>
	####<p><strong>Giải thích</strong>\: Để hỗ trợ tính năng này, một nhà cung cấp lưu trữ chỉ cần triển khai một vài CSI API calls như CreateSnapshot, DeleteSnapshot và ListSnapshots.</p>
}

// question: 8.13 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Định nghĩa nào về PersistentVolumeClaim là đúng?</p>{
	~[moodle]PersistentVolumeClaim (PVC) là một tham chiếu đến PersistentVolume đã được gắn kết vào Pod.#<p>PVC là yêu cầu, không phải tham chiếu đến volume đã gắn.</p>
	~[moodle]PersistentVolumeClaim (PVC) là một tài nguyên cluster-scoped dùng để cung cấp lưu trữ động.#<p>PVC là tài nguyên namespace-scoped.</p>
	=[moodle]PersistentVolumeClaim (PVC) là một yêu cầu về tài nguyên lưu trữ của Pod, được ràng buộc với một PersistentVolume cụ thể.
	~[moodle]PersistentVolumeClaim (PVC) là một volume được quản lý bởi kubelet trên mỗi node.#<p>PVC là API object, không phải volume được kubelet quản lý trực tiếp.</p>
	####<p><strong>Giải thích</strong>\: PersistentVolumeClaim (PVC) là một tham chiếu được đặt tên đến PersistentVolume. Yêu cầu này ràng buộc một volume nếu volume đó thuộc loại RWO (read-write-once).</p>
}

// question: 8.14 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Tại sao copy-on-write filesystems (được sử dụng bởi các lớp container) có thể gây performance hit khi ghi tệp?</p>{
	~[moodle]Vì chúng yêu cầu nén dữ liệu liên tục.#<p>Copy-on-write không liên quan đến nén dữ liệu.</p>
	=[moodle]Vì chúng phải sao chép tệp từ lớp dưới lên lớp trên trước khi sửa đổi.
	~[moodle]Vì chúng luôn mã hóa dữ liệu trước khi ghi.#<p>Copy-on-write không mã hóa dữ liệu.</p>
	~[moodle]Vì chúng phải giao tiếp qua mạng với storage controller.#<p>Copy-on-write là hoạt động cục bộ trên đĩa của node.</p>
	####<p><strong>Giải thích</strong>\: Copy-on-write filesystems thường chậm (và có khả năng tốn CPU) so với các hoạt động filesystem gốc. Điều này xảy ra khi một container muốn sửa đổi hoặc xóa một tệp tồn tại ở một trong các lớp dưới nhưng không có trong upperdir.</p>
}

// question: 8.15 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Các StorageClasses và GatewayClasses được so sánh với nhau như thế nào trong bối cảnh các API trung lập với nhà cung cấp (vendor-neutral APIs) trong Kubernetes?</p>{
	~[moodle]Cả hai đều định nghĩa các quy tắc bảo mật cho luồng dữ liệu.#<p>StorageClasses định nghĩa lưu trữ, GatewayClasses định nghĩa truy cập mạng lớp 7. Cả hai có thể ảnh hưởng đến bảo mật, nhưng đó không phải là định nghĩa chính của chúng.</p>
	=[moodle]Cả hai đều định nghĩa một loại điểm truy cập tài nguyên hạ tầng mà nhà phát triển có thể yêu cầu.
	~[moodle]StorageClasses dành cho lưu trữ phân tán, còn GatewayClasses dành cho lưu trữ cục bộ.#<p>StorageClasses không chỉ dành cho lưu trữ phân tán, và GatewayClasses không dành cho lưu trữ.</p>
	~[moodle]StorageClasses là để cấp phát tài nguyên CPU, còn GatewayClasses là để cấp phát tài nguyên bộ nhớ.#<p>StorageClasses và GatewayClasses không liên quan đến CPU hoặc bộ nhớ.</p>
	####<p><strong>Giải thích</strong>\: GatewayClasses tương tự như StorageClasses cho CSI ở một số khía cạnh, vì chúng định nghĩa một loại điểm truy cập vào mạng. StorageClasses cũng định nghĩa một loại tài nguyên lưu trữ.</p>
}

// question: 8.16 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Tại sao việc giữ etcd dưới 8GB dung lượng lưu trữ là một khuyến nghị quan trọng trong Kubernetes?</p>{
	=[moodle]etcd không được thiết kế để lưu trữ dữ liệu ứng dụng lớn, mà là metadata cấu hình.
	~[moodle]etcd sẽ tự động xóa dữ liệu vượt quá 8GB.#<p>etcd không tự động xóa dữ liệu, nhưng có thể gặp vấn đề về hiệu suất.</p>
	~[moodle]Kubelet không thể truy cập etcd nếu nó vượt quá giới hạn này.#<p>etcd vẫn có thể truy cập nhưng hiệu suất sẽ bị ảnh hưởng.</p>
	~[moodle]Việc này cải thiện hiệu suất của các hoạt động đọc/ghi etcd một cách đáng kể.#<p>etcd được thiết kế cho sự nhất quán và điều phối, không phải là cơ sở dữ liệu hiệu suất cao cho dữ liệu ứng dụng lớn.</p>
	####<p><strong>Giải thích</strong>\: Giới hạn dung lượng lưu trữ mặc định là 2GB, và khuyến nghị rằng hầu hết cơ sở dữ liệu etcd nên dưới 8GB. etcd không được thiết kế để lưu trữ các kiểu dữ liệu lớn vô hạn, mà là để xử lý các cặp khóa/giá trị nhỏ điển hình cho cấu hình và metadata trạng thái của các hệ thống phân tán.</p>
}

// question: 8.17 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Khía cạnh Advanced storage functionality trong mô hình lưu trữ Kubernetes bao gồm những gì?</p>{
	~[moodle]Chỉ hỗ trợ các loại volume có sẵn trong cây nhân Kubernetes.#<p>Advanced storage functionality hướng đến việc sử dụng CSI để hỗ trợ các loại volume ngoài cây nhân.</p>
	=[moodle]Khả năng tạo snapshots và cloning (nhân bản) các đĩa.
	~[moodle]Tích hợp Docker overlay filesystem với PersistentVolumes.#<p>Docker overlay filesystem là lưu trữ tạm thời của container, không phải PersistentVolumes.</p>
	~[moodle]Khả năng giám sát network traffic đến các storage volumes.#<p>Network traffic đến storage volumes là một khía cạnh của mạng, không phải chức năng lưu trữ nâng cao của volume.</p>
	####<p><strong>Giải thích</strong>\: Kể từ Kubernetes 1.17, snapshots và cloning (có thể được triển khai hoàn toàn trong Kubernetes) đang nổi lên như các hoạt động mới trong Kubernetes API.</p>
}

// question: 8.18 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Khi nào một StorageClass với provisioner là rancher.io/local-path thường được sử dụng?</p>{
	~[moodle]Trong các môi trường sản xuất quy mô lớn để cung cấp lưu trữ phân tán.#<p>rancher.io/local-path không được thiết kế cho lưu trữ phân tán quy mô lớn trong sản xuất.</p>
	=[moodle]Trong các cluster kind hoặc môi trường phát triển cục bộ để cung cấp lưu trữ động đơn giản.
	~[moodle]Để kết nối với các hệ thống SAN hoặc NAS bên ngoài.#<p>rancher.io/local-path dùng local path, không phải kết nối SAN/NAS.</p>
	~[moodle]Để cấp phát volume dựa trên bộ nhớ (RAM-backed volumes).#<p>emptyDir với tmpfs mới là RAM-backed volumes.</p>
	####<p><strong>Giải thích</strong>\: rancher.io/local-path là một provisioner thường đi kèm với kind và được dùng cho các cluster kind hoặc môi trường cục bộ để cung cấp local storage động.</p>
}

// question: 8.19 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>PodDisruptionBudget (PDB) có vai trò gì trong bối cảnh quản lý ứng dụng StatefulSet như CockroachDB?</p>{
	~[moodle]PDB đảm bảo rằng StatefulSet có thể hoạt động mà không cần lưu trữ.#<p>PDB liên quan đến sự gián đoạn của Pod, không phải khả năng hoạt động không lưu trữ.</p>
	=[moodle]PDB giúp duy trì số lượng tối thiểu các Pod có sẵn của một StatefulSet trong quá trình gián đoạn không tự nguyện.
	~[moodle]PDB tự động mở rộng hoặc thu nhỏ số lượng Pod dựa trên tải.#<p>Autoscaling là chức năng mở rộng/thu nhỏ Pod.</p>
	~[moodle]PDB bảo vệ dữ liệu khỏi bị hỏng khi node bị lỗi.#<p>PDB giảm thiểu gián đoạn, nhưng không trực tiếp bảo vệ dữ liệu khỏi hỏng hóc; việc đó là của hệ thống lưu trữ và ứng dụng.</p>
	####<p><strong>Giải thích</strong>\: PodDisruptionBudget (PDB) là một API object giúp duy trì tính sẵn sàng của ứng dụng bằng cách giới hạn số lượng Pod của một Deployment hoặc StatefulSet có thể bị gián đoạn không tự nguyện.</p>
}

// question: 8.20 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Việc tắt swap trong Kubernetes (ví dụ: —fail-swap-on=false hoặc không cho phép hệ điều hành sử dụng swap) có ý nghĩa gì đối với hiệu suất bộ nhớ?</p>{
	~[moodle]Tắt swap cho phép hệ điều hành sử dụng swap khi cần, cải thiện khả năng đóng gói Pod.#<p>--fail-swap-on=false là một cờ để kubelet có thể khởi động ngay cả khi swap được bật, nhưng khuyến nghị chung là tắt swap.</p>
	=[moodle]Tắt swap đảm bảo rằng việc truy cập bộ nhớ của Pod không bị chậm do swap ra đĩa.
	~[moodle]Tắt swap cho phép kubelet tự động điều chỉnh giới hạn bộ nhớ của Pod.#<p>kubelet không tự động điều chỉnh giới hạn bộ nhớ qua swap.</p>
	~[moodle]Tắt swap là một biện pháp bảo mật để ngăn chặn container escape.#<p>Tắt swap chủ yếu là về hiệu suất, không phải bảo mật container escape.</p>
	####<p><strong>Giải thích</strong>\: Tắt swap đảm bảo hiệu suất bộ nhớ nhất quán và không có biến động do hệ điều hành sử dụng swap ra đĩa.</p>
}

// question: 8.21 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Làm thế nào NodeAffinity ảnh hưởng đến quá trình scheduling Pod trong Kubernetes?</p>{
	~[moodle]NodeAffinity buộc Pod phải chạy trên một node bất kỳ trong cluster.#<p>NodeAffinity không buộc chạy bất kỳ node nào.</p>
	=[moodle]NodeAffinity ưu tiên hoặc yêu cầu Pod phải chạy trên các node có nhãn (labels) phù hợp.
	~[moodle]NodeAffinity là một cách để cấm Pod chạy trên một số node nhất định.#<p>NodeTaints cấm Pod chạy trên node, NodeAffinity là ưu tiên/yêu cầu.</p>
	~[moodle]NodeAffinity tự động tạo node mới nếu không có node nào phù hợp.#<p>NodeAffinity không tạo node, đó là nhiệm vụ của Cluster API hoặc các công cụ provisioning.</p>
	####<p><strong>Giải thích</strong>\: NodeAffinity là một plugin Filter trong scheduler framework kiểm tra các ràng buộc về node như nhãn (labels), đảm bảo Pod được lên lịch trên node phù hợp.</p>
}

// question: 8.22 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Khi một StorageClass được định nghĩa với reclaimPolicy: Delete, điều gì sẽ xảy ra với PersistentVolume và dữ liệu khi PersistentVolumeClaim tương ứng bị xóa?</p>{
	~[moodle]PersistentVolume sẽ vẫn tồn tại, nhưng dữ liệu sẽ bị xóa.#<p>PersistentVolume cũng sẽ bị xóa.</p>
	=[moodle]PersistentVolume và tất cả dữ liệu liên quan sẽ bị xóa.
	~[moodle]PersistentVolume sẽ được giữ lại, và dữ liệu cũng được giữ lại.#<p>reclaimPolicy: Retain mới giữ lại volume và dữ liệu.</p>
	~[moodle]PersistentVolume sẽ được đặt ở trạng thái Pending.#<p>Pending là trạng thái chờ được cấp phát, không liên quan đến reclaim policy.</p>
	####<p><strong>Giải thích</strong>\: reclaimPolicy: Delete có nghĩa là PersistentVolume và storage liên quan sẽ bị xóa hoàn toàn khi PersistentVolumeClaim tương ứng bị xóa.</p>
}

// question: 8.23 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Lý do chính để sử dụng VolumeClaimTemplate trong StatefulSet so với việc định nghĩa các PersistentVolumeClaim riêng lẻ là gì?</p>{
	~[moodle]VolumeClaimTemplate cho phép StatefulSet chạy trên nhiều namespace khác nhau.#<p>StatefulSet không chạy trên nhiều namespace theo cách đó.</p>
	=[moodle]VolumeClaimTemplate đơn giản hóa việc quản lý và mở rộng StatefulSet bằng cách tự động tạo PVC được đặt tên phù hợp cho mỗi bản sao.
	~[moodle]VolumeClaimTemplate tăng cường bảo mật bằng cách ẩn các chi tiết của PersistentVolume khỏi người dùng.#<p>VolumeClaimTemplate chủ yếu để quản lý, không phải ẩn thông tin bảo mật.</p>
	~[moodle]VolumeClaimTemplate chỉ được hỗ trợ bởi các CSI driver cụ thể.#<p>VolumeClaimTemplate là một tính năng của Kubernetes API, hoạt động với bất kỳ CSI driver hoặc storage provisioner nào.</p>
	####<p><strong>Giải thích</strong>\: VolumeClaimTemplate đơn giản hóa việc quản lý và mở rộng StatefulSet bằng cách tự động tạo PVC được đặt tên phù hợp cho mỗi bản sao, loại bỏ nhu cầu tạo PVC thủ công.</p>
}

// question: 8.24 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Tại sao việc tắt Transparent HugePages có thể tạo ra sự khác biệt về hiệu suất trên các hệ điều hành cụ thể?</p>{
	~[moodle]Transparent HugePages luôn cải thiện hiệu suất cho tất cả các ứng dụng.#<p>Transparent HugePages không phải lúc nào cũng cải thiện hiệu suất.</p>
	=[moodle]Việc tắt Transparent HugePages có thể ngăn chặn các vấn đề hiệu suất đối với một số ứng dụng sử dụng bộ nhớ lớn không hiệu quả.
	~[moodle]Transparent HugePages gây ra network latency cho các Pod.#<p>Transparent HugePages liên quan đến bộ nhớ, không phải network latency.</p>
	~[moodle]Transparent HugePages chỉ liên quan đến hiệu suất CPU, không phải bộ nhớ.#<p>Transparent HugePages liên quan đến quản lý bộ nhớ.</p>
	####<p><strong>Giải thích</strong>\: Tắt Transparent HugePages có thể tạo ra sự khác biệt về hiệu suất cho bạn trên các hệ điều hành cụ thể. Một số ứng dụng hiệu suất cao sử dụng HugePages một cách rõ ràng.</p>
}

// question: 8.25 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Điều gì sẽ xảy ra nếu một Pod yêu cầu một volume chỉ cho phép một người đọc đồng thời, nhưng một Pod hiện có đã truy cập vào volume đó?</p>{
	~[moodle]Scheduler sẽ vẫn lên lịch Pod mới, sau đó kubelet sẽ cố gắng tranh giành quyền truy cập.#<p>Scheduler đủ thông minh để tránh điều này.</p>
	=[moodle]Scheduler sẽ chủ động tránh lên lịch Pod mới trên các node có volume đó để ngăn lỗi khởi động Pod.
	~[moodle]API server sẽ tạo một bản sao của volume cho Pod mới.#<p>API server không tạo bản sao volume theo cách này.</p>
	~[moodle]Container runtime sẽ cho phép cả hai Pod truy cập volume ở chế độ chỉ đọc.#<p>Container runtime không có quyền bỏ qua các access mode của volume.</p>
	####<p><strong>Giải thích</strong>\: Scheduler chủ động tránh lên lịch một Pod phụ thuộc vào một volume chỉ cho phép một người đọc đồng thời trong trường hợp một Pod hiện có đã truy cập vào volume đó. Điều này ngăn chặn các lỗi khởi động Pod.</p>
}

// question: 8.26 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Ba phương pháp chính mà quản trị viên đã sử dụng để giải quyết vấn đề truy cập cơ sở dữ liệu trong môi trường cloud là gì?</p>{
	~[moodle]Sao chép trực tiếp thông tin xác thực vào Dockerfile.#<p>Sao chép thông tin xác thực vào Dockerfile là một security anti-pattern.</p>
	~[moodle]Truy cập cơ sở dữ liệu với password hardcoded trong source code.#<p>Hardcoding password là một security anti-pattern lớn.</p>
	=[moodle]Sử dụng ConfigMaps, Secrets hoặc sidecar containers với các công cụ như Kiam hoặc Kube2iam.
	~[moodle]Gắn kết volume trực tiếp từ database server vào Pod.#<p>Mounting volume trực tiếp từ database server không phải là cách điển hình để truy cập cơ sở dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: Quản trị viên đã giải quyết vấn đề này bằng ba cách: 1) ConfigMaps cho thông tin cấu hình không nhạy cảm, 2) Secrets cho mật khẩu và chứng chỉ, và 3) sidecar containers với các công cụ như Kiam hoặc Kube2iam.</p>
}

// question: 8.27 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Ưu điểm chính của việc sử dụng các StorageClass khác nhau cho heterogeneous workloads (khối lượng công việc không đồng nhất) là gì?</p>{
	~[moodle]Để đảm bảo tất cả các ứng dụng đều sử dụng cùng một loại lưu trữ nhằm đơn giản hóa quản lý.#<p>Heterogeneous workloads thường cần các loại lưu trữ khác nhau.</p>
	=[moodle]Để cho phép chọn các storage models khác nhau và triển khai các chính sách cụ thể cho từng loại khối lượng công việc.
	~[moodle]Để giảm thiểu chi phí bằng cách luôn chọn StorageClass rẻ nhất.#<p>StorageClass có thể được dùng để tối ưu chi phí, nhưng không phải là lợi ích chính của việc dùng StorageClass khác nhau.</p>
	~[moodle]Để loại bỏ hoàn toàn nhu cầu về PersistentVolumeClaim.#<p>StorageClass là một phần của quy trình PVC.</p>
	####<p><strong>Giải thích</strong>\: Đối với heterogeneous workloads, khả năng lựa chọn giữa các storage models khác nhau và triển khai các chính sách (hoặc Operators) xung quanh việc fulfillment PVC trở nên ngày càng quan trọng.</p>
}

// question: 8.28 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Trong kiến trúc Kubernetes, ai chịu trách nhiệm bind (ràng buộc) một PersistentVolume (PV) với một PersistentVolumeClaim (PVC) đã được cấp phát?</p>{
	~[moodle]Kubelet.#<p>Kubelet gắn PV đã được bind vào Pod.</p>
	~[moodle]API server.#<p>API server lưu trữ các đối tượng, nhưng control plane thực hiện logic binding.</p>
	=[moodle]Kubernetes control plane.
	~[moodle]Storage provisioner.#<p>Storage provisioner tạo PV, nhưng control plane thực hiện binding.</p>
	####<p><strong>Giải thích</strong>\: Trong Kubernetes core, nếu một volume tồn tại đáp ứng nhu cầu của một PVC, thì một sự kiện binding sẽ xảy ra. Đây là chức năng của Kubernetes control plane.</p>
}

// question: 8.29 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Nếu bạn cần chạy một ứng dụng legacy (kế thừa) có yêu cầu hardware hoặc software đặc biệt khó containerize, thì Kubernetes có thể là lựa chọn không phù hợp vì lý do gì?</p>{
	~[moodle]Kubernetes không hỗ trợ bất kỳ ứng dụng legacy nào.#<p>Kubernetes có thể chạy các ứng dụng legacy nhưng có thể không tối ưu.</p>
	=[moodle]Container hóa ứng dụng legacy có thể không mang lại nhiều lợi thế.
	~[moodle]Kubernetes chỉ hoạt động với các application containers nhỏ.#<p>Kubernetes có thể chạy các container lớn nhưng phức tạp.</p>
	~[moodle]Kubernetes sẽ tự động sửa đổi application code để phù hợp với container.#<p>Kubernetes không sửa đổi application code.</p>
	####<p><strong>Giải thích</strong>\: Một số ứng dụng có các yêu cầu về hardware, software và latency khiến việc containerize chúng trở nên khó khăn. Ví dụ, bạn có thể có các ứng dụng đã mua từ một công ty phần mềm không chính thức hỗ trợ chạy trong container hoặc chạy ứng dụng của họ trong một Kubernetes cluster.</p>
}

// question: 8.30 name: Chapter 8: Storage implementation and modeling
::Chapter 8\: Storage implementation and modeling::[html]<p>Kubernetes được sinh ra từ các phương pháp tiếp cận configuration-driven và container-driven trước đó. Điều này ám chỉ điều gì về thiết kế của nó?</p>{
	~[moodle]Kubernetes là một hệ thống hoàn toàn mới, không có liên kết với công nghệ cũ.#<p>Kubernetes là sự tiến hóa, không phải hoàn toàn mới.</p>
	=[moodle]Kubernetes kế thừa và cải thiện các khái niệm từ các giải pháp quản lý container và cấu hình trước đó.
	~[moodle]Kubernetes chỉ hỗ trợ containerization dựa trên Docker.#<p>Kubernetes đã chuyển từ sự phụ thuộc Docker sang CRI.</p>
	~[moodle]Kubernetes loại bỏ hoàn toàn nhu cầu về các tệp cấu hình.#<p>Kubernetes dựa rất nhiều vào các tệp cấu hình YAML hoặc JSON.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes được sinh ra từ các phương pháp tiếp cận configuration-driven và container-driven trước đó. Điều này có nghĩa là nó đã xây dựng dựa trên những kinh nghiệm và công nghệ đã có.</p>
}

// Chapter 9: Running Pods: How the kubelet works
// question: 9 name: Switch category to $module$/top/Chapter 9: Running Pods: How the kubelet works
$CATEGORY: $module$/top/Chapter 9: Running Pods: How the kubelet works

// question: 9.1 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Vai trò chính của kubelet trong một Kubernetes cluster là gì?</p>{
	~[moodle]Kubelet là bộ não của Kubernetes control plane, chịu trách nhiệm scheduling Pods trên toàn cluster.#<p>Control plane là bộ não và scheduler chịu trách nhiệm scheduling trên toàn cluster.</p>
	=[moodle]Kubelet là một node agent và Pod scheduler cục bộ, chạy trên mỗi node và quản lý vòng đời của workloads.
	~[moodle]Kubelet là một giao diện cho phép các nhà cung cấp lưu trữ cắm giải pháp của họ vào Kubernetes.#<p>CSI là giao diện cho lưu trữ.</p>
	~[moodle]Kubelet chịu trách nhiệm cung cấp địa chỉ IP cho Pods và tạo mạng Pod.#<p>CNI provider chịu trách nhiệm cung cấp địa chỉ IP cho Pods và tạo mạng Pod.</p>
	####<p><strong>Giải thích</strong>\: Kubelet là workhorse (con ngựa thồ) của một Kubernetes cluster, chạy trên mỗi node và là Pod scheduler và node agent, nhưng chỉ cho node cục bộ. Nó giám sát và duy trì thông tin về máy chủ nó đang chạy.</p>
}

// question: 9.2 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Container Runtime Interface (CRI) đóng vai trò gì đối với kubelet?</p>{
	~[moodle]CRI là một công cụ command-line để quản lý Docker images.#<p>runc là một container runtime, không phải công cụ command-line cho Docker images.</p>
	=[moodle]CRI là giao diện mà kubelet sử dụng để tương tác với các container runtimes như containerd hoặc runc.
	~[moodle]CRI chịu trách nhiệm networking và storage cho Pods.#<p>CNI và CSI chịu trách nhiệm networking và storage.</p>
	~[moodle]CRI là một abstraction của kubelet để quản lý Pod lifecycle.#<p>GenericRuntimeManager là abstraction của kubelet.</p>
	####<p><strong>Giải thích</strong>\: CRI là giao diện mà kubelet sử dụng để tương tác với các container runtimes. Ví dụ, containerd được phân loại là container runtime vì nó lấy một image và tạo ra một running container.</p>
}

// question: 9.3 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Tại sao kubelet được thiết kế để khá "chatty" (nói nhiều) với API server trong các phiên bản Kubernetes cũ hơn?</p>{
	~[moodle]Để API server có thể liên tục gửi các lệnh mới đến kubelet.#<p>API server gửi lệnh nhưng chatty để báo cáo trạng thái.</p>
	=[moodle]Vì control plane cần biết node có khỏe mạnh hay không để lên lịch Pods.
	~[moodle]Để kubelet đồng bộ hóa filesystem của nó với API server.#<p>kubelet không đồng bộ hóa filesystem với API server.</p>
	~[moodle]Để giảm thiểu network traffic trong cluster.#<p>Chatty làm tăng network traffic, không giảm.</p>
	####<p><strong>Giải thích</strong>\: Theo thiết kế, kubelet khá "chatty" với API server vì control plane trong một cluster cần biết node có khỏe mạnh hay không. Trong các phiên bản cũ hơn của Kubernetes (trước 1.17), Node object được cập nhật trong một status loop mỗi 10 giây thông qua kubelet gọi API server.</p>
}

// question: 9.4 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Trong các phiên bản Kubernetes 1.17 trở đi, cơ chế nào đã được triển khai để tối ưu hóa hiệu suất của các cluster lớn và giảm sự "chatty" của kubelet với API server?</p>{
	~[moodle]Kubelet ngừng gửi heartbeat đến API server.#<p>Kubelet vẫn gửi heartbeat nhưng thông qua Lease object nhỏ gọn.</p>
	=[moodle]Kubernetes triển khai một API server endpoint cụ thể để quản lý kubelet thông qua leasing mechanism của etcd.
	~[moodle]Kubelet chuyển sang sử dụng UDP thay vì TCP để giao tiếp với API server.#<p>Kubernetes API sử dụng HTTP/REST, thường chạy trên TCP.</p>
	~[moodle]API server gửi các batch update cho kubelet mỗi giờ.#<p>Heartbeat vẫn định kỳ, nhưng dữ liệu ít hơn.</p>
	####<p><strong>Giải thích</strong>\: Để tối ưu hóa hiệu suất của các cluster lớn và giảm sự "chatty" của mạng, các phiên bản Kubernetes 1.17 trở lên triển khai một API server endpoint cụ thể để quản lý kubelet thông qua leasing mechanism của etcd.</p>
}

// question: 9.5 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Khi một Pod được tạo, kubelet sẽ làm gì với tệp /etc/resolv.conf bên trong container của Pod?</p>{
	~[moodle]Kubelet xóa tệp /etc/resolv.conf để ngăn Pod truy cập DNS.#<p>Pod cần DNS để hoạt động.</p>
	=[moodle]Kubelet tạo và gắn kết tệp /etc/resolv.conf để Pod có thể thực hiện DNS lookup.
	~[moodle]Kubelet sao chép tệp /etc/resolv.conf từ host vào Pod mà không sửa đổi.#<p>Kubelet tạo một tệp resolv.conf cụ thể cho Pod với các thông tin DNS của cluster.</p>
	~[moodle]Kubelet yêu cầu Container runtime tạo tệp /etc/resolv.conf.#<p>Kubelet chịu trách nhiệm tạo tệp này, không ủy quyền cho Container runtime.</p>
	####<p><strong>Giải thích</strong>\: Kubelet, khi tạo một Pod, sẽ tạo và gắn tệp resolv.conf. Điều này cho phép Pod thực hiện DNS lookup.</p>
}

// question: 9.6 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Đâu là một ví dụ về một trong số kubelet configuration options có trong tệp types.go, liên quan đến quản lý DNS?</p>{
	~[moodle]ImageMinimumGCAge.#<p>ImageMinimumGCAge liên quan đến garbage collection của image.</p>
	~[moodle]EvictionHard.#<p>EvictionHard liên quan đến giới hạn cứng khi Pod bị xóa.</p>
	=[moodle]ClusterDNS.
	~[moodle]ContainerRuntimeEndpoint.#<p>ContainerRuntimeEndpoint là một cờ command-line cho kubelet, không phải API value trong types.go.</p>
	####<p><strong>Giải thích</strong>\: ClusterDNS là một danh sách các địa chỉ IP cho DNS server của cluster. Nếu được đặt, kubelet sẽ cấu hình tất cả các container sử dụng nó để phân giải DNS.</p>
}

// question: 9.7 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Pause container đóng vai trò gì trong quá trình tạo Pod của kubelet?</p>{
	~[moodle]Pause container là image ứng dụng chính chạy trong Pod.#<p>Pause container là placeholder, không phải image ứng dụng chính.</p>
	=[moodle]Pause container tạo ra một network namespace và filesystem dùng chung cho tất cả các container trong một Pod.
	~[moodle]Pause container chịu trách nhiệm pull images từ registry.#<p>ImageService của CRI chịu trách nhiệm pull images.</p>
	~[moodle]Pause container giám sát CPU và memory usage của Pod.#<p>cgroups và ContainerMetricsGetter giám sát CPU và memory usage.</p>
	####<p><strong>Giải thích</strong>\: Pause container tạo ra một network namespace và filesystem dùng chung cho tất cả các container trong một Pod.</p>
}

// question: 9.8 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Tại sao Kubernetes đang loại bỏ native Docker support và chuyển sang Container Runtime Interface (CRI)?</p>{
	~[moodle]Docker không còn được sử dụng trong môi trường sản xuất.#<p>Docker vẫn được sử dụng rộng rãi, đặc biệt trong phát triển.</p>
	=[moodle]CRI cho phép Kubernetes trở nên vendor-neutral và hỗ trợ nhiều container runtimes khác nhau.
	~[moodle]Docker không đủ an toàn cho Kubernetes.#<p>CRI không phải là về bảo mật mà là về abstraction.</p>
	~[moodle]CRI cung cấp hiệu suất cao hơn Docker đối với network I/O.#<p>CRI là giao diện, không phải runtime cụ thể để có hiệu suất network I/O cao hơn.</p>
	####<p><strong>Giải thích</strong>\: CRI là một giao diện gRPC, Kubernetes đặt mục tiêu di chuyển logic container runtime ra khỏi Kubernetes core theo thời gian. kubelet có thể điều chỉnh nhiều triển khai containerization khác nhau (container VM, container gVisor, v.v.). Docker đã bị deprecated.</p>
}

// question: 9.9 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>GenericRuntimeManager của kubelet đóng vai trò gì trong việc trừu tượng hóa CRI?</p>{
	~[moodle]GenericRuntimeManager là một container runtime thay thế containerd.#<p>GenericRuntimeManager là một abstraction, không phải container runtime.</p>
	=[moodle]GenericRuntimeManager cung cấp một wrapper cho bất kỳ CRI provider nào, quản lý các cuộc gọi đến bốn CRI interfaces cốt lõi.
	~[moodle]GenericRuntimeManager chịu trách nhiệm pull images từ Docker Hub.#<p>ImageService của CRI chịu trách nhiệm pull images.</p>
	~[moodle]GenericRuntimeManager là một công cụ command-line để kiểm tra trạng thái của container.#<p>kubectl là công cụ command-line chính.</p>
	####<p><strong>Giải thích</strong>\: Kubelet cung cấp một Runtime interface, được triển khai bởi kuberuntime.NewKubeGenericRuntimeManager, như một wrapper cho bất kỳ CRI provider nào (containerd, CRI-O, Docker, v.v.). Runtime manager này quản lý tất cả các cuộc gọi đến bốn CRI interfaces cốt lõi.</p>
}

// question: 9.10 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Bốn interfaces cấp cao mà CRI bao gồm để hợp nhất tất cả các chức năng cốt lõi mà Kubernetes cần để chạy container là gì?</p>{
	~[moodle]ImageService, NetworkService, StorageService, ProcessService.#<p>NetworkService và StorageService không phải là tên interface trong CRI.</p>
	=[moodle]PodSandBoxManager, ContainerRuntime, ImageService, ContainerMetricsGetter.
	~[moodle]KubeletManager, SchedulerManager, ControllerManager, APIServerManager.#<p>Manager ở đây là các thành phần của control plane, không phải CRI interfaces.</p>
	~[moodle]GetInfo, CreateContainer, StartContainer, StopContainer.#<p>Đây là các gRPC calls cho ContainerRuntime và Identity service, không phải interfaces cấp cao.</p>
	####<p><strong>Giải thích</strong>\: CRI bao gồm bốn interfaces cấp cao: PodSandBoxManager, ContainerRuntime, ImageService, và ContainerMetricsGetter.</p>
}

// question: 9.11 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Trong quy trình Pod creation, sau khi scheduler tìm được home phù hợp cho Pod, bước tiếp theo mà kubelet thực hiện là gì?</p>{
	~[moodle]Kubelet gửi heartbeat đến API server.#<p>Heartbeat là một hoạt động liên tục, không phải bước tiếp theo cụ thể trong quy trình tạo Pod.</p>
	=[moodle]Kubelet tạo cgroups cho container mà không khởi động nó.
	~[moodle]Kubelet yêu cầu CRI provider khởi động container.#<p>Kubelet sẽ gọi CRI để khởi động container sau khi cgroups và namespaces được thiết lập.</p>
	~[moodle]Kubelet tải application code vào Pod.#<p>Application code nằm trong image, kubelet kéo image.</p>
	####<p><strong>Giải thích</strong>\: Kubelet tạo cgroups cho container mà không khởi động container.</p>
}

// question: 9.12 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>ImagePullSecrets được sử dụng để làm gì trong Kubernetes?</p>{
	~[moodle]ImagePullSecrets được dùng để bảo mật container runtime trên node.#<p>ImagePullSecrets không bảo mật container runtime.</p>
	=[moodle]ImagePullSecrets cung cấp thông tin xác thực cho kubelet để pull images từ các registry riêng tư.
	~[moodle]ImagePullSecrets là Secret lưu trữ Dockerfiles.#<p>Secrets nói chung không lưu trữ Dockerfiles.</p>
	~[moodle]ImagePullSecrets cho phép Pod chia sẻ volume một cách an toàn.#<p>Volume được chia sẻ thông qua PersistentVolumes hoặc emptyDir.</p>
	####<p><strong>Giải thích</strong>\: ImagePullSecrets là Secret có thông tin xác thực của registry mà kubelet sử dụng để pull image.</p>
}

// question: 9.13 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Tại sao kubelet cần một Container Runtime Interface (CRI) provider và một CNI provider để thực hiện công việc thực sự?</p>{
	~[moodle]CRI provider cung cấp network policies, và CNI provider quản lý DNS.#<p>Network policies được quản lý bởi CNI hoặc các công cụ ngoài CNI, DNS bởi CoreDNS.</p>
	=[moodle]CRI provider chịu trách nhiệm chạy container, và CNI provider cấp phát IP address.
	~[moodle]CRI provider quản lý storage volumes, và CNI provider scheduling Pods.#<p>CSI quản lý storage, scheduler scheduling Pods.</p>
	~[moodle]CRI provider thực hiện health checks, và CNI provider logging.#<p>Health checks là một phần của Pod lifecycle, logging là một dịch vụ.</p>
	####<p><strong>Giải thích</strong>\: Kubelet không thể thực hiện công việc thực sự nếu không có cả CNI provider và container runtime có thể truy cập thông qua Container Runtime Interface (CRI). CNI cuối cùng phục vụ nhu cầu của CRI, sau đó CRI khởi động và dừng container.</p>
}

// question: 9.14 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Khi nào Pod có thể bị rescheduled sang một node mới?</p>{
	=[moodle]Khi container của Pod chết hoặc health check của nó thất bại.
	~[moodle]Khi node hiện tại bị quá tải CPU nhưng vẫn khỏe mạnh.#<p>Rescheduling là do sự cố, không phải quá tải CPU đơn thuần.</p>
	~[moodle]Khi kubelet trên node quyết định tự di chuyển Pod.#<p>Kubelet quản lý Pod trên node đó, scheduler quyết định reschedule.</p>
	~[moodle]Pod không bao giờ bị rescheduled nếu nó đã bắt đầu.#<p>Pod có thể bị rescheduled do nhiều lý do.</p>
	####<p><strong>Giải thích</strong>\: Nếu có điều gì đó không ổn, chẳng hạn như container chết hoặc health check của nó thất bại, chính Pod có thể được di chuyển đến một node mới. Điều này được gọi là rescheduling.</p>
}

// question: 9.15 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Điều gì sẽ xảy ra nếu kubelet không thể kết nối với control plane khi nó khởi động?</p>{
	~[moodle]Kubelet sẽ tự động chuyển sang chế độ offline và chạy các Pod cục bộ.#<p>Kubelet không có chế độ offline để chạy Pods cục bộ mà không control plane.</p>
	=[moodle]Kubelet sẽ liên tục cố gắng giao tiếp với control plane cho đến khi nó có sẵn.
	~[moodle]Kubelet sẽ tự động shutdown để tránh resource contention.#<p>Kubelet sẽ chờ control plane.</p>
	~[moodle]Kubelet sẽ chỉ khởi động các static Pods đã được định cấu hình sẵn.#<p>Static Pods được kubelet quản lý độc lập, nhưng kubelet vẫn cố gắng kết nối control plane cho các Pod khác.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn theo dõi một cluster khởi động, bạn sẽ nhận thấy binary kubelet cố gắng giao tiếp với control plane, và nó sẽ làm như vậy nhiều lần cho đến khi control plane có sẵn.</p>
}

// question: 9.16 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Node object trong Kubernetes API cung cấp thông tin gì quan trọng cho việc scheduling Pods?</p>{
	~[moodle]Danh sách các Pod đang chạy trên node.#<p>kubectl get pods hiển thị Pods đang chạy, Node object hiển thị thông tin về node.</p>
	=[moodle]Các trường allocatable về CPU và memory có sẵn trên node.
	~[moodle]Phiên bản của Docker Engine đang chạy.#<p>Container runtime (như containerd) được ghi trong metadata annotations, không phải Docker Engine.</p>
	~[moodle]IP address của tất cả các Pods trên node.#<p>Pod IP addresses là thông tin động được CNI quản lý.</p>
	####<p><strong>Giải thích</strong>\: Các trường allocatable cho node bao gồm thông tin về CPU và memory. Thông tin trong Node object là rất quan trọng cho các hoạt động như scheduling Pods.</p>
}

// question: 9.17 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Các kubelet configurations và API được định nghĩa như thế nào?</p>{
	~[moodle]Chỉ thông qua command-line options.#<p>Các lựa chọn này không đầy đủ.</p>
	~[moodle]Chỉ thông qua các YAML configuration files.#<p>Các lựa chọn này không đầy đủ.</p>
	=[moodle]Thông qua command-line options, default values hoặc YAML configuration files.
	~[moodle]Thông qua Container Runtime Interface (CRI).#<p>CRI là giao diện để kubelet tương tác với container runtime, không phải cách cấu hình kubelet.</p>
	####<p><strong>Giải thích</strong>\: Tất cả các giá trị này được đặt thông qua command-line options, default values, hoặc YAML configuration files.</p>
}

// question: 9.18 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>KubeGenericRuntime interface trong mã nguồn của kubelet được sử dụng để làm gì?</p>{
	~[moodle]Để định nghĩa các hàm gRPC service client cho API server.#<p>gRPC service clients là các hàm cho phép kubelet tương tác với CRI, không phải API server.</p>
	=[moodle]Để bọc (wrap) các chức năng cốt lõi trong CRI runtime và được quản lý bên trong Kubernetes.
	~[moodle]Để cung cấp giao diện cho kubelet kéo image từ registry.#<p>ImageService interface được dùng để pull image.</p>
	~[moodle]Để định nghĩa các options command-line cho kubelet.#<p>kubeletFlags struct định nghĩa các command-line options.</p>
	####<p><strong>Giải thích</strong>\: KubeGenericRuntime interface được quản lý bên trong Kubernetes, bọc các chức năng cốt lõi trong CRI runtime.</p>
}

// question: 9.19 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>ImageService interface của CRI cung cấp các chức năng chính nào?</p>{
	~[moodle]StartContainer, StopContainer, ExecSync.#<p>StartContainer, StopContainer, ExecSync là các chức năng của ContainerRuntime.</p>
	=[moodle]PullImage, ListImages, RemoveImage.
	~[moodle]CreatePodSandbox, StopPodSandbox, RemovePodSandbox.#<p>CreatePodSandbox, StopPodSandbox, RemovePodSandbox là các chức năng của PodSandBoxManager.</p>
	~[moodle]GetContainerMetrics, ListContainerMetrics.#<p>GetContainerMetrics, ListContainerMetrics là các chức năng của ContainerMetricsGetter.</p>
	####<p><strong>Giải thích</strong>\: ImageService interface cung cấp các chức năng PullImage, ListImages, và RemoveImage.</p>
}

// question: 9.20 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Tại sao kubelet không chạy container trực tiếp mà ủy quyền cho CRI?</p>{
	~[moodle]Để kubelet có thể tập trung vào quản lý network policies.#<p>Kubelet có nhiều trách nhiệm, không chỉ network policies.</p>
	=[moodle]Vì container runtimes được thiết kế để chuyên biệt trong việc tạo và quản lý container.
	~[moodle]Để giảm thiểu việc sử dụng CPU của kubelet.#<p>Việc ủy quyền là về separation of concerns (tách biệt các mối quan tâm), không nhất thiết là giảm CPU.</p>
	~[moodle]Kubelet không có quyền truy cập vào container images.#<p>Kubelet tương tác với ImageService của CRI để pull images.</p>
	####<p><strong>Giải thích</strong>\: Kubelet không chạy container: đó là công việc của CRI. Kubelet duy trì vòng đời của Pod về việc sử dụng tài nguyên, nó ủy quyền cho một giao diện được gọi là CRI (Container Runtime Interface) để khởi động và dừng Pod, cũng như kéo image cho container.</p>
}

// question: 9.21 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Khi kubelet khởi động, Node life cycle được cập nhật trong API server như thế nào trong các phiên bản Kubernetes 1.17 trở lên?</p>{
	~[moodle]Node object được cập nhật mỗi 10 giây với toàn bộ trạng thái.#<p>Đây là cách hoạt động trước Kubernetes 1.17.</p>
	=[moodle]Kubelet cập nhật một Lease object nhỏ gọn mỗi 10 giây.
	~[moodle]Node life cycle chỉ được cập nhật khi kubelet bị lỗi.#<p>Node life cycle được cập nhật liên tục để đảm bảo control plane có thông tin chính xác.</p>
	~[moodle]API server tự động suy ra trạng thái node mà không cần kubelet gửi cập nhật.#<p>API server cần kubelet để nhận cập nhật trạng thái node.</p>
	####<p><strong>Giải thích</strong>\: Để tối ưu hóa hiệu suất của các cluster lớn và giảm sự "chatty" của mạng, các phiên bản Kubernetes 1.17 trở lên triển khai một API server endpoint cụ thể để quản lý kubelet thông qua leasing mechanism của etcd. Kubelet cập nhật độc lập một Lease object (rất nhỏ) mỗi 10 giây.</p>
}

// question: 9.22 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Vai trò của containerd trong kiến trúc Kubernetes hiện đại là gì?</p>{
	~[moodle]Containerd là một hypervisor để chạy VMs.#<p>Containerd là container runtime, không phải hypervisor.</p>
	=[moodle]Containerd là một container runtime được kubelet sử dụng để chạy container, thường thông qua runc.
	~[moodle]Containerd là một scheduler cho Pods.#<p>Kube-scheduler là scheduler.</p>
	~[moodle]Containerd là một công cụ command-line để quản lý Kubernetes cluster.#<p>kubectl là công cụ command-line chính.</p>
	####<p><strong>Giải thích</strong>\: Containerd là một container runtime được Docker Engine sử dụng mặc định, và modern Kubernetes clusters thường sử dụng containerd làm runtime cho Linux. Hầu hết các cluster thực thi runc làm container runtime ở cấp độ thấp nhất, trong đó runc được gọi bởi containerd hoặc CRI-O.</p>
}

// question: 9.23 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Làm thế nào để kubelet biết nơi CRI service của nó đang chạy?</p>{
	~[moodle]Kubelet tự động phát hiện CRI service thông qua network broadcast.#<p>Kubelet không tự động phát hiện qua network broadcast.</p>
	=[moodle]CRI service endpoint được cung cấp cho kubelet như một startup argument hoặc được cấu hình.
	~[moodle]CRI service đăng ký với API server, sau đó kubelet truy vấn API server.#<p>CRI service giao tiếp trực tiếp với kubelet, không phải qua API server để xác định endpoint.</p>
	~[moodle]Kubelet đọc thông tin từ Dockerfile của image.#<p>Dockerfile không chứa thông tin về CRI service.</p>
	####<p><strong>Giải thích</strong>\: CRI service endpoint được cung cấp như một startup argument cho kubelet hoặc được cấu hình theo một cách khác.</p>
}

// question: 9.24 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Một trong những cấu hình kubelet quan trọng là evictionHard. Nó quy định điều gì?</p>{
	~[moodle]EvictionHard xác định thời gian kubelet chờ trước khi evict một Pod.#<p>EvictionSoft quy định thời gian chờ.</p>
	=[moodle]EvictionHard chỉ định khi Pod nên bị xóa dựa trên system load (ví dụ: bộ nhớ, dung lượng đĩa).
	~[moodle]EvictionHard là một giới hạn cứng cho CPU usage của Pod.#<p>cgroups quản lý CPU usage.</p>
	~[moodle]EvictionHard xác định số lượng image tối thiểu cần giữ lại trên node.#<p>ImageMinimumGCAge quy định tuổi thọ image.</p>
	####<p><strong>Giải thích</strong>\: EvictionHard (cho hard limits) chỉ định khi Pod nên bị xóa, dựa trên system load (ví dụ: imagefs.available, nodefs.available, nodefs.inodesFree).</p>
}

// question: 9.25 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Tại sao pause container cần được khởi chạy trước container ứng dụng thực tế trong Pod?</p>{
	~[moodle]Để pause container thực hiện health check cho container ứng dụng.#<p>Health check là trách nhiệm của kubelet và container ứng dụng.</p>
	=[moodle]Để Linux OS có thời gian tạo network và PID namespace dùng chung cho Pod.
	~[moodle]Để pause container quản lý volume mounts cho container ứng dụng.#<p>Pause container tạo filesystem dùng chung, không trực tiếp quản lý volume mounts.</p>
	~[moodle]Pause container tải các binary cần thiết cho container ứng dụng.#<p>Binary nằm trong image của container ứng dụng.</p>
	####<p><strong>Giải thích</strong>\: Kubelet khởi chạy một pause container, cung cấp cho Linux OS thời gian để tạo một network cho container. Pause container này là tiền thân của ứng dụng thực tế mà chúng ta sẽ chạy. Nó tồn tại với mục đích tạo một home ban đầu để bootstrap network process và process ID (PID) mới của container.</p>
}

// question: 9.26 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Mối quan hệ giữa CRI và runc là gì?</p>{
	~[moodle]Runc là một hypervisor mà CRI sử dụng.#<p>runc là container runtime, không phải hypervisor.</p>
	=[moodle]Runc là một container runtime cấp thấp mà containerd (thông qua CRI) gọi để chạy container trên Linux.
	~[moodle]CRI là một programming language mà runc được viết bằng.#<p>CRI là giao diện, không phải programming language.</p>
	~[moodle]CRI và runc là các thuật ngữ có thể thay thế cho nhau.#<p>CRI là giao diện, runc là một triển khai runtime.</p>
	####<p><strong>Giải thích</strong>\: runc là một chương trình nhỏ trong bức tranh khi nói đến những gì Kubernetes cần để chạy container ở quy mô lớn. Toàn bộ bí ẩn chủ yếu được định nghĩa bởi giao diện CRI, trừu tượng hóa runc cùng với các chức năng khác để cho phép scheduling cấp cao hơn, image management và chức năng container runtime. Containerd gọi runc cho Linux containers.</p>
}

// question: 9.27 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Các kubeletFlags struct và kubeletConfiguration khác nhau như thế nào?</p>{
	~[moodle]kubeletFlags chứa các options có thể thay đổi an toàn trong vòng đời node, còn kubeletConfiguration là các options không thay đổi.#<p>kubeletFlags thường không thay đổi an toàn, kubeletConfiguration được thiết kế để chia sẻ giữa các node.</p>
	=[moodle]kubeletFlags dành cho các CLI flags và kubeletConfiguration dành cho các giá trị API trong tệp cấu hình.
	~[moodle]kubeletFlags chỉ dành cho Windows kubelets, còn kubeletConfiguration dành cho Linux kubelets.#<p>Cả hai đều không dành riêng cho hệ điều hành nào.</p>
	~[moodle]kubeletFlags được sử dụng bởi scheduler, còn kubeletConfiguration được sử dụng bởi controller manager.#<p>Cả hai đều được kubelet sử dụng.</p>
	####<p><strong>Giải thích</strong>\: kubeletFlags chứa các configuration flags cho kubelet (tức là các CLI flags). Trong khi đó, kubeletConfiguration chứa các giá trị API được xác định trong một tệp cấu hình (ví dụ: config.yaml) và được dùng để chia sẻ cấu hình giữa các node.</p>
}

// question: 9.28 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Trong Pod lifecycle của kubelet, điều gì xảy ra sau khi storage và networking được thiết lập cho Pod?</p>{
	~[moodle]Kubelet giám sát container một cách liên tục.#<p>Monitoring diễn ra sau khi container bắt đầu.</p>
	=[moodle]Kubelet bắt đầu (starts) các container bên trong Pod.
	~[moodle]Kubelet restart container nếu nó unhealthy.#<p>Restart container là một hành động khi có sự cố, không phải bước tiếp theo.</p>
	~[moodle]Kubelet stops Pod nếu ứng dụng hoàn thành.#<p>Stopping Pods là bước cuối cùng trong vòng đời.</p>
	####<p><strong>Giải thích</strong>\: Kubelet quản lý vòng đời của Pod bao gồm: Khởi động Pod, đảm bảo Pod đang chạy, thiết lập storage và networking, sau đó start container(s).</p>
}

// question: 9.29 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>kubelet binary được khởi động như thế nào trên một node trong Kubernetes?</p>{
	~[moodle]Nó được khởi động thủ công bởi system administrator.#<p>systemd tự động khởi động.</p>
	=[moodle]Nó được khởi động bởi systemd và chạy như một node agent.
	~[moodle]Nó được khởi động bởi API server khi có Pod cần được lên lịch.#<p>API server không khởi động kubelet, mà tương tác với kubelet đã chạy.</p>
	~[moodle]Nó được khởi động bởi Container runtime để quản lý container images.#<p>Container runtime được kubelet sử dụng, không phải khởi động kubelet.</p>
	####<p><strong>Giải thích</strong>\: Kubelet là một binary, được khởi động bởi systemd. Kubelet chạy trên mỗi node và là Pod scheduler và node agent.</p>
}

// question: 9.30 name: Chapter 9: Running Pods: How the kubelet works
::Chapter 9\: Running Pods: How the kubelet works::[html]<p>Tại sao kubelet được gọi là Pod scheduler cục bộ?</p>{
	~[moodle]Vì nó tự lên lịch cho các Pod của chính kubelet.#<p>Kubelet không tự lên lịch cho Pods của nó, mà quản lý Pods được giao.</p>
	=[moodle]Vì nó quản lý việc scheduling và lifecycle của Pods chỉ trên node mà nó đang chạy.
	~[moodle]Vì nó có thể override các quyết định scheduling của Kubernetes scheduler.#<p>Kubernetes scheduler đưa ra quyết định tổng thể, kubelet thực thi cục bộ.</p>
	~[moodle]Vì nó chỉ schedule các static Pods mà không tương tác với Kubernetes scheduler.#<p>Kubelet quản lý cả static Pods và các Pods được scheduler chỉ định.</p>
	####<p><strong>Giải thích</strong>\: Kubelet là node agent và Pod scheduler, nhưng chỉ cho node cục bộ. Nó quản lý vòng đời của Pods trên node đó.</p>
}

// Chapter 10: DNS in Kubernetes
// question: 10 name: Switch category to $module$/top/Chapter 10: DNS in Kubernetes
$CATEGORY: $module$/top/Chapter 10: DNS in Kubernetes

// question: 10.1 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Thành phần nào cung cấp dịch vụ DNS chính cho Pods trong Kubernetes?</p>{
	~[moodle]kube-proxy.#<p>kube-proxy quản lý định tuyến dịch vụ cấp thấp, không phải dịch vụ DNS chính.</p>
	=[moodle]CoreDNS.
	~[moodle]etcd.#<p>etcd là kho lưu trữ key/value nhất quán, cốt lõi của control plane.</p>
	~[moodle]kubelet.#<p>kubelet là tác nhân nút, quản lý vòng đời Pod trên nút cục bộ.</p>
	####<p><strong>Giải thích</strong>\: CoreDNS là dịch vụ DNS mặc định cho Kubernetes, cung cấp chức năng DNS cho Pods.</p>
}

// question: 10.2 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Mục đích chính của việc có DNS trong Kubernetes là gì?</p>{
	~[moodle]Đảm bảo mọi Pod đều có IP công khai.#<p>DNS không đảm bảo IP công khai cho Pods; đó là chức năng của LoadBalancer hoặc NodePort.</p>
	=[moodle]Giúp các ứng dụng tìm thấy dịch vụ nội bộ dễ dàng.
	~[moodle]Mã hóa tất cả lưu lượng mạng giữa các Pod.#<p>DNS không mã hóa lưu lượng mạng; đó là nhiệm vụ của TLS hoặc Service Mesh.</p>
	~[moodle]Cung cấp lưu trữ dữ liệu bền vững cho Pods.#<p>DNS không cung cấp lưu trữ dữ liệu bền vững; đó là chức năng của PersistentVolumes.</p>
	####<p><strong>Giải thích</strong>\: DNS trong Kubernetes giúp các microservice truy cập Service nội bộ một cách dễ dàng và cục bộ.</p>
}

// question: 10.3 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Tệp resolv.conf trong container Pod được kubelet cấu hình để làm gì?</p>{
	~[moodle]Cấu hình cgroups của Pod.#<p>cgroups được quản lý thông qua hệ thống tệp cgroup, không phải resolv.conf.</p>
	=[moodle]Thực hiện tra cứu DNS.
	~[moodle]Xác định loại hình ảnh container.#<p>Loại hình ảnh container được xác định trong Pod spec, không phải bởi resolv.conf.</p>
	~[moodle]Quản lý tài nguyên lưu trữ.#<p>Quản lý lưu trữ là nhiệm vụ của CSI và PersistentVolumes.</p>
	####<p><strong>Giải thích</strong>\: Tệp resolv.conf được kubelet tạo và mount vào Pod để thực hiện tra cứu DNS.</p>
}

// question: 10.4 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Để các Pods trong cùng một namespace có thể giao tiếp với nhau bằng tên dịch vụ, cơ chế DNS nào được sử dụng?</p>{
	~[moodle]Fully Qualified Domain Name (FQDN).#<p>FQDN được dùng khi giao tiếp giữa các namespace hoặc với bên ngoài.</p>
	=[moodle]Tên dịch vụ ngắn (short service name).
	~[moodle]Địa chỉ IP của nút.#<p>Địa chỉ IP của nút không được dùng để tra cứu dịch vụ nội bộ Pod.</p>
	~[moodle]Cổng ngẫu nhiên (random port).#<p>Cổng ngẫu nhiên không liên quan đến việc tra cứu dịch vụ bằng tên.</p>
	####<p><strong>Giải thích</strong>\: Pods trong cùng một namespace có thể tra cứu dịch vụ bằng tên dịch vụ ngắn của chúng.</p>
}

// question: 10.5 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>dnsPolicy của một Pod mặc định là gì khi không được cấu hình rõ ràng?</p>{
	~[moodle]None.#<p>None có nghĩa là Pod sẽ không sử dụng DNS của cụm.</p>
	=[moodle]ClusterFirst.
	~[moodle]Default.#<p>Default có nghĩa là Pod sẽ sử dụng cấu hình DNS của nút.</p>
	~[moodle]NodeLocalDNS.#<p>NodeLocalDNS là một chính sách tối ưu hiệu suất, không phải mặc định.</p>
	####<p><strong>Giải thích</strong>\: dnsPolicy mặc định là ClusterFirst, nghĩa là Pod sẽ ưu tiên tìm kiếm trong cụm trước.</p>
}

// question: 10.6 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Nếu một Pod chạy trong namespace joe muốn truy cập database my-db trong cùng namespace, URL mặc định sẽ là gì?</p>{
	~[moodle]my-db.svc.cluster.local.#<p>Đây là FQDN, sử dụng khi tra cứu giữa các namespace.</p>
	~[moodle]my-db.joe.#<p>Đây là tên dịch vụ + namespace, sử dụng khi từ namespace khác.</p>
	=[moodle]my-db.
	~[moodle]my-db.cluster.local.#<p>Đây là tên dịch vụ + tên miền cụm, cũng dùng khi từ namespace khác.</p>
	####<p><strong>Giải thích</strong>\: Nếu Pod và dịch vụ ở cùng một namespace, chỉ cần sử dụng tên dịch vụ ngắn my-db.</p>
}

// question: 10.7 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>CoreDNS sử dụng hệ thống plugin để làm gì?</p>{
	~[moodle]Tự động mã hóa lưu lượng DNS.#<p>Plugin không tự động mã hóa lưu lượng DNS.</p>
	=[moodle]Cấu hình và mở rộng chức năng DNS.
	~[moodle]Phân bổ địa chỉ IP cho Pods.#<p>Phân bổ IP cho Pods là nhiệm vụ của CNI provider.</p>
	~[moodle]Theo dõi hiệu suất ổ đĩa.#<p>Theo dõi hiệu suất ổ đĩa không phải là chức năng của CoreDNS.</p>
	####<p><strong>Giải thích</strong>\: CoreDNS được cung cấp bởi các plugin, cho phép cấu hình linh hoạt và mở rộng chức năng DNS.</p>
}

// question: 10.8 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Plugin cache của CoreDNS có chức năng gì?</p>{
	~[moodle]Giới hạn số lượng truy vấn DNS.#<p>Chức năng chính không phải là giới hạn truy vấn, mà là tối ưu hiệu suất.</p>
	=[moodle]Tăng tốc độ phản hồi bằng cách lưu trữ kết quả.
	~[moodle]Chuyển tiếp các truy vấn đến DNS bên ngoài.#<p>Chuyển tiếp truy vấn là chức năng của plugin forward.</p>
	~[moodle]Giám sát các lỗi DNS.#<p>Giám sát lỗi là chức năng của plugin errors hoặc health.</p>
	####<p><strong>Giải thích</strong>\: Plugin cache cho phép CoreDNS lưu trữ kết quả tra cứu DNS trong một khoảng thời gian nhất định (ví dụ 30 giây) để tăng tốc độ phản hồi.</p>
}

// question: 10.9 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Điều gì xảy ra nếu plugin Kubernetes của CoreDNS không thể giải quyết một địa chỉ?</p>{
	~[moodle]Truy vấn sẽ bị hủy.#<p>Truy vấn không bị hủy ngay lập tức mà sẽ thử cơ chế khác.</p>
	=[moodle]CoreDNS sẽ cố gắng giải quyết qua /etc/resolv.conf.
	~[moodle]CoreDNS sẽ tự động khởi động lại.#<p>CoreDNS không tự động khởi động lại do lỗi giải quyết DNS.</p>
	~[moodle]Kubernetes API server sẽ bị lỗi.#<p>API server không bị lỗi trực tiếp bởi một truy vấn DNS không giải quyết được.</p>
	####<p><strong>Giải thích</strong>\: Nếu plugin Kubernetes không thể giải quyết, CoreDNS sẽ chuyển tiếp truy vấn tới /etc/resolv.conf của nút để giải quyết địa chỉ bên ngoài.</p>
}

// question: 10.10 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Tên miền svc.cluster.local đại diện cho điều gì trong Kubernetes?</p>{
	~[moodle]Một dịch vụ bên ngoài cụm.#<p>Các dịch vụ bên ngoài cụm không sử dụng .svc.cluster.local.</p>
	=[moodle]Một dịch vụ bên trong cụm.
	~[moodle]Một Pod đang chạy.#<p>Pods có thể được định danh bằng hostname riêng, nhưng không phải tên miền này.</p>
	~[moodle]Một Node của cụm.#<p>Nút không được định danh trực tiếp bằng tên miền này.</p>
	####<p><strong>Giải thích</strong>\: svc.cluster.local là một phần của FQDN cho các dịch vụ nội bộ trong cụm Kubernetes.</p>
}

// question: 10.11 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Làm thế nào để giảm thời gian làm mới kết quả DNS được lưu trong bộ nhớ cache của CoreDNS?</p>{
	~[moodle]Tăng giá trị cache lên 300 giây.#<p>Tăng giá trị cache sẽ làm cho kết quả được giữ lâu hơn, giảm làm mới.</p>
	=[moodle]Giảm giá trị cache xuống một số nhỏ hơn.
	~[moodle]Tắt hoàn toàn plugin cache.#<p>Tắt cache có thể tăng tải lên control plane.</p>
	~[moodle]Chỉ sử dụng địa chỉ IP trực tiếp.#<p>Sử dụng IP trực tiếp bỏ qua DNS, không phải cách điều chỉnh cache.</p>
	####<p><strong>Giải thích</strong>\: Để làm mới kết quả nhanh hơn, bạn có thể giảm giá trị cache trong cấu hình CoreDNS (ví dụ từ 30 xuống 5 giây).</p>
}

// question: 10.12 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Tại sao việc sử dụng chính sách NodeLocalDNS trong Kubernetes lại quan trọng đối với các cụm lớn?</p>{
	~[moodle]Để tắt hoàn toàn DNS trong cụm.#<p>Nó không tắt DNS mà tối ưu hóa nó.</p>
	~[moodle]Để lưu trữ tất cả các bản ghi DNS bên ngoài cụm.#<p>Nó tập trung vào việc lưu cache các yêu cầu DNS nội bộ.</p>
	=[moodle]Để tăng tốc độ phản hồi DNS bằng cách lưu cache trên mỗi nút.
	~[moodle]Để gán địa chỉ IP duy nhất cho mỗi Pod.#<p>Gán IP cho Pod là nhiệm vụ của CNI, không phải NodeLocalDNS.</p>
	####<p><strong>Giải thích</strong>\: Chính sách NodeLocalDNS tăng tốc độ DNS bằng cách chạy một DaemonSet trên tất cả các nút để lưu cache các yêu cầu DNS cục bộ.</p>
}

// question: 10.13 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Một StatefulSet có thể có các bản ghi DNS bền vững (persistent DNS records) không?</p>{
	~[moodle]Không, StatefulSet không hỗ trợ DNS.#<p>StatefulSet được thiết kế để quản lý các ứng dụng có trạng thái, bao gồm cả DNS bền vững.</p>
	=[moodle]Có, thông qua việc sử dụng headless service.
	~[moodle]Chỉ khi sử dụng external DNS.#<p>external DNS không phải là cách duy nhất để có bản ghi DNS bền vững.</p>
	~[moodle]Chỉ khi mọi Pod đều có IP tĩnh.#<p>IP tĩnh không phải là điều kiện tiên quyết duy nhất.</p>
	####<p><strong>Giải thích</strong>\: StatefulSet thường được sử dụng với headless service để cung cấp các bản ghi DNS bền vững cho mỗi Pod.</p>
}

// question: 10.14 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Để truy cập một Pod cụ thể trong một StatefulSet bằng DNS, bạn sẽ sử dụng cú pháp nào?</p>{
	~[moodle]<service-name>.<namespace>.svc.cluster.local.#<p>Đây là cú pháp để truy cập dịch vụ chung, không phải Pod cụ thể trong StatefulSet.</p>
	=[moodle]<pod-name>.<service-name>.<namespace>.svc.cluster.local.
	~[moodle]<service-name>.<cluster.local>.#<p>Cú pháp này thiếu thông tin namespace.</p>
	~[moodle]<pod-name>.<namespace>.cluster.local.#<p>Cú pháp này thiếu tên dịch vụ service-name.</p>
	####<p><strong>Giải thích</strong>\: Để truy cập một Pod cụ thể trong StatefulSet, bạn sử dụng cú pháp <pod-name>.<service-name>.<namespace>.svc.cluster.local.</p>
}

// question: 10.15 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Tại sao việc sử dụng phiên bản NGINX cũ (ví dụ 1.7) trong các ví dụ về DNS lại được nhắc đến?</p>{
	~[moodle]Vì nó an toàn hơn.#<p>Các container hiện đại thường bỏ shell vì lý do bảo mật, làm phiên bản cũ kém an toàn hơn.</p>
	=[moodle]Vì nó cho phép truy cập shell để kiểm tra.
	~[moodle]Vì nó có hiệu suất tốt hơn.#<p>Hiệu suất không phải lý do chính ở đây.</p>
	~[moodle]Vì nó không cần cấu hình DNS.#<p>Mọi container đều cần cấu hình DNS để hoạt động.</p>
	####<p><strong>Giải thích</strong>\: Phiên bản NGINX cũ được sử dụng trong ví dụ để cho phép truy cập shell, giúp dễ dàng kiểm tra cấu hình DNS từ bên trong Pod.</p>
}

// question: 10.16 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>distroless image được khuyến nghị cho các container vì lý do gì?</p>{
	~[moodle]Tăng kích thước hình ảnh.#<p>distroless image làm giảm kích thước hình ảnh.</p>
	=[moodle]Giảm dấu chân lỗ hổng bảo mật (vulnerability footprint).
	~[moodle]Cung cấp một shell đầy đủ tính năng.#<p>distroless image thường không có shell.</p>
	~[moodle]Cho phép nhiều ứng dụng chạy trong một container.#<p>Container thường được thiết kế để chạy một ứng dụng duy nhất.</p>
	####<p><strong>Giải thích</strong>\: distroless image là hình ảnh Linux tối giản, chỉ chứa những gì cần thiết cho ứng dụng, giúp giảm dấu chân lỗ hổng bảo mật.</p>
}

// question: 10.17 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>CoreDNS sử dụng cổng tiêu chuẩn nào cho dịch vụ DNS của nó?</p>{
	~[moodle]Cổng 80.#<p>Cổng 80 là cổng HTTP tiêu chuẩn.</p>
	~[moodle]Cổng 443.#<p>Cổng 443 là cổng HTTPS tiêu chuẩn.</p>
	=[moodle]Cổng 53.
	~[moodle]Cổng 8080.#<p>Cổng 8080 thường dùng cho các ứng dụng web.</p>
	####<p><strong>Giải thích</strong>\: CoreDNS gửi lưu lượng đến cổng 53, là tiêu chuẩn phổ biến cho dịch vụ DNS.</p>
}

// question: 10.18 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Lệnh kubectl exec -it <pod-name> -- /bin/bash được dùng để làm gì trong ngữ cảnh kiểm tra DNS?</p>{
	~[moodle]Xóa Pod.#<p>Để xóa Pod, dùng kubectl delete pod.</p>
	~[moodle]Chỉnh sửa cấu hình DNS của Pod.#<p>Cấu hình DNS của Pod được quản lý bởi kubelet và CoreDNS, không trực tiếp chỉnh sửa qua shell.</p>
	=[moodle]Truy cập shell của Pod để chạy lệnh.
	~[moodle]Khởi động lại dịch vụ DNS.#<p>Lệnh này không khởi động lại dịch vụ DNS.</p>
	####<p><strong>Giải thích</strong>\: Lệnh này cho phép bạn truy cập một shell tương tác bên trong container của Pod để chạy các lệnh như cat /etc/resolv.conf.</p>
}

// question: 10.19 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>search default.svc.cluster.local svc.cluster.local cluster.local trong resolv.conf của Pod có ý nghĩa gì?</p>{
	~[moodle]Danh sách các máy chủ DNS bên ngoài.#<p>Đây không phải danh sách máy chủ DNS mà là các hậu tố tên miền.</p>
	=[moodle]Các miền tìm kiếm DNS sẽ được thử.
	~[moodle]Địa chỉ IP của các dịch vụ trong cụm.#<p>IP dịch vụ là clusterIP, không phải thông tin tìm kiếm.</p>
	~[moodle]Cài đặt bảo mật cho DNS.#<p>Cài đặt bảo mật không nằm trong dòng search.</p>
	####<p><strong>Giải thích</strong>\: Dòng search định nghĩa các miền tìm kiếm DNS mà trình phân giải sẽ thử khi nhận được một truy vấn không đủ điều kiện.</p>
}

// question: 10.20 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Giá trị ndots:5 trong resolv.conf của Pod ảnh hưởng đến độ phân giải DNS như thế nào?</p>{
	~[moodle]Bắt buộc Pod sử dụng 5 máy chủ DNS.#<p>Nó không liên quan đến số lượng máy chủ DNS.</p>
	=[moodle]Bắt buộc một tên miền có ít nhất 5 dấu chấm mới được coi là FQDN.
	~[moodle]Đặt giới hạn tối đa 5 truy vấn DNS.#<p>Nó không phải giới hạn số lượng truy vấn.</p>
	~[moodle]Chỉ cho phép các Pod có 5 container.#<p>Nó không liên quan đến số lượng container trong Pod.</p>
	####<p><strong>Giải thích</strong>\: ndots:5 có nghĩa là một tên miền có ít nhất 5 dấu chấm (dots) sẽ được coi là FQDN và không thêm các hậu tố tìm kiếm.</p>
}

// question: 10.21 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>kube-dns Pod được dùng làm ví dụ điển hình để nghiên cứu DNS trong Kubernetes vì lý do gì?</p>{
	~[moodle]Nó có đặc quyền đặc biệt trong cụm.#<p>Nó không có đặc quyền đặc biệt.</p>
	~[moodle]Nó chạy trên host network.#<p>Nó sử dụng mạng Pod thông thường, không phải host network.</p>
	=[moodle]Nó chạy trong mọi cụm Kubernetes và sử dụng mạng Pod thông thường.
	~[moodle]Nó không gửi lưu lượng đến cổng 53.#<p>Nó gửi lưu lượng đến cổng 53.</p>
	####<p><strong>Giải thích</strong>\: kube-dns Pod là một ví dụ tốt vì nó chạy trong mọi cụm, không có đặc quyền đặc biệt và sử dụng mạng Pod tiêu chuẩn.</p>
}

// question: 10.22 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Khi một service được tạo, ClusterIP của nó được cấp phát từ đâu?</p>{
	~[moodle]Từ CNI provider.#<p>CNI provider chủ yếu cấp phát IP cho Pods.</p>
	=[moodle]Từ dải CIDR được chỉ định khi khởi động control plane.
	~[moodle]Từ địa chỉ IP của nút.#<p>Địa chỉ IP của nút là khác biệt và không được dùng trực tiếp cho ClusterIP.</p>
	~[moodle]Từ một IP công khai trên internet.#<p>IP công khai là chức năng của LoadBalancer.</p>
	####<p><strong>Giải thích</strong>\: Khi tạo một ClusterIP Service mới, control plane của Kubernetes cấp phát một IP từ dải CIDR được cung cấp khi khởi động (ví dụ: --service-cluster-ip-range).</p>
}

// question: 10.23 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Sự khác biệt chính giữa Service loại ClusterIP và NodePort là gì?</p>{
	~[moodle]ClusterIP có thể truy cập từ bên ngoài cụm, NodePort chỉ nội bộ.#<p>Ngược lại, ClusterIP chỉ nội bộ, NodePort có thể truy cập từ bên ngoài qua IP nút.</p>
	=[moodle]NodePort mở một cổng trên mỗi nút, ClusterIP chỉ nội bộ cụm.
	~[moodle]NodePort không cần IP, ClusterIP thì cần.#<p>Cả hai đều có IP.</p>
	~[moodle]ClusterIP dùng cho TCP, NodePort dùng cho UDP.#<p>Cả hai đều hỗ trợ TCP và UDP.</p>
	####<p><strong>Giải thích</strong>\: NodePort mở một cổng trên mỗi nút của toàn bộ cụm, cho phép truy cập từ bên ngoài, trong khi ClusterIP chỉ có thể truy cập từ bên trong cụm.</p>
}

// question: 10.24 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Service loại LoadBalancer được triển khai như thế nào trong môi trường đám mây?</p>{
	~[moodle]Bằng cách gán một IP nội bộ cụm.#<p>IP nội bộ là của ClusterIP.</p>
	=[moodle]Nhà cung cấp đám mây cấp phát một IP bên ngoài.
	~[moodle]Nó chỉ hoạt động trên các nút vật lý.#<p>LoadBalancer chủ yếu dùng trong môi trường đám mây ảo hóa.</p>
	~[moodle]Nó sử dụng cùng IP với ClusterIP.#<p>IP của LoadBalancer là IP bên ngoài, khác với ClusterIP.</p>
	####<p><strong>Giải thích</strong>\: Nếu là loại LoadBalancer, nhà cung cấp đám mây sẽ cấp phát một IP bên ngoài, có thể truy cập từ internet hoặc mạng bên ngoài cụm.</p>
}

// question: 10.25 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Khi cấu hình CoreDNS để chuyển tiếp DNS bên ngoài, tệp nào được tham chiếu trong Corefile?</p>{
	~[moodle]/etc/hosts.#<p>/etc/hosts chứa ánh xạ tĩnh hostname-IP, không dùng để chuyển tiếp DNS.</p>
	~[moodle]/etc/kubernetes/admin.conf.#<p>/etc/kubernetes/admin.conf là tệp cấu hình kubectl.</p>
	=[moodle]/etc/resolv.conf.
	~[moodle]/var/log/containers.#<p>/var/log/containers chứa log của container.</p>
	####<p><strong>Giải thích</strong>\: CoreDNS sử dụng plugin forward . /etc/resolv.conf để chuyển tiếp các truy vấn DNS không thể giải quyết nội bộ ra bên ngoài, thông qua resolv.conf của nút.</p>
}

// question: 10.26 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Để một Pod tra cứu và giao tiếp với một Pod khác đang chạy CockroachDB, yếu tố nào cần được triển khai?</p>{
	~[moodle]Chỉ cần địa chỉ IP tĩnh.#<p>IP tĩnh không đủ cho cơ chế tra cứu dịch vụ động của Kubernetes.</p>
	=[moodle]Định danh mạng và tra cứu dịch vụ.
	~[moodle]Cấu hình proxy thủ công.#<p>Kubernetes tự động hóa việc này thông qua dịch vụ DNS và kube-proxy.</p>
	~[moodle]Một cổng duy nhất trên mỗi nút.#<p>Cổng trên mỗi nút là tính năng của NodePort, không phải giải pháp tổng thể.</p>
	####<p><strong>Giải thích</strong>\: Để các microservice có thể giao tiếp với CockroachDB, cần triển khai định danh mạng và tra cứu dịch vụ (definitive networking and service lookup).</p>
}

// question: 10.27 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Làm cách nào để một Pod trong một namespace có thể truy cập một dịch vụ trong một namespace khác?</p>{
	~[moodle]Chỉ cần sử dụng tên dịch vụ ngắn.#<p>Tên dịch vụ ngắn chỉ dùng trong cùng namespace.</p>
	=[moodle]Sử dụng FQDN bao gồm tên dịch vụ và namespace.
	~[moodle]Bằng cách gán cùng một IP cho cả hai namespace.#<p>Gán cùng IP sẽ gây xung đột.</p>
	~[moodle]Không thể truy cập giữa các namespace khác nhau.#<p>Kubernetes được thiết kế để hỗ trợ giao tiếp giữa các namespace.</p>
	####<p><strong>Giải thích</strong>\: Một Pod có thể truy cập dịch vụ trong một namespace khác bằng cách sử dụng FQDN, ví dụ: <service-name>.<namespace>.svc.cluster.local.</p>
}

// question: 10.28 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>CoreDNS có thể được cấu hình để hoạt động với các plugin khác nhau thông qua tệp nào?</p>{
	~[moodle]config.toml.#<p>config.toml là cấu hình của containerd.</p>
	=[moodle]Corefile.
	~[moodle]daemon.json.#<p>daemon.json là cấu hình của Docker daemon.</p>
	~[moodle]kubeconfig.#<p>kubeconfig là tệp cấu hình cho kubectl.</p>
	####<p><strong>Giải thích</strong>\: Cấu hình CoreDNS được đọc từ tệp Corefile, nơi mỗi plugin được định nghĩa trên một dòng mới.</p>
}

// question: 10.29 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Plugin errors trong CoreDNS dùng để làm gì?</p>{
	~[moodle]Chuyển tiếp lỗi đến API server.#<p>Nó ghi lại lỗi, không phải chuyển tiếp lỗi trực tiếp tới API server.</p>
	=[moodle]Ghi lại các lỗi khi xử lý truy vấn DNS.
	~[moodle]Ngăn chặn các truy vấn DNS độc hại.#<p>Ngăn chặn truy vấn độc hại là chức năng bảo mật rộng hơn.</p>
	~[moodle]Tự động sửa lỗi cấu hình DNS.#<p>Nó không tự động sửa lỗi mà chỉ ghi nhận.</p>
	####<p><strong>Giải thích</strong>\: Plugin errors trong CoreDNS dùng để ghi lại các lỗi xảy ra khi xử lý truy vấn DNS.</p>
}

// question: 10.30 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Để đảm bảo một StatefulSet có các bản ghi DNS riêng lẻ cho mỗi Pod, cần phải cấu hình gì cho Service?</p>{
	=[moodle]clusterIP: None.
	~[moodle]type: LoadBalancer.#<p>LoadBalancer sẽ cấp IP bên ngoài chung, không phải riêng lẻ cho từng Pod.</p>
	~[moodle]externalIPs.#<p>externalIPs cũng cấp IP bên ngoài, không phải riêng lẻ cho từng Pod.</p>
	~[moodle]ports: [].#<p>Không có cổng sẽ ngăn giao tiếp.</p>
	####<p><strong>Giải thích</strong>\: Để có các bản ghi DNS riêng lẻ cho mỗi Pod trong StatefulSet, Service cần được cấu hình với clusterIP: None, biến nó thành một headless service.</p>
}

// question: 10.31 name: Chapter 10: DNS in Kubernetes
::Chapter 10\: DNS in Kubernetes::[html]<p>Tại sao việc tuning DNS là một chủ đề sâu rộng ở bất kỳ trung tâm dữ liệu nào, không chỉ Kubernetes?</p>{
	~[moodle]Vì DNS chỉ dùng cho các ứng dụng đám mây.#<p>DNS được dùng rộng rãi, không chỉ cho ứng dụng đám mây.</p>
	~[moodle]Vì các bản ghi DNS không bao giờ thay đổi.#<p>Bản ghi DNS có thể thay đổi, đặc biệt trong môi trường động như Kubernetes.</p>
	=[moodle]Vì quản lý DNS ảnh hưởng đến hiệu suất và khả năng mở rộng.
	~[moodle]Vì DNS chỉ có một loại cấu hình duy nhất.#<p>Có nhiều loại cấu hình DNS khác nhau.</p>
	####<p><strong>Giải thích</strong>\: Tuning DNS là chủ đề phức tạp ở bất kỳ trung tâm dữ liệu nào vì nó ảnh hưởng trực tiếp đến hiệu suất, độ trễ và khả năng mở rộng của ứng dụng.</p>
}

// Chapter 11: The core of the control plane
// question: 11 name: Switch category to $module$/top/Chapter 11: The core of the control plane
$CATEGORY: $module$/top/Chapter 11: The core of the control plane

// question: 11.1 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Control plane của Kubernetes là gì?</p>{
	~[moodle]Một tập hợp các nút chạy Pods ứng dụng.#<p>Các nút chạy Pods ứng dụng được gọi là worker nodes.</p>
	=[moodle]Bộ não của cụm, quản lý lập lịch và đối tượng Kubernetes.
	~[moodle]Một giao diện người dùng đồ họa để quản lý cụm.#<p>Giao diện người dùng là một công cụ, không phải control plane.</p>
	~[moodle]Cơ chế lưu trữ dữ liệu chính của cụm.#<p>Cơ chế lưu trữ dữ liệu chính là etcd, một phần của control plane.</p>
	####<p><strong>Giải thích</strong>\: Control plane là bộ não của một cụm Kubernetes, nơi diễn ra việc lập lịch các container và quản lý tất cả các đối tượng Kubernetes.</p>
}

// question: 11.2 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Namespace kube-system thường chứa những thành phần nào?</p>{
	~[moodle]Chỉ các ứng dụng của người dùng.#<p>Không khuyến khích cài ứng dụng người dùng vào đây để giảm rủi ro bảo mật.</p>
	=[moodle]Các thành phần cốt lõi của control plane.
	~[moodle]Chỉ các Pods có trạng thái.#<p>StatefulSet thường chạy trong các namespace dành riêng cho ứng dụng.</p>
	~[moodle]Chỉ các volume lưu trữ dữ liệu.#<p>Volume lưu trữ thuộc về Pods, có thể ở bất kỳ namespace nào.</p>
	####<p><strong>Giải thích</strong>\: Các thành phần cốt lõi của control plane thường được cài đặt trong namespace kube-system.</p>
}

// question: 11.3 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Điều gì xảy ra khi bạn không chỉ định ServiceAccount cho một Pod?</p>{
	~[moodle]Pod sẽ không thể chạy.#<p>Pod vẫn có thể chạy, nhưng với ServiceAccount mặc định.</p>
	=[moodle]Pod sẽ sử dụng ServiceAccount mặc định của namespace.
	~[moodle]Pod sẽ chạy với quyền root.#<p>ServiceAccount không trực tiếp liên quan đến việc chạy với quyền root, mà là xác thực API.</p>
	~[moodle]Pod sẽ bị tự động xóa.#<p>Pod không bị xóa do thiếu ServiceAccount được chỉ định.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn không chỉ định một ServiceAccount cụ thể, Pod sẽ tham gia vào ServiceAccount mặc định được tạo trong Namespace.</p>
}

// question: 11.4 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Chức năng chính của kube-apiserver là gì?</p>{
	~[moodle]Lập lịch Pod trên các nút.#<p>Lập lịch Pod là nhiệm vụ của kube-scheduler.</p>
	=[moodle]Cung cấp giao diện RESTful cho các đối tượng API.
	~[moodle]Quản lý lưu trữ bền vững.#<p>Quản lý lưu trữ là nhiệm vụ của controller manager và CSI.</p>
	~[moodle]Giám sát tình trạng của các container.#<p>Giám sát container là nhiệm vụ của kubelet và CRI.</p>
	####<p><strong>Giải thích</strong>\: kube-apiserver là một máy chủ REST dựa trên HTTP, phơi bày các đối tượng API cho cụm Kubernetes, hỗ trợ các hoạt động CRUD.</p>
}

// question: 11.5 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Custom Resource Definitions (CRDs) được tạo ra để giải quyết vấn đề gì?</p>{
	~[moodle]Giới hạn số lượng đối tượng API trong Kubernetes.#<p>CRDs mở rộng khả năng của API, không giới hạn số lượng đối tượng.</p>
	=[moodle]Cho phép nhà phát triển tạo các đối tượng API riêng của họ.
	~[moodle]Tăng tốc độ khởi động của control plane.#<p>CRDs không trực tiếp tăng tốc độ khởi động control plane.</p>
	~[moodle]Cung cấp giao diện người dùng cho các ứng dụng.#<p>CRDs là định nghĩa dữ liệu, không phải giao diện người dùng.</p>
	####<p><strong>Giải thích</strong>\: CRDs cho phép nhà phát triển tạo định nghĩa đối tượng API riêng của họ và áp dụng chúng vào API server, tách biệt các đối tượng phi-core khỏi API server.</p>
}

// question: 11.6 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Trạng thái nào của đối tượng API được định nghĩa bởi trường spec?</p>{
	~[moodle]Trạng thái hiện tại.#<p>Trạng thái hiện tại được báo cáo trong trường status.</p>
	=[moodle]Trạng thái mong muốn.
	~[moodle]Thông tin metadata.#<p>Thông tin metadata nằm trong trường metadata.</p>
	~[moodle]Phiên bản API.#<p>Phiên bản API nằm trong trường apiVersion.</p>
	####<p><strong>Giải thích</strong>\: Trường spec định nghĩa các thông số kỹ thuật, tức là trạng thái mong muốn của một đối tượng.</p>
}

// question: 11.7 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Điều gì xảy ra khi một Pod không thể chạy trên một nút do thiếu volume yêu cầu?</p>{
	~[moodle]Pod bị xóa vĩnh viễn.#<p>Pod không bị xóa mà được tái lập lịch.</p>
	=[moodle]Lập lịch cho Pod đó được đưa vào hàng đợi lại.
	~[moodle]kubelet sẽ tự động tạo volume.#<p>kubelet không tự động tạo volume mà dựa vào CSI provisioner.</p>
	~[moodle]API server sẽ ngừng hoạt động.#<p>Lỗi lập lịch của Pod không làm ngừng hoạt động API server.</p>
	####<p><strong>Giải thích</strong>\: Nếu việc tạo volume yêu cầu thất bại, Pod không thể chạy trên nút đó và việc lập lịch cho Pod đó được đưa vào hàng đợi lại.</p>
}

// question: 11.8 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Plugin Filter trong scheduler framework có chức năng gì?</p>{
	~[moodle]Sắp xếp các Pod trong hàng đợi.#<p>Sắp xếp Pod là chức năng của QueueSort.</p>
	=[moodle]Lọc ra các nút không thể chạy Pod.
	~[moodle]Tính điểm cho các nút đủ điều kiện.#<p>Tính điểm là chức năng của Score.</p>
	~[moodle]Gắn Pod vào nút đã chọn.#<p>Gắn Pod vào nút là chức năng của Bind.</p>
	####<p><strong>Giải thích</strong>\: Plugin Filter chịu trách nhiệm lọc ra các nút không thể chạy Pod, dựa trên các ràng buộc như tài nguyên.</p>
}

// question: 11.9 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>kube-controller-manager (KCM) bao gồm những loại controller nào theo lịch sử?</p>{
	~[moodle]Chỉ các controller liên quan đến networking.#<p>KCM quản lý nhiều loại controller, không chỉ networking.</p>
	=[moodle]Một tập hợp các control loop chạy nhiều controller.
	~[moodle]Chỉ các controller liên quan đến bảo mật.#<p>Bảo mật cũng được quản lý bởi các controller khác, không chỉ KCM.</p>
	~[moodle]Một binary duy nhất để quản lý tất cả Pods.#<p>KCM quản lý các đối tượng Kubernetes, không phải tất cả Pods.</p>
	####<p><strong>Giải thích</strong>\: KCM là một binary duy nhất nhưng vận hành nhiều control loop và các controller khác nhau.</p>
}

// question: 11.10 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Cloud Controller Managers (CCMs) được thiết kế để làm gì?</p>{
	~[moodle]Chạy các container trên các máy ảo.#<p>CCM tương tác với API đám mây, không phải chạy container trên VM.</p>
	=[moodle]Cho phép phát triển các nhà cung cấp đám mây nhanh hơn.
	~[moodle]Quản lý các Pods ở quy mô nhỏ.#<p>CCM hoạt động ở quy mô cụm, không phải quy mô nhỏ.</p>
	~[moodle]Thay thế hoàn toàn kube-controller-manager.#<p>CCM hoạt động cùng với KCM, không thay thế hoàn toàn.</p>
	####<p><strong>Giải thích</strong>\: CCMs được thiết kế để cho phép phát triển và bảo trì nhà cung cấp đám mây nhanh hơn, tách biệt khỏi kho lưu trữ Kubernetes chính.</p>
}

// question: 11.11 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Node controller trong CCM có chức năng gì?</p>{
	~[moodle]Lập lịch Pod trên các nút đám mây.#<p>Lập lịch Pod là nhiệm vụ của kube-scheduler.</p>
	=[moodle]Cung cấp thông tin cụ thể về nút trong môi trường đám mây cho API server.
	~[moodle]Tạo mới các nút vật lý.#<p>Tạo nút vật lý là nhiệm vụ của nhà cung cấp đám mây.</p>
	~[moodle]Quản lý mạng nội bộ giữa các Pod.#<p>Quản lý mạng nội bộ là nhiệm vụ của CNI và kube-proxy.</p>
	####<p><strong>Giải thích</strong>\: Node controller cung cấp thông tin cụ thể về nút trong môi trường đám mây (ví dụ: thông tin vùng) cho API server và xử lý việc xóa nút.</p>
}

// question: 11.12 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>API objects trong Kubernetes có những thành phần cốt lõi nào?</p>{
	~[moodle]Chỉ tên và nội dung.#<p>Thiếu các thông tin cấu trúc quan trọng khác.</p>
	=[moodle]apiVersion, kind, và metadata.
	~[moodle]Chỉ địa chỉ IP và cổng.#<p>Địa chỉ IP và cổng là thuộc tính của Pods/Services, không phải của mọi đối tượng API.</p>
	~[moodle]spec, status, và log.#<p>log không phải là một thành phần cốt lõi của đối tượng API.</p>
	####<p><strong>Giải thích</strong>\: Tất cả các đối tượng API Kubernetes đều có apiVersion, kind và một phần metadata.</p>
}

// question: 11.13 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>ClusterRoleBinding là một đối tượng API beta có ý nghĩa gì?</p>{
	~[moodle]Chỉ dành cho môi trường thử nghiệm.#<p>API alpha mới là dành cho thử nghiệm.</p>
	=[moodle]Sẵn sàng cho sản xuất và được hỗ trợ.
	~[moodle]Có thể thay đổi không tương thích trong các phiên bản sau.#<p>Các thay đổi không tương thích thường xảy ra với API alpha.</p>
	~[moodle]Chỉ hoạt động trên một số nền tảng nhất định.#<p>API beta có phạm vi hỗ trợ rộng rãi hơn.</p>
	####<p><strong>Giải thích</strong>\: Đối tượng API beta trong Kubernetes được coi là sẵn sàng cho sản xuất và được hỗ trợ.</p>
}

// question: 11.14 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>API rbac.authorization.k8s.io/v1 dùng để định nghĩa loại đối tượng nào?</p>{
	~[moodle]Pods.#<p>Pods dùng apiVersion: v1.</p>
	~[moodle]Deployments.#<p>Deployments dùng apiVersion: apps/v1.</p>
	=[moodle]Role-based Access Control (RBAC).
	~[moodle]Services.#<p>Services dùng apiVersion: v1.</p>
	####<p><strong>Giải thích</strong>\: API rbac.authorization.k8s.io/v1 được dùng để định nghĩa các đối tượng liên quan đến Role-based Access Control (RBAC).</p>
}

// question: 11.15 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Trong scheduler framework, QueueSort plugin được sử dụng để làm gì?</p>{
	~[moodle]Lọc các nút không phù hợp.#<p>Lọc nút là chức năng của Filter.</p>
	=[moodle]Sắp xếp các Pod trong hàng đợi lập lịch.
	~[moodle]Tính điểm cho các nút.#<p>Tính điểm là chức năng của Score.</p>
	~[moodle]Dự trữ tài nguyên cho Pod.#<p>Dự trữ tài nguyên là chức năng của Reserve.</p>
	####<p><strong>Giải thích</strong>\: QueueSort là một danh sách các plugin được gọi khi sắp xếp các Pod trong hàng đợi lập lịch.</p>
}

// question: 11.16 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Plugin volumebinding trong giai đoạn Filter và Reserve của scheduler có vai trò gì?</p>{
	=[moodle]Kiểm tra khả năng gắn volume của nút.
	~[moodle]Tạo mới một volume vật lý.#<p>Tạo volume vật lý là nhiệm vụ của CSI provisioner.</p>
	~[moodle]Chỉ định StorageClass mặc định.#<p>Chỉ định StorageClass mặc định do admission controller thực hiện.</p>
	~[moodle]Xóa các volume không sử dụng.#<p>Xóa volume do KCM hoặc CSI controller thực hiện.</p>
	####<p><strong>Giải thích</strong>\: Plugin volumebinding trong giai đoạn Filter kiểm tra xem một nút có khả năng gắn volume không và trong Reserve thì dự trữ volume cho Pod.</p>
}

// question: 11.17 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Pod anti-affinity có chức năng gì trong quá trình lập lịch?</p>{
	~[moodle]Đảm bảo Pods được lập lịch trên cùng một nút.#<p>Pod affinity sẽ làm điều ngược lại.</p>
	=[moodle]Ngăn Pods từ StatefulSet cư trú trên cùng một nút.
	~[moodle]Phân tán Pods đều khắp các zone.#<p>Phân tán Pods đều khắp các zone là chức năng của PodTopologySpread.</p>
	~[moodle]Ưu tiên các nút có ít tài nguyên hơn.#<p>noderesources.BalancedAllocationName ưu tiên nút có ít yêu cầu hơn.</p>
	####<p><strong>Giải thích</strong>\: Pod anti-affinity đảm bảo rằng các Pods của StatefulSet cư trú trên các nút khác nhau để tăng khả năng chịu lỗi.</p>
}

// question: 11.18 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Controller Manager được tạo ra để đảm bảo điều gì đối với Endpoints?</p>{
	~[moodle]Endpoints được mã hóa.#<p>Endpoints không được mã hóa tự động.</p>
	~[moodle]Endpoints chỉ có IP nội bộ.#<p>Endpoints có thể có cả IP nội bộ và bên ngoài (qua LoadBalancer).</p>
	=[moodle]Endpoints luôn có thông tin về IP của Pods backing một service.
	~[moodle]Endpoints được lưu trữ trong etcd.#<p>Endpoints là đối tượng API được lưu trữ trong etcd, nhưng đó không phải là mục đích của controller này.</p>
	####<p><strong>Giải thích</strong>\: Endpoint controller trong controller manager đảm bảo rằng các đối tượng Endpoints luôn có các địa chỉ IP của các Pods hỗ trợ một service.</p>
}

// question: 11.19 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Service accounts and tokens trong Kubernetes dùng để làm gì?</p>{
	~[moodle]Cung cấp IP tĩnh cho Pods.#<p>IP tĩnh không phải là mục đích của ServiceAccount.</p>
	=[moodle]Quản lý xác thực và cấp quyền cho Pods khi truy cập API server.
	~[moodle]Lưu trữ dữ liệu nhạy cảm của ứng dụng.#<p>Dữ liệu nhạy cảm được lưu trữ trong Secrets.</p>
	~[moodle]Tối ưu hóa hiệu suất mạng.#<p>ServiceAccount không liên quan trực tiếp đến hiệu suất mạng.</p>
	####<p><strong>Giải thích</strong>\: Service accounts and tokens được sử dụng để quản lý quyền truy cập của Pods vào Kubernetes API server, bằng cách mount token API vào Pod.</p>
}

// question: 11.20 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Chức năng LoadBalancer của CCM là gì?</p>{
	=[moodle]Tạo, cập nhật và xóa LoadBalancer của nhà cung cấp đám mây.
	~[moodle]Cân bằng tải nội bộ giữa các Pod.#<p>Cân bằng tải nội bộ do kube-proxy đảm nhiệm.</p>
	~[moodle]Chỉ định cổng cho các dịch vụ.#<p>Chỉ định cổng là một phần của định nghĩa Service.</p>
	~[moodle]Giám sát lưu lượng mạng.#<p>Giám sát lưu lượng mạng là nhiệm vụ của các công cụ khác như Prometheus.</p>
	####<p><strong>Giải thích</strong>\: Service controller của CCM (là một phần của chức năng LoadBalancer) tạo, cập nhật và xóa các LoadBalancer của nhà cung cấp đám mây.</p>
}

// question: 11.21 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>PreFilter plugin trong scheduler framework được dùng để làm gì?</p>{
	~[moodle]Sắp xếp các Pod ưu tiên cao nhất.#<p>Sắp xếp Pod là nhiệm vụ của QueueSort.</p>
	=[moodle]Chạy trước giai đoạn lọc, chuẩn bị dữ liệu hoặc kiểm tra nhanh.
	~[moodle]Ghi nhật ký tất cả các sự kiện lập lịch.#<p>Ghi nhật ký là chức năng logging.</p>
	~[moodle]Đảm bảo tài nguyên mạng cho Pod.#<p>Tài nguyên mạng do CNI đảm nhiệm.</p>
	####<p><strong>Giải thích</strong>\: PreFilter là một danh sách các plugin được gọi ở điểm mở rộng PreFilter của scheduling framework, thường dùng để chuẩn bị dữ liệu hoặc thực hiện kiểm tra nhanh.</p>
}

// question: 11.22 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Tại sao việc không sử dụng kube-system namespace cho các ứng dụng không phải control plane lại được khuyến nghị?</p>{
	~[moodle]Để tránh trùng tên.#<p>Mặc dù có thể trùng tên, lý do chính là bảo mật.</p>
	=[moodle]Để tăng cường bảo mật và giảm "blast radius" khi có tấn công.
	~[moodle]Để tiết kiệm tài nguyên.#<p>Việc này không trực tiếp tiết kiệm tài nguyên.</p>
	~[moodle]Vì namespace này không hỗ trợ Deployments.#<p>Namespace này hỗ trợ mọi đối tượng Kubernetes.</p>
	####<p><strong>Giải thích</strong>\: Không nên sử dụng kube-system cho các ứng dụng không phải control plane để giảm "blast radius" (phạm vi ảnh hưởng của một cuộc tấn công bảo mật).</p>
}

// question: 11.23 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Các API objects trong Kubernetes có thể có bao nhiêu API group?</p>{
	~[moodle]Chỉ một API group duy nhất.#<p>Mỗi đối tượng API thuộc về một API group cụ thể, nhưng có nhiều API group trong Kubernetes.</p>
	=[moodle]Nhiều API group.
	~[moodle]Không có API group nào.#<p>Mọi đối tượng API đều thuộc một API group hoặc là core group.</p>
	~[moodle]Tối đa 3 API group.#<p>Không có giới hạn cứng là 3 API group.</p>
	####<p><strong>Giải thích</strong>\: Các đối tượng API có thể thuộc về nhiều API group, như rbac.authorization.k8s.io hoặc apps.</p>
}

// question: 11.24 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Khi kube-scheduler không thể tìm được nút phù hợp cho một Pod, nó sẽ làm gì?</p>{
	~[moodle]Xóa Pod ngay lập tức.#<p>Pod không bị xóa mà được tái lập lịch.</p>
	=[moodle]Giữ Pod trong hàng đợi lập lịch để thử lại sau.
	~[moodle]Báo cáo lỗi cho kubelet.#<p>kubelet chỉ nhận lệnh từ scheduler sau khi Pod được lập lịch.</p>
	~[moodle]Gán Pod vào một nút ngẫu nhiên.#<p>kube-scheduler có logic phức tạp để chọn nút, không gán ngẫu nhiên.</p>
	####<p><strong>Giải thích</strong>\: Nếu scheduler không tìm được nút phù hợp, nó sẽ đưa Pod vào backoff queue để thử lại sau.</p>
}

// question: 11.25 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Controller Manager chịu trách nhiệm gì đối với Service accounts?</p>{
	~[moodle]Cấp IP cho Service accounts.#<p>Service accounts không được cấp IP.</p>
	=[moodle]Tạo ServiceAccount mặc định và token truy cập API cho namespace mới.
	~[moodle]Xóa tất cả Service accounts không sử dụng.#<p>Nó không tự động xóa Service accounts không sử dụng.</p>
	~[moodle]Cấu hình bảo mật cho Service accounts.#<p>Nó tạo các thành phần, không phải cấu hình bảo mật chi tiết.</p>
	####<p><strong>Giải thích</strong>\: Khi một Namespace mới được tạo, Kubernetes controller manager tạo một ServiceAccount mặc định và token truy cập API cho Namespace đó.</p>
}

// question: 11.26 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Tại sao nên tắt tự động mount token ServiceAccount nếu Pod không cần nó?</p>{
	~[moodle]Để tăng hiệu suất của Pod.#<p>Ảnh hưởng hiệu suất là tối thiểu.</p>
	=[moodle]Để giảm rủi ro bảo mật ("blast radius").
	~[moodle]Để tiết kiệm bộ nhớ.#<p>Tiết kiệm bộ nhớ không phải lý do chính.</p>
	~[moodle]Để đơn giản hóa cấu hình.#<p>Nó có thể làm cấu hình phức tạp hơn một chút.</p>
	####<p><strong>Giải thích</strong>\: Nếu Pod không cần token ServiceAccount, việc tắt automountServiceAccountToken sẽ giảm "blast radius" (phạm vi ảnh hưởng) trong trường hợp bị tấn công.</p>
}

// question: 11.27 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Route controller trong CCM có vai trò gì?</p>{
	=[moodle]Thiết lập các tuyến đường trong cơ sở hạ tầng đám mây.
	~[moodle]Kiểm tra tình trạng của các tuyến đường mạng.#<p>Kiểm tra tình trạng là nhiệm vụ của các công cụ giám sát.</p>
	~[moodle]Cấu hình DNS cho các Pod.#<p>Cấu hình DNS là nhiệm vụ của CoreDNS.</p>
	~[moodle]Quản lý lưu lượng truy cập HTTP.#<p>Quản lý lưu lượng HTTP là nhiệm vụ của Ingress controllers.</p>
	####<p><strong>Giải thích</strong>\: Route controller chịu trách nhiệm thiết lập các tuyến đường trong cơ sở hạ tầng đám mây underlying.</p>
}

// question: 11.28 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Thành phần nào trong scheduler framework chịu trách nhiệm gán Pod vào nút đã chọn?</p>{
	~[moodle]PreFilter.#<p>PreFilter chuẩn bị dữ liệu.</p>
	~[moodle]Filter.#<p>Filter loại bỏ các nút không phù hợp.</p>
	~[moodle]Score.#<p>Score tính điểm cho các nút còn lại.</p>
	=[moodle]Bind.
	####<p><strong>Giải thích</strong>\: Giai đoạn Bind của scheduler là nơi Pod được gán vào nút đã chọn, lưu đối tượng Bind thông qua API server.</p>
}

// question: 11.29 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>Các verbs trong định nghĩa Role của RBAC bao gồm những gì?</p>{
	~[moodle]Chỉ các hành động HTTP như GET, POST.#<p>Các verbs mở rộng ra ngoài các hành động HTTP cơ bản.</p>
	=[moodle]Các động từ yêu cầu API như get, list, create, delete.
	~[moodle]Chỉ các lệnh shell cơ bản như ls, cat.#<p>Đây là các lệnh Linux, không phải verbs RBAC.</p>
	~[moodle]Các từ khóa đặc biệt để định nghĩa vai trò.#<p>verbs là các hành động cụ thể, không phải từ khóa.</p>
	####<p><strong>Giải thích</strong>\: Các verbs (động từ) trong định nghĩa Role bao gồm các động từ yêu cầu API như get, list, create, update, delete, v.v..</p>
}

// question: 11.30 name: Chapter 11: The core of the control plane
::Chapter 11\: The core of the control plane::[html]<p>PreBind plugin trong scheduler framework có vai trò gì?</p>{
	=[moodle]Thực hiện các hành động trước khi binding thực sự xảy ra, như chuẩn bị volume.
	~[moodle]Đánh giá khả năng của nút để chấp nhận Pod.#<p>Đó là chức năng của Filter và Score.</p>
	~[moodle]Sắp xếp thứ tự các Pod.#<p>Sắp xếp Pod là của QueueSort.</p>
	~[moodle]Cập nhật trạng thái của Pod trong API server.#<p>Bind là hành động lưu trữ đối tượng Bind vào API server.</p>
	####<p><strong>Giải thích</strong>\: PreBind plugin thực hiện các hành động trước khi binding thực sự xảy ra, thường liên quan đến việc chuẩn bị volume cho Pod.</p>
}

// Chapter 12: etcd and the control plane
// question: 12 name: Switch category to $module$/top/Chapter 12: etcd and the control plane
$CATEGORY: $module$/top/Chapter 12: etcd and the control plane

// question: 12.1 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>etcd là gì trong bối cảnh Kubernetes?</p>{
	~[moodle]Một database SQL để lưu trữ log.#<p>etcd không phải database SQL và không phải lưu trữ log chính.</p>
	=[moodle]Một kho lưu trữ key/value với các đảm bảo tính nhất quán mạnh mẽ.
	~[moodle]Một giao thức mạng để giao tiếp Pod-to-Pod.#<p>Giao thức mạng cho Pod-to-Pod là nhiệm vụ của CNI.</p>
	~[moodle]Một công cụ cân bằng tải cho các dịch vụ.#<p>Cân bằng tải là nhiệm vụ của kube-proxy và LoadBalancers.</p>
	####<p><strong>Giải thích</strong>\: etcd là một kho lưu trữ key/value với các đảm bảo tính nhất quán mạnh mẽ, đóng vai trò quan trọng trong control plane.</p>
}

// question: 12.2 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Các thành phần của control plane (scheduler, kubelet, controller manager) giao tiếp với nhau như thế nào?</p>{
	~[moodle]Trực tiếp với nhau thông qua RPC.#<p>Giao tiếp không trực tiếp mà thông qua API server.</p>
	=[moodle]Bằng cách cập nhật API server.
	~[moodle]Thông qua một message queue độc lập.#<p>Message queue không phải là cơ chế chính.</p>
	~[moodle]Qua giao thức UDP.#<p>Giao thức UDP không phải là cơ chế chính.</p>
	####<p><strong>Giải thích</strong>\: Các thành phần này giao tiếp với nhau bằng cách cập nhật API server, giúp chúng được tách rời mạnh mẽ.</p>
}

// question: 12.3 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Tại sao việc có nhiều nút etcd (tối thiểu 3) lại được khuyến nghị trong một cụm sản xuất?</p>{
	~[moodle]Để tăng tốc độ đọc dữ liệu.#<p>Dự phòng tăng tính khả dụng, không nhất thiết tăng tốc độ đọc.</p>
	=[moodle]Để cung cấp tính dự phòng và chịu lỗi.
	~[moodle]Để giảm chi phí lưu trữ.#<p>Nhiều nút sẽ tăng chi phí, không giảm.</p>
	~[moodle]Để đơn giản hóa việc cấu hình.#<p>Nhiều nút làm cấu hình phức tạp hơn.</p>
	####<p><strong>Giải thích</strong>\: Cần có các nút etcd dự phòng (tối thiểu 3) để chịu lỗi trong trường hợp một nút tính toán bị hỏng.</p>
}

// question: 12.4 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Mọi hành động của API server (ví dụ kubectl create) đều dẫn đến một ghi (write) đồng bộ vào đâu?</p>{
	~[moodle]Log file.#<p>Log file ghi lại các sự kiện, không phải là nơi lưu trữ trạng thái nhất quán.</p>
	=[moodle]etcd.
	~[moodle]Cache cục bộ.#<p>Cache cục bộ là tạm thời.</p>
	~[moodle]Database tạm thời.#<p>Database tạm thời không có tính bền vững.</p>
	####<p><strong>Giải thích</strong>\: Mọi hành động của API server đều dẫn đến một ghi đồng bộ vào etcd, đảm bảo yêu cầu được lưu trữ trên đĩa.</p>
}

// question: 12.5 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>etcd v3 có gì tốt hơn etcd v2 về hiệu suất?</p>{
	~[moodle]Sử dụng RESTful API.#<p>etcd v3 sử dụng gRPC, không phải RESTful API.</p>
	~[moodle]Có không gian khóa phân cấp.#<p>etcd v3 có không gian khóa phẳng, không phân cấp.</p>
	=[moodle]Sử dụng gRPC cho các giao dịch nhanh hơn.
	~[moodle]Hỗ trợ ít client hơn.#<p>etcd v3 hỗ trợ hàng nghìn client hiệu quả hơn.</p>
	####<p><strong>Giải thích</strong>\: etcd v3 sử dụng gRPC cho các giao dịch nhanh hơn và có hiệu suất tốt hơn v2.</p>
}

// question: 12.6 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Chức năng watch của etcd có vai trò gì trong Kubernetes?</p>{
	~[moodle]Ngăn chặn các ghi dữ liệu đồng thời.#<p>watch không ngăn chặn ghi dữ liệu.</p>
	=[moodle]Cho phép các controller phản hồi các sự kiện API.
	~[moodle]Mã hóa dữ liệu lưu trữ.#<p>Mã hóa dữ liệu là một khía cạnh riêng.</p>
	~[moodle]Tự động sao lưu dữ liệu.#<p>watch không tự động sao lưu dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: Chức năng watch cho phép các controller của Kubernetes "quan sát" các tài nguyên API và phản hồi các sự kiện mới (ví dụ: tạo Pod).</p>
}

// question: 12.7 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Tại sao etcd được chọn làm database cho Kubernetes thay vì các database khác như ZooKeeper?</p>{
	~[moodle]Vì nó có API cấp thấp hơn.#<p>ZooKeeper có API cấp thấp hơn.</p>
	=[moodle]Vì nó có mô hình nhất quán nghiêm ngặt dựa trên giao thức Raft.
	~[moodle]Vì nó không hỗ trợ chức năng watch.#<p>etcd v3 hỗ trợ chức năng watch rất hiệu quả.</p>
	~[moodle]Vì nó được thiết kế cho các tập dữ liệu lớn.#<p>etcd không được thiết kế cho các tập dữ liệu lớn.</p>
	####<p><strong>Giải thích</strong>\: etcd có mô hình nhất quán nghiêm ngặt dựa trên giao thức Raft, phù hợp hơn để điều phối các trung tâm dữ liệu.</p>
}

// question: 12.8 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>fsync operations đóng vai trò gì trong việc đảm bảo tính nhất quán của etcd?</p>{
	~[moodle]Tăng tốc độ ghi dữ liệu lên RAM.#<p>fsync liên quan đến đĩa, không phải RAM, và có thể làm chậm hoạt động.</p>
	=[moodle]Đảm bảo dữ liệu được ghi vật lý xuống đĩa trước khi trả về kết quả.
	~[moodle]Nén dữ liệu trước khi lưu trữ.#<p>fsync không liên quan đến nén dữ liệu.</p>
	~[moodle]Giảm số lượng nút etcd cần thiết.#<p>fsync đảm bảo tính nhất quán, không ảnh hưởng trực tiếp đến số nút.</p>
	####<p><strong>Giải thích</strong>\: fsync operations chặn các ghi đĩa, đảm bảo rằng etcd nhất quán bằng cách ghi dữ liệu vật lý xuống đĩa trước khi trả về.</p>
}

// question: 12.9 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Nếu thời gian fsync của etcd quá chậm (ví dụ: gần 1 giây), điều gì có thể xảy ra với cụm Kubernetes?</p>{
	~[moodle]Cụm sẽ hoạt động nhanh hơn.#<p>Hiệu suất sẽ giảm, không tăng.</p>
	=[moodle]Cụm Kubernetes có thể bị chậm lại hoặc hỏng.
	~[moodle]etcd sẽ tự động chuyển sang chế độ chỉ đọc.#<p>etcd không tự động chuyển sang chế độ chỉ đọc.</p>
	~[moodle]Các Pods sẽ được lập lịch trên các nút khác.#<p>Lập lịch Pod bị ảnh hưởng bởi hiệu suất etcd, nhưng không giải quyết được vấn đề cơ bản.</p>
	####<p><strong>Giải thích</strong>\: Nếu thời gian fsync kéo dài gần 1 giây, đây là dấu hiệu hiệu suất đang gặp rủi ro và cụm Kubernetes có thể chậm lại hoặc bị hỏng.</p>
}

// question: 12.10 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>CAP theorem đề cập đến những lựa chọn đánh đổi nào trong hệ thống phân tán?</p>{
	~[moodle]Compute, Access, Performance.#<p>Đây là những khái niệm không phải của CAP theorem.</p>
	=[moodle]Consistency, Availability, Partitionability.
	~[moodle]Capacity, Authentication, Persistence.#<p>Đây là những khái niệm không phải của CAP theorem.</p>
	~[moodle]Configuration, Administration, Protocols.#<p>Đây là những khái niệm không phải của CAP theorem.</p>
	####<p><strong>Giải thích</strong>\: CAP theorem chỉ ra rằng bạn phải chọn giữa Consistency (nhất quán), Availability (khả dụng) và Partitionability (khả năng phân vùng).</p>
}

// question: 12.11 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>etcd không được thiết kế để lưu trữ loại dữ liệu nào?</p>{
	~[moodle]Cấu hình và metadata cho hệ thống phân tán.#<p>etcd lý tưởng cho cấu hình và metadata.</p>
	=[moodle]Các tập dữ liệu lớn hoặc dữ liệu ứng dụng.
	~[moodle]Key/value pairs nhỏ.#<p>etcd lý tưởng cho các key/value pairs nhỏ.</p>
	~[moodle]Trạng thái mong muốn của cụm.#<p>etcd lưu trữ trạng thái mong muốn của cụm.</p>
	####<p><strong>Giải thích</strong>\: etcd không được thiết kế để lưu trữ các tập dữ liệu lớn hoặc dữ liệu ứng dụng, mà chỉ dùng cho cấu hình và metadata.</p>
}

// question: 12.12 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Giới hạn kích thước mặc định cho một yêu cầu (request) trong etcd là bao nhiêu?</p>{
	~[moodle]2 GB.#<p>2 GB là giới hạn lưu trữ mặc định của database.</p>
	~[moodle]10 KB.#<p>10 KB là ước tính cho mỗi namespace.</p>
	=[moodle]1.5 MiB.
	~[moodle]64 GB.#<p>64 GB là RAM khuyến nghị cho cụm lớn.</p>
	####<p><strong>Giải thích</strong>\: Theo mặc định, kích thước tối đa của bất kỳ yêu cầu nào trong etcd là 1.5 MiB.</p>
}

// question: 12.13 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Tại sao etcd encryption at rest (mã hóa dữ liệu khi không hoạt động) lại quan trọng?</p>{
	~[moodle]Để tăng hiệu suất truy cập dữ liệu.#<p>Mã hóa có thể làm giảm hiệu suất truy cập.</p>
	=[moodle]Để bảo vệ thông tin nhạy cảm như mật khẩu database.
	~[moodle]Để giảm kích thước của database.#<p>Mã hóa không giảm kích thước database.</p>
	~[moodle]Để đồng bộ hóa dữ liệu nhanh hơn.#<p>Mã hóa không đồng bộ hóa dữ liệu nhanh hơn.</p>
	####<p><strong>Giải thích</strong>\: etcd encryption at rest quan trọng để bảo vệ thông tin nhạy cảm như mật khẩu database, vì chúng được lưu trữ trong etcd.</p>
}

// question: 12.14 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Khi cấu hình etcd cho triển khai phân tán địa lý, heartbeat-interval và election-timeout nên được đặt như thế nào?</p>{
	~[moodle]Cả hai đều nên ngắn.#<p>Ngắn có thể gây ra lưu lượng mạng và bầu chọn leader thường xuyên hơn.</p>
	=[moodle]Cả hai đều nên dài hơn.
	~[moodle]heartbeat-interval ngắn, election-timeout dài.#<p>Cả hai đều cần được tăng lên trong môi trường phân tán.</p>
	~[moodle]heartbeat-interval dài, election-timeout ngắn.#<p>Cả hai đều cần được tăng lên trong môi trường phân tán.</p>
	####<p><strong>Giải thích</strong>\: Với triển khai phân tán địa lý, nên khởi động etcd với heartbeat-interval và election-timeout dài hơn để giảm lưu lượng và tránh bầu chọn leader không cần thiết.</p>
}

// question: 12.15 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Nested virtualization ảnh hưởng đến etcd như thế nào?</p>{
	~[moodle]Tăng hiệu suất I/O.#<p>Nó làm giảm hiệu suất I/O.</p>
	=[moodle]Hạn chế IOPS và dẫn đến lỗi ghi thường xuyên, làm etcd không đáng tin cậy.
	~[moodle]Giúp etcd dễ dàng đồng bộ hóa hơn.#<p>Nó làm cho việc đồng bộ hóa khó khăn hơn.</p>
	~[moodle]Không ảnh hưởng gì đến etcd.#<p>Nó có ảnh hưởng lớn đến etcd.</p>
	####<p><strong>Giải thích</strong>\: Nested virtualization hạn chế IOPS và dẫn đến lỗi ghi phổ biến, làm etcd trở nên cực kỳ không đáng tin cậy do độ trễ ghi đĩa.</p>
}

// question: 12.16 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>etcdctl là một công cụ gì?</p>{
	~[moodle]Một GUI để quản lý etcd.#<p>etcdctl là công cụ CLI, không phải GUI.</p>
	=[moodle]Một công cụ dòng lệnh mạnh mẽ để kiểm tra và chẩn đoán etcd.
	~[moodle]Một dịch vụ chạy bên trong Pod.#<p>Nó là một công cụ độc lập, không phải dịch vụ bên trong Pod.</p>
	~[moodle]Một plugin của CoreDNS.#<p>Nó không liên quan đến CoreDNS.</p>
	####<p><strong>Giải thích</strong>\: etcdctl là một công cụ dòng lệnh mạnh mẽ để kiểm tra các cặp key/value, stress test và chẩn đoán các vấn đề trên nút etcd.</p>
}

// question: 12.17 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Mặc dù Kubernetes có thể hỗ trợ các OS không phải Linux cho workloads (ví dụ Windows), nhưng các thành phần control plane vẫn chủ yếu chạy trên hệ điều hành nào?</p>{
	~[moodle]macOS.#<p>macOS không được hỗ trợ đầy đủ cho etcd sản xuất.</p>
	~[moodle]Windows.#<p>Windows không được hỗ trợ đầy đủ cho etcd và các thành phần control plane khác.</p>
	=[moodle]Linux.
	~[moodle]Bất kỳ OS nào.#<p>Không phải bất kỳ OS nào.</p>
	####<p><strong>Giải thích</strong>\: API server, scheduler, controller managers và etcd chỉ được hỗ trợ trên Linux, ngay cả trong các cụm Kubernetes hỗ trợ Windows workloads.</p>
}

// question: 12.18 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>etcd v3 có khả năng quan sát nhiều bản ghi (records) qua bao nhiêu kết nối TCP?</p>{
	~[moodle]Nhiều kết nối TCP cho mỗi bản ghi.#<p>Đây là đặc điểm của etcd v2 hoặc các database khác.</p>
	=[moodle]Một kết nối TCP duy nhất.
	~[moodle]Không hỗ trợ quan sát bản ghi.#<p>etcd hỗ trợ mạnh mẽ chức năng watch.</p>
	~[moodle]Chỉ quan sát được 1 bản ghi qua 1 kết nối.#<p>Đây là hạn chế của etcd v2.</p>
	####<p><strong>Giải thích</strong>\: etcd v3 có khả năng quan sát nhiều bản ghi qua một kết nối TCP duy nhất, tối ưu hóa cho các cụm Kubernetes lớn.</p>
}

// question: 12.19 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Tại sao kubeadm không đi kèm với một giải pháp etcd end-to-end cho các trường hợp sản xuất?</p>{
	~[moodle]Vì kubeadm chỉ dành cho môi trường phát triển.#<p>kubeadm là nền tảng cho nhiều bản phân phối Kubernetes.</p>
	=[moodle]Để cho phép người dùng tùy chỉnh và kiến trúc etcd riêng.
	~[moodle]Vì etcd quá đơn giản để cần quản lý.#<p>etcd là phức tạp ở quy mô lớn.</p>
	~[moodle]kubeadm không cần etcd.#<p>kubeadm yêu cầu etcd.</p>
	####<p><strong>Giải thích</strong>\: kubeadm là một trình cài đặt mặc định nhưng không có giải pháp etcd end-to-end, cho phép người dùng đưa kho dữ liệu etcd của riêng họ để đáp ứng các yêu cầu về khả năng mở rộng.</p>
}

// question: 12.20 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Khi trực quan hóa hiệu suất etcd bằng Prometheus, chỉ số quan trọng cần xem xét để đánh giá thời gian ghi đĩa là gì?</p>{
	~[moodle]etcd_server_is_leader.#<p>Chỉ số này cho biết nút hiện tại có phải là leader không.</p>
	~[moodle]etcd_request_duration_seconds.#<p>Đây là thời gian yêu cầu tổng thể, không cụ thể cho ghi đĩa.</p>
	=[moodle]etcd_disk_wal_fsync_duration_seconds.
	~[moodle]etcd_network_peer_sent_bytes_total.#<p>Chỉ số này liên quan đến lưu lượng mạng giữa các peer.</p>
	####<p><strong>Giải thích</strong>\: Chỉ số etcd_disk_wal_fsync_duration_seconds cho biết thời gian các thao tác ghi vào đĩa của etcd đang diễn ra, là một chỉ số quan trọng về hiệu suất ghi.</p>
}

// question: 12.21 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Lý do chính tại sao nested virtualization gây nguy hiểm cho cấu hình phần cứng của etcd là gì?</p>{
	~[moodle]Nó gây ra sự cạnh tranh tài nguyên CPU.#<p>Nó cũng có thể gây cạnh tranh CPU nhưng độ trễ ghi đĩa là vấn đề lớn nhất.</p>
	=[moodle]Nó tăng độ trễ cho các hoạt động ghi vào ổ đĩa.
	~[moodle]Nó làm etcd tiêu thụ quá nhiều bộ nhớ.#<p>Bộ nhớ tiêu thụ không phải vấn đề chính của nested virtualization.</p>
	~[moodle]Nó chặn các yêu cầu mạng của etcd.#<p>Nó không chặn các yêu cầu mạng một cách trực tiếp.</p>
	####<p><strong>Giải thích</strong>\: Lý do chính là nested virtualization tăng độ trễ cho các hoạt động ghi vào ổ cứng, làm etcd trở nên cực kỳ không đáng tin cậy.</p>
}

// question: 12.22 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>etcd quản lý việc cân bằng tải ở cấp độ client như thế nào?</p>{
	~[moodle]Bằng cách sử dụng một load balancer phần cứng bên ngoài.#<p>Kubernetes có thể sử dụng load balancer bên ngoài, nhưng etcd client cũng có logic cân bằng tải riêng.</p>
	=[moodle]Bằng cách duy trì kết nối TCP với một endpoint được chọn từ tất cả các endpoint được cung cấp.
	~[moodle]Bằng cách gán IP tĩnh cho mỗi client.#<p>etcd không gán IP tĩnh cho client.</p>
	~[moodle]Bằng cách sử dụng DNS để phân phối tải.#<p>DNS có thể được sử dụng để khám phá endpoint etcd, nhưng cơ chế cân bằng tải là ở cấp độ client.</p>
	####<p><strong>Giải thích</strong>\: etcd giữ một kết nối TCP đến một endpoint được chọn từ tất cả các endpoint được cung cấp cho client, và có thể failover sang endpoint khác khi mất kết nối.</p>
}

// question: 12.23 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Giới hạn lưu trữ mặc định của database etcd là bao nhiêu?</p>{
	~[moodle]1.5 MiB.#<p>1.5 MiB là giới hạn tải trọng tối đa cho một yêu cầu.</p>
	=[moodle]2 GB.
	~[moodle]8 GB.#<p>8 GB là kích thước khuyến nghị, không phải giới hạn mặc định.</p>
	~[moodle]64 GB.#<p>64 GB là dung lượng RAM khuyến nghị cho cụm lớn.</p>
	####<p><strong>Giải thích</strong>\: Giới hạn lưu trữ mặc định của database etcd là 2 GB, mặc dù khuyến nghị nên giữ dưới 8 GB.</p>
}

// question: 12.24 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Write-ahead log của etcd có vai trò gì?</p>{
	~[moodle]Cải thiện tốc độ đọc dữ liệu.#<p>Nó không trực tiếp cải thiện tốc độ đọc.</p>
	=[moodle]Ghi lại tất cả các thay đổi trước khi chúng được áp dụng vào database.
	~[moodle]Đồng bộ hóa dữ liệu giữa các nút etcd.#<p>Nó là một phần của cơ chế nhất quán, nhưng không phải là đồng bộ hóa dữ liệu tổng thể.</p>
	~[moodle]Giảm thiểu việc sử dụng bộ nhớ.#<p>Nó có thể tiêu thụ tài nguyên đĩa, không phải giảm bộ nhớ.</p>
	####<p><strong>Giải thích</strong>\: Write-ahead log của etcd ghi lại tất cả các thay đổi trước khi chúng được áp dụng vào database, đảm bảo tính bền vững và khả năng phục hồi dữ liệu.</p>
}

// question: 12.25 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Khi nào etcd v2 bị coi là không còn được hỗ trợ bởi Kubernetes?</p>{
	~[moodle]Sau Kubernetes 1.10.#<p>Không chính xác.</p>
	=[moodle]Sau Kubernetes 1.13.0.
	~[moodle]Sau Kubernetes 1.17.#<p>Không chính xác.</p>
	~[moodle]etcd v2 vẫn được hỗ trợ đầy đủ.#<p>Không chính xác.</p>
	####<p><strong>Giải thích</strong>\: Bất kỳ phiên bản Kubernetes nào sau 1.13.0 sẽ báo lỗi "etcd2 is no longer a supported storage backend".</p>
}

// question: 12.26 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Leasing mechanism trong etcd được Kubernetes sử dụng để làm gì?</p>{
	~[moodle]Cấp phát địa chỉ IP cho Pods.#<p>Cấp phát IP là nhiệm vụ của CNI.</p>
	=[moodle]Tối ưu hóa hiệu suất của các cụm lớn và giảm độ "chát" mạng.
	~[moodle]Mã hóa giao tiếp giữa các thành phần control plane.#<p>Leasing không liên quan đến mã hóa giao tiếp.</p>
	~[moodle]Quản lý lưu trữ bền vững cho ứng dụng.#<p>Lưu trữ bền vững là PersistentVolumes/CSI.</p>
	####<p><strong>Giải thích</strong>\: etcd leasing mechanism được Kubernetes 1.17 trở lên sử dụng để tối ưu hóa hiệu suất của các cụm lớn và giảm độ "chát" mạng giữa kubelet và API server.</p>
}

// question: 12.27 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Làm cách nào để một client etcd thiết lập trên một cụm kind?</p>{
	~[moodle]Cài đặt etcd server trực tiếp trên nút kind.#<p>etcd thường đã chạy trong một Pod trên nút control plane.</p>
	=[moodle]Sử dụng một Pod với hostNetwork: true và mount các chứng chỉ etcd.
	~[moodle]Chạy etcdctl từ bên ngoài cụm.#<p>Có thể chạy etcdctl từ bên ngoài, nhưng thiết lập client bên trong Pod là cách được mô tả.</p>
	~[moodle]Cấu hình CoreDNS để trỏ tới etcd.#<p>CoreDNS không trỏ tới etcd trực tiếp.</p>
	####<p><strong>Giải thích</strong>\: Để thiết lập một client etcd trên cụm kind, bạn có thể tạo một Pod với hostNetwork: true và mount các chứng chỉ bảo mật etcd vào Pod đó.</p>
}

// question: 12.28 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Tại sao việc tắt swap hoàn toàn là yêu cầu đối với các cài đặt kubelet?</p>{
	~[moodle]Để tăng tính nhất quán của etcd.#<p>swap không liên quan đến tính nhất quán của etcd.</p>
	=[moodle]Để đảm bảo hiệu suất truy cập bộ nhớ được dự đoán được.
	~[moodle]Để giảm tải CPU của nút.#<p>Tắt swap không trực tiếp giảm tải CPU.</p>
	~[moodle]Để tiết kiệm không gian đĩa.#<p>Nó không nhằm mục đích tiết kiệm không gian đĩa.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes tắt swap hoàn toàn để đảm bảo hiệu suất bộ nhớ nhất quán và dễ dự đoán, vì việc hoán đổi bộ nhớ có thể gây ra độ trễ không mong muốn.</p>
}

// question: 12.29 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>Nếu bạn muốn biết cgroups nào tồn tại cho scheduler trong Linux kernel, lệnh nào có thể được sử dụng?</p>{
	~[moodle]ps -ax | grep scheduler.#<p>Lệnh này chỉ tìm PID của scheduler.</p>
	=[moodle]cat /proc/<PID>/cgroup.
	~[moodle]kubectl get pods -A.#<p>Lệnh này liệt kê Pods trong Kubernetes, không phải cgroups kernel.</p>
	~[moodle]systemctl status.#<p>Lệnh này hiển thị trạng thái của systemd, không phải cgroups cụ thể.</p>
	####<p><strong>Giải thích</strong>\: Sau khi tìm được PID của scheduler (ví dụ bằng ps -ax), bạn có thể dùng cat /proc/<PID>/cgroup để hỏi Linux kernel về các cgroups của nó.</p>
}

// question: 12.30 name: Chapter 12: etcd and the control plane
::Chapter 12\: etcd and the control plane::[html]<p>etcd_disk_wal_fsync_duration_seconds_bucket{le="0.001"} 1239 trong Prometheus metric cho biết điều gì?</p>{
	~[moodle]1239 yêu cầu mất chính xác 0.001 giây.#<p>Bucket le là "less than or equal to", không phải chính xác.</p>
	=[moodle]1239 hoạt động ghi đĩa diễn ra trong 0.001 giây hoặc ít hơn.
	~[moodle]Tổng thời gian ghi đĩa là 1239 giây.#<p>sum mới là tổng thời gian.</p>
	~[moodle]Chỉ có 1239 hoạt động ghi đĩa.#<p>count là tổng số hoạt động ghi đĩa.</p>
	####<p><strong>Giải thích</strong>\: Giá trị 1239 trong bucket le="0.001" cho biết có 1239 hoạt động ghi đĩa hoàn thành trong 0.001 giây hoặc ít hơn.</p>
}

// Chapter 13: Container and Pod security
// question: 13 name: Switch category to $module$/top/Chapter 13: Container and Pod security
$CATEGORY: $module$/top/Chapter 13: Container and Pod security

// question: 13.1 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Khái niệm "blast radius" trong bảo mật Kubernetes đề cập đến điều gì?</p>{
	~[moodle]Phạm vi của các bản vá bảo mật cần áp dụng cho một ứng dụng.#<p>"Blast radius" không phải là về phạm vi bản vá bảo mật.</p>
	=[moodle]Mức độ tác động và lan truyền của một cuộc tấn công bảo mật.
	~[moodle]Số lượng container tối đa có thể chạy trên một node.#<p>Nó không liên quan đến số lượng container trên một node.</p>
	~[moodle]Khả năng phục hồi của hệ thống sau một sự cố mạng.#<p>Khả năng phục hồi hệ thống là một khía cạnh khác của bảo mật, không phải định nghĩa của "blast radius".</p>
	####<p><strong>Giải thích</strong>\: "Blast radius" đề cập đến phạm vi và độ sâu của một cuộc xâm nhập bảo mật, tức là mức độ một cuộc tấn công có thể lan rộng và gây thiệt hại.</p>
}

// question: 13.2 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Thực hành tốt nhất nào được khuyến nghị để giảm "blast radius" của các ứng dụng không phải controller chạy trong kube-system namespace?</p>{
	=[moodle]Di chuyển tất cả các ứng dụng ra khỏi kube-system namespace.
	~[moodle]Giới hạn quyền truy cập mạng cho các Pod trong kube-system.#<p>Giới hạn quyền truy cập mạng là một biện pháp bảo mật chung, không phải là cách chính để giảm "blast radius" do vị trí.</p>
	~[moodle]Sử dụng các Pod có tài nguyên hạn chế trong kube-system.#<p>Hạn chế tài nguyên là để quản lý hiệu suất và độ ổn định, không phải trực tiếp giảm "blast radius" về mặt bảo mật.</p>
	~[moodle]Thường xuyên cập nhật các bản vá bảo mật cho kube-system.#<p>Cập nhật bản vá là một thực hành bảo mật chung cho mọi namespace.</p>
	####<p><strong>Giải thích</strong>\: Một trong những lý do chính không nên sử dụng kube-system namespace là các ứng dụng không phải controller chạy trong đó sẽ làm tăng "blast radius" của cuộc xâm nhập bảo mật.</p>
}

// question: 13.3 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Theo nguồn, việc đầu tiên cần làm khi có kế hoạch bảo mật container là gì?</p>{
	~[moodle]Cấu hình xác thực đa yếu tố cho quyền truy cập container.#<p>Xác thực đa yếu tố là một phần của quản lý truy cập, không phải kế hoạch cập nhật container.</p>
	=[moodle]Lên kế hoạch cập nhật container và phần mềm tùy chỉnh thường xuyên.
	~[moodle]Giới hạn kích thước của các image container.#<p>Giới hạn kích thước container là một thực hành tốt, nhưng không phải bước đầu tiên trong việc lập kế hoạch cập nhật.</p>
	~[moodle]Sử dụng công cụ linter để quét lỗ hổng.#<p>Công cụ linter được sử dụng để quét các lỗi cấu hình hoặc lỗ hổng, không phải là kế hoạch cập nhật.</p>
	####<p><strong>Giải thích</strong>\: Kế hoạch cập nhật container và phần mềm tùy chỉnh là một trong những thực hành bảo mật container được đề xuất đầu tiên.</p>
}

// question: 13.4 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Tại sao việc chạy container với người dùng không phải root lại là một thực hành bảo mật được khuyến nghị?</p>{
	~[moodle]Giảm chi phí tài nguyên hệ thống.#<p>Việc này không trực tiếp giảm chi phí tài nguyên hệ thống.</p>
	~[moodle]Ngăn chặn container truy cập internet.#<p>Nó không ảnh hưởng đến khả năng truy cập internet của container.</p>
	=[moodle]Giảm đáng kể các rủi ro bảo mật tiềm ẩn.
	~[moodle]Tăng tốc độ khởi động của container.#<p>Không có mối liên hệ trực tiếp với tốc độ khởi động container.</p>
	####<p><strong>Giải thích</strong>\: Chạy container với người dùng không phải root là một thực hành được khuyến nghị để tránh các vấn đề bảo mật. Nếu container bị xâm nhập, các hành động độc hại sẽ bị hạn chế bởi quyền của người dùng không phải root.</p>
}

// question: 13.5 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Dự án "distroless" của Google hỗ trợ thực hành bảo mật container nào?</p>{
	~[moodle]Giảm thời gian downtime của ứng dụng.#<p>Mặc dù container nhỏ có thể gián tiếp góp phần vào độ ổn định, nhưng đây không phải là mục tiêu chính của distroless.</p>
	=[moodle]Sử dụng container nhỏ nhất có thể.
	~[moodle]Tăng cường khả năng giao tiếp giữa các container.#<p>Distroless không liên quan đến việc tăng cường giao tiếp.</p>
	~[moodle]Tự động mã hóa dữ liệu trong container.#<p>Distroless không cung cấp tính năng mã hóa dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: Dự án "distroless" của Google cung cấp các tùy chọn container nhẹ, chỉ chứa những gì cần thiết cho ứng dụng, giúp giảm thiểu dấu vết lỗ hổng.</p>
}

// question: 13.6 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>"Container provenance" trong ngữ cảnh bảo mật container liên quan đến điều gì?</p>{
	=[moodle]Nguồn gốc của các image container và thành phần của chúng.
	~[moodle]Hiệu suất của container trên các kiến trúc phần cứng khác nhau.#<p>Không liên quan đến hiệu suất trên các kiến trúc khác nhau.</p>
	~[moodle]Khả năng di chuyển của container giữa các môi trường.#<p>Không liên quan đến khả năng di chuyển.</p>
	~[moodle]Phương pháp quản lý vòng đời của container.#<p>Provenance là một khía cạnh của việc theo dõi nguồn gốc, không phải quản lý vòng đời.</p>
	####<p><strong>Giải thích</strong>\: "Container provenance" đề cập đến việc xác định nguồn gốc của các image container và đảm bảo tính toàn vẹn của các thành phần bên trong.</p>
}

// question: 13.7 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>"Linters for containers" được sử dụng cho mục đích gì trong bảo mật container?</p>{
	~[moodle]Tối ưu hóa hiệu suất của container.#<p>Linters không trực tiếp tối ưu hóa hiệu suất.</p>
	~[moodle]Đảm bảo tính nhất quán của cấu hình.#<p>Mặc dù có thể kiểm tra tính nhất quán, mục đích chính là tìm lỗi bảo mật.</p>
	=[moodle]Quét các lỗ hổng hoặc lỗi cấu hình trong container.
	~[moodle]Tự động triển khai các bản cập nhật bảo mật.#<p>Việc tự động triển khai bản cập nhật không phải là chức năng của linters.</p>
	####<p><strong>Giải thích</strong>\: "Linters for containers" là các công cụ được sử dụng để quét các lỗ hổng tiềm ẩn trong cấu hình và nội dung của container.</p>
}

// question: 13.8 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>"Security context" trong định nghĩa Pod được sử dụng để làm gì?</p>{
	~[moodle]Định nghĩa chính sách mạng cho Pod.#<p>Chính sách mạng được định nghĩa bằng NetworkPolicies.</p>
	=[moodle]Cấu hình các thiết lập bảo mật cấp độ Pod hoặc container.
	~[moodle]Quản lý việc lưu trữ dữ liệu bền vững cho Pod.#<p>Lưu trữ dữ liệu được quản lý bằng PersistentVolumes.</p>
	~[moodle]Xác định cách Pod tương tác với API server.#<p>Tương tác với API server liên quan đến ServiceAccounts và RBAC.</p>
	####<p><strong>Giải thích</strong>\: "Security context" được sử dụng để định nghĩa các thiết lập bảo mật và đặc quyền cho một Pod hoặc container.</p>
}

// question: 13.9 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Giá trị runAsUser trong "security context" của một Pod có tác dụng gì?</p>{
	=[moodle]Xác định người dùng chạy tiến trình chính của container.
	~[moodle]Đặt ID của nhóm chính cho tiến trình của container.#<p>runAsGroup đặt ID của nhóm chính.</p>
	~[moodle]Chỉ định ID nhóm sở hữu các thư mục được mount.#<p>fsGroup chỉ định ID nhóm sở hữu các volume được mount.</p>
	~[moodle]Thiết lập ID của người dùng để truy cập API server.#<p>Truy cập API server liên quan đến ServiceAccount.</p>
	####<p><strong>Giải thích</strong>\: runAsUser xác định ID của người dùng mà các tiến trình trong container sẽ chạy.</p>
}

// question: 13.10 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Khi một Pod với securityContext.runAsUser và runAsGroup cụ thể không thể khởi động, nguyên nhân phổ biến nhất là gì?</p>{
	~[moodle]Pod không có đủ quyền truy cập mạng.#<p>Vấn đề quyền truy cập mạng thường xuất hiện sau khi Pod khởi động.</p>
	=[moodle]Image container được cấu hình để chạy với người dùng root theo mặc định.
	~[moodle]Không có đủ tài nguyên CPU hoặc bộ nhớ.#<p>Thiếu tài nguyên dẫn đến trạng thái Pending hoặc OOMKilled, không phải lỗi trong securityContext.</p>
	~[moodle]PersistentVolume không được gắn kết thành công.#<p>Lỗi gắn kết volume cũng dẫn đến trạng thái Pending hoặc CrashLoopBackOff, nhưng ít liên quan đến runAsUser/Group.</p>
	####<p><strong>Giải thích</strong>\: Pod có thể không khởi động được nếu image container của nó được cấu hình để chạy với người dùng root theo mặc định, nhưng runAsUser trong securityContext lại chỉ định một người dùng không phải root.</p>
}

// question: 13.11 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Khả năng (capabilities) Linux NET_ADMIN và BPF cấp cho Pod quyền gì?</p>{
	~[moodle]Quyền truy cập đầy đủ vào hệ thống tệp tin của host.#<p>CAP_SYS_ADMIN mới cấp quyền truy cập hệ thống tệp tin rộng hơn, không phải NET_ADMIN hay BPF.</p>
	=[moodle]Quyền quản trị mạng và sử dụng bộ lọc gói tin nâng cao.
	~[moodle]Quyền khởi động lại node mà Pod đang chạy.#<p>CAP_SYS_BOOT là khả năng khởi động lại node.</p>
	~[moodle]Quyền thực thi bất kỳ lệnh nào với quyền root.#<p>CAP_SYS_ADMIN cơ bản tương đương với quyền root.</p>
	####<p><strong>Giải thích</strong>\: NET_ADMIN cho phép quản trị mạng (ví dụ: sửa đổi quy tắc iptables), và BPF cho phép sử dụng các chức năng Bộ lọc Gói tin Berkeley nâng cao.</p>
}

// question: 13.12 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Điều gì xảy ra khi CAP_SYS_ADMIN được cấp cho một Pod?</p>{
	~[moodle]Pod sẽ chỉ có quyền đọc trên hệ thống tệp tin host.#<p>CAP_SYS_ADMIN cấp quyền ghi, không chỉ đọc.</p>
	~[moodle]Pod có thể quản lý cgroups và namespaces một cách an toàn.#<p>CAP_SYS_ADMIN có thể quản lý chúng, nhưng không an toàn.</p>
	=[moodle]Nó cơ bản cấp quyền root cho Pod, rất nguy hiểm.
	~[moodle]Pod sẽ có quyền truy cập độc quyền vào một CPU core.#<p>CAP_SYS_ADMIN không liên quan đến quyền truy cập CPU độc quyền.</p>
	####<p><strong>Giải thích</strong>\: CAP_SYS_ADMIN cơ bản thiết lập quyền root cho Pod, làm cho nó cực kỳ mạnh mẽ và nguy hiểm.</p>
}

// question: 13.13 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Mục đích chính của "Pod Security Policies (PSPs)" là gì?</p>{
	=[moodle]Cung cấp một cách để kiểm soát các loại quyền và cấu hình Pod được phép.
	~[moodle]Giám sát lưu lượng mạng giữa các Pod.#<p>Giám sát lưu lượng mạng là chức năng của NetworkPolicies và các công cụ khác.</p>
	~[moodle]Quản lý vòng đời của các PersistentVolume.#<p>Quản lý PersistentVolume là chức năng của CSI và PersistentVolumeControllers.</p>
	~[moodle]Tự động chia tỷ lệ số lượng Pod trong một Deployment.#<p>Tự động chia tỷ lệ là chức năng của Horizontal Pod Autoscaler.</p>
	####<p><strong>Giải thích</strong>\: PSPs được sử dụng để đặt ra các quy tắc về các quyền và cấu hình Pod được phép trên một cluster, ví dụ như cấm chạy Pod với quyền root.</p>
}

// question: 13.14 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Theo Kubernetes v1.21, PSPs đã được đánh dấu là "deprecated". Điều gì sẽ thay thế chúng?</p>{
	~[moodle]Open Policy Agent (OPA).#<p>OPA là một công cụ chính sách chung, nhưng Pod Security Admission là giải pháp thay thế trực tiếp được tích hợp.</p>
	~[moodle]Container Runtime Interface (CRI).#<p>CRI là giao diện runtime container, không liên quan đến chính sách bảo mật Pod.</p>
	=[moodle]Pod Security Admission.
	~[moodle]NetworkPolicy.#<p>NetworkPolicy là để kiểm soát mạng, không phải bảo mật tổng thể của Pod.</p>
	####<p><strong>Giải thích</strong>\: PSPs bị deprecated trong Kubernetes v1.21 và dự kiến sẽ bị loại bỏ trong v1.25, được thay thế bởi Pod Security Admission.</p>
}

// question: 13.15 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Điều gì xảy ra khi PSPs được thêm vào một cluster và một số Pods đã chạy?</p>{
	~[moodle]Các Pod đang chạy sẽ tự động được cập nhật để tuân thủ chính sách mới.#<p>PSPs không tự động cập nhật Pods đang chạy.</p>
	~[moodle]Các Pod đang chạy sẽ bị dừng lại ngay lập tức nếu không tuân thủ.#<p>Pods không bị dừng ngay lập tức khi PSPs được thêm vào.</p>
	=[moodle]Các Pod đang chạy sẽ tiếp tục hoạt động, nhưng các Pod mới hoặc Pod được khởi động lại sẽ được kiểm tra.
	~[moodle]Cluster sẽ từ chối tất cả các Pod mới cho đến khi tất cả các Pod cũ được cập nhật.#<p>Cluster sẽ chỉ từ chối các Pod mới không tuân thủ, không phải tất cả các Pod.</p>
	####<p><strong>Giải thích</strong>\: PSPs được thực hiện tại thời điểm admission (khi Pod được tạo hoặc cập nhật). Các Pod đang chạy sẽ không bị ảnh hưởng ngay lập tức, nhưng nếu chúng chết và cần khởi động lại, chúng sẽ phải tuân thủ chính sách mới.</p>
}

// question: 13.16 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>"Service account token" của Pod được tự động gắn kết vào Pod trừ khi nào?</p>{
	~[moodle]automountServiceAccountToken được đặt thành true.#<p>automountServiceAccountToken là true theo mặc định.</p>
	~[moodle]Pod chạy trong kube-system namespace.#<p>kube-system namespace không ảnh hưởng đến cài đặt này.</p>
	=[moodle]automountServiceAccountToken được đặt thành false.
	~[moodle]Pod có "security context" với quyền root.#<p>security context không trực tiếp kiểm soát việc gắn kết token.</p>
	####<p><strong>Giải thích</strong>\: "Service account token" được tự động gắn kết vào Pod trừ khi người dùng vô hiệu hóa việc gắn kết bằng cách đặt automountServiceAccountToken thành false.</p>
}

// question: 13.17 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Tại sao nên vô hiệu hóa việc gắn kết "service account token" nếu Pod không cần nó?</p>{
	~[moodle]Để tiết kiệm tài nguyên bộ nhớ trên Pod.#<p>Lượng bộ nhớ tiết kiệm được là không đáng kể.</p>
	=[moodle]Để giảm bề mặt tấn công bảo mật của Pod.
	~[moodle]Để tăng tốc độ khởi động của Pod.#<p>Không có tác động đáng kể đến tốc độ khởi động.</p>
	~[moodle]Để đơn giản hóa cấu hình của Pod.#<p>Nó thêm một dòng cấu hình, không đơn giản hóa.</p>
	####<p><strong>Giải thích</strong>\: Nếu một Pod không cần "ServiceAccount token", việc vô hiệu hóa gắn kết sẽ giảm bề mặt tấn công bảo mật, vì token này cấp quyền truy cập vào API server.</p>
}

// question: 13.18 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>"Root-like Pods" là gì trong ngữ cảnh bảo mật Kubernetes?</p>{
	~[moodle]Các Pod chỉ chạy các tiến trình hệ thống quan trọng.#<p>Không chỉ giới hạn ở tiến trình hệ thống.</p>
	~[moodle]Các Pod có quyền truy cập vào tất cả các node trong cluster.#<p>Quyền truy cập node là một khía cạnh khác, không phải định nghĩa của "root-like".</p>
	=[moodle]Các Pod chạy với quyền cao (root) hoặc các khả năng mạnh mẽ.
	~[moodle]Các Pod được quản lý bởi một Operator đặc biệt.#<p>Việc quản lý bởi Operator không định nghĩa quyền của Pod.</p>
	####<p><strong>Giải thích</strong>\: "Root-like Pods" là các Pod chạy với quyền root hoặc các khả năng Linux mạnh mẽ, có thể gây ra rủi ro bảo mật nghiêm trọng nếu bị xâm nhập.</p>
}

// question: 13.19 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>"Security outskirts" của một Pod bao gồm những gì?</p>{
	~[moodle]Mạng, lưu trữ và DNS.#<p>Đây là các thành phần chức năng, không phải riêng khía cạnh bảo mật.</p>
	~[moodle]API server, scheduler và controller manager.#<p>Đây là các thành phần của control plane.</p>
	~[moodle]Các quy tắc tường lửa và các thiết bị vật lý của node.#<p>Đây là các khía cạnh vật lý và cấu hình mạng cấp độ thấp hơn.</p>
	=[moodle]Các thiết lập bảo mật không thuộc "security context" trực tiếp.
	####<p><strong>Giải thích</strong>\: "Security outskirts" đề cập đến các khía cạnh bảo mật bên ngoài "security context" trực tiếp của Pod, bao gồm các chính sách mạng, các quyền RBAC và các cấu hình khác có thể ảnh hưởng đến bảo mật của Pod.</p>
}

// question: 13.20 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Khi một certificate's user không khớp với process ID user, điều gì có thể gây ra sự cố?</p>{
	~[moodle]Lỗi cấu hình mạng.#<p>Không liên quan trực tiếp đến lỗi mạng.</p>
	=[moodle]Vấn đề với chứng chỉ SSL/TLS được mount dưới dạng Secret.
	~[moodle]Thiếu tài nguyên CPU cho Pod.#<p>Không liên quan đến tài nguyên CPU.</p>
	~[moodle]Sự cố với DNS lookup.#<p>Không liên quan đến DNS lookup.</p>
	####<p><strong>Giải thích</strong>\: Một hạn chế hiện tại trong Kubernetes là khi một Secret được mount không khớp với fsGroup, có thể gây ra sự cố với code kiểm tra người dùng của chứng chỉ.</p>
}

// question: 13.21 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>"Container screening" là gì trong bảo mật container?</p>{
	~[moodle]Quá trình chọn image container phù hợp nhất.#<p>Là một phần của việc sử dụng container, nhưng không phải "screening".</p>
	=[moodle]Kiểm tra các image container để phát hiện lỗ hổng.
	~[moodle]Lọc lưu lượng mạng đến và đi của container.#<p>Đây là chức năng của Network Policies.</p>
	~[moodle]Phân loại container theo mức độ bảo mật.#<p>Đây là kết quả của việc đánh giá, không phải "screening".</p>
	####<p><strong>Giải thích</strong>\: "Container screening" là việc quét các image container để tìm kiếm các lỗ hổng đã biết.</p>
}

// question: 13.22 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Để chạy một chương trình trong một không gian tệp tin giả lập (fake filesystem) mà không ảnh hưởng đến hệ thống tệp tin host, lệnh Linux nào thường được sử dụng?</p>{
	~[moodle]mount --bind.#<p>mount --bind dùng để gắn kết một thư mục vào một vị trí khác.</p>
	~[moodle]unshare.#<p>unshare tạo ra các namespace mới (PID, mạng, v.v.).</p>
	=[moodle]chroot.
	~[moodle]cgroup.#<p>cgroup dùng để quản lý tài nguyên, không phải hệ thống tệp tin.</p>
	####<p><strong>Giải thích</strong>\: chroot được sử dụng để thay đổi thư mục gốc của tiến trình đang chạy thành một thư mục khác, tạo ra một không gian tệp tin giả lập.</p>
}

// question: 13.23 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Khi sử dụng chroot để tạo môi trường container thủ công, bạn cần sao chép những thành phần nào vào không gian giả lập để chạy các lệnh cơ bản như ls hoặc bash?</p>{
	~[moodle]Chỉ các tệp tin cấu hình mạng.#<p>chroot không liên quan trực tiếp đến tệp tin cấu hình mạng.</p>
	=[moodle]Các thư viện dùng chung và các tệp thực thi của lệnh đó.
	~[moodle]Toàn bộ nhân Linux.#<p>chroot không yêu cầu toàn bộ nhân Linux, mà chỉ sử dụng nhân host.</p>
	~[moodle]Chỉ các tệp tin nhật ký của hệ thống.#<p>chroot không yêu cầu tệp tin nhật ký.</p>
	####<p><strong>Giải thích</strong>\: Để các lệnh như ls hoặc bash hoạt động trong môi trường chroot, bạn cần sao chép các tệp thực thi của chúng cùng với các thư viện dùng chung mà chúng phụ thuộc vào.</p>
}

// question: 13.24 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Lệnh unshare trong Linux chủ yếu được sử dụng cho mục đích gì khi xây dựng container?</p>{
	~[moodle]Điều chỉnh mức sử dụng CPU của một tiến trình.#<p>cgroups được dùng để điều chỉnh CPU.</p>
	=[moodle]Tạo các namespace mới để cách ly tài nguyên.
	~[moodle]Gắn kết các volume lưu trữ vào một tiến trình.#<p>mount được dùng để gắn kết volume.</p>
	~[moodle]Kiểm tra tình trạng sức khỏe của một tiến trình.#<p>check process health là chức năng khác.</p>
	####<p><strong>Giải thích</strong>\: unshare được sử dụng để tạo các namespace mới (như PID, mạng, IPC, cgroup, mount, user) cho một tiến trình, giúp cách ly tiến trình đó khỏi các tài nguyên khác trên hệ thống.</p>
}

// question: 13.25 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Việc thiếu thiết bị eth0 trong một tiến trình được chroot mà không có network namespace cho thấy điều gì?</p>{
	~[moodle]Tiến trình đó có thể giao tiếp với các Pod khác.#<p>Nếu không có eth0 thì không thể giao tiếp mạng.</p>
	=[moodle]Tiến trình đó không thể truy cập mạng.
	~[moodle]Tiến trình đó chạy với quyền root.#<p>chroot không tự động cấp quyền root.</p>
	~[moodle]Tiến trình đó đang sử dụng loopback interface.#<p>loopback interface (lo) chỉ cho phép giao tiếp nội bộ.</p>
	####<p><strong>Giải thích</strong>\: Nếu một tiến trình chỉ chạy trong môi trường chroot mà không có network namespace riêng, nó sẽ không có thiết bị eth0 và do đó không thể truy cập mạng bên ngoài.</p>
}

// question: 13.26 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>"Capabilities" trong Linux là gì và được sử dụng như thế nào trong bảo mật Pod?</p>{
	~[moodle]Là các tệp thực thi của hệ thống được phép chạy trong Pod.#<p>Không phải là các tệp thực thi.</p>
	=[moodle]Là các nhóm đặc quyền Linux có thể được cấp hoặc thu hồi từ một tiến trình.
	~[moodle]Là các thông số cấu hình tài nguyên (CPU, memory) cho Pod.#<p>Cấu hình tài nguyên là chức năng của cgroups.</p>
	~[moodle]Là danh sách các cổng mạng mà Pod được phép sử dụng.#<p>Các cổng mạng là chức năng của network policies.</p>
	####<p><strong>Giải thích</strong>\: "Capabilities" là các nhóm đặc quyền có thể được cấp cho một tiến trình, cho phép nó thực hiện các hành động cụ thể mà không cần có toàn bộ quyền root, giúp tinh chỉnh bảo mật.</p>
}

// question: 13.27 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Khi một Pod bị chấm dứt vì vượt quá giới hạn tài nguyên, Kubernetes sẽ trả về trạng thái nào?</p>{
	~[moodle]Pending.#<p>Pending là trạng thái chờ tài nguyên hoặc lên lịch.</p>
	~[moodle]Error.#<p>Error là một trạng thái chung chung.</p>
	=[moodle]OOMKilled (nếu do bộ nhớ) hoặc một mã thoát.
	~[moodle]Unknown.#<p>Unknown là trạng thái khi kubelet không thể liên lạc với API server.</p>
	####<p><strong>Giải thích</strong>\: Kubernetes sẽ báo cáo mã thoát và trạng thái OOMKilled (Out Of Memory Killed) trong các trường hợp tiến trình bị chấm dứt do vượt quá giới hạn bộ nhớ.</p>
}

// question: 13.28 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>"QoS classes" (Quality of Service classes) trong Kubernetes được tạo ra dựa trên yếu tố nào trong định nghĩa Pod?</p>{
	~[moodle]Chỉ dựa vào metadata.labels.#<p>metadata.labels dùng để chọn Pod.</p>
	=[moodle]Dựa vào việc thiết lập resources.requests và limits.
	~[moodle]Chỉ dựa vào spec.containers.image.#<p>image là image container.</p>
	~[moodle]Dựa vào số lượng replica của Pod.#<p>replicas là số lượng bản sao.</p>
	####<p><strong>Giải thích</strong>\: Các "QoS classes" như Burstable, Guaranteed, và BestEffort được tạo ra tùy thuộc vào cách bạn định nghĩa resources.requests và limits cho Pod.</p>
}

// question: 13.29 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Điều gì làm cho một Pod được xếp vào loại Burstable QoS class?</p>{
	~[moodle]Không có requests hoặc limits nào được định nghĩa.#<p>Đó là loại BestEffort.</p>
	~[moodle]Có requests và limits được định nghĩa giống nhau cho CPU và memory.#<p>Guaranteed class.</p>
	=[moodle]Có requests được định nghĩa nhưng limits không được định nghĩa hoặc cao hơn.
	~[moodle]Chỉ có limits được định nghĩa mà không có requests.#<p>BestEffort nếu không có cả requests và limits.</p>
	####<p><strong>Giải thích</strong>\: Một Pod thuộc loại Burstable QoS class nếu nó có định nghĩa requests nhưng không có limits hoặc limits cao hơn requests cho CPU và/hoặc memory.</p>
}

// question: 13.30 name: Chapter 13: Container and Pod security
::Chapter 13\: Container and Pod security::[html]<p>Mục đích chính của "init containers" là gì trong một Pod?</p>{
	~[moodle]Chạy các dịch vụ chính của ứng dụng.#<p>Các container chính mới chạy dịch vụ ứng dụng.</p>
	=[moodle]Thực hiện các thiết lập cần thiết trước khi container chính khởi động.
	~[moodle]Thu thập các log từ các container khác.#<p>Thu thập log là chức năng của các logging agent.</p>
	~[moodle]Cung cấp lưu trữ tạm thời cho Pod.#<p>emptyDir hoặc các loại volume khác cung cấp lưu trữ tạm thời.</p>
	####<p><strong>Giải thích</strong>\: "Init containers" được sử dụng để thực hiện các công việc thiết lập hoặc khởi động cần thiết mà phải hoàn thành trước khi các container ứng dụng chính của Pod khởi động.</p>
}

// Chapter 14: Nodes and Kubernetes security
// question: 14 name: Switch category to $module$/top/Chapter 14: Nodes and Kubernetes security
$CATEGORY: $module$/top/Chapter 14: Nodes and Kubernetes security

// question: 14.1 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Tất cả các giao tiếp bên ngoài trong Kubernetes thường diễn ra qua giao thức nào để đảm bảo bảo mật?</p>{
	~[moodle]HTTP.#<p>HTTP không an toàn nếu không có TLS (HTTPS).</p>
	~[moodle]TCP/IP.#<p>TCP/IP là giao thức truyền tải, TLS là lớp bảo mật trên đó.</p>
	=[moodle]TLS (Transport Layer Security).
	~[moodle]UDP.#<p>UDP là giao thức truyền tải, TLS là lớp bảo mật trên đó.</p>
	####<p><strong>Giải thích</strong>\: Tất cả các giao tiếp bên ngoài trong Kubernetes nói chung đều diễn ra qua TLS (Transport Layer Security), mặc dù điều này có thể được cấu hình.</p>
}

// question: 14.2 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>"Cipher suites" trong TLS là gì và tại sao chúng quan trọng cho API server?</p>{
	~[moodle]Là tập hợp các địa chỉ IP cho phép truy cập API server.#<p>Không phải là danh sách địa chỉ IP.</p>
	=[moodle]Là các bộ thuật toán được sử dụng để bảo mật giao tiếp TLS.
	~[moodle]Là danh sách các certificate được cấp bởi API server.#<p>Không phải là các certificate được cấp.</p>
	~[moodle]Là các quy tắc cho phép các Pod giao tiếp với API server.#<p>Không phải là quy tắc giao tiếp Pod.</p>
	####<p><strong>Giải thích</strong>\: "Cipher suites" là các tập hợp thuật toán cho phép TLS diễn ra an toàn. Việc định nghĩa cipher suite cho API server đảm bảo nó chỉ kết nối với các dịch vụ khác bằng bộ thuật toán đã chọn.</p>
}

// question: 14.3 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Khi nói về các node Kubernetes, "immutable operating systems" có lợi ích gì về bảo mật?</p>{
	~[moodle]Giảm chi phí vận hành node.#<p>Giảm chi phí vận hành không phải là lợi ích chính.</p>
	=[moodle]Tăng tính nhất quán và giảm "drift" cấu hình.
	~[moodle]Cho phép cài đặt phần mềm tùy chỉnh dễ dàng hơn.#<p>Ngược lại, việc cài đặt phần mềm tùy chỉnh có thể khó khăn hơn trên OS bất biến.</p>
	~[moodle]Tăng tốc độ khởi động của node.#<p>Không trực tiếp ảnh hưởng đến tốc độ khởi động.</p>
	####<p><strong>Giải thích</strong>\: Chạy Kubernetes trên các hệ điều hành bất biến (immutable OS) có nghĩa là hệ điều hành cơ bản chỉ cập nhật khi toàn bộ hệ điều hành được cập nhật, giúp duy trì tính nhất quán môi trường và tránh "drift" cấu hình.</p>
}

// question: 14.4 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Tại sao việc xây dựng các image tùy chỉnh cho Windows worker node lại quan trọng?</p>{
	~[moodle]Để sử dụng Docker Engine làm runtime container.#<p>Windows worker nodes vẫn có thể sử dụng các runtime container khác.</p>
	=[moodle]Vì hệ điều hành Windows không thể phân phối lại.
	~[moodle]Để giảm số lượng CPU cần thiết cho node.#<p>Không liên quan đến số lượng CPU.</p>
	~[moodle]Để đảm bảo tính tương thích với các ứng dụng Linux.#<p>Không liên quan đến ứng dụng Linux.</p>
	####<p><strong>Giải thích</strong>\: Hệ điều hành Windows không thể phân phối lại, vì vậy người dùng cuối phải xây dựng image Windows kubelet nếu họ muốn sử dụng mô hình triển khai bất biến.</p>
}

// question: 14.5 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Đơn vị cơ bản mà Kubernetes sử dụng để đo CPU là gì?</p>{
	~[moodle]MHz (Megahertz).#<p>MHz là cách đo khác, không phải đơn vị cơ bản trong cấu hình Kubernetes.</p>
	=[moodle]1, tương đương một hyperthread hoặc một core/vCPU.
	~[moodle]% (phần trăm).#<p>Phần trăm là cách đo khác, không phải đơn vị cơ bản trong cấu hình Kubernetes.</p>
	~[moodle]Bytes.#<p>Bytes là đơn vị đo bộ nhớ.</p>
	####<p><strong>Giải thích</strong>\: Đơn vị cơ bản mà Kubernetes sử dụng để đo CPU là 1, tương đương với một hyperthread trên bare metal hoặc một core/vCPU trong đám mây.</p>
}

// question: 14.6 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Các suffix như E, P, T, G, M, hoặc K được sử dụng để đo lường tài nguyên nào trong Kubernetes?</p>{
	~[moodle]CPU.#<p>CPU được đo bằng đơn vị 1 hoặc m.</p>
	=[moodle]Bộ nhớ (Memory).
	~[moodle]Lưu trữ Ephemeral (Ephemeral Storage).#<p>Ephemeral storage cũng được đo bằng các đơn vị lưu trữ nhưng nguồn tập trung vào memory.</p>
	~[moodle]Network bandwidth.#<p>Network bandwidth không được cấu hình trực tiếp với các suffix này.</p>
	####<p><strong>Giải thích</strong>\: Bộ nhớ được đo bằng byte, dưới dạng số nguyên và số thập phân bằng các suffix như E, P, T, G, M, K hoặc Ei, Pi, Ti, Gi, Mi, Ki.</p>
}

// question: 14.7 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>"Ephemeral storage limits" trong Pod áp dụng cho những thành phần lưu trữ nào?</p>{
	~[moodle]PersistentVolumes và Secret.#<p>PersistentVolumes và Secret là các loại lưu trữ khác.</p>
	=[moodle]Các volume emptyDir (trừ tmpfs), nhật ký cấp node, và các lớp container có thể ghi.
	~[moodle]Chỉ các volume được gắn kết từ hệ thống tệp tin host.#<p>hostPath là một loại volume khác.</p>
	~[moodle]Chỉ các image container đã kéo về.#<p>Image container không phải là ephemeral storage trực tiếp.</p>
	####<p><strong>Giải thích</strong>\: "Ephemeral storage limits" áp dụng cho ba thành phần lưu trữ: các volume emptyDir (trừ tmpfs), các thư mục chứa nhật ký cấp node, và các lớp container có thể ghi.</p>
}

// question: 14.8 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Điều gì xảy ra khi một Pod vượt quá "ephemeral storage limit"?</p>{
	~[moodle]Pod sẽ được tự động di chuyển sang node khác.#<p>Evict khác với di chuyển.</p>
	=[moodle]Kubelet sẽ trục xuất (evict) Pod đó.
	~[moodle]Node sẽ bị sập.#<p>Eviction được thiết kế để ngăn node bị sập.</p>
	~[moodle]Lưu lượng mạng của Pod sẽ bị giảm.#<p>Ephemeral storage không liên quan trực tiếp đến lưu lượng mạng.</p>
	####<p><strong>Giải thích</strong>\: Khi một giới hạn (ephemeral storage) bị vượt quá, kubelet sẽ trục xuất (evict) Pod.</p>
}

// question: 14.9 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Tại sao việc cho phép một Pod tham gia mạng host (hostNetwork: true) lại làm tăng "blast radius" khi bị tấn công?</p>{
	~[moodle]Pod không thể giao tiếp với các Pod khác.#<p>hostNetwork giúp giao tiếp dễ dàng hơn, không phải cản trở.</p>
	=[moodle]Pod có quyền truy cập dễ dàng hơn vào node và các tài nguyên host.
	~[moodle]Pod tiêu thụ nhiều tài nguyên CPU và bộ nhớ hơn.#<p>hostNetwork không trực tiếp làm tăng tiêu thụ CPU/memory.</p>
	~[moodle]Pod không thể được chia tỷ lệ tự động.#<p>hostNetwork không ảnh hưởng đến khả năng chia tỷ lệ tự động.</p>
	####<p><strong>Giải thích</strong>\: Việc cho một Pod tham gia mạng host cho phép Pod truy cập dễ dàng hơn vào node, và do đó, làm tăng "blast radius" khi bị tấn công.</p>
}

// question: 14.10 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Khi nào thì việc chạy một Pod trên mạng host (hostNetwork: true) thường được chấp nhận?</p>{
	~[moodle]Đối với tất cả các ứng dụng người dùng cuối.#<p>Không nên cho ứng dụng người dùng cuối chạy trên mạng host vì lý do bảo mật.</p>
	=[moodle]Khi Pod thực hiện các tác vụ quản trị như ghi log hoặc mạng (nhà cung cấp CNI).
	~[moodle]Để tiết kiệm địa chỉ IP.#<p>hostNetwork không phải là cách tiết kiệm địa chỉ IP.</p>
	~[moodle]Khi Pod cần truy cập trực tiếp vào internet.#<p>hostNetwork cung cấp quyền truy cập mạng rộng hơn, nhưng không phải là lý do duy nhất để sử dụng nó.</p>
	####<p><strong>Giải thích</strong>\: Bạn thường sẽ thấy các Pod chạy trên mạng host nếu Pod đang thực hiện các tác vụ quản trị, chẳng hạn như ghi nhật ký hoặc mạng (một nhà cung cấp CNI).</p>
}

// question: 14.11 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>"Verbs" trong định nghĩa Role và ClusterRole của RBAC (Role-Based Access Control) là gì?</p>{
	~[moodle]Các tên của tài nguyên API mà Role có thể truy cập.#<p>Resources mới là tên tài nguyên.</p>
	=[moodle]Các hành động API (ví dụ: get, create, update) mà Role được phép thực hiện.
	~[moodle]Các điều kiện cho phép Pod được lên lịch.#<p>Scheduler mới xử lý điều kiện lên lịch.</p>
	~[moodle]Các địa chỉ IP mà Role được phép kết nối.#<p>Verbs không liên quan đến địa chỉ IP.</p>
	####<p><strong>Giải thích</strong>\: "Verbs" bao gồm các động từ API và HTTP, mô tả các hành động mà Role được phép thực hiện trên các tài nguyên (ví dụ: get, list, create, update, patch, delete).</p>
}

// question: 14.12 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Động từ API deletecollection trong RBAC có chức năng gì?</p>{
	~[moodle]Xóa một tài nguyên API cụ thể.#<p>Delete là để xóa một tài nguyên cụ thể.</p>
	=[moodle]Xóa một nhóm tài nguyên API cùng một lúc.
	~[moodle]Xóa một namespace và tất cả các tài nguyên bên trong.#<p>Delete namespace là một hoạt động cấp cao hơn.</p>
	~[moodle]Xóa một Pod và tất cả các container của nó.#<p>Delete Pod là một hoạt động cấp Pod.</p>
	####<p><strong>Giải thích</strong>\: deletecollection là một động từ API cho phép xóa một tập hợp các tài nguyên cùng lúc, không phải chỉ một tài nguyên duy nhất.</p>
}

// question: 14.13 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>"Subjects" trong RBAC định nghĩa những đối tượng nào có thể được cấp quyền?</p>{
	~[moodle]Chỉ các Pod và Deployments.#<p>Các Pod và Deployments không phải là subjects trong RBAC.</p>
	~[moodle]Chỉ các ServiceAccount.#<p>ServiceAccount là một phần, nhưng không phải toàn bộ.</p>
	=[moodle]ServiceAccount, User, và Group.
	~[moodle]Chỉ các ClusterRole.#<p>ClusterRole là các quy tắc, không phải subjects.</p>
	####<p><strong>Giải thích</strong>\: "Subjects" trong RBAC định nghĩa các đối tượng có thể được cấp quyền, bao gồm ServiceAccount, User và Group.</p>
}

// question: 14.14 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Khi một ServiceAccount được sử dụng trong một Pod, nó được dùng để làm gì?</p>{
	~[moodle]Để định nghĩa các giới hạn tài nguyên của Pod.#<p>ResourceLimits mới là giới hạn tài nguyên.</p>
	=[moodle]Để cung cấp danh tính cho Pod khi truy cập Kubernetes API server.
	~[moodle]Để chỉ định network policy cho Pod.#<p>NetworkPolicy mới là chính sách mạng.</p>
	~[moodle]Để quản lý các PersistentVolumeClaim của Pod.#<p>PVC và PV mới quản lý PersistentVolumeClaim.</p>
	####<p><strong>Giải thích</strong>\: ServiceAccount cung cấp danh tính cho Pod để truy cập vào Kubernetes API server, trừ khi bị vô hiệu hóa.</p>
}

// question: 14.15 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Tại sao không nên sử dụng "compute engine default service account" cho các cluster Kubernetes trong Google Cloud (GCP)?</p>{
	~[moodle]Nó có quá ít quyền, gây khó khăn cho hoạt động của cluster.#<p>Ngược lại, nó có quyền quá cao.</p>
	=[moodle]Nó có quyền editor, cho phép sửa đổi nhiều tài nguyên dự án, tăng rủi ro bảo mật.
	~[moodle]Nó làm chậm quá trình khởi tạo cluster.#<p>Không có mối liên hệ trực tiếp với tốc độ khởi tạo.</p>
	~[moodle]Nó không tương thích với RBAC của Kubernetes.#<p>Nó có thể tương thích, nhưng vấn đề là quyền hạn.</p>
	####<p><strong>Giải thích</strong>\: "Editor" trong Google Cloud cho phép một tài khoản (trong trường hợp này, một node trong cluster, có thể dịch sang bất kỳ Pod nào) chỉnh sửa bất kỳ tài nguyên nào trong dự án, gây rủi ro bảo mật nghiêm trọng.</p>
}

// question: 14.16 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Các "NetworkPolicies" trong Kubernetes có thể kiểm soát loại lưu lượng mạng nào?</p>{
	~[moodle]Chỉ lưu lượng mạng ingress (đến).#<p>NetworkPolicies kiểm soát cả ingress và egress.</p>
	~[moodle]Chỉ lưu lượng mạng egress (đi).#<p>NetworkPolicies kiểm soát cả ingress và egress.</p>
	=[moodle]Cả lưu lượng ingress và egress.
	~[moodle]Chỉ lưu lượng mạng giữa các namespace khác nhau.#<p>NetworkPolicies không giới hạn ở lưu lượng giữa các namespace.</p>
	####<p><strong>Giải thích</strong>\: "NetworkPolicies" kiểm soát cả lưu lượng mạng ingress (đến) và egress (đi) cho các Pod.</p>
}

// question: 14.17 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Các "NetworkPolicies" có thể định nghĩa lưu lượng mạng dựa trên yếu tố nào?</p>{
	~[moodle]Chỉ dựa trên địa chỉ IP của Pod.#<p>Không chỉ giới hạn ở địa chỉ IP của Pod.</p>
	=[moodle]Dựa trên dải CIDR, một namespace cụ thể, hoặc một Pod/tập hợp Pods phù hợp.
	~[moodle]Chỉ dựa trên tên dịch vụ của Pod.#<p>Service name không phải là yếu tố chính.</p>
	~[moodle]Chỉ dựa trên số lượng CPU được yêu cầu.#<p>CPU không liên quan đến network policies.</p>
	####<p><strong>Giải thích</strong>\: "NetworkPolicies" có thể định nghĩa lưu lượng mạng được xác định bởi một dải CIDR, một namespace cụ thể, hoặc một Pod/tập hợp Pods phù hợp thông qua các label selector.</p>
}

// question: 14.18 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>"Open Policy Agent (OPA)" được sử dụng để làm gì trong Kubernetes?</p>{
	~[moodle]Tự động chia tỷ lệ Pod dựa trên tải.#<p>HPA (Horizontal Pod Autoscaler) thực hiện chia tỷ lệ Pod.</p>
	=[moodle]Viết và thực thi các chính sách bảo mật tùy chỉnh cho cluster.
	~[moodle]Giám sát hiệu suất của các node Kubernetes.#<p>Prometheus và cAdvisor là công cụ giám sát hiệu suất.</p>
	~[moodle]Quản lý các PersistentVolumeClaim.#<p>CSI và PV/PVC quản lý PersistentVolumeClaim.</p>
	####<p><strong>Giải thích</strong>\: OPA cho phép người dùng viết các chính sách bảo mật và thực thi chúng trên một cluster Kubernetes, thông qua các query để đánh giá chính sách và dữ liệu.</p>
}

// question: 14.19 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Hai thành phần chính mà OPA duy trì là gì?</p>{
	~[moodle]OPA Agent và OPA Controller.#<p>Đây không phải là các thành phần chính được nhắc đến trong nguồn.</p>
	=[moodle]OPA Admission Controller và OPA Gatekeeper.
	~[moodle]OPA Policy Server và OPA Client.#<p>Đây không phải là các thành phần chính được nhắc đến trong nguồn.</p>
	~[moodle]OPA Runtime và OPA Compiler.#<p>Đây không phải là các thành phần chính được nhắc đến trong nguồn.</p>
	####<p><strong>Giải thích</strong>\: OPA duy trì hai thành phần khác nhau: OPA Admission Controller và OPA Gatekeeper. Gatekeeper không sử dụng sidecar, sử dụng CRDs, có thể mở rộng và thực hiện chức năng audit.</p>
}

// question: 14.20 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>"OPA Gatekeeper" có những đặc điểm nào?</p>{
	~[moodle]Nó sử dụng một sidecar để thực thi chính sách.#<p>Gatekeeper không sử dụng sidecar.</p>
	=[moodle]Nó sử dụng CRDs (Custom Resource Definitions), có thể mở rộng và thực hiện chức năng audit.
	~[moodle]Nó chỉ hỗ trợ các chính sách mạng.#<p>Gatekeeper hỗ trợ các chính sách rộng hơn, không chỉ mạng.</p>
	~[moodle]Nó là một công cụ độc lập, không tích hợp với Kubernetes API.#<p>Gatekeeper tích hợp chặt chẽ với Kubernetes API thông qua CRDs.</p>
	####<p><strong>Giải thích</strong>\: "Gatekeeper" không sử dụng sidecar, sử dụng CRDs (custom resource definitions), có thể mở rộng và thực hiện chức năng audit.</p>
}

// question: 14.21 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>"Multi-tenancy" trong Kubernetes được phân loại dựa trên yếu tố nào?</p>{
	~[moodle]Số lượng namespace trong cluster.#<p>Namespace là một công cụ tổ chức, không phải yếu tố phân loại chính.</p>
	=[moodle]Mức độ tin cậy mà các tenant (người thuê) có với nhau.
	~[moodle]Loại ứng dụng mà các tenant triển khai.#<p>Application type không phải là yếu tố phân loại chính.</p>
	~[moodle]Kiến trúc mạng của cluster.#<p>Network architecture là một khía cạnh kỹ thuật, không phải yếu tố phân loại "multi-tenancy" chính.</p>
	####<p><strong>Giải thích</strong>\: Để phân loại "multi-tenancy", bạn cần xem xét mức độ tin cậy mà các tenant có với nhau, sau đó phát triển mô hình đó.</p>
}

// question: 14.22 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Mô hình "multi-tenancy" "Zero trust" hoặc "Low trust" giữa các tenant yêu cầu giải pháp gì trong Kubernetes?</p>{
	~[moodle]Triển khai tất cả các ứng dụng trong một namespace duy nhất.#<p>Một namespace sẽ không cung cấp cách ly cần thiết.</p>
	=[moodle]Sử dụng các cluster riêng biệt cho mỗi client/tenant.
	~[moodle]Tăng cường giới hạn tài nguyên cho các Pod.#<p>Giới hạn tài nguyên không đủ để đảm bảo "zero trust".</p>
	~[moodle]Sử dụng một LoadBalancer để cách ly mạng.#<p>LoadBalancer không cung cấp cách ly cấp cluster.</p>
	####<p><strong>Giải thích</strong>\: Khi có "zero trust" hoặc "low trust" giữa các tenant, bạn cần sử dụng các cluster riêng biệt cho mỗi client. Một số công ty chạy hàng trăm cluster để mỗi nhóm ứng dụng nhỏ có cluster riêng.</p>
}

// question: 14.23 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Kubernetes được thiết kế ban đầu với khái niệm "hard multi-tenancy" (nhiều khách hàng được cách ly trong cùng một cluster) hay không?</p>{
	~[moodle]Có, nó được xây dựng với mục tiêu đó ngay từ đầu.#<p>Jessie Frazelle đã chỉ ra rằng Kubernetes không được thiết kế ban đầu cho "hard multi-tenancy".</p>
	=[moodle]Không, API của Kubernetes không được xây dựng với khái niệm có nhiều khách hàng được cách ly.
	~[moodle]Chỉ với các phiên bản Kubernetes mới nhất.#<p>Các công cụ và phiên bản mới hơn đang cố gắng giải quyết vấn đề này, nhưng không phải là thiết kế ban đầu.</p>
	~[moodle]Chỉ khi sử dụng OPA Gatekeeper.#<p>Các công cụ và phiên bản mới hơn đang cố gắng giải quyết vấn đề này, nhưng không phải là thiết kế ban đầu.</p>
	####<p><strong>Giải thích</strong>\: API của Kubernetes không được xây dựng với khái niệm có nhiều khách hàng được cách ly trong cùng một cluster. Docker Engine và các container runtime khác cũng có vấn đề với việc chạy các workload độc hại hoặc không đáng tin cậy.</p>
}

// question: 14.24 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Các ứng dụng containerized có khả năng làm gì để quản lý cấu hình và trạng thái của chúng?</p>{
	~[moodle]Luôn yêu cầu sự can thiệp thủ công để cập nhật.#<p>Operator và kapp-controller cho phép quản lý tự động.</p>
	=[moodle]Có thể sử dụng Kubernetes API server để lưu trữ dữ liệu cấu hình.
	~[moodle]Phải lưu trữ tất cả cấu hình trong Dockerfile.#<p>Dockerfile không lưu trữ cấu hình runtime.</p>
	~[moodle]Không thể tương tác với Kubernetes API.#<p>Operator là một ví dụ về tương tác với Kubernetes API.</p>
	####<p><strong>Giải thích</strong>\: Các ứng dụng native của Kubernetes thường tạo ra nhiều CRD (Custom Resource Definitions) cho các ứng dụng của chúng. CRD cho phép bất kỳ ứng dụng nào sử dụng Kubernetes API server để lưu trữ dữ liệu cấu hình.</p>
}

// question: 14.25 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Điều gì có thể xảy ra nếu một Pod bị xâm nhập khi nó có quyền "editor" trên Google Cloud?</p>{
	~[moodle]Chỉ có thể sửa đổi các Pod trong cùng một namespace.#<p>Editor có quyền rộng hơn nhiều.</p>
	=[moodle]Có thể xóa toàn bộ fleet cơ sở dữ liệu hoặc các tài nguyên đám mây khác.
	~[moodle]Chỉ có thể đọc các tệp cấu hình của hệ thống.#<p>Editor có quyền ghi.</p>
	~[moodle]Có thể thay đổi giới hạn tài nguyên của các Pod khác.#<p>Editor có thể làm được nhiều hơn là chỉ thay đổi giới hạn tài nguyên.</p>
	####<p><strong>Giải thích</strong>\: Nếu một Pod có quyền "editor" trên Google Cloud, nó có thể xóa toàn bộ fleet cơ sở dữ liệu, load balancer TCP, hoặc các mục DNS đám mây bằng cách xâm nhập một Pod cụ thể trong cluster.</p>
}

// question: 14.26 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Mục đích của kubeletCgroups trong cấu hình kubelet là gì?</p>{
	~[moodle]Định nghĩa các giao diện mạng cho Pod.#<p>CNI mới định nghĩa giao diện mạng.</p>
	=[moodle]Cấu hình root và driver cho cgroup của Pod.
	~[moodle]Quản lý việc kéo image từ registry.#<p>ImageService mới quản lý việc kéo image.</p>
	~[moodle]Xác định chu kỳ kiểm tra sức khỏe của Pod.#<p>Health check được định nghĩa trong liveness/readiness probes.</p>
	####<p><strong>Giải thích</strong>\: kubeletCgroups trong cấu hình kubelet được sử dụng để định nghĩa root và driver cho cgroup của Pod.</p>
}

// question: 14.27 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>EvictionHard và EvictionSoft trong cấu hình kubelet có tác dụng gì?</p>{
	~[moodle]Định nghĩa các ngưỡng tài nguyên cho phép Pod hoạt động.#<p>Requests và limits là ngưỡng tài nguyên.</p>
	=[moodle]Xác định khi nào Pod nên bị xóa dựa trên tải hệ thống hoặc thời gian chờ.
	~[moodle]Đặt mức độ ưu tiên cho việc lên lịch Pod.#<p>QoS classes mới là ưu tiên lên lịch.</p>
	~[moodle]Cấu hình thời gian phục hồi của Pod sau khi bị lỗi.#<p>restartPolicy mới cấu hình thời gian phục hồi.</p>
	####<p><strong>Giải thích</strong>\: EvictionHard và EvictionSoft là các cấu trúc trong types.go của kubelet để xác định khi nào Pod nên bị xóa (evicted), dựa trên tải hệ thống (hard limits) hoặc thời gian chờ trước khi trục xuất một Pod "greedy" (soft limits).</p>
}

// question: 14.28 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Trong cấu hình kubeletFlags, trường hợp nào một trường cấu hình nên nằm trong kubeletFlags thay vì kubeletConfiguration?</p>{
	~[moodle]Giá trị của nó có thể thay đổi an toàn trong thời gian hoạt động của node.#<p>kubeletConfiguration mới chứa các giá trị có thể thay đổi.</p>
	=[moodle]Giá trị của nó không thể thay đổi an toàn trong vòng đời của node hoặc không thể chia sẻ giữa các node.
	~[moodle]Nó định nghĩa các thông số cho một Pod cụ thể.#<p>PodSpec định nghĩa thông số Pod.</p>
	~[moodle]Nó kiểm soát hành vi mặc định của CRI.#<p>containerd/CRI-O định nghĩa hành vi CRI.</p>
	####<p><strong>Giải thích</strong>\: Một trường cấu hình nên nằm trong kubeletFlags thay vì kubeletConfiguration nếu giá trị của nó không bao giờ hoặc không thể thay đổi an toàn trong vòng đời của node, hoặc giá trị của nó không thể chia sẻ an toàn giữa các node cùng lúc.</p>
}

// question: 14.29 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Điều gì làm cho etcd_disk_wal_fsync_duration_seconds_bucket trở thành một metric quan trọng để giám sát etcd?</p>{
	~[moodle]Nó đo lường thời gian trung bình để đọc dữ liệu từ etcd.#<p>fsync là về ghi, không phải đọc.</p>
	=[moodle]Nó theo dõi thời gian fsync (ghi đĩa) bị chặn, cho biết hiệu suất ghi của etcd.
	~[moodle]Nó đếm số lượng yêu cầu watch đang hoạt động trên etcd.#<p>etcd_server_has_leader liên quan đến watch.</p>
	~[moodle]Nó theo dõi số lượng lỗi xảy ra trong quá trình đồng thuận etcd.#<p>etcd_server_leader_changes_seen_total liên quan đến lỗi đồng thuận.</p>
	####<p><strong>Giải thích</strong>\: Metric etcd_disk_wal_fsync_duration_seconds_bucket (một histogram) cho biết thời gian các thao tác fsync bị chặn trên đĩa, là một chỉ số quan trọng về hiệu suất ghi của etcd. Nếu các ghi này kéo dài gần 1 giây, hiệu suất etcd đang gặp rủi ro.</p>
}

// question: 14.30 name: Chapter 14: Nodes and Kubernetes security
::Chapter 14\: Nodes and Kubernetes security::[html]<p>Khi một cluster Kubernetes chạy trên "nested virtualization" (ví dụ: VM trong VM), điều gì có thể xảy ra với etcd?</p>{
	~[moodle]Hiệu suất etcd sẽ tăng đáng kể.#<p>Nested virtualization làm giảm hiệu suất.</p>
	=[moodle]etcd có thể trở nên không đáng tin cậy do độ trễ ghi đĩa cao.
	~[moodle]etcd sẽ tự động chuyển sang etcd v2 để tăng độ ổn định.#<p>etcd v2 không còn được hỗ trợ.</p>
	~[moodle]etcd sẽ yêu cầu ít bộ nhớ hơn để hoạt động.#<p>Nested virtualization không làm giảm yêu cầu bộ nhớ.</p>
	####<p><strong>Giải thích</strong>\: "Nested virtualization" tạo ra độ trễ hiệu suất lớn và không được khuyến nghị cho production, vì nó làm tăng độ trễ cho các thao tác ghi đĩa, khiến etcd trở nên cực kỳ không đáng tin cậy.</p>
}

// Chapter 15: Installing applications
// question: 15 name: Switch category to $module$/top/Chapter 15: Installing applications
$CATEGORY: $module$/top/Chapter 15: Installing applications

// question: 15.1 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Một ứng dụng Kubernetes được định nghĩa là gì?</p>{
	~[moodle]Một image container chạy một dịch vụ duy nhất.#<p>Đó là một phần của ứng dụng, không phải toàn bộ ứng dụng.</p>
	=[moodle]Một tập hợp các tài nguyên API cần được triển khai cho một dịch vụ.
	~[moodle]Một tập hợp các tệp cấu hình YAML được lưu trữ trong Git.#<p>YAML files là cách định nghĩa, không phải ứng dụng.</p>
	~[moodle]Một dịch vụ microservice có khả năng tự phục hồi.#<p>Microservice là một kiến trúc, không phải định nghĩa ứng dụng Kubernetes.</p>
	####<p><strong>Giải thích</strong>\: Một ứng dụng Kubernetes là một tập hợp các tài nguyên API cần được triển khai cho một dịch vụ. Ví dụ điển hình là ứng dụng Guestbook.</p>
}

// question: 15.2 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Điều gì gây ra chi phí cao khi quản lý các ứng dụng microservice so với các ứng dụng monolith truyền thống?</p>{
	~[moodle]Yêu cầu ít tài nguyên CPU hơn.#<p>Microservice có thể tiêu thụ ít CPU hơn nhưng tổng chi phí quản lý cấu hình cao.</p>
	=[moodle]Yêu cầu hàng nghìn dòng mã cấu hình.
	~[moodle]Khó khăn trong việc giao tiếp giữa các dịch vụ.#<p>Microservice được thiết kế để giao tiếp dễ dàng hơn qua mạng.</p>
	~[moodle]Thiếu công cụ giám sát hiệu suất.#<p>Kubernetes ecosystem có nhiều công cụ giám sát.</p>
	####<p><strong>Giải thích</strong>\: Microservice có chi phí cao khi so sánh với ứng dụng monolith vì chúng yêu cầu cấu hình riêng cho từng dịch vụ, dẫn đến hàng nghìn dòng mã cấu hình YAML.</p>
}

// question: 15.3 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Khi triển khai nhiều tài nguyên Kubernetes dưới dạng một ứng dụng từ một tệp lớn duy nhất, vấn đề chính là gì?</p>{
	=[moodle]Khó theo dõi nguồn gốc và trạng thái sức khỏe tổng thể của ứng dụng.
	~[moodle]Các Pod sẽ không thể giao tiếp với nhau.#<p>Networking vẫn hoạt động bình thường.</p>
	~[moodle]Ứng dụng sẽ không thể chia tỷ lệ tự động.#<p>Scaling là chức năng của Kubernetes.</p>
	~[moodle]Việc này sẽ làm tăng chi phí lưu trữ đáng kể.#<p>Storage cost không liên quan trực tiếp đến định nghĩa YAML.</p>
	####<p><strong>Giải thích</strong>\: Triển khai một danh sách lớn tài nguyên Kubernetes từ một tệp lớn gây khó khăn trong việc theo dõi nguồn gốc và trạng thái sức khỏe tổng thể của ứng dụng.</p>
}

// question: 15.4 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Hai giải pháp được đề xuất để quản lý cấu hình ứng dụng Kubernetes trong thế giới thực là gì?</p>{
	~[moodle]Sử dụng Helm charts và GitOps.#<p>Các công cụ được liệt kê là khả thi, nhưng không phải giải pháp chính được thảo luận.</p>
	=[moodle]Sử dụng YAML templating và triển khai/nâng cấp bằng Operator.
	~[moodle]Sử dụng ConfigMaps và Secrets.#<p>Các công cụ được liệt kê là khả thi, nhưng không phải giải pháp chính được thảo luận.</p>
	~[moodle]Sử dụng Kustomize và ArgoCD.#<p>Các công cụ được liệt kê là khả thi, nhưng không phải giải pháp chính được thảo luận.</p>
	####<p><strong>Giải thích</strong>\: Hai giải pháp được đề xuất là "YAML templating" (ví dụ: với ytt, kustomize hoặc helm3) và "triển khai và nâng cấp ứng dụng" (ví dụ: với Carvel kapp-controller hoặc Kubernetes Operator).</p>
}

// question: 15.5 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Bộ công cụ Carvel bao gồm những công cụ mô-đun nào?</p>{
	~[moodle]Docker, kubectl, Helm.#<p>Đây là các công cụ khác, không thuộc bộ công cụ Carvel.</p>
	=[moodle]ytt, kapp, kapp-controller, kbld, imgpkg, kwt, vendir.
	~[moodle]Prometheus, Grafana, Loki.#<p>Đây là các công cụ khác, không thuộc bộ công cụ Carvel.</p>
	~[moodle]Ansible, Chef, Puppet.#<p>Đây là các công cụ khác, không thuộc bộ công cụ Carvel.</p>
	####<p><strong>Giải thích</strong>\: Bộ công cụ Carvel bao gồm nhiều công cụ mô-đun như ytt, kapp, kapp-controller, kbld, imgpkg, kwt, vendir.</p>
}

// question: 15.6 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Tại sao việc chia nhỏ các tệp cấu hình YAML lớn thành các tệp nhỏ hơn được khuyến nghị?</p>{
	~[moodle]Để tăng hiệu suất triển khai ứng dụng.#<p>Performance không phải là lý do chính.</p>
	=[moodle]Để làm cho việc sử dụng các công cụ như grep hoặc sed dễ dàng hơn.
	~[moodle]Để giảm tổng kích thước của cấu hình ứng dụng.#<p>Total size không thay đổi.</p>
	~[moodle]Để kích hoạt tính năng tự động chia tỷ lệ của Kubernetes.#<p>Auto-scaling không liên quan đến cấu trúc tệp YAML.</p>
	####<p><strong>Giải thích</strong>\: Việc chia nhỏ tài nguyên thành các tệp riêng biệt giúp việc sử dụng các công cụ như grep hoặc sed dễ dàng hơn và đơn giản hóa việc kiểm soát phiên bản.</p>
}

// question: 15.7 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>ytt (YAML templating engine) cho phép tùy chỉnh tệp YAML theo những cách nào?</p>{
	~[moodle]Chỉ bằng cách thêm các biến môi trường.#<p>Variables chỉ là một phần nhỏ.</p>
	=[moodle]Bằng cách overlaying, patching, và sử dụng ngôn ngữ Starlark để logic.
	~[moodle]Chỉ bằng cách sắp xếp lại các khóa YAML.#<p>Reordering không phải là tùy chỉnh chính.</p>
	~[moodle]Bằng cách tự động tạo các bản sao của tệp YAML.#<p>ytt là công cụ "YAML in, YAML out", không tự động tạo bản sao.</p>
	####<p><strong>Giải thích</strong>\: ytt cho phép tùy chỉnh các tệp YAML bằng cách overlaying, patching, và nó cũng hỗ trợ các cấu trúc nâng cao bằng cách sử dụng ngôn ngữ Starlark để thực hiện các quyết định logic cho việc thao tác văn bản.</p>
}

// question: 15.8 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Khi cả ENTRYPOINT và CMD đều được định nghĩa trong Dockerfile (và đều ở dạng exec form), điều gì xảy ra khi container khởi chạy?</p>{
	~[moodle]CMD sẽ được thực thi trước, sau đó là ENTRYPOINT.#<p>ENTRYPOINT chạy trước và nhận CMD như đối số.</p>
	=[moodle]ENTRYPOINT sẽ được thực thi với các đối số được cung cấp bởi CMD.
	~[moodle]Cả hai lệnh sẽ chạy song song dưới dạng các tiến trình độc lập.#<p>Chỉ ENTRYPOINT chạy như tiến trình chính.</p>
	~[moodle]CMD sẽ bị bỏ qua hoàn toàn nếu ENTRYPOINT được định nghĩa.#<p>CMD không bị bỏ qua mà cung cấp đối số.</p>
	####<p><strong>Giải thích</strong>\: Khi cả ENTRYPOINT và CMD đều được định nghĩa (và ở dạng exec form), bất cứ thứ gì được cung cấp cho CMD sẽ được truyền vào ENTRYPOINT dưới dạng đối số. ENTRYPOINT sẽ chạy như tiến trình cấp cao nhất của container và nhận các đối số đó.</p>
}

// question: 15.9 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>ytt là một công cụ "YAML in, YAML out". Điều này có ý nghĩa gì?</p>{
	=[moodle]Nó chỉ chấp nhận tệp YAML làm đầu vào và luôn trả về YAML làm đầu ra.
	~[moodle]Nó là công cụ duy nhất trong Carvel framework xử lý YAML.#<p>kapp cũng xử lý YAML.</p>
	~[moodle]Nó có thể chuyển đổi các tệp cấu hình từ bất kỳ định dạng nào sang YAML.#<p>ytt không chuyển đổi định dạng.</p>
	~[moodle]Nó là công cụ triển khai ứng dụng Kubernetes chính.#<p>kapp là công cụ triển khai.</p>
	####<p><strong>Giải thích</strong>\: ytt là một công cụ "YAML in, YAML out", nghĩa là nó tập trung vào việc thao tác YAML: chấp nhận YAML làm đầu vào và trả về YAML đã được sửa đổi làm đầu ra.</p>
}

// question: 15.10 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Công cụ kapp trong bộ công cụ Carvel được sử dụng để làm gì?</p>{
	~[moodle]Để tạo các image container mới.#<p>kbld và imgpkg là để tạo và quản lý image.</p>
	=[moodle]Để quản lý và triển khai toàn bộ ứng dụng Kubernetes như một đơn vị duy nhất.
	~[moodle]Để tùy chỉnh các tệp YAML bằng cách thêm các biến.#<p>ytt là để tùy chỉnh YAML.</p>
	~[moodle]Để quét các lỗ hổng bảo mật trong cấu hình ứng dụng.#<p>Linters là để quét lỗ hổng.</p>
	####<p><strong>Giải thích</strong>\: kapp được sử dụng để quản lý và triển khai toàn bộ ứng dụng Kubernetes dưới dạng một tập hợp các tài nguyên được quản lý một cách nguyên tử (atomic fashion).</p>
}

// question: 15.11 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Khi sử dụng kapp, một ứng dụng được coi là một "first-class citizen". Điều này có ý nghĩa gì?</p>{
	~[moodle]Nó cho phép kapp chỉ quản lý các ứng dụng cốt lõi của Kubernetes.#<p>kapp quản lý các ứng dụng của người dùng.</p>
	=[moodle]kapp cung cấp thông tin chi tiết về trạng thái của tất cả các tài nguyên trong ứng dụng đó.
	~[moodle]Các ứng dụng chỉ có thể được triển khai trong default namespace.#<p>kapp có thể triển khai trong nhiều namespace.</p>
	~[moodle]Các ứng dụng phải được định nghĩa bằng CRD.#<p>kapp có thể hoạt động mà không cần CRD.</p>
	####<p><strong>Giải thích</strong>\: kapp coi một ứng dụng là "first-class citizen", nghĩa là nó cung cấp nhiều thông tin hơn so với kubectl, bao gồm trạng thái thành công/thất bại của tất cả các tài nguyên trong ứng dụng đó trong một định dạng bảng dễ đọc.</p>
}

// question: 15.12 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>"kapp Operator" trong kapp-controller giúp tự động hóa điều gì?</p>{
	~[moodle]Chỉ việc sao chép tệp YAML từ Git repository.#<p>Fetch là để lấy code, không phải tự động hóa ytt.</p>
	=[moodle]Việc tự động hóa độ phức tạp của ytt và quản lý ứng dụng một cách khai báo.
	~[moodle]Chỉ việc xóa các tài nguyên ứng dụng.#<p>kapp delete là để xóa, không phải tự động hóa cấu hình.</p>
	~[moodle]Việc cung cấp PersistentVolumes động.#<p>CSI provisioner cung cấp PersistentVolumes động.</p>
	####<p><strong>Giải thích</strong>\: kapp-controller cho phép tự động hóa độ phức tạp của ytt và quản lý ứng dụng một cách khai báo, hoàn toàn trong Kubernetes, bằng cách tạo một kapp CR (Custom Resource).</p>
}

// question: 15.13 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>"Kubernetes Operator" là gì?</p>{
	~[moodle]Một công cụ dòng lệnh để quản lý các Pod.#<p>kubectl là công cụ dòng lệnh.</p>
	=[moodle]Một controller Kubernetes theo dõi API server để thay đổi và chạy các tác vụ quản trị.
	~[moodle]Một giao diện lập trình ứng dụng (API) để tương tác với các dịch vụ đám mây.#<p>Kubernetes API là giao diện lập trình.</p>
	~[moodle]Một hình ảnh cơ sở (base image) được tối ưu hóa cho các ứng dụng microservice.#<p>distroless là hình ảnh cơ sở.</p>
	####<p><strong>Giải thích</strong>\: "Operator" là các controller Kubernetes theo dõi API server để tìm kiếm các thay đổi và sau đó chạy các tác vụ quản trị Kubernetes để phản hồi, mở rộng khả năng của Kubernetes.</p>
}

// question: 15.14 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Tại sao các ứng dụng native của Kubernetes thường tạo ra nhiều "CRDs" (Custom Resource Definitions)?</p>{
	~[moodle]Để tối ưu hóa việc sử dụng CPU của Pod.#<p>CRDs không trực tiếp tối ưu hóa CPU.</p>
	=[moodle]Để sử dụng Kubernetes API server làm nơi lưu trữ dữ liệu cấu hình.
	~[moodle]Để tích hợp với các công cụ giám sát bên ngoài.#<p>CRDs có thể giúp tích hợp giám sát, nhưng không phải là mục đích chính.</p>
	~[moodle]Để tăng tốc độ triển khai ứng dụng.#<p>CRDs thêm một lớp trừu tượng, có thể không tăng tốc độ triển khai.</p>
	####<p><strong>Giải thích</strong>\: Các ứng dụng native của Kubernetes thường tạo ra nhiều CRD cho các ứng dụng của chúng. CRD cho phép bất kỳ ứng dụng nào sử dụng Kubernetes API server để lưu trữ dữ liệu cấu hình.</p>
}

// question: 15.15 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Điều gì đã thay đổi cách code PersistentVolume được quản lý trong Kubernetes?</p>{
	~[moodle]Sự ra đời của Deployment.#<p>Deployment quản lý Pod.</p>
	=[moodle]Sự phát triển của CSI (Container Storage Interface).
	~[moodle]Việc sử dụng hostPath volume.#<p>hostPath là một loại volume cụ thể.</p>
	~[moodle]Sự phổ biến của emptyDir volume.#<p>emptyDir là một loại volume cụ thể.</p>
	####<p><strong>Giải thích</strong>\: CSI (Container Storage Interface) đã thay đổi cách quản lý PersistentVolume, khiến code PersistentVolume không cần phải được biên dịch vào bản phát hành Kubernetes nữa.</p>
}

// question: 15.16 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>"Dynamic provisioning" (cung cấp động) trong Kubernetes đề cập đến khả năng gì?</p>{
	~[moodle]Tự động di chuyển Pod giữa các node.#<p>Scheduler và kubelet quản lý di chuyển Pod.</p>
	=[moodle]Cung cấp các volume lưu trữ khi có yêu cầu (PVC) mà không cần tạo thủ công.
	~[moodle]Điều chỉnh số lượng node trong cluster một cách tự động.#<p>Cluster autoscaler điều chỉnh số lượng node.</p>
	~[moodle]Tự động cấu hình DNS cho các Pod.#<p>CoreDNS cấu hình DNS.</p>
	####<p><strong>Giải thích</strong>\: "Dynamic provisioning" là khả năng tạo các volume lưu trữ "on the fly" (ngay lập tức) khi một PVC được tạo, thay vì phải tạo PersistentVolume thủ công trước.</p>
}

// question: 15.17 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Các StorageClasses trong Kubernetes chủ yếu được sử dụng cho mục đích gì?</p>{
	~[moodle]Để tạo các bản sao lưu (snapshots) của dữ liệu.#<p>VolumeSnapshot API mới hỗ trợ snapshots.</p>
	=[moodle]Để chỉ định các ngữ nghĩa lưu trữ phức tạp một cách khai báo.
	~[moodle]Để mã hóa dữ liệu trên đĩa.#<p>etcd encryption hoặc các giải pháp mã hóa khác xử lý mã hóa dữ liệu.</p>
	~[moodle]Để giám sát việc sử dụng lưu trữ.#<p>Prometheus và cAdvisor là công cụ giám sát.</p>
	####<p><strong>Giải thích</strong>\: StorageClasses cho phép các ngữ nghĩa lưu trữ phức tạp được chỉ định một cách khai báo, đáp ứng các yêu cầu khác nhau của người dùng cuối.</p>
}

// question: 15.18 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Tại sao emptyDir volume được coi là một "Swiss army knife" cho các Pod?</p>{
	~[moodle]Vì nó có thể được sử dụng để lưu trữ dữ liệu bền vững.#<p>emptyDir không bền vững, dữ liệu bị xóa khi Pod bị xóa.</p>
	=[moodle]Vì nó được sử dụng như một scratchpad để chia sẻ dữ liệu giữa các container trong cùng một Pod.
	~[moodle]Vì nó cung cấp hiệu suất I/O cao nhất trên các hệ thống non-Linux.#<p>emptyDir trên tmpfs có thể nhanh, nhưng không phải trên non-Linux.</p>
	~[moodle]Vì nó tự động sao lưu dữ liệu ra bên ngoài cluster.#<p>emptyDir không có tính năng sao lưu.</p>
	####<p><strong>Giải thích</strong>\: emptyDir volume thường được sử dụng như một "Swiss army knife" (dao đa năng) trong Pods cho nhiều mục đích khác nhau, đặc biệt là khi hai container cần một scratchpad để ghi dữ liệu.</p>
}

// question: 15.19 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Hạn chế chính của việc lưu trữ dữ liệu trong OverlayFS mặc định của container Docker là gì?</p>{
	~[moodle]Dữ liệu chỉ có thể được truy cập bởi một container duy nhất.#<p>OverlayFS cho phép container truy cập dữ liệu, nhưng không phải là giải pháp lưu trữ dữ liệu bền vững.</p>
	~[moodle]Hiệu suất đọc/ghi bị suy giảm đáng kể.#<p>Copy-up có thể làm chậm hiệu suất I/O, nhưng nhược điểm chính được nhấn mạnh là mất dữ liệu.</p>
	=[moodle]Dữ liệu sẽ bị xóa sau khi container bị xóa.
	~[moodle]Dữ liệu không thể sao lưu hoặc phục hồi.#<p>Có những cách để sao lưu và phục hồi dữ liệu từ container thông qua Volumes hoặc bind mounts.</p>
	####<p><strong>Giải thích</strong>\: Một nhược điểm lớn của hệ thống tệp tin overlay là mọi dữ liệu được lưu trữ trong đó sẽ bị xóa khi container bị xóa.</p>
}

// question: 15.20 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>VolumeClaimTemplates trong StatefulSet có chức năng gì?</p>{
	~[moodle]Định nghĩa cấu hình mạng cho các Pod trong StatefulSet.#<p>Service và NetworkPolicy định nghĩa mạng.</p>
	=[moodle]Cung cấp một cách để khai báo PersistentVolumes cho một StatefulSet.
	~[moodle]Xác định chính sách bảo mật cho các Pod trong StatefulSet.#<p>Security context định nghĩa bảo mật.</p>
	~[moodle]Tạo các bản sao lưu (snapshots) của dữ liệu cho StatefulSet.#<p>VolumeSnapshot API mới hỗ trợ snapshots.</p>
	####<p><strong>Giải thích</strong>\: VolumeClaimTemplates là một cấu trúc trong Kubernetes API cho phép khai báo PersistentVolumes cho một StatefulSet một cách tự động, dựa trên kích thước của StatefulSet.</p>
}

// question: 15.21 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Khi nào thì việc sử dụng hostPath volume trong Kubernetes thường được coi là một "anti-pattern" cho việc lưu trữ dữ liệu bền vững?</p>{
	~[moodle]Khi Pod cần truy cập các tệp tin hệ thống.#<p>hostPath là cần thiết cho các tác vụ quản trị như CNI/CSI.</p>
	~[moodle]Khi ứng dụng cần chia sẻ dữ liệu giữa các container.#<p>emptyDir được sử dụng để chia sẻ dữ liệu giữa các container.</p>
	=[moodle]Khi Pod biến mất và được lên lịch lại trên một node mới, dữ liệu có thể không còn ở cùng vị trí dự đoán.
	~[moodle]Khi Pod cần hiệu suất I/O cao.#<p>hostPath có thể cung cấp I/O nhanh nếu nó là đĩa cục bộ, nhưng đây không phải là lý do nó là "anti-pattern".</p>
	####<p><strong>Giải thích</strong>\: hostPath volume thường là một "anti-pattern" vì khi một Pod biến mất và sau đó được lên lịch lại trên một node mới, dữ liệu của nó không còn tồn tại ở vị trí dự đoán ban đầu, khiến ứng dụng hoạt động khác biệt.</p>
}

// question: 15.22 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Các "volume snapshots" và "cloning" trong Kubernetes 1.17 trở đi là gì?</p>{
	=[moodle]Các tùy chọn lưu trữ phổ biến mới, có thể được triển khai hoàn toàn trong Kubernetes.
	~[moodle]Các công cụ gỡ lỗi mới cho các lỗi lưu trữ.#<p>Snapshots không phải là công cụ gỡ lỗi.</p>
	~[moodle]Các chính sách để tự động xóa các volume cũ.#<p>Reclaim policy là để xóa volume cũ.</p>
	~[moodle]Các tính năng tích hợp với Docker Hub.#<p>Không liên quan đến Docker Hub.</p>
	####<p><strong>Giải thích</strong>\: Kể từ Kubernetes 1.17, "snapshots" và "cloning" đang nổi lên như các tùy chọn lưu trữ phổ biến mới trong Kubernetes API, có thể được triển khai hoàn toàn trong Kubernetes.</p>
}

// question: 15.23 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Để hỗ trợ tính năng "snapshots" và "cloning", một nhà cung cấp lưu trữ chỉ cần triển khai những gì trong API CSI?</p>{
	~[moodle]Các hàm CreateVolume, DeleteVolume.#<p>CreateVolume, DeleteVolume là cho quản lý volume cơ bản.</p>
	=[moodle]Các hàm CreateSnapshot, DeleteSnapshot, ListSnapshots.
	~[moodle]Các hàm NodeStageVolume, NodePublishVolume.#<p>NodeStageVolume, NodePublishVolume là cho gắn kết volume trên node.</p>
	~[moodle]Hàm GetPluginInfo.#<p>GetPluginInfo là để tự nhận diện plugin.</p>
	####<p><strong>Giải thích</strong>\: Để hỗ trợ tính năng "snapshots" và "cloning", một nhà cung cấp lưu trữ chỉ cần triển khai một vài API CSI như CreateSnapshot, DeleteSnapshot, ListSnapshots.</p>
}

// question: 15.24 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>FROM scratch trong một Dockerfile dùng để làm gì trong các build multi-stage?</p>{
	~[moodle]Để tạo một base image chứa tất cả các công cụ phát triển.#<p>scratch tạo ra một image trống.</p>
	=[moodle]Để tạo một image Docker tối thiểu, chỉ chứa ứng dụng cuối cùng mà không có hệ điều hành cơ bản.
	~[moodle]Để sử dụng phiên bản cũ nhất của base image.#<p>scratch không liên quan đến phiên bản cũ nhất.</p>
	~[moodle]Để đảm bảo image được xây dựng trên kiến trúc X86.#<p>scratch không liên quan đến kiến trúc X86.</p>
	####<p><strong>Giải thích</strong>\: FROM scratch được sử dụng để tạo một image cơ sở của riêng bạn. Trong các build multi-stage, nó đặc biệt hữu ích để tạo một giai đoạn cuối cùng nơi bạn sao chép artifact ứng dụng cuối cùng vào một image scratch, làm cho image gần như chỉ lớn bằng ứng dụng và hoàn toàn tự chứa.</p>
}

// question: 15.25 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Mục đích chính của việc sử dụng các "build multi-stage" trong Dockerfile là gì?</p>{
	~[moodle]Chỉ cho phép sử dụng một base image duy nhất trong Dockerfile.#<p>Multi-stage builds cho phép nhiều base image.</p>
	=[moodle]Tạo ra các image container cuối cùng nhỏ hơn và an toàn hơn.
	~[moodle]Tăng kích thước image container bằng cách thêm tất cả các công cụ phát triển vào đó.#<p>Multi-stage builds giúp giảm kích thước image.</p>
	~[moodle]Hạn chế khả năng chạy ứng dụng trên các kiến trúc bộ xử lý khác nhau.#<p>Multi-stage builds không ảnh hưởng đến kiến trúc bộ xử lý.</p>
	####<p><strong>Giải thích</strong>\: Lợi ích chính của việc sử dụng các "build multi-stage" là tạo ra các image container cuối cùng nhỏ hơn và an toàn hơn bằng cách chỉ giữ lại các artifact cần thiết.</p>
}

// question: 15.26 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Công cụ kind (Kubernetes in Docker) được sử dụng để làm gì?</p>{
	~[moodle]Triển khai các cluster Kubernetes production quy mô lớn.#<p>kind không được thiết kế cho production.</p>
	=[moodle]Tạo các cluster Kubernetes (đơn hoặc đa node) bên trong một container runtime như Docker Engine.
	~[moodle]Giám sát hiệu suất của các cluster Kubernetes.#<p>Prometheus là để giám sát hiệu suất.</p>
	~[moodle]Cung cấp lưu trữ bền vững cho các ứng dụng Kubernetes.#<p>CSI và PV/PVC cung cấp lưu trữ.</p>
	####<p><strong>Giải thích</strong>\: kind là một công cụ dành cho nhà phát triển để chạy các cluster Kubernetes (đơn hoặc đa node) bên trong một container runtime như Docker Engine, không có các phụ thuộc khác.</p>
}

// question: 15.27 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Ưu điểm chính của việc sử dụng kind cho mục đích học tập và thử nghiệm Kubernetes là gì?</p>{
	~[moodle]Đảm bảo hiệu suất cao cho các workload production.#<p>kind không dành cho production.</p>
	=[moodle]Chi phí bằng không, có thể cài đặt và xây dựng lại nhanh chóng.
	~[moodle]Tích hợp sâu với các dịch vụ đám mây lớn.#<p>kind không tích hợp với các dịch vụ đám mây.</p>
	~[moodle]Hỗ trợ tất cả các hệ điều hành một cách tự nhiên mà không cần ảo hóa.#<p>kind sử dụng Docker, hoạt động trên các OS khác thông qua ảo hóa (ví dụ: WSL 2 trên Windows).</p>
	####<p><strong>Giải thích</strong>\: Ưu điểm của kind cho việc học là nó không tốn kém, có thể cài đặt và xây dựng lại trong vài giây, và có thể chạy chức năng Kubernetes cơ bản mà không gặp vấn đề.</p>
}

// question: 15.28 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Trong quá trình cài đặt ứng dụng Guestbook với kapp, kapp thực hiện điều gì sau khi triển khai tài nguyên?</p>{
	~[moodle]Ngay lập tức xóa các tài nguyên nếu có lỗi.#<p>kapp chờ và báo cáo trạng thái, không xóa ngay lập tức.</p>
	=[moodle]Chú thích (annotate) các tài nguyên để sau này có thể quản lý chúng.
	~[moodle]Tự động chuyển đổi định dạng tài nguyên thành CRD.#<p>kapp không tự động chuyển đổi thành CRD, mặc dù nó có thể quản lý chúng.</p>
	~[moodle]Thay đổi tên của các tài nguyên để tránh xung đột.#<p>kapp sử dụng tên bạn cung cấp, không phải thay đổi chúng.</p>
	####<p><strong>Giải thích</strong>\: kapp sẽ chú thích các tài nguyên của bạn để nó có thể quản lý chúng sau này, bao gồm nâng cấp, xóa hoặc cung cấp trạng thái tổng thể của ứng dụng theo tên.</p>
}

// question: 15.29 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Điều gì làm cho các CNI (Container Network Interface) và CSI (Container Storage Interface) driver dựa vào việc sử dụng hostPath volume?</p>{
	~[moodle]Để đơn giản hóa việc cấu hình mạng.#<p>hostPath không phải để đơn giản hóa cấu hình mạng mà là để kích hoạt chức năng cấp thấp.</p>
	=[moodle]Để cài đặt các binary của chúng từ bên trong container lên node.
	~[moodle]Để tăng hiệu suất truy cập mạng.#<p>hostPath không trực tiếp tăng hiệu suất mạng.</p>
	~[moodle]Để đảm bảo khả năng tương thích với Windows OS.#<p>hostPath theo truyền thống là giải pháp Linux cụ thể, các OS khác có cơ chế khác.</p>
	####<p><strong>Giải thích</strong>\: Các nhà cung cấp CNI cài đặt chính chúng vào kubelet bằng cách ghi các binary của họ từ bên trong một container lên chính node đó, thường vào thư mục /opt/cni/bin. Điều này cũng đúng với CSI.</p>
}

// question: 15.30 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Khi nào việc cài đặt toàn bộ Docker Engine bên trong một container để chạy "Docker in Docker" không được khuyến nghị?</p>{
	~[moodle]Khi container cần truy cập internet.#<p>Các vấn đề của cách tiếp cận này không trực tiếp liên quan đến truy cập internet.</p>
	~[moodle]Khi cần một cách ly mạng mạnh mẽ.#<p>Các vấn đề của cách tiếp cận này không trực tiếp liên quan đến cách ly mạng mạnh mẽ.</p>
	=[moodle]Có nhiều vấn đề và không được khuyến nghị.
	~[moodle]Khi ứng dụng cần hiệu suất cao.#<p>Các vấn đề của cách tiếp cận này không trực tiếp liên quan đến hiệu suất cao.</p>
	####<p><strong>Giải thích</strong>\: Cài đặt toàn bộ Docker Engine bên trong container có nhiều vấn đề và không được khuyến nghị.</p>
}

// question: 15.31 name: Chapter 15: Installing applications
::Chapter 15\: Installing applications::[html]<p>Phương pháp được khuyến nghị để chạy "Docker in Docker" là gì?</p>{
	~[moodle]Cài đặt toàn bộ Docker Engine bên trong container.#<p>Cài đặt toàn bộ Docker Engine bên trong container có nhiều vấn đề và không được khuyến nghị.</p>
	=[moodle]Gắn kết Unix socket của Docker Engine vào container và chỉ cài đặt Docker client.
	~[moodle]Sử dụng một hypervisor ảo hóa bên trong container.#<p>Cách tiếp cận này không phải là "Docker in Docker" mà là nested virtualization, và không được khuyến nghị cho Docker in Docker.</p>
	~[moodle]Xây dựng lại Docker Engine từ mã nguồn bên trong container.#<p>Rebuilding from source code là không thực tế và không cần thiết.</p>
	####<p><strong>Giải thích</strong>\: Phương pháp được khuyến nghị và đơn giản hơn nhiều là cấu hình container để giao tiếp với một Docker Engine hiện có bằng cách gắn kết Unix socket của Docker Engine (thường là /var/run/docker.sock) vào container, và chỉ cài đặt Docker client bên trong container.</p>
}