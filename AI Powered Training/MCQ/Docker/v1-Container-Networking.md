// Chapter 1: Motivation

// question: 1.1  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>What is the primary characteristic of the "cattle approach" to infrastructure, as established by Randy Bias?</p>{
	~[moodle]Machines are individually named, statically allocated, and manually nursed back to health when ill.#<p>This describes the "pets approach" where machines are treated as individuals.</p>
	=[moodle]Machines are anonymous, identical, numbered, and replaced rather than nursed back to health when issues arise.
	~[moodle]Applications are manually deployed onto specific machines, which are then carefully monitored as unique entities.#<p>This also describes the "pets approach," focusing on manual deployment and individual machine treatment.</p>
	~[moodle]Infrastructure is primarily composed of bare-metal servers, where each server runs a single, dedicated application for maximum performance.#<p>The cattle approach applies to both virtual machines and commodity hardware, and its core is about treating machines as interchangeable, not about specific hardware types or single applications per server.</p>
	####<p><strong>Explanation</strong>\: With the cattle approach, machines are anonymous, identical (modulo hardware upgrades), have numbers rather than names, and apps are automatically deployed onto any and each of the machines. When one gets ill, it is replaced.</p>
}

// question: 1.2  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>According to the source, what is one of the main benefits for operators when applying the "cattle approach" to infrastructure?</p>{
	~[moodle]It simplifies the process of manually reconfiguring network settings for each individual machine.#<p>The cattle approach simplifies management by treating machines as interchangeable, not by simplifying manual network reconfigurations.</p>
	~[moodle]It ensures that applications are always deployed on the highest-performing, specialized hardware available in the datacenter.#<p>The cattle approach allows scaling out on commodity hardware, not necessarily high-performing specialized hardware.</p>
	=[moodle]It allows for a decent night's sleep by automating the replacement of broken components or restarting hanging apps on different servers.
	~[moodle]It guarantees that all system patches and software updates are applied uniformly and immediately across all machines in the cluster.#<p>While automation is a goal, the source does not state that the cattle approach automatically guarantees uniform and immediate patching/updates across all machines.</p>
	####<p><strong>Explanation</strong>\: From an operator's point of view, the cattle approach allows for a decent night's sleep, as they are no longer paged at 3 a.m. to replace a broken hard disk drive or relaunch a hanging app on a different server.</p>
}

// question: 1.3  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>What are the two main categories of challenges posed by the "cattle approach" to infrastructure?</p>{
	~[moodle]Financial challenges related to hardware investment and security challenges regarding data breaches.#<p>While these can be concerns, the source specifically categorizes challenges into social and technical.</p>
	=[moodle]Social challenges concerning team buy-in and technical challenges dealing with base provisioning and communication links.
	~[moodle]Performance challenges due to shared resources and scalability challenges when handling sudden traffic spikes.#<p>These are potential technical concerns, but the main categories given are social and technical, which encompass these.</p>
	~[moodle]Compliance challenges with industry regulations and integration challenges with legacy enterprise systems.#<p>These are also potential concerns, but not the primary categories identified in the source.</p>
	####<p><strong>Explanation</strong>\: The cattle approach poses social challenges (e.g., convincing managers, team buy-in) and technical challenges (e.g., base provisioning, setting up communication links, automatic deployment and discovery).</p>
}

// question: 1.4  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>Which of the following components is part of the low-level networking layer in the container networking stack?</p>{
	~[moodle]Single-host bridge networking modes and multi-host, IP-per-container solutions.#<p>These are part of the container networking layer.</p>
	~[moodle]Container schedulers and service discovery mechanisms, including load balancing.#<p>These are part of the container orchestration layer.</p>
	=[moodle]Networking gear, iptables, routing, IPVLAN, and Linux namespaces.
	~[moodle]Software-Defined Networking (SDN) APIs for configuring networks programmatically.#<p>SDN is an umbrella term for network configuration using software, which can span multiple layers but is described separately from the low-level components.</p>
	####<p><strong>Explanation</strong>\: The low-level networking layer includes networking gear, iptables, routing, IPVLAN, and Linux namespaces.</p>
}

// question: 1.5  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>What is the primary function of the container networking layer in the overall container networking stack?</p>{
	~[moodle]To manage the lifecycle of containers by making scheduling decisions and performing health checks.#<p>This describes the container orchestration layer.</p>
	=[moodle]To provide abstractions such as single-host bridge networking and multi-host, IP-per-container solutions.
	~[moodle]To configure networks using software via APIs and complementing network function virtualization.#<p>This relates to Software-Defined Networking (SDN).</p>
	~[moodle]To include basic networking hardware like physical routers, switches, and network cables.#<p>This would be part of the low-level networking layer.</p>
	####<p><strong>Explanation</strong>\: The container networking layer provides some abstractions, such as the single-host bridge networking mode and the multi-host, IP-per-container solution.</p>
}

// question: 1.6  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>Which layer in the container networking stack is responsible for marrying the container scheduler’s decisions with lower layer primitives and includes service discovery and load balancing?</p>{
	~[moodle]The low-level networking layer, which deals with physical networking hardware and kernel features.#<p>The low-level layer is about foundational components like iptables and namespaces.</p>
	~[moodle]The container networking layer, providing single-host and multi-host network abstractions.#<p>The container networking layer provides abstractions like bridge and multi-host IP-per-container.</p>
	=[moodle]The container orchestration layer, which focuses on scheduling, service discovery, and load balancing.
	~[moodle]The Software-Defined Networking (SDN) layer, which allows network configuration through APIs.#<p>SDN is a broader concept for configuring networks via software, not a specific layer in this context.</p>
	####<p><strong>Explanation</strong>\: The container orchestration layer marries the container scheduler’s decisions on where to place a container with primitives from lower layers. It includes service discovery and load balancing.</p>
}

// question: 1.7  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>What is Software-Defined Networking (SDN) described as in the context of the container networking stack?</p>{
	~[moodle]A specific hardware component that optimizes network performance for containerized applications.#<p>SDN is about configuring networks using software, not a hardware component.</p>
	=[moodle]An umbrella marketing term that provides advantages to networks similar to what virtual machines introduced over bare-metal servers.
	~[moodle]A standard protocol for secure communication between containers across different physical machines.#<p>While security is a concern, SDN is not defined as a standard communication protocol.</p>
	~[moodle]A low-level kernel feature that ensures network isolation for each individual container within a host.#<p>Network isolation is achieved through Linux kernel features like namespaces, not directly by SDN as an umbrella term.</p>
	####<p><strong>Explanation</strong>\: SDN is described as an umbrella (marketing) term, providing essentially the same advantages to networks that virtual machines introduced over bare-metal servers.</p>
}

// question: 1.8  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>When considering a "Simple" stage of container deployment, what is the typical setup and what are the use cases?</p>{
	~[moodle]Bare metal or VM, with no containers, used for the majority of today's production deployments.#<p>This describes the "Traditional" stage.</p>
	=[moodle]Manually launched containers used for app-level dependency management, typically in development and test environments.
	~[moodle]A custom, homegrown scheduler to launch and potentially restart containers, as seen with companies like RelateIQ.#<p>This describes the "Ad hoc" stage.</p>
	~[moodle]An established scheduler from Chapter 4 to manage containers, offering fault tolerance and self-healing capabilities.#<p>This describes the "Full-blown" stage.</p>
	####<p><strong>Explanation</strong>\: In the "Simple" stage, the typical setup involves manually launched containers used for app-level dependency management, often in development and test environments.</p>
}

// question: 1.9  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>What does the source recommend reading up on if one is dealing with distributed systems in general, especially when deploying containers into a network of computers?</p>{
	~[moodle]The principles of object-oriented programming for microservices architectures.#<p>While relevant to application design, this is not the specific recommendation for understanding distributed systems themselves.</p>
	=[moodle]The fallacies of distributed computing, if not already familiar with the topic.
	~[moodle]The latest advancements in quantum computing for improved network security.#<p>This is a future technology not directly addressed by the recommendation.</p>
	~[moodle]The history of the internet and the evolution of network protocols.#<p>This is background knowledge, but not the specific recommendation provided.</p>
	####<p><strong>Explanation</strong>\: The source suggests reading up on the fallacies of distributed computing, given that deploying containers often involves distributed systems.</p>
}

// question: 1.10  name: Chapter 1: Motivation
::Chapter 1\: Motivation::[html]<p>Which of the following statements about the motivation for container networking is true?</p>{
	~[moodle]Container networking is a trivial aspect that automatically configures itself when using Docker.#<p>The book itself highlights the challenges, indicating it's not trivial.</p>
	=[moodle]Without a proper understanding of container networking and a sound strategy, one will likely encounter significant challenges.
	~[moodle]The field of container networking and service discovery is already mature and highly standardized, with few changes expected.#<p>The author notes that "The space of container networking and service discovery is still relatively young".</p>
	~[moodle]Container networking primarily focuses on optimizing hardware performance, rather than connectivity.#<p>The book is about "networking", which is about connectivity, not primarily hardware performance optimization.</p>
	####<p><strong>Explanation</strong>\: The author states that "Without a proper understanding of the networking aspect of (Docker) containers and a sound strategy in place, you will have more than one bad day when adopting containers".</p>
}

// Chapter 2: Introduction to Container Networking

// question: 2.1  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>In a Docker container environment, what is the typical relationship between a host and the containers running on it?</p>{
	~[moodle]A single container usually runs on multiple hosts simultaneously for redundancy.#<p>Containers are typically scaled horizontally by running more containers on more hosts, not by running a single container across multiple hosts.</p>
	=[moodle]One host typically has several containers running on it, with an average of 10 to 40 containers.
	~[moodle]Each host is dedicated to running only one container to ensure maximum isolation and performance.#<p>This contradicts the common practice of running multiple containers per host to maximize resource utilization.</p>
	~[moodle]Hosts and containers always have a one-to-one relationship to simplify network management.#<p>The source explicitly states a 1:N relationship, where N is usually greater than one.</p>
	####<p><strong>Explanation</strong>\: The relationship between a host and containers is 1:N, meaning one host typically has several containers running on it. For example, Facebook reports an average of 10 to 40 containers per host.</p>
}

// question: 2.2  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>For single-host Docker deployments, what is the default network driver used for applications running in standalone containers?</p>{
	~[moodle]Host mode, which removes network isolation to the host.#<p>Host mode is an alternative, not the default.</p>
	=[moodle]Bridge mode, where the Docker daemon creates a virtual Ethernet bridge.
	~[moodle]Container mode, which reuses the network namespace of another container.#<p>Container mode is for reusing another container's network namespace.</p>
	~[moodle]No networking mode, which disables all external network connectivity.#<p>No networking explicitly turns off networking.</p>
	####<p><strong>Explanation</strong>\: Bridge mode is the default network driver, usually used for apps running in standalone containers.</p>
}

// question: 2.3  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>What is a key characteristic of Host mode networking in Docker?</p>{
	~[moodle]The container operates on a completely isolated network stack, independent of the host.#<p>This is the opposite of host mode, which removes network isolation.</p>
	=[moodle]The container shares the network namespace of the host, meaning it has the same IP address as the host.
	~[moodle]The container is assigned a unique virtual IP address, which is then translated by a NAT gateway for external access.#<p>This is more characteristic of bridge mode where containers get private IPs, but host mode explicitly shares the host's IP.</p>
	~[moodle]The container automatically creates its own virtual Ethernet bridge for internal communication, separate from the host.#<p>Bridge mode creates a virtual Ethernet bridge, not host mode.</p>
	####<p><strong>Explanation</strong>\: Host mode effectively disables network isolation, allowing the container to share the network namespace of the host and inherit its IP address.</p>
}

// question: 2.4  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>When using Bridge mode networking in Docker, what happens if the -P argument (publishes all exposed ports) or -p <host_port>:<container_port> (publishes a specific port) is not used?</p>{
	~[moodle]The container will automatically use the host's network stack, similar to host mode.#<p>This is the behavior of host mode, not bridge mode without port publishing.</p>
	=[moodle]The IP packets will not be routable to the container from outside of the host.
	~[moodle]Docker will create a new virtual network for the container, completely isolated from the host.#<p>Bridge mode connects containers to an internal network, but the issue is external routability without publishing ports.</p>
	~[moodle]The container will still be accessible via its assigned IP address, but only within the Docker daemon's internal network.#<p>The container is accessible within the internal network, but the key point is the lack of routability outside the host without publishing.</p>
	####<p><strong>Explanation</strong>\: If you do not use the -P or -p arguments, the IP packets will not be routable to the container outside of the host.</p>
}

// question: 2.5  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>What is the primary use case for Container mode networking in Docker, where one container reuses the network namespace of another?</p>{
	~[moodle]To automatically scale the container horizontally across multiple physical hosts.#<p>Container mode is a single-host networking concept, not for multi-host scaling.</p>
	~[moodle]To create a completely isolated environment for batch jobs that do not require network access.#<p>This describes the "No networking" mode.</p>
	=[moodle]To gain fine-grained control over the network stack and manage its lifecycle, as used in Kubernetes.
	~[moodle]To encrypt all network traffic between the two containers for enhanced security.#<p>Container mode reuses a network namespace, it does not inherently provide encryption.</p>
	####<p><strong>Explanation</strong>\: Container mode is useful for fine-grained control over the network stack and its lifecycle, and is used in Kubernetes networking.</p>
}

// question: 2.6  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>When using the No networking mode, for what two main cases is it useful?</p>{
	~[moodle]For containers that need to share the host's IP address directly, like web servers.#<p>This describes host mode.</p>
	=[moodle]For containers that do not require network access (e.g., batch jobs writing to disk) or when setting up custom networking.
	~[moodle]For creating a virtual Ethernet bridge that forwards packets between containers on the same host.#<p>This describes bridge mode.</p>
	~[moodle]For allowing containers to communicate with each other using service names instead of IP addresses.#<p>This is typically a feature of custom bridge networks or orchestrators with DNS.</p>
	####<p><strong>Explanation</strong>\: The "No networking" mode is useful for containers that don't need a network (e.g., batch jobs writing to a disk volume) or if you want to set up your own custom networking.</p>
}

// question: 2.7  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>What is one of the key administrative considerations regarding network security in Docker, particularly concerning inter-container communication?</p>{
	~[moodle]Docker containers are inherently secure and do not require any additional security configurations by default.#<p>The source indicates that security policies need to be reflected in the Docker daemon setup due to default settings.</p>
	~[moodle]Docker automatically enables on-the-wire encryption (TLS/SSL) for all inter-container communication by default.#<p>On-the-wire encryption (TLS/SSL) is a separate network security aspect, not a default behavior for inter-container communication.</p>
	=[moodle]Inter-container communication is enabled by default, meaning containers on a host can communicate without restrictions, which can lead to attacks.
	~[moodle]Docker explicitly blocks all inter-container communication unless it is manually configured and whitelisted by the user.#<p>The default is icc=true, meaning communication is enabled, not blocked.</p>
	####<p><strong>Explanation</strong>\: Out of the box, Docker has inter-container communication enabled (--icc=true by default), which means containers on a host can communicate without restrictions and potentially lead to denial-of-service attacks.</p>
}

// question: 2.8  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>Why is manually allocating IP addresses unsustainable when containers frequently come and go in large numbers?</p>{
	~[moodle]Because each container is automatically assigned a fixed, public IP address by Docker, which cannot be changed.#<p>Containers typically get private IPs in bridge mode, and the issue is dynamic allocation, not fixed public IPs.</p>
	~[moodle]Because Docker's bridge mode automatically handles IP address allocation, making manual intervention unnecessary.#<p>While bridge mode helps, the question is why manual allocation is unsustainable, pointing to the dynamic nature.</p>
	~[moodle]Because it prevents ARP collisions on the local network, which are handled by Docker generating MAC addresses.#<p>This is a feature of Docker's IP allocation in bridge mode, not a reason why manual allocation is unsustainable.</p>
	=[moodle]Because the dynamic nature of container lifecycles makes it impractical to keep track of and assign IPs manually.
	####<p><strong>Explanation</strong>\: Manually allocating IP addresses when containers come and go frequently and in large numbers is not sustainable.</p>
}

// question: 2.9  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>What is the basic idea behind using a distributed system (for computation or storage)?</p>{
	~[moodle]To centralize all data on a single, powerful machine to ensure consistent access.#<p>Distributed systems aim to distribute data and computation, not centralize them.</p>
	=[moodle]To benefit from parallel processing, usually together with data locality, and gain fault tolerance.
	~[moodle]To manually manage all network connections between individual compute nodes for optimal control.#<p>Distributed systems often employ automation for network management, not manual control.</p>
	~[moodle]To avoid the complexities of inter-container communication by strictly isolating each container.#<p>While isolation is a concept, distributed systems inherently involve communication and cooperation between components.</p>
	####<p><strong>Explanation</strong>\: The basic idea behind using a distributed system is to benefit from parallel processing, usually together with data locality, and to gain fault tolerance.</p>
}

// question: 2.10  name: Chapter 2: Introduction to Container Networking
::Chapter 2\: Introduction to Container Networking::[html]<p>How does Docker's dockerd program facilitate interaction with a container registry for single-host deployments?</p>{
	~[moodle]It bypasses the need for a container registry by storing images directly on the host's filesystem.#<p>While images are stored locally after pulling, the registry is essential for distribution and sharing.</p>
	=[moodle]It acts as the core daemon that runs on the host, enabling pulling and pushing of container images.
	~[moodle]It only manages running containers and does not directly interact with image registries.#<p>The daemon is explicitly mentioned as enabling interaction with the registry.</p>
	~[moodle]It provides a graphical user interface (GUI) for browsing and selecting images from various registries.#<p>dockerd is a backend program, not a GUI. The client (docker-cli) provides the command-line interface.</p>
	####<p><strong>Explanation</strong>\: The host has a daemon (dockerd) and a client running, enabling you to interact with a container registry and pull/push container images.</p>
}

// Chapter 3: Multi-Host Networking

// question: 3.1  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>When would you primarily need to consider multi-host container networking?</p>{
	~[moodle]When you want to ensure all containers run on a single, isolated physical server.#<p>This describes a single-host scenario, which multi-host networking aims to move beyond.</p>
	=[moodle]When the capacity of a single host is insufficient for your workload or you require more resilience.
	~[moodle]When you need to manually allocate static IP addresses to each container for better control.#<p>Manual IP allocation is unsustainable in dynamic container environments, and multi-host solutions aim to automate this.</p>
	~[moodle]When you are developing a batch job that has no external network dependencies.#<p>This is a use case for "No networking" mode on a single host, not multi-host networking.</p>
	####<p><strong>Explanation</strong>\: Multi-host networking is necessary if the capacity of a single host is not enough or when you want more resilience.</p>
}

// question: 3.2  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>Which of the following is not explicitly listed as an option for multi-host container networking in the source?</p>{
	~[moodle]Flannel by CoreOS.#<p>Flannel is listed.</p>
	=[moodle]Kubernetes' built-in networking.
	~[moodle]Weave Net by Weaveworks.#<p>Weave Net is listed.</p>
	~[moodle]Open vSwitch from the OpenStack project.#<p>Open vSwitch is listed.</p>
	####<p><strong>Explanation</strong>\: The source lists Flannel, Weave Net, Project Calico, Open vSwitch, OpenVPN, and Docker's native overlay networks as multi-host options. Kubernetes' networking is discussed in a separate chapter as a consumer of these, but not listed here as one of the "options for Multi-Host Container Networking" in the same category as the others. Kubernetes is an orchestrator that uses CNI, which these solutions often implement.</p>
}

// question: 3.3  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>What is the main purpose of flannel by CoreOS in multi-host container networking?</p>{
	~[moodle]To provide a high-performance HTTP reverse proxy for load balancing across containers.#<p>Load balancing is a different concept, often implemented by other tools.</p>
	=[moodle]To create a virtual network that assigns a subnet to each host, giving each container a unique, routable IP within the cluster.
	~[moodle]To encapsulate layer 2 traffic into a higher layer for secure communication over untrusted networks.#<p>Flannel supports backends like VXLAN, which involves encapsulation, but its main purpose is the subnet assignment.</p>
	~[moodle]To manage port allocations by dynamically assigning a single public port to all containers on a host.#<p>Flannel reduces the complexity of port mapping, but its core function is subnet assignment and routable IPs.</p>
	####<p><strong>Explanation</strong>\: Flannel is a virtual network that assigns a subnet to each host for use with container runtimes, ensuring each container (or pod) has a unique, routable IP inside the cluster.</p>
}

// question: 3.4  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>How does Project Calico differentiate itself from most other multi-host networking solutions?</p>{
	~[moodle]It primarily uses an overlay network by encapsulating layer 2 traffic into a higher layer.#<p>This describes what Calico contrasts with, not what it does primarily.</p>
	~[moodle]It assigns a random MAC address to each container for enhanced network isolation.#<p>This characteristic is more associated with macvlan.</p>
	=[moodle]It uses standard IP routing, specifically Border Gateway Protocol (BGP), to provide a layer 3 solution often without encapsulation.
	~[moodle]It creates a virtual switch that supports distribution across multiple physical servers, like Xen and KVM.#<p>This describes Open vSwitch.</p>
	####<p><strong>Explanation</strong>\: Project Calico uses standard IP routing (BGP) and networking tools to provide a layer 3 solution. In contrast, most other solutions build an overlay network by encapsulating layer 2 traffic into a higher layer.</p>
}

// question: 3.5  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>What did Docker 1.9 introduce that significantly changed multi-host networking capabilities?</p>{
	~[moodle]The deprecation of the docker network command, favoring external SDN solutions.#<p>The command was introduced, not deprecated.</p>
	=[moodle]A new docker network command, allowing containers to dynamically connect to different networks backed by various drivers.
	~[moodle]A mandatory requirement to use only the host network driver for multi-host deployments.#<p>The overlay driver became the default, not host mode.</p>
	~[moodle]The integration of a single, centralized key-value store to manage all network configurations globally.#<p>While it uses pluggable key-value stores, it's about the docker network command and driver flexibility, not a single centralized store for all configurations.</p>
	####<p><strong>Explanation</strong>\: Docker 1.9 introduced a new docker network command, with which containers can dynamically connect to other networks, each potentially backed by a different network driver.</p>
}

// question: 3.6  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>What is the Overlay Driver in Docker primarily used for in multi-host networking?</p>{
	~[moodle]To provide network isolation to a Docker container by reusing the host's network namespace.#<p>This describes Host mode.</p>
	=[moodle]To extend the normal bridge mode with peer-to-peer communication and distribute cluster state via a pluggable key-value store.
	~[moodle]To disable all network connectivity for containers, useful for batch jobs.#<p>This describes the "No networking" mode.</p>
	~[moodle]To manually assign a fixed IP address to each container from a predefined range.#<p>Overlay networking automates IP assignment, it doesn't rely on manual fixed IP assignment.</p>
	####<p><strong>Explanation</strong>\: The Overlay Driver extends the normal bridge mode with peer-to-peer communication and uses a pluggable key-value store backend (Consul, etcd, ZooKeeper) to distribute cluster state.</p>
}

// question: 3.7  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>What is IPVLAN, introduced in Linux kernel version 3.19, designed to achieve for containers?</p>{
	~[moodle]To create a separate virtual Ethernet bridge for each container on a single host.#<p>This is more descriptive of bridge mode networking.</p>
	=[moodle]To assign each container on a host a unique and routable IP address by creating multiple virtual network interfaces with different MAC addresses.
	~[moodle]To encapsulate all container network traffic, ensuring it cannot be inspected by the host system.#<p>While some solutions encapsulate, IPVLAN's primary goal is unique IP-per-container, not traffic encapsulation.</p>
	~[moodle]To provide a mechanism for containers to share a single MAC address, simplifying network configuration.#<p>IPVLAN creates multiple virtual network interfaces with different MAC addresses, not a shared one.</p>
	####<p><strong>Explanation</strong>\: IPVLAN assigns each container on a host a unique and routable IP address by taking a single network interface and creating multiple virtual network interfaces with different MAC addresses.</p>
}

// question: 3.8  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>What is one of the key challenges of IP address management (IPAM) in multi-host networking?</p>{
	~[moodle]Ensuring that all IP addresses are publicly routable across the internet.#<p>Containers often use private IPs, and the challenge is internal allocation and routability, not necessarily public routability.</p>
	~[moodle]Manually configuring DNS records for each container's IP address.#<p>IPAM is about the addresses themselves, while DNS is for name resolution.</p>
	=[moodle]Allocating IP addresses to containers in a cluster, either within the existing network or via an orthogonal networking layer.
	~[moodle]Eliminating the need for any IP addresses by using service names for all container communication.#<p>Containers still require IP addresses; service names abstract these for applications but don't eliminate the underlying IPs.</p>
	####<p><strong>Explanation</strong>\: One of the key challenges of multi-host networking is the allocation of IP addresses to containers in a cluster, with strategies including integrating into existing networks or spawning an overlay network.</p>
}

// question: 3.9  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>Why is it important to check for orchestration tool compatibility when selecting a multi-host networking solution?</p>{
	~[moodle]Because all multi-host networking solutions are exclusively designed to work with Docker Swarm.#<p>This is incorrect; many solutions work with various orchestrators.</p>
	=[moodle]Because many solutions are coprocesses wrapping the Docker API and configuring the network, so they must be compatible with your chosen orchestrator.
	~[moodle]Because different orchestration tools have varying hardware requirements for their networking components.#<p>While hardware requirements exist, the primary compatibility concern is with the orchestration tool's API and how it manages networks.</p>
	~[moodle]Because selecting an incompatible networking solution will automatically downgrade your Kubernetes cluster to Docker Compose.#<p>This is a false statement. Incompatibility would likely lead to networking failures, not a specific downgrade.</p>
	####<p><strong>Explanation</strong>\: Many multi-host networking solutions are effectively coprocesses wrapping the Docker API and configuring the network. Therefore, it's crucial to check for compatibility issues with the container orchestration tool you're using.</p>
}

// question: 3.10  name: Chapter 3: Multi-Host Networking
::Chapter 3\: Multi-Host Networking::[html]<p>What is a significant advantage that IPv6 could bring to Docker deployments in the future compared to IPv4?</p>{
	~[moodle]IPv6 will remove the need for any network configuration, as it is fully self-configuring.#<p>IPv6 simplifies some aspects but doesn't eliminate all network configuration.</p>
	=[moodle]IPv6 is witnessing some uptake and could relax the IP address shortage, potentially getting rid of network address translation (NAT).
	~[moodle]IPv6 will only work with bare-metal servers, providing superior performance over virtualized environments.#<p>IPv6 works with various environments, not just bare-metal.</p>
	~[moodle]IPv6 automatically encrypts all network traffic, making all other security measures redundant.#<p>IPv6 does not inherently encrypt all network traffic; encryption is a separate security layer.</p>
	####<p><strong>Explanation</strong>\: IPv6 is witnessing some uptake, and the ever-growing address shortage in IPv4-land might encourage more IPv6 deployments down the line, also getting rid of network address translation (NAT).</p>
}

// Chapter 4: Orchestration

// question: 4.1  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>What is the primary role of an orchestrator in managing the life cycle of containers?</p>{
	~[moodle]To manually assign specific machines for running particular applications.#<p>This is contrary to the cattle approach, where manual allocation is avoided.</p>
	=[moodle]To manage the life cycle of containers, automatically scheduling them on available hosts.
	~[moodle]To only perform automated health checks without intervening in container placement.#<p>Health checks are a function, but the primary role is broader, including scheduling.</p>
	~[moodle]To provide a static mapping between application names and their fixed IP addresses.#<p>Orchestrators deal with dynamic, not static, mappings, and often integrate with service discovery.</p>
	####<p><strong>Explanation</strong>\: With the cattle approach, you leave it up to an orchestrator to manage the life cycle of your containers, including scheduling them on a host.</p>
}

// question: 4.2  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>Which of the following is considered an "organizational primitive" provided by container orchestration systems like Kubernetes?</p>{
	~[moodle]Manual configuration files to define network routes.#<p>Configuration files are part of setup, but labels are the primitive for organization.</p>
	=[moodle]Labels to query and group containers based on various criteria.
	~[moodle]Physical network interfaces used for inter-container communication.#<p>These are low-level networking components.</p>
	~[moodle]Dedicated virtual machines for each container to ensure isolation.#<p>Orchestration aims to use containers, not necessarily VMs per container.</p>
	####<p><strong>Explanation</strong>\: Organizational primitives, such as labels in Kubernetes, are used to query and group containers.</p>
}

// question: 4.3  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>What is the relationship between service discovery and scheduling in container orchestration?</p>{
	~[moodle]Service discovery is an independent component that operates without any input from the scheduler.#<p>They are inherently linked, not independent.</p>
	=[moodle]They are two sides of the same coin; the scheduler decides placement, and service discovery maps containers to locations.
	~[moodle]Scheduling is solely responsible for resource allocation, while service discovery is only for external application access.#<p>Scheduling includes placement, and service discovery is for both internal and external access.</p>
	~[moodle]Service discovery primarily focuses on persistent storage, whereas scheduling is about ephemeral workloads.#<p>This misrepresents the focus of both concepts.</p>
	####<p><strong>Explanation</strong>\: Service discovery and scheduling are really two sides of the same coin. The scheduler decides where a container is placed and supplies other parts with an up-to-date mapping in the form of containers to locations.</p>
}

// question: 4.4  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>As of early 2018, what is considered the de facto container orchestration standard?</p>{
	~[moodle]Docker Swarm.#<p>This is an alternative, but Kubernetes is stated as the de facto standard.</p>
	~[moodle]Apache Mesos.#<p>This is an alternative, but Kubernetes is stated as the de facto standard.</p>
	~[moodle]HashiCorp Nomad.#<p>This is an alternative, but Kubernetes is stated as the de facto standard.</p>
	=[moodle]Kubernetes.
	####<p><strong>Explanation</strong>\: As of early 2018, the industry has standardized on Kubernetes as the portable way of doing container orchestration.</p>
}

// question: 4.5  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>What is the primary function of the scheduler in a distributed system context for containerized workloads?</p>{
	~[moodle]To manually configure network routes and firewall rules for each container.#<p>Network configuration is typically handled by networking layers and drivers, not primarily the scheduler.</p>
	=[moodle]To take an application requested by a user and place it on one or more of the available hosts.
	~[moodle]To solely monitor the health of running containers and restart them if they fail.#<p>Health checks and restarts are part of orchestration, but scheduling is about initial placement.</p>
	~[moodle]To provide a static inventory of all available compute resources in the cluster.#<p>It uses knowledge of cluster state, which includes resource inventory, but its function is placement, not just inventory.</p>
	####<p><strong>Explanation</strong>\: A scheduler for a distributed system takes an application (binary or container image) as requested by a user and places it on one or more of the available hosts.</p>
}

// question: 4.6  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>Since Docker 1.12, what has been integrated with Docker Engine for orchestration features in a distributed setting?</p>{
	~[moodle]Standalone Docker Swarm.#<p>Standalone Docker Swarm was used previous to Docker 1.12.</p>
	=[moodle]Swarm Mode, built using SwarmKit.
	~[moodle]Apache Mesos frameworks.#<p>Apache Mesos is a separate orchestrator.</p>
	~[moodle]HashiCorp Nomad agents.#<p>HashiCorp Nomad is also a separate orchestrator.</p>
	####<p><strong>Explanation</strong>\: Since Docker 1.12, swarm mode has been integrated with Docker Engine, with orchestration features built using SwarmKit.</p>
}

// question: 4.7  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>What is the essential difference between standalone containers and swarm services in Docker's swarm mode?</p>{
	~[moodle]Standalone containers are fault-tolerant and self-healing, while swarm services are not.#<p>Swarm services are designed for desired state maintenance and fault tolerance.</p>
	=[moodle]Only swarm managers can manage a swarm, while standalone containers can be started on any host.
	~[moodle]Swarm services offer greater network isolation, whereas standalone containers always share the host's network.#<p>Network isolation depends on the network driver used, not inherently on whether it's a standalone or swarm service.</p>
	~[moodle]Standalone containers are deployed with a declarative YAML file, while swarm services require manual command-line execution.#<p>Swarm services are defined, but the method of deployment (e.g., CLI or Compose files) is not the fundamental difference described.</p>
	####<p><strong>Explanation</strong>\: The essential difference is that only swarm managers can manage a swarm, while standalone containers can be started on any host.</p>
}

// question: 4.8  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>What is Apache Mesos described as?</p>{
	~[moodle]A simple container runtime that only supports Docker containers.#<p>Mesos supports both containerized workloads and plain executables, and is a resource manager, not just a runtime.</p>
	=[moodle]A general-purpose cluster resource manager that abstracts cluster resources like CPU and RAM.
	~[moodle]A dedicated orchestrator exclusively for long-running web servers.#<p>Mesos is used with "frameworks" like Marathon for long-running services, but it's a general-purpose manager itself.</p>
	~[moodle]A proprietary cloud platform for managing containerized applications.#<p>Mesos is an open-source project.</p>
	####<p><strong>Explanation</strong>\: Apache Mesos is a general-purpose cluster resource manager that abstracts the resources of a cluster (CPU, RAM, etc.).</p>
}

// question: 4.9  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>How does HashiCorp Nomad ensure state replication and automatic clustering?</p>{
	~[moodle]By relying solely on manual configuration files for cluster state.#<p>Nomad uses HCL or JSON for job definitions, but not solely for state replication.</p>
	=[moodle]By using a consensus protocol for state replication and a gossip protocol for automatic clustering and multi-region federation.
	~[moodle]By integrating with a centralized external database for all state management.#<p>It uses internal protocols, not an external database.</p>
	~[moodle]By requiring operators to periodically synchronize cluster state across all nodes.#<p>It automates state management through its protocols.</p>
	####<p><strong>Explanation</strong>\: Nomad makes use of both a consensus protocol (strongly consistent) for all state replication and scheduling, and a gossip protocol used to manage the addresses of servers for automatic clustering and multi-region federation.</p>
}

// question: 4.10  name: Chapter 4: Orchestration
::Chapter 4\: Orchestration::[html]<p>According to the source, what is a key consideration when selecting an orchestration system, beyond its technical features?</p>{
	~[moodle]The specific programming language used to develop the orchestrator.#<p>The language is not listed as a key indicator for selection.</p>
	~[moodle]The historical performance benchmarks of the orchestrator from prior years.#<p>While performance is important, community activity is highlighted as a distinct selection criterion.</p>
	=[moodle]The size and activity of the community behind and around the orchestrator.
	~[moodle]The geographical location of the orchestrator's primary development team.#<p>This is not mentioned as a key indicator.</p>
	####<p><strong>Explanation</strong>\: An important aspect to consider when selecting an orchestration system is the community behind and around it, including indicators like governance, mailing list activity, and independent providers.</p>
}

// Chapter 5: Service Discovery

// question: 5.1  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>What is the core challenge that service discovery addresses in the context of containers and the "cattle approach"?</p>{
	~[moodle]How to manually configure port mappings for each container on a single host.#<p>Service discovery aims to automate this, not manually configure.</p>
	=[moodle]How to reliably maintain a mapping between a running container and its location (IP address and port) across the cluster.
	~[moodle]How to enforce strict network isolation between all containers to prevent unauthorized access.#<p>Network isolation is a security aspect, not the core challenge of service discovery.</p>
	~[moodle]How to automatically generate Dockerfiles for new applications deployed in the cluster.#<p>This is about image building, not service discovery.</p>
	####<p><strong>Explanation</strong>\: The challenge of service discovery boils down to reliably maintaining a mapping between a running container and its location (IP address and port) in a timely and accurate manner across relaunches of the container throughout the cluster.</p>
}

// question: 5.2  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>What are the two distinct operations that must be supported by a container service discovery solution?</p>{
	~[moodle]Authentication and Authorization.#<p>These are other important aspects of distributed systems, but not the two distinct operations defined for service discovery.</p>
	=[moodle]Registration and Lookup.
	~[moodle]Encryption and Decryption.#<p>These are other important aspects of distributed systems, but not the two distinct operations defined for service discovery.</p>
	~[moodle]Monitoring and Alerting.#<p>These are other important aspects of distributed systems, but not the two distinct operations defined for service discovery.</p>
	####<p><strong>Explanation</strong>\: Two distinct operations must be supported by a container service discovery solution: Registration (establishes container -> location mapping) and Lookup (enables other services to find the mapping).</p>
}

// question: 5.3  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>What is Apache ZooKeeper primarily used for in the context of service discovery?</p>{
	~[moodle]As a high-performance HTTP reverse proxy for load balancing.#<p>HAProxy is used with ZooKeeper, but ZooKeeper itself is not the proxy.</p>
	=[moodle]As a JVM-based, centralized tool for configuration management, using a hierarchy of znodes.
	~[moodle]As a pure-play DNS server that polls for running tasks and exposes IP/port info.#<p>This describes Mesos-DNS or SkyDNS.</p>
	~[moodle]As a client-side load balancer with built-in round-robin capabilities.#<p>This describes a feature of Netflix's Eureka client.</p>
	####<p><strong>Explanation</strong>\: Apache ZooKeeper is a JVM-based, centralized tool for configuration management, organizing data in a hierarchy of znodes.</p>
}

// question: 5.4  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>What is etcd described as in the context of service discovery?</p>{
	~[moodle]A bespoke system developed at Netflix for locating services in an AWS environment.#<p>This describes Netflix's Eureka.</p>
	=[moodle]A lightweight, distributed key-value store written in Go, using the Raft algorithm for consensus.
	~[moodle]A daemon that automatically configures HAProxy instances deployed on Apache Mesos.#<p>This describes Bamboo.</p>
	~[moodle]A network plug-in for failover and high availability of networking in cloud-native environments.#<p>This describes the Bonding CNI plug-in.</p>
	####<p><strong>Explanation</strong>\: etcd, a product of CoreOS, is a lightweight, distributed key-value store written in Go that uses the Raft algorithm for consensus.</p>
}

// question: 5.5  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>What are the two main ways Consul allows services to be queried?</p>{
	~[moodle]Through a proprietary binary protocol and a command-line interface.#<p>While a CLI exists, these are not the two main query methods specified.</p>
	=[moodle]Using the HTTP API or through DNS.
	~[moodle]Via environment variables and shared memory segments.#<p>These are not the primary query mechanisms for Consul.</p>
	~[moodle]Directly by accessing the host's /etc/hosts file.#<p>These are not the primary query mechanisms for Consul.</p>
	####<p><strong>Explanation</strong>\: Services in Consul can be queried using the HTTP API or through DNS.</p>
}

// question: 5.6  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>What is the primary characteristic of a pure-play DNS-based solution for service discovery, such as Mesos-DNS?</p>{
	~[moodle]It relies on a distributed key-value store like etcd for all its service definitions.#<p>SkyDNS uses etcd, but Mesos-DNS polls the Mesos master.</p>
	~[moodle]It's often used when strong consistency is prioritized over eventual consistency for service lookups.#<p>The eventual consistency of DNS is noted as a characteristic, implying it doesn't prioritize strong consistency.</p>
	=[moodle]It leverages the DNS system's eventual consistency and SRV records for service lookups.
	~[moodle]It requires manual updates of DNS records for every container lifecycle event.#<p>Mesos-DNS polls the Mesos master for running tasks, automating updates.</p>
	####<p><strong>Explanation</strong>\: Pure-play DNS-based solutions like Mesos-DNS use the eventual consistency of the DNS system and rely on SRV records for service lookups.</p>
}

// question: 5.7  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>What is the primary goal of load balancing in the context of containers and microservices?</p>{
	~[moodle]To enforce strict adherence to security policies and access controls.#<p>Security is a separate concern, not the primary goal of load balancing.</p>
	=[moodle]To spread the inbound service requests across multiple containers to maximize throughput and minimize response time.
	~[moodle]To provide a static mapping of service names to their physical IP addresses within the cluster.#<p>This is a function of service discovery, not load balancing directly.</p>
	~[moodle]To automatically scale the number of running containers based on CPU utilization.#<p>Autoscaling is related but distinct from the core function of load balancing, which is distributing requests.</p>
	####<p><strong>Explanation</strong>\: Load balancing enables you to spread the load (inbound service requests) across a number of containers to maximize throughput, minimize response time, and avoid hot-spotting.</p>
}

// question: 5.8  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>Which load balancing option is described as a high-performance distributed proxy written in C++, originally built at Lyft, and is the default data plane in Istio?</p>{
	~[moodle]HAProxy.#<p>HAProxy is a stable and mature workhorse, but not built at Lyft or the default data plane in Istio.</p>
	~[moodle]NGINX.#<p>NGINX is a leading solution but is a web server and reverse proxy, not specifically described this way.</p>
	=[moodle]Envoy.
	~[moodle]MetalLB.#<p>MetalLB is a load-balancer for bare-metal Kubernetes clusters.</p>
	####<p><strong>Explanation</strong>\: Envoy is described as a high-performance distributed proxy written in C++, originally built at Lyft, and is the default data plane in Istio.</p>
}

// question: 5.9  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>What is kube-proxy's role in Kubernetes, specifically regarding service IPs?</p>{
	=[moodle]It runs on each node and updates service IPs, supporting simple TCP/UDP forwarding and round-robin load balancing.
	~[moodle]It provides external load balancing to expose services to the public internet.#<p>kube-proxy is for cluster-internal load balancing, not primarily external exposure, which is handled by NodePort, LoadBalancer, or Ingress.</p>
	~[moodle]It acts as a client-side load balancer that automatically discovers backend pods.#<p>It's a node-level proxy, not a client-side load balancer.</p>
	~[moodle]It is a deprecated component, replaced by newer service mesh technologies.#<p>kube-proxy is a core component of Kubernetes networking.</p>
	####<p><strong>Explanation</strong>\: kube-proxy runs on each node of a Kubernetes cluster and updates services IPs. It supports simple TCP/UDP forwarding and round-robin load balancing, and is for cluster-internal load balancing.</p>
}

// question: 5.10  name: Chapter 5: Service Discovery
::Chapter 5\: Service Discovery::[html]<p>How does Netflix's Eureka differ from ZooKeeper, etcd, or Consul in its consistency model?</p>{
	~[moodle]Eureka favors strong consistency, ensuring all clients always receive the most up-to-date service information.#<p>This is the opposite of Eureka's design choice.</p>
	=[moodle]Eureka maintains eventual consistency, prioritizing service availability over strong consistency and leaving stale reads to the client.
	~[moodle]Eureka uses a two-phase commit protocol to guarantee atomicity across its distributed service registries.#<p>Eureka replicates asynchronously and prioritizes availability, not a two-phase commit for strong consistency.</p>
	~[moodle]Eureka implements a gossip protocol to achieve eventual consistency while still providing strong consistency for critical metadata.#<p>It favors availability over strong consistency; while gossip protocols can achieve eventual consistency, the key is the explicit trade-off.</p>
	####<p><strong>Explanation</strong>\: In contrast to ZK, etcd, or Consul, Eureka favors service availability over strong consistency; it leaves it up to the client to deal with stale reads, but has the upside of being more resilient in case of networking partitions.</p>
}

// Chapter 6: The Container Network Interface

// question: 6.1  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>What does the Container Network Interface (CNI) primarily provide for containers and container orchestrators?</p>{
	~[moodle]A dedicated hardware module for accelerated network processing.#<p>CNI is a software interface, not a hardware module.</p>
	=[moodle]A plug-in-oriented networking solution consisting of a specification and libraries for writing network plug-ins.
	~[moodle]A proprietary Docker-specific networking model called libnetwork.#<p>libnetwork is Docker's proprietary approach, which CNI contrasts with.</p>
	~[moodle]A centralized database for storing all network configurations and routing tables.#<p>While CNI deals with network configuration, it's not described as a centralized database.</p>
	####<p><strong>Explanation</strong>\: CNI provides a plug-in-oriented networking solution for containers and container orchestrators, consisting of a specification and libraries for writing plug-ins.</p>
}

// question: 6.2  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>CNI was pioneered by which company in the context of the container runtime rkt?</p>{
	~[moodle]Docker Inc.#<p>Docker initially planned to support CNI but then developed libnetwork.</p>
	~[moodle]Red Hat.#<p>This company is involved with container technology and Kubernetes, but CoreOS pioneered CNI.</p>
	=[moodle]CoreOS.
	~[moodle]Google.#<p>This company is involved with container technology and Kubernetes, but CoreOS pioneered CNI.</p>
	####<p><strong>Explanation</strong>\: CNI was pioneered by CoreOS in the context of the container runtime rkt.</p>
}

// question: 6.3  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>What is the CNI definition of a "Container"?</p>{
	~[moodle]Any physical machine that hosts containerized applications.#<p>CNI's container definition is a software concept, not a physical machine.</p>
	=[moodle]A Linux network namespace, with the specific unit depending on the runtime implementation.
	~[moodle]A virtual machine that runs a single application in complete isolation.#<p>This is a VM, not a container as defined by CNI.</p>
	~[moodle]A tightly coupled set of one or more applications that share resources.#<p>While pods are tightly coupled, the CNI definition focuses on the underlying network namespace.</p>
	####<p><strong>Explanation</strong>\: In the context of CNI, a "Container" is synonymous with a Linux network namespace, with the unit corresponding to either a single container or a pod, depending on the runtime.</p>
}

// question: 6.4  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>What is the CNI definition of a "Network"?</p>{
	~[moodle]A collection of physical networking devices like routers and switches.#<p>This describes hardware components, not CNI's abstract definition of a network.</p>
	=[moodle]A uniquely addressable group of entities (containers, machines, or other network devices) that can communicate.
	~[moodle]A software application that manages IP address allocation for an entire datacenter.#<p>This is a function of an IPAM plug-in, not the definition of a network.</p>
	~[moodle]A security policy that restricts communication between different containerized applications.#<p>Security policies are a separate concern from the definition of a network itself.</p>
	####<p><strong>Explanation</strong>\: In the context of CNI, a "Network" is defined as a uniquely addressable group of entities that can communicate with one another. These entities might include individual containers, machines, or other network devices.</p>
}

// question: 6.5  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>What are the three operations defined by the current version of CNI?</p>{
	~[moodle]Start container, stop container, pause container.#<p>These are container lifecycle operations, not CNI-specific networking operations.</p>
	=[moodle]Add container to networks, delete container from network, report CNI version.
	~[moodle]Create network, delete network, list networks.#<p>While related to network management, these are not the container-specific operations defined by CNI.</p>
	~[moodle]Encrypt traffic, decrypt traffic, audit traffic.#<p>These are security functions, not CNI core operations.</p>
	####<p><strong>Explanation</strong>\: The current version of CNI defines the following operations: Add container to one or more networks, Delete container from network, and Report CNI version.</p>
}

// question: 6.6  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>What is the role of a dedicated IP Address Management (IPAM) plug-in in CNI?</p>{
	~[moodle]It is responsible for setting up network routes for the host system, not containers.#<p>IPAM is for container IPs, not host routes directly.</p>
	~[moodle]It assigns an IP address to the interface and sets up network routes relevant for the container.#<p>The CNI plug-in assigns the IP and sets up routes, but IPAM manages the range.</p>
	=[moodle]It takes care of the IP range management independently from the main CNI plug-in.
	~[moodle]It monitors the network traffic of containers for performance bottlenecks.#<p>Monitoring is a separate function, often handled by other tools.</p>
	####<p><strong>Explanation</strong>\: CNI defines a dedicated IP Address Management (IPAM) plug-in that takes care of the IP range management independently.</p>
}

// question: 6.7  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>Which component is responsible for creating a new network namespace for a container and then invoking one or more CNI plug-ins?</p>{
	~[moodle]The network gear.#<p>Network gear is hardware, not a software component that invokes plug-ins.</p>
	~[moodle]The CNI specification itself.#<p>The specification defines how it works, but doesn't perform the action.</p>
	=[moodle]The container runtime.
	~[moodle]The IP Address Management (IPAM) plug-in.#<p>IPAM manages IP ranges, it doesn't create namespaces or invoke CNI plug-ins directly.</p>
	####<p><strong>Explanation</strong>\: For CNI to add a container to a network, the container runtime must first create a new network namespace for the container and then invoke one or more of the defined plug-ins.</p>
}

// question: 6.8  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>Which of the following is not explicitly listed as a container orchestrator or runtime supporting CNI?</p>{
	~[moodle]Kubernetes.#<p>This is listed as supporting CNI.</p>
	~[moodle]Mesos.#<p>This is listed as supporting CNI.</p>
	=[moodle]Docker Swarm.
	~[moodle]Cloud Foundry.#<p>This is listed as supporting CNI.</p>
	####<p><strong>Explanation</strong>\: The source states that "pretty much every container orchestrator with the exception of Docker Swarm uses CNI". Kubernetes, Mesos, and Cloud Foundry are listed as supporting CNI.</p>
}

// question: 6.9  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>What is the primary function of the Cilium CNI plug-in?</p>{
	~[moodle]To create overlay networks using Open vSwitch for Kubernetes.#<p>This describes Linen.</p>
	=[moodle]To provide connectivity between containers, operating at layers 3/4 for networking/security and layer 7 for modern protocols.
	~[moodle]To manage a flat layer 3 network using standard IP routing and BGP.#<p>This describes Project Calico.</p>
	~[moodle]To assign a subnet to each host for use with container runtimes like rkt.#<p>This describes Flannel.</p>
	####<p><strong>Explanation</strong>\: Cilium is a BPF-based solution providing connectivity between containers, operating at layer 3/4 for networking and security services, and layer 7 to protect modern protocols like HTTP and gRPC.</p>
}

// question: 6.10  name: Chapter 6: The Container Network Interface
::Chapter 6\: The Container Network Interface::[html]<p>Which CNI plug-in is specifically designed for overlay networks with Open vSwitch?</p>{
	~[moodle]Calico.#<p>Calico manages a flat layer 3 network, and can work with overlays like Flannel, but Linen is specifically for Open vSwitch overlay.</p>
	~[moodle]Multus.#<p>Multus is a multi–plug-in environment.</p>
	=[moodle]Linen.
	~[moodle]Weave Net.#<p>Weave Net is a multi-host Docker network, also a CNI plug-in.</p>
	####<p><strong>Explanation</strong>\: Linen is a CNI plug-in designed for overlay networks with Open vSwitch.</p>
}

// Chapter 7: Kubernetes Networking

// question: 7.1  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>What are the three fundamental networking requirements that Kubernetes states for its networking solutions?</p>{
	=[moodle]Containers can communicate with all other containers without NAT; Nodes can communicate with all containers without NAT; The IP a container sees itself is the same IP as others see it.
	~[moodle]All containers must be assigned a public IP address; All nodes must be in the same subnet; All traffic must be encrypted end-to-end.#<p>These options contain incorrect or incomplete requirements compared to the source.</p>
	~[moodle]Kubernetes must provide a built-in SDN solution by default; No external network traffic is allowed; All containers must use the host network mode.#<p>These options contain incorrect or incomplete requirements compared to the source.</p>
	~[moodle]Services must use fixed DNS entries; Pods must communicate through a centralized proxy; Network policies must be configured manually for every deployment.#<p>These options contain incorrect or incomplete requirements compared to the source.</p>
	####<p><strong>Explanation</strong>\: Kubernetes states three fundamental requirements: Containers can communicate with all other containers without NAT; Nodes can communicate with all containers (and vice versa) without NAT; The IP a container sees itself is the same IP as others see it.</p>
}

// question: 7.2  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>What is the unit of scheduling in Kubernetes?</p>{
	~[moodle]A single container that runs an individual process.#<p>A container is part of a pod, but the pod is the scheduling unit.</p>
	~[moodle]A virtual machine that encapsulates an entire operating system.#<p>Kubernetes orchestrates containers, not virtual machines as its primary scheduling unit.</p>
	=[moodle]A pod, which is a tightly coupled set of one or more containers always collocated.
	~[moodle]A deployment, which defines a set of identical pods and their desired state.#<p>A deployment manages pods, but the pod itself is the unit of scheduling.</p>
	####<p><strong>Explanation</strong>\: The unit of scheduling in Kubernetes is a pod. Essentially, this is a tightly coupled set of one or more containers that are always collocated (scheduled onto a node as a unit).</p>
}

// question: 7.3  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>What is an "infrastructure container" in a Kubernetes pod responsible for?</p>{
	~[moodle]Running the main application logic and serving network requests.#<p>This is the role of the application containers, not the infra container.</p>
	=[moodle]Acquiring the pod’s IP, setting up the network namespace, and acting as the home for other containers' namespaces.
	~[moodle]Providing persistent storage for all other containers within the pod.#<p>Persistent storage is handled by Persistent Volumes, not the infra container.</p>
	~[moodle]Managing external ingress and egress traffic for the entire Kubernetes cluster.#<p>Ingress and Egress are cluster-level networking concepts, not managed by an individual infra container.</p>
	####<p><strong>Explanation</strong>\: Within a pod, an "infrastructure container" is the first container launched by the kubelet. It acquires the pod’s IP, sets up the network namespace, and all other containers in the pod then join its network and IPC namespace. Its sole purpose is to act as the home for the namespaces.</p>
}

// question: 7.4  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>How do all containers within a Kubernetes pod communicate with each other?</p>{
	~[moodle]They communicate through a centralized Kubernetes API server that routes traffic.#<p>The API server is for control plane interactions, not direct inter-container communication within a pod.</p>
	=[moodle]They communicate using localhost (or 127.0.0.1 in IPv4) because they share a network namespace.
	~[moodle]They are completely isolated from each other and cannot communicate directly.#<p>They are explicitly not completely isolated at the network level within a pod.</p>
	~[moodle]They use their individual, routable IP addresses assigned by the pod network.#<p>The pod gets one IP; containers within the pod share this and use localhost for internal communication.</p>
	####<p><strong>Explanation</strong>\: As a result of sharing the infra container's network namespace, all containers within a pod can communicate amongst each other using localhost (or 127.0.0.1 in IPv4).</p>
}

// question: 7.5  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>What is the primary purpose of a Kubernetes Service?</p>{
	=[moodle]To provide a stable virtual IP (VIP) address for a set of pods, allowing clients to reliably discover and connect to them.
	~[moodle]To manage the scaling of pods by automatically increasing or decreasing their replica count.#<p>Scaling is handled by controllers (e.g., Deployments), which services interact with, but it's not the primary purpose of the service itself.</p>
	~[moodle]To directly expose the host's physical network interface to all containers within a pod.#<p>Services provide network abstraction, not direct exposure to the host's interface.</p>
	~[moodle]To ensure that all containers within a pod run with elevated privileges for administrative tasks.#<p>Services are for network connectivity and discovery, not privilege management.</p>
	####<p><strong>Explanation</strong>\: A service provides a stable virtual IP (VIP) address for a set of pods. While pods may come and go, services allow clients to reliably discover and connect to the containers running in the pods by using the VIP.</p>
}

// question: 7.6  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>How does kube-proxy maintain the mapping between a Service's VIP and its target pods?</p>{
	~[moodle]It periodically reboots all nodes in the cluster to refresh network configurations.#<p>This is disruptive and not how kube-proxy operates.</p>
	=[moodle]It queries the API server to learn about new services and updates the node’s iptables rules accordingly.
	~[moodle]It broadcasts DNS queries across the network to discover the latest pod IP addresses.#<p>While DNS is used for service discovery, kube-proxy's mechanism is through API server queries and iptables.</p>
	~[moodle]It manually updates the /etc/hosts file on each node with the pod IPs.#<p>kube-proxy uses iptables rules, not /etc/hosts for dynamic routing.</p>
	####<p><strong>Explanation</strong>\: The kube-proxy process queries the API server to learn about new services in the cluster and updates the node’s iptables rules accordingly, to provide the necessary routing information.</p>
}

// question: 7.7  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>What are the two built-in service discovery mechanisms available in Kubernetes?</p>{
	~[moodle]Through a distributed key-value store and external load balancers.#<p>These are not the two built-in mechanisms mentioned for service discovery in Kubernetes.</p>
	=[moodle]Through environment variables and using DNS.
	~[moodle]Through manual IP address allocation and port mapping.#<p>These are not the two built-in mechanisms mentioned for service discovery in Kubernetes.</p>
	~[moodle]Through SSH tunnels and VPN connections.#<p>These are not the two built-in mechanisms mentioned for service discovery in Kubernetes.</p>
	####<p><strong>Explanation</strong>\: Conceptually, you can use one of the two built-in discovery mechanisms: through environment variables (limited) or using DNS (available cluster-wide if a respective DNS cluster add-on has been installed).</p>
}

// question: 7.8  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>What is the primary drawback of environment variables–based service discovery in Kubernetes?</p>{
	~[moodle]It requires all services to be publicly exposed to the internet.#<p>Environment variables provide internal discovery, not public exposure.</p>
	~[moodle]It only works for services running on the same physical host.#<p>It can work across hosts within the cluster, provided the service is created first.</p>
	=[moodle]Any service to be discovered must be created before the pod from which you want to discover it, otherwise variables won't be populated.
	~[moodle]It leads to significant network latency and reduced application performance due to overhead.#<p>The drawback is about variable population order, not performance.</p>
	####<p><strong>Explanation</strong>\: Discovery via environment variables has a fundamental drawback: any service that you want to discover must be created before the pod from which you want to discover it, otherwise the environment variables will not be populated by Kubernetes.</p>
}

// question: 7.9  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>What is Ingress in Kubernetes used for?</p>{
	~[moodle]Routing internal traffic between pods within the same namespace.#<p>This is inter-pod networking within the cluster.</p>
	=[moodle]Routing traffic from external users or applications into the cluster to a service.
	~[moodle]Controlling egress traffic from pods to external APIs.#<p>This is the definition of Egress.</p>
	~[moodle]Defining network policies to restrict inter-pod communication.#<p>This is the role of Network Policies.</p>
	####<p><strong>Explanation</strong>\: Ingress is used to route traffic from the external world to a service in the cluster, handling "North-South" traffic.</p>
}

// question: 7.10  name: Chapter 7: Kubernetes Networking
::Chapter 7\: Kubernetes Networking::[html]<p>What is the core idea behind using a service mesh like Istio or Conduit in Kubernetes?</p>{
	~[moodle]To manually configure each container's network interface for specific routing rules.#<p>Service meshes aim to automate and abstract away such manual configurations.</p>
	~[moodle]To centralize all application logs and metrics for easier debugging and monitoring.#<p>While they provide observability (including metrics and tracing), their scope is broader to control and secure traffic.</p>
	=[moodle]To outsource non-functional networking communication and control to the mesh, gaining traffic control, observability, and security without code changes.
	~[moodle]To deploy multiple applications within a single container to simplify resource management and reduce overhead.#<p>Service meshes are for managing communication between containers/pods, and running multiple apps in one container is generally not recommended.</p>
	####<p><strong>Explanation</strong>\: The idea of a service mesh is that instead of putting the burden of networking communication and control onto the developer, these nonfunctional things are outsourced to the mesh, benefiting from traffic control, observability, and security without code changes.</p>
}