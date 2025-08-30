// Chapter 1: What is Amazon Web Services?

// question: 1.1  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>AWS được phân loại là loại hình dịch vụ điện toán đám mây nào dựa trên các tài nguyên cơ bản như máy tính ảo, lưu trữ và mạng?</p>{
	~[moodle]Platform as a service (PaaS) cung cấp các nền tảng để triển khai ứng dụng tùy chỉnh cho đám mây.#<p>PaaS cung cấp các nền tảng để triển khai ứng dụng tùy chỉnh lên đám mây, ví dụ như AWS Elastic Beanstalk.</p>
	~[moodle]Software as a service (SaaS) kết hợp cơ sở hạ tầng và phần mềm chạy trên đám mây.#<p>SaaS kết hợp cơ sở hạ tầng và phần mềm chạy trên đám mây, bao gồm các ứng dụng văn phòng như Amazon WorkSpaces.</p>
	=[moodle]Infrastructure as a service (IaaS) cung cấp các tài nguyên cơ bản như máy tính, lưu trữ và mạng.
	~[moodle]Cloud-native as a service (CNaaS) tập trung vào các ứng dụng được xây dựng cho đám mây.#<p>CNaaS không phải là một phân loại dịch vụ đám mây tiêu chuẩn được đề cập trong nguồn.</p>
	####<p><strong>Giải thích</strong>: Infrastructure as a service (IaaS) cung cấp các tài nguyên cơ bản như khả năng tính toán, lưu trữ và mạng, sử dụng các máy ảo như Amazon EC2.</p>
}

// question: 1.2  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>Lợi ích chính của việc sử dụng AWS về mặt khả năng điều chỉnh tài nguyên là gì?</p>{
	~[moodle]Giảm thiểu rủi ro lỗi phần cứng bằng cách sử dụng các máy chủ vật lý mạnh mẽ.#<p>AWS cung cấp độ tin cậy và khả năng phục hồi từ lỗi, nhưng lợi ích chính về khả năng điều chỉnh tài nguyên là sự linh hoạt trong dung lượng.</p>
	=[moodle]Loại bỏ nhu cầu dự đoán trước nhu cầu dung lượng lưu trữ và tính toán trong tương lai.
	~[moodle]Tăng cường khả năng bảo mật vật lý cho các trung tâm dữ liệu toàn cầu của bạn.#<p>AWS chịu trách nhiệm về bảo mật của đám mây, nhưng đây không phải là lợi ích chính của khả năng điều chỉnh tài nguyên.</p>
	~[moodle]Đảm bảo rằng tất cả các ứng dụng luôn chạy với quyền truy cập root vào hệ điều hành.#<p>Việc cấp quyền root không phải là một lợi ích liên quan đến khả năng điều chỉnh dung lượng mà là một khía cạnh bảo mật.</p>
	####<p><strong>Giải thích</strong>: Flexible capacity (scalability) giải phóng bạn khỏi việc lập kế hoạch. Bạn không còn cần phải dự đoán nhu cầu dung lượng trong tương lai cho các tháng và năm tới.</p>
}

// question: 1.3  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>Trung tâm dữ liệu của AWS được phân bố trên toàn thế giới nhằm mục đích chính nào?</p>{
	~[moodle]Giảm thiểu chi phí vận hành cho khách hàng bằng cách tập trung tài nguyên vào một vài địa điểm.#<p>Mặc dù AWS mang lại lợi ích về kinh tế theo quy mô, việc phân bố trung tâm dữ liệu không nhằm mục đích tập trung tài nguyên mà là phân tán.</p>
	=[moodle]Cho phép khách hàng phục vụ người dùng trên toàn cầu với độ trễ mạng thấp hơn và tuân thủ các quy định khu vực.
	~[moodle]Đơn giản hóa kiến trúc ứng dụng bằng cách loại bỏ nhu cầu về các vùng sẵn sàng.#<p>Các vùng sẵn sàng (AZs) là một phần quan trọng của kiến trúc AWS để xây dựng hệ thống có tính sẵn sàng cao.</p>
	~[moodle]Hạn chế khả năng mở rộng của ứng dụng để đảm bảo hiệu suất ổn định.#<p>Cơ sở hạ tầng toàn cầu của AWS thúc đẩy khả năng mở rộng, không hạn chế nó.</p>
	####<p><strong>Giải thích</strong>: Việc sử dụng cơ sở hạ tầng toàn cầu của AWS có các lợi thế như độ trễ mạng thấp giữa người dùng và cơ sở hạ tầng của bạn, khả năng tuân thủ các yêu cầu bảo vệ dữ liệu khu vực.</p>
}

// question: 1.4  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>Mô hình giá "trả theo mức sử dụng" (pay-per-use) của AWS tạo ra cơ hội mới nào cho các dự án khởi nghiệp?</p>{
	~[moodle]Yêu cầu đầu tư lớn vào cơ sở hạ tầng ban đầu trước khi triển khai.#<p>Điều này ngược lại với lợi ích mà mô hình pay-per-use mang lại.</p>
	=[moodle]Hạ thấp rào cản để bắt đầu một dự án mới do không cần đầu tư cơ sở hạ tầng ban đầu.
	~[moodle]Giới hạn số lượng dịch vụ AWS có thể sử dụng trong một dự án.#<p>Mô hình giá không giới hạn số lượng dịch vụ, mà là tính phí dựa trên việc sử dụng.</p>
	~[moodle]Buộc người dùng phải cam kết trước về dung lượng lưu trữ sẽ sử dụng.#<p>Bạn không cần cam kết trả trước về dung lượng lưu trữ.</p>
	####<p><strong>Giải thích</strong>: Mô hình giá pay-per-use của AWS tạo ra cơ hội mới, ví dụ như hạ thấp rào cản để bắt đầu một dự án mới, vì bạn không còn cần phải đầu tư vào cơ sở hạ tầng trả trước.</p>
}

// question: 1.5  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>Khi một ứng dụng web có lưu lượng truy cập thay đổi theo mùa (ví dụ: ngày so với đêm), AWS có thể giúp bằng cách nào?</p>{
	~[moodle]Cố định dung lượng máy chủ để xử lý mức tải cao nhất mọi lúc.#<p>Điều này dẫn đến chi phí không cần thiết khi lưu lượng thấp.</p>
	=[moodle]Tự động thêm dung lượng khi lưu lượng truy cập tăng và loại bỏ khi giảm.
	~[moodle]Yêu cầu người dùng tự điều chỉnh lưu lượng truy cập của họ để phù hợp với dung lượng máy chủ.#<p>Người dùng không có khả năng kiểm soát lưu lượng để điều chỉnh cho phù hợp với dung lượng máy chủ.</p>
	~[moodle]Chuyển đổi ứng dụng sang một trung tâm dữ liệu khác mỗi khi lưu lượng thay đổi.#<p>Chuyển đổi ứng dụng giữa các trung tâm dữ liệu không phải là cách chính để xử lý lưu lượng theo mùa mà là giải pháp cho tính sẵn sàng cao hoặc độ trễ thấp.</p>
	####<p><strong>Giải thích</strong>: Flexible capacity (scalability) cho phép bạn thêm dung lượng khi lưu lượng tăng và loại bỏ dung lượng khi lưu lượng giảm, thích ứng với các mô hình lưu lượng truy cập theo mùa.</p>
}

// question: 1.6  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>Amazon EC2 và Amazon S3 được mô tả là gì trong bối cảnh các dịch vụ của AWS?</p>{
	~[moodle]Chúng là các dịch vụ hỗ trợ mạng và tích hợp ứng dụng cho các hệ thống phức tạp.#<p>Mặc dù chúng có thể được tích hợp, đây không phải là mô tả chính về bản chất của chúng.</p>
	=[moodle]Chúng là các dịch vụ nổi bật nhất, cung cấp máy ảo và khả năng lưu trữ.
	~[moodle]Chúng là các công cụ quản lý triển khai và tự động hóa cơ sở hạ tầng.#<p>Các dịch vụ này không phải là công cụ triển khai hoặc tự động hóa cơ sở hạ tầng chính, mặc dù chúng có thể được quản lý bằng các công cụ đó.</p>
	~[moodle]Chúng là các công cụ phân tích dữ liệu và học máy tiên tiến cho các ứng dụng đám mây.#<p>EC2 và S3 là các dịch vụ tính toán và lưu trữ cơ bản, không phải dịch vụ phân tích hay học máy.</p>
	####<p><strong>Giải thích</strong>: Các dịch vụ nổi bật nhất do AWS cung cấp là EC2, cung cấp máy ảo, và S3, cung cấp khả năng lưu trữ.</p>
}

// question: 1.7  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>Khi nào nên sử dụng AWS Management Console?</p>{
	~[moodle]Khi bạn cần tự động hóa các tác vụ lặp đi lặp lại thông qua script và lệnh.#<p>CLI phù hợp hơn cho các tác vụ tự động hóa.</p>
	~[moodle]Khi bạn muốn tích hợp các dịch vụ AWS vào ứng dụng của mình bằng mã.#<p>SDKs được sử dụng để tích hợp các dịch vụ AWS vào ứng dụng.</p>
	=[moodle]Khi bạn đang bắt đầu hoặc thử nghiệm với AWS để có cái nhìn tổng quan nhanh chóng.
	~[moodle]Khi bạn cần triển khai cơ sở hạ tầng phức tạp dựa trên các bản thiết kế tự động hoàn toàn.#<p>Blueprints và CloudFormation phù hợp hơn cho việc triển khai tự động hóa cơ sở hạ tầng phức tạp.</p>
	####<p><strong>Giải thích</strong>: Khi bắt đầu hoặc thử nghiệm với AWS, Management Console là nơi tốt nhất để bắt đầu. Nó giúp bạn có được cái nhìn tổng quan về các dịch vụ khác nhau một cách nhanh chóng.</p>
}

// question: 1.8  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>Việc AWS liên tục giảm giá dịch vụ được xem là lợi ích nào của việc sử dụng nền tảng này?</p>{
	~[moodle]Khả năng phục hồi từ lỗi (Reliability) của hệ thống.#<p>Giảm giá không trực tiếp liên quan đến độ tin cậy.</p>
	=[moodle]Lợi ích từ kinh tế theo quy mô (Economies of Scale).
	~[moodle]Tăng tốc thời gian ra thị trường (Reducing Time to Market).#<p>Giảm giá không trực tiếp liên quan đến thời gian ra thị trường.</p>
	~[moodle]Nền tảng đổi mới và phát triển nhanh chóng (Innovative and Fast-Growing Platform).#<p>Mặc dù AWS là một nền tảng đổi mới, việc giảm giá là một biểu hiện của kinh tế theo quy mô.</p>
	####<p><strong>Giải thích</strong>: AWS liên tục tăng cường cơ sở hạ tầng toàn cầu của mình, do đó AWS được hưởng lợi từ kinh tế theo quy mô. Là khách hàng, bạn sẽ hưởng lợi một phần từ những hiệu ứng này, ví dụ như giá dịch vụ giảm.</p>
}

// question: 1.9  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>Nếu bạn muốn kiểm soát AWS từ terminal của mình, công cụ nào là phù hợp nhất?</p>{
	~[moodle]AWS Management Console để cấu hình dịch vụ thông qua giao diện đồ họa.#<p>Management Console là giao diện đồ họa dựa trên web.</p>
	~[moodle]AWS Software Development Kits (SDKs) để viết mã và tích hợp vào ứng dụng.#<p>SDKs được sử dụng để lập trình với các ngôn ngữ phổ biến.</p>
	=[moodle]AWS Command-Line Interface (CLI) để quản lý dịch vụ từ dòng lệnh.
	~[moodle]AWS CloudFormation để mô tả cơ sở hạ tầng bằng các mẫu JSON/YAML.#<p>CloudFormation sử dụng các mẫu để khai báo cơ sở hạ tầng.</p>
	####<p><strong>Giải thích</strong>: Command-line interface (CLI) cho phép bạn quản lý và truy cập các dịch vụ AWS trong terminal của bạn, rất hữu ích để tự động hóa các tác vụ định kỳ.</p>
}

// question: 1.10  name: Chapter 1: What is Amazon Web Services?
::Chapter 1\: What is Amazon Web Services?::[html]<p>Khi tạo tài khoản AWS mới, bước nào liên quan đến việc bảo vệ truy cập vào máy ảo Linux của bạn?</p>{
	~[moodle]Chọn gói hỗ trợ Basic miễn phí.#<p>Các bước này là một phần của quy trình tạo tài khoản nhưng không trực tiếp liên quan đến việc bảo vệ truy cập SSH vào máy ảo.</p>
	~[moodle]Cung cấp thông tin chi tiết thanh toán của bạn.#<p>Các bước này là một phần của quy trình tạo tài khoản nhưng không trực tiếp liên quan đến việc bảo vệ truy cập SSH vào máy ảo.</p>
	~[moodle]Xác minh danh tính của bạn bằng cuộc gọi điện thoại.#<p>Các bước này là một phần của quy trình tạo tài khoản nhưng không trực tiếp liên quan đến việc bảo vệ truy cập SSH vào máy ảo.</p>
	=[moodle]Tạo một cặp khóa (key pair) cho truy cập SSH.
	####<p><strong>Giải thích</strong>: Một cặp khóa (key pair) bao gồm khóa riêng tư và khóa công khai, được sử dụng để xác thực khi truy cập máy Linux thông qua giao thức SSH.</p>
}

// Chapter 2: A simple example: WordPress in five minutes

// question: 2.1  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi triển khai WordPress trên AWS bằng CloudFormation, dịch vụ nào được sử dụng để phân phối lưu lượng truy cập và đảm bảo tính sẵn sàng cao?</p>{
	~[moodle]Amazon Relational Database Service (RDS) cho cơ sở dữ liệu MySQL.#<p>RDS cung cấp cơ sở dữ liệu MySQL được quản lý cho WordPress.</p>
	=[moodle]Elastic Load Balancing (ELB) để cân bằng tải giữa các máy chủ web.
	~[moodle]Amazon Elastic File System (EFS) để lưu trữ các tệp ứng dụng và tải lên của người dùng.#<p>EFS cung cấp một hệ thống tệp mạng có khả năng mở rộng, sẵn sàng cao và bền bỉ để lưu trữ các tệp.</p>
	~[moodle]Amazon EC2 để chạy các máy chủ web riêng lẻ.#<p>EC2 cung cấp các máy ảo, nhưng ELB chịu trách nhiệm phân phối lưu lượng và tính sẵn sàng cao cho các máy ảo đó.</p>
	####<p><strong>Giải thích</strong>: Elastic Load Balancing (ELB) là một dịch vụ cân bằng tải có sẵn, phân phối lưu lượng truy cập đến một nhóm máy ảo và có tính sẵn sàng cao theo mặc định.</p>
}

// question: 2.2  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Dịch vụ nào của AWS được sử dụng để quản lý cơ sở dữ liệu MySQL cho WordPress, xử lý các tác vụ vận hành như sao lưu và cập nhật bản vá?</p>{
	~[moodle]Amazon EC2 để tự cài đặt và quản lý MySQL.#<p>Tự quản lý MySQL trên EC2 sẽ đòi hỏi nhiều công sức vận hành hơn.</p>
	~[moodle]Amazon DynamoDB, một dịch vụ cơ sở dữ liệu NoSQL, để lưu trữ dữ liệu.#<p>DynamoDB là cơ sở dữ liệu NoSQL, không tương thích với WordPress yêu cầu MySQL.</p>
	=[moodle]Amazon Relational Database Service (RDS) cho MySQL.
	~[moodle]Amazon S3 để lưu trữ các tệp cơ sở dữ liệu dưới dạng đối tượng.#<p>S3 là dịch vụ lưu trữ đối tượng, không phải cơ sở dữ liệu quan hệ.</p>
	####<p><strong>Giải thích</strong>: Amazon Relational Database Service (RDS) cho MySQL được sử dụng vì WordPress dựa vào cơ sở dữ liệu MySQL phổ biến. RDS đảm nhận các tác vụ vận hành như tạo bản sao lưu, cài đặt bản vá và cập nhật.</p>
}

// question: 2.3  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Để chia sẻ các tệp ứng dụng và tệp tải lên của người dùng giữa nhiều máy chủ web WordPress, dịch vụ nào của AWS được sử dụng?</p>{
	~[moodle]Amazon Elastic Block Store (EBS) để đính kèm bộ nhớ cấp khối vào mỗi máy ảo.#<p>EBS là bộ nhớ cấp khối được gắn vào một máy ảo duy nhất, không dễ dàng chia sẻ giữa nhiều máy ảo.</p>
	~[moodle]Amazon Simple Storage Service (S3) để lưu trữ các đối tượng riêng lẻ.#<p>S3 là dịch vụ lưu trữ đối tượng, không phải hệ thống tệp mạng.</p>
	=[moodle]Amazon Elastic File System (EFS) cung cấp một hệ thống tệp mạng có thể chia sẻ.
	~[moodle]Amazon Glacier để lưu trữ lâu dài các tệp không thường xuyên truy cập.#<p>Glacier là giải pháp lưu trữ dữ liệu lâu dài và không được sử dụng để chia sẻ tệp ứng dụng đang hoạt động.</p>
	####<p><strong>Giải thích</strong>: Elastic File System (EFS) được sử dụng để lưu trữ các tệp và truy cập chúng từ nhiều máy ảo, cung cấp một hệ thống tệp mạng có thể chia sẻ.</p>
}

// question: 2.4  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Trong kiến trúc WordPress trên AWS, "nhóm bảo mật" (security groups) đóng vai trò gì?</p>{
	~[moodle]Cung cấp mã hóa cho tất cả dữ liệu được truyền giữa các dịch vụ.#<p>Mã hóa được cấu hình ở các cấp độ khác nhau, không phải là chức năng chính của nhóm bảo mật.</p>
	=[moodle]Kiểm soát lưu lượng mạng đến và đi từ các tài nguyên AWS của bạn như máy ảo và cơ sở dữ liệu.
	~[moodle]Tự động sao lưu dữ liệu cơ sở dữ liệu của bạn vào Amazon S3.#<p>Sao lưu cơ sở dữ liệu được xử lý bởi RDS.</p>
	~[moodle]Giám sát hiệu suất của các máy chủ web và tự động điều chỉnh dung lượng.#<p>Giám sát và điều chỉnh dung lượng được xử lý bởi CloudWatch và Auto Scaling.</p>
	####<p><strong>Giải thích</strong>: Nhóm bảo mật đóng vai trò là tường lửa ảo để kiểm soát lưu lượng truy cập đến và đi từ các tài nguyên AWS của bạn, như máy ảo, cơ sở dữ liệu hoặc bộ cân bằng tải.</p>
}

// question: 2.5  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi tạo cơ sở hạ tầng WordPress phức tạp chỉ bằng vài cú nhấp chuột, dịch vụ AWS nào được sử dụng để tự động hóa tất cả các bước này?</p>{
	~[moodle]AWS Identity and Access Management (IAM) để quản lý quyền truy cập.#<p>IAM quản lý quyền truy cập vào tài nguyên đám mây của bạn.</p>
	=[moodle]AWS CloudFormation để triển khai cơ sở hạ tầng từ một bản thiết kế.
	~[moodle]AWS Elastic Beanstalk để triển khai ứng dụng web tự động.#<p>Elastic Beanstalk là một công cụ triển khai nhưng không phải là công cụ chính được sử dụng để tự động hóa toàn bộ cơ sở hạ tầng phức tạp này trong ví dụ.</p>
	~[moodle]AWS OpsWorks để triển khai ứng dụng đa tầng.#<p>OpsWorks cũng là một công cụ triển khai nhưng tập trung vào các ứng dụng đa tầng.</p>
	####<p><strong>Giải thích</strong>: AWS CloudFormation tự động thực hiện việc tạo bộ cân bằng tải, cơ sở dữ liệu MySQL, hệ thống tệp mạng, quy tắc tường lửa và hai máy ảo chạy máy chủ web với WordPress đã cấu hình.</p>
}

// question: 2.6  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Sau khi tạo một stack CloudFormation cho WordPress, bạn tìm thấy URL để truy cập cài đặt WordPress ở đâu trong AWS Management Console?</p>{
	~[moodle]Trong tab "Events" của stack CloudFormation.#<p>Tab "Events" hiển thị các sự kiện trong quá trình tạo stack.</p>
	=[moodle]Trong tab "Outputs" của stack CloudFormation.
	~[moodle]Trong phần "Resources" của stack CloudFormation.#<p>Phần "Resources" liệt kê các tài nguyên được tạo nhưng không cung cấp URL truy cập trực tiếp.</p>
	~[moodle]Trong nhật ký CloudWatch cho các máy ảo EC2.#<p>Nhật ký CloudWatch chứa nhật ký của ứng dụng và hệ điều hành, không phải URL truy cập chính.</p>
	####<p><strong>Giải thích</strong>: Sau khi tất cả các tài nguyên cần thiết đã được tạo, trạng thái sẽ thay đổi thành CREATE_COMPLETE. Trong tab "Outputs", bạn sẽ tìm thấy URL để cài đặt WordPress của mình.</p>
}

// question: 2.7  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi xem xét các máy ảo (EC2 instances) trong cơ sở hạ tầng WordPress được tạo tự động, tab "Monitoring" cung cấp thông tin gì?</p>{
	~[moodle]Chi tiết về các phiên bản hệ điều hành và gói phần mềm được cài đặt.#<p>Thông tin này thường được tìm thấy trong chi tiết AMI hoặc thông tin hệ điều hành của máy ảo.</p>
	=[moodle]Các biểu đồ về mức độ sử dụng tài nguyên của máy ảo như CPU.
	~[moodle]Danh sách các cặp khóa SSH được liên kết với máy ảo.#<p>Cặp khóa SSH được liên kết trong quá trình khởi chạy và được hiển thị trong chi tiết phiên bản.</p>
	~[moodle]Lịch sử của tất cả các thay đổi cấu hình được áp dụng cho máy ảo.#<p>Lịch sử thay đổi cấu hình được quản lý thông qua CloudFormation hoặc các công cụ cấu hình khác.</p>
	####<p><strong>Giải thích</strong>: Tab "Monitoring" hiển thị các biểu đồ về cách máy ảo của bạn được sử dụng, ví dụ: nếu CPU được sử dụng hơn 80%, đó có thể là lúc cần thêm một máy ảo khác.</p>
}

// question: 2.8  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Đối với cơ sở dữ liệu MySQL trong WordPress, tại sao bạn nên bật tính năng sao lưu tự động (automated snapshots) trong môi trường sản xuất?</p>{
	~[moodle]Để giảm chi phí lưu trữ dữ liệu cơ sở dữ liệu bằng cách xóa các bản sao lưu cũ.#<p>Sao lưu tự động sẽ phát sinh chi phí lưu trữ, không phải giảm chi phí.</p>
	=[moodle]Để đảm bảo có thể khôi phục cơ sở dữ liệu về một thời điểm cụ thể trong trường hợp lỗi.
	~[moodle]Để tự động tăng dung lượng lưu trữ của cơ sở dữ liệu khi cần.#<p>Tăng dung lượng lưu trữ được quản lý riêng biệt.</p>
	~[moodle]Để cải thiện hiệu suất đọc/ghi của cơ sở dữ liệu bằng cách phân phối tải.#<p>Cải thiện hiệu suất đọc/ghi thường liên quan đến loại phiên bản hoặc sao chép đọc.</p>
	####<p><strong>Giải thích</strong>: Việc bật sao lưu tự động cho phép bạn khôi phục cơ sở dữ liệu của mình về một thời điểm cụ thể.</p>
}

// question: 2.9  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Theo ví dụ WordPress, các tệp PHP, HTML, CSS và PNG được lưu trữ ở đâu để có thể truy cập từ tất cả các máy ảo?</p>{
	~[moodle]Trên ổ cứng cục bộ của mỗi máy ảo EC2.#<p>Lưu trữ cục bộ sẽ không cho phép chia sẻ giữa nhiều máy ảo.</p>
	~[moodle]Trong Amazon S3 dưới dạng các đối tượng tĩnh riêng lẻ.#<p>S3 có thể lưu trữ các tệp tĩnh nhưng không phải là một hệ thống tệp mạng để ứng dụng truy cập trực tiếp như EFS.</p>
	=[moodle]Trên Amazon Elastic File System (EFS), một hệ thống tệp mạng.
	~[moodle]Trong Amazon RDS như một phần của cơ sở dữ liệu MySQL.#<p>Cơ sở dữ liệu MySQL chỉ lưu trữ dữ liệu có cấu trúc, không phải các tệp ứng dụng.</p>
	####<p><strong>Giải thích</strong>: EFS được sử dụng để lưu trữ các tệp và truy cập chúng từ nhiều máy ảo. Tất cả các tệp thuộc về WordPress đều được lưu trữ trên EFS để có thể truy cập từ tất cả các máy ảo.</p>
}

// question: 2.10  name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Điều gì sẽ xảy ra với hóa đơn AWS của bạn nếu số lượng khách truy cập trang web WordPress của bạn tăng gấp năm lần trong một tháng?</p>{
	~[moodle]Hóa đơn sẽ vẫn giữ nguyên vì bạn đã trả phí cố định hàng tháng.#<p>AWS không tính phí cố định mà là trả theo mức sử dụng.</p>
	=[moodle]Hóa đơn sẽ tăng lên một cách tương ứng vì bạn phải trả tiền dựa trên mức sử dụng tài nguyên.
	~[moodle]Hóa đơn sẽ giảm xuống do hiệu ứng kinh tế theo quy mô của AWS.#<p>Mặc dù có lợi ích kinh tế theo quy mô, việc tăng cường sử dụng tài nguyên vẫn làm tăng chi phí.</p>
	~[moodle]Các dịch vụ AWS sẽ tự động ngừng hoạt động để tránh vượt quá giới hạn ngân sách.#<p>Các dịch vụ AWS sẽ mở rộng quy mô, không phải ngừng hoạt động, nhưng chi phí sẽ tăng lên.</p>
	####<p><strong>Giải thích</strong>: Hóa đơn AWS tương tự như hóa đơn tiền điện, các dịch vụ được lập hóa đơn dựa trên mức sử dụng. Nếu lưu lượng truy cập tăng, bạn sẽ phải trả nhiều tiền hơn cho các dịch vụ như CDN, máy chủ web và cơ sở dữ liệu.</p>
}

// Chapter 3: Using virtual machines: EC2

// question: 3.1  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi khởi chạy một máy ảo EC2, "Amazon Machine Image (AMI)" đóng vai trò gì?</p>{
	~[moodle]Nó là một thiết bị lưu trữ vật lý mà máy ảo sử dụng để lưu trữ dữ liệu.#<p>Lưu trữ vật lý được cung cấp bởi EBS hoặc instance store.</p>
	~[moodle]Nó là một bản ghi DNS công khai để truy cập máy ảo từ internet.#<p>DNS công khai là một phần của thông tin mạng, không phải AMI.</p>
	=[moodle]Nó là một bản mẫu đã được cấu hình sẵn, bao gồm hệ điều hành và phần mềm cài đặt sẵn.
	~[moodle]Nó là một tập hợp các quy tắc tường lửa để kiểm soát lưu lượng mạng của máy ảo.#<p>Quy tắc tường lửa được quản lý bằng các nhóm bảo mật.</p>
	####<p><strong>Giải thích</strong>: AMI là một bản mẫu được cấu hình sẵn, bao gồm hệ điều hành và phần mềm cài đặt sẵn cho máy ảo của bạn.</p>
}

// question: 3.2  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>"Instance type" trong EC2 chủ yếu mô tả điều gì về máy ảo?</p>{
	~[moodle]Phiên bản của hệ điều hành được cài đặt trên máy ảo.#<p>Phiên bản hệ điều hành là một phần của AMI.</p>
	=[moodle]Số lượng CPU ảo và dung lượng bộ nhớ của máy ảo.
	~[moodle]Vị trí địa lý của trung tâm dữ liệu mà máy ảo được đặt.#<p>Vị trí địa lý là khu vực (region) và vùng sẵn sàng (availability zone).</p>
	~[moodle]Tên của cặp khóa SSH được sử dụng để truy cập máy ảo.#<p>Cặp khóa SSH được sử dụng để xác thực truy cập, không phải mô tả loại instance.</p>
	####<p><strong>Giải thích</strong>: Một instance type chủ yếu mô tả số lượng CPU ảo và dung lượng bộ nhớ.</p>
}

// question: 3.3  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Loại instance nào sau đây được tối ưu hóa cho hiệu suất CPU cao và phù hợp cho các khối lượng công việc đòi hỏi nhiều tính toán?</p>{
	~[moodle]T family (ví dụ: t2.micro).#<p>T family là các loại instance rẻ, hiệu suất cơ bản vừa phải với khả năng tăng tốc hiệu suất CPU trong thời gian ngắn.</p>
	~[moodle]M family (ví dụ: m4.large).#<p>M family là các loại instance đa năng, có tỷ lệ CPU và bộ nhớ cân bằng.</p>
	=[moodle]C family (ví dụ: c4.large).
	~[moodle]R family (ví dụ: r4.large).#<p>R family được tối ưu hóa cho bộ nhớ, với nhiều bộ nhớ hơn công suất CPU.</p>
	####<p><strong>Giải thích</strong>: C family được tối ưu hóa cho tính toán, với hiệu suất CPU cao.</p>
}

// question: 3.4  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi nào bạn nên xem xét việc sử dụng "Spot Instances" cho máy ảo EC2 của mình?</p>{
	~[moodle]Cho các ứng dụng web quan trọng yêu cầu tính sẵn sàng cao và không bị gián đoạn.#<p>Các ứng dụng quan trọng cần độ tin cậy cao nên sử dụng On-demand hoặc Reserved Instances.</p>
	=[moodle]Cho các khối lượng công việc có thể chịu được sự gián đoạn và không yêu cầu thời gian chạy cụ thể, như xử lý hàng loạt.
	~[moodle]Cho các cơ sở dữ liệu quan hệ yêu cầu hiệu suất I/O liên tục và có thể dự đoán được.#<p>Cơ sở dữ liệu yêu cầu hiệu suất ổn định và có thể dự đoán được, không phù hợp với sự gián đoạn của Spot Instances.</p>
	~[moodle]Cho các máy chủ mail hoặc máy chủ DNS yêu cầu địa chỉ IP công khai cố định.#<p>Spot Instances có thể bị chấm dứt, không phù hợp với các dịch vụ yêu cầu địa chỉ IP cố định.</p>
	####<p><strong>Giải thích</strong>: Spot instances cho phép bạn đặt giá thầu cho dung lượng chưa sử dụng trong đám mây AWS với chiết khấu đáng kể. Bạn không nên sử dụng chúng cho các tác vụ như máy chủ web hoặc mail, nhưng có thể sử dụng chúng để chạy các tác vụ không đồng bộ như phân tích dữ liệu hoặc mã hóa tài sản truyền thông.</p>
}

// question: 3.5  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Để gán một địa chỉ IP công khai cố định cho một máy ảo EC2 để nó không thay đổi khi máy ảo được dừng và khởi động lại, dịch vụ nào của AWS được sử dụng?</p>{
	~[moodle]Amazon Virtual Private Cloud (VPC) để tạo mạng riêng.#<p>VPC là để tạo mạng riêng ảo.</p>
	~[moodle]Amazon EC2 Security Group để kiểm soát lưu lượng.#<p>Security Group là tường lửa ảo.</p>
	=[moodle]Elastic IP Address (EIP).
	~[moodle]Amazon Route 53 cho quản lý DNS.#<p>Route 53 là dịch vụ DNS.</p>
	####<p><strong>Giải thích</strong>: AWS cung cấp dịch vụ có tên Elastic IPs để cấp phát địa chỉ IP công khai cố định. Mỗi khi bạn khởi chạy hoặc dừng một máy ảo, địa chỉ IP công khai sẽ thay đổi, nhưng EIP khắc phục điều này.</p>
}

// question: 3.6  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi bạn cần tăng sức mạnh tính toán hoặc bộ nhớ của một máy ảo EC2 đang chạy, bạn có thể làm gì?</p>{
	~[moodle]Tạo một cặp khóa SSH mới và kết nối lại với máy ảo.#<p>Cặp khóa SSH không ảnh hưởng đến sức mạnh tính toán.</p>
	=[moodle]Thay đổi "Instance type" của máy ảo.
	~[moodle]Cài đặt lại hệ điều hành của máy ảo thông qua một AMI mới.#<p>Cài đặt lại hệ điều hành sẽ xóa dữ liệu và không trực tiếp tăng sức mạnh.</p>
	~[moodle]Đính kèm thêm một địa chỉ IP công khai Elastic IP.#<p>Thêm EIP không tăng sức mạnh tính toán mà chỉ cung cấp địa chỉ IP cố định.</p>
	####<p><strong>Giải thích</strong>: Luôn có thể thay đổi kích thước của một máy ảo. Đây là một trong những lợi thế của việc sử dụng đám mây và nó mang lại cho bạn khả năng mở rộng theo chiều dọc. Nếu bạn cần nhiều sức mạnh tính toán hơn, hãy tăng kích thước của instance EC2.</p>
}

// question: 3.7  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Các trung tâm dữ liệu của AWS được nhóm thành các khu vực (regions). Khi quyết định chọn khu vực nào cho cơ sở hạ tầng đám mây của bạn, yếu tố "Latency" (độ trễ) đề cập đến điều gì?</p>{
	~[moodle]Chi phí lưu trữ dữ liệu trong khu vực đó.#<p>Chi phí dịch vụ có thể khác nhau giữa các khu vực, nhưng đây không phải là độ trễ.</p>
	~[moodle]Các quy định bảo vệ dữ liệu phải tuân thủ trong khu vực.#<p>Các quy định là yếu tố "Compliance".</p>
	=[moodle]Khoảng cách ngắn nhất giữa người dùng và cơ sở hạ tầng của bạn.
	~[moodle]Số lượng dịch vụ AWS có sẵn trong khu vực.#<p>Số lượng dịch vụ có sẵn là yếu tố "Service availability".</p>
	####<p><strong>Giải thích</strong>: Độ trễ là một tiêu chí quan trọng khi chọn khu vực, đề cập đến khu vực nào cung cấp khoảng cách ngắn nhất giữa người dùng và cơ sở hạ tầng của bạn.</p>
}

// question: 3.8  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Để kiểm tra các bản cập nhật bảo mật của phần mềm trên máy ảo EC2 chạy Amazon Linux, lệnh nào sau đây thường được sử dụng?</p>{
	~[moodle]apt-get update --security.#<p>apt-get được sử dụng trên các hệ điều hành dựa trên Debian/Ubuntu.</p>
	=[moodle]yum -y --security update.
	~[moodle]sudo systemctl restart --security.#<p>systemctl restart dùng để khởi động lại dịch vụ.</p>
	~[moodle]ps aux --security.#<p>ps aux dùng để liệt kê các tiến trình đang chạy.</p>
	####<p><strong>Giải thích</strong>: Đối với các máy ảo chạy Amazon Linux (dựa trên Red Hat Enterprise Linux), lệnh yum -y --security update được sử dụng để cài đặt các bản cập nhật bảo mật.</p>
}

// question: 3.9  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi gỡ lỗi một máy ảo EC2, bạn có thể xem các thông báo nhật ký hệ thống (system logs) mà bình thường sẽ hiển thị trên màn hình vật lý trong quá trình khởi động bằng cách nào?</p>{
	~[moodle]Kết nối SSH vào máy ảo và chạy journalctl -f.#<p>Lệnh này yêu cầu truy cập SSH và thường xem nhật ký trực tiếp, không phải nhật ký khởi động hệ thống như được hiển thị trong bảng điều khiển.</p>
	=[moodle]Truy cập EC2 Management Console, chọn phiên bản, và chọn Instance Settings > Get System Log.
	~[moodle]Chạy lệnh aws ec2 describe-instances --logs từ AWS CLI.#<p>Không có tùy chọn describe-instances --logs trong AWS CLI để xem nhật ký hệ thống trực tiếp như vậy.</p>
	~[moodle]Kiểm tra nhật ký CloudWatch cho máy ảo với các bộ lọc đặc biệt.#<p>CloudWatch có thể thu thập nhật ký, nhưng Get System Log là một tính năng cụ thể để xem nhật ký khởi động của máy ảo.</p>
	####<p><strong>Giải thích</strong>: Để xem nhật ký hệ thống của máy ảo, bạn có thể mở EC2 Management Console, chọn phiên bản đang chạy, và chọn Actions > Instance Settings > Get System Log.</p>
}

// question: 3.10  name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi một máy ảo EC2 được "terminated" (chấm dứt), điều gì xảy ra với nó?</p>{
	~[moodle]Máy ảo được dừng nhưng vẫn giữ lại tất cả dữ liệu và địa chỉ IP công cộng.#<p>Việc dừng máy ảo giữ lại dữ liệu nhưng không phải địa chỉ IP công cộng, việc chấm dứt sẽ xóa dữ liệu trên instance store và không giữ địa chỉ IP.</p>
	=[moodle]Máy ảo được tắt và không còn khả dụng, cuối cùng biến mất khỏi danh sách các máy ảo.
	~[moodle]Máy ảo được đặt vào trạng thái chờ và có thể được khởi động lại ngay lập tức mà không mất dữ liệu.#<p>Trạng thái chờ không áp dụng cho việc chấm dứt.</p>
	~[moodle]Máy ảo được tự động thay thế bằng một máy ảo mới có cùng cấu hình.#<p>Điều này có thể xảy ra với Auto Scaling Group, nhưng không phải là hành vi mặc định khi chấm dứt một instance EC2 đơn lẻ.</p>
	####<p><strong>Giải thích</strong>: Sau khi bạn chấm dứt một máy ảo, nó không còn khả dụng và cuối cùng biến mất khỏi danh sách các máy ảo.</p>
}

// Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation

// question: 4.1  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>"Infrastructure as Code" (Cơ sở hạ tầng dưới dạng Mã) là ý tưởng sử dụng ngôn ngữ lập trình cấp cao để kiểm soát điều gì?</p>{
	~[moodle]Các quy trình triển khai phần mềm và kiểm thử tự động.#<p>Đây là một phần của quy trình phát triển phần mềm, nhưng "Infrastructure as Code" tập trung vào cơ sở hạ tầng.</p>
	=[moodle]Cơ sở hạ tầng điện toán, bao gồm cấu trúc mạng, bộ cân bằng tải và mục nhập DNS.
	~[moodle]Việc quản lý các nhóm phát triển và vận hành trong một công ty.#<p>Quản lý đội nhóm không liên quan trực tiếp đến "Infrastructure as Code".</p>
	~[moodle]Tối ưu hóa hiệu suất của các ứng dụng chạy trên máy ảo EC2.#<p>Mặc dù IaC có thể gián tiếp cải thiện hiệu suất, mục tiêu chính là quản lý cơ sở hạ tầng.</p>
	####<p><strong>Giải thích</strong>: Infrastructure as Code là ý tưởng sử dụng ngôn ngữ lập trình cấp cao để kiểm soát cơ sở hạ tầng. Cơ sở hạ tầng có thể là bất kỳ tài nguyên AWS nào, như cấu trúc mạng, bộ cân bằng tải, mục nhập DNS, v.v..</p>
}

// question: 4.2  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>Trong bối cảnh AWS, API REST được truy cập qua giao thức HTTPS đóng vai trò gì?</p>{
	~[moodle]Nó là một giao diện đồ họa người dùng để quản lý các dịch vụ AWS.#<p>AWS Management Console là giao diện đồ họa.</p>
	~[moodle]Nó là một bộ công cụ phát triển phần mềm để xây dựng các ứng dụng phía máy khách.#<p>SDKs là bộ công cụ phát triển phần mềm.</p>
	=[moodle]Nó là nền tảng cơ bản cho tất cả các công cụ khác của AWS (CLI, SDK, CloudFormation) để kiểm soát mọi phần của AWS.
	~[moodle]Nó là một cơ sở dữ liệu NoSQL phân tán được sử dụng để lưu trữ dữ liệu ứng dụng.#<p>DynamoDB là cơ sở dữ liệu NoSQL.</p>
	####<p><strong>Giải thích</strong>: Trên AWS, mọi thứ đều có thể được kiểm soát thông qua API. Bạn tương tác với AWS bằng cách gọi API REST sử dụng giao thức HTTPS. API là nền tảng của tất cả các công cụ đó (CLI, SDK, CloudFormation).</p>
}

// question: 4.3  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>Lợi ích chính của việc tự động hóa cơ sở hạ tầng bằng script hoặc bản thiết kế (blueprint) thay vì sử dụng AWS Management Console là gì?</p>{
	~[moodle]Tăng cường khả năng kiểm soát thủ công đối với từng tài nguyên riêng lẻ.#<p>Tự động hóa giảm kiểm soát thủ công.</p>
	=[moodle]Giúp tiết kiệm thời gian về lâu dài và cho phép xây dựng cơ sở hạ tầng mới nhanh chóng với các module sẵn có.
	~[moodle]Loại bỏ hoàn toàn nhu cầu về kỹ năng lập trình và kiến thức về AWS CLI/SDK.#<p>Tự động hóa bằng script/blueprint yêu cầu kỹ năng lập trình và kiến thức về CLI/SDK.</p>
	~[moodle]Đảm bảo rằng tất cả các lỗi được phát hiện và sửa chữa tự động mà không cần can thiệp của con người.#<p>Tự động hóa giảm lỗi con người nhưng không loại bỏ hoàn toàn, và vẫn cần giám sát.</p>
	####<p><strong>Giải thích</strong>: Một script hoặc bản thiết kế có thể được tái sử dụng và sẽ giúp bạn tiết kiệm thời gian về lâu dài. Bạn có thể xây dựng cơ sở hạ tầng mới nhanh chóng với các module sẵn sàng sử dụng từ các dự án trước đây của mình.</p>
}

// question: 4.4  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>Khi sử dụng AWS CLI, tùy chọn --query với JMESPath có mục đích gì?</p>{
	~[moodle]Để xác định loại dịch vụ AWS mà lệnh sẽ tương tác.#<p>Đây là các phần của cấu trúc lệnh CLI cơ bản.</p>
	~[moodle]Để chỉ định các giá trị cho các tham số đầu vào của lệnh.#<p>Đây là các phần của cấu trúc lệnh CLI cơ bản.</p>
	=[moodle]Để trích xuất và lọc dữ liệu cụ thể từ kết quả JSON trả về của lệnh.
	~[moodle]Để định cấu hình thông tin xác thực cho người dùng AWS CLI.#<p>Cấu hình thông tin xác thực được thực hiện bằng lệnh aws configure.</p>
	####<p><strong>Giải thích</strong>: Tùy chọn --query sử dụng JMESPath, một ngôn ngữ truy vấn cho JSON, để trích xuất dữ liệu từ kết quả. Điều này hữu ích vì thường bạn chỉ cần một trường cụ thể từ kết quả.</p>
}

// question: 4.5  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>Khi sử dụng AWS SDK để tương tác với AWS API, SDK chịu trách nhiệm xử lý những việc gì?</p>{
	~[moodle]Tạo mã ứng dụng logic và giao diện người dùng cho ứng dụng của bạn.#<p>Đây là những trách nhiệm của nhà phát triển ứng dụng hoặc người quản trị hệ thống, không phải của SDK.</p>
	~[moodle]Quản lý việc cài đặt và cấu hình hệ điều hành trên máy ảo.#<p>Đây là những trách nhiệm của nhà phát triển ứng dụng hoặc người quản trị hệ thống, không phải của SDK.</p>
	=[moodle]Xác thực, thử lại khi lỗi, giao tiếp HTTPS và (de)serialization XML hoặc JSON.
	~[moodle]Thiết kế kiến trúc cơ sở dữ liệu và truy vấn SQL cho ứng dụng.#<p>Đây là những trách nhiệm của nhà phát triển ứng dụng hoặc người quản trị hệ thống, không phải của SDK.</p>
	####<p><strong>Giải thích</strong>: AWS SDK là một cách thuận tiện để gọi AWS API từ ngôn ngữ lập trình yêu thích của bạn. SDK xử lý các vấn đề như xác thực, thử lại khi lỗi, giao tiếp HTTPS và (de)serialization XML hoặc JSON.</p>
}

// question: 4.6  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>Mục đích chính của "AWS CloudFormation" là gì trong việc quản lý cơ sở hạ tầng AWS?</p>{
	~[moodle]Thực thi các script tùy chỉnh trên các máy ảo EC2 đã chạy để cài đặt phần mềm.#<p>Đây có thể là một phần của UserData trong CloudFormation, nhưng không phải là mục đích chính của CloudFormation.</p>
	~[moodle]Triển khai các ứng dụng web đơn giản vào các môi trường runtime được tiêu chuẩn hóa.#<p>Đây là chức năng của AWS Elastic Beanstalk.</p>
	=[moodle]Mô tả trạng thái mong muốn của cơ sở hạ tầng bằng các mẫu JSON hoặc YAML và tự động đạt được trạng thái đó.
	~[moodle]Cung cấp một giao diện web đồ họa để quản lý tất cả các dịch vụ AWS thủ công.#<p>Đây là chức năng của AWS Management Console.</p>
	####<p><strong>Giải thích</strong>: CloudFormation dựa trên các mẫu, là mô tả về cơ sở hạ tầng của bạn, được viết bằng JSON hoặc YAML, có thể được CloudFormation diễn giải. Nó sử dụng cách tiếp cận khai báo để bạn chỉ cần nói cho CloudFormation biết cơ sở hạ tầng của bạn nên trông như thế nào.</p>
}

// question: 4.7  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>Lợi ích nào sau đây không phải là một trong những lợi ích chính của việc sử dụng CloudFormation?</p>{
	~[moodle]Khả năng xử lý các phụ thuộc giữa các tài nguyên AWS một cách tự động.#<p>Đây là một lợi ích quan trọng của CloudFormation, giúp tăng độ tin cậy, hiệu quả và tính nhất quán.</p>
	~[moodle]Giảm thiểu lỗi của con người trong quá trình triển khai cơ sở hạ tầng.#<p>Đây là một lợi ích quan trọng của CloudFormation, giúp tăng độ tin cậy, hiệu quả và tính nhất quán.</p>
	~[moodle]Cung cấp một cách nhất quán để mô tả cơ sở hạ tầng trên AWS.#<p>Đây là một lợi ích quan trọng của CloudFormation, giúp tăng độ tin cậy, hiệu quả và tính nhất quán.</p>
	=[moodle]Yêu cầu trả phí bổ sung cho mỗi stack CloudFormation đang chạy.
	####<p><strong>Giải thích</strong>: Việc sử dụng CloudFormation không mất thêm phí. Nếu bạn đăng ký gói hỗ trợ AWS, bạn cũng nhận được hỗ trợ cho CloudFormation.</p>
}

// question: 4.8  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>Trong một mẫu CloudFormation, phần "Resources" được sử dụng để định nghĩa những gì?</p>{
	~[moodle]Các giá trị tham số tùy chỉnh mà người dùng cung cấp khi tạo stack.#<p>Các giá trị tham số được định nghĩa trong phần "Parameters".</p>
	~[moodle]Mô tả ngắn gọn về mục đích tổng thể của mẫu.#<p>Mô tả tổng thể được định nghĩa trong phần "Description".</p>
	=[moodle]Các tài nguyên AWS nhỏ nhất có thể được mô tả, ví dụ như một máy ảo hoặc một bộ cân bằng tải.
	~[moodle]Các giá trị đầu ra được trả về từ mẫu sau khi stack được tạo thành công.#<p>Các giá trị đầu ra được định nghĩa trong phần "Outputs".</p>
	####<p><strong>Giải thích</strong>: Một resource là khối nhỏ nhất bạn có thể mô tả. Ví dụ là một máy ảo, một bộ cân bằng tải hoặc một địa chỉ IP Elastic.</p>
}

// question: 4.9  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>Khi cập nhật một stack CloudFormation, CloudFormation sẽ xác định điều gì để áp dụng các thay đổi?</p>{
	~[moodle]CloudFormation yêu cầu bạn chỉ định một danh sách các hành động API cần được thực hiện.#<p>Điều này ngược lại với cách tiếp cận khai báo của CloudFormation.</p>
	~[moodle]CloudFormation tự động đoán xem bạn muốn thay đổi gì mà không cần mẫu cập nhật.#<p>Điều này ngược lại với cách tiếp cận khai báo của CloudFormation.</p>
	=[moodle]CloudFormation so sánh mẫu đã cập nhật với trạng thái hiện tại của cơ sở hạ tầng và tính toán các bước cần thiết.
	~[moodle]CloudFormation luôn xóa toàn bộ cơ sở hạ tầng hiện có và tạo lại từ mẫu mới.#<p>CloudFormation cố gắng cập nhật mà không cần xóa và tạo lại toàn bộ để giảm thiểu gián đoạn.</p>
	####<p><strong>Giải thích</strong>: CloudFormation hỗ trợ cập nhật cơ sở hạ tầng của bạn. Nó sẽ tìm ra các phần của mẫu đã thay đổi và áp dụng các thay đổi đó một cách suôn sẻ nhất có thể cho cơ sở hạ tầng của bạn.</p>
}

// question: 4.10  name: Chapter 4: Programming your infrastructure: The command-line, SDKs, and CloudFormation
::Chapter 4\: Programming your infrastructure: The command-line, SDKs, and CloudFormation::[html]<p>Khi sử dụng hàm nội tại !Sub trong CloudFormation, điều gì xảy ra với các tham chiếu nằm trong \$\{\}?</p>{
	~[moodle]Các tham chiếu này bị bỏ qua và không được xử lý.#<p>Mục đích của !Sub là để thay thế các tham chiếu.</p>
	=[moodle]Các tham chiếu được thay thế bằng giá trị thực của chúng.
	~[moodle]Các tham chiếu được mã hóa Base64 trước khi sử dụng.#<p>Hàm !Base64 được sử dụng để mã hóa Base64.</p>
	~[moodle]Các tham chiếu chỉ được sử dụng cho mục đích ghi nhật ký và không ảnh hưởng đến cấu hình.#<p>Các tham chiếu là để cấu hình, không chỉ ghi nhật ký.</p>
	####<p><strong>Giải thích</strong>: Với !Sub, tất cả các tham chiếu trong \$\{\} được thay thế bằng giá trị thực của chúng.</p>
}

// Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks

// question: 5.1  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Khi bạn muốn tận dụng các tính năng của đám mây như mở rộng số lượng máy dựa trên tải hiện tại, điều gì là cần thiết cho quy trình triển khai phần mềm của bạn?</p>{
	~[moodle]Thực hiện triển khai thủ công từng máy ảo để có kiểm soát chi tiết.#<p>Triển khai thủ công trở nên không thể khi số lượng máy ảo tăng.</p>
	=[moodle]Tự động hóa quy trình triển khai ứng dụng.
	~[moodle]Giới hạn số lượng máy ảo tối đa để đảm bảo ổn định.#<p>Hạn chế số lượng máy ảo sẽ hạn chế khả năng mở rộng.</p>
	~[moodle]Chuyển đổi tất cả các ứng dụng sang kiến trúc monolithic.#<p>Kiến trúc microservices thường được ưu tiên trong môi trường đám mây linh hoạt.</p>
	####<p><strong>Giải thích</strong>: Đầu tư vào một quy trình triển khai tự động sẽ mang lại lợi ích trong tương lai bằng cách tăng hiệu quả và giảm lỗi của con người, đặc biệt khi bạn cần khởi động các máy ảo mới nhiều lần trong ngày để tận dụng khả năng mở rộng của đám mây.</p>
}

// question: 5.2  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Dịch vụ nào của AWS được mô tả là phù hợp nhất để triển khai các ứng dụng web phổ biến (như PHP, Node.js, Java) với nỗ lực thấp và quản lý môi trường runtime tự động?</p>{
	~[moodle]AWS OpsWorks Stacks.#<p>OpsWorks phù hợp cho các ứng dụng đa tầng và có nhiều tùy chỉnh hơn với Chef.</p>
	~[moodle]AWS CloudFormation với các script khởi động tùy chỉnh.#<p>CloudFormation với script cung cấp nhiều quyền kiểm soát nhất nhưng đòi hỏi nhiều công sức hơn.</p>
	=[moodle]AWS Elastic Beanstalk.
	~[moodle]AWS Lambda.#<p>Lambda là dịch vụ serverless cho các hàm, không phải môi trường runtime hoàn chỉnh cho ứng dụng web.</p>
	####<p><strong>Giải thích</strong>: AWS Elastic Beanstalk giúp bạn triển khai các ứng dụng web dựa trên nhiều ngôn ngữ. Với Elastic Beanstalk, bạn chỉ cần xử lý ứng dụng của mình, còn hệ điều hành và môi trường runtime được AWS quản lý.</p>
}

// question: 5.3  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Điều gì xảy ra khi bạn đóng gói một shell script vào "user data" của một máy ảo EC2 trong CloudFormation?</p>{
	~[moodle]Script sẽ được lưu trữ dưới dạng một đối tượng trên Amazon S3 và được tải xuống khi cần.#<p>User data được truyền trực tiếp khi khởi chạy phiên bản, mặc dù nó có thể fetch script từ S3.</p>
	=[moodle]Script sẽ được thực thi tự động ở cuối quá trình khởi động của máy ảo.
	~[moodle]Script sẽ được chạy dưới dạng một hàm Lambda riêng biệt trên AWS.#<p>User data chạy trên máy ảo, không phải dưới dạng hàm Lambda.</p>
	~[moodle]Script sẽ được sử dụng để tạo một AMI tùy chỉnh mới cho máy ảo.#<p>AMI được tạo từ một phiên bản hiện có hoặc là một bản mẫu độc lập.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể sử dụng user data để thực thi một script ngay sau khi máy ảo khởi động. User data là một phần của EC2 instance và sẽ được chạy tự động.</p>
}

// question: 5.4  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Để triển khai một ứng dụng đa tầng phức tạp, ví dụ như ứng dụng chat IRC với máy khách web và máy chủ IRC, dịch vụ nào của AWS sẽ cung cấp sự linh hoạt cao hơn so với Elastic Beanstalk?</p>{
	~[moodle]AWS CloudFormation với user data scripts.#<p>CloudFormation với user data scripts cung cấp nhiều quyền kiểm soát nhất nhưng đòi hỏi nhiều công sức hơn.</p>
	=[moodle]AWS OpsWorks Stacks.
	~[moodle]Amazon Lightsail.#<p>Lightsail là một dịch vụ đơn giản hóa cho các ứng dụng cơ bản.</p>
	~[moodle]Amazon EC2 Container Service (ECS).#<p>ECS là một dịch vụ quản lý container, không được đề cập trong so sánh trực tiếp này.</p>
	####<p><strong>Giải thích</strong>: Nếu bạn phải triển khai một ứng dụng phức tạp hơn bao gồm các dịch vụ khác nhau - còn gọi là các layer - bạn sẽ gặp giới hạn của AWS Elastic Beanstalk. AWS OpsWorks Stacks có thể giúp bạn triển khai một ứng dụng đa tầng.</p>
}

// question: 5.5  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Trong AWS Elastic Beanstalk, "Application Version" (Phiên bản Ứng dụng) chứa gì?</p>{
	~[moodle]Cấu hình mặc định cho môi trường runtime của ứng dụng.#<p>Cấu hình mặc định nằm trong "Configuration template".</p>
	=[moodle]Một bản phát hành cụ thể của ứng dụng của bạn, được đóng gói vào một kho lưu trữ trên Amazon S3.
	~[moodle]Một tập hợp các máy ảo EC2 chạy ứng dụng của bạn.#<p>Tập hợp máy ảo nằm trong "Environment".</p>
	~[moodle]Các quy tắc tường lửa và cấu hình mạng cho ứng dụng.#<p>Quy tắc tường lửa được quản lý bởi Security Groups.</p>
	####<p><strong>Giải thích</strong>: Một version chứa một bản phát hành cụ thể của ứng dụng của bạn. Để tạo một phiên bản mới, bạn phải tải lên các tệp thực thi của mình (được đóng gói vào một kho lưu trữ) lên Amazon S3.</p>
}

// question: 5.6  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Khi triển khai OpenSwan VPN server trên EC2 bằng CloudFormation, script cài đặt và cấu hình VPN server thực sự nằm ở đâu?</p>{
	~[moodle]Trực tiếp trong template CloudFormation dưới dạng mã YAML dài.#<p>Mặc dù user data được định nghĩa trong template, nhưng thường sẽ fetch một script bên ngoài để giữ template sạch sẽ.</p>
	=[moodle]Trong một script shell riêng biệt được fetch và thực thi bởi user data.
	~[moodle]Được cài đặt tự động bởi AWS mà không cần script tùy chỉnh nào.#<p>Cần có script tùy chỉnh để cài đặt OpenSwan.</p>
	~[moodle]Trong một AMI tùy chỉnh có OpenSwan được cài đặt sẵn.#<p>Mặc dù có thể tạo AMI tùy chỉnh, ví dụ này minh họa cách sử dụng user data với AMI tiêu chuẩn.</p>
	####<p><strong>Giải thích</strong>: User data chứa một script nhỏ để fetch và thực thi script thực sự, vpn-setup.sh, chứa tất cả các lệnh để cài đặt các tệp thực thi và cấu hình dịch vụ. Điều này giúp bạn không phải chèn các script phức tạp vào mẫu CloudFormation.</p>
}

// question: 5.7  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Điều gì cho phép AWS OpsWorks Stacks kiểm soát việc triển khai ứng dụng, mở rộng quy mô, giám sát và cập nhật các máy ảo?</p>{
	~[moodle]Việc sử dụng các Docker container được quản lý hoàn toàn.#<p>OpsWorks hỗ trợ Docker nhưng không phải là nền tảng container chính.</p>
	=[moodle]Một công cụ quản lý cấu hình gọi là Chef, sử dụng các recipe và cookbook.
	~[moodle]Một giao diện lập trình ứng dụng (API) độc quyền mà người dùng phải học.#<p>OpsWorks sử dụng Chef, một công cụ phổ biến.</p>
	~[moodle]Tích hợp chặt chẽ với các dịch vụ mạng vật lý của AWS.#<p>OpsWorks hoạt động ở cấp độ phần mềm và cấu hình, không phải ở cấp độ mạng vật lý.</p>
	####<p><strong>Giải thích</strong>: Việc triển khai được kiểm soát bằng Chef, một công cụ quản lý cấu hình. Chef sử dụng các recipe được tổ chức thành cookbook để triển khai ứng dụng cho bất kỳ loại hệ thống nào.</p>
}

// question: 5.8  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Trong AWS OpsWorks Stacks, "Layer" (Tầng) đại diện cho điều gì?</p>{
	~[moodle]Một bản sao lưu hoàn chỉnh của toàn bộ cơ sở hạ tầng của bạn.#<p>Layer không phải là bản sao lưu.</p>
	=[moodle]Một ứng dụng hoặc dịch vụ cụ thể, có thể bao gồm một hoặc nhiều máy ảo.
	~[moodle]Một bộ sưu tập các IAM role được sử dụng để quản lý quyền truy cập.#<p>IAM role là các thành phần bảo mật riêng biệt.</p>
	~[moodle]Một chính sách mở rộng quy mô tự động dựa trên các chỉ số hiệu suất.#<p>Chính sách mở rộng quy mô là một phần của việc quản lý instance trong layer, không phải layer đó.</p>
	####<p><strong>Giải thích</strong>: Một layer thuộc về một stack. Một layer đại diện cho một ứng dụng; bạn cũng có thể gọi nó là một dịch vụ. AWS OpsWorks Stacks cung cấp các layer định sẵn cho các ứng dụng web tiêu chuẩn.</p>
}

// question: 5.9  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Theo so sánh, dịch vụ triển khai nào của AWS mang lại quyền kiểm soát cao nhất cho người dùng khi triển khai các ứng dụng phức tạp?</p>{
	~[moodle]AWS Elastic Beanstalk do tính đơn giản và môi trường chuẩn hóa.#<p>Elastic Beanstalk dễ sử dụng nhưng ít linh hoạt hơn.</p>
	~[moodle]AWS OpsWorks Stacks do sử dụng Chef recipes và các layer tùy chỉnh.#<p>OpsWorks linh hoạt hơn Elastic Beanstalk nhưng vẫn có một số ràng buộc của Chef.</p>
	=[moodle]AWS CloudFormation với các script khởi động tùy chỉnh trên máy ảo.
	~[moodle]AWS CodeDeploy để tự động hóa việc triển khai mã.#<p>CodeDeploy là một công cụ triển khai mã, không phải là công cụ triển khai cơ sở hạ tầng hoàn chỉnh.</p>
	####<p><strong>Giải thích</strong>: CloudFormation với việc triển khai ứng dụng bằng script khởi động mang lại quyền kiểm soát cao nhất, vì bạn có thể triển khai bất kỳ ứng dụng nào và tinh chỉnh mọi chi tiết.</p>
}

// question: 5.10  name: Chapter 5: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks
::Chapter 5\: Automating deployment: CloudFormation, Elastic Beanstalk, and OpsWorks::[html]<p>Khi nào bạn nên tạo một "Custom Layer" (Tầng Tùy chỉnh) trong AWS OpsWorks Stacks?</p>{
	~[moodle]Khi ứng dụng của bạn là một ứng dụng web tiêu chuẩn như PHP hoặc Java.#<p>Các ứng dụng web tiêu chuẩn có các layer định sẵn trong OpsWorks.</p>
	~[moodle]Khi ứng dụng của bạn yêu cầu một máy ảo EC2 duy nhất không cần chia sẻ tài nguyên.#<p>Layer có thể chứa nhiều instance.</p>
	=[moodle]Khi ứng dụng của bạn không phù hợp với các loại layer tiêu chuẩn được cung cấp bởi OpsWorks Stacks.
	~[moodle]Khi bạn muốn sử dụng Docker container thay vì máy ảo truyền thống.#<p>OpsWorks có layer Docker, nhưng custom layer được dùng khi không có layer tiêu chuẩn nào phù hợp.</p>
	####<p><strong>Giải thích</strong>: Một IRC server không phải là một ứng dụng web điển hình, vì vậy các loại layer tiêu chuẩn không phù hợp. Bạn sẽ sử dụng một custom layer để triển khai một IRC server.</p>
}

// Chapter 6: Securing your system: IAM, security groups, and VPC

// question: 6.1  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>Theo mô hình trách nhiệm chung của AWS, ai chịu trách nhiệm về "bảo mật trong đám mây" (security of the cloud)?</p>{
	~[moodle]Khách hàng, chịu trách nhiệm cho tất cả các khía cạnh bảo mật của ứng dụng và dữ liệu.#<p>Khách hàng chịu trách nhiệm về "bảo mật trong đám mây" (security in the cloud), tức là cấu hình hệ điều hành, nền tảng, ứng dụng, dữ liệu và cấu hình mạng.</p>
	=[moodle]AWS, chịu trách nhiệm bảo vệ cơ sở hạ tầng chạy tất cả các dịch vụ đám mây.
	~[moodle]Một nhà cung cấp dịch vụ bên thứ ba được khách hàng thuê để quản lý bảo mật.#<p>Nhà cung cấp bên thứ ba có thể hỗ trợ, nhưng trách nhiệm chính vẫn được chia sẻ giữa AWS và khách hàng.</p>
	~[moodle]Hệ điều hành trên máy ảo, tự động cài đặt các bản cập nhật bảo mật cần thiết.#<p>Hệ điều hành là trách nhiệm của khách hàng trong mô hình IaaS.</p>
	####<p><strong>Giải thích</strong>: AWS chịu trách nhiệm về "bảo mật trong đám mây", tức là bảo vệ cơ sở hạ tầng chạy tất cả các dịch vụ đám mây.</p>
}

// question: 6.2  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>"AWS Identity and Access Management (IAM)" cung cấp chức năng chính nào cho tài khoản AWS của bạn?</p>{
	~[moodle]Giám sát hiệu suất của các dịch vụ AWS và gửi cảnh báo khi ngưỡng bị vi phạm.#<p>Giám sát hiệu suất là chức năng của CloudWatch.</p>
	=[moodle]Xác thực và ủy quyền cho API của AWS, kiểm soát ai có thể làm gì trong tài khoản của bạn.
	~[moodle]Tự động mở rộng quy mô tài nguyên AWS dựa trên tải ứng dụng.#<p>Tự động mở rộng quy mô là chức năng của Auto Scaling.</p>
	~[moodle]Mã hóa tất cả dữ liệu được lưu trữ trong các dịch vụ AWS theo mặc định.#<p>Mã hóa được cấu hình cho từng dịch vụ và không phải là chức năng mặc định của IAM.</p>
	####<p><strong>Giải thích</strong>: IAM cung cấp xác thực và ủy quyền cho API của AWS. Khi bạn gửi yêu cầu đến API của AWS, IAM xác minh danh tính của bạn và kiểm tra xem bạn có được phép thực hiện hành động đó hay không.</p>
}

// question: 6.3  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>Trong một chính sách IAM (IAM policy), điều gì sẽ xảy ra nếu có nhiều statement áp dụng cho cùng một hành động và một statement Deny xung đột với một statement Allow?</p>{
	~[moodle]Statement Allow sẽ được ưu tiên và hành động sẽ được cho phép.#<p>Điều này ngược lại với quy tắc của IAM.</p>
	=[moodle]Statement Deny sẽ được ưu tiên và hành động sẽ bị từ chối.
	~[moodle]IAM sẽ yêu cầu người dùng xác nhận hành động một lần nữa.#<p>IAM không yêu cầu xác nhận trong trường hợp này.</p>
	~[moodle]Chính sách IAM sẽ bị coi là không hợp lệ và không được áp dụng.#<p>IAM không coi chính sách không hợp lệ trong trường hợp này.</p>
	####<p><strong>Giải thích</strong>: Nếu bạn có nhiều statement áp dụng cho cùng một hành động, Deny sẽ ghi đè Allow.</p>
}

// question: 6.4  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>Khi nào bạn nên sử dụng "IAM role" (Vai trò IAM) thay vì "IAM user" (Người dùng IAM) để xác thực các tài nguyên AWS như các phiên bản EC2?</p>{
	~[moodle]Khi bạn cần cấp quyền truy cập lâu dài cho một cá nhân để quản lý tài khoản AWS.#<p>Người dùng IAM có quyền truy cập lâu dài cho cá nhân.</p>
	=[moodle]Khi một ứng dụng hoặc dịch vụ AWS cần truy cập vào các dịch vụ AWS khác một cách an toàn.
	~[moodle]Khi bạn muốn tạo một cặp khóa truy cập tĩnh để sử dụng với AWS CLI.#<p>IAM user có khóa truy cập tĩnh, nhưng vai trò IAM được ưu tiên cho tài nguyên.</p>
	~[moodle]Khi bạn cần đăng nhập vào AWS Management Console bằng mật khẩu.#<p>Người dùng root hoặc người dùng IAM có mật khẩu để đăng nhập vào bảng điều khiển.</p>
	####<p><strong>Giải thích</strong>: Thay vì sử dụng một người dùng IAM để xác thực, bạn nên sử dụng một vai trò IAM bất cứ khi nào bạn cần xác thực các tài nguyên AWS như các phiên bản EC2. Khi sử dụng vai trò IAM, khóa truy cập của bạn được tự động tiêm vào phiên bản EC2 của bạn.</p>
}

// question: 6.5  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>Để kiểm soát lưu lượng mạng đến và đi từ các phiên bản EC2 của bạn, AWS Security Groups sử dụng những gì làm cơ sở để cho phép hoặc từ chối lưu lượng?</p>{
	~[moodle]Dựa trên ID phiên bản EC2 hoặc tên AMI.#<p>Các yếu tố này không được sử dụng trực tiếp để định nghĩa quy tắc trong Security Group.</p>
	=[moodle]Dựa trên hướng (inbound/outbound), giao thức IP, cổng và nguồn/đích (địa chỉ IP hoặc nhóm bảo mật).
	~[moodle]Dựa trên số lượng CPU và dung lượng bộ nhớ của phiên bản EC2.#<p>Số lượng CPU và bộ nhớ không liên quan đến quy tắc Security Group.</p>
	~[moodle]Dựa trên ngôn ngữ lập trình được sử dụng bởi ứng dụng đang chạy trên phiên bản.#<p>Ngôn ngữ lập trình không liên quan đến quy tắc Security Group.</p>
	####<p><strong>Giải thích</strong>: Một nhóm bảo mật bao gồm một tập hợp các quy tắc. Mỗi quy tắc cho phép lưu lượng mạng dựa trên hướng (inbound hoặc outbound), giao thức IP (TCP, UDP, ICMP), cổng và nguồn/đích dựa trên địa chỉ IP, dải địa chỉ IP hoặc nhóm bảo mật.</p>
}

// question: 6.6  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>Khi định nghĩa một quy tắc Security Group để cho phép truy cập SSH (port 22) từ bất kỳ đâu, giá trị nào sau đây được sử dụng làm CidrIp?</p>{
	~[moodle]10.0.0.0/8.#<p>Đây là dải địa chỉ IP riêng, không đại diện cho "bất kỳ đâu".</p>
	~[moodle]192.168.1.0/24.#<p>Đây là dải địa chỉ IP riêng, không đại diện cho "bất kỳ đâu".</p>
	=[moodle]0.0.0.0/0.
	~[moodle]172.31.0.0/16.#<p>Đây là dải địa chỉ IP riêng, không đại diện cho "bất kỳ đâu".</p>
	####<p><strong>Giải thích</strong>: 0.0.0.0/0 là một CIDR block đại diện cho tất cả các địa chỉ IP, cho phép truy cập từ bất kỳ đâu.</p>
}

// question: 6.7  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>Để tạo một mạng riêng biệt trong đám mây AWS mà không nhất thiết phải kết nối với internet công cộng, bạn sẽ sử dụng dịch vụ nào?</p>{
	~[moodle]Amazon EC2 để tạo các máy ảo riêng tư.#<p>EC2 tạo máy ảo, nhưng VPC định nghĩa mạng mà chúng chạy trong đó.</p>
	~[moodle]Amazon S3 để lưu trữ dữ liệu riêng tư.#<p>S3 lưu trữ đối tượng, không phải dịch vụ mạng.</p>
	=[moodle]Amazon Virtual Private Cloud (VPC).
	~[moodle]AWS Direct Connect để tạo kết nối mạng riêng tư.#<p>Direct Connect tạo kết nối riêng giữa trung tâm dữ liệu của bạn và AWS, nhưng VPC là dịch vụ định nghĩa mạng riêng trong AWS.</p>
	####<p><strong>Giải thích</strong>: Khi bạn tạo một VPC, bạn sẽ có mạng riêng của mình trên AWS. "Riêng tư" có nghĩa là bạn có thể sử dụng các dải địa chỉ như 10.0.0.0/8, 172.16.0.0/12 hoặc 192.168.0.0/16 để thiết kế một mạng không nhất thiết phải kết nối với internet công cộng.</p>
}

// question: 6.8  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>Trong một VPC, "Internet Gateway (IGW)" đóng vai trò gì?</p>{
	~[moodle]Mã hóa tất cả lưu lượng truy cập đi ra khỏi VPC.#<p>Mã hóa không phải là chức năng của IGW.</p>
	=[moodle]Chuyển đổi các địa chỉ IP công cộng của máy ảo thành địa chỉ IP riêng của chúng bằng NAT và kiểm soát lưu lượng công cộng.
	~[moodle]Phân phối lưu lượng truy cập giữa các vùng sẵn sàng khác nhau.#<p>Phân phối lưu lượng giữa các AZs thường được xử lý bởi Load Balancer.</p>
	~[moodle]Cung cấp các kết nối VPN an toàn giữa VPC và mạng tại chỗ.#<p>VPN Gateway xử lý các kết nối VPN.</p>
	####<p><strong>Giải thích</strong>: IGW sẽ chuyển đổi các địa chỉ IP công cộng của máy ảo của bạn thành địa chỉ IP riêng của chúng bằng cách sử dụng Network Address Translation (NAT). Tất cả các địa chỉ IP công cộng được sử dụng trong VPC đều được kiểm soát bởi IGW này.</p>
}

// question: 6.9  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>Sự khác biệt duy nhất giữa một "public subnet" và một "private subnet" trong VPC là gì?</p>{
	=[moodle]Public subnet có một đường định tuyến đến Internet Gateway (IGW), trong khi private subnet không có.
	~[moodle]Private subnet chỉ có thể chứa các máy ảo chạy Windows, trong khi public subnet chứa Linux.#<p>Loại hệ điều hành không liên quan đến việc public hay private của subnet.</p>
	~[moodle]Public subnet cho phép truy cập SSH từ bất kỳ đâu theo mặc định.#<p>Cả hai đều được bảo vệ bởi Security Groups và Network ACLs, và quyền truy cập SSH cần được cấu hình.</p>
	~[moodle]Private subnet luôn được bảo vệ bởi một Network ACL, trong khi public subnet không cần.#<p>Network ACLs có thể được áp dụng cho cả public và private subnets.</p>
	####<p><strong>Giải thích</strong>: Sự khác biệt duy nhất giữa public subnet và private subnet là public subnet có một đường định tuyến đến IGW.</p>
}

// question: 6.10  name: Chapter 6: Securing your system: IAM, security groups, and VPC
::Chapter 6\: Securing your system: IAM, security groups, and VPC::[html]<p>Khi bạn cần truy cập internet từ các máy ảo trong một private subnet, dịch vụ AWS nào thường được sử dụng?</p>{
	~[moodle]Internet Gateway (IGW) được gắn trực tiếp vào private subnet.#<p>IGW được gắn vào VPC, không trực tiếp vào private subnet, và các phiên bản trong private subnet không có đường định tuyến đến IGW.</p>
	~[moodle]VPN Gateway để tạo một kết nối an toàn.#<p>VPN Gateway để kết nối với mạng tại chỗ, không phải internet công cộng.</p>
	=[moodle]NAT Gateway (Network Address Translation Gateway).
	~[moodle]Security Group được cấu hình để cho phép tất cả lưu lượng đi ra.#<p>Security Group kiểm soát lưu lượng cho từng phiên bản, nhưng cần NAT Gateway để cho phép lưu lượng đi ra internet từ private subnet.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể tạo một NAT Gateway để các phiên bản trong một private subnet có thể truy cập internet công cộng nhưng không thể nhận các kết nối không mong muốn từ internet.</p>
}

// Chapter 7: Automating operational tasks with Lambda

// question: 7.1  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>Tính năng chính của AWS Lambda trong việc chạy mã là gì?</p>{
	~[moodle]Yêu cầu bạn phải cung cấp và quản lý máy ảo để chạy mã của mình.#<p>Lambda giúp loại bỏ trách nhiệm quản lý máy ảo.</p>
	=[moodle]Thực thi mã của bạn trong một môi trường tính toán được quản lý hoàn toàn mà không cần máy ảo.
	~[moodle]Yêu cầu bạn phải cài đặt và cập nhật hệ điều hành và phần mềm runtime.#<p>Lambda giúp loại bỏ trách nhiệm quản lý hệ điều hành và runtime.</p>
	~[moodle]Chỉ hỗ trợ các ngôn ngữ lập trình đặc biệt của AWS.#<p>Lambda hỗ trợ nhiều ngôn ngữ phổ biến như Java, Node.js, C#, Python và Go.</p>
	####<p><strong>Giải thích</strong>: AWS Lambda cung cấp khả năng tính toán nhưng ở mức độ chi tiết: một môi trường thực thi cho các hàm nhỏ, thay vì một hệ điều hành hoặc container hoàn chỉnh. Bạn không cần máy ảo để chạy mã của riêng mình nữa.</p>
}

// question: 7.2  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>So với máy ảo EC2, AWS Lambda mang lại lợi ích gì về khả năng mở rộng (scalability)?</p>{
	~[moodle]Yêu cầu bạn phải cấu hình và giám sát các hoạt động mở rộng một cách thủ công.#<p>Cấu hình và giám sát mở rộng là trách nhiệm của bạn với EC2 Auto Scaling.</p>
	=[moodle]Tự động mở rộng quy mô (scales automatically) để đáp ứng nhu cầu, với giới hạn điều tiết có thể tăng lên.
	~[moodle]Hạn chế số lượng bản sao của hàm Lambda chạy đồng thời để giữ chi phí ổn định.#<p>Lambda có giới hạn điều tiết nhưng mục tiêu chính là tự động mở rộng quy mô.</p>
	~[moodle]Giảm đáng kể số lượng CPU và bộ nhớ có sẵn cho mỗi hàm Lambda.#<p>Lambda cung cấp môi trường chạy mã hiệu quả, không phải giảm CPU và bộ nhớ.</p>
	####<p><strong>Giải thích</strong>: AWS Lambda tự động mở rộng quy mô. Giới hạn điều tiết ngăn bạn tạo các khoản phí không mong muốn một cách vô tình và có thể được tăng lên bởi hỗ trợ AWS nếu cần.</p>
}

// question: 7.3  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>AWS Lambda được lập hóa đơn dựa trên yếu tố nào?</p>{
	~[moodle]Phí thuê bao hàng tháng cố định cho mỗi hàm đã triển khai.#<p>Lambda không tính phí cố định hàng tháng mà dựa trên mức sử dụng.</p>
	~[moodle]Số lượng CPU ảo và dung lượng bộ nhớ được phân bổ cho hàm.#<p>Bộ nhớ ảnh hưởng đến chi phí nhưng không phải cơ sở chính.</p>
	=[moodle]Số lượng lần gọi (invocation) và thời gian thực thi của mã của bạn.
	~[moodle]Tổng dung lượng lưu trữ được sử dụng bởi các gói triển khai của hàm.#<p>Lưu trữ gói triển khai có giới hạn miễn phí và không phải cơ sở chính.</p>
	####<p><strong>Giải thích</strong>: AWS Lambda được lập hóa đơn dựa trên số lượng lần gọi. Do đó, bạn không phải trả tiền cho các tài nguyên nhàn rỗi đang chờ công việc.</p>
}

// question: 7.4  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>Để thực hiện các kiểm tra sức khỏe định kỳ cho một trang web (ví dụ: cứ sau 5 phút), bạn có thể sử dụng tính năng nào của AWS Lambda?</p>{
	~[moodle]Một API Gateway để nhận các yêu cầu HTTP bên ngoài.#<p>API Gateway được sử dụng để tạo API REST, không phải để kích hoạt định kỳ.</p>
	=[moodle]Một sự kiện được lên lịch (Scheduled event) để kích hoạt hàm Lambda.
	~[moodle]Một DynamoDB Stream để phản ứng với các thay đổi trong cơ sở dữ liệu.#<p>DynamoDB Streams phản ứng với các thay đổi trong cơ sở dữ liệu DynamoDB.</p>
	~[moodle]Một CloudWatch Alarm được cấu hình để kích hoạt khi có lỗi.#<p>CloudWatch Alarm giám sát các chỉ số và kích hoạt hành động khi ngưỡng bị vi phạm, không phải để kích hoạt định kỳ một hàm.</p>
	####<p><strong>Giải thích</strong>: Một sự kiện được lên lịch (Scheduled event) kích hoạt hàm Lambda cứ sau 5 phút. Điều này tương đương với dịch vụ cron trên Linux.</p>
}

// question: 7.5  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>Khi tạo một hàm Lambda mới trong AWS Management Console, bạn có thể sử dụng các "blueprint" (bản thiết kế) do AWS cung cấp để làm gì?</p>{
	~[moodle]Để định cấu hình thông tin xác thực IAM cho hàm Lambda.#<p>Cấu hình IAM role được thực hiện riêng biệt, mặc dù blueprint có thể gợi ý.</p>
	~[moodle]Để tự động tạo các bản sao lưu của mã hàm Lambda.#<p>Sao lưu mã hàm Lambda được thực hiện thông qua các công cụ triển khai hoặc quản lý phiên bản.</p>
	=[moodle]Để cung cấp mã và cấu hình hàm Lambda đã được định nghĩa trước cho các trường hợp sử dụng phổ biến.
	~[moodle]Để giám sát chi phí của hàm Lambda và tạo cảnh báo.#<p>Giám sát chi phí là chức năng của CloudWatch Billing Alarm.</p>
	####<p><strong>Giải thích</strong>: AWS cung cấp các blueprint cho các trường hợp sử dụng khác nhau, bao gồm mã và cấu hình hàm Lambda. Chúng hữu ích để bắt đầu nhanh chóng.</p>
}

// question: 7.6  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>Để truyền các cài đặt động vào hàm Lambda của bạn (ví dụ: URL của trang web để kiểm tra sức khỏe), bạn nên sử dụng cơ chế nào?</p>{
	~[moodle]Mã hóa cứng các giá trị trực tiếp trong mã nguồn của hàm.#<p>Mã hóa cứng làm giảm tính linh hoạt và khả năng tái sử dụng.</p>
	~[moodle]Truyền các giá trị này dưới dạng tham số dòng lệnh khi gọi hàm.#<p>Hàm Lambda không nhận tham số dòng lệnh theo cách truyền thống.</p>
	=[moodle]Sử dụng các biến môi trường (environment variables) được cấu hình cho hàm.
	~[moodle]Lưu trữ các giá trị trong một đối tượng S3 và đọc chúng từ hàm.#<p>Mặc dù có thể, biến môi trường là cách tiêu chuẩn hơn cho các cài đặt nhỏ.</p>
	####<p><strong>Giải thích</strong>: Các biến môi trường thường được sử dụng để truyền các cài đặt động vào hàm của bạn. Ví dụ: URL của trang web và văn bản mong đợi cho kiểm tra sức khỏe.</p>
}

// question: 7.7  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>Khi một hàm Lambda gặp lỗi bên trong hàm (ví dụ: ngoại lệ hoặc hết thời gian), chỉ số CloudWatch nào sẽ đếm số lần hàm bị lỗi?</p>{
	~[moodle]Invocations (Số lần gọi).#<p>Invocations đếm tổng số lần hàm được gọi, bao gồm cả thành công và thất bại.</p>
	~[moodle]Duration (Thời lượng).#<p>Duration đo thời gian chạy mã.</p>
	=[moodle]Errors (Lỗi).
	~[moodle]Throttles (Điều tiết).#<p>Throttles đếm số lần hàm bị điều tiết do đạt giới hạn chạy đồng thời.</p>
	####<p><strong>Giải thích</strong>: Chỉ số Errors đếm số lần một hàm bị lỗi do lỗi bên trong hàm, ví dụ như ngoại lệ hoặc hết thời gian.</p>
}

// question: 7.8  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>Khi muốn thêm một thẻ chứa tên chủ sở hữu vào các phiên bản EC2 mới được khởi chạy một cách tự động, hàm Lambda của bạn cần được kích hoạt bởi sự kiện CloudWatch nào?</p>{
	~[moodle]Một sự kiện được lên lịch (Scheduled Event) cứ sau vài phút.#<p>Sự kiện lên lịch là để các tác vụ định kỳ, không phải phản ứng với các thay đổi tức thì.</p>
	=[moodle]Một sự kiện từ CloudTrail với detail-type là "AWS API Call" và eventName là "RunInstances" từ dịch vụ EC2.
	~[moodle]Một sự kiện từ S3 khi một đối tượng mới được tải lên.#<p>Các sự kiện này không liên quan đến việc khởi chạy phiên bản EC2.</p>
	~[moodle]Một sự kiện từ DynamoDB Streams khi một mục mới được thêm vào bảng.#<p>Các sự kiện này không liên quan đến việc khởi chạy phiên bản EC2.</p>
	####<p><strong>Giải thích</strong>: Để thêm thẻ chủ sở hữu vào các phiên bản EC2 mới, hàm Lambda cần được kích hoạt bởi một sự kiện từ CloudTrail cho biết có ai đó đã khởi chạy một phiên bản EC2. Mẫu sự kiện sẽ khớp với detail-type là "AWS API Call", source là "ec2" và eventName là "RunInstances".</p>
}

// question: 7.9  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>"Serverless Application Model (SAM)" được AWS phát hành để làm gì?</p>{
	~[moodle]Cung cấp một giao diện đồ họa người dùng để quản lý các ứng dụng serverless.#<p>SAM là một framework dựa trên mẫu, không phải giao diện đồ họa.</p>
	=[moodle]Cung cấp một framework để xây dựng các ứng dụng serverless, mở rộng các mẫu CloudFormation để dễ dàng triển khai các hàm Lambda.
	~[moodle]Tự động hóa việc tạo và quản lý các máy ảo cho các ứng dụng serverless.#<p>SAM tập trung vào các hàm serverless, không phải máy ảo.</p>
	~[moodle]Chỉ cho phép triển khai các hàm Lambda được viết bằng Node.js và Python.#<p>SAM hỗ trợ nhiều runtime của Lambda.</p>
	####<p><strong>Giải thích</strong>: SAM cung cấp một framework cho các ứng dụng serverless, mở rộng các mẫu CloudFormation để dễ dàng triển khai các hàm Lambda.</p>
}

// question: 7.10  name: Chapter 7: Automating operational tasks with Lambda
::Chapter 7\: Automating operational tasks with Lambda::[html]<p>Khi triển khai một hàm Lambda bằng SAM kết hợp với AWS CLI, các bước cần thiết là gì?</p>{
	~[moodle]Chỉ cần viết mã hàm Lambda và tải nó lên trực tiếp AWS.#<p>Cần đóng gói và cấu hình các phụ thuộc.</p>
	=[moodle]Tải gói triển khai lên S3, sau đó tạo và cấu hình hàm Lambda cùng với các phụ thuộc của nó.
	~[moodle]Chỉ định URL của mã nguồn trên GitHub và SAM sẽ tự động triển khai.#<p>Cần một bản build hoặc zip để tải lên S3.</p>
	~[moodle]Cài đặt thủ công tất cả các phụ thuộc của hàm Lambda trên một máy ảo EC2.#<p>Hàm Lambda chạy trong môi trường được quản lý, không cần cài đặt thủ công trên EC2.</p>
	####<p><strong>Giải thích</strong>: Để triển khai một hàm Lambda, bạn cần tải gói triển khai lên S3. Sau đó, bạn cần tạo và cấu hình hàm Lambda cũng như tất cả các phụ thuộc (IAM role, event rule, v.v.). Sử dụng SAM kết hợp với AWS CLI cho phép bạn hoàn thành cả hai tác vụ này.</p>
}

// Chapter 8: Storing your objects: S3 and Glacier

// question: 8.1  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>Trong một "object store" như Amazon S3, một đối tượng (object) được cấu tạo từ ba phần chính nào?</p>{
	~[moodle]Một ID duy nhất, thông tin về người dùng đã truy cập gần đây và lịch sử thay đổi.#<p>Các yếu tố này là các khía cạnh liên quan nhưng không phải là ba phần cấu tạo cốt lõi của một đối tượng.</p>
	=[moodle]Một ID duy nhất, siêu dữ liệu mô tả nội dung và chính nội dung (dữ liệu) đó.
	~[moodle]Một ID duy nhất, các quy tắc truy cập cụ thể cho từng cá nhân và các chính sách bảo mật.#<p>Các yếu tố này là các khía cạnh liên quan nhưng không phải là ba phần cấu tạo cốt lõi của một đối tượng.</p>
	~[moodle]Một ID duy nhất, thông tin về khu vực lưu trữ vật lý và loại hệ thống tệp được sử dụng.#<p>Các yếu tố này là các khía cạnh liên quan nhưng không phải là ba phần cấu tạo cốt lõi của một đối tượng.</p>
	####<p><strong>Giải thích</strong>: Các đối tượng được lưu trữ trong một object store có ba phần: một ID duy nhất, siêu dữ liệu mô tả nội dung và chính nội dung đó (ví dụ: một hình ảnh).</p>
}

// question: 8.2  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>Amazon S3 là viết tắt của gì và nó cung cấp dịch vụ gì?</p>{
	~[moodle]Amazon Secure Storage Solution, cung cấp khả năng lưu trữ đối tượng được mã hóa.#<p>Tên này không chính xác và S3 không chỉ giới hạn ở lưu trữ mã hóa.</p>
	=[moodle]Amazon Simple Storage Service, là một kho lưu trữ dữ liệu phân tán tổ chức dữ liệu dưới dạng đối tượng.
	~[moodle]Amazon Scalable Server System, cung cấp máy chủ ảo có thể mở rộng.#<p>Tên này không chính xác và mô tả dịch vụ EC2.</p>
	~[moodle]Amazon Smart Sync Service, tự động đồng bộ hóa dữ liệu giữa các thiết bị.#<p>Tên này không chính xác và không phải chức năng của S3.</p>
	####<p><strong>Giải thích</strong>: Amazon S3 là viết tắt của Amazon Simple Storage Service. Đó là một dịch vụ web điển hình cho phép bạn lưu trữ và truy xuất dữ liệu được tổ chức dưới dạng đối tượng thông qua một API có thể truy cập qua HTTPS.</p>
}

// question: 8.3  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>Trường hợp sử dụng điển hình nào sau đây phù hợp nhất với Amazon S3?</p>{
	~[moodle]Chạy cơ sở dữ liệu quan hệ yêu cầu hiệu suất I/O cấp khối thấp.#<p>Cơ sở dữ liệu quan hệ thường sử dụng RDS hoặc EBS.</p>
	=[moodle]Lưu trữ và cung cấp nội dung trang web tĩnh như HTML, JavaScript, CSS và hình ảnh.
	~[moodle]Chạy hệ điều hành của một máy ảo EC2.#<p>Hệ điều hành EC2 thường khởi động từ EBS.</p>
	~[moodle]Chia sẻ dữ liệu cấp tệp giữa nhiều máy ảo Linux.#<p>Chia sẻ dữ liệu cấp tệp giữa nhiều máy ảo thường sử dụng EFS.</p>
	####<p><strong>Giải thích</strong>: Các trường hợp sử dụng điển hình của S3 bao gồm lưu trữ và cung cấp nội dung trang web tĩnh, ví dụ như blog cloudonaut.io được lưu trữ trên S3.</p>
}

// question: 8.4  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>Khi sử dụng AWS CLI để sao lưu dữ liệu lên S3, lệnh nào sau đây được sử dụng để tạo một bucket S3?</p>{
	~[moodle]aws s3 cp s3://my-bucket.#<p>aws s3 cp được sử dụng để sao chép tệp.</p>
	~[moodle]aws s3 rm s3://my-bucket.#<p>aws s3 rm được sử dụng để xóa tệp hoặc bucket.</p>
	=[moodle]aws s3 mb s3://my-bucket.
	~[moodle]aws s3 sync s3://my-bucket.#<p>aws s3 sync được sử dụng để đồng bộ hóa thư mục.</p>
	####<p><strong>Giải thích</strong>: Lệnh aws s3 mb (make bucket) được sử dụng để tạo một bucket S3 mới.</p>
}

// question: 8.5  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>Để tự động di chuyển các đối tượng từ Amazon S3 sang Amazon Glacier sau một khoảng thời gian nhất định (ví dụ: sau một ngày), bạn cần cấu hình điều gì trên bucket S3?</p>{
	~[moodle]Bật tính năng sao chép xuyên vùng (cross-region replication).#<p>Sao chép xuyên vùng là để sao chép dữ liệu giữa các khu vực.</p>
	=[moodle]Thêm một quy tắc vòng đời (lifecycle rule) vào bucket.
	~[moodle]Sử dụng tính năng mã hóa mặc định của S3.#<p>Mã hóa liên quan đến bảo mật dữ liệu, không phải quản lý vòng đời.</p>
	~[moodle]Thiết lập một CloudWatch Alarm để kích hoạt việc di chuyển dữ liệu.#<p>CloudWatch Alarm dùng để giám sát và cảnh báo, không trực tiếp quản lý vòng đời đối tượng.</p>
	####<p><strong>Giải thích</strong>: Bạn cần thêm một quy tắc vòng đời (lifecycle rule) vào bucket S3 để tự động di chuyển các đối tượng sang Glacier sau một khoảng thời gian nhất định.</p>
}

// question: 8.6  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>So với Amazon S3, Amazon Glacier có đặc điểm chính nào về chi phí và thời gian truy cập dữ liệu?</p>{
	~[moodle]Chi phí lưu trữ cao hơn nhưng truy cập tức thì.#<p>S3 có chi phí lưu trữ cao hơn Glacier.</p>
	=[moodle]Chi phí lưu trữ thấp hơn nhiều nhưng thời gian truy xuất dữ liệu chậm hơn đáng kể.
	~[moodle]Chi phí lưu trữ và thời gian truy xuất tương đương nhau.#<p>Chi phí và thời gian truy xuất của Glacier khác biệt đáng kể so với S3.</p>
	~[moodle]Chi phí lưu trữ thấp hơn nhưng chỉ có thể truy xuất dữ liệu trong vòng vài phút.#<p>Thời gian truy xuất của Glacier có thể mất từ một phút đến mười hai giờ.</p>
	####<p><strong>Giải thích</strong>: Glacier là giải pháp lưu trữ dữ liệu không thường xuyên với chi phí cực kỳ thấp, nhưng thời gian truy cập dữ liệu có thể mất từ một phút đến mười hai giờ, tùy thuộc vào tùy chọn truy xuất.</p>
}

// question: 8.7  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>Khi sử dụng S3 để lưu trữ các đối tượng một cách lập trình thông qua AWS SDK, các hoạt động nào sau đây thường có thể thực hiện được?</p>{
	~[moodle]Chỉ có thể tạo và xóa bucket mà không thể thao tác với đối tượng bên trong.#<p>S3 SDK hỗ trợ đầy đủ các thao tác CRUD trên đối tượng.</p>
	=[moodle]Liệt kê các bucket và đối tượng của chúng, tạo, xóa, cập nhật đối tượng và quản lý quyền truy cập.
	~[moodle]Chỉ có thể tải lên các tệp có kích thước tối đa 1GB.#<p>S3 hỗ trợ lưu trữ các đối tượng có kích thước gần như không giới hạn.</p>
	~[moodle]Chỉ có thể đọc đối tượng mà không thể sửa đổi hoặc xóa chúng.#<p>S3 SDK hỗ trợ đầy đủ các thao tác CRUD.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể thực hiện các hoạt động như liệt kê bucket và đối tượng của chúng, tạo, xóa, cập nhật và xóa (CRUD) đối tượng và bucket, và quản lý quyền truy cập đối tượng.</p>
}

// question: 8.8  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>Tại sao bạn không thể lưu trữ một ứng dụng như WordPress (dựa trên PHP) trực tiếp trên Amazon S3 khi sử dụng S3 cho web hosting tĩnh?</p>{
	~[moodle]Vì S3 không hỗ trợ lưu trữ các tệp lớn hơn 1GB.#<p>S3 hỗ trợ lưu trữ các đối tượng có kích thước gần như không giới hạn.</p>
	=[moodle]Vì S3 không thể thực thi các script phía máy chủ (server-side scripts) như PHP.
	~[moodle]Vì S3 yêu cầu mã hóa tất cả nội dung được lưu trữ.#<p>Mã hóa là một tính năng của S3 nhưng không phải là lý do hạn chế web hosting động.</p>
	~[moodle]Vì S3 không cung cấp địa chỉ IP công khai cố định cho các trang web.#<p>S3 có thể được cấu hình cho web hosting tĩnh với URL và tích hợp với các dịch vụ DNS khác.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể lưu trữ một trang web tĩnh với S3 và cung cấp nội dung tĩnh như HTML, JavaScript, CSS, hình ảnh, âm thanh và video. Nhưng hãy nhớ rằng bạn không thể thực thi các script phía máy chủ như PHP hoặc JSP. Ví dụ: không thể lưu trữ WordPress, một CMS dựa trên PHP, trên S3.</p>
}

// question: 8.9  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>Khi tạo, cập nhật hoặc xóa một đối tượng trên S3, hoạt động này có tính chất "atomic". Điều này có nghĩa là gì?</p>{
	~[moodle]Bạn luôn nhận được dữ liệu cũ trong một khoảng thời gian ngắn sau khi thay đổi một đối tượng.#<p>S3 có tính nhất quán cuối cùng (eventual consistency) cho các bản ghi đè và xóa, có nghĩa là có thể đọc dữ liệu cũ trong một thời gian ngắn.</p>
	=[moodle]Bạn sẽ không bao giờ nhận được dữ liệu bị hỏng hoặc một phần.
	~[moodle]Hoạt động được thực hiện bởi một máy ảo duy nhất để đảm bảo tính nhất quán.#<p>S3 là một kho lưu trữ phân tán, không phải một máy ảo duy nhất.</p>
	~[moodle]Không có đảm bảo về tính nhất quán dữ liệu sau khi hoạt động hoàn tất.#<p>S3 cung cấp đảm bảo về tính nhất quán (atomic) của các thao tác.</p>
	####<p><strong>Giải thích</strong>: Khi bạn tạo, cập nhật hoặc xóa một đối tượng trên S3, hoạt động này có tính chất atomic. Điều này có nghĩa là nếu bạn đọc một đối tượng sau khi tạo, cập nhật hoặc xóa, bạn sẽ không bao giờ nhận được dữ liệu bị hỏng hoặc một phần.</p>
}

// question: 8.10  name: Chapter 8: Storing your objects: S3 and Glacier
::Chapter 8\: Storing your objects: S3 and Glacier::[html]<p>Để giảm thời gian tải cho nội dung web tĩnh và phân phối nó đến các node trên toàn thế giới, dịch vụ AWS nào có thể được sử dụng cùng với S3?</p>{
	~[moodle]Amazon RDS để lưu trữ dữ liệu cơ sở dữ liệu.#<p>RDS là cho cơ sở dữ liệu quan hệ, không phải nội dung tĩnh.</p>
	=[moodle]Amazon CloudFront, một Content Delivery Network (CDN).
	~[moodle]Amazon Elastic Block Store (EBS) để tăng tốc I/O.#<p>EBS là bộ nhớ cấp khối cho EC2, không phải phân phối nội dung toàn cầu.</p>
	~[moodle]AWS Lambda để xử lý dữ liệu động.#<p>Lambda là để thực thi mã serverless, không phải phân phối nội dung tĩnh.</p>
	####<p><strong>Giải thích</strong>: Sử dụng mạng phân phối nội dung (CDN) giúp giảm thời gian tải cho nội dung web tĩnh. Amazon CloudFront là CDN được cung cấp bởi AWS, phân phối nội dung tĩnh đến các node trên toàn thế giới để giảm độ trễ.</p>
}

// Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store

// question: 9.1  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Dịch vụ Amazon Elastic Block Store (EBS) cung cấp loại bộ nhớ nào và đặc điểm chính của nó là gì?</p>{
	~[moodle]Bộ nhớ cấp đối tượng (object storage) có khả năng lưu trữ không giới hạn cho dữ liệu không có cấu trúc.#<p>Đây là mô tả của Amazon S3, một dịch vụ lưu trữ đối tượng.</p>
	=[moodle]Bộ nhớ cấp khối (block-level storage) liên tục được gắn qua mạng cho các instance EC2.
	~[moodle]Bộ nhớ trong bộ nhớ (in-memory storage) tốc độ cao để lưu trữ dữ liệu tạm thời với độ trễ thấp.#<p>Đây là mô tả của Amazon ElastiCache, một dịch vụ bộ nhớ đệm trong bộ nhớ.</p>
	~[moodle]Bộ nhớ cấp tệp (file-level storage) có thể mở rộng được chia sẻ giữa nhiều máy chủ Linux.#<p>Đây là mô tả của Amazon EFS, một hệ thống tệp mạng.</p>
	####<p><strong>Giải thích</strong>\: EBS cung cấp bộ nhớ cấp khối liên tục được gắn qua mạng cho các instance EC2, và nó vẫn tồn tại ngay cả khi instance EC2 bị chấm dứt.</p>
}

// question: 9.2  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Điều gì xảy ra với volume EBS khi instance EC2 mà nó được gắn vào bị chấm dứt (terminated)?</p>{
	~[moodle]Volume EBS sẽ tự động bị xóa cùng với instance EC2 để tránh chi phí không cần thiết.#<p>Điều này chỉ đúng nếu thuộc tính DeleteOnTermination được đặt thành true trên volume gốc, nhưng không phải là mặc định cho tất cả các volume EBS.</p>
	=[moodle]Volume EBS vẫn tồn tại độc lập với instance EC2 và có thể được gắn vào một instance khác.
	~[moodle]Volume EBS được chuyển đổi thành snapshot và lưu trữ trong Amazon S3 để truy xuất sau này.#<p>EBS snapshots là một cơ chế sao lưu thủ công hoặc tự động nhưng không phải là hành vi mặc định khi chấm dứt instance.</p>
	~[moodle]Volume EBS được chuyển thành chế độ chỉ đọc và không thể ghi vào được nữa.#<p>Volume EBS không tự động thay đổi chế độ ghi khi instance EC2 bị chấm dứt.</p>
	####<p><strong>Giải thích</strong>\: Các volume EBS không phải là một phần của instance EC2; chúng được gắn vào instance EC2 qua kết nối mạng. Nếu bạn chấm dứt instance EC2, các volume EBS vẫn còn.</p>
}

// question: 9.3  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Instance Store khác với EBS ở đặc điểm nào liên quan đến tính bền vững của dữ liệu?</p>{
	~[moodle]Instance Store cung cấp bộ nhớ bền vững được sao chép tự động trên nhiều Availability Zone.#<p>Tính năng sao chép và bền vững là đặc điểm của EBS và EFS, không phải Instance Store.</p>
	=[moodle]Instance Store cung cấp bộ nhớ cấp khối tạm thời, chỉ khả dụng khi instance EC2 đang chạy và sẽ bị xóa khi instance dừng hoặc chấm dứt.
	~[moodle]Instance Store cung cấp bộ nhớ cấp đối tượng với tính bền vững rất cao, phù hợp cho việc sao lưu dài hạn.#<p>Amazon S3 và Glacier là các dịch vụ lưu trữ đối tượng và lưu trữ dữ liệu dài hạn, không phải Instance Store.</p>
	~[moodle]Instance Store cung cấp bộ nhớ cấp tệp được chia sẻ, đảm bảo dữ liệu không bị mất khi instance bị chấm dứt.#<p>EFS là dịch vụ lưu trữ cấp tệp được chia sẻ.</p>
	####<p><strong>Giải thích</strong>\: Instance Store cung cấp bộ nhớ cấp khối tạm thời được gắn trực tiếp vào máy chủ lưu trữ VM. Nó chỉ khả dụng khi instance của bạn đang chạy; nó sẽ không duy trì dữ liệu của bạn nếu bạn dừng hoặc chấm dứt instance.</p>
}

// question: 9.4  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Trong các trường hợp sử dụng sau, loại volume EBS nào được khuyến nghị làm mặc định cho hầu hết các workload với tải trung bình và mô hình truy cập ngẫu nhiên?</p>{
	~[moodle]Provisioned IOPS SSD (io1) để đảm bảo hiệu suất I/O cao nhất cho các ứng dụng quan trọng.#<p>Provisioned IOPS SSD (io1) dành cho các workload yêu cầu mức I/O cao và hiệu suất ổn định.</p>
	=[moodle]General Purpose SSD (gp2) để cung cấp hiệu suất cơ bản vừa phải với khả năng tăng đột biến.
	~[moodle]Cold HDD (sc1) để lưu trữ dữ liệu không thường xuyên truy cập với chi phí thấp nhất.#<p>Cold HDD (sc1) được thiết kế cho các workload có dữ liệu ít truy cập, chi phí thấp.</p>
	~[moodle]EBS Magnetic HDD (standard) cho các workload cũ hoặc không quan trọng về hiệu suất.#<p>EBS Magnetic HDD (standard) là loại volume cũ hơn với hiệu suất thấp và không còn được khuyến nghị cho các workload mới.</p>
	####<p><strong>Giải thích</strong>\: General Purpose SSD (gp2) được khuyến nghị sử dụng làm mặc định cho hầu hết các workload với tải trung bình và mô hình truy cập ngẫu nhiên, ví dụ như volume khởi động hoặc các ứng dụng có tải I/O thấp đến trung bình.</p>
}

// question: 9.5  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Để cải thiện hiệu suất đọc/ghi của volume EBS, bạn cần xem xét những yếu tố nào ngoài loại volume EBS?</p>{
	~[moodle]Chỉ cần tăng kích thước của volume EBS là đủ để cải thiện hiệu suất I/O.#<p>Tăng kích thước volume gp2 có thể tăng IOPS cơ bản nhưng không phải là yếu tố duy nhất.</p>
	=[moodle]Loại instance EC2 và việc instance đó có được tối ưu hóa cho EBS hay không, vì nó ảnh hưởng đến băng thông dành riêng.
	~[moodle]Số lượng Availability Zone mà volume EBS được sao chép tự động để tăng cường khả năng truy cập song song.#<p>Volume EBS chỉ khả dụng trong một Availability Zone duy nhất; nó không được sao chép tự động giữa các AZ.</p>
	~[moodle]Phương thức mã hóa dữ liệu trên volume EBS, vì mã hóa làm giảm hiệu suất I/O đáng kể.#<p>Mã hóa có thể có một chút ảnh hưởng nhưng không phải là yếu tố chính quyết định hiệu suất như loại instance và tối ưu hóa EBS.</p>
	####<p><strong>Giải thích</strong>\: Hiệu suất EBS phức tạp hơn nhiều. Hiệu suất phụ thuộc vào loại instance EC2 cũng như loại volume EBS. Các instance EC2 được tối ưu hóa cho EBS được hưởng lợi bằng cách có băng thông dành riêng cho các volume EBS của chúng.</p>
}

// question: 9.6  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Điều nào sau đây KHÔNG phải là trường hợp sử dụng điển hình cho Amazon EBS?</p>{
	~[moodle]Vận hành một hệ thống cơ sở dữ liệu quan hệ trên một máy ảo EC2.
	~[moodle]Chạy một ứng dụng yêu cầu hệ thống tệp để lưu trữ dữ liệu trên EC2.
	~[moodle]Khởi động hệ điều hành của một máy ảo từ volume EBS.
	=[moodle]Lưu trữ và phân phối nội dung web tĩnh như HTML, CSS và hình ảnh.
	####<p><strong>Giải thích</strong>\: Lưu trữ và phân phối nội dung web tĩnh là trường hợp sử dụng điển hình cho Amazon S3, không phải EBS. EBS được thiết kế cho bộ nhớ cấp khối để gắn vào instance EC2.</p>
}

// question: 9.7  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Để sao lưu dữ liệu từ một volume Instance Store, phương pháp nào được đề xuất vì không có cơ chế sao lưu tích hợp sẵn?</p>{
	~[moodle]Tự động sao lưu Instance Store vào Amazon Glacier hàng ngày để lưu trữ dài hạn.#<p>Glacier là dịch vụ lưu trữ đối tượng chi phí thấp cho dữ liệu ít truy cập, nhưng việc sao lưu trực tiếp từ Instance Store không phải là cơ chế tích hợp.</p>
	=[moodle]Định kỳ đồng bộ hóa các tệp tới một S3 bucket bằng AWS CLI.
	~[moodle]Tạo snapshot của volume Instance Store và lưu trữ chúng trong Amazon EBS.#<p>Snapshot chỉ có thể được tạo từ các volume EBS, không phải Instance Store.</p>
	~[moodle]Sử dụng cơ chế sao lưu tích hợp của hypervisor để tạo bản sao của Instance Store.#<p>Hypervisor không cung cấp cơ chế sao lưu dữ liệu từ Instance Store cho người dùng AWS.</p>
	####<p><strong>Giải thích</strong>\: Không có cơ chế sao lưu tích hợp sẵn cho các volume Instance Store. Bạn có thể sử dụng kết hợp các job theo lịch trình và S3 để sao lưu dữ liệu của mình định kỳ bằng lệnh aws s3 sync.</p>
}

// question: 9.8  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Khi tạo snapshot EBS, điều gì làm cho chúng hiệu quả về chi phí cho các bản sao lưu gia tăng?</p>{
	~[moodle]Snapshot chỉ lưu trữ siêu dữ liệu của volume, không phải dữ liệu thực tế, để giảm chi phí.#<p>Snapshot lưu trữ dữ liệu của volume, không chỉ siêu dữ liệu.</p>
	=[moodle]Snapshot chỉ lưu trữ các khối dữ liệu đã thay đổi kể từ snapshot cuối cùng, giảm không gian lưu trữ cần thiết.
	~[moodle]Snapshot tự động nén tất cả dữ liệu trên volume trước khi lưu trữ, tiết kiệm chi phí.#<p>Mặc dù nén có thể được áp dụng ở một số cấp độ, nhưng cơ chế chính tiết kiệm chi phí là tính gia tăng, không phải nén tự động trên tất cả dữ liệu.</p>
	~[moodle]Snapshot chỉ được lưu trữ tạm thời trong một Availability Zone duy nhất, làm cho chúng rẻ hơn.#<p>EBS snapshots được lưu trữ trên S3, do đó chúng có sẵn trong nhiều Availability Zone và không chỉ tạm thời.</p>
	####<p><strong>Giải thích</strong>\: EBS snapshots là các bản sao lưu cấp khối gia tăng. Điều này có nghĩa là chỉ những thay đổi đối với các khối mới được lưu trữ khi thực hiện nhiều snapshot.</p>
}

// question: 9.9  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Giả sử bạn có một ứng dụng legacy yêu cầu một hệ thống tệp để lưu trữ dữ liệu và cần tính bền vững cao. Bạn nên chọn giải pháp lưu trữ nào trên AWS?</p>{
	~[moodle]Amazon S3 vì nó cung cấp bộ nhớ đối tượng có khả năng mở rộng không giới hạn với tính bền vững cao.#<p>S3 là bộ nhớ đối tượng, không phải hệ thống tệp truyền thống mà ứng dụng legacy có thể yêu cầu.</p>
	~[moodle]Amazon DynamoDB vì nó là cơ sở dữ liệu NoSQL hiệu suất cao cho dữ liệu có cấu trúc và không cần schema.#<p>DynamoDB là cơ sở dữ liệu NoSQL, không phải bộ nhớ cấp khối hoặc hệ thống tệp.</p>
	=[moodle]Amazon EBS với loại volume phù hợp, vì nó cung cấp bộ nhớ cấp khối liên tục và khả năng sao lưu bằng snapshot.
	~[moodle]Amazon ElastiCache để tăng tốc độ truy cập dữ liệu bằng cách lưu trữ trong bộ nhớ, cải thiện hiệu suất.#<p>ElastiCache là bộ nhớ đệm trong bộ nhớ, không phải để lưu trữ dữ liệu bền vững cho ứng dụng.</p>
	####<p><strong>Giải thích</strong>\: EBS cung cấp bộ nhớ cấp khối liên tục mà ứng dụng legacy có thể sử dụng như một hệ thống tệp để lưu trữ dữ liệu. Nó cũng cung cấp tính bền vững và khả năng sao lưu bằng snapshot, phù hợp với yêu cầu về dữ liệu quan trọng.</p>
}

// question: 9.10  name: Chapter 9: Lưu trữ dữ liệu trên ổ cứng: EBS và Instance Store
::Chapter 9\: Lưu trữ dữ liệu trên ổ cứng\: EBS và Instance Store::[html]<p>Khi nào nên sử dụng Instance Store thay vì EBS cho instance EC2?</p>{
	~[moodle]Khi ứng dụng yêu cầu bộ nhớ cấp khối có thể được chia sẻ giữa nhiều instance EC2.#<p>EFS được sử dụng để chia sẻ bộ nhớ cấp khối.</p>
	~[moodle]Khi dữ liệu cần được duy trì sau khi instance EC2 bị chấm dứt hoặc dừng.#<p>EBS là lựa chọn phù hợp khi cần duy trì dữ liệu.</p>
	=[moodle]Khi ứng dụng yêu cầu bộ nhớ tốc độ rất cao cho dữ liệu tạm thời hoặc bộ nhớ đệm.
	~[moodle]Khi chi phí là yếu tố quan trọng nhất và ứng dụng có thể chịu được hiệu suất thấp.#<p>Instance Store không phải lúc nào cũng là lựa chọn rẻ nhất và nó có thể mang lại hiệu suất rất cao, tùy thuộc vào loại instance.</p>
	####<p><strong>Giải thích</strong>\: Instance Store cung cấp bộ nhớ cấp khối trực tiếp gắn vào máy chủ lưu trữ VM, mang lại hiệu suất I/O rất cao và độ trễ rất thấp. Nó phù hợp cho dữ liệu tạm thời, bộ nhớ đệm hoặc các workload yêu cầu hiệu suất cao nhưng không cần tính bền vững sau khi instance bị dừng/chấm dứt.</p>
}

// Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS

// question: 10.1  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Amazon Elastic File System (EFS) dựa trên giao thức nào để cho phép các instance EC2 truy cập hệ thống tệp được chia sẻ?</p>{
	~[moodle]HTTP/HTTPS để truy cập tệp như đối tượng từ các dịch vụ web.#<p>Đây là cách truy cập Amazon S3, một dịch vụ lưu trữ đối tượng.</p>
	~[moodle]SMB/CIFS để tương thích với các hệ thống tệp của Windows.#<p>EFS không hỗ trợ Windows EC2 instances tại thời điểm viết sách.</p>
	=[moodle]NFSv4.1 để gắn kết và chia sẻ tệp giữa các instance Linux.
	~[moodle]iSCSI để cung cấp bộ nhớ cấp khối cho các instance Windows.#<p>EFS không hỗ trợ Windows EC2 instances tại thời điểm viết sách.</p>
	####<p><strong>Giải thích</strong>\: EFS dựa trên giao thức NFSv4.1, vì vậy bạn có thể gắn nó giống như bất kỳ hệ thống tệp nào khác để chia sẻ giữa các instance Linux.</p>
}

// question: 10.2  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Amazon EFS hỗ trợ instance EC2 chạy hệ điều hành nào tại thời điểm viết sách?</p>{
	~[moodle]Chỉ hỗ trợ Windows Server để cung cấp khả năng chia sẻ tệp mạnh mẽ trong môi trường doanh nghiệp.#<p>Các lựa chọn này sai vì EFS giới hạn ở Linux.</p>
	=[moodle]Chỉ hỗ trợ Linux để tối ưu hóa hiệu suất và tương thích với giao thức NFSv4.1.
	~[moodle]Hỗ trợ cả Windows Server và Linux, nhưng yêu cầu cấu hình phức tạp cho Windows.#<p>Các lựa chọn này sai vì EFS giới hạn ở Linux.</p>
	~[moodle]Hỗ trợ tất cả các hệ điều hành phổ biến, bao gồm macOS và FreeBSD, với các driver đặc biệt.#<p>Các lựa chọn này sai vì EFS giới hạn ở Linux.</p>
	####<p><strong>Giải thích</strong>\: Tại thời điểm viết sách, EFS không được hỗ trợ bởi các instance EC2 của Windows. Nó chỉ hoạt động với Linux.</p>
}

// question: 10.3  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Để đạt được tính sẵn sàng cao (high availability) cho hệ thống tệp EFS, bạn cần tạo bao nhiêu mount target và ở đâu?</p>{
	~[moodle]Một mount target duy nhất trong Availability Zone chính của bạn để đơn giản hóa cấu hình.#<p>Một mount target hoặc nhiều mount target trong cùng một AZ sẽ tạo ra một điểm lỗi duy nhất (single point of failure) cho hệ thống tệp nếu AZ đó gặp sự cố.</p>
	~[moodle]Ít nhất hai mount target trong cùng một Availability Zone để tăng cường băng thông.#<p>Một mount target hoặc nhiều mount target trong cùng một AZ sẽ tạo ra một điểm lỗi duy nhất (single point of failure) cho hệ thống tệp nếu AZ đó gặp sự cố.</p>
	=[moodle]Ít nhất hai mount target trong các Availability Zone khác nhau để đảm bảo khả năng phục hồi sau lỗi AZ.
	~[moodle]Không cần mount target vì EFS tự động có sẵn trên tất cả các instance EC2 trong VPC.#<p>Mount target là cần thiết để EC2 instances có thể gắn và truy cập EFS.</p>
	####<p><strong>Giải thích</strong>\: EFS mount target liên kết với một Availability Zone và được bảo vệ bởi security group. Bạn cần ít nhất hai mount target trong các AZ khác nhau để có tính sẵn sàng cao.</p>
}

// question: 10.4  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Amazon EFS định giá dựa trên yếu tố nào?</p>{
	~[moodle]Số lượng thao tác I/O mỗi giây (IOPS) mà bạn cung cấp cho hệ thống tệp.#<p>IOPS là một yếu tố định giá cho EBS Provisioned IOPS SSD, không phải EFS.</p>
	~[moodle]Số lượng request API được gửi đến hệ thống tệp mỗi tháng.#<p>Số lượng request API có thể là một yếu tố định giá cho các dịch vụ khác như S3, nhưng không phải EFS.</p>
	=[moodle]Dung lượng lưu trữ thực tế mà bạn sử dụng tính theo GB mỗi tháng.
	~[moodle]Số lượng instance EC2 được gắn vào hệ thống tệp mỗi giờ.#<p>EFS không tính phí dựa trên số lượng instance được gắn.</p>
	####<p><strong>Giải thích</strong>\: Tính toán chi phí EFS rất đơn giản. Bạn chỉ cần biết dung lượng lưu trữ bạn sử dụng tính bằng GB. EFS tính phí cho mỗi GB mỗi tháng.</p>
}

// question: 10.5  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Chế độ hiệu suất "Max I/O" của EFS phù hợp nhất cho loại workload nào?</p>{
	~[moodle]Các workload nhạy cảm với độ trễ (latency-sensitive workloads) với nhiều tệp nhỏ được truy cập thường xuyên.#<p>Chế độ General Purpose phù hợp hơn cho các workload nhạy cảm với độ trễ, nơi người dùng mong đợi độ trễ thấp để nhận tệp ngay lập tức.</p>
	=[moodle]Các workload phân tích dữ liệu lớn (data analytics) yêu cầu thông lượng cao và ít quan tâm đến độ trễ.
	~[moodle]Các ứng dụng cơ sở dữ liệu quan hệ yêu cầu hiệu suất I/O ổn định và nhất quán.#<p>Cơ sở dữ liệu thường sử dụng EBS hoặc RDS để đạt hiệu suất ổn định.</p>
	~[moodle]Các workload sao lưu định kỳ với dữ liệu ít truy cập, ưu tiên chi phí thấp.#<p>EFS không phải là lựa chọn tối ưu về chi phí cho sao lưu dữ liệu ít truy cập; S3 hoặc Glacier sẽ phù hợp hơn.</p>
	####<p><strong>Giải thích</strong>\: Đối với phân tích dữ liệu, độ trễ không quan trọng. Thông lượng là chỉ số bạn muốn tối ưu hóa. Tối ưu hóa thông lượng có thể đạt được bằng cách sử dụng chế độ hiệu suất Max I/O.</p>
}

// question: 10.6  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Khi bạn gắn EFS share trên các instance EC2, điều gì xảy ra với dữ liệu /home hiện có trên instance EC2 thứ hai (khi sử dụng tập lệnh trong ví dụ sách)?</p>{
	~[moodle]Dữ liệu /home hiện có trên instance thứ hai sẽ được hợp nhất với dữ liệu EFS.#<p>Các lựa chọn này sai vì tập lệnh được thiết kế để xử lý việc sao chép dữ liệu một cách an toàn.</p>
	~[moodle]Dữ liệu /home hiện có trên instance thứ hai sẽ bị ghi đè hoàn toàn bởi nội dung của EFS.#<p>Các lựa chọn này sai vì tập lệnh được thiết kế để xử lý việc sao chép dữ liệu một cách an toàn.</p>
	~[moodle]Instance thứ hai sẽ không khởi động được nếu thư mục /home đã tồn tại trước khi gắn EFS.#<p>Các lựa chọn này sai vì tập lệnh được thiết kế để xử lý việc sao chép dữ liệu một cách an toàn.</p>
	=[moodle]Dữ liệu /home hiện có được sao chép vào EFS trước khi gắn, đảm bảo không mất dữ liệu.
	####<p><strong>Giải thích</strong>\: Tập lệnh được chuẩn bị trong sách sẽ sao chép dữ liệu /home ban đầu vào thư mục /oldhome trước khi gắn hệ thống tệp EFS, sau đó sao chép dữ liệu từ /oldhome vào /home (EFS) sau khi EFS được gắn. Điều này đảm bảo rằng bạn sao chép dữ liệu gốc lần đầu tiên trước khi gắn hệ thống tệp EFS, vốn mặc định là trống.</p>
}

// question: 10.7  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Điều nào sau đây là cách hiệu quả nhất để kiểm soát lưu lượng mạng đến và đi từ EFS mount target?</p>{
	~[moodle]Sử dụng Network Access Control Lists (ACLs) để lọc lưu lượng dựa trên địa chỉ IP.#<p>ACLs hoạt động ở cấp độ subnet và là firewall không trạng thái, ít linh hoạt hơn Security Groups.</p>
	~[moodle]Sử dụng AWS Web Application Firewall (WAF) để bảo vệ khỏi các cuộc tấn công cấp ứng dụng.#<p>WAF bảo vệ các ứng dụng web khỏi các cuộc tấn công web phổ biến, không phải kiểm soát lưu lượng cấp mạng cho EFS.</p>
	=[moodle]Sử dụng Security Groups để cho phép hoặc từ chối lưu lượng truy cập dựa trên các quy tắc đã định nghĩa.
	~[moodle]Tắt tất cả các kết nối mạng đến EFS mount target để đảm bảo an ninh tối đa.#<p>Tắt tất cả kết nối sẽ ngăn chặn EFS hoạt động đúng cách.</p>
	####<p><strong>Giải thích</strong>\: Security Group là cách bạn kiểm soát lưu lượng mạng trên AWS. Bạn có thể sử dụng security group để cho phép lưu lượng truy cập đến instance EC2 hoặc cơ sở dữ liệu RDS, và điều tương tự cũng đúng với mount target EFS.</p>
}

// question: 10.8  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Khi theo dõi EFS, chỉ số BurstCreditBalance được sử dụng để làm gì?</p>{
	~[moodle]Để đo lường tổng dung lượng lưu trữ đã sử dụng trên hệ thống tệp EFS.#<p>Chỉ số MeteredIOBytes hoặc StorageBytes được sử dụng để đo lường dung lượng lưu trữ.</p>
	~[moodle]Để theo dõi số lượng instance EC2 đang gắn hệ thống tệp EFS.#<p>Không có chỉ số cụ thể nào để theo dõi số lượng instance gắn trực tiếp từ EFS.</p>
	=[moodle]Để giám sát số lượng tín dụng có sẵn cho hiệu suất tăng đột biến, giúp tránh suy giảm hiệu suất.
	~[moodle]Để kiểm tra số lượng lỗi I/O xảy ra trên hệ thống tệp EFS trong một khoảng thời gian nhất định.#<p>Các chỉ số liên quan đến lỗi I/O không phải là BurstCreditBalance.</p>
	####<p><strong>Giải thích</strong>\: Chỉ số BurstCreditBalance đo lượng tín dụng tăng đột biến còn lại cho hệ thống tệp của bạn. Khi số lượng này thấp, hệ thống tệp có thể gặp phải giới hạn thông lượng của nó, và việc đặt báo động cho chỉ số này có thể giúp bạn tránh suy giảm hiệu suất.</p>
}

// question: 10.9  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Điều nào sau đây là LỢI ÍCH chính của việc sử dụng EFS so với việc gắn các volume EBS độc lập trên nhiều instance EC2 cho cùng một dữ liệu?</p>{
	~[moodle]EFS cung cấp hiệu suất I/O cao hơn đáng kể so với EBS cho mọi loại workload.#<p>Hiệu suất của EFS có thể khác nhau và không phải lúc nào cũng cao hơn EBS cho mọi workload, đặc biệt là các workload yêu cầu IOPS rất cao.</p>
	=[moodle]EFS tự động nhân bản dữ liệu giữa các Availability Zone, tăng tính bền vững và sẵn sàng cao.
	~[moodle]EFS hoàn toàn miễn phí khi được sử dụng với các instance EC2 thuộc Free Tier.#<p>Chỉ 5GB đầu tiên của EFS miễn phí trong năm đầu tiên của tài khoản AWS (Free Tier).</p>
	~[moodle]EFS có thể được gắn trực tiếp vào các instance EC2 của Windows mà không cần cấu hình thêm.#<p>EFS không được hỗ trợ bởi các instance EC2 của Windows tại thời điểm viết sách.</p>
	####<p><strong>Giải thích</strong>\: EFS lưu trữ tất cả các tệp của bạn trên nhiều đĩa trong nhiều Availability Zone. Do đó, khả năng mất dữ liệu do sự cố phần cứng thấp. Volume EBS chỉ khả dụng trong một AZ duy nhất.</p>
}

// question: 10.10  name: Chapter 10: Chia sẻ volume dữ liệu giữa các máy: EFS
::Chapter 10\: Chia sẻ volume dữ liệu giữa các máy\: EFS::[html]<p>Khi không có cách nào tích hợp để sao lưu EFS, giải pháp sao lưu hiệu quả về chi phí nào được đề xuất cho lịch sử thay đổi nếu dữ liệu đủ nhỏ để phù hợp trên một volume?</p>{
	~[moodle]Đồng bộ hóa các tệp EFS với một bucket S3 định kỳ để tận dụng chi phí thấp.#<p>Đồng bộ hóa với S3 là một lựa chọn, nhưng việc quản lý lịch sử thay đổi và tính gia tăng có thể phức tạp hơn so với EBS snapshot.</p>
	=[moodle]Sử dụng một volume EBS và snapshot, vì snapshot EBS là bản sao lưu gia tăng cấp khối.
	~[moodle]Đồng bộ hóa các tệp EFS với một hệ thống tệp EFS thứ hai trong một khu vực khác.#<p>Sử dụng EFS thứ hai có thể tốn kém hơn so với EBS snapshot cho dữ liệu nhỏ.</p>
	~[moodle]Triển khai một giải pháp sao lưu của bên thứ ba được tích hợp trực tiếp với EFS.#<p>Các giải pháp bên thứ ba có thể tốt, nhưng câu hỏi yêu cầu một cách hiệu quả về chi phí được đề xuất từ sách.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn cần một cách hiệu quả về chi phí để sao lưu lịch sử thay đổi cho EFS, chúng tôi khuyên bạn nên sử dụng một volume EBS và snapshot. Như bạn đã biết từ mục 9.1, snapshot EBS là bản sao lưu gia tăng cấp khối. Điều này có nghĩa là chỉ những thay đổi đối với các khối mới được lưu trữ khi thực hiện nhiều snapshot.</p>
}

// Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS

// question: 11.1  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Amazon RDS là một dịch vụ được quản lý, có nghĩa là AWS chịu trách nhiệm cho những tác vụ nào sau đây?</p>{
	~[moodle]Cấu hình schema cơ sở dữ liệu, tối ưu hóa truy vấn và quản lý người dùng ứng dụng.#<p>Các tác vụ này thuộc trách nhiệm của khách hàng.</p>
	=[moodle]Cung cấp máy ảo, hệ điều hành cơ bản, và xử lý các tác vụ vận hành như sao lưu, vá lỗi và cập nhật.
	~[moodle]Phát triển ứng dụng khách kết nối với cơ sở dữ liệu và đảm bảo mã nguồn hoạt động chính xác.#<p>Các tác vụ này thuộc trách nhiệm của khách hàng.</p>
	~[moodle]Thiết kế kiến trúc tổng thể của hệ thống, bao gồm cách các instance EC2 tương tác với cơ sở dữ liệu.#<p>Các tác vụ này thuộc trách nhiệm của khách hàng.</p>
	####<p><strong>Giải thích</strong>\: RDS là một dịch vụ được quản lý. Nhà cung cấp dịch vụ được quản lý — trong trường hợp này là AWS — chịu trách nhiệm cung cấp một tập hợp các dịch vụ được xác định — trong trường hợp này, vận hành một hệ thống cơ sở dữ liệu quan hệ. AWS chịu trách nhiệm về sao lưu, vá lỗi, cập nhật và sao chép.</p>
}

// question: 11.2  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Amazon RDS hỗ trợ các công cụ cơ sở dữ liệu quan hệ nào sau đây?</p>{
	~[moodle]Chỉ MySQL và PostgreSQL để tập trung vào các giải pháp mã nguồn mở phổ biến.#<p>RDS hỗ trợ nhiều công cụ hơn.</p>
	=[moodle]MySQL, PostgreSQL, Oracle Database, Microsoft SQL Server, MariaDB và Amazon Aurora.
	~[moodle]Chỉ các cơ sở dữ liệu NoSQL như DynamoDB và Cassandra cho hiệu suất cao.#<p>DynamoDB là dịch vụ NoSQL riêng biệt.</p>
	~[moodle]Chỉ các cơ sở dữ liệu dữ liệu lớn như Amazon Redshift và Amazon EMR để phân tích.#<p>Redshift và EMR là dịch vụ dữ liệu lớn riêng biệt.</p>
	####<p><strong>Giải thích</strong>\: AWS cung cấp dịch vụ cho MySQL, PostgreSQL, Oracle Database, Microsoft SQL Server, MariaDB và Amazon Aurora.</p>
}

// question: 11.3  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Để đảm bảo tính sẵn sàng cao (high availability) cho cơ sở dữ liệu RDS, bạn nên cấu hình tùy chọn triển khai nào?</p>{
	=[moodle]Multi-AZ (Multi-Availability Zone) để duy trì một bản sao dự phòng trong một AZ khác và tự động chuyển đổi dự phòng.
	~[moodle]Triển khai read replica (bản sao chỉ đọc) trong cùng một Availability Zone để tăng cường khả năng phục hồi.#<p>Read replica dùng để mở rộng khả năng đọc, không phải là cơ chế chuyển đổi dự phòng chính cho tính sẵn sàng cao.</p>
	~[moodle]Tắt tính năng sao lưu tự động để giảm thiểu thời gian ngừng hoạt động trong trường hợp khẩn cấp.#<p>Tắt sao lưu là một rủi ro; sao lưu tự động là quan trọng cho khả năng phục hồi dữ liệu.</p>
	~[moodle]Sử dụng Instance Store cho volume cơ sở dữ liệu để đạt được hiệu suất I/O cực cao.#<p>Instance Store là bộ nhớ tạm thời và không bền vững, không phù hợp cho cơ sở dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: Để bật triển khai sẵn sàng cao cho cơ sở dữ liệu RDS, bạn sử dụng tùy chọn MultiAZ: true trong CloudFormation. Điều này sẽ duy trì một bản sao dự phòng và tự động chuyển đổi dự phòng trong trường hợp AZ chính gặp sự cố.</p>
}

// question: 11.4  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Khi sao lưu cơ sở dữ liệu RDS, sự khác biệt chính giữa snapshot tự động (automated snapshots) và snapshot thủ công (manual snapshots) là gì?</p>{
	~[moodle]Snapshot tự động được lưu trữ trên Amazon Glacier, trong khi snapshot thủ công được lưu trữ trên Amazon S3.#<p>Cả hai loại snapshot đều được lưu trữ trên S3.</p>
	=[moodle]Snapshot tự động bị xóa khi instance RDS bị xóa, trong khi snapshot thủ công vẫn tồn tại.
	~[moodle]Snapshot tự động có thể được tạo bất kỳ lúc nào, trong khi snapshot thủ công chỉ có thể được tạo trong cửa sổ bảo trì.#<p>Ngược lại, snapshot tự động được tạo trong một cửa sổ bảo trì đã định cấu hình, trong khi snapshot thủ công có thể được tạo bất kỳ lúc nào.</p>
	~[moodle]Snapshot tự động có thể được sử dụng để khôi phục đến một điểm bất kỳ trong thời gian, trong khi snapshot thủ công chỉ khôi phục đến thời điểm snapshot được tạo.#<p>Snapshot tự động hỗ trợ khôi phục đến một điểm bất kỳ trong thời gian (point-in-time recovery) trong khoảng thời gian lưu giữ, trong khi snapshot thủ công chỉ khôi phục đến thời điểm snapshot được tạo.</p>
	####<p><strong>Giải thích</strong>\: Snapshot tự động sẽ bị xóa khi instance cơ sở dữ liệu RDS bị xóa. Snapshot thủ công vẫn còn.</p>
}

// question: 11.5  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Để kiểm soát quyền truy cập cấu hình của cơ sở dữ liệu RDS (ví dụ: tạo, sửa đổi, xóa database instance), dịch vụ AWS nào được sử dụng?</p>{
	~[moodle]Security Groups để lọc lưu lượng mạng đến và đi từ cơ sở dữ liệu.#<p>Security Groups kiểm soát lưu lượng mạng, không phải quyền quản lý cấu hình RDS.</p>
	=[moodle]IAM (Identity and Access Management) để xác định quyền người dùng và vai trò.
	~[moodle]CloudWatch để giám sát hoạt động API và đặt báo động cho các thay đổi cấu hình.#<p>CloudWatch giám sát và báo động, không phải quản lý quyền truy cập.</p>
	~[moodle]VPC (Virtual Private Cloud) để tạo một mạng riêng biệt cho cơ sở dữ liệu.#<p>VPC cung cấp mạng riêng nhưng không quản lý quyền truy cập API.</p>
	####<p><strong>Giải thích</strong>\: Bạn có thể sử dụng IAM để kiểm soát truy cập vào cấu hình của cơ sở dữ liệu RDS, tương tự như cách bạn kiểm soát truy cập vào các dịch vụ AWS khác. Ví dụ, bạn có thể tạo một chính sách IAM để từ chối các hành động rds:Delete*.</p>
}

// question: 11.6  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Khi di chuyển một cơ sở dữ liệu lớn đến AWS với thời gian ngừng hoạt động tối thiểu, dịch vụ nào của AWS có thể hữu ích?</p>{
	~[moodle]AWS CLI để thực hiện các lệnh mysqldump và mysql từ xa.#<p>AWS CLI có thể được sử dụng cho các thao tác dump/import, nhưng không tối ưu cho thời gian ngừng hoạt động tối thiểu trên cơ sở dữ liệu lớn.</p>
	=[moodle]AWS Database Migration Service (DMS) để di chuyển dữ liệu liên tục và đồng bộ hóa.
	~[moodle]AWS CloudFormation để tự động tạo cơ sở dữ liệu RDS và các tài nguyên liên quan.#<p>CloudFormation dùng để tự động hóa hạ tầng, không phải công cụ di chuyển dữ liệu liên tục.</p>
	~[moodle]AWS Lambda để chạy các script tùy chỉnh để sao chép dữ liệu giữa các cơ sở dữ liệu.#<p>Lambda phù hợp cho các tác vụ hoạt động nhỏ, không phải di chuyển cơ sở dữ liệu lớn.</p>
	####<p><strong>Giải thích</strong>\: Khi di chuyển một cơ sở dữ liệu lớn đến AWS với thời gian ngừng hoạt động tối thiểu, Dịch vụ Di chuyển Cơ sở dữ liệu (DMS) có thể giúp ích.</p>
}

// question: 11.7  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Để cải thiện hiệu suất đọc của cơ sở dữ liệu RDS cho các ứng dụng có lượng đọc cao, bạn có thể triển khai gì?</p>{
	~[moodle]Tăng kích thước instance của cơ sở dữ liệu chính lên một loại instance mạnh hơn.#<p>Tăng kích thước instance chính cải thiện hiệu suất tổng thể nhưng không tối ưu hóa cụ thể cho workload đọc cao.</p>
	=[moodle]Thêm một hoặc nhiều read replica (bản sao chỉ đọc) để xử lý các yêu cầu đọc.
	~[moodle]Thay đổi loại bộ nhớ của cơ sở dữ liệu từ General Purpose SSD sang Magnetic.#<p>Magnetic storage có hiệu suất thấp nhất và không được khuyến nghị cho các workload sản xuất.</p>
	~[moodle]Di chuyển cơ sở dữ liệu sang một Availability Zone khác để phân tán tải.#<p>Di chuyển AZ có thể ảnh hưởng đến độ trễ và không trực tiếp giải quyết vấn đề mở rộng khả năng đọc.</p>
	####<p><strong>Giải thích</strong>\: Read replica được thiết kế để xử lý các yêu cầu đọc từ ứng dụng, giúp giảm tải cho cơ sở dữ liệu chính và cải thiện hiệu suất đọc tổng thể.</p>
}

// question: 11.8  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Điều nào sau đây là một yếu tố quan trọng CẦN xem xét khi sao chép snapshot cơ sở dữ liệu RDS sang một khu vực (region) khác?</p>{
	~[moodle]Chi phí sao chép snapshot giữa các khu vực luôn miễn phí trong AWS Free Tier.#<p>Chi phí sao chép snapshot không miễn phí.</p>
	~[moodle]Khả năng tương thích của snapshot với các công cụ cơ sở dữ liệu khác nhau ở khu vực đích.#<p>Snapshot RDS được gắn với một công cụ cơ sở dữ liệu cụ thể, và việc sao chép giữa các khu vực vẫn duy trì công cụ đó.</p>
	=[moodle]Các luật riêng tư và quy định tuân thủ dữ liệu có thể bị vi phạm khi dữ liệu vượt qua biên giới.
	~[moodle]Snapshot chỉ có thể được sao chép đến các khu vực không có Availability Zone.#<p>Các khu vực đều có Availability Zone.</p>
	####<p><strong>Giải thích</strong>\: Di chuyển dữ liệu từ một khu vực này sang khu vực khác có thể vi phạm luật riêng tư hoặc quy tắc tuân thủ, đặc biệt nếu dữ liệu vượt qua biên giới. Đảm bảo bạn được phép sao chép dữ liệu sang khu vực khác nếu bạn làm việc với dữ liệu thực.</p>
}

// question: 11.9  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Khi tăng kích thước của một instance RDS (ví dụ: từ db.t2.micro lên db.m3.large), các thay đổi nào sẽ xảy ra?</p>{
	~[moodle]Chỉ dung lượng lưu trữ của instance cơ sở dữ liệu được tăng lên, không ảnh hưởng đến CPU hoặc RAM.#<p>Dung lượng lưu trữ được quản lý riêng biệt.</p>
	~[moodle]Chỉ số lượng kết nối tối đa được hỗ trợ bởi cơ sở dữ liệu được tăng lên, không ảnh hưởng đến tài nguyên vật lý.#<p>Số lượng kết nối tối đa có thể tăng do tài nguyên lớn hơn, nhưng đó không phải là thay đổi trực tiếp duy nhất.</p>
	=[moodle]Sức mạnh tính toán và bộ nhớ của máy ảo cơ bản được tăng lên, cải thiện hiệu suất tổng thể.
	~[moodle]Cơ sở dữ liệu tự động được chuyển sang một Availability Zone khác để phân tán tải.#<p>Thay đổi kích thước instance không tự động thay đổi AZ; Multi-AZ là một cấu hình riêng biệt.</p>
	####<p><strong>Giải thích</strong>\: Khi bạn khởi động một cơ sở dữ liệu RDS, bạn chọn một loại instance. Loại instance xác định sức mạnh tính toán và bộ nhớ của máy ảo cơ bản của bạn. Chọn một loại instance lớn hơn sẽ tăng sức mạnh tính toán và bộ nhớ cho cơ sở dữ liệu RDS.</p>
}

// question: 11.10  name: Chapter 11: Sử dụng dịch vụ cơ sở dữ liệu quan hệ: RDS
::Chapter 11\: Sử dụng dịch vụ cơ sở dữ liệu quan hệ\: RDS::[html]<p>Để kiểm soát quyền truy cập mạng đến cơ sở dữ liệu RDS (ví dụ: cho phép lưu lượng truy cập từ các web server), bạn nên sử dụng dịch vụ AWS nào?</p>{
	~[moodle]Network Access Control Lists (ACLs) ở cấp độ subnet để định nghĩa các quy tắc lọc lưu lượng.#<p>ACLs là firewall không trạng thái hoạt động ở cấp độ subnet, trong khi security group là firewall trạng thái hoạt động ở cấp độ instance và linh hoạt hơn cho các quy tắc cụ thể.</p>
	~[moodle]IAM policies để xác định các quyền truy cập mạng cho các vai trò và người dùng.#<p>IAM kiểm soát quyền truy cập API, không phải quyền truy cập mạng trực tiếp đến endpoint cơ sở dữ liệu.</p>
	=[moodle]Security Groups được liên kết với instance RDS để định nghĩa các quy tắc firewall.
	~[moodle]VPC peering để kết nối cơ sở dữ liệu RDS với các mạng riêng bên ngoài.#<p>VPC peering dùng để kết nối các VPC, không phải để kiểm soát lưu lượng đến một instance cụ thể.</p>
	####<p><strong>Giải thích</strong>\: Cơ sở dữ liệu RDS được liên kết với security group. Mỗi security group bao gồm các quy tắc cho một firewall kiểm soát lưu lượng truy cập cơ sở dữ liệu đến và đi.</p>
}

// Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache

// question: 12.1  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>Amazon ElastiCache là một dịch vụ được quản lý cung cấp loại bộ nhớ đệm nào?</p>{
	~[moodle]Bộ nhớ đệm dựa trên ổ đĩa cứng (hard drive-based cache) để lưu trữ dữ liệu lớn với chi phí thấp.#<p>Đây không phải là mô tả chính xác của ElastiCache.</p>
	~[moodle]Bộ nhớ đệm cấp khối (block-level cache) để tăng tốc độ truy cập vào các volume EBS.#<p>Đây là một khái niệm khác, thường liên quan đến các hệ thống tệp cục bộ.</p>
	=[moodle]Bộ nhớ đệm trong bộ nhớ (in-memory data store) dựa trên Redis hoặc Memcached.
	~[moodle]Bộ nhớ đệm phân phối (distributed cache) dựa trên DynamoDB để lưu trữ cặp khóa-giá trị.#<p>DynamoDB là cơ sở dữ liệu NoSQL, không phải bộ nhớ đệm trong bộ nhớ.</p>
	####<p><strong>Giải thích</strong>\: ElastiCache là dịch vụ cung cấp các hệ thống cơ sở dữ liệu trong bộ nhớ được quản lý như Redis hoặc Memcached.</p>
}

// question: 12.2  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>Mục đích chính của việc sử dụng Amazon ElastiCache là gì trong một ứng dụng web?</p>{
	~[moodle]Để lưu trữ tất cả dữ liệu vĩnh viễn của ứng dụng và thay thế hoàn toàn cơ sở dữ liệu chính.#<p>ElastiCache không được thiết kế để thay thế cơ sở dữ liệu chính vì dữ liệu trong bộ nhớ không bền vững theo mặc định.</p>
	~[moodle]Để mã hóa tất cả dữ liệu nhạy cảm trước khi lưu trữ trong cơ sở dữ liệu quan hệ.#<p>Mã hóa là một khía cạnh bảo mật riêng biệt.</p>
	=[moodle]Để tăng tốc ứng dụng và giảm tải cho tầng cơ sở dữ liệu bằng cách lưu trữ dữ liệu thường xuyên truy cập trong bộ nhớ.
	~[moodle]Để quản lý các phiên người dùng (user sessions) trên nhiều instance EC2 một cách bền vững.#<p>Mặc dù ElastiCache có thể được sử dụng để lưu trữ phiên, đó không phải là mục đích chính duy nhất.</p>
	####<p><strong>Giải thích</strong>\: Chương 12 nói về việc thêm bộ nhớ đệm vào hạ tầng của bạn để tăng tốc ứng dụng và tiết kiệm chi phí do giảm thiểu tải trên tầng cơ sở dữ liệu. Cụ thể, bạn sẽ tìm hiểu về Amazon ElastiCache, cung cấp Redis hoặc Memcached dưới dạng dịch vụ. ElastiCache được sử dụng để lưu trữ dữ liệu trong bộ nhớ, thường là dữ liệu tạm thời hoặc dữ liệu thường xuyên truy cập để cải thiện tốc độ và giảm tải.</p>
}

// question: 12.3  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>So sánh giữa Redis và Memcached, Redis có đặc điểm nào mà Memcached không có?</p>{
	~[moodle]Redis hỗ trợ đa luồng (multi-threaded) để xử lý nhiều yêu cầu đồng thời một cách hiệu quả hơn.#<p>Memcached là đa luồng, trong khi Redis là đơn luồng.</p>
	=[moodle]Redis cung cấp các kiểu dữ liệu phức tạp hơn, giao dịch (transactions) và khả năng kịch bản hóa phía máy chủ (server-side scripting) bằng Lua.
	~[moodle]Redis được thiết kế để lưu trữ dữ liệu rất đơn giản dưới dạng cặp khóa-giá trị mà không cần tính năng nâng cao.#<p>Mô tả này phù hợp hơn với Memcached.</p>
	~[moodle]Redis có khả năng tự động mở rộng quy mô (auto-scaling) dựa trên tải CPU, trong khi Memcached không có.#<p>Cả hai đều được AWS quản lý và có thể mở rộng quy mô.</p>
	####<p><strong>Giải thích</strong>\: Bảng so sánh giữa Memcached và Redis cho thấy Redis có các kiểu dữ liệu phức tạp, 125 lệnh thao tác dữ liệu, hỗ trợ kịch bản hóa phía máy chủ (Lua) và giao dịch, trong khi Memcached có kiểu dữ liệu đơn giản và 12 lệnh.</p>
}

// question: 12.4  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>Để kiểm soát quyền truy cập mạng đến cluster ElastiCache, dịch vụ AWS nào được sử dụng?</p>{
	~[moodle]IAM policies để định nghĩa người dùng và vai trò có thể truy cập cluster.#<p>IAM kiểm soát quyền truy cập API của AWS, không phải truy cập dữ liệu trực tiếp trong ElastiCache.</p>
	=[moodle]Security Groups để định nghĩa các quy tắc firewall cho phép hoặc từ chối lưu lượng mạng đến cluster.
	~[moodle]Network Access Control Lists (ACLs) để lọc lưu lượng ở cấp độ subnet.#<p>ACLs là firewall không trạng thái hoạt động ở cấp độ subnet, kém linh hoạt hơn security group.</p>
	~[moodle]AWS WAF để bảo vệ cluster khỏi các cuộc tấn công web phổ biến.#<p>WAF bảo vệ các ứng dụng web, không phải là cơ chế kiểm soát truy cập mạng cho cơ sở dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: ElastiCache không thực hiện quản lý truy cập dữ liệu. Khi được kết nối với một key-value store, bạn có quyền truy cập vào tất cả dữ liệu. Để kiểm soát truy cập mạng đến cluster, bạn sử dụng Security Groups. Ví dụ, cho phép lưu lượng TCP trên cổng 6379 (cho Redis) từ security group của các instance EC2 ứng dụng.</p>
}

// question: 12.5  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>Khi nào bạn nên xem xét sử dụng sharding hoặc read replica cho cluster ElastiCache?</p>{
	~[moodle]Khi bạn cần lưu trữ tất cả dữ liệu của ứng dụng trong bộ nhớ mà không cần bền vững.#<p>Mặc dù ElastiCache lưu trữ trong bộ nhớ, nó không được khuyến nghị để lưu trữ tất cả dữ liệu vĩnh viễn.</p>
	=[moodle]Khi bạn muốn mở rộng quy mô theo chiều ngang (horizontally) để tăng thông lượng đọc và khả năng lưu trữ.
	~[moodle]Khi bạn muốn tối ưu hóa chi phí bằng cách sử dụng các node type nhỏ nhất.#<p>Node type nhỏ nhất được dùng để tiết kiệm chi phí, nhưng sharding/replica là để mở rộng.</p>
	~[moodle]Khi bạn cần mã hóa tất cả dữ liệu trong bộ nhớ để đáp ứng các yêu cầu tuân thủ.#<p>Mã hóa là một tính năng bảo mật riêng biệt, không phải mục đích của sharding/read replica.</p>
	####<p><strong>Giải thích</strong>\: Bạn có thể sử dụng sharding hoặc read replicas để mở rộng theo chiều ngang. Đây là một trong ba cách để tối ưu hóa hiệu suất bộ nhớ đệm.</p>
}

// question: 12.6  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>Điều nào sau đây là một yếu tố quan trọng để tối ưu hóa hiệu suất của bộ nhớ đệm ElastiCache?</p>{
	=[moodle]Tăng kích thước node type của bộ nhớ đệm để có thêm tài nguyên (CPU, bộ nhớ, mạng).
	~[moodle]Giảm thiểu số lượng node trong cluster để đơn giản hóa quản lý và giảm độ trễ.#<p>Giảm số lượng node có thể làm giảm khả năng mở rộng.</p>
	~[moodle]Vô hiệu hóa tính năng sao lưu tự động để tránh ảnh hưởng đến hiệu suất ghi.#<p>Vô hiệu hóa sao lưu có thể ảnh hưởng đến khả năng phục hồi dữ liệu.</p>
	~[moodle]Lưu trữ tất cả dữ liệu của ứng dụng trong bộ nhớ đệm, bất kể tần suất truy cập.#<p>Chỉ nên lưu trữ dữ liệu thường xuyên truy cập trong bộ nhớ đệm để đạt hiệu quả tối ưu.</p>
	####<p><strong>Giải thích</strong>\: Một trong những cách để điều chỉnh hiệu suất bộ nhớ đệm là chọn loại node bộ nhớ đệm phù hợp. Một loại instance lớn hơn đi kèm với nhiều tài nguyên hơn (CPU, bộ nhớ, mạng) để bạn có thể mở rộng theo chiều dọc.</p>
}

// question: 12.7  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>Khi thiết lập một cluster ElastiCache, "subnet group" có vai trò gì?</p>{
	~[moodle]Nó định nghĩa các quy tắc firewall để kiểm soát lưu lượng mạng đến các node trong cluster.#<p>Security Group định nghĩa các quy tắc firewall.</p>
	=[moodle]Nó xác định các subnet mà các node của cluster sẽ được khởi chạy trong đó.
	~[moodle]Nó nhóm các cluster ElastiCache lại với nhau để quản lý tập trung.#<p>Subnet group không nhóm các cluster lại với nhau.</p>
	~[moodle]Nó chỉ định loại bộ nhớ đệm (Redis hoặc Memcached) sẽ được sử dụng cho cluster.#<p>Loại bộ nhớ đệm được chỉ định bằng thuộc tính Engine.</p>
	####<p><strong>Giải thích</strong>\: Subnet group của ElastiCache là một bộ sưu tập các subnet mà bạn chỉ định trong VPC của bạn. Điều này cho phép ElastiCache khởi chạy các node cluster của bạn trong các subnet đó.</p>
}

// question: 12.8  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>Giả sử bạn đang chạy một ứng dụng Ruby on Rails (như Discourse) và cần một bộ nhớ đệm trong bộ nhớ. ElastiCache có thể cung cấp loại công cụ nào cho mục đích này?</p>{
	~[moodle]Amazon S3 cho lưu trữ đối tượng và bộ nhớ đệm tĩnh.#<p>Các dịch vụ này không phải là bộ nhớ đệm trong bộ nhớ mà ElastiCache cung cấp.</p>
	~[moodle]Amazon DynamoDB cho bộ nhớ đệm dựa trên NoSQL.#<p>Các dịch vụ này không phải là bộ nhớ đệm trong bộ nhớ mà ElastiCache cung cấp.</p>
	=[moodle]Redis hoặc Memcached cho bộ nhớ đệm trong bộ nhớ.
	~[moodle]Amazon RDS cho bộ nhớ đệm dựa trên cơ sở dữ liệu quan hệ.#<p>Các dịch vụ này không phải là bộ nhớ đệm trong bộ nhớ mà ElastiCache cung cấp.</p>
	####<p><strong>Giải thích</strong>\: Discourse yêu cầu một Redis cache và PostgreSQL làm kho dữ liệu chính. ElastiCache cung cấp Redis hoặc Memcached làm dịch vụ.</p>
}

// question: 12.9  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>Điều nào sau đây KHÔNG phải là lợi ích của việc sử dụng một dịch vụ bộ nhớ đệm như ElastiCache?</p>{
	~[moodle]Giảm tải trên cơ sở dữ liệu chính bằng cách phục vụ dữ liệu từ bộ nhớ đệm.
	~[moodle]Tăng tốc độ phản hồi của ứng dụng bằng cách giảm độ trễ truy xuất dữ liệu.
	=[moodle]Đảm bảo tính bền vững và toàn vẹn dữ liệu cho tất cả dữ liệu được lưu trữ, ngay cả sau khi mất điện.
	~[moodle]Giảm chi phí vận hành cơ sở hạ tầng bằng cách tối ưu hóa việc sử dụng tài nguyên.
	####<p><strong>Giải thích</strong>\: ElastiCache là bộ nhớ đệm trong bộ nhớ, và dữ liệu trong bộ nhớ thường không bền vững theo mặc định (trừ khi được cấu hình đặc biệt để duy trì dữ liệu, nhưng đó không phải là đặc điểm tự nhiên của "cache"). Các dịch vụ này được thiết kế để tăng tốc và giảm tải, nhưng không phải để đảm bảo tính bền vững hoàn toàn cho tất cả dữ liệu.</p>
}

// question: 12.10  name: Chapter 12: Bộ nhớ đệm dữ liệu trong bộ nhớ: Amazon ElastiCache
::Chapter 12\: Bộ nhớ đệm dữ liệu trong bộ nhớ\: Amazon ElastiCache::[html]<p>Khi nào bạn nên chỉ định rõ ràng phiên bản của công cụ ElastiCache (ví dụ: EngineVersion: '3.2.4' cho Redis) trong CloudFormation?</p>{
	~[moodle]Luôn luôn sử dụng phiên bản mới nhất để đảm bảo bạn có các tính năng và bản vá bảo mật mới nhất.#<p>Mặc dù các tính năng mới là tốt, nhưng việc tự động cập nhật phiên bản mới nhất có thể gây ra lỗi không mong muốn cho ứng dụng của bạn nếu có thay đổi phá vỡ tương thích.</p>
	~[moodle]Chỉ khi bạn gặp phải lỗi không tương thích với các phiên bản cũ hơn của công cụ.#<p>Việc chỉ định phiên bản giúp chủ động tránh lỗi, không chỉ khắc phục khi đã xảy ra.</p>
	=[moodle]Nên luôn chỉ định phiên bản để tránh các vấn đề không tương thích trong tương lai nếu các phiên bản mới được giới thiệu.
	~[moodle]Không cần thiết, vì ElastiCache tự động quản lý việc cập nhật phiên bản một cách liền mạch.#<p>ElastiCache quản lý việc cập nhật, nhưng không phải lúc nào cũng liền mạch cho các ứng dụng không được chuẩn bị trước cho các thay đổi phiên bản.</p>
	####<p><strong>Giải thích</strong>\: Bạn có thể chỉ định phiên bản chính xác của Redis mà bạn muốn chạy. Nếu không, phiên bản mới nhất sẽ được sử dụng, điều này có thể gây ra các vấn đề không tương thích trong tương lai. Chúng tôi khuyến nghị luôn chỉ định phiên bản.</p>
}

// Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB

// question: 13.1  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>Amazon DynamoDB được phân loại là loại cơ sở dữ liệu nào và đặc điểm chính của nó là gì?</p>{
	~[moodle]Cơ sở dữ liệu quan hệ (relational database) hỗ trợ SQL với schema cố định và giao dịch ACID.#<p>Đây là mô tả của các dịch vụ RDS.</p>
	=[moodle]Cơ sở dữ liệu NoSQL kiểu cặp khóa-giá trị (key-value database) độc quyền của AWS với khả năng mở rộng tự động.
	~[moodle]Cơ sở dữ liệu đồ thị (graph database) tối ưu cho việc lưu trữ và truy vấn các mối quan hệ phức tạp.#<p>Neo4j là một ví dụ về cơ sở dữ liệu đồ thị.</p>
	~[moodle]Cơ sở dữ liệu tài liệu (document database) tương thích với MongoDB, lý tưởng cho dữ liệu JSON.#<p>MongoDB là một ví dụ về cơ sở dữ liệu tài liệu.</p>
	####<p><strong>Giải thích</strong>\: DynamoDB là cơ sở dữ liệu NoSQL kiểu cặp khóa-giá trị độc quyền của AWS, được thiết kế để mở rộng quy mô một cách liền mạch.</p>
}

// question: 13.2  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>Amazon DynamoDB xử lý việc mở rộng dung lượng lưu trữ như thế nào khi bạn thêm nhiều item vào một bảng?</p>{
	~[moodle]Bạn cần thủ công cung cấp thêm dung lượng lưu trữ bằng cách điều chỉnh kích thước volume EBS được gắn vào.#<p>Đây là cách quản lý lưu trữ cho các cơ sở dữ liệu tự lưu trữ trên EC2 với EBS.</p>
	=[moodle]Dung lượng lưu trữ của cơ sở dữ liệu tự động tăng lên khi bạn thêm nhiều item mà không cần hành động thủ công nào.
	~[moodle]Bạn phải định nghĩa các sharding key để phân tán dữ liệu trên nhiều bảng khi dung lượng tăng lên.#<p>DynamoDB quản lý sharding nội bộ, bạn chỉ cần định nghĩa khóa chính.</p>
	~[moodle]DynamoDB sẽ tự động chuyển dữ liệu cũ hơn sang Amazon Glacier để giải phóng dung lượng cho dữ liệu mới.#<p>DynamoDB không tự động chuyển dữ liệu sang Glacier.</p>
	####<p><strong>Giải thích</strong>\: Không cần hành động nào: DynamoDB tự động phát triển cùng với các item của bạn. Bạn không cần phải cung cấp thêm bộ nhớ cho DynamoDB.</p>
}

// question: 13.3  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>Để mở rộng hiệu suất của DynamoDB (tăng ReadCapacityUnits hoặc WriteCapacityUnits), cách tiếp cận nào được thực hiện?</p>{
	~[moodle]Mở rộng theo chiều dọc bằng cách tăng kích thước instance cơ sở dữ liệu và thông lượng ổ đĩa.#<p>Đây là cách mở rộng theo chiều dọc cho các cơ sở dữ liệu quan hệ tự quản lý hoặc RDS.</p>
	=[moodle]Mở rộng theo chiều ngang bằng cách thêm nhiều máy chủ dưới nền mà DynamoDB tự động quản lý.
	~[moodle]Tắt tính năng sao lưu tự động để giải phóng tài nguyên hệ thống cho các yêu cầu I/O.#<p>Tắt sao lưu có thể gây mất dữ liệu và không phải là giải pháp mở rộng hiệu suất.</p>
	~[moodle]Sử dụng bộ nhớ đệm trong bộ nhớ như ElastiCache để giảm tải cho DynamoDB.#<p>Sử dụng ElastiCache là một chiến lược tối ưu hóa, nhưng không phải là cách DynamoDB tự mở rộng.</p>
	####<p><strong>Giải thích</strong>\: Để tăng hiệu suất (Capacity Units), DynamoDB mở rộng theo chiều ngang bằng cách thêm nhiều máy chủ dưới nền. Đây là một trong những lợi ích chính của DynamoDB so với các cơ sở dữ liệu quan hệ.</p>
}

// question: 13.4  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>Khi sử dụng DynamoDB, điều nào sau đây là đúng về schema của bảng?</p>{
	~[moodle]Mỗi item trong một bảng phải có cùng tập hợp các thuộc tính (attributes) và kiểu dữ liệu.#<p>Các lựa chọn này mô tả schema cố định, là đặc điểm của cơ sở dữ liệu quan hệ, không phải DynamoDB.</p>
	~[moodle]Schema của bảng phải được định nghĩa rõ ràng trước khi thêm bất kỳ item nào và không thể thay đổi sau đó.#<p>Các lựa chọn này mô tả schema cố định, là đặc điểm của cơ sở dữ liệu quan hệ, không phải DynamoDB.</p>
	=[moodle]Các item trong một bảng không bắt buộc phải có cùng các thuộc tính; không có schema cố định (enforced schema).
	~[moodle]DynamoDB tự động tạo schema dựa trên item đầu tiên được thêm vào bảng.#<p>DynamoDB không tự động tạo schema; bạn chỉ định khóa chính khi tạo bảng.</p>
	####<p><strong>Giải thích</strong>\: Các item trong một bảng không bắt buộc phải có cùng các thuộc tính; không có schema cố định. Đây là một đặc điểm của cơ sở dữ liệu NoSQL.</p>
}

// question: 13.5  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>Để truy vấn dữ liệu trong DynamoDB dựa trên các thuộc tính không phải là khóa chính một cách hiệu quả, bạn nên sử dụng tính năng nào?</p>{
	~[moodle]Scan và Filter toàn bộ bảng, sau đó lọc kết quả ở phía client.#<p>Scan và Filter toàn bộ bảng sẽ rất chậm và tốn kém khi kích thước bảng lớn, vì nó yêu cầu kiểm tra mọi item.</p>
	=[moodle]Secondary indexes (chỉ mục phụ) như Global Secondary Index (GSI) hoặc Local Secondary Index (LSI).
	~[moodle]Chuyển đổi bảng DynamoDB thành cơ sở dữ liệu quan hệ để sử dụng câu lệnh SQL SELECT.#<p>DynamoDB là NoSQL, không hỗ trợ SQL trực tiếp.</p>
	~[moodle]Xuất dữ liệu sang Amazon S3, sau đó chạy các truy vấn phân tích bằng Amazon Redshift.#<p>Đây là một giải pháp phân tích, không phải để truy vấn dữ liệu trực tiếp trong DynamoDB.</p>
	####<p><strong>Giải thích</strong>\: Hai vấn đề phát sinh với cách tiếp cận truy vấn trên khóa chính: Lọc có thể chậm tùy thuộc vào kích thước kết quả từ truy vấn khóa chính. Để giải quyết điều đó, bạn có thể tạo secondary indexes.</p>
}

// question: 13.6  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>DynamoDB Local được sử dụng cho mục đích gì?</p>{
	~[moodle]Để triển khai một phiên bản DynamoDB tự quản lý trong môi trường sản xuất của bạn.#<p>DynamoDB Local không được khuyến nghị cho môi trường sản xuất.</p>
	=[moodle]Để mô phỏng DynamoDB trên máy cục bộ của nhà phát triển cho mục đích phát triển và thử nghiệm ngoại tuyến.
	~[moodle]Để kết nối DynamoDB với các cơ sở dữ liệu on-premises thông qua VPN.#<p>Không phải mục đích chính.</p>
	~[moodle]Để chạy các tác vụ phân tích dữ liệu lớn trực tiếp trên dữ liệu DynamoDB mà không cần xuất.#<p>Không phải mục đích chính.</p>
	####<p><strong>Giải thích</strong>\: AWS cung cấp một triển khai của DynamoDB, có sẵn để tải xuống. Nó chỉ được dùng cho mục đích phát triển và cung cấp chức năng tương tự như DynamoDB, nhưng sử dụng một triển khai khác: chỉ API là giống nhau.</p>
}

// question: 13.7  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>Mô hình nhất quán mặc định (default consistency model) của DynamoDB là gì?</p>{
	~[moodle]Strongly Consistent Reads (Đọc nhất quán mạnh), đảm bảo bạn luôn đọc được dữ liệu mới nhất.#<p>Strongly Consistent Reads có thể được yêu cầu, nhưng tốn kém hơn và có độ trễ cao hơn.</p>
	=[moodle]Eventually Consistent Reads (Đọc nhất quán cuối cùng), có nghĩa là bạn có thể đọc dữ liệu cũ trong một thời gian ngắn.
	~[moodle]Read-after-write consistency (Nhất quán đọc-sau-ghi), đảm bảo mọi yêu cầu đọc sau khi ghi sẽ trả về dữ liệu mới nhất.#<p>Read-after-write consistency không phải là mô hình mặc định.</p>
	~[moodle]Serializability (Tính tuần tự), đảm bảo các giao dịch thực hiện theo một thứ tự tuần tự toàn cầu.#<p>Đây là một mức độ cô lập giao dịch cao hơn, không phải mô hình nhất quán dữ liệu của DynamoDB.</p>
	####<p><strong>Giải thích</strong>\: Các đọc nhất quán cuối cùng là mặc định. Bạn có thể đọc dữ liệu đã cũ trong một khoảng thời gian ngắn. Sau khi ghi, bạn có thể đọc phiên bản cũ của dữ liệu.</p>
}

// question: 13.8  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>DynamoDB Auto Scaling giúp bạn quản lý ReadCapacityUnits (RCU) và WriteCapacityUnits (WCU) như thế nào?</p>{
	~[moodle]Bằng cách cho phép bạn thủ công điều chỉnh RCU và WCU dựa trên phân tích workload hàng ngày.#<p>Đây là cách tiếp cận thủ công, auto scaling được tạo ra để tự động hóa điều này.</p>
	=[moodle]Bằng cách tự động điều chỉnh RCU và WCU của bảng dựa trên mức sử dụng thực tế để duy trì hiệu suất mong muốn.
	~[moodle]Bằng cách chuyển đổi các yêu cầu WCU dư thừa thành RCU khi workload đọc tăng lên.#<p>Không có cơ chế chuyển đổi tự động giữa WCU và RCU.</p>
	~[moodle]Bằng cách giới hạn RCU và WCU ở một mức cố định để tránh chi phí không mong muốn.#<p>Auto scaling được thiết kế để điều chỉnh, không phải giới hạn ở một mức cố định.</p>
	####<p><strong>Giải thích</strong>\: DynamoDB auto scaling giúp bạn quản lý thông lượng của bảng bằng cách tự động điều chỉnh ReadCapacityUnits (RCU) và WriteCapacityUnits (WCU) khi lưu lượng truy cập thay đổi. Điều này giúp tránh việc cung cấp quá mức hoặc thiếu hụt tài nguyên.</p>
}

// question: 13.9  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>Giả sử bạn đang phát triển một ứng dụng to-do list và cần lưu trữ các task. Mỗi task có thể có một uid (user ID) và một tid (task ID). Loại khóa chính nào bạn nên sử dụng trong DynamoDB để có thể truy vấn tất cả các task của một người dùng cụ thể và cũng có thể sắp xếp chúng?</p>{
	~[moodle]Chỉ Partition Key là tid.#<p>Chỉ một Partition Key sẽ không cho phép bạn truy vấn hoặc sắp xếp các task của một người dùng một cách hiệu quả.</p>
	~[moodle]Chỉ Partition Key là uid.#<p>Chỉ một Partition Key sẽ không cho phép bạn truy vấn hoặc sắp xếp các task của một người dùng một cách hiệu quả.</p>
	=[moodle]Partition Key là uid và Sort Key là tid.
	~[moodle]Global Secondary Index trên tid.#<p>Global Secondary Index sẽ tốt để truy vấn trên tid cho tất cả người dùng, nhưng để truy vấn tất cả các task của một người dùng, khóa chính uid/tid là tối ưu.</p>
	####<p><strong>Giải thích</strong>\: Để truy vấn tất cả các task của một người dùng cụ thể, uid nên là Partition Key. Để sắp xếp hoặc lọc các task đó (ví dụ: theo thời gian tạo hoặc ID task), tid nên là Sort Key. Khóa chính kết hợp (Partition Key + Sort Key) cho phép các truy vấn hiệu quả trên cả hai thuộc tính.</p>
}

// question: 13.10  name: Chapter 13: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL: DynamoDB
::Chapter 13\: Lập trình cho dịch vụ cơ sở dữ liệu NoSQL\: DynamoDB::[html]<p>Khi nào bạn nên sử dụng Global Secondary Index trong DynamoDB?</p>{
	~[moodle]Khi bạn cần một chỉ mục cho các truy vấn chỉ sử dụng Partition Key của bảng.#<p>Đây là chức năng của khóa chính.</p>
	~[moodle]Khi bạn cần một chỉ mục cho các truy vấn yêu cầu lọc trên Sort Key của bảng.#<p>LSI (Local Secondary Index) được sử dụng cho điều này.</p>
	=[moodle]Khi bạn cần một chỉ mục cho các truy vấn trên các thuộc tính không phải là khóa chính của bảng.
	~[moodle]Khi bạn cần một chỉ mục để đảm bảo tính nhất quán mạnh (strongly consistent reads) cho tất cả các truy vấn.#<p>GSI có mô hình nhất quán cuối cùng.</p>
	####<p><strong>Giải thích</strong>\: Bạn có thể sử dụng Global Secondary Index (GSI) cho các truy vấn linh hoạt hơn. GSI cho phép bạn truy vấn trên các thuộc tính không phải là khóa chính của bảng.</p>
}

// Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch

// question: 14.1  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>Trong AWS, Availability Zone (AZ) được định nghĩa là gì?</p>{
	~[moodle]Một trung tâm dữ liệu duy nhất trong một khu vực địa lý lớn để lưu trữ tài nguyên AWS.#<p>Một AZ có thể là một hoặc nhiều trung tâm dữ liệu nhưng được thiết kế để độc lập.</p>
	=[moodle]Một nhóm các trung tâm dữ liệu được cô lập về mặt vật lý trong một khu vực, được thiết kế để chống lại lỗi riêng biệt.
	~[moodle]Một khu vực địa lý lớn bao gồm nhiều khu vực để phân tán ứng dụng toàn cầu.#<p>Đây là mô tả của một Region.</p>
	~[moodle]Một dịch vụ mạng đặc biệt để kết nối các trung tâm dữ liệu khác nhau trên toàn cầu.#<p>Không phải là định nghĩa của AZ.</p>
	####<p><strong>Giải thích</strong>\: Mỗi khu vực bao gồm nhiều Availability Zone (AZs). Bạn có thể coi một AZ là một nhóm trung tâm dữ liệu được cô lập, và một khu vực là một khu vực nơi nhiều Availability Zone được đặt cách nhau một khoảng đủ lớn.</p>
}

// question: 14.2  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>Sự khác biệt chính giữa hệ thống sẵn sàng cao (highly available system) và hệ thống chịu lỗi (fault-tolerant system) là gì?</p>{
	=[moodle]Hệ thống sẵn sàng cao có thể phục hồi tự động sau lỗi với thời gian ngừng hoạt động ngắn, trong khi hệ thống chịu lỗi cung cấp dịch vụ không bị gián đoạn.
	~[moodle]Hệ thống sẵn sàng cao chỉ áp dụng cho tầng ứng dụng, trong khi hệ thống chịu lỗi áp dụng cho toàn bộ cơ sở hạ tầng.#<p>Các lựa chọn này không mô tả chính xác sự khác biệt cơ bản giữa hai khái niệm.</p>
	~[moodle]Hệ thống sẵn sàng cao đòi hỏi chi phí đầu tư ban đầu cao hơn nhiều so với hệ thống chịu lỗi.#<p>Các lựa chọn này không mô tả chính xác sự khác biệt cơ bản giữa hai khái niệm.</p>
	~[moodle]Hệ thống sẵn sàng cao chỉ có thể được triển khai trong một Availability Zone duy nhất, trong khi hệ thống chịu lỗi yêu cầu nhiều AZ.#<p>Các lựa chọn này không mô tả chính xác sự khác biệt cơ bản giữa hai khái niệm.</p>
	####<p><strong>Giải thích</strong>\: Hệ thống sẵn sàng cao có thể phục hồi tự động sau lỗi với thời gian ngừng hoạt động ngắn. Ngược lại, hệ thống chịu lỗi yêu cầu hệ thống cung cấp dịch vụ mà không bị gián đoạn trong trường hợp có lỗi thành phần.</p>
}

// question: 14.3  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>Recovery Time Objective (RTO) được định nghĩa là gì trong ngữ cảnh phục hồi sau thảm họa?</p>{
	~[moodle]Khoảng thời gian chấp nhận được về dữ liệu bị mất do lỗi hệ thống.#<p>Đây là định nghĩa của Recovery Point Objective (RPO).</p>
	=[moodle]Thời gian cần thiết để hệ thống phục hồi từ một lỗi và đạt được trạng thái hoạt động trở lại.
	~[moodle]Số lượng snapshot tự động được tạo ra trong một ngày để đảm bảo phục hồi.#<p>Các lựa chọn này không phải là định nghĩa của RTO.</p>
	~[moodle]Khả năng chịu lỗi của một ứng dụng khi một trong các thành phần của nó gặp sự cố.#<p>Các lựa chọn này không phải là định nghĩa của RTO.</p>
	####<p><strong>Giải thích</strong>\: Recovery Time Objective (RTO) là thời gian để một hệ thống phục hồi từ một lỗi; đó là khoảng thời gian cho đến khi hệ thống đạt được trạng thái hoạt động trở lại, được định nghĩa là mức độ dịch vụ hệ thống, sau một sự cố.</p>
}

// question: 14.4  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>Các volume EBS được liên kết với một Availability Zone cụ thể như thế nào khi một instance EC2 bị lỗi và cần phục hồi trong một AZ khác?</p>{
	~[moodle]Volume EBS tự động được di chuyển đến AZ mới cùng với instance EC2 để đảm bảo truy cập.#<p>Các lựa chọn này sai vì EBS không có khả năng tự động di chuyển hoặc sao chép giữa các AZ.</p>
	=[moodle]Volume EBS bị ràng buộc với một AZ duy nhất và không thể truy cập được từ một AZ khác.
	~[moodle]Volume EBS được sao chép tự động sang tất cả các AZ trong khu vực để đảm bảo tính sẵn sàng cao.#<p>Các lựa chọn này sai vì EBS không có khả năng tự động di chuyển hoặc sao chép giữa các AZ.</p>
	~[moodle]AWS sẽ tự động tạo một bản sao của volume EBS trong AZ mới khi instance phục hồi.#<p>Các lựa chọn này sai vì EBS không có khả năng tự động di chuyển hoặc sao chép giữa các AZ.</p>
	####<p><strong>Giải thích</strong>\: Các volume EBS cũng chỉ nằm trong một Availability Zone duy nhất. Nếu máy ảo của bạn được khởi động trong một Availability Zone khác do một sự cố, volume EBS không thể được truy cập từ Availability Zone khác.</p>
}

// question: 14.5  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>Để khắc phục hạn chế của volume EBS khi cần bộ nhớ được chia sẻ và khả năng phục hồi sau lỗi AZ cho instance EC2, bạn có thể sử dụng dịch vụ nào?</p>{
	~[moodle]Amazon S3 để lưu trữ dữ liệu đối tượng được chia sẻ và có sẵn toàn cầu.#<p>S3 là bộ nhớ đối tượng, không phải hệ thống tệp và không phải là bộ nhớ cấp khối.</p>
	=[moodle]Amazon EFS để cung cấp bộ nhớ cấp khối (qua NFSv4.1) và nhân bản dữ liệu tự động giữa các AZ.
	~[moodle]Amazon DynamoDB để lưu trữ dữ liệu có cấu trúc và truy cập từ bất kỳ AZ nào.#<p>DynamoDB là cơ sở dữ liệu NoSQL, không phải hệ thống tệp được chia sẻ.</p>
	~[moodle]Amazon Glacier để lưu trữ dữ liệu dài hạn và có thể truy xuất từ bất kỳ AZ nào khi cần.#<p>Glacier là dịch vụ lưu trữ đối tượng chi phí thấp cho dữ liệu ít truy cập, không phải bộ nhớ cấp khối.</p>
	####<p><strong>Giải thích</strong>\: Để giải quyết vấn đề bộ nhớ được chia sẻ giữa các AZ cho instance EC2, EFS cung cấp bộ nhớ cấp khối (qua NFSv4.1) và nhân bản dữ liệu tự động giữa các Availability Zone trong một khu vực.</p>
}

// question: 14.6  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>Khi sử dụng Auto Scaling Group (ASG), điều gì sẽ xảy ra nếu một instance EC2 bị lỗi?</p>{
	~[moodle]ASG sẽ cố gắng phục hồi instance bị lỗi trong cùng một Availability Zone, không khởi chạy instance mới.#<p>ASG có thể khởi chạy instance mới trong cùng hoặc các AZ khác tùy cấu hình.</p>
	=[moodle]ASG sẽ tự động phát hiện lỗi và khởi chạy một instance EC2 mới dựa trên cấu hình khởi chạy để thay thế.
	~[moodle]ASG sẽ gửi thông báo đến người quản trị và chờ họ thủ công khởi chạy một instance thay thế.#<p>ASG được thiết kế để tự động hóa việc phục hồi, không yêu cầu can thiệp thủ công ngay lập tức.</p>
	~[moodle]ASG sẽ tạm thời giảm kích thước mong muốn (DesiredCapacity) của nhóm để tiết kiệm chi phí.#<p>ASG sẽ duy trì số lượng instance mong muốn.</p>
	####<p><strong>Giải thích</strong>\: Auto Scaling Group (ASG) quan sát một nhóm máy chủ: Thay thế các máy chủ bị lỗi và tăng/giảm kích thước của nhóm dựa trên các trigger bên ngoài như mức sử dụng CPU.</p>
}

// question: 14.7  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>Điều nào sau đây là LỢI ÍCH của việc sử dụng Elastic IP (EIP) khi phục hồi instance EC2 bằng Auto Scaling Group trên nhiều AZ?</p>{
	~[moodle]Elastic IP cung cấp một địa chỉ IP riêng tĩnh cho instance EC2, không thay đổi sau khi phục hồi.#<p>EIP là địa chỉ IP công cộng tĩnh.</p>
	=[moodle]Elastic IP cho phép địa chỉ IP công cộng của instance EC2 không thay đổi sau khi phục hồi, duy trì endpoint ứng dụng.
	~[moodle]Elastic IP tự động cân bằng tải lưu lượng truy cập đến các instance EC2 trong ASG.#<p>Elastic Load Balancing là dịch vụ cân bằng tải.</p>
	~[moodle]Elastic IP giảm chi phí chuyển dữ liệu giữa các Availability Zone trong khu vực.#<p>EIP không trực tiếp giảm chi phí chuyển dữ liệu.</p>
	####<p><strong>Giải thích</strong>\: Việc cấp phát Elastic IP và liên kết nó với instance EC2 cho bạn sự linh hoạt để thay thế một VM mà không thay đổi địa chỉ IP công cộng. Khi sử dụng EIP với auto-scaling, địa chỉ IP công cộng của ứng dụng không thay đổi, cho phép ứng dụng phục hồi mà không ảnh hưởng đến người dùng.</p>
}

// question: 14.8  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>Để giảm RPO (Recovery Point Objective) xuống bằng 0 khi instance EC2 bị lỗi, bạn nên áp dụng nguyên tắc kiến trúc nào?</p>{
	~[moodle]Lưu trữ tất cả dữ liệu trên các volume Instance Store để đạt hiệu suất cao nhất.#<p>Instance Store là bộ nhớ tạm thời và dữ liệu sẽ bị mất khi instance bị lỗi.</p>
	=[moodle]Đảm bảo server không trạng thái (stateless) và sử dụng các dịch vụ lưu trữ như RDS, EFS, S3, DynamoDB.
	~[moodle]Triển khai tất cả các instance EC2 trong một Availability Zone duy nhất để đơn giản hóa việc quản lý dữ liệu.#<p>Triển khai trong một AZ duy nhất tạo ra điểm lỗi duy nhất và tăng RPO nếu AZ đó gặp sự cố.</p>
	~[moodle]Tạo snapshot thủ công của các volume EBS cứ sau vài giờ để giảm thiểu mất dữ liệu.#<p>Snapshot thủ công vẫn có thể dẫn đến mất dữ liệu trong khoảng thời gian giữa các snapshot.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn muốn có thể phục hồi sau một sự cố Availability Zone và cần giảm RPO, bạn nên cố gắng đạt được một server không trạng thái. Sử dụng các dịch vụ lưu trữ như RDS, EFS, S3 và DynamoDB có thể giúp bạn làm điều đó.</p>
}

// question: 14.9  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>CloudWatch alarm được sử dụng để theo dõi tình trạng của instance EC2 và kích hoạt hành động phục hồi như thế nào?</p>{
	~[moodle]Bằng cách gửi thông báo email đến người quản trị khi instance EC2 bị lỗi.#<p>Gửi email là một hành động báo động, nhưng CloudWatch có thể kích hoạt hành động phục hồi tự động.</p>
	=[moodle]Bằng cách giám sát chỉ số StatusCheckFailed_System và kích hoạt hành động phục hồi nếu ngưỡng bị vượt quá.
	~[moodle]Bằng cách tự động khởi động lại hệ điều hành của instance EC2 khi phát hiện lỗi ứng dụng.#<p>Hành động phục hồi là khởi chạy instance mới, không chỉ khởi động lại HĐH.</p>
	~[moodle]Bằng cách thay đổi loại instance EC2 sang một loại nhỏ hơn để tiết kiệm chi phí trong thời gian lỗi.#<p>Không phải là hành động phục hồi tiêu chuẩn.</p>
	####<p><strong>Giải thích</strong>\: AWS kiểm tra trạng thái của máy ảo mỗi phút. Kết quả của các kiểm tra này được ghi vào chỉ số StatusCheckFailed_System. Báo động kiểm tra chỉ số này. Nếu có năm lần kiểm tra lỗi liên tiếp, báo động sẽ được kích hoạt.</p>
}

// question: 14.10  name: Chapter 14: Đạt được tính sẵn sàng cao: Availability Zone, Auto-Scaling và CloudWatch
::Chapter 14\: Đạt được tính sẵn sàng cao\: Availability Zone, Auto-Scaling và CloudWatch::[html]<p>Khi xây dựng một kiến trúc sẵn sàng cao (High Availability) trên AWS, bạn nên phân tán các instance EC2 của mình như thế nào?</p>{
	~[moodle]Triển khai tất cả các instance trong cùng một subnet để đảm bảo giao tiếp mạng nhanh chóng.#<p>Triển khai trong một subnet có thể tạo ra điểm lỗi duy nhất.</p>
	=[moodle]Phân tán các instance trên nhiều Availability Zone trong cùng một khu vực để giảm thiểu tác động của lỗi AZ.
	~[moodle]Triển khai các instance trên nhiều khu vực (regions) khác nhau để đạt được tính sẵn sàng toàn cầu.#<p>Triển khai trên nhiều khu vực là để phục hồi sau thảm họa khu vực, không phải cho HA cơ bản.</p>
	~[moodle]Sử dụng một instance EC2 duy nhất và cấu hình nó với tất cả các tùy chọn dự phòng có thể.#<p>Một instance duy nhất luôn là một điểm lỗi duy nhất.</p>
	####<p><strong>Giải thích</strong>\: Bạn có thể sử dụng các Availability Zone để xây dựng một kiến trúc có tính sẵn sàng cao. Việc phân tán các instance EC2 trên nhiều AZ cho phép hệ thống tiếp tục hoạt động nếu một AZ gặp sự cố.</p>
}

// Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service

// question: 15.1  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Elastic Load Balancing (ELB) được sử dụng để đạt được loại phân tách nào giữa các client và các instance EC2?</p>{
	~[moodle]Phân tách không đồng bộ (asynchronous decoupling) để xử lý các tác vụ nền.#<p>SQS là ví dụ về phân tách không đồng bộ.</p>
	=[moodle]Phân tách đồng bộ (synchronous decoupling) để phân phối yêu cầu theo thời gian thực.
	~[moodle]Phân tách dữ liệu (data decoupling) để tách biệt lưu trữ dữ liệu khỏi ứng dụng.#<p>Các lựa chọn này không mô tả loại phân tách chính mà ELB cung cấp.</p>
	~[moodle]Phân tách bảo mật (security decoupling) để mã hóa tất cả lưu lượng mạng.#<p>Các lựa chọn này không mô tả loại phân tách chính mà ELB cung cấp.</p>
	####<p><strong>Giải thích</strong>\: Cân bằng tải có thể được sử dụng với nhiều hơn các máy chủ web — bạn có thể sử dụng cân bằng tải trước bất kỳ hệ thống nào xử lý giao tiếp kiểu yêu cầu/phản hồi miễn là giao thức dựa trên TCP. ELB là một ví dụ về phân tách đồng bộ.</p>
}

// question: 15.2  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Amazon Simple Queue Service (SQS) được sử dụng chủ yếu để đạt được loại phân tách nào trong kiến trúc ứng dụng?</p>{
	~[moodle]Phân tách đồng bộ (synchronous decoupling) để cân bằng tải lưu lượng truy cập web theo thời gian thực.#<p>Đây là mục đích của ELB.</p>
	=[moodle]Phân tách không đồng bộ (asynchronous decoupling) để xử lý các tác vụ trong nền mà không làm chậm ứng dụng chính.
	~[moodle]Phân tách dữ liệu (data decoupling) để lưu trữ dữ liệu ở các tầng khác nhau với các mô hình nhất quán khác nhau.#<p>Các lựa chọn này không mô tả loại phân tách chính mà SQS cung cấp.</p>
	~[moodle]Phân tách tính sẵn sàng (availability decoupling) để đảm bảo ứng dụng luôn hoạt động ngay cả khi một thành phần bị lỗi.#<p>Các lựa chọn này không mô tả loại phân tách chính mà SQS cung cấp.</p>
	####<p><strong>Giải thích</strong>\: Chương này giới thiệu khái niệm phân tách hệ thống của bạn để tăng độ tin cậy. Bạn sẽ tìm hiểu cách sử dụng phân tách đồng bộ với sự trợ giúp của Elastic Load Balancing (ELB). Phân tách không đồng bộ cũng là một phần của chương này; chúng tôi giải thích cách sử dụng Amazon Simple Queue Service (SQS), một dịch vụ xếp hàng phân tán, để xây dựng một hệ thống chịu lỗi. SQS dùng để biến một quy trình đồng bộ thành không đồng bộ.</p>
}

// question: 15.3  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Điều nào sau đây KHÔNG phải là lợi ích chính của Amazon SQS?</p>{
	~[moodle]Khả năng đặt nhiều tin nhắn vào hàng đợi SQS mà không có giới hạn về số lượng.
	~[moodle]Tính sẵn sàng cao (highly available) mặc định, đảm bảo hàng đợi luôn hoạt động.
	=[moodle]Chi phí cố định hàng tháng, không phụ thuộc vào số lượng tin nhắn được xử lý.
	~[moodle]Hỗ trợ long polling để giảm thiểu các phản hồi trống và tăng hiệu quả.
	####<p><strong>Giải thích</strong>\: SQS tính phí theo tin nhắn (pay per message), không phải chi phí cố định hàng tháng.</p>
}

// question: 15.4  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Khi cấu hình VisibilityTimeout cho tin nhắn SQS, mục đích của nó là gì?</p>{
	~[moodle]Đây là thời gian tối đa một tin nhắn có thể tồn tại trong hàng đợi trước khi bị xóa tự động.#<p>Đây là MessageRetentionPeriod.</p>
	=[moodle]Đây là thời gian mà tin nhắn bị ẩn khỏi các yêu cầu ReceiveMessage sau khi được một consumer nhận.
	~[moodle]Đây là thời gian mà consumer phải chờ trước khi có thể gửi yêu cầu ReceiveMessage tiếp theo.#<p>Không phải là mục đích của VisibilityTimeout.</p>
	~[moodle]Đây là thời gian tối đa mà AWS sẽ giữ một tin nhắn trong hàng đợi trước khi chuyển nó sang dead-letter queue.#<p>Đây là một phần của cấu hình dead-letter queue, liên quan đến số lần tin nhắn được nhận.</p>
	####<p><strong>Giải thích</strong>\: VisibilityTimeout là số giây bạn muốn ẩn tin nhắn này khỏi hàng đợi để xử lý nó. Trong thời gian đó, bạn phải xóa tin nhắn, hoặc nó sẽ được gửi lại vào hàng đợi.</p>
}

// question: 15.5  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Khi sử dụng ELB với một Auto Scaling Group (ASG), làm thế nào để các instance EC2 mới được ASG khởi chạy được thêm vào cân bằng tải?</p>{
	~[moodle]Bạn cần thủ công đăng ký các instance EC2 mới với ELB mỗi khi chúng được khởi chạy.#<p>Các lựa chọn này không mô tả hành vi tự động của ASG và ELB.</p>
	=[moodle]ASG tự động đăng ký các instance EC2 mới với ELB dựa trên cấu hình nhóm mục tiêu (Target Group).
	~[moodle]ELB định kỳ quét các instance EC2 đang chạy trong VPC và tự động thêm chúng vào.#<p>Các lựa chọn này không mô tả hành vi tự động của ASG và ELB.</p>
	~[moodle]ASG yêu cầu bạn cấu hình một sự kiện Lambda để đăng ký các instance mới với ELB.#<p>Các lựa chọn này không mô tả hành vi tự động của ASG và ELB.</p>
	####<p><strong>Giải thích</strong>\: Các máy chủ được khởi động trong auto-scaling group sẽ tự động đăng ký với ALB. Trong CloudFormation, điều này được thực hiện thông qua thuộc tính TargetGroupARNs trong ASG.</p>
}

// question: 15.6  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Long polling trong SQS giúp ích như thế nào?</p>{
	~[moodle]Nó cho phép consumer nhận nhiều tin nhắn hơn trong một yêu cầu duy nhất.#<p>MaxNumberOfMessages cho phép nhận nhiều tin nhắn.</p>
	~[moodle]Nó làm tăng VisibilityTimeout của tin nhắn để có nhiều thời gian xử lý hơn.#<p>VisibilityTimeout là một tham số riêng.</p>
	=[moodle]Nó giảm số lượng các yêu cầu ReceiveMessage trống bằng cách chờ tin nhắn đến trong một khoảng thời gian nhất định.
	~[moodle]Nó đảm bảo các tin nhắn được nhận theo thứ tự First-In-First-Out (FIFO).#<p>SQS tiêu chuẩn không đảm bảo FIFO, SQS FIFO mới đảm bảo điều này.</p>
	####<p><strong>Giải thích</strong>\: Long polling cho phép bạn chờ đợi một khoảng thời gian nhất định (tối đa 20 giây) để nhận tin nhắn nếu chúng không có sẵn ngay lập tức. Khi sử dụng long polling, bạn sẽ không nhận được phản hồi ngay lập tức từ API AWS nếu không có tin nhắn nào có sẵn. Nếu một tin nhắn mới đến trong vòng 10 giây, phản hồi HTTP sẽ được gửi cho bạn.</p>
}

// question: 15.7  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Khi nào bạn nên sử dụng Application Load Balancer (ALB) thay vì Classic Load Balancer?</p>{
	~[moodle]Khi ứng dụng của bạn chủ yếu giao tiếp qua các giao thức cấp độ mạng (Layer 4) như TCP hoặc UDP.#<p>Network Load Balancer (NLB) phù hợp hơn cho các giao thức Layer 4.</p>
	=[moodle]Khi bạn cần các tính năng định tuyến dựa trên nội dung (content-based routing) hoặc định tuyến đến nhiều nhóm mục tiêu.
	~[moodle]Khi bạn cần hỗ trợ các ứng dụng legacy không tương thích với giao thức HTTP/HTTPS.#<p>Classic Load Balancer (CLB) có thể phù hợp hơn cho các ứng dụng legacy.</p>
	~[moodle]Khi bạn muốn tối ưu hóa chi phí bằng cách sử dụng một load balancer đơn giản hơn.#<p>ALB có thể phức tạp hơn CLB nhưng cung cấp nhiều tính năng hơn.</p>
	####<p><strong>Giải thích</strong>\: Chương này giới thiệu Application Load Balancer (ALB) hoạt động ở Layer 7 (HTTP và HTTPS). ALB cung cấp các tính năng định tuyến nâng cao như định tuyến dựa trên đường dẫn URL hoặc header HTTP, và có thể định tuyến đến nhiều nhóm mục tiêu, phù hợp hơn cho các microservices.</p>
}

// question: 15.8  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Đối với các ứng dụng chịu lỗi (fault-tolerant applications), tại sao việc thiết kế hệ thống phân tách không đồng bộ (asynchronously decoupled) lại quan trọng?</p>{
	~[moodle]Nó đảm bảo rằng các yêu cầu luôn được xử lý ngay lập tức để duy trì trải nghiệm người dùng.#<p>Phân tách không đồng bộ có thể dẫn đến việc xử lý yêu cầu bị trì hoãn.</p>
	=[moodle]Nó cho phép các thành phần hoạt động độc lập, giảm thiểu tác động của lỗi và dễ dàng mở rộng quy mô.
	~[moodle]Nó làm cho toàn bộ hệ thống trở nên đơn luồng, đơn giản hóa việc quản lý trạng thái.#<p>Phân tách không liên quan đến việc biến hệ thống thành đơn luồng.</p>
	~[moodle]Nó yêu cầu tất cả các thành phần phải hoạt động trong cùng một Availability Zone để giao tiếp hiệu quả.#<p>Phân tách không đồng bộ cho phép các thành phần hoạt động trên các AZ khác nhau.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn thiết kế hệ thống của mình được phân tách không đồng bộ, việc mở rộng quy mô rất dễ dàng và đó là một nền tảng tốt để chịu lỗi. Nếu một worker bị lỗi vì lý do nào đó, tin nhắn đang được xử lý sẽ trở nên khả dụng để được consumer khác nhận sau hai phút.</p>
}

// question: 15.9  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Trong kiến trúc URL2PNG (ví dụ trong sách), vai trò của SQS là gì?</p>{
	~[moodle]Lưu trữ các screenshot đã tạo dưới dạng đối tượng.#<p>S3 được sử dụng để lưu trữ các screenshot đã tạo.</p>
	~[moodle]Gửi yêu cầu HTTP đến các URL để tạo screenshot.#<p>Các worker sẽ gửi yêu cầu HTTP.</p>
	=[moodle]Làm hàng đợi tin nhắn để decoupling yêu cầu tạo screenshot từ việc xử lý.
	~[moodle]Cân bằng tải các yêu cầu tạo screenshot giữa các worker.#<p>ELB là dịch vụ cân bằng tải.</p>
	####<p><strong>Giải thích</strong>\: Trong kiến trúc ứng dụng URL2PNG, SQS được sử dụng làm hàng đợi tin nhắn để decoupling yêu cầu tạo screenshot từ việc xử lý. Nó biến một quy trình đồng bộ thành không đồng bộ, nơi các yêu cầu được đặt vào hàng đợi để các worker xử lý sau.</p>
}

// question: 15.10  name: Chapter 15: Phân tách hạ tầng của bạn: Elastic Load Balancing và Simple Queue Service
::Chapter 15\: Phân tách hạ tầng của bạn\: Elastic Load Balancing và Simple Queue Service::[html]<p>Khi cân bằng tải lưu lượng truy cập HTTP/HTTPS đến các instance EC2, điều nào sau đây là một trong những thông tin chi tiết bạn có thể tìm thấy trong tab Monitoring của bảng điều khiển ELB?</p>{
	~[moodle]Địa chỉ IP riêng của tất cả các instance EC2 không khỏe mạnh.#<p>Bạn có thể tìm thấy trạng thái sức khỏe của instance trong nhóm mục tiêu, nhưng không phải địa chỉ IP riêng của tất cả các instance không khỏe mạnh.</p>
	=[moodle]Số lượng request, độ trễ và số lượng phản hồi HTTP 5xx.
	~[moodle]Cấu hình security group chi tiết cho mỗi instance EC2 trong nhóm mục tiêu.#<p>Cấu hình security group được quản lý riêng biệt.</p>
	~[moodle]Lịch sử của tất cả các phiên người dùng đã được load balancer xử lý.#<p>ELB không lưu giữ lịch sử các phiên người dùng theo cách này.</p>
	####<p><strong>Giải thích</strong>\: Bảng điều khiển ELB có một tab Monitoring, nơi bạn có thể tìm thấy các biểu đồ về độ trễ, số lượng request và nhiều hơn nữa. Các biểu đồ này sẽ trễ một phút.</p>
}

// Chapter 16: Xây dựng ứng dụng chịu lỗi

// question: 16.1  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Trong ngữ cảnh xây dựng ứng dụng chịu lỗi trên AWS, nguyên tắc "let it crash" (hãy để nó sập) được hiểu như thế nào?</p>{
	~[moodle]Các thành phần ứng dụng nên được thiết kế để tự động tắt nếu phát hiện lỗi, ngăn chặn sự lây lan của lỗi.#<p>"Let it crash" ngụ ý rằng lỗi không phải là thảm họa mà là một phần của quy trình mà hệ thống được thiết kế để xử lý bằng cách phục hồi nhanh.</p>
	~[moodle]Tập trung vào việc tạo ra các hệ thống không thể bị lỗi bằng cách sử dụng phần cứng dự phòng tối đa.#<p>Đây là mục tiêu không thực tế và tốn kém, đi ngược lại nguyên tắc "let it crash".</p>
	=[moodle]Thiết kế các thành phần để phục hồi nhanh chóng sau lỗi thay vì cố gắng xây dựng hệ thống không thể bị lỗi.
	~[moodle]Chấp nhận rằng các ứng dụng sẽ thường xuyên bị sập và không cần cố gắng phục hồi chúng.#<p>Mục đích là phục hồi, không phải bỏ qua.</p>
	####<p><strong>Giải thích</strong>\: Thay vì cố gắng đạt được mục tiêu không thể đạt được là một hệ thống không thể bị lỗi, AWS lập kế hoạch cho lỗi: "Mọi thứ đều thất bại mọi lúc." Chương này nói về việc tập trung vào việc phục hồi nhanh chóng từ lỗi.</p>
}

// question: 16.2  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Một hành động "idempotent" (bất biến) trong hệ thống chịu lỗi có nghĩa là gì?</p>{
	~[moodle]Hành động chỉ có thể được thực hiện một lần duy nhất và không thể lặp lại.#<p>Các lựa chọn này không mô tả chính xác khái niệm idempotent.</p>
	=[moodle]Hành động luôn trả về cùng một kết quả, bất kể số lần nó được thực hiện.
	~[moodle]Hành động yêu cầu xác nhận thủ công trước khi được thực hiện để tránh lỗi.#<p>Các lựa chọn này không mô tả chính xác khái niệm idempotent.</p>
	~[moodle]Hành động không thể bị hoàn tác (rollback) sau khi đã được thực hiện thành công.#<p>Các lựa chọn này không mô tả chính xác khái niệm idempotent.</p>
	####<p><strong>Giải thích</strong>\: Idempotent có nghĩa là một hoạt động tạo ra cùng một kết quả bất kể số lần nó được thực hiện.</p>
}

// question: 16.3  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Tại sao việc giữ cho các EC2 instance không trạng thái (stateless) là một yêu cầu tiên quyết quan trọng để xây dựng ứng dụng chịu lỗi?</p>{
	~[moodle]Để giảm tải CPU trên các instance EC2 bằng cách tránh lưu trữ dữ liệu cục bộ.#<p>Mặc dù có thể giảm tải CPU, đây không phải là lý do chính yếu cho fault tolerance.</p>
	=[moodle]Để cho phép các instance EC2 bị thay thế hoặc mở rộng quy mô mà không làm mất dữ liệu quan trọng hoặc trạng thái ứng dụng.
	~[moodle]Để đơn giản hóa cấu hình mạng và giảm số lượng security groups cần thiết.#<p>Không liên quan trực tiếp đến cấu hình mạng.</p>
	~[moodle]Để đảm bảo rằng tất cả các yêu cầu được xử lý đồng bộ và không có độ trễ.#<p>Server không trạng thái không đảm bảo xử lý đồng bộ hoặc không có độ trễ.</p>
	####<p><strong>Giải thích</strong>\: Trạng thái không nên nằm trên instance EC2 (một server không trạng thái) như một điều kiện tiên quyết. Nếu bạn muốn mở rộng quy mô các instance của mình theo workload hiện tại, chúng phải không trạng thái. Nếu một instance bị lỗi, nó có thể dễ dàng bị thay thế mà không mất trạng thái.</p>
}

// question: 16.4  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Trong kiến trúc ứng dụng Imagery chịu lỗi (ví dụ trong sách), dịch vụ AWS nào được sử dụng để lưu trữ trạng thái của quá trình xử lý hình ảnh (ví dụ: 'created', 'uploaded', 'processed')?</p>{
	~[moodle]Amazon S3 để lưu trữ các tệp trạng thái dưới dạng đối tượng.#<p>S3 lưu trữ hình ảnh thô và đã xử lý, không phải trạng thái của quá trình.</p>
	~[moodle]Amazon RDS để lưu trữ trạng thái trong một cơ sở dữ liệu quan hệ.#<p>RDS là một lựa chọn nhưng DynamoDB được chọn trong ví dụ.</p>
	=[moodle]Amazon DynamoDB để lưu trữ trạng thái trong một bảng NoSQL, tận dụng tính khả dụng cao.
	~[moodle]Amazon EFS để lưu trữ trạng thái trong một hệ thống tệp được chia sẻ giữa các worker.#<p>EFS lưu trữ hệ thống tệp được chia sẻ.</p>
	####<p><strong>Giải thích</strong>\: DynamoDB chứa trạng thái hiện tại của quá trình xử lý. Trạng thái của quá trình xử lý được lưu trữ trong bảng DynamoDB.</p>
}

// question: 16.5  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Khi một ứng dụng chịu lỗi sử dụng SQS để gửi thông báo để kích hoạt quá trình xử lý hình ảnh, điều gì xảy ra nếu một worker bị lỗi trong khi đang xử lý một tin nhắn?</p>{
	~[moodle]Tin nhắn bị mất vĩnh viễn và không thể được xử lý lại.#<p>Tin nhắn không bị mất do tính bền vững của SQS.</p>
	~[moodle]Tin nhắn ngay lập tức được gửi lại cho hàng đợi và được một worker khác nhận.#<p>Không ngay lập tức; nó sẽ hết hạn VisibilityTimeout trước.</p>
	=[moodle]Tin nhắn sẽ trở nên khả dụng để được consumer khác nhận sau khi VisibilityTimeout hết hạn.
	~[moodle]Tin nhắn được tự động chuyển đến dead-letter queue (DLQ) để phân tích sau này.#<p>Tin nhắn chỉ được chuyển đến DLQ sau khi được nhận một số lần cấu hình và không xử lý thành công.</p>
	####<p><strong>Giải thích</strong>\: Nếu một worker chết vì lý do nào đó, tin nhắn đang được xử lý sẽ trở nên khả dụng để được consumer khác nhận sau hai phút (hoặc thời gian VisibilityTimeout đã cấu hình).</p>
}

// question: 16.6  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Để đảm bảo tính toàn vẹn dữ liệu và tránh ghi đè dữ liệu không chính xác trong một hệ thống phân tán như Imagery, bạn có thể sử dụng cơ chế nào để cập nhật trạng thái của item DynamoDB?</p>{
	=[moodle]Sử dụng ConditionExpression để đảm bảo item chỉ được cập nhật nếu thuộc tính version khớp với phiên bản cũ.
	~[moodle]Sử dụng TransactWriteItems để đảm bảo tất cả các cập nhật trên các item khác nhau đều thành công hoặc thất bại.#<p>TransactWriteItems đảm bảo tính nguyên tử cho nhiều hoạt động, không phải là cơ chế chính để tránh ghi đè dữ liệu không chính xác trong một item.</p>
	~[moodle]Tăng WriteCapacityUnits của bảng DynamoDB lên mức tối đa để giảm thiểu xung đột ghi.#<p>Tăng WCU chỉ cải thiện thông lượng, không giải quyết vấn đề xung đột ghi logic.</p>
	~[moodle]Tắt tính năng tự động ghi đè của DynamoDB để ngăn chặn mọi thay đổi không mong muốn.#<p>DynamoDB không có tính năng tắt ghi đè trực tiếp mà dựa vào ConditionExpression.</p>
	####<p><strong>Giải thích</strong>\: Để bảo vệ khỏi việc ghi đè, bạn có thể sử dụng ConditionExpression để đảm bảo mục chỉ được cập nhật nếu thuộc tính version khớp với phiên bản cũ. Đây là một hình thức của optimistic locking.</p>
}

// question: 16.7  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Điều nào sau đây là LỢI ÍCH của việc sử dụng AWS Elastic Beanstalk cho việc triển khai ứng dụng web chịu lỗi?</p>{
	~[moodle]Nó cung cấp toàn quyền kiểm soát cấu hình cấp hệ điều hành và phần cứng của các instance cơ bản.#<p>Elastic Beanstalk là một dịch vụ PaaS, giảm bớt quyền kiểm soát cấp thấp để đơn giản hóa việc triển khai.</p>
	=[moodle]Nó tự động quản lý cân bằng tải, mở rộng quy mô và giám sát các instance ứng dụng.
	~[moodle]Nó đảm bảo tất cả dữ liệu ứng dụng được lưu trữ vĩnh viễn trên các instance EC2.#<p>EB không tự động lưu trữ tất cả dữ liệu vĩnh viễn; bạn cần kết hợp với các dịch vụ lưu trữ khác.</p>
	~[moodle]Nó cho phép ứng dụng của bạn chạy trực tiếp trên các máy chủ bare metal mà không cần ảo hóa.#<p>EB chạy trên EC2 instances, vốn là máy ảo.</p>
	####<p><strong>Giải thích</strong>\: Elastic Beanstalk giúp bạn xử lý các vấn đề định kỳ như cung cấp môi trường chạy cho ứng dụng web, cập nhật môi trường, tự động cài đặt và cập nhật ứng dụng web, cấu hình ứng dụng và môi trường, mở rộng quy mô ứng dụng và giám sát/gỡ lỗi. Elastic Beanstalk sử dụng ELB để phân phối lưu lượng truy cập đến các instance EC2 cũng do Elastic Beanstalk quản lý.</p>
}

// question: 16.8  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Để đảm bảo tính chịu lỗi (fault tolerance) cho một ứng dụng web, việc tách biệt tầng ứng dụng (web server) khỏi tầng dữ liệu là quan trọng như thế nào?</p>{
	~[moodle]Không quan trọng, vì việc đặt tầng ứng dụng và tầng dữ liệu trên cùng một máy sẽ giảm độ trễ và tăng hiệu suất.#<p>Mặc dù có thể giảm độ trễ, nhưng việc tích hợp tạo ra điểm lỗi duy nhất.</p>
	=[moodle]Rất quan trọng, vì nó cho phép tầng ứng dụng không trạng thái và dễ dàng thay thế, trong khi tầng dữ liệu có thể được quản lý độc lập để bền vững.
	~[moodle]Tùy thuộc vào kích thước của ứng dụng; đối với các ứng dụng nhỏ, việc tích hợp là tối ưu.#<p>Nguyên tắc này áp dụng cho mọi kích thước ứng dụng để đảm bảo tính chịu lỗi.</p>
	~[moodle]Chỉ quan trọng nếu ứng dụng yêu cầu quyền truy cập vào nhiều loại cơ sở dữ liệu khác nhau.#<p>Không phải lý do chính.</p>
	####<p><strong>Giải thích</strong>\: Để xây dựng một ứng dụng chịu lỗi, bạn phải có thể thay thế một máy chủ bị lỗi bất cứ lúc nào mà không làm mất trạng thái. Server không trạng thái là một tiền đề cho fault tolerance. S3, DynamoDB, EFS và RDS có thể giúp bạn làm cho các máy chủ của bạn không trạng thái.</p>
}

// question: 16.9  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Điều nào sau đây là một trong những thành phần cốt lõi của Elastic Beanstalk khi triển khai một ứng dụng?</p>{
	~[moodle]IAM Users: Các tài khoản người dùng được tạo để đăng nhập vào ứng dụng web.#<p>IAM users và key pairs là các khái niệm về bảo mật và truy cập, không phải thành phần cốt lõi của quá trình triển khai EB.</p>
	~[moodle]EC2 Key Pairs: Được sử dụng để mã hóa dữ liệu giữa các máy chủ trong môi trường Elastic Beanstalk.#<p>IAM users và key pairs là các khái niệm về bảo mật và truy cập, không phải thành phần cốt lõi của quá trình triển khai EB.</p>
	=[moodle]Application Versions: Chứa một bản phát hành cụ thể của ứng dụng của bạn, được tải lên S3 dưới dạng một file zip.
	~[moodle]CloudFormation Stacks: Được tự động tạo ra cho mỗi yêu cầu người dùng để tăng cường khả năng mở rộng.#<p>EB tự tạo tài nguyên CloudFormation dưới nền, nhưng "stack" không phải là một thành phần cốt lõi của ứng dụng EB.</p>
	####<p><strong>Giải thích</strong>\: Một version chứa một bản phát hành cụ thể của ứng dụng của bạn. Để tạo một version mới, bạn phải tải các file thực thi của mình (được đóng gói thành một archive) lên Amazon S3, nơi lưu trữ các file tĩnh. Một version về cơ bản là một con trỏ đến archive các file thực thi này.</p>
}

// question: 16.10  name: Chapter 16: Xây dựng ứng dụng chịu lỗi
::Chapter 16\: Xây dựng ứng dụng chịu lỗi::[html]<p>Để tích hợp một ứng dụng Node.js với SQS trong môi trường Elastic Beanstalk (EB) Worker, bạn cần cấu hình điều gì trong cài đặt ứng dụng EB?</p>{
	~[moodle]Chỉ định địa chỉ IP công cộng của hàng đợi SQS trong file cấu hình của ứng dụng Node.js.#<p>SQS không có địa chỉ IP công cộng trực tiếp mà có QueueUrl.</p>
	=[moodle]Cấu hình biến môi trường WorkerQueueURL để trỏ đến URL của hàng đợi SQS và HttpPath để nhận tin nhắn.
	~[moodle]Đăng ký trực tiếp ứng dụng Node.js với SQS như một lambda function.#<p>Ứng dụng Node.js chạy trên EC2 instance, không phải Lambda function.</p>
	~[moodle]Sử dụng một trình cắm (plugin) bên thứ ba để xử lý việc giao tiếp giữa Node.js và SQS.#<p>EB cung cấp tích hợp riêng với SQS.</p>
	####<p><strong>Giải thích</strong>\: Bạn cấu hình biến môi trường WorkerQueueURL để trỏ đến URL của hàng đợi SQS và HttpPath để định nghĩa endpoint HTTP mà ứng dụng worker của bạn sẽ lắng nghe để nhận tin nhắn SQS. Elastic Beanstalk worker tier sẽ đẩy tin nhắn SQS đến endpoint này.</p>
}

// Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch

// question: 17.1  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Tính năng "elasticity" (tính linh hoạt) của AWS cho phép bạn làm gì với tài nguyên hạ tầng?</p>{
	~[moodle]Đặt trước tài nguyên với cam kết dài hạn để giảm chi phí cố định.#<p>Đây là một chiến lược tối ưu hóa chi phí, không phải tính linh hoạt.</p>
	~[moodle]Chỉ mở rộng quy mô tài nguyên theo chiều dọc (vertical scaling) bằng cách tăng kích thước máy chủ.#<p>Tính linh hoạt bao gồm cả mở rộng theo chiều ngang (horizontal scaling).</p>
	=[moodle]Tăng hoặc giảm tài nguyên một cách linh hoạt theo nhu cầu hiện tại của workload.
	~[moodle]Khởi chạy tất cả tài nguyên trong một Availability Zone duy nhất để đơn giản hóa quản lý.#<p>Điều này sẽ tạo ra điểm lỗi duy nhất, đi ngược lại các nguyên tắc thiết kế trên AWS.</p>
	####<p><strong>Giải thích</strong>\: Bạn có thể mở rộng từ một instance EC2 lên hàng nghìn instance EC2. Bộ nhớ có thể tăng từ gigabyte lên petabyte. Bạn có thể mở rộng quy mô theo yêu cầu, do đó thay thế việc lập kế hoạch dung lượng. Khả năng mở rộng theo yêu cầu được gọi là tính linh hoạt (elasticity) của AWS.</p>
}

// question: 17.2  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Auto Scaling Group (ASG) bao gồm những thành phần chính nào để quản lý một nhóm instance EC2 động?</p>{
	~[moodle]IAM roles, Security Groups và Network ACLs.#<p>Đây là các dịch vụ hoặc thành phần khác có thể tích hợp với ASG, nhưng không phải là các thành phần cốt lõi của ASG.</p>
	=[moodle]Launch configuration, Auto Scaling Group và scaling plans.
	~[moodle]Elastic Load Balancers, Target Groups và Listener.#<p>Đây là các dịch vụ hoặc thành phần khác có thể tích hợp với ASG, nhưng không phải là các thành phần cốt lõi của ASG.</p>
	~[moodle]CloudWatch alarms, SNS topics và Lambda functions.#<p>Đây là các dịch vụ hoặc thành phần khác có thể tích hợp với ASG, nhưng không phải là các thành phần cốt lõi của ASG.</p>
	####<p><strong>Giải thích</strong>\: Auto Scaling Group bao gồm ba phần: 1. Cấu hình khởi chạy (Launch configuration) định nghĩa kích thước, image và cấu hình của các máy ảo. 2. Auto Scaling Group chỉ định số lượng máy ảo cần chạy dựa trên cấu hình khởi chạy. 3. Các kế hoạch mở rộng quy mô (Scaling plans) điều chỉnh số lượng instance EC2 mong muốn trong auto-scaling group dựa trên kế hoạch hoặc động.</p>
}

// question: 17.3  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Điều nào sau đây là đúng về Launch Configuration trong Auto Scaling?</p>{
	~[moodle]Nó định nghĩa số lượng instance EC2 tối thiểu và tối đa trong ASG.#<p>Điều này được định nghĩa trong Auto Scaling Group.</p>
	=[moodle]Nó chỉ định kích thước, image (AMI) và cấu hình của các instance EC2 mới sẽ được khởi chạy.
	~[moodle]Nó chịu trách nhiệm theo dõi sức khỏe của các instance EC2 và thay thế các instance bị lỗi.#<p>Đây là chức năng của Auto Scaling Group.</p>
	~[moodle]Nó là một cơ chế định giá cho các instance EC2 được khởi chạy theo nhu cầu.#<p>Launch Configuration là một template, không phải cơ chế định giá.</p>
	####<p><strong>Giải thích</strong>\: Bạn sử dụng cấu hình khởi chạy để định nghĩa và cấu hình các máy ảo mới. Bảng 17.1 cho thấy các tham số quan trọng nhất cho một cấu hình khởi chạy, bao gồm ImageId, InstanceType, UserData, KeyName, SecurityGroups, v.v..</p>
}

// question: 17.4  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Để tự động tăng hoặc giảm số lượng instance EC2 trong một ASG dựa trên các mô hình tải lặp lại (ví dụ: giảm vào ban đêm), bạn nên sử dụng loại trigger auto-scaling nào?</p>{
	=[moodle]Scheduled actions (hành động theo lịch trình).
	~[moodle]CloudWatch alarms (báo động CloudWatch) dựa trên mức sử dụng CPU.#<p>Các báo động CloudWatch và chính sách mở rộng theo mục tiêu được sử dụng để phản ứng với tải động và không thể đoán trước, không phải các mô hình lặp lại.</p>
	~[moodle]Target tracking scaling policies (chính sách mở rộng theo mục tiêu).#<p>Các báo động CloudWatch và chính sách mở rộng theo mục tiêu được sử dụng để phản ứng với tải động và không thể đoán trước, không phải các mô hình lặp lại.</p>
	~[moodle]Manual scaling (mở rộng quy mô thủ công).#<p>Mở rộng quy mô thủ công không phải là tự động.</p>
	####<p><strong>Giải thích</strong>\: Các hành động theo lịch trình (scheduled actions) điều chỉnh dung lượng của bạn bằng các hành động một lần hoặc lặp lại. Bạn có thể sử dụng các loại hành động khác nhau để phản ứng với cả hai loại mô hình tải.</p>
}

// question: 17.5  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Mục đích của "Target Tracking Scaling Policy" trong Auto Scaling là gì?</p>{
	~[moodle]Để thủ công định nghĩa các ngưỡng và bước mở rộng phức tạp cho các chỉ số tùy chỉnh.#<p>Đây là mô tả của step scaling.</p>
	=[moodle]Để tự động điều chỉnh số lượng instance EC2 nhằm duy trì một chỉ số mục tiêu cụ thể (ví dụ: mức sử dụng CPU trung bình 70%).
	~[moodle]Để chỉ mở rộng quy mô theo chiều dọc bằng cách thay đổi loại instance EC2 đang chạy.#<p>Scaling trong ASG thường là mở rộng theo chiều ngang.</p>
	~[moodle]Để đảm bảo rằng số lượng instance EC2 luôn ở mức tối thiểu đã định, bất kể workload.#<p>Mục tiêu là duy trì chỉ số, không phải chỉ mức tối thiểu.</p>
	####<p><strong>Giải thích</strong>\: Target tracking giải phóng bạn khỏi việc định nghĩa các bước và ngưỡng mở rộng. Bạn chỉ cần định nghĩa một mục tiêu (ví dụ: mức sử dụng CPU 70%) và số lượng instance EC2 sẽ được điều chỉnh tương ứng.</p>
}

// question: 17.6  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Điều nào sau đây là một trong những chỉ số được định nghĩa trước (predefined metrics) có thể được sử dụng với Target Tracking Scaling Policy?</p>{
	~[moodle]ASGAverageDiskReadBytes để mở rộng quy mô dựa trên hoạt động I/O của đĩa.#<p>Mặc dù có thể sử dụng chỉ số tùy chỉnh cho I/O đĩa, ASGAverageDiskReadBytes không phải là chỉ số được định nghĩa trước.</p>
	=[moodle]ASGAverageCPUUtilization để mở rộng quy mô dựa trên mức sử dụng CPU trung bình.
	~[moodle]ALBHTTPCode_Target_5XX_Count để mở rộng quy mô dựa trên lỗi của ứng dụng.#<p>Lỗi HTTP 5xx là một chỉ số CloudWatch nhưng không phải là chỉ số được định nghĩa trước cho Target Tracking.</p>
	~[moodle]QueueLength từ Amazon SQS để mở rộng quy mô dựa trên số lượng tin nhắn trong hàng đợi.#<p>QueueLength có thể được sử dụng với step scaling, nhưng không phải Target Tracking vì nó không tương quan tỉ lệ trực tiếp với số lượng instance.</p>
	####<p><strong>Giải thích</strong>\: Các chỉ số được định nghĩa trước cho việc sử dụng target tracking là ASGAverageCPUUtilization để mở rộng quy mô dựa trên mức sử dụng CPU trung bình giữa tất cả các instance trong một auto-scaling group.</p>
}

// question: 17.7  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Tại sao cần phân tách (decouple) dynamic EC2 instance pool khỏi các client khi mở rộng quy mô (scaling)?</p>{
	~[moodle]Để instance EC2 có thể trực tiếp giao tiếp với Internet mà không cần qua bất kỳ lớp trung gian nào.#<p>Phân tách thường thêm một lớp trung gian.</p>
	=[moodle]Để giao diện có thể truy cập từ bên ngoài hệ thống vẫn giữ nguyên, bất kể số lượng instance EC2 đang hoạt động phía sau.
	~[moodle]Để giảm độ trễ giữa các instance EC2 trong cùng một nhóm tự động mở rộng.#<p>Phân tách có thể thêm độ trễ nhỏ tùy thuộc vào kiến trúc.</p>
	~[moodle]Để kích hoạt tính năng snapshot tự động cho các volume EBS của các instance EC2.#<p>Không liên quan trực tiếp đến việc phân tách.</p>
	####<p><strong>Giải thích</strong>\: Nếu bạn muốn sử dụng auto-scaling để tăng và giảm số lượng máy ảo, bạn cần phân tách các instance EC2 khỏi các client, vì giao diện có thể truy cập từ bên ngoài hệ thống cần phải giữ nguyên bất kể số lượng instance EC2 đang hoạt động phía sau.</p>
}

// question: 17.8  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Khi nào thì việc sử dụng một hàng đợi tin nhắn (message queue) để phân tách không đồng bộ một nhóm instance EC2 động là có lợi hơn một load balancer?</p>{
	~[moodle]Khi các yêu cầu cần được trả lời ngay lập tức để duy trì trải nghiệm người dùng theo thời gian thực.#<p>Các workload yêu cầu phản hồi ngay lập tức phù hợp hơn với phân tách đồng bộ bằng load balancer.</p>
	~[moodle]Khi workload yêu cầu xử lý liên tục, độ trễ thấp và không có tác vụ nền.#<p>Các workload yêu cầu phản hồi ngay lập tức phù hợp hơn với phân tách đồng bộ bằng load balancer.</p>
	=[moodle]Khi các yêu cầu không cần được trả lời ngay lập tức và workload có thể được xử lý trong nền, tận dụng các job nền.
	~[moodle]Khi ứng dụng là một hệ thống microservices phức tạp và mỗi dịch vụ cần có một endpoint công cộng duy nhất.#<p>Microservices có thể sử dụng cả hai cách phân tách, nhưng load balancer thường là cổng vào cho các endpoint công cộng.</p>
	####<p><strong>Giải thích</strong>\: Phân tách một nhóm instance EC2 động một cách không đồng bộ mang lại lợi thế nếu bạn muốn mở rộng quy mô dựa trên workload: vì các yêu cầu không cần được trả lời ngay lập tức, bạn có thể đặt các yêu cầu vào một hàng đợi và mở rộng quy mô số lượng instance EC2 dựa trên độ dài của hàng đợi.</p>
}

// question: 17.9  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Đối với các instance EC2 cung cấp hiệu suất tăng đột biến (burstable performance) như loại instance T2, điều gì xảy ra khi tất cả các tín dụng tăng đột biến (burst credits) đã được sử dụng hết?</p>{
	~[moodle]Instance EC2 sẽ tự động bị chấm dứt bởi AWS để ngăn chặn việc sử dụng tài nguyên quá mức.#<p>Các lựa chọn này sai về cách instance T2 hoạt động khi hết tín dụng.</p>
	=[moodle]Instance EC2 sẽ chuyển sang hoạt động ở mức hiệu suất CPU cơ bản và có thể trải qua hiệu suất giảm.
	~[moodle]Instance EC2 sẽ tự động mở rộng quy mô lên một loại instance lớn hơn để duy trì hiệu suất.#<p>Các lựa chọn này sai về cách instance T2 hoạt động khi hết tín dụng.</p>
	~[moodle]Instance EC2 sẽ tự động dừng và không thể khởi động lại cho đến khi có thêm tín dụng.#<p>Các lựa chọn này sai về cách instance T2 hoạt động khi hết tín dụng.</p>
	####<p><strong>Giải thích</strong>\: Các máy ảo này cung cấp hiệu suất CPU cơ bản và có thể tăng đột biến hiệu suất trong thời gian ngắn dựa trên tín dụng. Nếu tất cả tín dụng đã được sử dụng hết, instance hoạt động ở mức cơ bản. Ví dụ, đối với một instance t2.micro, hiệu suất cơ bản là 10% hiệu suất của CPU vật lý bên dưới.</p>
}

// question: 17.10  name: Chapter 17: Mở rộng quy mô lên và xuống: Auto-Scaling và CloudWatch
::Chapter 17\: Mở rộng quy mô lên và xuống\: Auto-Scaling và CloudWatch::[html]<p>Khi nào bạn nên sử dụng Auto Scaling Group (ASG) cho ứng dụng của mình?</p>{
	~[moodle]Chỉ khi bạn cần khởi chạy một instance EC2 duy nhất và không cần khả năng phục hồi tự động.#<p>ASG được dùng để quản lý một nhóm instance, không phải một instance duy nhất.</p>
	=[moodle]Khi bạn cần khởi chạy nhiều instance EC2 giống hệt nhau và quản lý khả năng phục hồi cũng như khả năng mở rộng của chúng.
	~[moodle]Chỉ khi bạn triển khai các ứng dụng máy tính lớn (mainframe applications) trong môi trường on-premises.#<p>ASG dành cho đám mây, không phải on-premises.</p>
	~[moodle]Khi bạn muốn giảm thiểu hoàn toàn chi phí cơ sở hạ tầng bằng cách luôn chạy số lượng máy chủ tối thiểu.#<p>ASG giúp tối ưu hóa chi phí bằng cách mở rộng quy mô, nhưng không phải là mục tiêu duy nhất.</p>
	####<p><strong>Giải thích</strong>\: Bất cứ khi nào phân phối một ứng dụng trên nhiều instance EC2, bạn nên sử dụng auto-scaling group. Làm như vậy cho phép bạn khởi chạy các instance giống hệt nhau một cách dễ dàng. Bạn tận dụng tối đa các khả năng của đám mây khi mở rộng quy mô số lượng instance dựa trên lịch trình hoặc chỉ số phụ thuộc vào mô hình tải.</p>
}