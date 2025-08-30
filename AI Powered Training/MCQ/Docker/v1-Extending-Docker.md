Chapter 1: Introduction to Extending Docker
Question 1.1: What core problem does Docker primarily address for development and IT operations teams? A. Managing complex financial reporting and data synchronization across global databases. B. Ensuring applications behave consistently across different environments (development, staging, production). C. Optimizing hardware performance by completely virtualizing entire server systems. D. Facilitating real-time code collaboration and automated debugging for large software projects.
• Correct Answer: B
• Explanation (B): Docker provides an integrated technology suite that helps development and IT operations teams build, ship, and run distributed applications anywhere, specifically addressing the challenge of ensuring an application can consistently work across development, staging, and production stages.
• Explanation (A): While Docker can be part of solutions for data management, it's not its primary focus.
• Explanation (C): Docker focuses on containerization, which is lighter than full system virtualization provided by VMs.
• Explanation (D): Docker focuses on packaging and deployment, not direct code collaboration or debugging tools.
Question 1.2: What is a significant limitation when running multiple applications on a single dedicated machine? A. Dedicated machines are inherently less secure due to open network ports for all applications. B. All applications must share the same binaries and libraries, leading to compatibility issues during upgrades. C. The hardware performance is significantly reduced compared to virtualized environments. D. They are unable to connect to external databases, limiting their use to only local storage.
• Correct Answer: B
• Explanation (B): On a dedicated machine, binaries and libraries must be shared across the entire machine, leading to potential compatibility problems, such as when upgrading PHP for one application might break another that relies on an older version.
• Explanation (A), (C), (D): These are not the primary limitations described for dedicated machines in the source.
Question 1.3: From an IT operations perspective, what is a primary drawback of using virtual machines (VMs) compared to dedicated machines? A. VMs offer less isolation between applications, increasing the risk of cross-application interference. B. VMs require significantly more CPU, RAM, and disk space due to the overhead of running multiple guest operating systems. C. VMs prevent direct access to underlying hardware, leading to substantial performance degradation for I/O intensive tasks. D. Managing VMs is less complex as hypervisors automate most of the patching and monitoring activities.
• Correct Answer: B
• Explanation (B): From an IT operations perspective, VMs require more CPU, RAM, and disk space due to the overhead of running multiple guest operating systems, and they also increase management burden because each VM needs to be patched, monitored, and maintained.
• Explanation (A), (C), (D): These options either misrepresent VM characteristics or benefits/drawbacks as described in the source.
Question 1.4: What is the fundamental trade-off between dedicated and virtual machines, as illustrated by their configuration differences? A. A choice between strict security protocols and open-source software flexibility. B. A balance between resource utilization efficiency and the ability to use diverse binaries/libraries. C. A decision between local data storage reliability and cloud-based data accessibility. D. A compromise between rapid deployment speed and long-term system maintenance costs.
• Correct Answer: B
• Explanation (B): The biggest difference between dedicated and virtual machines highlights a trade-off between resource utilization and the ability to run applications using different binaries/libraries.
• Explanation (A), (C), (D): These options do not reflect the core trade-off explicitly mentioned in the source.
Question 1.5: What is a key advantage of Docker containers over virtual machines, particularly regarding resource usage? A. Containers allow applications to directly emulate diverse hardware, improving compatibility. B. Containers remove the need for a hypervisor and a guest operating system, significantly reducing overhead. C. Containers provide a fully isolated kernel for each application, enhancing security features. D. Containers automatically manage and scale underlying hardware resources based on application demand.
• Correct Answer: B
• Explanation (B): Docker containers offer the benefits of virtual machines but with a vastly reduced footprint, by removing the need for the hypervisor and guest operating system completely, and replacing them with a SlimLine interface directly into the host machine's kernel.
• Explanation (A), (C), (D): These statements misrepresent how Docker containers function or their primary advantages as described in the source.
Question 1.6: According to the IBM research report, how does Docker's performance generally compare to KVM? A. Docker significantly underperforms KVM across all tested workloads, especially for CPU and memory. B. Docker's performance is comparable to or exceeds KVM in most tested scenarios, with negligible CPU and memory overhead. C. KVM consistently outperforms Docker in I/O intensive workloads due to its native hardware virtualization. D. Both Docker and KVM have severe overheads for all types of workloads, making them unsuitable for production.
• Correct Answer: B
• Explanation (B): An IBM research report concluded that "Docker equals or exceeds KVM performance in every case we tested" and that "both KVM and Docker introduce negligible overhead for CPU and memory performance".
• Explanation (A), (C), (D): These contradict the findings presented in the IBM report, which notes I/O intensive workloads should be used carefully but doesn't state overall underperformance or severe overheads.
Question 1.7: In the context of the container lifecycle example, what is demonstrated by replacing a PHP 5.6 container with a PHP 7.0 container? A. The inherent difficulty in upgrading application dependencies within a Docker environment. B. The ability to quickly and consistently swap out different versions of an application or its dependencies. C. Docker's requirement for a complete system reboot when critical application components are updated. D. The necessity of manually compiling PHP from source each time a version change is required.
• Correct Answer: B
• Explanation (B): The example demonstrates the ability to quickly and consistently launch containers on top of code bases, by terminating a PHP 5.6 container and replacing it with a PHP 7.0 container to show an upgrade process.
• Explanation (A), (C), (D): These statements do not accurately reflect the purpose or outcome of the example.
Question 1.8: What is the recommended command to verify a successful Docker installation by running a test container? A. docker version check --all-modules B. docker status --verbose C. docker run hello-world D. docker system info --detailed
• Correct Answer: C
• Explanation (C): After installing Docker, you can check if everything worked as expected by running the Docker hello-world container using the command docker run hello-world.
• Explanation (A), (B), (D): These commands are not the standard or recommended way to verify a basic Docker installation as described.
Question 1.9: What is a major limitation of storing a container's codebase directly on the host machine's filesystem? A. It complicates version control and code collaboration for development teams. B. It prevents the container from being run on any other host, creating a single point of failure. C. It automatically exposes the host's entire filesystem to the container, posing a security risk. D. It drastically reduces the container's startup speed due to increased I/O operations.
• Correct Answer: B
• Explanation (B): Storing the codebase on the host machine's filesystem means that the container can only run on that single-host machine, which creates a single point of failure.
• Explanation (A), (C), (D): While these might be considerations, the primary limitation highlighted is the inability to run the container on other hosts.
Question 1.10: Which of the following is NOT a first-party tool provided by Docker to extend the core Docker Engine's functionality, as mentioned in the summary? A. Docker Machine B. Docker Swarm C. Docker Compose D. Kubernetes
• Correct Answer: D
• Explanation (D): The summary mentions Docker Toolbox, Docker Compose, Docker Machine, and Docker Swarm as first-party tools that will be covered in the next chapter. Kubernetes is a third-party container orchestrator.
• Explanation (A), (B), (C): These are explicitly listed as first-party tools by Docker.
Chapter 2: Introducing First-party Tools
Question 2.1: Which of the following components is NOT typically included in the Docker Toolbox installer package? A. Docker Machine for provisioning hosts. B. Docker Compose for multi-container applications. C. Docker Kitematic for GUI management. D. Docker Swarm for orchestrating clusters.
• Correct Answer: D
• Explanation (D): Docker Toolbox includes Docker Client, Docker Machine, Docker Compose, Docker Kitematic, and VM VirtualBox. While Docker Swarm is a first-party tool discussed alongside these, it is not explicitly listed as a component installed by the Docker Toolbox installer package.
• Explanation (A), (B), (C): These are explicitly listed as components installed by Docker Toolbox.
Question 2.2: What is the primary purpose of Docker Machine? A. To manage Docker images and layers within a private registry. B. To orchestrate multi-container applications on a single host. C. To provision and manage Docker hosts, both locally and on cloud providers. D. To scan Docker containers for security vulnerabilities and policy compliance.
• Correct Answer: C
• Explanation (C): Docker Machine is used to launch virtual machines running Docker and can connect to various cloud services to provision instances, configuring the local Docker client to communicate with these cloud-based instances.
• Explanation (A): Image management is generally handled by Docker CLI and registries.
• Explanation (B): Multi-container orchestration on a single host is primarily Docker Compose's role.
• Explanation (D): Security scanning is a separate tool or service.
Question 2.3: When using the DigitalOcean driver with Docker Machine, which command-line flag is used to specify the desired region for launching an instance? A. --digitalocean-location B. --digitalocean-zone C. --digitalocean-region D. --digitalocean-datacenter
• Correct Answer: C
• Explanation (C): To change the region when launching a DigitalOcean instance, the --digitalocean-region flag is used, for example, --digitalocean-region lon1.
• Explanation (A), (B), (D): These are not the correct flags as specified for the DigitalOcean driver.
Question 2.4: What is the default EC2 instance type launched by the Amazon Web Services driver when creating a Docker Machine? A. m4.large for general-purpose computing. B. t2.micro for cost-effective development and testing. C. c5.xlarge for CPU-intensive workloads. D. r4.2xlarge for memory-optimized applications.
• Correct Answer: B
• Explanation (B): The AWS driver for Docker Machine has sensible defaults, including amazonec2-instance-type = t2.micro.
• Explanation (A), (C), (D): These are not the default instance types mentioned.
Question 2.5: What is the primary role of Docker Swarm in a Docker environment? A. To manage the persistent storage for Docker volumes across different hosts. B. To provide a graphical user interface for interacting with Docker containers. C. To act as a scheduler, deciding where to deploy containers across a cluster of Docker hosts. D. To encrypt network traffic between Docker containers for enhanced security.
• Correct Answer: C
• Explanation (C): Docker Swarm acts as a scheduler between your Docker client and host Docker instances, deciding where to launch containers based on scheduling rules.
• Explanation (A): Volume management is handled by volume drivers.
• Explanation (B): Kitematic is a GUI tool.
• Explanation (D): Network encryption is a feature of some network drivers like Weave.
Question 2.6: Which of the following discovery services is NOT supported by Docker Swarm, as listed in the source? A. etcd B. Consul C. Kubernetes D. ZooKeeper
• Correct Answer: C
• Explanation (C): Docker Swarm supports etcd, Consul, and ZooKeeper as discovery services. Kubernetes is a separate container orchestrator, not a discovery backend for Swarm.
• Explanation (A), (B), (D): These are explicitly listed as supported discovery services for Docker Swarm.
Question 2.7: What was the original name of Docker Compose when it started as a third-party service? A. Swarm B. Machine C. Fig D. Kitematic
• Correct Answer: C
• Explanation (C): Docker Compose started its life as a third-party service called Fig, written by Orchard Labs.
• Explanation (A), (B), (D): These are other Docker first-party tools but not the original name of Compose.
Question 2.8: In a Docker Compose file, what is the primary function of the links key between services? A. To specify the network interface that containers should use for external communication. B. To define shared storage volumes that are accessible by multiple containers. C. To enable inter-container communication by exposing one container's ports to another within the network. D. To apply resource limits like CPU and memory to ensure fair usage among linked services.
• Correct Answer: C
• Explanation (C): The links key is used to link containers together, exposing, for example, a MySQL container to a WordPress container, allowing them to communicate.
• Explanation (A), (B), (D): These are not the functions of the links key; networking, volumes, and resource limits are handled by other configurations.
Question 2.9: What potential issue can arise when launching multiple Docker Compose environments on the same Docker host? A. Containers from different environments might share underlying filesystem layers, leading to data corruption. B. The Docker daemon might become overloaded, causing all containers to crash unexpectedly. C. Port assignments could clash if multiple environments attempt to use the same host port. D. Inter-container communication between services within the same environment might fail due to network conflicts.
• Correct Answer: C
• Explanation (C): When multiple Compose environments are launched on the same host, port assignments can clash as you cannot have two services listening on the same host port.
• Explanation (A), (B), (D): These are not the primary issues highlighted for running multiple Compose environments on a single host.
Question 2.10: Which of the following best describes the overall design philosophy of Docker's first-party tools like Docker Machine and Docker Compose? A. They are complex, low-level tools requiring extensive configuration and expertise to use effectively. B. They are open-source and community-driven, with no direct support from Docker itself. C. They are designed to extend core Docker functionality, fitting intuitively into existing workflows and being simple to use. D. They are proprietary tools focused exclusively on large-scale enterprise deployments, with limited local use.
• Correct Answer: C
• Explanation (C): Docker's client tools, including Docker Toolbox, Docker Machine, Docker Swarm, and Docker Compose, are designed to extend the core Docker installation's functionality and are intended to slot into workflows, being as simple and seamless as possible to use.
• Explanation (A), (B), (D): These statements contradict the description of the first-party tools in the source.
Chapter 3: Volume Plugins
Question 3.1: What is the primary consequence of running a Docker container without using any volumes for persistent data? A. The container will automatically be assigned a read-only filesystem, preventing any data modification. B. All data generated or modified within the container will be lost when the container is removed. C. The container's network connectivity will be severely limited, impacting its ability to access external resources. D. The container will consume excessive host machine resources, leading to performance bottlenecks.
• Correct Answer: B
• Explanation (B): When running a Docker container without volumes, any data stored directly on the container's filesystem will be lost once the container is removed, as demonstrated by the WordPress installation reappearing after container deletion.
• Explanation (A), (C), (D): These are not the primary consequences described for running containers without volumes.
Question 3.2: What is the main characteristic of the default local volume driver in Docker, as described in the source? A. It encrypts all data at rest by default for enhanced security measures. B. It enables volumes to be automatically replicated across multiple Docker hosts for high availability. C. It creates volumes on the Docker instance, mounting a folder from the host machine to the container. D. It provides a distributed filesystem, allowing data to be shared across a Swarm cluster without manual configuration.
• Correct Answer: C
• Explanation (C): The local volume driver, which is the default, creates the volume on the Docker instance and mounts a folder from the host machine (e.g., a VirtualBox host) into the container.
• Explanation (A), (B), (D): These features are not characteristic of the default local volume driver; they are typically provided by third-party or more advanced storage solutions.
Question 3.3: What significant problem do third-party volume drivers primarily aim to solve in a Dockerized environment? A. Reducing the initial image size of Docker containers before deployment. B. Enabling applications to run with elevated root privileges by default. C. Overcoming the limitation of data being tied to a single Docker host instance. D. Automating the process of building and pushing Docker images to a registry.
• Correct Answer: C
• Explanation (C): Third-party volume drivers are used to overcome the biggest limitation of default volumes, which is that the data is tied to a single instance, preventing data sharing or migration across multiple Docker hosts.
• Explanation (A), (B), (D): These are not the primary problems addressed by volume drivers.
Question 3.4: When installing Convoy, what type of file is created in /etc/docker/plugins/ to inform Docker about Convoy's availability? A. convoy.conf B. convoy.json C. convoy.spec D. convoy.yaml
• Correct Answer: C
• Explanation (C): After installing the Convoy binary, a convoy.spec file is created in /etc/docker/plugins/ to tell Docker where it can access Convoy.
• Explanation (A), (B), (D): These are not the correct file types mentioned for configuring Convoy as a Docker plugin.
Question 3.5: What are the two primary destination types supported by Convoy for storing volume backups, as demonstrated in the source? A. Local filesystem paths and network attached storage (NAS) shares. B. Version control systems (e.g., Git) and encrypted cloud drives. C. Local filesystem paths and Amazon S3 buckets. D. Dedicated backup servers and offsite tape archives.
• Correct Answer: C
• Explanation (C): Convoy supports creating backups to a local filesystem directory (e.g., vfs:///opt/backup/) and also to Amazon S3 buckets.
• Explanation (A), (B), (D): The source specifically details local file system (vfs) and Amazon S3 as backup destinations for Convoy.
Question 3.6: What is the primary characteristic that differentiates REX-Ray from default Docker volume drivers? A. REX-Ray enforces strict data encryption for all volumes by default, regardless of the backend. B. REX-Ray allows containers to directly attach and use remote block storage volumes like Amazon EBS. C. REX-Ray automates the backup and restore process to a central registry without manual configuration. D. REX-Ray is exclusively designed for on-premise deployments, lacking cloud provider integration.
• Correct Answer: B
• Explanation (B): REX-Ray enables the use of remote storage that is directly attached to containers, such as Amazon Elastic Block Store (EBS) volumes in AWS.
• Explanation (A), (C), (D): These statements do not accurately describe the core functionality or limitations of REX-Ray as presented.
Question 3.7: Which feature best highlights Flocker's strength as a third-party volume driver? A. Its exceptionally small binary size and minimal resource footprint, ideal for constrained environments. B. Its wide support for a diverse range of storage backends, including public clouds and enterprise solutions. C. Its automatic integration with Docker's default NAT networking for enhanced performance. D. Its exclusive focus on in-memory storage, prioritizing speed over data persistence for ephemeral data.
• Correct Answer: B
• Explanation (B): Flocker is described as the most feature-rich of the third-party volume drivers, with the widest coverage of storage backends, including various public cloud options and enterprise solutions.
• Explanation (A), (C), (D): These are not the primary strengths or characteristics described for Flocker.
Question 3.8: What are two essential prerequisites for setting up a Flocker cluster using the AWS CloudFormation template, as described? A. An existing Kubernetes cluster and a pre-configured Docker Hub private registry. B. An Amazon EC2 Key Pair and a ClusterHQ Volume Hub account. C. A local VirtualBox installation and an active Docker Swarm discovery service. D. A dedicated VPN connection and a pre-provisioned NFS share.
• Correct Answer: B
• Explanation (B): To launch a Flocker cluster with the AWS CloudFormation template, essential prerequisites include creating an AWS Key Pair (e.g., flocker-test) and having an account on the ClusterHQ Volume Hub to obtain a token.
• Explanation (A), (C), (D): These are not the direct prerequisites for the described Flocker setup.
Question 3.9: How does Flocker typically manage Docker volumes when containers are moved between different nodes in a cluster? A. Flocker automatically deletes the original volume and creates a new one on the destination node. B. Flocker un-attaches the volume from the source node and reattaches it to the destination node. C. Flocker forces a complete rebuild of the container image to include the volume data. D. Flocker requires manual intervention to copy volume data between nodes before moving a container.
• Correct Answer: B
• Explanation (B): Flocker handles the un-attaching and reattaching of volumes to nodes, which takes a little longer to launch when moving containers between hosts.
• Explanation (A), (C), (D): These options do not accurately describe Flocker's volume migration capabilities.
Question 3.10: What is a significant benefit of using Docker's plugin architecture for volume management, as highlighted in the chapter summary? A. It mandates the use of a single, universal storage backend for all container deployments. B. It provides a consistent client experience for managing volumes, regardless of the underlying storage driver. C. It completely eliminates the need for container image caching and local storage. D. It restricts volume access to only the container that initially created the data, enhancing security.
• Correct Answer: B
• Explanation (B): A key feature of using Docker plugins is the consistent experience from the client's point of view, meaning how you interact with volumes using the Docker client remains largely the same across different third-party drivers.
• Explanation (A), (C), (D): These statements do not reflect the benefits of Docker's plugin architecture as described.
Chapter 4: Network Plugins
Question 4.1: What is the primary limitation of Docker's default network bridge when working with multiple Docker hosts? A. It significantly degrades network performance due to excessive NAT translations. B. It prevents containers from accessing external network resources like the internet. C. It restricts containers to communication only within a single Docker host. D. It requires manual configuration of IP addresses for every container in the network.
• Correct Answer: C
• Explanation (C): Docker's default network bridge limits containers to being brought up on a single host, meaning that containers on different hosts within a cluster would not be able to communicate with each other.
• Explanation (A), (B), (D): These are not the primary limitations described for the default network bridge.
Question 4.2: What is the fundamental capability that Docker's multi-host overlay networking provides? A. It allows containers to directly emulate different network hardware interfaces. B. It enables containers on separate Docker hosts to communicate as if they were on the same host. C. It completely isolates container network traffic from the underlying host network. D. It forces all container network communication to pass through a central, external proxy server.
• Correct Answer: B
• Explanation (B): In Docker terms, an overlay network allows containers on one Docker host to communicate directly with containers on another Docker host, as if they were situated on the same host.
• Explanation (A), (C), (D): These statements do not accurately describe the core function of overlay networks in Docker.
Question 4.3: Why is a persistent key/value store like Consul required as a prerequisite for Docker's multi-host networking with overlays? A. To cache frequently accessed Docker images across the cluster. B. To store permanent and accessible values about the Docker Swarm cluster. C. To provide a secure vault for encrypting sensitive container environment variables. D. To facilitate real-time performance monitoring and logging for all network traffic.
• Correct Answer: B
• Explanation (B): Multi-host networking requires a persistent key/value store, such as Consul, to provide a permanent and accessible place to store values about the Docker Swarm cluster.
• Explanation (A), (C), (D): These are not the primary functions of a persistent key/value store for multi-host networking.
Question 4.4: When preparing a Docker Swarm cluster for multi-host networking, which Docker Machine flag is used to connect the Swarm nodes to a Consul discovery service? A. --swarm-join-consul B. --swarm-link-service C. --swarm-discovery D. --engine-connect-consul
• Correct Answer: C
• Explanation (C): The --swarm-discovery flag is used to connect the Swarm master and nodes to the Consul discovery service, specifying the Consul host's IP address and port.
• Explanation (A), (B), (D): These are not the correct flags for Swarm discovery as specified in the examples.
Question 4.5: What command is used to create a new overlay network for a Docker Swarm cluster, including specifying its driver and subnet? A. docker create network --overlay --subnet=10.0.9.0/24 my-network B. docker network new --type overlay --ip-range 10.0.9.0/24 my-network C. docker network create --driver overlay --subnet=10.0.9.0/24 my-network D. docker build network --overlay --cidr 10.0.9.0/24 my-network
• Correct Answer: C
• Explanation (C): The command docker network create --driver overlay --subnet=10.0.9.0/24 <network_name> is used to create an overlay network with a specified driver and subnet, which is then distributed to all Swarm cluster nodes.
• Explanation (A), (B), (D): These options use incorrect syntax or flags for creating a Docker network.
Question 4.6: When containers are launched in the same Docker Overlay Network, what happens regarding their communication without explicit link flags? A. They can only communicate if their ports are explicitly published to the host. B. Docker automatically handles their communication and linking within the network. C. Communication is entirely disabled by default for security reasons. D. They must resolve each other's IP addresses manually using external DNS servers.
• Correct Answer: B
• Explanation (B): When containers are launched in the same Overlay Network, Docker assumes they can communicate with each other and automatically handles the linking of these containers without requiring explicit link flags.
• Explanation (A), (C), (D): These statements do not accurately describe communication within an overlay network.
Question 4.7: What is the purpose of adding --internal flag when creating a Docker Overlay Network? A. To allow containers within the network to communicate only with the Docker host. B. To disable all network traffic, making the containers completely isolated. C. To ensure the network is only accessible from specific, predefined external IP addresses. D. To prevent the network from having an external gateway, making it internal-only.
• Correct Answer: D
• Explanation (D): The --internal flag is used when creating an overlay network to ensure that the network will not have an external gateway, thereby restricting it to internal-only communication.
• Explanation (A), (B), (C): These options misrepresent the functionality of the --internal flag.
Question 4.8: What type of networking service is Weave Net primarily described as? A. A hardware-based network accelerator. B. A simple port forwarding utility. C. A mature software-defined networking (SDN) service. D. A proprietary network traffic analyzer.
• Correct Answer: C
• Explanation (C): Weave Net is described as a mature software-defined networking (SDN) service by Weaveworks.
• Explanation (A), (B), (D): These options do not accurately describe Weave Net's core functionality.
Question 4.9: In a Docker Compose file configured for Weave networking, what is the primary purpose of defining hostname, dns, and dns_search for containers? A. To enable direct hardware access for improved application performance. B. To configure security policies for inter-container communication. C. To integrate with Weave's internal DNS system for service discovery. D. To automatically generate SSL certificates for secure network connections.
• Correct Answer: C
• Explanation (C): When using Weave, defining hostname, dns (e.g., 172.17.0.1), and dns_search (e.g., weave.local) in the Docker Compose file allows containers to integrate with Weave's internal DNS system for service discovery.
• Explanation (A), (B), (D): These are not the primary purposes of these configurations for Weave.
Question 4.10: What is a unique capability of the Weavemesh driver compared to the global scope Weave driver that operates with Docker Swarm? A. It exclusively supports IPv6 addressing for all container networks. B. It operates without the need for a cluster store and can span non-clustered machines. C. It provides automatic load balancing and service discovery across multiple data centers. D. It requires a dedicated hardware appliance for network virtualization.
• Correct Answer: B
• Explanation (B): Weave Mesh is a local scope driver that operates without the need for a cluster store and can be used to create networks that span non-clustered machines, creating a single network called Weave across them.
• Explanation (A), (C), (D): These are not the unique characteristics of Weavemesh as described.
Chapter 5: Building Your Own Plugin
Question 5.1: What types of plugin engines are currently supported by the Docker API for third-party integration, as stated in the source? A. User interface customization and authentication providers. B. Hardware virtualization and operating system emulation. C. Storage and networking engines. D. Application monitoring and logging aggregators.
• Correct Answer: C
• Explanation (C): The Docker API currently allows third-party plugin services to hook their own storage and networking engines into the Docker Engine.
• Explanation (A), (B), (D): These are not the specific plugin types mentioned as currently supported by the Docker API.
Question 5.2: What programming language is most commonly used for writing Docker plugins, as observed across Convoy, REX-Ray, and Weave? A. Python, known for its extensive libraries and community support. B. Java, preferred for large-scale enterprise applications and robust ecosystems. C. Go, chosen for its expressiveness, efficiency, and concurrency mechanisms. D. Ruby, often used for automation and configuration management tools.
• Correct Answer: C
• Explanation (C): The majority of the services for plugins like Convoy, REX-Ray, and Weave are written in Go, which is valued for its expressiveness, conciseness, efficiency, concurrency, and modular program construction.
• Explanation (A), (B), (D): While Flocker is in Python, Go is noted as the language for the majority.
Question 5.3: How does Docker formally define a plugin in the context of the Docker Engine? A. A plugin is an embedded module that modifies the core Docker daemon's internal logic. B. A plugin is an out-of-process extension that adds capabilities to the Docker Engine. C. A plugin is a container image pre-loaded with specialized tools for specific tasks. D. A plugin is a command-line utility that provides additional Docker CLI functions.
• Correct Answer: B
• Explanation (B): Docker defines a plugin as "out-of-process extensions which add capabilities to the Docker Engine".
• Explanation (A), (C), (D): These definitions do not match Docker's formal description of a plugin.
Question 5.4: Where does Docker primarily look for files to discover and register new plugins on a Linux system? A. Only in the /var/log/docker/plugins directory for logging purposes. B. In /run/docker/plugins for Unix socket files, and /etc/docker/plugins or /usr/lib/docker/plugins for .spec or .json files. C. Within the Dockerfile of an image when a container is built. D. Directly in the host's /usr/local/bin folder as executable binaries.
• Correct Answer: B
• Explanation (B): Docker discovers plugins by looking for files in /run/docker/plugins for Unix socket files, and in /etc/docker/plugins or /usr/lib/docker/plugins for .spec or .json files.
• Explanation (A), (C), (D): These are incorrect locations for plugin discovery.
Question 5.5: What is the ideal startup order for a Docker plugin service relative to the Docker daemon, and how can this be enforced with systemd? A. The Docker daemon should always start before the plugin service to initialize the environment; this is enforced with After=docker.service. B. The plugin service should ideally start before the Docker daemon; this can be achieved using Before=docker.service in a systemd unit file. C. The startup order is irrelevant as Docker dynamically discovers and activates plugins on demand. D. Both the plugin service and Docker daemon must start simultaneously using a unified systemd target.
• Correct Answer: B
• Explanation (B): Ideally, your plugin service should be started before Docker, which can be achieved by using a systemd service file with Before=docker.service.
• Explanation (A), (C), (D): These statements contradict the recommended startup order or method of enforcement.
Question 5.6: What is the required HTTP POST request path that Docker makes to a plugin service to activate it? A. /plugin/activate B. /Plugin.Activate C. /docker/plugin/init D. /api/v1/plugin/register
• Correct Answer: B
• Explanation (B): The first request made by Docker to a plugin service for activation will be a POST request to /Plugin.Activate.
• Explanation (A), (C), (D): These are not the correct HTTP POST request paths for plugin activation.
Question 5.7: After successful activation, how does the Docker daemon communicate with the plugin service for subsequent operations? A. Through direct system calls to the plugin's kernel module. B. By sending RPC-style JSON over HTTP POST requests to the plugin service. C. Via shared memory segments that are constantly polled by the plugin. D. Using a proprietary binary protocol that is not publicly documented.
• Correct Answer: B
• Explanation (B): Once activated, the Docker daemon will make POST requests using RPC-style JSON over HTTP to the plugin service, using either the socket file or the URL defined in the .spec or .json file.
• Explanation (A), (C), (D): These are not the methods of communication described between the Docker daemon and plugin service.
Question 5.8: Where can developers find an official SDK (Software Development Kit) to assist with writing Docker plugins in Go? A. On the Docker Hub as a pre-built container image for plugin development. B. As a collection of Go helpers on the github.com/docker/go-plugins-helpers repository. C. Integrated directly into the Docker CLI, accessible via docker plugin dev --sdk. D. Through third-party community forums and unofficial documentation wikis.
• Correct Answer: B
• Explanation (B): Docker provides an SDK as a collection of Go helpers, which can be found at https://github.com/docker/go-plugins-helpers.
• Explanation (A), (C), (D): These are not the correct locations or methods for accessing the official Docker plugin SDK.
Question 5.9: What is the key distinction between the Docker Plugin API and the Docker Remote API? A. The Plugin API is used for internal Docker daemon processes, while the Remote API is for external client interactions. B. The Plugin API allows Docker to interact with your plugin application, whereas the Remote API allows your application to interact with Docker. C. The Plugin API is solely for network drivers, while the Remote API is exclusively for storage drivers. D. The Plugin API is deprecated and replaced by the Remote API for all extension purposes.
• Correct Answer: B
• Explanation (B): The Docker Plugin API is designed for Docker to interact with your plugin service, whereas the Docker Remote API is what allows your applications to interact with Docker.
• Explanation (A), (C), (D): These statements incorrectly describe the relationship or purpose of the two APIs.
Question 5.10: Which of the following is a fundamental requirement for a custom plugin service to successfully interact with the Docker daemon, as outlined in the challenges of building a plugin? A. The plugin service must be written exclusively in Python for cross-platform compatibility. B. The plugin service must expose its functionality through a simple command-line interface only. C. The plugin service must include an HTTP server bound to a Unix socket or TCP port to accept Docker's requests. D. The plugin service must be embedded directly within the Docker daemon binary for optimal performance.
• Correct Answer: C
• Explanation (C): A plugin service needs to contain an HTTP server bound to a Unix socket or TCP port to accept and answer requests made to it by the Docker daemon.
• Explanation (A), (B), (D): These statements do not accurately reflect the requirements for a custom plugin service.
Chapter 6: Extending Your Infrastructure
Question 6.1: Why might users consider employing third-party infrastructure tools with Docker, even after Docker introduced its own first-party tools? A. Docker's first-party tools are proprietary and require expensive licenses for production use. B. Many third-party tools are more mature, have active communities, and offer broader functionality beyond Docker. C. Third-party tools inherently provide better security isolation for containers compared to Docker's native offerings. D. Docker's first-party tools are exclusively designed for cloud environments, making them unsuitable for on-premise use.
• Correct Answer: B
• Explanation (B): While Docker has been releasing its own tooling, some third-party options are actually more mature and have quite an active community behind them, offering functionality that complements or precedes Docker's built-in tools.
• Explanation (A), (C), (D): These are not the primary reasons provided for using third-party tools.
Question 6.2: What is the core principle of Puppet in managing IT infrastructure? A. It provides a real-time monitoring and alert system for all server resources. B. It allows administrators to define the desired state of their infrastructure, which Puppet then automatically enforces. C. It offers a command-line interface for manual, interactive configuration of individual servers. D. It serves as a distributed database for storing application secrets and credentials securely.
• Correct Answer: B
• Explanation (B): Puppet allows you to define the state of your IT infrastructure, and it automatically enforces this desired state, automating various steps of the software delivery process.
• Explanation (A), (C), (D): These are not the core principles of Puppet's configuration management.
Question 6.3: What is the purpose of a Puppet manifest like docker.pp when integrating Puppet with Docker? A. It defines the network topology and routing rules for Docker containers. B. It specifies which Docker images to download and which containers to launch and configure. C. It provides a real-time dashboard for monitoring Docker container performance. D. It automates the process of building custom Docker images from source code.
• Correct Answer: B
• Explanation (B): A Puppet manifest, such as docker.pp, defines configurations like which Docker images to install and which containers to run and with what settings.
• Explanation (A), (C), (D): These are not the primary functions of a Puppet manifest for Docker.
Question 6.4: What is a key disadvantage of using Puppet for container orchestration, even in a Master/Agent setup, compared to a tool like Docker Swarm? A. Puppet requires a complex, proprietary database to store configuration states, increasing overhead. B. Puppet's configuration logic for container placement is manual, not automated like a scheduler. C. Puppet agents only pull configurations once, making dynamic updates impossible without manual intervention. D. Puppet is incompatible with most Linux distributions, limiting its deployment options for Docker hosts.
• Correct Answer: B
• Explanation (B): A downside of using Puppet for Docker orchestration is that it does not replace Docker Swarm because all of the logic as to where the containers are launched is defined manually within each manifest file, rather than being scheduled automatically.
• Explanation (A), (C), (D): These statements misrepresent Puppet's features or limitations.
Question 6.5: Why is it generally advised against bundling a Puppet Agent inside Docker containers? A. It prevents the container from properly connecting to the Docker Hub for image downloads. B. It adds unnecessary bloat and additional processes to the container, contradicting the single-process ideal. C. It creates a security vulnerability by exposing the host's Puppet Master to the container's environment. D. It causes conflicts with Docker's native volume drivers, leading to data corruption issues.
• Correct Answer: B
• Explanation (B): It is advised to avoid bundling a Puppet Agent inside containers because it may add unnecessary bloat and introduce additional processes, whereas containers in an ideal world should run a single process.
• Explanation (A), (C), (D): These are not the primary reasons given for avoiding Puppet Agent in containers.
Question 6.6: When using Ansible to provision Docker hosts on DigitalOcean, what information is typically stored in the group_vars/do.yml file? A. The default network bridge configurations for all Docker containers. B. The DigitalOcean API token and the SSH key name for authentication. C. A list of all Docker images to be pre-pulled onto the hosts. D. The desired number of CPU cores and RAM allocation for each container.
• Correct Answer: B
• Explanation (B): The group_vars/do.yml file is used to store the DigitalOcean API token and the SSH key name required by the Ansible playbook for launching instances and connecting to them.
• Explanation (A), (C), (D): These are not the primary contents specified for the group_vars/do.yml file.
Question 6.7: In an Ansible playbook for Docker deployment, which section is responsible for connecting the Weave networks between the newly provisioned Docker hosts? A. Section one, dedicated to launching the initial Droplets. B. Section two, which handles the installation of Docker and Weave binaries. C. Section three, specifically the weave-connect role. D. Section four, where the WordPress container is deployed.
• Correct Answer: C
• Explanation (C): The weave-connect role within Section three of the site.yml file is responsible for connecting the two Weave networks on the two hosts together.
• Explanation (A), (B), (D): These sections have different responsibilities in the playbook.
Question 6.8: What is a fundamental difference in how Ansible executes its tasks compared to Puppet? A. Ansible requires a persistent agent running on each target machine, unlike Puppet. B. Ansible compiles playbooks locally and executes them remotely via SSH in a defined order. C. Ansible primarily uses a declarative approach, while Puppet relies on imperative scripting. D. Ansible applies configurations using an eventual consistency model, which can take multiple runs.
• Correct Answer: B
• Explanation (B): When an Ansible playbook is run, it is compiled locally, then the compiled script is pushed to target servers using SSH and executed, with tasks running in the exact order defined in the playbook.
• Explanation (A), (D): These describe characteristics more aligned with Puppet.
• Explanation (C): Both tools are largely declarative, but their execution models differ significantly.
Question 6.9: What is the main drawback of using Vagrant's Docker provider (as opposed to the provisioner) for launching containers? A. It restricts the Docker version to older, less secure releases. B. It only supports port mapping and cannot assign IP addresses to containers, limiting network flexibility. C. It requires a dedicated, always-on internet connection to download base images. D. It automatically bundles unnecessary developer tools into container images, increasing their size.
• Correct Answer: B
• Explanation (B): A limitation of Vagrant's Docker provider is that it can only use port mapping and cannot assign an IP address to the virtual machine, which significantly limits network flexibility.
• Explanation (A), (C), (D): These are not the primary drawbacks specified for the Docker provider.
Question 6.10: What is a significant advantage of using Packer to build Docker images compared to traditional Dockerfile builds, particularly regarding image size? A. Packer automatically compresses all image layers, regardless of their content, reducing network transfer times. B. Packer leverages a proprietary image format that is inherently smaller than Docker's layered filesystem. C. Packer produces only two layers (base image + all changes), leading to significantly smaller final images. D. Packer completely eliminates the need for a base image, creating images from scratch every time.
• Correct Answer: C
• Explanation (C): A significant advantage of Packer is that it produces only two layers (the base image you define and everything else), which leads to smaller image sizes compared to Dockerfiles where each command creates a new layer.
• Explanation (A), (B), (D): These statements do not accurately describe how Packer optimizes image size.
Chapter 7: Looking at Schedulers
Question 7.1: Which of the following is NOT a core principle that Kubernetes is designed around? A. Planet Scale: Ability to scale without increasing operations teams. B. Proprietary Cloud Lock-in: Exclusive integration with Google Cloud Platform. C. Never Outgrow: Flexibility to grow with user needs from local testing to global enterprise. D. Run Anywhere: Open source, allowing deployment on-premise, hybrid, or public cloud.
• Correct Answer: B
• Explanation (B): Kubernetes is designed around principles like Planet Scale, Never Outgrow, and Run Anywhere. It is open source and not tied to any particular provider, actively moving away from cloud lock-in.
• Explanation (A), (C), (D): These are stated as core principles of Kubernetes.
Question 7.2: Before launching a Kubernetes cluster on Amazon Web Services using the provided installation script, what environment variable must be set to specify the cloud provider? A. CLOUD_PROVIDER=AWS B. KUBERNETES_PLATFORM=amazon C. KUBERNETES_PROVIDER=aws D. DEPLOY_TARGET=AWS_EC2
• Correct Answer: C
• Explanation (C): To instruct the Kubernetes installation script to launch the cluster in Amazon Web Services, the KUBERNETES_PROVIDER environment variable must be set to aws.
• Explanation (A), (B), (D): These are not the correct environment variables for specifying the cloud provider.
Question 7.3: In Kubernetes, what resource type is used to manage the number of running pods and ensure a specified number of replicas are always available? A. Service B. Deployment C. ReplicationController D. Ingress
• Correct Answer: C
• Explanation (C): When launching an application, a ReplicationController is defined, which is the process that manages the number of pods to ensure a specified number of replicas are running.
• Explanation (A), (B), (D): While related to deployment, these serve different purposes; Services expose pods, Deployments manage declarative updates to pods and ReplicaSets (a successor to ReplicationController).
Question 7.4: When defining a Kubernetes Pod to use an Amazon EBS volume, what specific property within the Pod definition YAML is used to specify the EBS volume ID? A. persistentVolumeClaim.volumeName B. hostPath.path C. awsElasticBlockStore.volumeID D. storageClass.name
• Correct Answer: C
• Explanation (C): In the Pod definition for MySQL, the awsElasticBlockStore section contains the volumeID property to specify the Amazon EBS volume to be used.
• Explanation (A), (B), (D): These are not the correct properties for directly specifying an EBS volume ID in a Pod definition.
Question 7.5: Which Kubernetes supporting tool is primarily used to record and visualize metrics such as CPU usage, memory usage, and network usage across the cluster and individual nodes? A. Kubernetes Dashboard B. Kibana C. Grafana D. Heapster
• Correct Answer: C
• Explanation (C): Grafana is the tool that records all the metrics displayed in the Kubernetes dashboard, providing a breakdown of metrics like CPU Usage, Memory Usage, Network Usage, and Filesystem Usage, both collectively and per individual node.
• Explanation (A): The Dashboard is a UI for management, showing data, but Grafana is the dedicated visualization tool for metrics.
• Explanation (B): Kibana is for log data visualization.
• Explanation (D): Heapster is an internal component that collects metrics, which Grafana then visualizes.
Question 7.6: What command is used to completely tear down a Kubernetes cluster that was deployed using the get.k8s.io script? A. kubectl delete cluster --all B. ./kubernetes/cluster/kube-down.sh C. docker-machine rm --kubernetes-cluster D. aws kubernetes terminate-environment
• Correct Answer: B
• Explanation (B): To remove a Kubernetes cluster deployed using the installation script, you run ./kubernetes/cluster/kube-down.sh from the same location where the cluster was initially deployed.
• Explanation (A), (C), (D): These are not the correct commands or methods for tearing down the cluster as described.
Question 7.7: What is a key benefit of Amazon EC2 Container Service (ECS) regarding cluster management? A. It requires users to manually install and manage all cluster management infrastructure. B. It eliminates the need for users to install, operate, and scale their own cluster management infrastructure. C. It provides exclusive support for non-Docker container runtimes for enhanced flexibility. D. It is a completely free service, with no charges for any underlying compute resources.
• Correct Answer: B
• Explanation (B): Amazon ECS eliminates the need for you to install, operate, and scale your own cluster management infrastructure, allowing you to run applications on a managed cluster of Amazon EC2 instances.
• Explanation (A), (C), (D): These statements contradict the described benefits or cost structure of ECS.
Question 7.8: In Amazon ECS, what is the purpose of a "Task Definition"? A. It defines the network routing rules for traffic between different ECS clusters. B. It specifies the container image, resource allocation (RAM, CPU), and port mappings for a container. C. It serves as a central registry for all Docker images deployed within ECS. D. It automates the backup and restore process for all persistent data volumes in the cluster.
• Correct Answer: B
• Explanation (B): A Task Definition in Amazon ECS is the equivalent of creating a Docker Compose file, where you define the container image to run, the resources it's allowed to consume (RAM, CPU), and the port mappings from the host to the container.
• Explanation (A), (C), (D): These are not the primary purposes of a Task Definition.
Question 7.9: What are the three different container orchestration tools (schedulers) that Rancher supports for creating environments? A. Mesos, Marathon, and Nomad. B. Kubernetes, Docker Swarm, and Cattle. C. OpenStack, VMware vSphere, and Hyper-V. D. Chef, Puppet, and Ansible.
• Correct Answer: B
• Explanation (B): Rancher supports three different schedulers: Docker Swarm, Kubernetes, and its own default scheduler called Cattle.
• Explanation (A), (C), (D): These are other orchestrators, virtualization platforms, or configuration management tools, not the schedulers directly supported by Rancher.
Question 7.10: When deploying applications in Rancher, what is a key feature that helps ensure application availability during upgrades or container failures? A. Rancher automatically halts all running services during an upgrade to prevent data inconsistency. B. Rancher provides built-in health checks that can automatically recreate unhealthy containers without downtime. C. Rancher requires manual intervention for every container restart, ensuring granular control. D. Rancher relies solely on external load balancers to detect and reroute traffic from failed containers.
• Correct Answer: B
• Explanation (B): Rancher provides health checks that can be configured to automatically recreate unhealthy containers (e.g., if a port stops responding), performing upgrades one container at a time to ensure no downtime.
• Explanation (A), (C), (D): These options contradict Rancher's features for high availability.
Chapter 8: Security, Challenges, and Conclusions
Question 8.1: As organizations move Docker containers from development to production, what becomes increasingly important regarding the container images they use? A. The aesthetic design and visual appeal of the container's base operating system. B. The file size of the container image, prioritizing the smallest possible size above all else. C. Knowing precisely what is installed within the image and who created it. D. The number of different programming languages supported by the base image.
• Correct Answer: C
• Explanation (C): As you move towards production, it becomes increasingly important to know what you are installing within your container images, including who created them and their contents.
• Explanation (A), (B), (D): While size can be a factor, these are not the primary security concerns for production containers.
Question 8.2: According to the source, what are the three main types of images that can be downloaded from Docker Hub? A. Community-contributed, Enterprise-licensed, and Experimental. B. Dockerfile-built, Official, and Pushed. C. Legacy, Current-release, and Beta. D. Local-only, Cloud-hosted, and Hybrid.
• Correct Answer: B
• Explanation (B): The three types of images that can be downloaded from Docker Hub are Dockerfile-built (publicly accessible Dockerfiles), Official images, and Pushed images (complete images uploaded by users).
• Explanation (A), (C), (D): These are not the classification categories for Docker Hub images mentioned.
Question 8.3: What is the main security advantage of a Docker image being built from a publicly accessible Dockerfile? A. It guarantees that the image will be significantly smaller in size compared to other image types. B. It allows users to transparently review the exact steps and contents used to build the image. C. It automatically performs vulnerability scanning and fixes all found issues before publication. D. It ensures that the image can only be deployed on specific, trusted cloud platforms.
• Correct Answer: B
• Explanation (B): Building an image from a publicly accessible Dockerfile, as with the Consul image example, allows users to see exactly what actions have been taken to build and configure the image, providing transparency.
• Explanation (A), (C), (D): These are not the primary security advantages of a publicly accessible Dockerfile.
Question 8.4: What is a critical security standard for Docker's "Official images" regarding their dependencies? A. Official images must never include any pre-installed software, only a base operating system. B. Official images can only be derived from or depend on other official images. C. Official images must explicitly declare all their external network dependencies in a separate manifest. D. Official images are required to use a proprietary, encrypted filesystem for all their layers.
• Correct Answer: B
• Explanation (B): An important characteristic of official images is that no official image can be derived from, or depend on, non-official images, ensuring that non-official content doesn't find its way into them.
• Explanation (A), (C), (D): These are not the specific dependency standards for official images mentioned.
Question 8.5: What mechanism did Docker introduce to address concerns about the integrity and origin of "pushed images" on Docker Hub? A. Automated source code review by Docker staff for all pushed images. B. A strict policy that prohibits pushing complete images, requiring Dockerfile builds instead. C. Docker Content Trust, which uses cryptographic signatures to verify image content. D. A system that automatically rebuilds all pushed images from a trusted base every 24 hours.
• Correct Answer: C
• Explanation (C): Docker introduced Content Trust to the Docker Hub, which signs an image with the publisher's private key before it is pushed, and the Docker Engine uses the public key to verify content on download, ensuring integrity.
• Explanation (A), (B), (D): These are not the specific mechanisms described for securing pushed images.
Question 8.6: What type of analysis does Docker Cloud's Security Scanning feature perform on images to identify vulnerabilities? A. Dynamic runtime analysis, monitoring container behavior in isolation. B. Static analysis, inspecting images for known vulnerabilities in binaries. C. Network traffic analysis, detecting malicious communication patterns. D. User behavior analysis, identifying suspicious activities within running containers.
• Correct Answer: B
• Explanation (B): Docker Cloud's Security Scanning feature performs a static analysis on your images, looking for known vulnerabilities in the binaries that have been installed.
• Explanation (A), (C), (D): These are not the types of analysis described for Docker Cloud's security scanning.
Question 8.7: What are two key characteristics that distinguish a private Docker registry from Docker Hub? A. Private registries always offer free unlimited storage and automatic vulnerability scanning. B. Private registries are typically only available to trusted hosts within a network and do not support automated builds or content trust. C. Private registries provide a public API for image discovery and global content delivery network integration. D. Private registries are managed exclusively by Docker Inc. and offer enhanced debugging tools.
• Correct Answer: B
• Explanation (B): Private registries are typically available only to trusted hosts within your network and are not publicly available; they also do not allow you to host automated builds and do not currently support content trust.
• Explanation (A), (C), (D): These statements contradict the described features of private registries.
Question 8.8: Which of the following tools is specifically mentioned as helping developers introduce Docker locally as the first step of the development process? A. Kubernetes B. Docker Swarm C. Docker Toolbox D. Amazon ECS
• Correct Answer: C
• Explanation (C): Docker Toolbox is listed as one of the tools that can help developers start to use Docker locally as the first step of the development process.
• Explanation (A), (B), (D): These are primarily orchestration or cloud services, not tools for local Docker introduction for developers.
Question 8.9: For creating a basic staging environment with multi-host networking and storage, which of the following is recommended as a volume plugin? A. Git LFS B. REX-Ray C. SSHFS D. Dropbox Sync
• Correct Answer: B
• Explanation (B): REX-Ray is listed as a volume plugin that could be used in conjunction with Docker Compose to create a basic staging environment with multi-host networking and storage.
• Explanation (A), (C), (D): These are not the specific volume plugins mentioned for a staging environment.
Question 8.10: For a production environment that needs to automatically react to failures, handle scaling events, and perform auto-registration with services like DNS and Load Balancers, which of the following tools is highly recommended? A. Vagrant B. Docker Compose C. Kubernetes D. Docker Toolbox
• Correct Answer: C
• Explanation (C): For a production environment requiring automated reactions to failure, scaling events, and auto-registration with services like DNS and Load Balancers, tools like Kubernetes, Amazon ECS, Docker Swarm, and Rancher are recommended as they provide scheduling capabilities.
• Explanation (A), (B), (D): These tools are more focused on local development or single-machine orchestration, not large-scale, self-managing production environments.