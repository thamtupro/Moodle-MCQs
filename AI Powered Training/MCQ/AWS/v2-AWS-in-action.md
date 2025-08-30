// Chapter 1: Amazon Web Services
// question: 1 name: Switch category to $module$/top/Chapter 1: Amazon Web Services
$CATEGORY: $module$/top/Chapter 1: Amazon Web Services

// question: 1.1 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Amazon Web Services (AWS) được định nghĩa chính xác là gì theo nguồn tài liệu?</p>{
	~[moodle]Một hệ điều hành độc quyền được thiết kế cho các thiết bị di động.#<p>Đây là mô tả không chính xác; AWS là một nền tảng dịch vụ, không phải hệ điều hành di động.</p>
	=[moodle]Một nền tảng dịch vụ web cung cấp các giải pháp điện toán, lưu trữ và mạng ở nhiều cấp độ trừu tượng khác nhau.
	~[moodle]Một công ty chuyên sản xuất phần cứng máy tính và linh kiện điện tử.#<p>AWS tập trung vào dịch vụ đám mây, không phải sản xuất phần cứng.</p>
	~[moodle]Một ngôn ngữ lập trình mới dành riêng cho phát triển ứng dụng đám mây.#<p>AWS không phải là một ngôn ngữ lập trình, mà là một tập hợp các dịch vụ có thể được sử dụng với nhiều ngôn ngữ khác nhau.</p>
	####<p><strong>Giải thích</strong>: AWS là một nền tảng dịch vụ web cung cấp các giải pháp cho điện toán, lưu trữ và mạng ở nhiều cấp độ trừu tượng khác nhau.</p>
}

// question: 1.2 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Lợi ích nào sau đây KHÔNG phải là một trong những lợi ích quan trọng nhất khi sử dụng AWS?</p>{
	~[moodle]Nền tảng đổi mới và phát triển nhanh chóng, với các dịch vụ giải quyết vấn đề chung.#<p>AWS là một nền tảng đổi mới và phát triển nhanh chóng, với các dịch vụ giải quyết các vấn đề phổ biến và cho phép tự động hóa.</p>
	~[moodle]Dung lượng linh hoạt (khả năng mở rộng) và được xây dựng để chống lỗi (độ tin cậy cao).#<p>AWS cung cấp dung lượng linh hoạt (khả năng mở rộng) và được thiết kế để chống lỗi (độ tin cậy).</p>
	~[moodle]Giảm thời gian đưa sản phẩm ra thị trường và hưởng lợi từ tính kinh tế theo quy mô.#<p>Sử dụng AWS giúp giảm thời gian đưa sản phẩm ra thị trường và hưởng lợi từ tính kinh tế theo quy mô nhờ hạ tầng toàn cầu.</p>
	=[moodle]Yêu cầu đầu tư lớn vào cơ sở hạ tầng vật lý ban đầu để khởi tạo dịch vụ.
	####<p><strong>Giải thích</strong>: AWS giúp loại bỏ nhu cầu đầu tư lớn vào cơ sở hạ tầng vật lý ban đầu, cho phép người dùng hưởng lợi từ mô hình trả tiền theo mức sử dụng.</p>
}

// question: 1.3 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Dịch vụ nào của AWS nổi bật nhất trong việc cung cấp máy ảo và khả năng lưu trữ?</p>{
	~[moodle]AWS Lambda và Amazon DynamoDB.#<p>AWS Lambda dùng để chạy mã mà không cần máy ảo, DynamoDB là dịch vụ cơ sở dữ liệu NoSQL.</p>
	=[moodle]Amazon EC2 và Amazon S3.
	~[moodle]Amazon RDS và Amazon Glacier.#<p>Amazon RDS là dịch vụ cơ sở dữ liệu quan hệ, Glacier là giải pháp lưu trữ dữ liệu không đắt tiền cho mục đích lưu trữ lâu dài.</p>
	~[moodle]Amazon VPC và Amazon CloudWatch.#<p>Amazon VPC là mạng riêng ảo, CloudWatch là dịch vụ giám sát và ghi nhật ký.</p>
	####<p><strong>Giải thích</strong>: Các dịch vụ nổi bật nhất do AWS cung cấp là EC2, cung cấp máy ảo và S3, cung cấp dung lượng lưu trữ.</p>
}

// question: 1.4 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Mô hình định giá "trả tiền theo mức sử dụng" của AWS có nghĩa là gì?</p>{
	~[moodle]Khách hàng phải trả một khoản phí cố định hàng tháng, không phụ thuộc vào mức độ sử dụng dịch vụ.#<p>Đây là mô tả của một mô hình định giá cố định, trái ngược với mô hình trả tiền theo mức sử dụng của AWS.</p>
	=[moodle]Khách hàng chỉ phải trả tiền cho các dịch vụ IT mà họ thực sự sử dụng, theo số lượng và thời gian tiêu thụ.
	~[moodle]Khách hàng được cung cấp tất cả các dịch vụ miễn phí trong một khoảng thời gian nhất định.#<p>Mặc dù có Free Tier, mô hình chung của AWS là trả tiền theo mức sử dụng, không phải miễn phí hoàn toàn cho tất cả dịch vụ.</p>
	~[moodle]Khách hàng phải mua giấy phép phần mềm trước khi có thể sử dụng bất kỳ dịch vụ AWS nào.#<p>AWS cung cấp dịch vụ dưới dạng đám mây, giảm thiểu nhu cầu mua giấy phép phần mềm truyền thống cho hạ tầng vật lý.</p>
	####<p><strong>Giải thích</strong>: Mô hình định giá của các dịch vụ AWS là trả tiền theo mức sử dụng. Điều này cho phép bạn thêm dung lượng khi lưu lượng truy cập tăng và giảm dung lượng khi lưu lượng truy cập giảm.</p>
}

// question: 1.5 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Đâu là một trong những cách chính để tương tác với với AWS, cho phép quản lý các dịch vụ qua giao diện người dùng dựa trên web?</p>{
	~[moodle]Amazon EC2 Instance Store.#<p>EC2 Instance Store là một loại lưu trữ khối cục bộ, không phải phương thức tương tác chính với AWS.</p>
	=[moodle]AWS Management Console.
	~[moodle]AWS Command-line Interface (CLI).#<p>CLI cho phép quản lý dịch vụ AWS từ terminal bằng cách gọi API.</p>
	~[moodle]AWS Software Development Kits (SDKs).#<p>SDK cho phép lập trình tương tác với AWS bằng các ngôn ngữ ưa thích bằng cách gọi API.</p>
	####<p><strong>Giải thích</strong>: Giao diện người dùng đồ họa (UI) là Management Console, nơi bạn được trình bày với tổng quan liệt kê các dịch vụ.</p>
}

// question: 1.6 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Điện toán đám mây (Cloud computing) được định nghĩa chính thức bởi National Institute of Standards and Technology (NIST) như thế nào?</p>{
	~[moodle]Một hệ thống lưu trữ dữ liệu cục bộ không được kết nối mạng.#<p>Định nghĩa này không liên quan đến lưu trữ cục bộ không kết nối mạng.</p>
	=[moodle]Một mô hình cho phép truy cập mạng theo yêu cầu, tiện lợi, phổ biến tới một nhóm tài nguyên điện toán cấu hình được chia sẻ, có thể cấp phát và giải phóng nhanh chóng.
	~[moodle]Một phương pháp phát triển phần mềm độc quyền chỉ dành cho các tập đoàn lớn.#<p>Điện toán đám mây là một mô hình công khai hoặc riêng tư, không giới hạn cho các tập đoàn lớn.</p>
	~[moodle]Một công nghệ dùng để tối ưu hóa hiệu suất của một máy tính cá nhân.#<p>Điện toán đám mây tập trung vào cung cấp tài nguyên IT theo yêu cầu, không phải tối ưu hóa máy tính cá nhân.</p>
	####<p><strong>Giải thích</strong>: Định nghĩa của NIST cho điện toán đám mây là "một mô hình cho phép truy cập mạng theo yêu cầu, tiện lợi, phổ biến tới một nhóm tài nguyên điện toán cấu hình được chia sẻ (mạng, máy ảo, lưu trữ, ứng dụng và dịch vụ) có thể được cấp phát và giải phóng nhanh chóng với nỗ lực quản lý tối thiểu hoặc tương tác nhà cung cấp dịch vụ tối thiểu.".</p>
}

// question: 1.7 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>AWS được phân loại là loại đám mây nào theo nguồn tài liệu?</p>{
	~[moodle]Đám mây riêng (Private cloud).#<p>Đám mây riêng được quản lý bởi một tổ chức cho mục đích sử dụng nội bộ.</p>
	=[moodle]Đám mây công cộng (Public cloud).
	~[moodle]Đám mây lai (Hybrid cloud).#<p>Đám mây lai là sự kết hợp giữa đám mây công cộng và đám mây riêng.</p>
	~[moodle]Đám mây cộng đồng (Community cloud).#<p>Đám mây cộng đồng không được đề cập trong các phân loại đám mây chính của nguồn tài liệu.</p>
	####<p><strong>Giải thích</strong>: AWS là một đám mây công cộng.</p>
}

// question: 1.8 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Dịch vụ "Infrastructure as a Service (IaaS)" trong điện toán đám mây cung cấp những tài nguyên cơ bản nào?</p>{
	~[moodle]Các ứng dụng phần mềm được đóng gói hoàn chỉnh như SaaS.#<p>Ứng dụng phần mềm hoàn chỉnh là SaaS (Software as a Service).</p>
	~[moodle]Các nền tảng phát triển ứng dụng đã được cấu hình sẵn như PaaS.#<p>Nền tảng phát triển ứng dụng đã được cấu hình sẵn là PaaS (Platform as a Service).</p>
	=[moodle]Các tài nguyên cơ bản như khả năng điện toán, lưu trữ và mạng, sử dụng máy ảo.
	~[moodle]Dịch vụ tư vấn và hỗ trợ kỹ thuật cho các hệ thống IT.#<p>Đây là một dịch vụ hỗ trợ, không phải tài nguyên IaaS.</p>
	####<p><strong>Giải thích</strong>: IaaS cung cấp các tài nguyên cơ bản như khả năng điện toán, lưu trữ và mạng, sử dụng máy ảo như Amazon EC2.</p>
}

// question: 1.9 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Một "key pair" trong AWS bao gồm những thành phần nào và vai trò của chúng?</p>{
	~[moodle]Một khóa bí mật (secret key) và một khóa API (API key) để truy cập dịch vụ.#<p>Khóa bí mật và khóa API có thể liên quan đến thông tin đăng nhập IAM, nhưng không phải là key pair theo định nghĩa này.</p>
	=[moodle]Một khóa riêng (private key) và một khóa công khai (public key), dùng để xác thực cho máy ảo.
	~[moodle]Hai khóa công khai được lưu trữ trên máy chủ AWS để tăng cường bảo mật.#<p>Key pair bao gồm một khóa riêng và một khóa công khai, không phải hai khóa công khai.</p>
	~[moodle]Một mật khẩu chính và một mã xác thực hai yếu tố cho tài khoản root.#<p>Đây là mô tả về xác thực đa yếu tố (MFA), không phải key pair.</p>
	####<p><strong>Giải thích</strong>: Một key pair bao gồm một khóa riêng và một khóa công khai. Khóa công khai sẽ được tải lên AWS và tiêm vào máy ảo. Khóa riêng là của bạn; nó giống như mật khẩu nhưng an toàn hơn nhiều. Nó được dùng để xác thực khi truy cập máy Linux qua SSH và giải mã mật khẩu quản trị viên cho máy Windows qua RDP.</p>
}

// question: 1.10 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Khi tạo một tài khoản AWS mới, điều gì được khuyến nghị để bảo vệ người dùng root của tài khoản?</p>{
	~[moodle]Chia sẻ thông tin đăng nhập root với tất cả thành viên trong nhóm phát triển.#<p>Chia sẻ thông tin đăng nhập root là một rủi ro bảo mật nghiêm trọng và không được khuyến nghị.</p>
	=[moodle]Tạo tài khoản người dùng IAM riêng biệt cho công việc hàng ngày và kích hoạt xác thực đa yếu tố (MFA) cho người dùng root.
	~[moodle]Chỉ sử dụng mật khẩu đơn giản để dễ nhớ và truy cập nhanh chóng.#<p>Sử dụng mật khẩu đơn giản làm suy yếu bảo mật tài khoản.</p>
	~[moodle]Ghi lại mật khẩu root trên một ghi chú dán và dán vào màn hình máy tính.#<p>Ghi mật khẩu ra giấy và để ở nơi dễ thấy là một hành vi bảo mật không an toàn.</p>
	####<p><strong>Giải thích</strong>: Bảo vệ người dùng root của tài khoản AWS là rất quan trọng, đặc biệt là bằng cách kích hoạt xác thực đa yếu tố (MFA). Nên tạo người dùng IAM riêng cho công việc hàng ngày thay vì sử dụng tài khoản root.</p>
}

// question: 1.11 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Trong AWS Management Console, thanh điều hướng ở trên cùng bao gồm những phần chính nào?</p>{
	=[moodle]AWS (trang bắt đầu), Dịch vụ, Nhóm tài nguyên, Phần tùy chỉnh, Tên của bạn, Vùng của bạn, Hỗ trợ.
	~[moodle]Bảng điều khiển tài nguyên, Cài đặt bảo mật, Trung tâm thanh toán, Nhật ký hoạt động.#<p>Các tùy chọn này bao gồm một số thành phần có thể tìm thấy trong Console nhưng không phải là cấu trúc chính của thanh điều hướng ở trên cùng.</p>
	~[moodle]Quản lý người dùng, Quản lý ứng dụng, Quản lý lưu trữ, Quản lý mạng.#<p>Các tùy chọn này bao gồm một số thành phần có thể tìm thấy trong Console nhưng không phải là cấu trúc chính của thanh điều hướng ở trên cùng.</p>
	~[moodle]Danh sách các máy ảo đang chạy, cấu hình cơ sở dữ liệu, các bản sao lưu.#<p>Các tùy chọn này bao gồm một số thành phần có thể tìm thấy trong Console nhưng không phải là cấu trúc chính của thanh điều hướng ở trên cùng.</p>
	####<p><strong>Giải thích</strong>: Thanh điều hướng ở trên cùng của Management Console bao gồm bảy phần: AWS (trang bắt đầu), Dịch vụ, Nhóm tài nguyên, Phần tùy chỉnh (Chỉnh sửa), Tên của bạn, Vùng của bạn, và Hỗ trợ.</p>
}

// question: 1.12 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Tính năng "Flexible capacity (scalability)" của AWS mang lại lợi ích gì cho các doanh nghiệp?</p>{
	~[moodle]Giới hạn nghiêm ngặt về số lượng máy ảo và dung lượng lưu trữ có thể sử dụng.#<p>AWS cho phép mở rộng dung lượng rất lớn, không giới hạn nghiêm ngặt về số lượng máy ảo hay dung lượng lưu trữ.</p>
	=[moodle]Giải phóng doanh nghiệp khỏi việc lập kế hoạch nhu cầu dung lượng trong tương lai, cho phép mở rộng linh hoạt theo yêu cầu.
	~[moodle]Yêu cầu khách hàng cam kết sử dụng một dung lượng cố định trong nhiều năm.#<p>Mặc dù có tùy chọn đặt trước (Reserved Instances) cho các cam kết sử dụng, tính linh hoạt theo yêu cầu là lợi ích cốt lõi của AWS.</p>
	~[moodle]Chỉ cho phép tăng dung lượng nhưng không cho phép giảm dung lượng khi cần.#<p>AWS cho phép tăng và giảm dung lượng (scaling up and down) linh hoạt theo lưu lượng truy cập hoặc nhu cầu.</p>
	####<p><strong>Giải thích</strong>: Flexible capacity giúp bạn không phải lập kế hoạch nhu cầu dung lượng trong tương lai. Bạn có thể mở rộng từ một máy ảo lên hàng ngàn máy ảo hoặc dung lượng lưu trữ từ gigabyte lên petabyte theo nhu cầu.</p>
}

// question: 1.13 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>AWS phân chia các trung tâm dữ liệu của mình thành các đơn vị địa lý nào để phục vụ khách hàng trên toàn thế giới?</p>{
	~[moodle]Các vùng cục bộ (Local zones) được đặt trong mỗi thành phố lớn.#<p>Local zones không phải là đơn vị phân chia chính được đề cập ở đây.</p>
	=[moodle]Các vùng (Regions) độc lập nhau, mỗi vùng chứa một tập hợp các trung tâm dữ liệu.
	~[moodle]Các điểm hiện diện (Points of Presence) chỉ dành cho dịch vụ CDN.#<p>CDN và DNS là các dịch vụ hoạt động toàn cầu trên các vùng và một số trung tâm dữ liệu bổ sung, không phải là đơn vị phân chia trung tâm dữ liệu chính.</p>
	~[moodle]Các khu vực tính toán (Compute zones) tập trung ở một số quốc gia.#<p>AWS không sử dụng thuật ngữ "khu vực tính toán" theo cách này.</p>
	####<p><strong>Giải thích</strong>: Amazon vận hành các trung tâm dữ liệu ở các vùng địa lý khác nhau (regions) trên thế giới. Các vùng này độc lập với nhau và dữ liệu không được chuyển giữa các vùng theo mặc định.</p>
}

// question: 1.14 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Dịch vụ nào của AWS tập trung vào việc tự động hóa hạ tầng của bạn bằng cách sử dụng các template (blueprints) để định nghĩa và quản lý tài nguyên?</p>{
	~[moodle]AWS Lambda.#<p>AWS Lambda tự động hóa các tác vụ vận hành bằng cách chạy mã mà không cần máy chủ.</p>
	~[moodle]Amazon EC2.#<p>Amazon EC2 cung cấp máy ảo, không phải tự động hóa hạ tầng tổng thể.</p>
	=[moodle]AWS CloudFormation.
	~[moodle]Amazon S3.#<p>Amazon S3 là dịch vụ lưu trữ đối tượng.</p>
	####<p><strong>Giải thích</strong>: CloudFormation là dịch vụ tự động hóa hạ tầng của bạn. Blueprints (hoặc template) là mô tả hệ thống của bạn chứa tất cả tài nguyên và các phụ thuộc của chúng, được chuyển thành hệ thống đang chạy.</p>
}

// question: 1.15 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Điều gì xảy ra khi bạn định cấu hình một tài nguyên trên AWS Management Console, CLI hoặc SDK?</p>{
	~[moodle]Các công cụ này trực tiếp thực thi các lệnh trên phần cứng vật lý của AWS.#<p>Người dùng không tương tác trực tiếp với phần cứng vật lý; API là lớp trừu tượng trung gian.</p>
	=[moodle]Các công cụ này thực hiện các lệnh gọi đến API của AWS để quản lý dịch vụ.
	~[moodle]Chúng tạo ra các bản sao lưu tự động cho tất cả các tài nguyên đã thay đổi.#<p>Tự động tạo bản sao lưu là một tính năng cụ thể của một số dịch vụ (ví dụ: RDS), không phải là hành động chung của mọi cấu hình.</p>
	~[moodle]Chúng chỉ ghi lại các thay đổi vào một tệp cấu hình cục bộ mà không ảnh hưởng đến đám mây.#<p>Các công cụ này tương tác trực tiếp với các dịch vụ trên đám mây, không chỉ là tệp cấu hình cục bộ.</p>
	####<p><strong>Giải thích</strong>: API đóng vai trò là giao diện giữa các dịch vụ AWS và ứng dụng của bạn. Management Console, CLI và SDK đều sử dụng các lệnh gọi API để tương tác với AWS.</p>
}

// question: 1.16 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>AWS cung cấp tính năng "Free Tier" cho người dùng mới và các trường hợp sử dụng nhất định với mục đích gì?</p>{
	~[moodle]Cung cấp tất cả các dịch vụ AWS miễn phí vĩnh viễn không giới hạn.#<p>Free Tier có giới hạn về thời gian hoặc mức sử dụng, không phải miễn phí vĩnh viễn cho tất cả dịch vụ.</p>
	=[moodle]Cho phép người dùng thử nghiệm các dịch vụ AWS mà không phải trả phí trong một giới hạn nhất định.
	~[moodle]Cung cấp một bộ các dịch vụ cơ bản hoàn toàn không thể mở rộng.#<p>Các dịch vụ trong Free Tier vẫn có khả năng mở rộng trong giới hạn của chúng.</p>
	~[moodle]Dành riêng cho các dự án nghiên cứu và phát triển phi lợi nhuận.#<p>Free Tier dành cho tất cả người dùng mới, không giới hạn cho các dự án phi lợi nhuận.</p>
	####<p><strong>Giải thích</strong>: Free Tier là cơ hội dùng thử AWS mà không phải trả tiền trong một giới hạn nhất định. Nó bao gồm 750 giờ máy ảo nhỏ, 750 giờ bộ cân bằng tải, 5 GB lưu trữ đối tượng, và 20 GB cơ sở dữ liệu nhỏ.</p>
}

// question: 1.17 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Một trong những cách AWS mang lại độ tin cậy ("reliability") cao là gì?</p>{
	~[moodle]Bắt buộc tất cả các ứng dụng phải chạy trên một máy chủ duy nhất để đơn giản hóa.#<p>Điều này đi ngược lại nguyên tắc thiết kế hệ thống phân tán và khả năng chống lỗi của AWS.</p>
	~[moodle]Hướng dẫn người dùng chỉ sử dụng các dịch vụ có thời gian ngừng hoạt động tối thiểu.#<p>Độ tin cậy là một tính năng tích hợp của nhiều dịch vụ, không phải chỉ là hướng dẫn cho người dùng.</p>
	=[moodle]Thiết kế các dịch vụ "được xây dựng để chống lỗi", với khả năng phục hồi tự động khỏi các sự cố.
	~[moodle]Cung cấp bảo hiểm cho tất cả các sự cố ngừng hoạt động của hệ thống khách hàng.#<p>AWS cung cấp các cơ chế để xây dựng hệ thống đáng tin cậy, không phải bảo hiểm trực tiếp cho sự cố ngừng hoạt động của khách hàng.</p>
	####<p><strong>Giải thích</strong>: AWS được xây dựng để chống lỗi (độ tin cậy). Hầu hết các dịch vụ AWS đều có sẵn tính năng sẵn sàng cao hoặc khả năng chịu lỗi theo mặc định. Ví dụ, dịch vụ cơ sở dữ liệu được cung cấp với khả năng sao chép và xử lý lỗi tự động.</p>
}

// question: 1.18 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>AWS CLI (Command Line Interface) mang lại lợi ích gì so với việc sử dụng Management Console cho các tác vụ phức tạp?</p>{
	~[moodle]Nó yêu cầu kiến thức lập trình chuyên sâu hơn để thực hiện các lệnh đơn giản.#<p>CLI có thể đơn giản để thực hiện các lệnh cơ bản và trở nên mạnh mẽ hơn với các tập lệnh, nhưng không nhất thiết yêu cầu kiến thức lập trình chuyên sâu cho mọi lệnh.</p>
	=[moodle]Nó cho phép tự động hóa các quy trình phức tạp thông qua các tập lệnh (scripts).
	~[moodle]Nó chỉ có sẵn trên các hệ điều hành độc quyền của AWS.#<p>CLI có sẵn trên Linux, macOS và Windows.</p>
	~[moodle]Nó cung cấp giao diện đồ họa phong phú hơn cho việc quản lý tài nguyên.#<p>Management Console cung cấp giao diện đồ họa, trong khi CLI là giao diện dòng lệnh.</p>
	####<p><strong>Giải thích</strong>: CLI cho phép bạn quản lý và truy cập các dịch vụ AWS từ terminal. Nó cho phép tự động hóa mọi thứ, bao gồm tạo mạng, khởi động cụm máy ảo hoặc triển khai cơ sở dữ liệu quan hệ.</p>
}

// question: 1.19 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Khi chạy một ứng dụng web trên AWS, việc sử dụng Mạng phân phối nội dung (CDN) có thể giúp cải thiện điều gì?</p>{
	~[moodle]Tăng chi phí bảo trì và vận hành máy chủ.#<p>CDN thường giúp giảm chi phí bằng cách giảm tải cho các máy chủ gốc và tối ưu hóa phân phối nội dung.</p>
	~[moodle]Giảm hiệu suất bằng cách thêm một lớp trung gian.#<p>Mục tiêu của CDN là cải thiện hiệu suất bằng cách giảm khoảng cách vật lý giữa nội dung và người dùng, không phải giảm hiệu suất.</p>
	=[moodle]Cải thiện hiệu suất bằng cách lưu trữ nội dung gần người dùng hơn.
	~[moodle]Giới hạn quyền truy cập vào trang web từ các khu vực địa lý nhất định.#<p>CDN phân phối nội dung rộng rãi hơn, không giới hạn quyền truy cập theo vùng địa lý mà là tối ưu hóa nó.</p>
	####<p><strong>Giải thích</strong>: CDN giúp cải thiện hiệu suất bằng cách phân phối nội dung tĩnh từ các máy chủ gần người dùng hơn, giảm độ trễ.</p>
}

// question: 1.20 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Đâu là một dịch vụ lưu trữ đối tượng (Object store) của AWS được thiết kế để lưu trữ dữ liệu không giới hạn kích thước và thường được sử dụng cho các trường hợp như sao lưu dữ liệu hoặc lưu trữ nội dung trang web tĩnh?</p>{
	~[moodle]Amazon Elastic Block Store (EBS).#<p>EBS cung cấp lưu trữ cấp khối được gắn qua mạng cho các phiên bản EC2.</p>
	=[moodle]Amazon S3 (Simple Storage Service).
	~[moodle]Amazon Elastic File System (EFS).#<p>EFS là một hệ thống tệp mạng (network filesystem) để chia sẻ dữ liệu giữa các máy ảo.</p>
	~[moodle]Amazon Relational Database Service (RDS).#<p>RDS là dịch vụ cơ sở dữ liệu quan hệ được quản lý.</p>
	####<p><strong>Giải thích</strong>: Amazon S3 là một dịch vụ lưu trữ đối tượng (object store) để lưu dữ liệu mà không có bất kỳ hạn chế kích thước nào và là một trong những dịch vụ lâu đời nhất của AWS. Các trường hợp sử dụng điển hình bao gồm lưu trữ và phân phối nội dung trang web tĩnh hoặc sao lưu dữ liệu.</p>
}

// question: 1.21 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Khi chạy ứng dụng Java EE trên AWS, mục tiêu chính của việc định nghĩa một mạng ảo (VPC) trong đám mây và kết nối nó với mạng công ty qua VPN là gì?</p>{
	~[moodle]Để cô lập hoàn toàn ứng dụng khỏi mạng công ty và internet.#<p>Mạng ảo được kết nối với mạng công ty, không phải cô lập hoàn toàn.</p>
	=[moodle]Để giảm chi phí và tăng tính linh hoạt bằng cách di chuyển một phần ứng dụng kinh doanh lên AWS.
	~[moodle]Để chỉ chạy các ứng dụng mã nguồn mở trên các máy ảo.#<p>Việc này không giới hạn loại ứng dụng được chạy, có thể bao gồm cả ứng dụng Java EE.</p>
	~[moodle]Để loại bỏ hoàn toàn nhu cầu về cơ sở hạ tầng mạng truyền thống.#<p>Nó bổ sung hoặc thay thế hạ tầng mạng truyền thống, không loại bỏ hoàn toàn nhu cầu về mạng.</p>
	####<p><strong>Giải thích</strong>: Maureen muốn chuyển một phần ứng dụng kinh doanh của công ty mình lên AWS khi hợp đồng trung tâm dữ liệu hết hạn để giảm chi phí và tăng tính linh hoạt. Việc này bao gồm định nghĩa một mạng ảo (VPC) và kết nối nó với mạng công ty qua VPN.</p>
}

// question: 1.22 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Định nghĩa nào mô tả đúng nhất "Platform as a Service (PaaS)" trong điện toán đám mây?</p>{
	~[moodle]Cung cấp các ứng dụng phần mềm được đóng gói hoàn chỉnh cho người dùng cuối.#<p>Đây là mô tả của SaaS (Software as a Service), cung cấp ứng dụng hoàn chỉnh cho người dùng.</p>
	~[moodle]Cung cấp các tài nguyên cơ bản như khả năng điện toán, lưu trữ và mạng dưới dạng máy ảo.#<p>Đây là mô tả của IaaS (Infrastructure as a Service), cung cấp các tài nguyên cơ bản.</p>
	=[moodle]Cung cấp các nền tảng để triển khai ứng dụng tùy chỉnh lên đám mây, ví dụ như AWS Elastic Beanstalk.
	~[moodle]Cung cấp dịch vụ quản lý cơ sở dữ liệu quan hệ được quản lý hoàn toàn.#<p>Dịch vụ quản lý cơ sở dữ liệu quan hệ là một ví dụ cụ thể của PaaS hoặc đôi khi được coi là một loại dịch vụ quản lý cấp cao hơn, nhưng PaaS rộng hơn nhiều.</p>
	####<p><strong>Giải thích</strong>: PaaS (Platform as a Service) cung cấp các nền tảng để triển khai các ứng dụng tùy chỉnh lên đám mây, ví dụ như AWS Elastic Beanstalk. Nó trừu tượng hóa các tài nguyên cơ bản, cho phép nhà phát triển tập trung vào mã ứng dụng.</p>
}

// question: 1.23 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>AWS được Gartner xếp hạng là "leader" trong Magic Quadrant for Cloud Infrastructure as a Service vào năm 2017, điều này chứng tỏ điều gì về AWS?</p>{
	~[moodle]AWS là người chơi duy nhất trên thị trường IaaS.#<p>Magic Quadrant phân nhóm các nhà cung cấp thành bốn loại (niche players, challengers, visionaries, leaders), cho thấy có nhiều người chơi khác nhau trên thị trường.</p>
	=[moodle]AWS có tốc độ đổi mới và chất lượng cao.
	~[moodle]AWS chỉ tập trung vào các nhà cung cấp dịch vụ nhỏ.#<p>AWS đã được các doanh nghiệp, các startup và chính phủ áp dụng rộng rãi, không chỉ các nhà cung cấp dịch vụ nhỏ.</p>
	~[moodle]AWS không có sự tăng trưởng đáng kể so với các năm trước.#<p>AWS báo cáo doanh thu ròng 4,1 tỷ USD vào Q2/2017 với tốc độ tăng trưởng 42% so với cùng kỳ năm trước (Q3/2016 so với Q3/2017), cho thấy sự tăng trưởng đáng kể.</p>
	####<p><strong>Giải thích</strong>: Việc Gartner phân loại AWS là "leader" trong Magic Quadrant for Cloud Infrastructure as a Service vào năm 2017 chứng tỏ tốc độ và chất lượng đổi mới cao của AWS.</p>
}

// question: 1.24 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Lợi ích nào của AWS cho phép bạn tự động hóa việc tạo mạng, khởi động cụm máy ảo hoặc triển khai cơ sở dữ liệu quan hệ bằng cách viết mã?</p>{
	~[moodle]AWS Management Console.#<p>AWS Management Console là giao diện người dùng đồ họa, không phải công cụ để viết mã tự động hóa trực tiếp.</p>
	~[moodle]AWS Marketplace.#<p>AWS Marketplace là nơi tìm kiếm và triển khai phần mềm, không phải là cơ chế để tự động hóa hạ tầng bằng mã.</p>
	=[moodle]AWS API.
	~[moodle]AWS Support.#<p>AWS Support cung cấp hỗ trợ kỹ thuật, không phải là một công cụ tự động hóa.</p>
	####<p><strong>Giải thích</strong>: Bởi vì AWS có API, bạn có thể tự động hóa mọi thứ bằng cách viết mã để tạo mạng, khởi động cụm máy ảo hoặc triển khai cơ sở dữ liệu quan hệ. API là giao diện cơ bản cho tất cả các dịch vụ AWS.</p>
}

// question: 1.25 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Theo nguồn tài liệu, các trung tâm dữ liệu AWS được phân bổ ở đâu trên thế giới?</p>{
	~[moodle]Chỉ ở Bắc Mỹ và châu Âu.#<p>Phạm vi địa lý của AWS rộng hơn nhiều so với chỉ Bắc Mỹ và châu Âu.</p>
	~[moodle]Chỉ tập trung ở Hoa Kỳ để đảm bảo an ninh.#<p>Các trung tâm dữ liệu AWS được phân phối toàn cầu, không chỉ tập trung ở Hoa Kỳ.</p>
	=[moodle]Ở Bắc Mỹ, Nam Mỹ, châu Âu, châu Á và châu Úc.
	~[moodle]Hiện tại chỉ có mặt ở một số quốc gia được chọn lọc.#<p>Mặc dù có một số trung tâm dữ liệu có điều kiện đặc biệt (ví dụ: Trung Quốc), AWS đã có hạ tầng toàn cầu rộng khắp.</p>
	####<p><strong>Giải thích</strong>: Các trung tâm dữ liệu AWS được phân bổ trên toàn thế giới ở Bắc Mỹ, Nam Mỹ, châu Âu, châu Á và châu Úc. Điều này cho phép phục vụ khách hàng trên toàn cầu với độ trễ thấp.</p>
}

// question: 1.26 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Khả năng "Built for failure (reliability)" của AWS có nghĩa là gì?</p>{
	~[moodle]Các dịch vụ AWS được thiết kế để thường xuyên gặp lỗi nhằm mục đích kiểm tra khả năng phục hồi của hệ thống.#<p>Mục tiêu là xây dựng hệ thống đáng tin cậy, không phải thiết kế để thường xuyên gặp lỗi.</p>
	=[moodle]Hầu hết các dịch vụ AWS đều có khả năng sẵn sàng cao hoặc khả năng chịu lỗi theo mặc định, hỗ trợ xây dựng hệ thống đáng tin cậy.
	~[moodle]AWS sẽ chịu trách nhiệm hoàn toàn cho mọi lỗi hệ thống của khách hàng.#<p>AWS tuân theo mô hình trách nhiệm chia sẻ, nơi khách hàng cũng có trách nhiệm đảm bảo bảo mật và độ tin cậy của ứng dụng của mình.</p>
	~[moodle]Khách hàng phải tự thiết kế và triển khai tất cả các cơ chế phục hồi lỗi cho ứng dụng của mình.#<p>AWS cung cấp các dịch vụ và công cụ hỗ trợ mạnh mẽ, giảm bớt gánh nặng cho khách hàng trong việc tự xây dựng tất cả các cơ chế phục hồi lỗi.</p>
	####<p><strong>Giải thích</strong>: "Built for failure (reliability)" có nghĩa là hầu hết các dịch vụ AWS đều có khả năng sẵn sàng cao hoặc khả năng chịu lỗi theo mặc định, giúp khách hàng xây dựng hệ thống một cách đáng tin cậy. Ví dụ, dịch vụ cơ sở dữ liệu được cung cấp với khả năng sao chép và xử lý lỗi tự động.</p>
}

// question: 1.27 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Trong mô hình định giá "trả tiền theo mức sử dụng" của AWS, các máy ảo EC2 chạy Linux thường được tính phí theo đơn vị nào?</p>{
	~[moodle]Mỗi giờ hoạt động.#<p>Tính phí theo giờ là một đơn vị phổ biến nhưng không phải mặc định cho các instance Linux EC2.</p>
	~[moodle]Mỗi ngày hoạt động.#<p>Tính phí theo ngày không phải là đơn vị được đề cập cho instance Linux EC2.</p>
	=[moodle]Mỗi giây hoạt động, với mức tối thiểu 60 giây.
	~[moodle]Mỗi gigabyte dữ liệu được xử lý.#<p>Tính phí theo dữ liệu xử lý thường áp dụng cho lưu trữ hoặc truyền dữ liệu, không phải thời gian chạy máy ảo.</p>
	####<p><strong>Giải thích</strong>: Hầu hết các instance EC2 chạy Linux (như Amazon Linux hoặc Ubuntu) được tính phí theo giây. Mức phí tối thiểu cho mỗi instance là 60 giây.</p>
}

// question: 1.28 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Khi tạo một tài khoản AWS mới, điều đầu tiên bạn cần cung cấp trong quá trình đăng ký là gì?</p>{
	~[moodle]Thông tin thanh toán (thẻ tín dụng).#<p>Thông tin thanh toán (thẻ tín dụng) được yêu cầu ở bước sau đó.</p>
	~[moodle]Thông tin liên hệ.#<p>Thông tin liên hệ được yêu cầu ở bước thứ hai sau khi cung cấp thông tin đăng nhập.</p>
	=[moodle]Địa chỉ email và mật khẩu tài khoản root.
	~[moodle]Tên miền cho ứng dụng của bạn.#<p>Tên miền không phải là thông tin bắt buộc khi tạo tài khoản AWS.</p>
	####<p><strong>Giải thích</strong>: Bước đầu tiên khi đăng ký tài khoản AWS mới là cung cấp địa chỉ email và mật khẩu cho tài khoản root. Đây là thông tin đăng nhập ban đầu.</p>
}

// question: 1.29 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Định nghĩa nào mô tả đúng nhất "Software as a Service (SaaS)" trong điện toán đám mây?</p>{
	~[moodle]Các nền tảng để triển khai các ứng dụng tùy chỉnh, ví dụ như AWS Elastic Beanstalk.#<p>Đây là mô tả của PaaS (Platform as a Service).</p>
	~[moodle]Các tài nguyên cơ bản như máy ảo, lưu trữ và mạng, ví dụ như Amazon EC2.#<p>Đây là mô tả của IaaS (Infrastructure as a Service).</p>
	=[moodle]Các ứng dụng phần mềm được đóng gói hoàn chỉnh chạy trong đám mây, ví dụ như Amazon WorkSpaces.
	~[moodle]Các công cụ quản lý hạ tầng dưới dạng mã (Infrastructure as Code).#<p>Infrastructure as Code là một phương pháp quản lý hạ tầng, không phải là một phân loại dịch vụ đám mây.</p>
	####<p><strong>Giải thích</strong>: SaaS (Software as a Service) kết hợp hạ tầng và phần mềm chạy trong đám mây, cung cấp các ứng dụng phần mềm hoàn chỉnh cho người dùng, ví dụ như Amazon WorkSpaces, Google Apps for Work, và Microsoft Office 365.</p>
}

// question: 1.30 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Lợi ích "Reducing time to market" của AWS được thể hiện như thế nào?</p>{
	~[moodle]AWS cung cấp các dịch vụ miễn phí vĩnh viễn, giảm gánh nặng tài chính ban đầu.#<p>Mặc dù có Free Tier, AWS không cung cấp dịch vụ miễn phí vĩnh viễn, và "Reducing time to market" không chỉ liên quan đến chi phí.</p>
	=[moodle]Khách hàng có thể yêu cầu một máy ảo mới và có sẵn để sử dụng chỉ trong vài phút, tăng tốc quá trình phát triển.
	~[moodle]AWS tự động kiểm thử tất cả các ứng dụng trước khi triển khai, giảm lỗi phần mềm.#<p>AWS không tự động kiểm thử ứng dụng của khách hàng; đó là trách nhiệm của khách hàng.</p>
	~[moodle]AWS cung cấp hỗ trợ kỹ thuật 24/7, giúp giải quyết các vấn đề nhanh chóng.#<p>Dịch vụ hỗ trợ kỹ thuật có sẵn, nhưng lợi ích chính của việc giảm thời gian đưa sản phẩm ra thị trường nằm ở tốc độ cấp phát tài nguyên.</p>
	####<p><strong>Giải thích</strong>: Lợi ích "Reducing time to market" (Giảm thời gian đưa sản phẩm ra thị trường) của AWS được thể hiện qua khả năng yêu cầu một máy ảo mới và có sẵn để sử dụng chỉ trong vài phút, cùng với các dịch vụ khác có sẵn theo yêu cầu. Điều này rút ngắn chu kỳ phản hồi và tăng tốc quá trình phát triển.</p>
}

// question: 1.31 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>AWS Management Console liệt kê bao nhiêu dịch vụ AWS trong tổng quan của nó?</p>{
	~[moodle]Khoảng 50 dịch vụ.#<p>Các con số này không chính xác theo thông tin trong nguồn tài liệu.</p>
	~[moodle]Khoảng 75 dịch vụ.#<p>Các con số này không chính xác theo thông tin trong nguồn tài liệu.</p>
	=[moodle]Khoảng 98 dịch vụ.
	~[moodle]Hơn 200 dịch vụ.#<p>Các con số này không chính xác theo thông tin trong nguồn tài liệu.</p>
	####<p><strong>Giải thích</strong>: Khi đăng nhập vào giao diện web của AWS, bạn sẽ được trình bày với tổng quan liệt kê 98 dịch vụ.</p>
}

// question: 1.32 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Điều nào sau đây là một ví dụ về dịch vụ IaaS mà AWS cung cấp?</p>{
	~[moodle]Amazon WorkSpaces (ứng dụng văn phòng).#<p>Amazon WorkSpaces là một ví dụ về SaaS (Software as a Service).</p>
	~[moodle]AWS Elastic Beanstalk (nền tảng triển khai ứng dụng).#<p>AWS Elastic Beanstalk là một ví dụ về PaaS (Platform as a Service).</p>
	=[moodle]Amazon EC2 (máy ảo).
	~[moodle]Amazon Route 53 (dịch vụ DNS).#<p>Amazon Route 53 là một dịch vụ mạng (DNS), thường được phân loại riêng hoặc là một phần của IaaS, nhưng EC2 là ví dụ điển hình nhất của IaaS về khả năng điện toán.</p>
	####<p><strong>Giải thích</strong>: Amazon EC2 là một ví dụ về dịch vụ IaaS (Infrastructure as a Service), cung cấp máy ảo làm tài nguyên điện toán cơ bản.</p>
}

// question: 1.33 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Lợi ích nào của việc sử dụng AWS giúp khách hàng tuân thủ các yêu cầu bảo vệ dữ liệu khu vực và hưởng lợi từ giá cơ sở hạ tầng khác nhau?</p>{
	~[moodle]Nền tảng đổi mới và phát triển nhanh chóng.#<p>Nền tảng đổi mới tập trung vào việc giới thiệu các tính năng mới, không trực tiếp vào vấn đề tuân thủ khu vực hoặc giá.</p>
	~[moodle]Dịch vụ giải quyết vấn đề chung.#<p>Dịch vụ giải quyết vấn đề chung liên quan đến việc cung cấp các giải pháp cho các thách thức phổ biến, không phải vị trí địa lý.</p>
	=[moodle]Hạ tầng toàn cầu.
	~[moodle]Kinh tế theo quy mô.#<p>Kinh tế theo quy mô liên quan đến việc giảm giá do quy mô lớn, nhưng hạ tầng toàn cầu là điều kiện tiên quyết cho việc lựa chọn vùng địa lý cụ thể.</p>
	####<p><strong>Giải thích</strong>: Sử dụng hạ tầng toàn cầu của AWS mang lại các lợi ích như độ trễ mạng thấp giữa khách hàng và hạ tầng, khả năng tuân thủ các yêu cầu bảo vệ dữ liệu khu vực, và hưởng lợi từ các mức giá cơ sở hạ tầng khác nhau ở các khu vực khác nhau.</p>
}

// question: 1.34 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Chứng nhận bảo mật nào sau đây liên quan đến tiêu chuẩn an toàn thông tin được chứng nhận bởi một tổ chức độc lập và có uy tín?</p>{
	~[moodle]PCI DSS Level 1.#<p>PCI DSS Level 1 là tiêu chuẩn an ninh dữ liệu cho ngành thẻ thanh toán (PCI).</p>
	~[moodle]ISO 9001.#<p>ISO 9001 là một phương pháp quản lý chất lượng tiêu chuẩn hóa được sử dụng trên toàn thế giới.</p>
	=[moodle]ISO 27001.
	~[moodle]HIPAA Compliance.#<p>HIPAA (Health Insurance Portability and Accountability Act) là quy định của Hoa Kỳ liên quan đến bảo mật dữ liệu y tế, không được đề cập trực tiếp là một chứng nhận toàn cầu trong nguồn.</p>
	####<p><strong>Giải thích</strong>: ISO 27001 là một tiêu chuẩn an toàn thông tin trên toàn thế giới được chứng nhận bởi một tổ chức chứng nhận độc lập và có uy tín, đảm bảo chất lượng và bảo mật của các dịch vụ AWS.</p>
}

// question: 1.35 name: Chapter 1: Amazon Web Services
::Chapter 1\: Amazon Web Services::[html]<p>Tại sao AWS được coi là một "Professional partner" cho các doanh nghiệp?</p>{
	~[moodle]Vì AWS luôn cung cấp dịch vụ miễn phí cho các doanh nghiệp lớn.#<p>AWS hoạt động theo mô hình trả tiền theo mức sử dụng, không cung cấp dịch vụ miễn phí cho các doanh nghiệp lớn.</p>
	=[moodle]Vì chất lượng và bảo mật của các dịch vụ AWS tuân thủ các tiêu chuẩn và chứng nhận mới nhất.
	~[moodle]Vì AWS chỉ phục vụ các tập đoàn công nghệ lớn như Netflix và Amazon.com.#<p>Mặc dù các công ty lớn sử dụng AWS, nó cũng phục vụ startup, công ty vừa và nhỏ.</p>
	~[moodle]Vì AWS loại bỏ hoàn toàn trách nhiệm của khách hàng về bảo mật hệ thống.#<p>Theo mô hình trách nhiệm chia sẻ, khách hàng vẫn chịu trách nhiệm về bảo mật trong đám mây.</p>
	####<p><strong>Giải thích</strong>: AWS được coi là "Professional partner" vì chất lượng và bảo mật của các dịch vụ AWS tuân thủ các tiêu chuẩn và chứng nhận mới nhất, như ISO 27001, ISO 9001 và PCI DSS Level 1.</p>
}

// Chapter 2: A simple example: WordPress in five minutes
// question: 2 name: Switch category to $module$/top/Chapter 2: A simple example: WordPress in five minutes
$CATEGORY: $module$/top/Chapter 2: A simple example: WordPress in five minutes

// question: 2.1 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Mục tiêu chính của ví dụ WordPress trong chương này là gì?</p>{
	~[moodle]Hướng dẫn cách tạo một ứng dụng web phức tạp từ đầu bằng mã hóa tùy chỉnh.#<p>Ví dụ này tập trung vào việc sử dụng các dịch vụ AWS có sẵn để triển khai WordPress, không phải xây dựng ứng dụng tùy chỉnh từ đầu.</p>
	=[moodle]Đánh giá khả năng di chuyển một ứng dụng web đơn giản lên AWS bằng cách thiết lập hạ tầng đám mây mẫu trong vòng năm phút.
	~[moodle]Cung cấp một giải pháp lưu trữ dữ liệu lâu dài và có chi phí thấp cho các tệp lớn.#<p>Chương tập trung vào WordPress và các dịch vụ hỗ trợ, không phải giải pháp lưu trữ lâu dài cụ thể như Glacier.</p>
	~[moodle]Minh họa cách tối ưu hóa hiệu suất của một cơ sở dữ liệu quan hệ cho lưu lượng truy cập cao.#<p>Mặc dù có đề cập đến cơ sở dữ liệu và hiệu suất, mục tiêu chính là triển khai WordPress và đánh giá chi phí tổng thể của hạ tầng.</p>
	####<p><strong>Giải thích</strong>: Trong chương này, bạn sẽ đánh giá việc di chuyển một ứng dụng web đơn giản lên AWS bằng cách thiết lập một hạ tầng đám mây mẫu trong vòng năm phút. Mục tiêu là thiết lập hạ tầng có tính sẵn sàng cao, ước tính chi phí và xóa hạ tầng sau đó.</p>
}

// question: 2.2 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>WordPress là một hệ thống quản lý nội dung (CMS) được viết bằng ngôn ngữ lập trình nào và sử dụng loại cơ sở dữ liệu nào?</p>{
	~[moodle]Java và cơ sở dữ liệu Oracle.#<p>Các tùy chọn này không đúng với thông tin trong nguồn tài liệu.</p>
	~[moodle]Python và cơ sở dữ liệu PostgreSQL.#<p>Các tùy chọn này không đúng với thông tin trong nguồn tài liệu.</p>
	=[moodle]PHP và cơ sở dữ liệu MySQL.
	~[moodle]Node.js và cơ sở dữ liệu MongoDB.#<p>Các tùy chọn này không đúng với thông tin trong nguồn tài liệu.</p>
	####<p><strong>Giải thích</strong>: WordPress được viết bằng PHP và sử dụng cơ sở dữ liệu MySQL để lưu trữ dữ liệu.</p>
}

// question: 2.3 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Dịch vụ AWS nào cho phép bạn tạo một hạ tầng WordPress có khả năng sẵn sàng cao trong vòng vài cú nhấp chuột bằng cách sử dụng một "blueprint"?</p>{
	~[moodle]Amazon EC2.#<p>EC2 cung cấp máy ảo, nhưng không tự động tạo toàn bộ hạ tầng WordPress có khả năng sẵn sàng cao bao gồm tất cả các dịch vụ khác.</p>
	~[moodle]AWS Identity and Access Management (IAM).#<p>IAM dùng để quản lý quyền truy cập, không phải triển khai hạ tầng.</p>
	=[moodle]AWS CloudFormation.
	~[moodle]Amazon Simple Storage Service (S3).#<p>S3 là dịch vụ lưu trữ đối tượng, không phải triển khai hạ tầng tổng thể.</p>
	####<p><strong>Giải thích</strong>: Việc tạo tất cả các thành phần hạ tầng WordPress có thể thực hiện chỉ với vài cú nhấp chuột bằng cách sử dụng dịch vụ AWS CloudFormation, được đề cập sẽ làm tất cả tự động trong nền dựa trên một blueprint.</p>
}

// question: 2.4 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Trong ví dụ WordPress, dịch vụ AWS Elastic Load Balancing (ELB) được sử dụng với mục đích gì?</p>{
	~[moodle]Để lưu trữ tất cả các tệp tĩnh của WordPress.#<p>Lưu trữ tệp tĩnh thường được thực hiện bởi S3 hoặc EFS trong ví dụ này.</p>
	=[moodle]Để phân phối lưu lượng truy cập đến một nhóm máy ảo và đảm bảo tính sẵn sàng cao.
	~[moodle]Để cung cấp một cơ sở dữ liệu quan hệ được quản lý.#<p>Cơ sở dữ liệu quan hệ được quản lý bởi RDS.</p>
	~[moodle]Để chạy mã xử lý sự kiện mà không cần máy chủ.#<p>Chạy mã xử lý sự kiện mà không cần máy chủ là chức năng của Lambda.</p>
	####<p><strong>Giải thích</strong>: Elastic Load Balancing (ELB) là một dịch vụ cân bằng tải do AWS cung cấp. Bộ cân bằng tải phân phối lưu lượng truy cập đến một nhóm máy ảo và có khả năng sẵn sàng cao theo mặc định.</p>
}

// question: 2.5 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Vai trò của Security Groups (Nhóm bảo mật) trong hạ tầng WordPress mẫu là gì?</p>{
	~[moodle]Để quản lý việc triển khai và cập nhật ứng dụng WordPress.#<p>Việc triển khai và cập nhật ứng dụng được thực hiện bởi các dịch vụ khác như CloudFormation hoặc Beanstalk.</p>
	=[moodle]Để kiểm soát lưu lượng mạng đến và đi từ máy ảo, cơ sở dữ liệu hoặc bộ cân bằng tải bằng tường lửa ảo.
	~[moodle]Để sao lưu tự động dữ liệu của cơ sở dữ liệu MySQL.#<p>Sao lưu cơ sở dữ liệu được thực hiện bởi RDS.</p>
	~[moodle]Để chia sẻ dữ liệu giữa nhiều máy ảo một cách dễ dàng.#<p>Chia sẻ dữ liệu giữa các máy ảo được thực hiện bởi EFS.</p>
	####<p><strong>Giải thích</strong>: Security Groups hoạt động như tường lửa ảo cho các tài nguyên của bạn. Bạn cần định nghĩa các quy tắc cụ thể để kiểm soát lưu lượng đến và đi cho từng loại tài nguyên, ví dụ: HTTP đến bộ cân bằng tải hoặc truy cập cơ sở dữ liệu từ máy ảo.</p>
}

// question: 2.6 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Trong quy trình tạo hạ tầng WordPress bằng CloudFormation, việc chỉ định "Stack name" (Tên Stack) và "KeyName" (Tên khóa) ở bước 2 của wizard có mục đích gì?</p>{
	~[moodle]Tên Stack chỉ là một chuỗi ngẫu nhiên không có ý nghĩa thực tế, KeyName dùng để cấp quyền truy cập vào bảng điều khiển.#<p>Tên Stack là quan trọng để quản lý hạ tầng; KeyName dùng để xác thực SSH, không phải cấp quyền truy cập bảng điều khiển.</p>
	=[moodle]Tên Stack định danh cho hạ tầng CloudFormation của bạn, và KeyName để kết nối SSH đến máy ảo.
	~[moodle]Tên Stack là tên người dùng của cơ sở dữ liệu, KeyName là tên của bộ cân bằng tải.#<p>Các tham số này có mục đích khác nhau, không phải là tên người dùng cơ sở dữ liệu hay tên bộ cân bằng tải.</p>
	~[moodle]Tên Stack để kích hoạt Free Tier, KeyName để xác định vùng địa lý.#<p>Các tham số này không liên quan trực tiếp đến Free Tier hoặc vùng địa lý.</p>
	####<p><strong>Giải thích</strong>: Bạn chỉ định wordpress làm Tên Stack để định danh cho hạ tầng CloudFormation của mình, và đặt KeyName (ví dụ: mykey) là cần thiết để kết nối SSH tới các máy ảo được tạo ra.</p>
}

// question: 2.7 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Để khám phá các tài nguyên AWS thuộc hạ tầng WordPress đã tạo, bạn nên sử dụng tính năng nào trong Management Console để nhóm các tài nguyên lại với nhau?</p>{
	~[moodle]AWS Billing Dashboard.#<p>Billing Dashboard dùng để theo dõi chi phí.</p>
	=[moodle]Resource Groups.
	~[moodle]CloudWatch Alarms.#<p>CloudWatch Alarms dùng để giám sát và cảnh báo dựa trên các chỉ số.</p>
	~[moodle]IAM Policies.#<p>IAM Policies dùng để quản lý quyền truy cập và ủy quyền.</p>
	####<p><strong>Giải thích</strong>: Bạn đã gắn thẻ hạ tầng blog với khóa system và giá trị wordpress. Sau đó, bạn sẽ sử dụng thẻ đó để tạo một nhóm tài nguyên (Resource Group) cho hạ tầng WordPress của mình, giúp nhóm các tài nguyên liên quan lại với nhau.</p>
}

// question: 2.8 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi kiểm tra chi tiết một máy ảo (EC2 Instance) trong hạ tầng WordPress, thông tin nào sau đây giúp bạn xác định sức mạnh xử lý và bộ nhớ của nó?</p>{
	~[moodle]IPv4 Public IP.#<p>IPv4 Public IP là địa chỉ IP công khai, không liên quan đến sức mạnh xử lý.</p>
	~[moodle]AMI ID.#<p>AMI ID cho biết phiên bản hệ điều hành mà máy ảo dựa trên.</p>
	=[moodle]Instance type.
	~[moodle]Security groups.#<p>Security groups là cấu hình tường lửa, kiểm soát lưu lượng mạng đến và đi.</p>
	####<p><strong>Giải thích</strong>: Instance type cho bạn biết máy ảo EC2 của bạn mạnh đến mức nào, bao gồm thông tin về số lượng CPU ảo và dung lượng bộ nhớ.</p>
}

// question: 2.9 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Amazon RDS (Relational Database Service) được sử dụng trong ví dụ WordPress với vai trò gì?</p>{
	~[moodle]Để lưu trữ các tệp ảnh và video được tải lên bởi người dùng.#<p>Lưu trữ tệp ảnh và video thường được xử lý bởi EFS hoặc S3.</p>
	=[moodle]Để cung cấp một cơ sở dữ liệu MySQL được quản lý, có khả năng sao lưu và quản lý bản vá.
	~[moodle]Để chạy các tác vụ xử lý hàng loạt dữ liệu không liên quan đến cơ sở dữ liệu.#<p>Các tác vụ xử lý hàng loạt có thể sử dụng EC2 hoặc Lambda, nhưng không phải là vai trò chính của RDS trong ngữ cảnh này.</p>
	~[moodle]Để điều khiển lưu lượng mạng đến các máy chủ web.#<p>Điều khiển lưu lượng mạng là chức năng của ELB và Security Groups.</p>
	####<p><strong>Giải thích</strong>: Cơ sở dữ liệu MySQL là một phần quan trọng của hạ tầng WordPress. RDS cung cấp cơ sở dữ liệu SQL dưới dạng dịch vụ được quản lý, hoàn chỉnh với các bản sao lưu, quản lý bản vá và tính sẵn sàng cao.</p>
}

// question: 2.10 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Tại sao Elastic File System (EFS) lại được sử dụng trong ví dụ WordPress?</p>{
	~[moodle]Để cung cấp bộ nhớ đệm trong bộ nhớ cho dữ liệu thường xuyên truy cập.#<p>Bộ nhớ đệm trong bộ nhớ được cung cấp bởi ElastiCache.</p>
	~[moodle]Để lưu trữ dữ liệu tạm thời trên các ổ cứng vật lý gắn trực tiếp vào máy ảo.#<p>Lưu trữ dữ liệu tạm thời trên các ổ cứng vật lý gắn trực tiếp vào máy ảo là Instance Store.</p>
	=[moodle]Để lưu trữ các tệp và truy cập chúng từ nhiều máy ảo, duy trì tính đồng bộ.
	~[moodle]Để tạo các bản sao lưu tự động của cơ sở dữ liệu.#<p>Tạo bản sao lưu tự động của cơ sở dữ liệu là chức năng của RDS.</p>
	####<p><strong>Giải thích</strong>: EFS được sử dụng để lưu trữ các tệp và truy cập chúng từ nhiều máy ảo, duy trì tính đồng bộ. Tất cả các tệp thuộc về WordPress (bao gồm PHP, HTML, CSS, PNG và tệp tải lên của người dùng như hình ảnh) đều được lưu trữ trên EFS để có thể truy cập từ tất cả các máy ảo.</p>
}

// question: 2.11 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Ví dụ WordPress được đề cập trong chương này có được bao phủ hoàn toàn bởi Free Tier của AWS không?</p>{
	~[moodle]Không, ví dụ này sẽ phát sinh chi phí đáng kể ngay lập tức.#<p>Nguồn tài liệu rõ ràng nói rằng nó được bao phủ bởi Free Tier.</p>
	=[moodle]Có, miễn là bạn không chạy ví dụ này quá vài ngày và sử dụng một tài khoản AWS mới.
	~[moodle]Có, nhưng chỉ khi bạn sử dụng hệ điều hành Windows cho các máy ảo.#<p>Free Tier không phụ thuộc vào hệ điều hành cụ thể của máy ảo; nó bao gồm cả Linux và Windows.</p>
	~[moodle]Không, Free Tier chỉ áp dụng cho các dịch vụ lưu trữ.#<p>Free Tier bao gồm nhiều dịch vụ khác nhau như máy ảo EC2, bộ cân bằng tải, S3 và RDS.</p>
	####<p><strong>Giải thích</strong>: Ví dụ trong chương này được bao phủ hoàn toàn bởi Free Tier. Miễn là bạn không chạy ví dụ này quá vài ngày, bạn sẽ không phải trả bất kỳ khoản nào. Điều này chỉ áp dụng nếu bạn đã tạo một tài khoản AWS mới cho cuốn sách này và không có gì khác đang diễn ra trong tài khoản AWS của bạn.</p>
}

// question: 2.12 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi ước tính chi phí cho hạ tầng WordPress, yếu tố nào sau đây KHÔNG được bao gồm trong ước tính ban đầu từ AWS Simple Monthly Calculator?</p>{
	~[moodle]Chi phí cho các máy ảo EC2.#<p>Chi phí cho máy ảo EC2 được bao gồm trong ước tính.</p>
	~[moodle]Chi phí cho dịch vụ cơ sở dữ liệu RDS.#<p>Chi phí cho dịch vụ cơ sở dữ liệu RDS được bao gồm trong ước tính.</p>
	=[moodle]Chi phí cho Application Load Balancer (ALB).
	~[moodle]Tổng chi phí ước tính hàng tháng.#<p>Tổng chi phí ước tính hàng tháng luôn được hiển thị trong công cụ tính toán.</p>
	####<p><strong>Giải thích</strong>: Đáng tiếc là Application Load Balancer (ALB), một dịch vụ mới hơn một chút, vẫn chưa được bao gồm trong ước tính từ AWS Simple Monthly Calculator tại thời điểm viết tài liệu.</p>
}

// question: 2.13 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Mục đích của việc sử dụng một "template URL" khi tạo stack CloudFormation là gì?</p>{
	~[moodle]Để tải lên các tệp mã nguồn ứng dụng trực tiếp từ máy tính cục bộ của bạn.#<p>Tải lên mã nguồn ứng dụng thường được thực hiện thông qua các dịch vụ triển khai như Elastic Beanstalk hoặc OpsWorks, hoặc trực tiếp lên S3.</p>
	=[moodle]Để cung cấp một đường dẫn đến tệp blueprint định nghĩa hạ tầng AWS mà bạn muốn triển khai.
	~[moodle]Để xác định địa chỉ IP công khai của bộ cân bằng tải sẽ được tạo.#<p>Địa chỉ IP công khai của bộ cân bằng tải là một đầu ra của stack, không phải đầu vào khi tạo stack.</p>
	~[moodle]Để cấu hình thông tin đăng nhập quản trị cho cơ sở dữ liệu MySQL.#<p>Thông tin đăng nhập cơ sở dữ liệu thường là các tham số của template nhưng không phải là mục đích của template URL.</p>
	####<p><strong>Giải thích</strong>: Bạn chọn "Specify an Amazon S3 template URL" và nhập URL của template đã chuẩn bị cho chương này để sử dụng blueprint định nghĩa hạ tầng AWS mà bạn muốn triển khai. Template này là một tệp YAML mô tả các tài nguyên AWS.</p>
}

// question: 2.14 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi kiểm tra các bản ghi log của máy ảo trong hạ tầng WordPress, dịch vụ AWS nào được sử dụng để tìm kiếm và xem các bản ghi đó?</p>{
	~[moodle]Amazon S3.#<p>S3 là dịch vụ lưu trữ đối tượng.</p>
	=[moodle]AWS CloudWatch.
	~[moodle]Amazon DynamoDB.#<p>DynamoDB là cơ sở dữ liệu NoSQL.</p>
	~[moodle]AWS Elastic Beanstalk.#<p>Elastic Beanstalk là dịch vụ triển khai ứng dụng web, không phải để xem log.</p>
	####<p><strong>Giải thích</strong>: Bạn có thể sử dụng CloudWatch để tìm kiếm thông qua các bản ghi log của hàm Lambda hoặc để theo dõi tải của máy ảo. CloudWatch là dịch vụ giám sát và ghi nhật ký chính của AWS.</p>
}

// question: 2.15 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Điều gì sẽ xảy ra nếu bạn không dọn dẹp hạ tầng WordPress đã tạo sau khi hoàn thành ví dụ trong chương này?</p>{
	~[moodle]Hạ tầng sẽ tự động được xóa bởi AWS sau một khoảng thời gian nhất định.#<p>AWS không tự động xóa tài nguyên sau một thời gian nhất định mà không có cấu hình cụ thể từ người dùng.</p>
	~[moodle]Bạn có thể tiếp tục sử dụng nó miễn phí vĩnh viễn vì nó nằm trong Free Tier.#<p>Free Tier có giới hạn về thời gian và mức sử dụng, và việc vượt quá sẽ phát sinh chi phí.</p>
	=[moodle]Bạn có thể phải trả phí cho các tài nguyên đã sử dụng, đặc biệt nếu vượt quá giới hạn Free Tier.
	~[moodle]AWS sẽ gửi email nhắc nhở bạn dọn dẹp nhưng không tính phí.#<p>AWS sẽ tính phí nếu tài nguyên được sử dụng vượt quá giới hạn Free Tier, không chỉ gửi email nhắc nhở.</p>
	####<p><strong>Giải thích</strong>: Nếu bạn không dọn dẹp hạ tầng, bạn có thể phải trả phí cho các tài nguyên đã sử dụng, đặc biệt nếu bạn chạy ví dụ này quá vài ngày hoặc vượt quá giới hạn Free Tier. "Để tránh phát sinh chi phí, bạn nên luôn tắt các máy ảo mà bạn không sử dụng".</p>
}

// question: 2.16 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Ngoài các tệp blog posts và comments, WordPress còn lưu trữ loại dữ liệu nào trên đĩa, khiến việc sử dụng EFS trở nên cần thiết trong hạ tầng nhiều máy chủ?</p>{
	~[moodle]Thông tin đăng nhập của người quản trị AWS.#<p>Thông tin đăng nhập AWS không liên quan đến dữ liệu ứng dụng của WordPress.</p>
	~[moodle]Mã nguồn của hệ điều hành Amazon Linux.#<p>Mã nguồn hệ điều hành là một phần của AMI, không phải dữ liệu WordPress được lưu trữ trên EFS.</p>
	=[moodle]Các tệp hình ảnh được tải lên bởi tác giả, plugin và theme.
	~[moodle]Dữ liệu tạm thời của bộ cân bằng tải.#<p>Dữ liệu tạm thời của bộ cân bằng tải không được lưu trữ trên EFS theo cách này.</p>
	####<p><strong>Giải thích</strong>: WordPress cũng lưu trữ dữ liệu ngoài cơ sở dữ liệu trên đĩa. Ví dụ, nếu một tác giả tải lên một hình ảnh cho bài đăng trên blog của họ, tệp đó sẽ được lưu trữ trên đĩa. Điều tương tự cũng đúng khi bạn cài đặt plugin và theme với tư cách quản trị viên.</p>
}

// question: 2.17 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Các mục nào sau đây là yếu tố chính ảnh hưởng đến chi phí ước tính hàng tháng của hạ tầng WordPress trên AWS?</p>{
	~[moodle]Giá trị cổ phiếu hiện tại của Amazon và tỷ giá hối đoái toàn cầu.#<p>Các yếu tố này không trực tiếp ảnh hưởng đến chi phí sử dụng AWS của bạn.</p>
	=[moodle]Vùng địa lý bạn chọn cho các dịch vụ và lượng lưu trữ cần thiết trên EFS.
	~[moodle]Số lượng máy chủ vật lý được sở hữu bởi AWS.#<p>Chi phí dựa trên mức sử dụng dịch vụ, không phải số lượng máy chủ vật lý được AWS sở hữu.</p>
	~[moodle]Số lượng tài khoản người dùng IAM được tạo trong tài khoản AWS của bạn.#<p>Số lượng người dùng IAM không ảnh hưởng trực tiếp đến chi phí dịch vụ AWS.</p>
	####<p><strong>Giải thích</strong>: Các yếu tố ảnh hưởng đến chi phí ước tính hàng tháng bao gồm vùng địa lý bạn chọn cho các dịch vụ (ví dụ: N. Virginia), vì giá cả của một số dịch vụ khác nhau tùy theo vùng. Ngoài ra, lượng lưu trữ cần thiết trên EFS (cho các tệp tải lên, plugin và theme) cũng sẽ làm tăng chi phí.</p>
}

// question: 2.18 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi khởi tạo hạ tầng WordPress bằng CloudFormation, định dạng tệp nào được sử dụng để mô tả blueprint CloudFormation trong ví dụ?</p>{
	~[moodle]JSON.#<p>CloudFormation hỗ trợ cả JSON và YAML, nhưng ví dụ này sử dụng YAML.</p>
	~[moodle]XML.#<p>XML không phải là định dạng chính được CloudFormation sử dụng cho template.</p>
	=[moodle]YAML.
	~[moodle]Text (TXT).#<p>Template cần một định dạng có cấu trúc như YAML hoặc JSON.</p>
	####<p><strong>Giải thích</strong>: Để sử dụng template đã chuẩn bị cho chương này, bạn chọn "Specify an Amazon S3 template URL" và nhập URL của template, ví dụ: https://s3.amazonaws.com/awsinaction-code2/chapter02/template.yaml. .yaml là định dạng YAML.</p>
}

// question: 2.19 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi khám phá hạ tầng WordPress, tab "Monitoring" trên chi tiết máy ảo (EC2 instance) cung cấp thông tin gì?</p>{
	~[moodle]Lịch sử các bản cập nhật hệ điều hành đã được cài đặt.#<p>Lịch sử cập nhật hệ điều hành không được hiển thị trực tiếp ở đây.</p>
	=[moodle]Biểu đồ về việc sử dụng tài nguyên của máy ảo như CPU.
	~[moodle]Danh sách các tài khoản người dùng đã đăng nhập vào máy ảo.#<p>Danh sách người dùng đăng nhập không phải là chức năng của tab Monitoring này.</p>
	~[moodle]Thông tin về các ứng dụng được cài đặt trên máy ảo.#<p>Thông tin về ứng dụng cài đặt không được hiển thị trực tiếp trên tab Monitoring này.</p>
	####<p><strong>Giải thích</strong>: Chọn tab Monitoring trên chi tiết máy ảo để xem máy ảo của bạn được sử dụng như thế nào. Tab này hiển thị các chỉ số được AWS thu thập, ví dụ: biểu đồ sử dụng CPU, giúp bạn đánh giá hiệu suất của hạ tầng.</p>
}

// question: 2.20 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Sau khi hạ tầng WordPress được tạo hoàn tất (CREATE_COMPLETE), bạn tìm thấy URL để truy cập cài đặt WordPress mới của mình ở đâu trong CloudFormation Console?</p>{
	~[moodle]Trong tab "Events" của stack.#<p>Tab "Events" hiển thị lịch sử các sự kiện tạo tài nguyên của stack.</p>
	~[moodle]Trong tab "Resources" của stack.#<p>Tab "Resources" liệt kê các tài nguyên đã tạo ra bởi stack.</p>
	=[moodle]Trong tab "Outputs" của stack.
	~[moodle]Trong tab "Parameters" của stack.#<p>Tab "Parameters" hiển thị các tham số đầu vào khi tạo stack.</p>
	####<p><strong>Giải thích</strong>: Sau khi tất cả các tài nguyên cần thiết đã được tạo, trạng thái sẽ thay đổi thành CREATE_COMPLETE. Chọn stack WordPress và chuyển sang tab Outputs. Ở đó bạn sẽ tìm thấy URL để truy cập cài đặt WordPress của mình.</p>
}

// question: 2.21 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Dịch vụ nào của AWS đóng vai trò là web server để phục vụ các trang WordPress trong kiến trúc mẫu?</p>{
	~[moodle]Amazon S3.#<p>Amazon S3 được dùng để lưu trữ đối tượng và có thể host nội dung tĩnh, nhưng WordPress cần máy chủ ứng dụng (như Apache) để chạy PHP.</p>
	=[moodle]Apache trên các máy ảo EC2.
	~[moodle]Elastic Load Balancing (ELB).#<p>ELB là bộ cân bằng tải, phân phối lưu lượng truy cập đến các web server, chứ không phải là web server chính.</p>
	~[moodle]Amazon RDS.#<p>Amazon RDS cung cấp cơ sở dữ liệu MySQL, nơi WordPress lưu trữ dữ liệu, không phải là web server.</p>
	####<p><strong>Giải thích</strong>: Trong kiến trúc mẫu WordPress, Apache được sử dụng làm web server để phục vụ các trang WordPress, chạy trên các máy ảo EC2.</p>
}

// question: 2.22 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi tạo hạ tầng WordPress bằng CloudFormation, việc sử dụng thẻ (tags) như (system:wordpress) có mục đích gì?</p>{
	~[moodle]Để xác định loại hệ điều hành được cài đặt trên các máy ảo.#<p>Loại hệ điều hành được xác định bởi AMI khi khởi chạy máy ảo, không phải bởi tags.</p>
	=[moodle]Để giúp tổ chức các tài nguyên trên AWS và dễ dàng tìm thấy chúng sau này.
	~[moodle]Để tự động cấu hình các quy tắc bảo mật cho cơ sở dữ liệu.#<p>Các quy tắc bảo mật được cấu hình thông qua Security Groups.</p>
	~[moodle]Để kích hoạt tính năng sao lưu dữ liệu tự động cho tất cả các dịch vụ.#<p>Sao lưu dữ liệu tự động là một tính năng của các dịch vụ như RDS, không phải chức năng của tags.</p>
	####<p><strong>Giải thích</strong>: Thẻ (tags), bao gồm cặp khóa-giá trị như (system:wordpress), được sử dụng để tổ chức các tài nguyên trên AWS. Chúng giúp bạn dễ dàng phân biệt giữa các môi trường (test/production), gán trung tâm chi phí, hoặc đánh dấu các tài nguyên thuộc về một ứng dụng cụ thể.</p>
}

// question: 2.23 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Hạ tầng WordPress mẫu sử dụng bao nhiêu máy ảo (EC2 instances) để chạy các web server?</p>{
	~[moodle]Một máy ảo duy nhất.#<p>Các con số này không chính xác theo thông tin trong nguồn tài liệu về ví dụ WordPress.</p>
	=[moodle]Hai máy ảo.
	~[moodle]Ba máy ảo.#<p>Các con số này không chính xác theo thông tin trong nguồn tài liệu về ví dụ WordPress.</p>
	~[moodle]Bốn máy ảo.#<p>Các con số này không chính xác theo thông tin trong nguồn tài liệu về ví dụ WordPress.</p>
	####<p><strong>Giải thích</strong>: CloudFormation sẽ tự động tạo hai máy ảo (EC2 instances) chạy các web server để phục vụ WordPress trong hạ tầng mẫu. Điều này giúp cải thiện độ tin cậy và khả năng xử lý tải.</p>
}

// question: 2.24 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Theo ví dụ WordPress, Amazon RDS cung cấp khả năng nào cho cơ sở dữ liệu MySQL để đảm bảo tính sẵn sàng cao?</p>{
	~[moodle]Chỉ quản lý bản vá và cập nhật.#<p>RDS không chỉ quản lý bản vá, mà còn cả sao lưu và các tác vụ vận hành khác.</p>
	~[moodle]Chỉ cung cấp khả năng sao lưu thủ công.#<p>RDS cung cấp cả sao lưu tự động và khả năng tạo snapshot thủ công.</p>
	=[moodle]Khả năng sao chép (replication) và xử lý lỗi tự động (fail-over).
	~[moodle]Tự động tắt cơ sở dữ liệu khi không sử dụng để tiết kiệm chi phí.#<p>RDS là dịch vụ quản lý cơ sở dữ liệu, không tự động tắt cơ sở dữ liệu khi không sử dụng mà nó sẽ phát sinh chi phí.</p>
	####<p><strong>Giải thích</strong>: Amazon RDS có thể cung cấp một cơ sở dữ liệu MySQL có khả năng sẵn sàng cao thông qua khả năng sao chép (replication) và xử lý lỗi tự động (fail-over handling). Trong trường hợp instance cơ sở dữ liệu chính gặp lỗi, instance dự phòng sẽ được tự động nâng cấp thành instance chính mới.</p>
}

// question: 2.25 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Điều gì cần thiết để cài đặt và chạy WordPress trên các máy ảo EC2 trong hạ tầng mẫu?</p>{
	~[moodle]Chỉ cần tải xuống và giải nén WordPress.#<p>Chỉ tải xuống và giải nén là không đủ; cần có web server, PHP runtime và cấu hình cơ sở dữ liệu.</p>
	=[moodle]Cần cài đặt Apache và PHP, sau đó cấu hình WordPress để sử dụng cơ sở dữ liệu MySQL đã tạo.
	~[moodle]Chỉ cần cấu hình cơ sở dữ liệu MySQL đã tạo.#<p>Cấu hình cơ sở dữ liệu là một phần, nhưng không phải là tất cả các bước cần thiết để chạy WordPress.</p>
	~[moodle]Cần sử dụng một hệ điều hành độc quyền của AWS.#<p>Ví dụ sử dụng Amazon Linux (dựa trên Red Hat Enterprise Linux), không phải một hệ điều hành độc quyền.</p>
	####<p><strong>Giải thích</strong>: Để cài đặt và chạy WordPress trên các máy ảo EC2, cần thực hiện các bước như: cài đặt Apache và PHP, tải xuống và giải nén WordPress, cấu hình WordPress để sử dụng cơ sở dữ liệu MySQL đã tạo (RDS), và khởi động web server Apache.</p>
}

// question: 2.26 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi theo dõi trạng thái tạo hạ tầng WordPress trong CloudFormation Console, trạng thái nào cho biết quá trình đang diễn ra?</p>{
	~[moodle]CREATE_COMPLETE.#<p>CREATE_COMPLETE cho biết quá trình tạo đã hoàn tất thành công.</p>
	~[moodle]DELETE_COMPLETE.#<p>DELETE_COMPLETE cho biết quá trình xóa stack đã hoàn tất.</p>
	=[moodle]CREATE_IN_PROGRESS.
	~[moodle]UPDATE_COMPLETE.#<p>UPDATE_COMPLETE cho biết quá trình cập nhật stack đã hoàn tất thành công.</p>
	####<p><strong>Giải thích</strong>: Khi CloudFormation đang tạo các tài nguyên cần thiết cho WordPress, trạng thái sẽ là CREATE_IN_PROGRESS.</p>
}

// question: 2.27 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Trong phần chi tiết của một máy ảo EC2 thuộc hạ tầng WordPress, "AMI ID" cung cấp thông tin gì?</p>{
	~[moodle]Địa chỉ IP công khai của máy ảo.#<p>Địa chỉ IP công khai của máy ảo được hiển thị dưới mục "IPv4 Public IP".</p>
	~[moodle]Cấu hình tường lửa cho máy ảo.#<p>Cấu hình tường lửa được hiển thị dưới mục "Security groups".</p>
	=[moodle]Phiên bản hệ điều hành mà máy ảo dựa trên.
	~[moodle]Sức mạnh xử lý và bộ nhớ của máy ảo.#<p>Sức mạnh xử lý và bộ nhớ của máy ảo được xác định bởi "Instance type".</p>
	####<p><strong>Giải thích</strong>: AMI ID (Amazon Machine Image ID) trong chi tiết máy ảo cho biết phiên bản hệ điều hành mà máy ảo dựa trên, cùng với các phần mềm cài đặt sẵn.</p>
}

// question: 2.28 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Trong ví dụ WordPress, việc sử dụng ổ đĩa từ tính (magnetic disks) cho cơ sở dữ liệu MySQL thay vì SSD có lợi ích gì?</p>{
	~[moodle]Tăng hiệu suất I/O lên mức tối đa.#<p>SSD thường cung cấp hiệu suất I/O cao hơn so với ổ đĩa từ tính.</p>
	~[moodle]Cung cấp tính sẵn sàng cao hơn.#<p>Tính sẵn sàng cao của RDS được cung cấp thông qua cấu hình Multi-AZ, không phụ thuộc vào loại ổ đĩa.</p>
	=[moodle]Chi phí rẻ hơn và đủ cho một ứng dụng web với lưu lượng truy cập thấp.
	~[moodle]Tăng dung lượng lưu trữ lên mức không giới hạn.#<p>Dung lượng lưu trữ của RDS (cũng như EBS) có giới hạn, không phải không giới hạn.</p>
	####<p><strong>Giải thích</strong>: Trong ví dụ WordPress, việc sử dụng ổ đĩa từ tính (magnetic disks) cho cơ sở dữ liệu MySQL được chọn vì nó rẻ hơn và đủ dùng cho một ứng dụng web với khoảng 1.000 khách truy cập mỗi ngày, thể hiện sự tối ưu hóa chi phí cho một blog có lưu lượng truy cập thấp.</p>
}

// question: 2.29 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Nếu bạn muốn tăng cường hiệu suất của cơ sở dữ liệu RDS trong hạ tầng WordPress mẫu, tùy chọn nào là hiệu quả nhất?</p>{
	~[moodle]Thay đổi loại ổ đĩa từ từ tính sang SSD.#<p>Thay đổi loại ổ đĩa từ từ tính sang SSD cũng cải thiện hiệu suất, nhưng việc thay đổi instance class thường mang lại tác động lớn hơn đến sức mạnh xử lý tổng thể của cơ sở dữ liệu.</p>
	=[moodle]Thay đổi "instance class" của cơ sở dữ liệu lên một loại mạnh hơn.
	~[moodle]Kích hoạt tính năng sao lưu tự động.#<p>Kích hoạt tính năng sao lưu tự động (automated backups) đảm bảo an toàn dữ liệu, nhưng không trực tiếp tăng hiệu suất của cơ sở dữ liệu đang hoạt động.</p>
	~[moodle]Giảm số lượng máy ảo EC2 kết nối đến cơ sở dữ liệu.#<p>Giảm số lượng máy ảo kết nối đến cơ sở dữ liệu có thể giảm tải, nhưng không phải là cách trực tiếp để tăng cường sức mạnh của chính cơ sở dữ liệu.</p>
	####<p><strong>Giải thích</strong>: Để tăng cường hiệu suất của cơ sở dữ liệu RDS, bạn có thể thay đổi "instance class" của cơ sở dữ liệu (ví dụ: từ db.t2.micro lên một loại mạnh hơn), điều này sẽ tăng CPU và bộ nhớ cho cơ sở dữ liệu.</p>
}

// question: 2.30 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Khi khám phá hạ tầng WordPress, dịch vụ EFS được truy cập thông qua giao thức nào?</p>{
	~[moodle]HTTP.#<p>HTTP (Hypertext Transfer Protocol) thường được dùng cho các ứng dụng web.</p>
	~[moodle]FTP.#<p>FTP (File Transfer Protocol) là một giao thức truyền tệp cũ hơn, không phải giao thức chính được EFS sử dụng.</p>
	=[moodle]NFSv4.1.
	~[moodle]SMB.#<p>SMB (Server Message Block) thường được sử dụng cho chia sẻ tệp trên Windows, không phải EFS.</p>
	####<p><strong>Giải thích</strong>: EFS (Elastic File System) được sử dụng để lưu trữ các tệp và có thể truy cập thông qua giao thức NFSv4.1.</p>
}

// question: 2.31 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Điều nào sau đây là một trong những tác vụ mà AWS CloudFormation tự động thực hiện trong nền khi triển khai hạ tầng WordPress mẫu?</p>{
	~[moodle]Tạo tài khoản người dùng IAM mới cho mỗi tác giả WordPress.#<p>CloudFormation không tự động tạo tài khoản người dùng IAM cho tác giả WordPress trong ví dụ này.</p>
	=[moodle]Cài đặt hệ điều hành và phần mềm Apache, PHP trên các máy ảo EC2.
	~[moodle]Thiết lập dịch vụ email marketing cho blog WordPress.#<p>Thiết lập dịch vụ email marketing không phải là một phần của triển khai hạ tầng cơ bản WordPress bằng CloudFormation.</p>
	~[moodle]Tối ưu hóa SEO cho các bài đăng trên blog WordPress.#<p>Tối ưu hóa SEO là một tác vụ cấp ứng dụng, không phải là một phần của triển khai hạ tầng bằng CloudFormation.</p>
	####<p><strong>Giải thích</strong>: AWS CloudFormation tự động thực hiện nhiều tác vụ trong nền, bao gồm việc tạo các máy ảo (EC2), gắn EFS, và cài đặt Apache và PHP cũng như tải xuống và cấu hình WordPress trên các máy ảo đó.</p>
}

// question: 2.32 name: Chapter 2: A simple example: WordPress in five minutes
::Chapter 2\: A simple example: WordPress in five minutes::[html]<p>Mục đích của việc sử dụng Application Load Balancer (ALB) trong hạ tầng WordPress mẫu là gì?</p>{
	~[moodle]Để lưu trữ dữ liệu cơ sở dữ liệu.#<p>Dữ liệu cơ sở dữ liệu được lưu trữ trong RDS.</p>
	=[moodle]Để cân bằng tải lưu lượng HTTP/HTTPS đến các máy chủ web.
	~[moodle]Để quản lý quyền truy cập của người dùng.#<p>Quản lý quyền truy cập người dùng được thực hiện bởi IAM và Security Groups.</p>
	~[moodle]Để lưu trữ các tệp tĩnh của trang web.#<p>Các tệp tĩnh của trang web được lưu trữ trên EFS hoặc S3.</p>
	####<p><strong>Giải thích</strong>: Application Load Balancer (ALB) được sử dụng để cân bằng tải lưu lượng HTTP và HTTPS đến một nhóm các máy ảo (web server) chạy WordPress, đảm bảo tính sẵn sàng cao và phân phối đều các yêu cầu.</p>
}

// Chapter 3: Using virtual machines: EC2
// question: 3 name: Switch category to $module$/top/Chapter 3: Using virtual machines: EC2
$CATEGORY: $module$/top/Chapter 3: Using virtual machines: EC2

// question: 3.1 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Một máy ảo (VM) được định nghĩa là gì trong ngữ cảnh của AWS EC2?</p>{
	~[moodle]Một hệ điều hành đầy đủ chạy trên phần cứng vật lý chuyên dụng.#<p>Mặc dù VM chạy hệ điều hành, nó là một phần được ảo hóa, không phải luôn trên phần cứng chuyên dụng hoàn toàn.</p>
	=[moodle]Một phần của máy vật lý được cách ly bằng phần mềm khỏi các VM khác trên cùng một máy vật lý, bao gồm CPU, bộ nhớ, giao diện mạng và lưu trữ.
	~[moodle]Một ứng dụng phần mềm được đóng gói sẵn để triển khai nhanh chóng.#<p>Đây là mô tả của một ứng dụng, không phải bản thân một VM.</p>
	~[moodle]Một dịch vụ mạng cho phép kết nối các máy tính từ xa mà không cần cài đặt phần mềm.#<p>Đây là mô tả một dịch vụ mạng, không phải bản thân VM.</p>
	####<p><strong>Giải thích</strong>: Một máy ảo (VM) là một phần của máy vật lý được cách ly bằng phần mềm khỏi các VM khác trên cùng một máy vật lý; nó bao gồm CPU, bộ nhớ, giao diện mạng và lưu trữ. Máy vật lý được gọi là host machine, và các VM chạy trên đó là guests.</p>
}

// question: 3.2 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi khởi chạy một máy ảo trong AWS EC2, "Amazon Machine Image (AMI)" đại diện cho điều gì?</p>{
	~[moodle]Một khóa bảo mật để truy cập SSH vào máy ảo.#<p>Khóa SSH được tạo riêng biệt và chọn khi khởi chạy VM.</p>
	=[moodle]Hệ điều hành đi kèm với phần mềm đã được cài đặt sẵn cho máy ảo của bạn.
	~[moodle]Kích thước và cấu hình phần cứng của máy ảo.#<p>Kích thước và cấu hình phần cứng được xác định bởi "instance type".</p>
	~[moodle]Vùng địa lý nơi máy ảo sẽ được triển khai.#<p>Vùng địa lý là do người dùng chọn khi khởi chạy, không phải là AMI.</p>
	####<p><strong>Giải thích</strong>: AMI (Amazon Machine Image) là hệ điều hành đi kèm với phần mềm đã được cài đặt sẵn cho máy ảo của bạn.</p>
}

// question: 3.3 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Các "instance types" trong AWS EC2 phân loại điều gì chủ yếu?</p>{
	~[moodle]Số lượng người dùng có thể truy cập máy ảo cùng lúc.#<p>Không có thông tin này trong nguồn, và không phải là yếu tố chính của instance type.</p>
	=[moodle]Sức mạnh điện toán cần thiết cho máy ảo, bao gồm số lượng vCPU và dung lượng bộ nhớ.
	~[moodle]Phiên bản của hệ điều hành được cài đặt trên máy ảo.#<p>Phiên bản hệ điều hành được chọn thông qua AMI.</p>
	~[moodle]Loại kết nối mạng mà máy ảo sẽ sử dụng (ví dụ: Wi-Fi hoặc Ethernet).#<p>Loại kết nối mạng không được định nghĩa trực tiếp bởi instance type, mặc dù hiệu suất mạng có thể khác nhau giữa các loại instance.</p>
	####<p><strong>Giải thích</strong>: Sức mạnh điện toán được phân loại thành các loại instance. Một instance type chủ yếu mô tả số lượng CPU ảo và dung lượng bộ nhớ.</p>
}

// question: 3.4 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Mục đích của việc sử dụng "Tags" khi cấu hình máy ảo EC2 là gì?</p>{
	~[moodle]Để xác định địa chỉ IP công khai duy nhất cho máy ảo.#<p>Địa chỉ IP công khai là thuộc tính của máy ảo, không phải tag.</p>
	=[moodle]Để giúp bạn tổ chức các tài nguyên trên AWS, chẳng hạn như đặt tên cho máy ảo.
	~[moodle]Để tự động cài đặt các bản cập nhật phần mềm bảo mật.#<p>Cập nhật phần mềm là tác vụ vận hành, không phải chức năng của tag.</p>
	~[moodle]Để kích hoạt tính năng sao lưu dữ liệu tự động cho máy ảo.#<p>Sao lưu dữ liệu là chức năng của các dịch vụ lưu trữ hoặc các công cụ sao lưu cụ thể.</p>
	####<p><strong>Giải thích</strong>: Thẻ (Tags) giúp bạn tổ chức các tài nguyên trên AWS. Mỗi thẻ chỉ là một cặp khóa-giá trị, ví dụ: để đặt tên cho máy ảo hoặc phân loại tài nguyên.</p>
}

// question: 3.5 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi khởi chạy máy ảo Linux, bạn sử dụng giao thức nào để kết nối từ xa và đăng nhập vào máy ảo?</p>{
	~[moodle]HTTP (Hypertext Transfer Protocol).#<p>HTTP dùng cho các trang web.</p>
	~[moodle]FTP (File Transfer Protocol).#<p>FTP dùng để truyền tệp.</p>
	=[moodle]SSH (Secure Shell Protocol).
	~[moodle]SMTP (Simple Mail Transfer Protocol).#<p>SMTP dùng để gửi email.</p>
	####<p><strong>Giải thích</strong>: Để truy cập máy Linux, bạn sử dụng giao thức SSH (Secure Shell Protocol); bạn sẽ sử dụng một key pair để xác thực thay vì mật khẩu trong quá trình đăng nhập.</p>
}

// question: 3.6 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Sự khác biệt cơ bản giữa việc "Stop" (dừng) và "Terminate" (chấm dứt) một máy ảo EC2 là gì?</p>{
	~[moodle]Dừng một máy ảo xóa tất cả dữ liệu, trong khi chấm dứt bảo toàn dữ liệu.#<p>Dừng máy ảo sẽ giữ lại các tài nguyên gắn kèm như lưu trữ EBS, dữ liệu sẽ không bị mất.</p>
	=[moodle]Dừng một máy ảo cho phép bạn khởi động lại nó sau này, trong khi chấm dứt máy ảo sẽ xóa nó vĩnh viễn.
	~[moodle]Chấm dứt máy ảo tính phí cho các tài nguyên gắn kèm, trong khi dừng thì không.#<p>Cả dừng và chấm dứt đều có thể phát sinh chi phí cho các tài nguyên gắn kèm (ví dụ: EBS) nếu chúng không được xóa riêng.</p>
	~[moodle]Dừng là một hành động vĩnh viễn, trong khi chấm dứt là tạm thời.#<p>Dừng là tạm thời, chấm dứt là vĩnh viễn.</p>
	####<p><strong>Giải thích</strong>: Sự khác biệt giữa việc dừng và chấm dứt một máy ảo là quan trọng. Bạn có thể khởi động lại một máy ảo đã dừng. Điều này không thể thực hiện được với một máy ảo đã chấm dứt, vì nếu bạn chấm dứt một máy ảo, bạn sẽ xóa nó vĩnh viễn.</p>
}

// question: 3.7 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi bạn cần tăng sức mạnh xử lý (CPU), bộ nhớ hoặc khả năng mạng cho máy ảo EC2, bạn có thể thực hiện hành động nào sau đây?</p>{
	~[moodle]Tạo một máy ảo hoàn toàn mới với cấu hình mong muốn.#<p>Việc này có thể thực hiện nhưng việc thay đổi instance type là một cách hiệu quả hơn để thay đổi tài nguyên mà không cần cấu hình lại từ đầu.</p>
	=[moodle]Thay đổi "instance type" của máy ảo hiện có sau khi dừng nó.
	~[moodle]Cập nhật hệ điều hành của máy ảo để mở khóa hiệu suất cao hơn.#<p>Cập nhật hệ điều hành không làm thay đổi trực tiếp cấu hình phần cứng ảo (CPU, bộ nhớ).</p>
	~[moodle]Sử dụng một "Elastic IP" để tự động nâng cấp tài nguyên.#<p>Elastic IP là địa chỉ IP công cộng cố định, không liên quan đến việc nâng cấp tài nguyên VM.</p>
	####<p><strong>Giải thích</strong>: Nếu bạn cần thêm CPU, bộ nhớ hoặc khả năng mạng, bạn có thể thay đổi instance type của máy ảo hiện có. Bạn cần dừng máy ảo trước khi thực hiện thay đổi này.</p>
}

// question: 3.8 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Tại sao AWS lại nhóm các trung tâm dữ liệu của mình thành các "regions" độc lập trên toàn thế giới?</p>{
	~[moodle]Để tối đa hóa việc chia sẻ tài nguyên giữa các khu vực địa lý khác nhau.#<p>Các regions độc lập với nhau và dữ liệu không được chuyển giữa các regions theo mặc định, nên việc chia sẻ tài nguyên trực tiếp giữa các regions không phải mục tiêu chính.</p>
	=[moodle]Để cung cấp khả năng xây dựng hạ tầng có độ sẵn sàng cao và phục vụ khách hàng trên toàn cầu với độ trễ thấp hơn.
	~[moodle]Để đơn giản hóa việc quản lý chỉ một trung tâm dữ liệu duy nhất cho mỗi khách hàng.#<p>Việc này làm phức tạp hóa quản lý hơn do có nhiều regions để lựa chọn.</p>
	~[moodle]Để hạn chế sự phát triển của các dịch vụ đám mây chỉ ở một số quốc gia.#<p>Việc này nhằm mở rộng dịch vụ ra nhiều quốc gia, không phải hạn chế.</p>
	####<p><strong>Giải thích</strong>: AWS nhóm các trung tâm dữ liệu thành các "regions" độc lập để cung cấp khả năng xây dựng hạ tầng có độ sẵn sàng cao và phục vụ khách hàng trên toàn cầu với độ trễ thấp hơn. Các regions được kết nối tốt với nhau.</p>
}

// question: 3.9 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Dịch vụ nào của AWS cho phép bạn cấp phát một địa chỉ IP công khai cố định và liên kết nó với một phiên bản EC2, để địa chỉ IP không thay đổi khi bạn dừng và khởi động lại máy ảo?</p>{
	~[moodle]Amazon S3.#<p>S3 là dịch vụ lưu trữ đối tượng.</p>
	~[moodle]Amazon Virtual Private Cloud (VPC).#<p>VPC là mạng riêng ảo trong đám mây, giúp định nghĩa cấu trúc mạng.</p>
	=[moodle]Elastic IP Address (EIP).
	~[moodle]Amazon Route 53.#<p>Route 53 là dịch vụ DNS, quản lý tên miền và định tuyến truy cập.</p>
	####<p><strong>Giải thích</strong>: Elastic IP Address (EIP) là dịch vụ của AWS để cấp phát một địa chỉ IP công khai cố định và liên kết nó với một phiên bản EC2. Điều này giải quyết vấn đề địa chỉ IP công khai thay đổi mỗi khi máy ảo được khởi chạy hoặc dừng.</p>
}

// question: 3.10 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi tối ưu hóa chi phí cho các máy ảo, loại instance nào yêu cầu bạn cam kết sử dụng một VM cụ thể trong một trung tâm dữ liệu cụ thể trong một khoảng thời gian (1 hoặc 3 năm) để đổi lấy giảm giá đáng kể?</p>{
	~[moodle]On-demand Instances.#<p>On-demand Instances là các VM bạn trả tiền theo giây, không cần cam kết sử dụng.</p>
	~[moodle]Spot Instances.#<p>Spot Instances cho phép bạn đặt giá thầu cho dung lượng chưa sử dụng và có thể bị chấm dứt nếu giá thầu bị vượt quá.</p>
	=[moodle]Reserved Instances.
	~[moodle]Dedicated Hosts.#<p>Dedicated Hosts không được đề cập trong bảng so sánh chính về tối ưu hóa chi phí instance.</p>
	####<p><strong>Giải thích</strong>: Reserved Instances là loại instance yêu cầu bạn cam kết sử dụng một VM cụ thể trong một trung tâm dữ liệu cụ thể trong một khoảng thời gian (1 hoặc 3 năm), đổi lại bạn sẽ được giảm giá đáng kể lên đến 60%. Bạn phải trả tiền cho một Reserved VM dù nó có đang chạy hay không.</p>
}

// question: 3.11 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Trong các tùy chọn tối ưu hóa chi phí của máy ảo, "Spot Instances" phù hợp nhất cho các loại tác vụ nào?</p>{
	~[moodle]Các ứng dụng kinh doanh quan trọng yêu cầu thời gian hoạt động 24/7.#<p>Spot Instances có thể bị chấm dứt bởi AWS, không phù hợp cho các ứng dụng kinh doanh quan trọng yêu cầu thời gian hoạt động liên tục.</p>
	=[moodle]Các khối lượng công việc có thể chịu được sự gián đoạn, như phân tích dữ liệu hoặc mã hóa phương tiện.
	~[moodle]Các máy chủ web và email yêu cầu địa chỉ IP cố định.#<p>Spot Instances không đảm bảo địa chỉ IP cố định và dễ bị chấm dứt, không phù hợp cho máy chủ web hoặc email.</p>
	~[moodle]Các cơ sở dữ liệu quan hệ yêu cầu hiệu suất I/O liên tục cao.#<p>Hiệu suất của Spot Instances có thể không ổn định do bản chất của thị trường, không lý tưởng cho các cơ sở dữ liệu đòi hỏi hiệu suất I/O cao liên tục.</p>
	####<p><strong>Giải thích</strong>: Spot Instances phù hợp nhất cho các khối lượng công việc có thể chịu được sự gián đoạn, như phân tích dữ liệu hoặc mã hóa phương tiện, vì AWS có thể chấm dứt các instance này nếu giá thị trường vượt quá giá đặt thầu của bạn.</p>
}

// question: 3.12 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi bạn kiểm tra log của một máy ảo, bạn sẽ tìm thấy thông tin nào sau đây?</p>{
	~[moodle]Lịch sử thay đổi cấu hình phần cứng của máy ảo.#<p>Log hệ thống không ghi lại lịch sử thay đổi cấu hình phần cứng ảo.</p>
	=[moodle]Các tin nhắn và sự kiện được ghi lại từ hệ điều hành và các ứng dụng đang chạy trên máy ảo.
	~[moodle]Dữ liệu thanh toán chi tiết cho mỗi phút hoạt động của máy ảo.#<p>Dữ liệu thanh toán được tìm thấy trong Billing Dashboard, không phải trong log của máy ảo.</p>
	~[moodle]Thông tin về tất cả các tài khoản AWS được liên kết với máy ảo.#<p>Thông tin tài khoản AWS được quản lý bởi IAM và các dịch vụ khác, không phải là nội dung chính của log máy ảo.</p>
	####<p><strong>Giải thích</strong>: Việc xem log của máy ảo giúp bạn truy cập các tin nhắn log hệ thống mà không cần kết nối SSH, bao gồm các tin nhắn và sự kiện được ghi lại từ hệ điều hành và các ứng dụng đang chạy trên máy ảo.</p>
}

// question: 3.13 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>EC2 Instance Store cung cấp loại lưu trữ khối (block-level storage) nào?</p>{
	~[moodle]Lưu trữ cấp khối cố định được gắn qua mạng và độc lập với máy ảo.#<p>Đây là mô tả của Elastic Block Store (EBS), là lưu trữ cấp khối được gắn qua mạng và độc lập với máy ảo.</p>
	=[moodle]Lưu trữ cấp khối tạm thời được gắn trực tiếp vào máy chủ vật lý của VM và sẽ bị xóa khi máy ảo dừng hoặc chấm dứt.
	~[moodle]Lưu trữ đối tượng được truy cập qua API HTTP(S).#<p>Đây là mô tả của Amazon S3, là dịch vụ lưu trữ đối tượng.</p>
	~[moodle]Hệ thống tệp mạng được chia sẻ giữa nhiều máy ảo.#<p>Đây là mô tả của Elastic File System (EFS), là một hệ thống tệp mạng được chia sẻ giữa nhiều máy ảo.</p>
	####<p><strong>Giải thích</strong>: Instance Store cung cấp lưu trữ cấp khối tạm thời được gắn trực tiếp vào máy chủ vật lý của VM. Nó chỉ khả dụng khi instance đang chạy và sẽ không duy trì dữ liệu nếu bạn dừng hoặc chấm dứt instance.</p>
}

// question: 3.14 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi kiểm tra hiệu suất của một ổ đĩa trong máy ảo Linux, công cụ dòng lệnh dd được sử dụng với mục đích gì?</p>{
	~[moodle]Để định dạng lại ổ đĩa và tạo một hệ thống tệp mới.#<p>Lệnh mkfs được dùng để tạo hệ thống tệp.</p>
	=[moodle]Để thực hiện các bài kiểm tra đọc và ghi cấp khối giữa một nguồn và một đích.
	~[moodle]Để sao chép toàn bộ hệ điều hành từ ổ đĩa này sang ổ đĩa khác.#<p>dd có thể làm điều này nhưng mục đích chính trong ngữ cảnh kiểm tra hiệu suất là đo lường I/O.</p>
	~[moodle]Để phân vùng lại ổ đĩa và thay đổi kích thước các phân vùng.#<p>Lệnh fdisk hoặc parted được dùng để phân vùng ổ đĩa.</p>
	####<p><strong>Giải thích</strong>: Để kiểm tra hiệu suất của các ổ đĩa của bạn (bao gồm EBS và Instance Store), bạn sẽ sử dụng công cụ đơn giản có tên dd, có thể thực hiện các thao tác đọc và ghi cấp khối giữa một nguồn và một đích.</p>
}

// question: 3.15 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Loại instance t2.micro trong AWS EC2 có đặc điểm hiệu suất CPU như thế nào?</p>{
	~[moodle]Hiệu suất CPU cơ bản cao, ổn định liên tục cho các ứng dụng chuyên sâu.#<p>Đây là đặc điểm của các instance family C (Compute optimized).</p>
	=[moodle]Hiệu suất CPU cơ bản vừa phải với khả năng tăng tốc độ xử lý lên cao hơn trong thời gian ngắn (burstable performance).
	~[moodle]Hiệu suất CPU được tối ưu hóa cho các tác vụ tính toán song song quy mô lớn.#<p>Các instance family P, G, và CG được tối ưu hóa cho tính toán tăng tốc.</p>
	~[moodle]Không có khả năng sử dụng CPU, chỉ dùng cho lưu trữ dữ liệu.#<p>Mọi instance type đều có CPU để thực hiện các tác vụ tính toán.</p>
	####<p><strong>Giải thích</strong>: Instance family t (ví dụ t2.micro) nhóm các máy ảo nhỏ, rẻ tiền với hiệu suất CPU cơ bản thấp nhưng có khả năng tăng tốc độ xử lý đáng kể (burstable performance) so với hiệu suất CPU cơ bản trong thời gian ngắn. t2.micro cũng thường đủ điều kiện cho Free Tier.</p>
}

// question: 3.16 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Đâu là một trong những tiêu chí cần xem xét khi quyết định chọn "region" (vùng) cho hạ tầng đám mây của bạn?</p>{
	~[moodle]Tên của người tạo tài khoản AWS đầu tiên.#<p>Các tùy chọn này không phải là tiêu chí kỹ thuật hoặc kinh doanh để chọn vùng.</p>
	=[moodle]Vị trí địa lý của khách hàng mục tiêu để giảm độ trễ.
	~[moodle]Màu sắc yêu thích của biểu tượng dịch vụ AWS.#<p>Các tùy chọn này không phải là tiêu chí kỹ thuật hoặc kinh doanh để chọn vùng.</p>
	~[moodle]Ngôn ngữ lập trình được sử dụng nhiều nhất trong đội ngũ của bạn.#<p>Các tùy chọn này không phải là tiêu chí kỹ thuật hoặc kinh doanh để chọn vùng.</p>
	####<p><strong>Giải thích</strong>: Khi quyết định chọn vùng cho hạ tầng đám mây của bạn, bạn cần tính đến các tiêu chí như vị trí địa lý của khách hàng để giảm độ trễ mạng (latency).</p>
}

// question: 3.17 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Các instance EC2 chạy Linux (như Amazon Linux hoặc Ubuntu) thường được tính phí theo đơn vị nào?</p>{
	~[moodle]Mỗi giờ hoạt động.#<p>Đây là các đơn vị tính phí phổ biến khác nhưng không phải mặc định cho Linux EC2.</p>
	~[moodle]Mỗi ngày hoạt động.#<p>Đây là các đơn vị tính phí phổ biến khác nhưng không phải mặc định cho Linux EC2.</p>
	=[moodle]Mỗi giây hoạt động, với mức tối thiểu 60 giây.
	~[moodle]Mỗi gigabyte dữ liệu được xử lý.#<p>Tính phí theo dữ liệu xử lý thường áp dụng cho lưu trữ hoặc truyền dữ liệu, không phải thời gian chạy VM.</p>
	####<p><strong>Giải thích</strong>: Hầu hết các instance EC2 chạy Linux (như Amazon Linux hoặc Ubuntu) được tính phí theo giây. Mức phí tối thiểu cho mỗi instance là 60 giây.</p>
}

// question: 3.18 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Tại sao việc tạo một bản sao lưu (snapshot) của một ổ đĩa EBS đang được gắn và sử dụng có thể gây ra vấn đề?</p>{
	~[moodle]Bởi vì bản sao lưu sẽ bị hỏng ngay lập tức và không thể phục hồi.#<p>Bản sao lưu có thể không bị hỏng hoàn toàn nhưng có thể không nhất quán, không phải hỏng ngay lập tức.</p>
	=[moodle]Nó có thể gây ra vấn đề với các thao tác ghi chưa được ghi vào đĩa, dẫn đến dữ liệu không nhất quán.
	~[moodle]AWS sẽ tự động ngừng máy ảo để tạo bản sao lưu, gây gián đoạn dịch vụ.#<p>AWS không tự động ngừng máy ảo khi tạo snapshot EBS.</p>
	~[moodle]Việc này không thể thực hiện được do các hạn chế kỹ thuật.#<p>Việc này có thể thực hiện nhưng có rủi ro về tính nhất quán dữ liệu.</p>
	####<p><strong>Giải thích</strong>: Tạo một bản sao lưu của một ổ đĩa đã gắn và đang sử dụng là có thể, nhưng có thể gây ra vấn đề với các thao tác ghi chưa được ghi vào đĩa, dẫn đến dữ liệu không nhất quán trong snapshot.</p>
}

// question: 3.19 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi bạn thêm một Network Interface (Giao diện mạng) phụ vào máy ảo EC2, mỗi giao diện mạng sẽ được kết nối với loại địa chỉ IP nào?</p>{
	~[moodle]Chỉ một địa chỉ IP công khai duy nhất.#<p>Mỗi giao diện có cả IP công khai và riêng.</p>
	~[moodle]Chỉ một địa chỉ IP riêng duy nhất.#<p>Mỗi giao diện có cả IP công khai và riêng.</p>
	=[moodle]Một địa chỉ IP riêng và một địa chỉ IP công khai.
	~[moodle]Một địa chỉ MAC duy nhất.#<p>Địa chỉ MAC là địa chỉ vật lý của giao diện mạng, không phải địa chỉ IP.</p>
	####<p><strong>Giải thích</strong>: Mỗi giao diện mạng (Network Interface) phụ được kết nối với một địa chỉ IP riêng và một địa chỉ IP công khai.</p>
}

// question: 3.20 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Việc triển khai OpenSwan, một máy chủ VPN, lên một máy ảo EC2 trong chương này được thực hiện như thế nào?</p>{
	~[moodle]Cài đặt thủ công từng thành phần thông qua giao diện người dùng đồ họa.#<p>Việc này được tự động hóa thông qua tập lệnh shell, không phải cài đặt thủ công.</p>
	=[moodle]Sử dụng AWS CloudFormation để khởi chạy máy ảo với dữ liệu người dùng (user data) chứa một tập lệnh shell.
	~[moodle]Triển khai OpenSwan thông qua AWS Elastic Beanstalk.#<p>Elastic Beanstalk được thiết kế để triển khai ứng dụng web phổ biến, không phải dịch vụ VPN cụ thể.</p>
	~[moodle]Sử dụng AWS OpsWorks Stacks để quản lý cấu hình.#<p>OpsWorks Stacks là để triển khai ứng dụng nhiều lớp, mặc dù có thể tùy chỉnh nhưng trong ví dụ này CloudFormation và user data được ưu tiên.</p>
	####<p><strong>Giải thích</strong>: Trong chương này, OpenSwan (máy chủ VPN) được triển khai lên máy ảo EC2 bằng cách sử dụng AWS CloudFormation để khởi chạy máy ảo với dữ liệu người dùng (user data) chứa một tập lệnh shell. Tập lệnh này sẽ cài đặt và cấu hình OpenSwan trong quá trình bootstrapping.</p>
}

// question: 3.21 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>"Hypervisor" trong kiến trúc máy ảo (VM) có vai trò gì?</p>{
	~[moodle]Cung cấp bộ nhớ RAM vật lý cho các máy ảo.#<p>Hypervisor quản lý và phân bổ bộ nhớ vật lý, nhưng không trực tiếp cung cấp RAM vật lý theo nghĩa là nguồn tài nguyên.</p>
	=[moodle]Cách ly các VM khỏi nhau và lên lịch yêu cầu tới phần cứng vật lý.
	~[moodle]Cài đặt hệ điều hành trên máy ảo.#<p>Hệ điều hành được cài đặt bên trong máy ảo, không phải bởi hypervisor.</p>
	~[moodle]Đóng gói các ứng dụng phần mềm để triển khai nhanh chóng.#<p>Đóng gói ứng dụng phần mềm là chức năng của AMI hoặc các công cụ triển khai.</p>
	####<p><strong>Giải thích</strong>: Trong kiến trúc máy ảo, Hypervisor chịu trách nhiệm cách ly các VM khỏi nhau và lên lịch các yêu cầu truy cập phần cứng bằng cách cung cấp một nền tảng phần cứng ảo cho hệ thống khách (guest system).</p>
}

// question: 3.22 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi khởi chạy một máy ảo EC2, đâu là lý do nên chọn Amazon Linux AMI?</p>{
	~[moodle]Nó tương thích duy nhất với các instance type dòng T.#<p>Amazon Linux AMI tương thích với nhiều instance type, không chỉ dòng T.</p>
	~[moodle]Nó là hệ điều hành duy nhất được AWS hỗ trợ.#<p>AWS hỗ trợ nhiều hệ điều hành khác như Ubuntu, Microsoft Windows Server.</p>
	=[moodle]Nó dựa trên Red Hat Enterprise Linux và được tối ưu hóa cho EC2.
	~[moodle]Nó là hệ điều hành thương mại phải trả phí.#<p>Amazon Linux AMI thường được cung cấp miễn phí khi sử dụng EC2.</p>
	####<p><strong>Giải thích</strong>: Amazon Linux AMI được AWS cung cấp, dựa trên Red Hat Enterprise Linux và được tối ưu hóa đặc biệt để sử dụng với EC2. AWS cũng tự duy trì và tối ưu hóa nó.</p>
}

// question: 3.23 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi điều chỉnh kích thước máy ảo EC2, nếu bạn cần nhiều CPU, bộ nhớ hoặc khả năng mạng hơn, bạn nên làm gì?</p>{
	~[moodle]Luôn tạo một máy ảo hoàn toàn mới với cấu hình lớn hơn.#<p>Tạo một máy ảo mới là một lựa chọn, nhưng thay đổi instance type của máy ảo hiện có là một phương pháp hiệu quả hơn để điều chỉnh tài nguyên.</p>
	=[moodle]Thay đổi "instance type" của máy ảo hiện có sau khi đã dừng nó.
	~[moodle]Chỉ cần khởi động lại máy ảo hiện có.#<p>Khởi động lại máy ảo sẽ không thay đổi instance type hoặc tài nguyên vật lý ảo của nó.</p>
	~[moodle]Cài đặt thêm phần mềm tối ưu hóa hiệu suất trên máy ảo.#<p>Cài đặt phần mềm tối ưu hóa có thể cải thiện hiệu suất ứng dụng nhưng không làm tăng tài nguyên CPU, bộ nhớ hay mạng cơ bản của máy ảo.</p>
	####<p><strong>Giải thích</strong>: Nếu bạn cần nhiều CPU, bộ nhớ hoặc khả năng mạng hơn, bạn có thể thay đổi "instance type" của máy ảo hiện có. Hành động này yêu cầu bạn phải dừng máy ảo trước.</p>
}

// question: 3.24 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Một trong những tiêu chí để chọn một "region" cho hạ tầng đám mây của bạn là "Compliance" (Tuân thủ). Điều này có nghĩa là gì?</p>{
	~[moodle]Vùng đó phải có nhiều trung tâm dữ liệu nhất.#<p>Số lượng trung tâm dữ liệu liên quan đến tính sẵn sàng cao, không phải trực tiếp đến tuân thủ.</p>
	~[moodle]Vùng đó phải có chi phí thấp nhất.#<p>Chi phí là một tiêu chí riêng biệt.</p>
	=[moodle]Bạn được phép lưu trữ và xử lý dữ liệu ở quốc gia hoặc khu vực đó theo quy định.
	~[moodle]Vùng đó phải hỗ trợ tất cả các dịch vụ AWS.#<p>Không phải tất cả các dịch vụ AWS đều có sẵn ở mọi vùng, đây là tiêu chí "Service availability".</p>
	####<p><strong>Giải thích</strong>: Tiêu chí "Compliance" khi chọn một "region" có nghĩa là bạn cần xem xét liệu bạn có được phép lưu trữ và xử lý dữ liệu ở quốc gia hoặc khu vực đó hay không, dựa trên các quy định pháp luật và chính sách của công ty.</p>
}

// question: 3.25 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Đâu là một trường hợp sử dụng điển hình của máy ảo (VM) trong AWS EC2?</p>{
	~[moodle]Quản lý tài khoản người dùng và quyền truy cập.#<p>Quản lý tài khoản người dùng và quyền truy cập được thực hiện bởi AWS IAM.</p>
	=[moodle]Hosting một ứng dụng web như WordPress.
	~[moodle]Tạo bản sao lưu tự động cho cơ sở dữ liệu.#<p>Tạo bản sao lưu tự động cho cơ sở dữ liệu là chức năng của các dịch vụ như Amazon RDS.</p>
	~[moodle]Phát triển ngôn ngữ lập trình mới.#<p>Phát triển ngôn ngữ lập trình mới không phải là trường hợp sử dụng chính của máy ảo EC2.</p>
	####<p><strong>Giải thích</strong>: Một trong những trường hợp sử dụng điển hình của máy ảo (VM) trong AWS EC2 là hosting một ứng dụng web như WordPress. Các trường hợp khác bao gồm vận hành ứng dụng doanh nghiệp hoặc chuyển đổi/phân tích dữ liệu.</p>
}

// question: 3.26 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>"Virtual appliance" trong ngữ cảnh ảo hóa được định nghĩa như thế nào?</p>{
	~[moodle]Một dịch vụ mạng cho phép kết nối máy ảo.#<p>Đây là một dịch vụ mạng, không phải virtual appliance.</p>
	=[moodle]Một hình ảnh máy ảo chứa hệ điều hành và phần mềm được cấu hình sẵn.
	~[moodle]Một công cụ giám sát hiệu suất cho máy ảo.#<p>Công cụ giám sát hiệu suất là CloudWatch.</p>
	~[moodle]Một dịch vụ lưu trữ tạm thời cho máy ảo.#<p>Dịch vụ lưu trữ tạm thời là Instance Store.</p>
	####<p><strong>Giải thích</strong>: Một virtual appliance là một hình ảnh của máy ảo chứa hệ điều hành và phần mềm đã được cấu hình sẵn. AMI là một loại đặc biệt của virtual appliance được sử dụng với dịch vụ EC2.</p>
}

// question: 3.27 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Trong số các Instance family của EC2, dòng "M family" có đặc điểm chính là gì?</p>{
	~[moodle]Cung cấp hiệu suất CPU cơ bản thấp nhưng có khả năng burst cao.#<p>Đây là đặc điểm của dòng T family.</p>
	=[moodle]Mục đích tổng quát (General purpose), với tỷ lệ CPU và bộ nhớ cân bằng.
	~[moodle]Được tối ưu hóa cho các ứng dụng yêu cầu nhiều bộ nhớ.#<p>Dòng R family được tối ưu hóa cho bộ nhớ.</p>
	~[moodle]Được tối ưu hóa cho các tác vụ tính toán chuyên sâu.#<p>Dòng C family được tối ưu hóa cho tính toán.</p>
	####<p><strong>Giải thích</strong>: Dòng M family được mô tả là mục đích tổng quát (General purpose), với tỷ lệ CPU và bộ nhớ cân bằng, phù hợp cho nhiều loại ứng dụng khác nhau.</p>
}

// question: 3.28 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi bạn nhận thấy ứng dụng của mình trên máy ảo EC2 đang gặp vấn đề về hiệu suất và bạn nghi ngờ do CPU hoặc bộ nhớ, bạn nên kiểm tra ở đâu trong AWS Management Console?</p>{
	~[moodle]Tab "Storage" trên chi tiết máy ảo.#<p>Tab "Storage" cung cấp thông tin về các ổ đĩa được gắn.</p>
	~[moodle]Tab "Networking" trên chi tiết máy ảo.#<p>Tab "Networking" cung cấp thông tin về cấu hình mạng.</p>
	=[moodle]Tab "Monitoring" trên chi tiết máy ảo.
	~[moodle]Tab "Tags" trên chi tiết máy ảo.#<p>Tab "Tags" dùng để quản lý các thẻ metadata.</p>
	####<p><strong>Giải thích</strong>: Để kiểm tra hiệu suất của máy ảo liên quan đến CPU, bộ nhớ hoặc khả năng mạng, bạn nên chọn tab "Monitoring" trên chi tiết máy ảo (EC2 instance). Tab này hiển thị các biểu đồ về việc sử dụng tài nguyên của máy ảo.</p>
}

// question: 3.29 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Định nghĩa "Virtual Private Cloud (VPC)" trong AWS là gì?</p>{
	~[moodle]Một dịch vụ lưu trữ đối tượng cho dữ liệu không cấu trúc.#<p>Đây là mô tả của Amazon S3.</p>
	=[moodle]Một mạng riêng ảo của riêng bạn trong đám mây AWS.
	~[moodle]Một dịch vụ cân bằng tải cho lưu lượng HTTP/HTTPS.#<p>Đây là mô tả của Elastic Load Balancing (ELB).</p>
	~[moodle]Một dịch vụ quản lý cơ sở dữ liệu quan hệ được quản lý.#<p>Đây là mô tả của Amazon Relational Database Service (RDS).</p>
	####<p><strong>Giải thích</strong>: VPC (Virtual Private Cloud) là mạng riêng ảo của riêng bạn trong đám mây AWS. Nó cho phép bạn định nghĩa cấu trúc mạng của riêng mình với các dải địa chỉ IP, subnet, bảng định tuyến và ACL.</p>
}

// question: 3.30 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Khi tạo một "Security Group" cho máy ảo EC2, bạn có thể kiểm soát lưu lượng mạng dựa trên những yếu tố nào?</p>{
	=[moodle]Hướng (inbound hoặc outbound), giao thức IP, cổng, nguồn/đích dựa trên địa chỉ IP hoặc Security Group.
	~[moodle]Chỉ có thể kiểm soát lưu lượng đến (inbound).#<p>Security Groups có thể kiểm soát cả lưu lượng đến và đi.</p>
	~[moodle]Chỉ có thể kiểm soát lưu lượng dựa trên tên người dùng.#<p>Kiểm soát lưu lượng dựa trên tên người dùng không phải là chức năng trực tiếp của Security Group.</p>
	~[moodle]Chỉ có thể kiểm soát lưu lượng cho các ứng dụng web.#<p>Security Groups có thể kiểm soát lưu lượng cho bất kỳ loại ứng dụng hoặc dịch vụ nào, không giới hạn ở ứng dụng web.</p>
	####<p><strong>Giải thích</strong>: Một Security Group bao gồm một tập hợp các quy tắc cho phép lưu lượng mạng dựa trên các yếu tố như hướng (inbound hoặc outbound), giao thức IP (TCP, UDP, ICMP), cổng và nguồn/đích (dựa trên địa chỉ IP, dải địa chỉ IP hoặc Security Group khác).</p>
}

// question: 3.31 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Điều gì xảy ra với dữ liệu trên EC2 Instance Store nếu máy ảo được dừng hoặc chấm dứt?</p>{
	~[moodle]Dữ liệu được tự động sao lưu lên S3.#<p>Không có cơ chế sao lưu tự động tích hợp cho Instance Store lên S3; bạn phải tự cấu hình.</p>
	~[moodle]Dữ liệu được chuyển sang một ổ đĩa EBS mới.#<p>Dữ liệu không được tự động chuyển sang ổ đĩa EBS; Instance Store và EBS là hai loại lưu trữ khác nhau.</p>
	=[moodle]Dữ liệu sẽ bị mất vĩnh viễn.
	~[moodle]Dữ liệu vẫn được giữ nguyên và có thể truy cập khi máy ảo khởi động lại.#<p>Dữ liệu không được giữ nguyên; nó chỉ khả dụng khi instance đang chạy.</p>
	####<p><strong>Giải thích</strong>: EC2 Instance Store cung cấp lưu trữ cấp khối tạm thời; nó sẽ không duy trì dữ liệu của bạn nếu bạn dừng hoặc chấm dứt instance, điều này có nghĩa là dữ liệu sẽ bị mất vĩnh viễn.</p>
}

// question: 3.32 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Mục đích của "Hypervisor" trong kiến trúc máy ảo là gì?</p>{
	~[moodle]Cung cấp bộ nhớ vật lý cho máy ảo.#<p>Hypervisor quản lý việc phân bổ bộ nhớ vật lý, nhưng không trực tiếp "cung cấp" theo nghĩa là nguồn tài nguyên độc lập.</p>
	=[moodle]Cách ly các máy ảo khỏi nhau và lên lịch yêu cầu tới phần cứng.
	~[moodle]Quản lý các kết nối mạng giữa các máy ảo.#<p>Hypervisor là một phần của hệ thống ảo hóa, nhưng quản lý kết nối mạng giữa các máy ảo thường liên quan đến cấu hình mạng ảo bên trong hypervisor.</p>
	~[moodle]Cài đặt hệ điều hành lên máy ảo.#<p>Hệ điều hành được cài đặt bên trong máy ảo, không phải bởi hypervisor.</p>
	####<p><strong>Giải thích</strong>: Hypervisor chịu trách nhiệm cách ly các máy ảo (guest) khỏi nhau trên cùng một máy vật lý (host) và lên lịch các yêu cầu truy cập phần cứng bằng cách cung cấp một nền tảng phần cứng ảo cho các hệ thống khách.</p>
}

// question: 3.33 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Nếu bạn muốn sử dụng một địa chỉ IP công khai không đổi cho một ứng dụng được host trên EC2, bạn nên sử dụng dịch vụ AWS nào?</p>{
	~[moodle]Amazon S3.#<p>S3 là dịch vụ lưu trữ đối tượng, không liên quan đến địa chỉ IP cho máy ảo.</p>
	~[moodle]Amazon Virtual Private Cloud (VPC).#<p>VPC là mạng riêng ảo trong đám mây, cung cấp cơ sở hạ tầng mạng nhưng không trực tiếp cấp phát IP công khai cố định cho một instance cụ thể.</p>
	=[moodle]Elastic IP Address (EIP).
	~[moodle]Amazon Route 53.#<p>Route 53 là dịch vụ DNS, ánh xạ tên miền tới địa chỉ IP, nhưng EIP là dịch vụ cung cấp IP cố định.</p>
	####<p><strong>Giải thích</strong>: Nếu bạn muốn host một ứng dụng dưới một địa chỉ IP cố định mà không thay đổi khi máy ảo được dừng hoặc khởi chạy lại, bạn nên sử dụng dịch vụ Elastic IP Address (EIP). EIP cho phép bạn cấp phát một địa chỉ IP công khai cố định.</p>
}

// question: 3.34 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>AWS CLI cung cấp "help keyword" ở bao nhiêu cấp độ chi tiết?</p>{
	~[moodle]Một cấp độ.#<p>Các con số này không chính xác theo thông tin trong nguồn.</p>
	~[moodle]Hai cấp độ.#<p>Các con số này không chính xác theo thông tin trong nguồn.</p>
	=[moodle]Ba cấp độ.
	~[moodle]Bốn cấp độ.#<p>Các con số này không chính xác theo thông tin trong nguồn.</p>
	####<p><strong>Giải thích</strong>: Một tính năng quan trọng của CLI là "help keyword", cho phép bạn nhận được trợ giúp ở ba cấp độ chi tiết: aws help (hiển thị tất cả các dịch vụ), aws <service> help (hiển thị tất cả các hành động cho một dịch vụ nhất định), và aws <service> <action> help (hiển thị tất cả các tùy chọn cho hành động dịch vụ cụ thể).</p>
}

// question: 3.35 name: Chapter 3: Using virtual machines: EC2
::Chapter 3\: Using virtual machines: EC2::[html]<p>Tại sao việc thử khởi động ứng dụng của bạn với một instance type nhỏ hơn bạn nghĩ ban đầu lại được khuyến nghị?</p>{
	=[moodle]Để tránh lãng phí tài nguyên và có thể thay đổi sau này nếu cần.
	~[moodle]Vì các instance type lớn hơn không có sẵn cho người dùng mới.#<p>Các instance type lớn hơn vẫn có sẵn, nhưng có thể phát sinh chi phí.</p>
	~[moodle]Vì các instance type nhỏ hơn có hiệu suất CPU ổn định hơn.#<p>Các instance type nhỏ hơn như dòng T có hiệu suất CPU cơ bản vừa phải với khả năng burst, không phải ổn định cao.</p>
	~[moodle]Để đảm bảo ứng dụng chỉ chạy trên một CPU duy nhất.#<p>Mục tiêu là phù hợp với nhu cầu, không phải giới hạn ở một CPU duy nhất.</p>
	####<p><strong>Giải thích</strong>: Kinh nghiệm cho thấy người dùng thường ước tính quá mức yêu cầu tài nguyên cho ứng dụng. Do đó, việc khuyến nghị là nên thử khởi động ứng dụng với một instance type nhỏ hơn bạn nghĩ ban đầu, vì bạn có thể thay đổi instance family và type sau này nếu cần, giúp tránh lãng phí tài nguyên.</p>
}