////////////////////////////////////////////////////////////////////////////////
// Chapter 1: Introducing the Istio service mesh
////////////////////////////////////////////////////////////////////////////////

// question: 1.1  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>What is the primary role of a service mesh?</p>{
	~[moodle]To replace application business logic with network functions.#<p>Istio does not implement or replace any business logic; it facilitates taking complicated networking code out of the application.</p>
	=[moodle]To provide application-level network capabilities transparently and out-of-process.
	~[moodle]To simplify database management for microservices.#<p>The service mesh primarily deals with service-to-service communication, not database management.</p>
	~[moodle]To automatically generate microservice code from API definitions.#<p>A service mesh does not generate application code; it manages network concerns for existing applications.</p>
	####<p><strong>Explanation</strong>\: A service mesh abstracts away application-networking logic into dedicated infrastructure, applying it to all services regardless of language or framework, and providing capabilities like resilience, observability, traffic control, security, and policy enforcement transparently.</p>
}

// question: 1.2  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>Which open-source proxy forms the data plane of Istio?</p>{
	~[moodle]Nginx.#<p>While Nginx is a popular proxy, Envoy is the specific proxy used by Istio's data plane.</p>
	~[moodle]HAProxy.#<p>HAProxy is another proxy, but not the one integrated by default as Istio's data plane.</p>
	=[moodle]Envoy.
	~[moodle]Apache HTTP Server.#<p>Apache HTTP Server is a web server that can also act as a proxy, but it's not Istio's data plane proxy.</p>
	####<p><strong>Explanation</strong>\: Istio's data plane is made up of service proxies, based on the Envoy proxy, that live alongside applications and act as intermediaries for networking behavior.</p>
}

// question: 1.3  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>What are the two main components of the Istio service mesh architecture?</p>{
	~[moodle]Load Balancer and Firewall.#<p>Load balancers and firewalls are network components, but not the fundamental architectural breakdown of Istio.</p>
	=[moodle]Data Plane and Control Plane.
	~[moodle]API Gateway and Message Broker.#<p>API gateways and message brokers are other architectural patterns that can interact with a service mesh, but they are not its core components.</p>
	~[moodle]Virtual Machine and Container Orchestrator.#<p>Virtual machines and container orchestrators are deployment platforms on which Istio can run, not its internal architectural components.</p>
	####<p><strong>Explanation</strong>\: Istio comprises a data plane, composed of service proxies, and a control plane, which exposes an API for operators to manipulate network behaviors.</p>
}

// question: 1.4  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>How does Istio address service resilience in microservices environments?</p>{
	~[moodle]By requiring applications to implement language-specific resilience libraries.#<p>Istio aims to remove the need for language-specific resilience libraries.</p>
	=[moodle]By providing out-of-the-box resilience features like circuit breaking and retries via service proxies.
	~[moodle]By centralizing all resilience logic in a single, high-availability service.#<p>Resilience is applied at the service proxy level, distributed across the data plane, not centralized in a single service.</p>
	~[moodle]By ensuring that all network connections are perfectly reliable and never fail.#<p>Istio acknowledges that the network is unreliable and provides tools to deal with failures, rather than assuming perfect reliability.</p>
	####<p><strong>Explanation</strong>\: With a service proxy next to each application instance, applications no longer need language-specific resilience libraries for circuit breaking, timeouts, retries, and load balancing; these are handled by the service proxy.</p>
}

// question: 1.5  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>What is a significant drawback of using application-specific libraries (e.g., NetflixOSS Hystrix) for application networking concerns?</p>{
	~[moodle]They are typically open-source and lack commercial support.#<p>Many such libraries, like NetflixOSS, are indeed open-source, but their main drawback in this context is the architectural coupling and inconsistency, not necessarily lack of commercial support.</p>
	=[moodle]They introduce implicit constraints and inconsistencies, especially in polyglot environments.
	~[moodle]They increase the performance overhead of network calls significantly.#<p>While libraries can add overhead, the primary architectural drawback highlighted is inconsistency and coupling.</p>
	~[moodle]They are only compatible with monolithic application architectures.#<p>Libraries like NetflixOSS were developed for distributed, microservice environments, not just monoliths.</p>
	####<p><strong>Explanation</strong>\: Application-specific libraries introduce implicit constraints around undefined protocols and make it difficult to find analogous replacements for each framework/language combination in polyglot environments, leading to inconsistency.</p>
}

// question: 1.6  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>How does Istio facilitate "observability" for services in a mesh?</p>{
	~[moodle]By eliminating the need for any form of monitoring.#<p>Istio enhances observability by providing tools for monitoring and understanding system behavior, not by eliminating it.</p>
	=[moodle]By collecting application-level metrics, distributed tracing spans, and access logs via sidecar proxies.
	~[moodle]By forcing developers to manually instrument every service with custom code.#<p>Istio's strength is that it provides observability with few or no application code changes.</p>
	~[moodle]By providing a single, centralized log file for the entire distributed system.#<p>While Istio contributes to logging, it's part of a broader observability strategy that includes metrics and tracing, not just a single log file.</p>
	####<p><strong>Explanation</strong>\: The service proxy handles metrics collection, distributed tracing, and access control. Istio captures important metrics related to request handling and service interaction and can send spans to distributed-tracing backends.</p>
}

// question: 1.7  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>What is the relationship between an API Gateway and a service mesh like Istio?</p>{
	~[moodle]An API Gateway completely replaces the functionality of a service mesh.#<p>While a service mesh can take on some API gateway functions, it doesn't completely replace it, as API gateways often handle broader concerns like billing, developer portals, etc.</p>
	~[moodle]A service mesh completely replaces the functionality of an API Gateway.#<p>A service mesh typically focuses on intra-service communication, while an API gateway traditionally handles north-south (external to internal) traffic and broader API management concerns.</p>
	=[moodle]A service mesh can implement some API Gateway functionalities, potentially leading to their convergence.
	~[moodle]They are entirely separate and do not interact in any way.#<p>They can and often do interact, with the service mesh extending capabilities that might traditionally fall to an API gateway.</p>
	####<p><strong>Explanation</strong>\: The service proxies in Istio are becoming a place to enforce and implement API gateway functionality, suggesting that API management might eventually be built on top of the service mesh.</p>
}

// question: 1.8  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>When is Istio particularly useful for an organization?</p>{
	~[moodle]Exclusively for new, greenfield monolithic applications.#<p>Istio can be deployed to existing legacy or brownfield environments, and its value increases with the number of services; it's not exclusive to monoliths or greenfield projects.</p>
	=[moodle]For architectures with a large number of services, interconnections, and unreliable cloud infrastructure.
	~[moodle]Only for applications written in a specific programming language.#<p>Istio is designed to be language-agnostic, applying consistently across services regardless of their implementation language.</p>
	~[moodle]As a replacement for all existing networking infrastructure.#<p>Istio is a component of networking infrastructure that works with, not replaces, underlying platforms like Kubernetes.</p>
	####<p><strong>Explanation</strong>\: Istio's power shines as you move to architectures that experience large numbers of services, interconnections, and networks over unreliable cloud infrastructure, potentially spanning clusters, clouds, and data centers. It enables greater overall velocity by enabling autonomous teams at scale.</p>
}

// question: 1.9  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>What problem does the Envoy proxy solve by implementing networking concerns out-of-process from the application?</p>{
	~[moodle]It forces applications to use a specific programming language.#<p>By being out-of-process, Envoy promotes polyglot environments, not restricts them.</p>
	=[moodle]It reduces the need for application-specific libraries and framework dependencies for networking.
	~[moodle]It eliminates the need for any operating system in the application container.#<p>Envoy is a proxy, not an operating system replacement for the container.</p>
	~[moodle]It centralizes all application business logic in the proxy.#<p>Envoy handles networking concerns, not application business logic.</p>
	####<p><strong>Explanation</strong>\: Envoy implements networking concerns like retries, timeouts, circuit breaking, and load balancing out-of-process from the application, reducing explicit language or framework dependencies.</p>
}

// question: 1.10  name: Chapter 1: Introducing the Istio service mesh
::Chapter 1\: Introducing the Istio service mesh::[html]<p>In a cloud-native application architecture, what role does Istio play regarding application code and the deployment platform?</p>{
	~[moodle]It replaces both the deployment platform and most of the application code.#<p>Istio does not replace the deployment platform or business logic.</p>
	=[moodle]It acts as a connective tissue, facilitating the removal of complicated networking code from the application.
	~[moodle]It dictates the programming language and frameworks for all applications.#<p>Istio is language and framework agnostic.</p>
	~[moodle]It solely focuses on hardware resource management.#<p>Istio deals with application networking concerns, not directly hardware resource management, which is typically handled by the deployment platform.</p>
	####<p><strong>Explanation</strong>\: Istio plays the role of connective tissue between the deployment platform and the application code, facilitating the removal of complicated networking code from the application.</p>
}

////////////////////////////////////////////////////////////////////////////////
// Chapter 2: First steps with Istio
////////////////////////////////////////////////////////////////////////////////

// question: 2.1  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>What is the recommended command-line tool for installing Istio?</p>{
	~[moodle]kubectl.#<p>kubectl is for interacting with Kubernetes, not for installing Istio itself.</p>
	=[moodle]istioctl.
	~[moodle]helm.#<p>While Helm can be used, istioctl is often preferred for its simplicity and safety using IstioOperator CRDs.</p>
	~[moodle]docker.#<p>docker is for managing Docker containers, not for installing Istio.</p>
	####<p><strong>Explanation</strong>\: The istioctl command-line tool is used to install Istio and is the official method for any real installation, alongside istio-operator or Helm.</p>
}

// question: 2.2  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>Which Kubernetes namespace is typically used for deploying Istio's control plane components?</p>{
	~[moodle]default.#<p>The default namespace is for general application deployments, not Istio's core components.</p>
	~[moodle]kube-system.#<p>kube-system is reserved for Kubernetes system components.</p>
	=[moodle]istio-system.
	~[moodle]kube-public.#<p>kube-public is for publicly accessible cluster data.</p>
	####<p><strong>Explanation</strong>\: The istio-system namespace is special in that the control plane is deployed into it and can act as a cluster-wide control plane for Istio.</p>
}

// question: 2.3  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>What is the purpose of the istiod component in the Istio control plane?</p>{
	~[moodle]To proxy all application network traffic.#<p>Application network traffic is proxied by the Envoy proxy (data plane), not istiod (control plane).</p>
	=[moodle]To take high-level Istio configurations and translate them into proxy-specific configurations.
	~[moodle]To provide a user interface for monitoring services.#<p>Monitoring UIs like Kiali or Grafana are supporting components, not istiod itself.</p>
	~[moodle]To manage persistent storage for applications.#<p>istiod is focused on configuration and management of the mesh, not persistent storage.</p>
	####<p><strong>Explanation</strong>\: istiod, sometimes referred to as Istio Pilot, is responsible for taking higher-level Istio configurations specified by the user/operator and turning them into proxy-specific configurations for each data-plane service proxy.</p>
}

// question: 2.4  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>How is the Istio service proxy typically deployed alongside an application in a Kubernetes Pod?</p>{
	~[moodle]As a separate Pod.#<p>A separate Pod would break the tight coupling and locality desired for a sidecar proxy.</p>
	=[moodle]As a sidecar container within the same Pod.
	~[moodle]As a virtual machine on the same node.#<p>While Istio can integrate VMs, the primary deployment model for the proxy with containers is as a sidecar.</p>
	~[moodle]As a daemonset across all worker nodes.#<p>A daemonset would deploy one proxy per node, not one per application instance, which is required for fine-grained control.</p>
	####<p><strong>Explanation</strong>\: The istioctl kube-inject command enriches a Kubernetes resource file with the sidecar deployment of the Istio service proxy and additional components. A sidecar deployment packages a complementing container alongside the main application container.</p>
}

// question: 2.5  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>Which Istio resource is used to define how a client talks to a specific service, including available versions and routing properties?</p>{
	~[moodle]Gateway.#<p>A Gateway defines the entry points for traffic into a cluster.</p>
	~[moodle]ServiceEntry.#<p>A ServiceEntry is used to add external services to Istio's internal service registry.</p>
	=[moodle]VirtualService.
	~[moodle]DestinationRule.#<p>A DestinationRule is used to define policies that apply to traffic after routing has occurred, such as load balancing and subsets.</p>
	####<p><strong>Explanation</strong>\: A VirtualService resource defines how a client talks to a specific service through its fully qualified domain name, which versions of a service are available, and other routing properties (like retries and request timeouts).</p>
}

// question: 2.6  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>What are two key responsibilities of the Istio control plane, as listed in the sources?</p>{
	~[moodle]Managing hardware resources and deploying containers.#<p>Hardware resource management and container deployment are typically handled by the underlying Kubernetes platform.</p>
	=[moodle]Issuing certificates for workload identity and specifying usage policies.
	~[moodle]Developing application business logic and handling database queries.#<p>Istio does not implement or replace application business logic or database queries.</p>
	~[moodle]Collecting raw network packets and performing deep packet inspection.#<p>While the data plane (Envoy) inspects traffic, the control plane's role is configuration and management.</p>
	####<p><strong>Explanation</strong>\: The control plane provides functions such as certificate issuance and rotation, workload identity assignment, and APIs for specifying usage policies.</p>
}

// question: 2.7  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>What does a 2/2 in the READY column for a Pod in Kubernetes, after Istio injection, typically indicate?</p>{
	~[moodle]The Pod is failing and has restarted twice.#<p>Restarts are indicated in the RESTARTS column, not READY.</p>
	=[moodle]The Pod has two containers, and both are in a ready state.
	~[moodle]The Pod is only partially ready and needs further configuration.#<p>2/2 indicates full readiness for the configured containers.</p>
	~[moodle]The Pod is running on two different nodes for high availability.#<p>The READY column indicates container status within a Pod, not deployment across nodes.</p>
	####<p><strong>Explanation</strong>\: The 2/2 in the Ready column means there are two containers in the Pod, and two of them are in the Ready state, typically consisting of the application container and the istio-proxy sidecar.</p>
}

// question: 2.8  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>What is a common strategy used by Istio to add resilience to service communication without modifying application code?</p>{
	~[moodle]Manually deploying new code versions and rolling back on failure.#<p>While rollback is a strategy, Istio's resilience features are proactive and automated, often preventing the need for manual rollbacks due to transient network issues.</p>
	=[moodle]Automatically retrying failed requests or applying timeouts via the service proxy.
	~[moodle]Removing all network dependencies between services.#<p>Microservices inherently rely on network dependencies; Istio manages them, not removes them.</p>
	~[moodle]Implementing custom resilience logic directly within each microservice.#<p>Istio aims to abstract away resilience logic from application code, not to put it back in.</p>
	####<p><strong>Explanation</strong>\: Using Istio, and without touching any application code, a level of resilience (like automatic retries or timeouts) can be added when communicating over the network.</p>
}

// question: 2.9  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>What does "deployment vs. release" mean in the context of safely rolling out new software with Istio?</p>{
	~[moodle]Deployment refers to installing the software, while release means making it publicly available immediately.#<p>The distinction emphasizes incremental exposure of live traffic.</p>
	=[moodle]Deployment is bringing new code to production, while release is bringing live traffic to it incrementally.
	~[moodle]Deployment is for internal testing only, and release is for external users.#<p>While internal testing can be part of the deployment phase, the core distinction lies in the exposure to live production traffic.</p>
	~[moodle]They are synonymous terms and can be used interchangeably.#<p>The source explicitly differentiates these two terms to highlight fine-grained control strategies.</p>
	####<p><strong>Explanation</strong>\: A deployment is when new code is brought to production, where tests can be run against it. A release is when live traffic is brought to it incrementally, often using a phased approach.</p>
}

// question: 2.10  name: Chapter 2: First steps with Istio
::Chapter 2\: First steps with Istio::[html]<p>When using Grafana for Istio observability, what is the initial step to view dashboards?</p>{
	~[moodle]Manually upload data files to Grafana.#<p>Istio's supporting components, like Prometheus, scrape metrics automatically; manual upload is not typical.</p>
	=[moodle]Run istioctl dashboard grafana to port-forward Grafana to your local machine.
	~[moodle]Write custom queries in Prometheus.#<p>While custom queries are possible, Istio provides preconfigured dashboards for initial viewing.</p>
	~[moodle]Configure each service to send metrics directly to Grafana.#<p>Istio proxies send metrics to a collection system like Prometheus, which Grafana then visualizes; applications don't send directly to Grafana.</p>
	####<p><strong>Explanation</strong>\: To view Grafana dashboards, you would use istioctl dashboard grafana to port-forward it to your local machine, which automatically opens your default browser to the Grafana home screen.</p>
}

////////////////////////////////////////////////////////////////////////////////
// Chapter 3: Istio’s data plane: The Envoy proxy
////////////////////////////////////////////////////////////////////////////////

// question: 3.1  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>What is the core functionality of the Envoy proxy in a service mesh?</p>{
	~[moodle]To write application business logic.#<p>Envoy is a networking proxy, not a tool for writing application business logic.</p>
	=[moodle]To act as an application-level proxy for network traffic, providing features like service discovery and load balancing.
	~[moodle]To provide a persistent storage layer for microservices.#<p>Envoy provides networking functionality, not persistent storage.</p>
	~[moodle]To manage virtual machines on cloud platforms.#<p>Envoy runs on deployment platforms, it does not manage them.</p>
	####<p><strong>Explanation</strong>\: Envoy is an application-level proxy that can be inserted into the request path of applications to provide service discovery, load balancing, health checking, and other enhanced capabilities that understand layer 7 protocols.</p>
}

// question: 3.2  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>Envoy is written in which programming language, primarily for performance and stability?</p>{
	~[moodle]Java.#<p>Java is used for many applications, but Envoy's core is C++.</p>
	~[moodle]Python.#<p>Python is a scripting language, not suitable for Envoy's high-performance requirements.</p>
	=[moodle]C++.
	~[moodle]Go.#<p>Go (Golang) is used for some cloud-native components, but Envoy is C++.</p>
	####<p><strong>Explanation</strong>\: Envoy was developed at Lyft and is written in C++ in an effort to increase performance and, more importantly, to make it more stable and deterministic at higher load echelons.</p>
}

// question: 3.3  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>What type of configuration does Istio primarily use to manage a large fleet of Envoy proxies dynamically?</p>{
	~[moodle]Static configuration files.#<p>While Envoy can use static configuration, Istio leverages its dynamic capabilities for scalability.</p>
	~[moodle]Manual command-line edits on each proxy.#<p>Manual edits are impractical for large-scale deployments.</p>
	=[moodle]Dynamic configuration via xDS APIs.
	~[moodle]Hardcoded configurations within the application binaries.#<p>Hardcoding configurations would defeat the purpose of a flexible service mesh.</p>
	####<p><strong>Explanation</strong>\: Istio uses dynamic configuration capabilities, specifically xDS discovery APIs, which allow Istio to manage a large fleet of Envoy proxies, each with its own potentially complex configuration, without needing to stop and reload.</p>
}

// question: 3.4  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>Which Envoy feature helps to make the network "understandable" by collecting a large set of metrics?</p>{
	~[moodle]Service Discovery.#<p>Service Discovery helps locate services, but metrics collection is about understanding their behavior.</p>
	~[moodle]Traffic Routing.#<p>Traffic Routing directs requests, but metrics provide insights into the routing's effectiveness.</p>
	=[moodle]Observability with Metrics Collection.
	~[moodle]Circuit Breaking.#<p>Circuit Breaking provides resilience, but metrics are needed to observe when it's needed or has been triggered.</p>
	####<p><strong>Explanation</strong>\: One of the goals of Envoy is to help make the network understandable by collecting a large set of metrics, tracking dimensions around downstream systems, the server itself, and upstream clusters. This is part of Observability with Metrics Collection.</p>
}

// question: 3.5  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>What are the xDS APIs (e.g., LDS, EDS, RDS) in Envoy used for?</p>{
	~[moodle]To specify deployment parameters for containers.#<p>Deployment parameters are handled by the orchestrator (Kubernetes).</p>
	=[moodle]To allow the control plane to dynamically configure service proxies without hot restarts.
	~[moodle]To manage persistent volumes in Kubernetes.#<p>Persistent volumes are a Kubernetes concern, unrelated to Envoy's dynamic configuration APIs.</p>
	~[moodle]To define the security policies for network firewalls.#<p>While Envoy can enforce security, xDS refers to its dynamic configuration capabilities, not specifically firewall policies.</p>
	####<p><strong>Explanation</strong>\: The xDS APIs (Listener Discovery Service [LDS], Endpoint Discovery Service [EDS], Route Discovery Service [RDS]) allow the data plane to separate how it is configured and dynamically adapt its behavior without having to stop and reload, which Istio's istiod component implements.</p>
}

// question: 3.6  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>How does Envoy support application-level resilience features like retries and timeouts?</p>{
	~[moodle]By offloading these concerns entirely to the application code.#<p>Envoy abstracts these concerns away from application code.</p>
	=[moodle]By understanding Layer 7 protocols like HTTP and gRPC.
	~[moodle]By performing only basic connection-level (L3/L4) load balancing.#<p>Envoy goes beyond L3/L4 to understand L7 protocols for richer features.</p>
	~[moodle]By requiring manual configuration updates and restarts for every change.#<p>Envoy supports dynamic configuration, reducing the need for manual updates and restarts.</p>
	####<p><strong>Explanation</strong>\: Envoy can understand layer 7 protocols that an application may speak when communicating with other services, allowing it to add behavior like request-level timeouts, retries, and circuit breaking, which cannot be accomplished with basic connection-level (L3/L4) proxies.</p>
}

// question: 3.7  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>When testing Envoy, what insight can the X-Request-Id header provide?</p>{
	~[moodle]The remaining time until the request times out.#<p>X-Envoy-Expected-Rq-Timeout-Ms indicates timeout expectations.</p>
	=[moodle]A unique identifier that can be used to correlate requests across multiple services.
	~[moodle]The specific programming language used by the upstream service.#<p>Envoy operates at the network level, abstracted from the application's programming language.</p>
	~[moodle]The amount of memory consumed by the Envoy proxy.#<p>Metrics would provide memory consumption, not a request ID header.</p>
	####<p><strong>Explanation</strong>\: Envoy generates an X-Request-Id, which can be used to correlate requests across a cluster and potentially multiple hops across services to fulfill the request.</p>
}

// question: 3.8  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>What is the role of istiod in relation to the Envoy proxy in Istio?</p>{
	~[moodle]istiod acts as a backup for the Envoy proxy in case of failure.#<p>Envoy proxies are designed for resilience even if istiod is temporarily unavailable, but istiod is not a backup for the proxy itself.</p>
	=[moodle]istiod implements the xDS APIs to dynamically configure the Envoy proxies.
	~[moodle]istiod inspects the internal state of the Envoy proxy's memory.#<p>istiod configures Envoy, it doesn't introspect its internal runtime memory state directly in this manner.</p>
	~[moodle]istiod runs the application container alongside the Envoy proxy.#<p>The application container runs alongside the Envoy proxy within the same Pod, but istiod is the control plane component, not part of the Pod's runtime.</p>
	####<p><strong>Explanation</strong>\: Istio implements the xDS APIs in the istiod control-plane component, which istiod uses to read Istio configurations (like virtual services) and dynamically configure the service proxies.</p>
}

// question: 3.9  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>When Envoy automatically retries a failed request, what happens to the count of upstream_rq_retry statistics?</p>{
	~[moodle]It decreases, indicating fewer errors.#<p>A decrease would imply fewer retries, not an indication of retries happening.</p>
	=[moodle]It increases, reflecting the number of retry attempts.
	~[moodle]It remains unchanged because retries are not errors.#<p>Retries are a specific event tracked by Envoy's metrics.</p>
	~[moodle]It is reset to zero after each successful retry.#<p>Statistics accumulate over time or until explicitly reset.</p>
	####<p><strong>Explanation</strong>\: When Envoy automatically retries a request, it is indicated by statistics like cluster.httpbin_service.upstream_rq_retry: 3, meaning the count increases, reflecting the number of retry attempts.</p>
}

// question: 3.10  name: Chapter 3: Istio’s data plane: The Envoy proxy
::Chapter 3\: Istio’s data plane\: The Envoy proxy::[html]<p>What is a "cluster" in Envoy's configuration?</p>{
	~[moodle]A group of Envoy proxies acting as a single unit.#<p>A cluster refers to a logical grouping of upstream services, not proxies.</p>
	=[moodle]A set of backend services to which requests can be routed, along with associated settings.
	~[moodle]A type of network listener for incoming traffic.#<p>Listeners handle incoming traffic, while clusters represent the destinations for outgoing traffic.</p>
	~[moodle]A component for managing certificates and security policies.#<p>While clusters can have security settings, their primary definition is about backend services and their endpoints.</p>
	####<p><strong>Explanation</strong>\: In Envoy, a cluster is defined as a logically similar upstream service, along with its associated settings, such as load balancing and circuit breaking. Each cluster has a group of endpoints to similar workloads.</p>
}

////////////////////////////////////////////////////////////////////////////////
// Chapter 4: Istio gateways: Getting traffic into a cluster
////////////////////////////////////////////////////////////////////////////////

// question: 4.1  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>What is the primary function of an Istio Gateway resource?</p>{
	~[moodle]To define fine-grained traffic routing rules within the service mesh.#<p>Fine-grained traffic routing within the mesh is handled by VirtualService and DestinationRule resources.</p>
	=[moodle]To specify entry points into a cluster for external client connections.
	~[moodle]To enable distributed tracing for internal service communication.#<p>Distributed tracing is an observability feature handled by sidecar proxies and tracing backends, not directly by a Gateway.</p>
	~[moodle]To manage persistent data storage for applications.#<p>Persistent storage is managed by Kubernetes storage primitives, not Istio Gateway resources.</p>
	####<p><strong>Explanation</strong>\: The Gateway resource defines ports, protocols, and virtual hosts that Istio wishes to listen for at the edge of the service-mesh cluster, serving as an entry point for external traffic.</p>
}

// question: 4.2  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>What is "virtual hosting" in the context of traffic ingress?</p>{
	~[moodle]Running multiple virtual machines on a single physical host.#<p>This describes VM virtualization, not network ingress concepts.</p>
	=[moodle]Mapping multiple different services to a single virtual IP address and entry point.
	~[moodle]Using virtual private networks to secure traffic.#<p>Virtual hosting is about multiplexing services, not necessarily VPNs.</p>
	~[moodle]Creating virtual network interfaces for each application.#<p>This refers to network interface configuration, not service multiplexing at an ingress point.</p>
	####<p><strong>Explanation</strong>\: Hosting multiple different services at a single entry point is known as virtual hosting, allowing a single IP to serve different services based on, for example, the Host header.</p>
}

// question: 4.3  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>How do Gateway and VirtualService resources work together for ingress traffic?</p>{
	~[moodle]Gateway defines internal mesh services, and VirtualService exposes them externally.#<p>Gateway defines external entry points; VirtualService defines how traffic is routed after entering.</p>
	=[moodle]Gateway defines the ingress port and protocol, while VirtualService routes traffic from the gateway to specific services.
	~[moodle]Gateway manages TLS certificates, and VirtualService encrypts traffic.#<p>While Gateway can be configured for TLS, it's not its sole function, and VirtualService is for routing, not encryption.</p>
	~[moodle]Gateway creates new application instances, and VirtualService monitors their health.#<p>These resources are for traffic management, not application instance creation or health monitoring.</p>
	####<p><strong>Explanation</strong>\: The Gateway resource configures an Istio gateway to expose specific ports and protocols. The VirtualService resource then defines where traffic should go once it's allowed in at the edge by the Gateway.</p>
}

// question: 4.4  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>What is a key difference between an Istio ingress gateway and a Kubernetes Ingress resource?</p>{
	~[moodle]Kubernetes Ingress supports advanced traffic management features like retries and circuit breakers, while Istio Ingress Gateway does not.#<p>Istio Ingress Gateway (Envoy) is designed to provide these advanced features.</p>
	=[moodle]Istio Ingress Gateway supports richer traffic management capabilities and broader protocol support compared to Kubernetes Ingress.
	~[moodle]Kubernetes Ingress automatically handles mTLS, while Istio Ingress Gateway requires manual configuration.#<p>Istio supports mTLS, and the ingress gateway can be configured for it, making it easier than manual configuration.</p>
	~[moodle]Istio Ingress Gateway is only for HTTP traffic, whereas Kubernetes Ingress supports all TCP/UDP traffic.#<p>Istio Gateway supports TCP traffic in addition to HTTP/HTTPS.</p>
	####<p><strong>Explanation</strong>\: Istio ingress gateway offers richer traffic management capabilities than Kubernetes Ingress and is designed to support more protocols than just HTTP/HTTPS.</p>
}

// question: 4.5  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>What is the significance of the istio-egressgateway component?</p>{
	~[moodle]It manages all internal service-to-service communication.#<p>Internal service-to-service communication is primarily handled by the sidecar proxies.</p>
	=[moodle]It routes traffic out of the cluster, for example, to external services.
	~[moodle]It provides a user interface for monitoring egress traffic.#<p>Monitoring is done by tools like Kiali and Grafana, not the gateway itself.</p>
	~[moodle]It encrypts all incoming traffic to the cluster.#<p>Encryption of incoming traffic is handled by the ingress gateway if configured for TLS/mTLS.</p>
	####<p><strong>Explanation</strong>\: The istio-egressgateway component is responsible for routing traffic out of the cluster.</p>
}

// question: 4.6  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>How can Istio secure HTTP traffic with TLS at the ingress gateway?</p>{
	~[moodle]By offloading TLS termination to the application services behind the gateway.#<p>The ingress gateway typically performs TLS termination before forwarding to backend services.</p>
	~[moodle]By requiring clients to use self-signed certificates for authentication.#<p>While possible, typically trusted CA-signed certificates are used for public-facing services.</p>
	=[moodle]By configuring the Gateway resource to use a Kubernetes secret containing TLS certificates and keys.
	~[moodle]By automatically redirecting all HTTP traffic to an external, secure proxy.#<p>Istio handles this internally, not by redirecting to an external proxy.</p>
	####<p><strong>Explanation</strong>\: To secure HTTP traffic with TLS, you configure the Gateway resource with a Kubernetes secret containing the TLS certificate and private key.</p>
}

// question: 4.7  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>What happens when Istio treats network traffic as "plain TCP" through a gateway?</p>{
	~[moodle]All advanced L7 features like retries and complex routing are fully available.#<p>The opposite is true; advanced L7 features are limited.</p>
	=[moodle]Only basic connection-level routing is possible, with limited advanced features.
	~[moodle]Traffic is automatically converted to HTTP for full feature support.#<p>Istio does not automatically convert plain TCP to HTTP.</p>
	~[moodle]The gateway automatically detects and applies L7 policies for any protocol.#<p>Detection and application of L7 policies require understanding the protocol, which is not guaranteed for "plain TCP".</p>
	####<p><strong>Explanation</strong>\: When Istio treats the traffic as plain TCP, it does not get as many useful features like retries, request-level circuit breaking, or complex routing, simply because Istio cannot tell what protocol is being used (unless it's a specific L7 protocol Istio understands, like MongoDB).</p>
}

// question: 4.8  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>What is SNI (Server Name Indication) passthrough used for in Istio gateways?</p>{
	~[moodle]To terminate TLS connections at the gateway and inspect HTTP headers.#<p>SNI passthrough avoids terminating TLS at the gateway.</p>
	=[moodle]To route TCP traffic based on the SNI hostname without terminating TLS at the gateway.
	~[moodle]To encrypt traffic between services within the mesh automatically.#<p>Automatic mTLS within the mesh is a separate security feature.</p>
	~[moodle]To automatically generate TLS certificates for all services.#<p>Istiod handles certificate issuance for mTLS, not SNI passthrough directly.</p>
	####<p><strong>Explanation</strong>\: SNI passthrough allows routing TCP traffic based on the SNI hostname without terminating the TLS traffic at the ingress gateway. The gateway inspects SNI headers and routes traffic to the specific backend service, which then terminates the TLS connection.</p>
}

// question: 4.9  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>When should accessLogging be explicitly enabled in an Istio Telemetry configuration for the ingress gateway?</p>{
	~[moodle]When all workloads are already printing access logs to standard output.#<p>If logs are already being printed, there's no need to explicitly enable them for that purpose.</p>
	=[moodle]When you want detailed access logs only for specific ingress gateway workloads.
	~[moodle]When you disable all other forms of observability.#<p>Access logging is one component of observability, not a replacement for others.</p>
	~[moodle]When using only plain TCP traffic.#<p>Access logs are typically more detailed for HTTP/HTTPS traffic where more L7 information is available.</p>
	####<p><strong>Explanation</strong>\: The Telemetry definition enables access logs for Pods matching the selector. If access logs are already printing to standard output, explicit enabling might not be needed, but it's useful for targeted logging.</p>
}

// question: 4.10  name: Chapter 4: Istio gateways: Getting traffic into a cluster
::Chapter 4\: Istio gateways\: Getting traffic into a cluster::[html]<p>What is a "mesh-wide" Istio configuration and where must it be applied?</p>{
	~[moodle]Applies to a single service and is defined in the service's namespace.#<p>This describes a namespace-wide or workload-specific configuration.</p>
	=[moodle]Applies to all workloads in the entire mesh and must be applied in the Istio installation namespace.
	~[moodle]Applies only to egress traffic and is configured on the egress gateway.#<p>While some mesh-wide configs might affect egress, their scope is broader than just egress traffic.</p>
	~[moodle]Applies to a specific Pod and is defined as an annotation on the Pod.#<p>This describes a workload-specific configuration, usually via annotations.</p>
	####<p><strong>Explanation</strong>\: Mesh-wide configurations are applied to workloads in the entire mesh and must be applied in the Istio installation namespace.</p>
}

////////////////////////////////////////////////////////////////////////////////
// Chapter 5: Traffic control: Fine-grained traffic routing
////////////////////////////////////////////////////////////////////////////////

// question: 5.1  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>What is the core principle behind using Istio for fine-grained traffic routing during software releases?</p>{
	~[moodle]To remove all network traffic between services.#<p>Istio manages network traffic, it doesn't remove it.</p>
	=[moodle]To decouple deployment from release, allowing incremental exposure of new software to users.
	~[moodle]To automate code compilation and deployment.#<p>Istio focuses on runtime traffic management, not build automation.</p>
	~[moodle]To force all users to update their clients to the latest version immediately.#<p>Istio enables controlled, incremental rollouts, avoiding forced immediate updates for all users.</p>
	####<p><strong>Explanation</strong>\: Decoupling deployment from release allows for fine-grained control over how and which users are exposed to new changes, reducing risk, by enabling incremental exposure of new software.</p>
}

// question: 5.2  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>What is a "dark launch" in the context of traffic routing with Istio?</p>{
	~[moodle]Deploying a new service without any network access.#<p>A dark launch involves exposing the new functionality to some traffic, not no traffic.</p>
	=[moodle]Exposing new functionality in a controlled way to a specific group of users without affecting everyone else.
	~[moodle]Releasing software only during nighttime hours to minimize impact.#<p>The "dark" refers to limited user visibility, not time of day.</p>
	~[moodle]Completely mirroring all production traffic to a new, isolated environment.#<p>While mirroring is a related technique, a dark launch specifically involves routing live user traffic to the new version for a subset of users.</p>
	####<p><strong>Explanation</strong>\: In a dark launch, new functionality is exposed in a controlled way to a specific group of users (e.g., internal employees) without affecting everyone else, by routing a subset of live traffic to a newer version.</p>
}

// question: 5.3  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>Which Istio resource is primarily used to specify different versions of a service as "subsets" for traffic routing?</p>{
	~[moodle]VirtualService.#<p>VirtualService routes traffic to these subsets, but DestinationRule defines them.</p>
	~[moodle]Gateway.#<p>Gateway defines ingress points, not service subsets.</p>
	=[moodle]DestinationRule.
	~[moodle]ServiceEntry.#<p>ServiceEntry is for external services, not internal versioning.</p>
	####<p><strong>Explanation</strong>\: A DestinationRule is used to define policies that apply to traffic for a service, including specifying different versions of the service as subsets, typically based on Kubernetes labels.</p>
}

// question: 5.4  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>How can Istio implement "weighted traffic shifting" for a new service version?</p>{
	~[moodle]By automatically load-balancing traffic equally across all versions.#<p>Kubernetes might do limited load balancing, but Istio offers granular control over weights, not just equal distribution.</p>
	=[moodle]By configuring a VirtualService to distribute traffic to different service subsets based on a defined percentage.
	~[moodle]By routing traffic only to the newest version of the service.#<p>This is a full cut-over, not a gradual shift.</p>
	~[moodle]By manually restarting services whenever traffic needs to be shifted.#<p>Istio's traffic management is dynamic and doesn't require service restarts for routing changes.</p>
	####<p><strong>Explanation</strong>\: Weighted traffic shifting is achieved by configuring a VirtualService to distribute all live traffic to a set of versions for a particular service based on weights, e.g., 10% to v2 and 90% to v1.</p>
}

// question: 5.5  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>What is the benefit of "traffic mirroring" (shadowing) compared to other release techniques like dark launches or weighted shifting?</p>{
	~[moodle]It allows direct interaction with mirrored traffic for real-time feedback.#<p>Responses from mirrored traffic are ignored, so there's no direct real-time feedback from user interaction.</p>
	=[moodle]It sends a copy of production traffic to a new deployment without impacting real users, as responses are ignored.
	~[moodle]It guarantees 100% of users will experience the new version without issues.#<p>Mirroring is used to test for issues, not to guarantee problem-free release, and it doesn't expose 100% of users to the new version.</p>
	~[moodle]It completely isolates the new deployment from the production network.#<p>While it provides isolation for user impact, the traffic is still derived from the production network.</p>
	####<p><strong>Explanation</strong>\: Traffic mirroring copies production traffic and sends it to a new deployment without impacting real users, because the Istio proxy ignores any responses (success/failure) from the mirrored cluster.</p>
}

// question: 5.6  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>By default, what is Istio's policy regarding outbound traffic leaving the service mesh?</p>{
	~[moodle]All outbound traffic is denied by default.#<p>Istio's default is ALLOW_ANY, not to deny all.</p>
	=[moodle]All outbound traffic is allowed by default.
	~[moodle]Only outbound traffic to other services within the same cluster is allowed.#<p>The default is more permissive; it allows traffic outside the mesh too.</p>
	~[moodle]Outbound traffic is only allowed if it passes through a dedicated egress gateway.#<p>While an egress gateway can be configured for outbound traffic, it's not the default policy.</p>
	####<p><strong>Explanation</strong>\: By default, Istio allows any traffic out of the service mesh. For example, if an application tries to talk with external websites or services not managed by the service mesh, Istio allows this traffic out.</p>
}

// question: 5.7  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>What is the purpose of an Istio ServiceEntry resource?</p>{
	~[moodle]To define internal Kubernetes services for discovery.#<p>Kubernetes services are discovered automatically; ServiceEntry is for external services.</p>
	=[moodle]To insert an entry for an external service into Istio's service registry.
	~[moodle]To apply network policies to services outside the mesh.#<p>It makes external services discoverable, but directly applying network policies to them requires more configuration.</p>
	~[moodle]To force all outbound traffic to be encrypted.#<p>ServiceEntry is about discovery, not enforced encryption for external services.</p>
	####<p><strong>Explanation</strong>\: The Istio ServiceEntry resource encapsulates registry metadata that is used to insert an entry for an external service into Istio's service registry, making external services known and accessible within the mesh.</p>
}

// question: 5.8  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>What does the REGISTRY_ONLY outbound traffic policy mode in Istio achieve?</p>{
	~[moodle]It allows outbound traffic to any destination without restriction.#<p>ALLOW_ANY is the default that allows unrestricted traffic.</p>
	=[moodle]It restricts outbound traffic to only services explicitly whitelisted in the service mesh registry.
	~[moodle]It prevents any service from communicating with external networks.#<p>REGISTRY_ONLY allows whitelisted traffic, not prevents all external communication.</p>
	~[moodle]It enables automatic discovery of all external services.#<p>ServiceEntry defines explicit entries, not automatic discovery for all external services.</p>
	####<p><strong>Explanation</strong>\: Setting meshConfig.outboundTrafficPolicy.mode to REGISTRY_ONLY means Istio will allow traffic to leave the mesh only if it's explicitly whitelisted in the service-mesh registry.</p>
}

// question: 5.9  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>Which tool can automate the canary release process using Istio's APIs, reducing manual configuration?</p>{
	~[moodle]kubectl.#<p>kubectl is for applying configurations, but Flagger automates the process of traffic shifting.</p>
	=[moodle]Flagger.
	~[moodle]Prometheus.#<p>Prometheus collects metrics, which Flagger can use to make decisions, but Prometheus itself doesn't automate releases.</p>
	~[moodle]Jaeger.#<p>Jaeger is for distributed tracing, an observability tool, not release automation.</p>
	####<p><strong>Explanation</strong>\: Flagger is a canary-automation tool that allows you to specify parameters for performing releases, opening them to more users, and rolling back if issues arise, leveraging Istio's APIs to automate traffic shifting.</p>
}

// question: 5.10  name: Chapter 5: Traffic control: Fine-grained traffic routing
::Chapter 5\: Traffic control\: Fine-grained traffic routing::[html]<p>What is a crucial consideration when using weighted traffic shifting or traffic mirroring?</p>{
	~[moodle]Applications must be entirely stateless to support multiple versions.#<p>While easier with stateless services, the source highlights context awareness and concurrent versions as key, even for stateful services, noting the increased difficulty.</p>
	=[moodle]Applications should be built to support multiple versions running concurrently and be context-aware.
	~[moodle]These techniques eliminate the need for any monitoring or observation.#<p>Monitoring and observation are essential to these techniques to detect issues and decide on rollbacks or progression.</p>
	~[moodle]Only one version of a service can ever be deployed at a time.#<p>These techniques are specifically designed for running multiple versions simultaneously to enable gradual rollout.</p>
	####<p><strong>Explanation</strong>\: When new software versions are slowly released, it's crucial to monitor and observe both new and old versions. Services need to be built to support multiple versions running concurrently and be context-aware (e.g., live vs. mirrored traffic).</p>
}

////////////////////////////////////////////////////////////////////////////////
// Chapter 6: Resilience: Solving application networking challenges
////////////////////////////////////////////////////////////////////////////////

// question: 6.1  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>Which resilience pattern in Istio limits the number of connections and requests that can pile up when calling a service, failing fast if thresholds are exceeded?</p>{
	~[moodle]Retries.#<p>Retries attempt to re-send failed requests, not limit active connections.</p>
	~[moodle]Timeouts.#<p>Timeouts enforce time limits on requests, not the number of concurrent connections.</p>
	=[moodle]Circuit Breaking (Connection Pool Control).
	~[moodle]Locality-Aware Load Balancing.#<p>Locality-aware load balancing prioritizes endpoints based on geographical proximity.</p>
	####<p><strong>Explanation</strong>\: Circuit breaking, specifically connection-pool control (using connectionPool settings in a DestinationRule), limits the number of connections and requests in flight to an upstream service, short-circuiting them (failing fast) if too many pile up.</p>
}

// question: 6.2  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>What is the default load-balancing algorithm used by Istio's service proxy (Envoy)?</p>{
	~[moodle]Random.#<p>Random is an available algorithm, but not the default.</p>
	~[moodle]Weighted Least Request.#<p>Weighted Least Request (LEAST_CONN) is an available algorithm, but not the default.</p>
	=[moodle]Round Robin.
	~[moodle]Consistent Hash.#<p>Consistent Hash is another load balancing method, but not a default or explicitly listed as a standard Istio algorithm in the provided sources.</p>
	####<p><strong>Explanation</strong>\: Istio's service proxy uses a ROUND_ROBIN load-balancing strategy by default, delivering requests to endpoints in succession.</p>
}

// question: 6.3  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>How does Istio facilitate client-side load balancing?</p>{
	~[moodle]By requiring applications to implement custom load-balancing logic.#<p>Istio aims to abstract load-balancing logic from application code.</p>
	=[moodle]By equipping the client-side proxy with up-to-date service endpoint information for routing.
	~[moodle]By routing all client requests through a single, central load balancer.#<p>Istio's approach is distributed, with proxies handling load balancing at the client side, not through a single central point.</p>
	~[moodle]By embedding load balancing directly into the Kubernetes API server.#<p>Kubernetes provides basic load balancing, but Istio's client-side load balancing is implemented in the Envoy proxy.</p>
	####<p><strong>Explanation</strong>\: Istio uses service and endpoint discovery to equip the client-side proxy with up-to-date service endpoint information for routing, allowing it to perform client-side load balancing.</p>
}

// question: 6.4  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>When configuring retries in a VirtualService with a perTryTimeout, what is a critical consideration regarding the overall request timeout?</p>{
	~[moodle]perTryTimeout must always be greater than the overall request timeout.#<p>This would cause the overall timeout to always be reached before any retry.</p>
	=[moodle]The perTryTimeout value multiplied by the total number of attempts must be less than the overall request timeout.
	~[moodle]The overall request timeout must be disabled when retries are enabled.#<p>Timeouts and retries work in conjunction; disabling one is not a general best practice.</p>
	~[moodle]perTryTimeout is ignored if an overall request timeout is set.#<p>perTryTimeout is a crucial setting that interacts with the overall timeout.</p>
	####<p><strong>Explanation</strong>\: The perTryTimeout value multiplied by the total number of attempts must be less than the overall request timeout; otherwise, the overall request timeout will kick in before all retries get a chance.</p>
}

// question: 6.5  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>What is the "power of two choices" principle in Envoy's LEAST_CONN load balancing?</p>{
	~[moodle]It prioritizes connections to endpoints in two specific geographical regions.#<p>LEAST_CONN is about active requests, not geographical regions directly.</p>
	=[moodle]It randomly picks two endpoints, checks which has fewer active requests, and chooses that one.
	~[moodle]It always sends requests to the two least-connected endpoints simultaneously.#<p>It picks one of the two for the request, not sends to both.</p>
	~[moodle]It allows the user to choose between two different load-balancing algorithms at runtime.#<p>This refers to the internal algorithm, not user choice of algorithms.</p>
	####<p><strong>Explanation</strong>\: Envoy's LEAST_CONN load balancer picks two random endpoints, checks which has the fewest active requests, and chooses the one with the fewest active requests. This is known as the power of two choices and is a good trade-off versus a full scan.</p>
}

// question: 6.6  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>How does Istio's "outlier detection" contribute to service resilience?</p>{
	~[moodle]By re-routing all traffic to a single, highly available service.#<p>It removes unhealthy endpoints, not reroutes all traffic to a single one.</p>
	=[moodle]By actively removing misbehaving endpoints from the load-balancing pool for a period of time.
	~[moodle]By increasing the connection pool limits indefinitely for all services.#<p>Outlier detection works with connection limits, not by increasing them.</p>
	~[moodle]By notifying developers to manually intervene and fix unhealthy services.#<p>While it provides insights, its primary function is automated self-healing at the network layer, not manual intervention.</p>
	####<p><strong>Explanation</strong>\: Outlier detection guards against unhealthy services by observing the health of endpoints in the load-balancing pool and evicting misbehaving endpoints for a time, thus stopping traffic to them.</p>
}

// question: 6.7  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>What is the behavior of Istio's retryRemoteLocalities setting when enabled (true)?</p>{
	~[moodle]It restricts retries only to endpoints within the same locality.#<p>This is the default behavior when retryRemoteLocalities is false.</p>
	~[moodle]It prevents any retries from occurring, regardless of the failure type.#<p>This setting modifies retry behavior, it doesn't disable it.</p>
	=[moodle]It allows retries to spill over to other localities, even if they are not preferred.
	~[moodle]It forces all retries to go through a central global load balancer.#<p>Retries are handled by the sidecar proxies, not a central global load balancer.</p>
	####<p><strong>Explanation</strong>\: By default, retries are attempted against endpoints in their own locality. Setting retryRemoteLocalities to true allows retries to spill over to other localities, even if they are not locally preferred.</p>
}

// question: 6.8  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>When a request fails due to tripping a circuit-breaking threshold, which HTTP header does Istio's service proxy add to the response?</p>{
	~[moodle]X-Request-Id.#<p>X-Request-Id is for request correlation.</p>
	~[moodle]X-Envoy-Expected-Rq-Timeout-Ms.#<p>This indicates an expected timeout, not a circuit breaker trip.</p>
	=[moodle]X-Envoy-Overloaded.
	~[moodle]X-Circuit-Breaker-Status.#<p>X-Circuit-Breaker-Status is not the header specified in the source; it's X-Envoy-Overloaded.</p>
	####<p><strong>Explanation</strong>\: When a request fails for tripping a circuit-breaking threshold, Istio's service proxy adds an x-envoy-overloaded header to the response, indicating the failure was due to circuit breaking.</p>
}

// question: 6.9  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>What is a potential negative consequence of "unbridled retries" in a distributed system?</p>{
	~[moodle]It ensures immediate recovery from all network failures.#<p>While retries aid recovery, unbridled retries can worsen a situation.</p>
	=[moodle]It can contribute to degraded system health and cause cascading failures by amplifying load.
	~[moodle]It significantly reduces the overall latency of requests.#<p>Increased retries and load can increase latency, not reduce it.</p>
	~[moodle]It simplifies the debugging process by providing more logs.#<p>Cascading failures due to retries make debugging more complex.</p>
	####<p><strong>Explanation</strong>\: Unbridled retries can contribute to degraded system health, including causing cascading failures, by amplifying the load on an already overloaded or misbehaving service.</p>
}

// question: 6.10  name: Chapter 6: Resilience: Solving application networking challenges
::Chapter 6\: Resilience\: Solving application networking challenges::[html]<p>What mechanism does Istio use to enable capabilities of Envoy that are not directly exposed by the Istio API (e.g., request hedging)?</p>{
	~[moodle]Directly modifying the Envoy proxy binary.#<p>Directly modifying binaries is not a standard, supportable way to extend Istio.</p>
	=[moodle]Using the EnvoyFilter resource to alter Envoy's native configuration.
	~[moodle]Implementing custom application-level libraries for missing features.#<p>Istio aims to abstract these concerns away from application code.</p>
	~[moodle]Relying on the underlying Kubernetes network policies.#<p>Kubernetes network policies are L3/L4 and don't provide the fine-grained L7 control needed for features like request hedging.</p>
	####<p><strong>Explanation</strong>\: EnvoyFilter resources can be used to implement capabilities of Envoy that are not exposed by the Istio API, allowing direct manipulation of Envoy's native configuration.</p>
}

// Chapter 7: Observability: Understanding the behavior of your services

// question: 7.1  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>What is the primary difference between "observability" and "monitoring" as discussed in the sources?</p>{
	~[moodle]They are synonymous terms and refer to the same concept.#<p>The source explicitly differentiates them.</p>
	=[moodle]Monitoring collects metrics for known undesirable states, while observability focuses on understanding unpredictable system behavior.
	~[moodle]Observability relies on manual checks, while monitoring is fully automated.#<p>Both can involve automation, but their goals differ.</p>
	~[moodle]Monitoring is for microservices, and observability is for monolithic applications.#<p>Both apply to various architectures, but observability gains importance with distributed complexity.</p>
	####<p><strong>Explanation</strong>: Monitoring collects and aggregates metrics to watch for known undesirable states. Observability is a characteristic of a system that allows understanding what's really happening at runtime when unpredictable things happen.</p>
}

// question: 7.2  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>How does Istio's data plane primarily contribute to observability?</p>{
	~[moodle]By eliminating the need for any application instrumentation.#<p>While Istio simplifies metrics collection, application- or business-level metrics are still needed.</p>
	=[moodle]By capturing application-level network metrics, traces, and logs via sidecar proxies.
	~[moodle]By providing an interactive visualization dashboard by default.#<p>Visualization dashboards like Grafana and Kiali are supporting tools that consume Istio's data, not direct contributions from the data plane itself.</p>
	~[moodle]By enforcing security policies that prevent data leakage.#<p>While security is a mesh feature, it's not its primary contribution to observability.</p>
	####<p><strong>Explanation</strong>: Istio's data plane is in a unique position to capture important metrics related to request handling and service interaction (such as requests per second, latency, failed requests), and also distributed tracing, as it sits in the network request path between services.</p>
}

// question: 7.3  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>Which components are examples of the "golden-signal networking metrics" that Istio helps collect?</p>{
	~[moodle]CPU usage, memory utilization, disk I/O, network bandwidth.#<p>These are infrastructure metrics, but not the application-level "golden signals" that Istio focuses on for networking.</p>
	=[moodle]Latency, throughput, errors, and saturation.
	~[moodle]Number of database queries, cache hit ratio, user login counts.#<p>These are application- or business-level metrics that Istio doesn't automatically collect.</p>
	~[moodle]Code coverage, cyclomatic complexity, lines of code.#<p>These are code quality metrics, unrelated to runtime observability.</p>
	####<p><strong>Explanation</strong>: The Google SRE book refers to latency, throughput, errors, and saturation as the golden-signal metrics, which Istio helps collect for networking.</p>
}

// question: 7.4  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>What does the istio_requests_total metric represent in Istio's standard metrics?</p>{
	~[moodle]The total bytes transferred for all requests.#<p>istio_request_bytes and istio_response_bytes track bytes.</p>
	=[moodle]A counter that increments for each request that comes through a service proxy.
	~[moodle]The duration of requests in milliseconds.#<p>istio_request_duration_milliseconds tracks duration.</p>
	~[moodle]The number of active connections to a service.#<p>Envoy tracks active connections, but istio_requests_total is specifically about request count.</p>
	####<p><strong>Explanation</strong>: istio_requests_total is a COUNTER that increments for each request that comes through, both inbound and outbound, with various dimensions.</p>
}

// question: 7.5  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>How can you configure Istio proxies to report more detailed Envoy statistics than the standard set?</p>{
	~[moodle]By manually logging into each Envoy proxy and enabling debug mode.#<p>Manual logging is impractical for scale; Istio provides declarative configuration.</p>
	=[moodle]By specifying proxyStatsMatcher.inclusionPrefixes in the meshConfig during Istio installation.
	~[moodle]By disabling all default Istio metrics.#<p>This would remove all metrics, not enhance detail.</p>
	~[moodle]By installing custom Prometheus client libraries in each application.#<p>This is for application-specific metrics, not extending Envoy's internal stats.</p>
	####<p><strong>Explanation</strong>: You have the option to configure this as a mesh-wide setting during the Istio installation by specifying defaultConfig.proxyStatsMatcher.inclusionPrefixes in the IstioOperator resource, customizing which metrics are reported.</p>
}

// question: 7.6  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>What is a "dimension" in the context of Istio metrics?</p>{
	~[moodle]The numerical value of a metric at a specific time.#<p>This is the metric's value, not a dimension.</p>
	~[moodle]A fixed unit of measurement for all metrics (e.g., milliseconds).#<p>This refers to the unit of the value, not a dimension that categorizes it.</p>
	=[moodle]An attribute that differentiates variations of a metric (e.g., response_code, reporter).
	~[moodle]The total sum of all metric values over a period.#<p>This is an aggregation, not a dimension.</p>
	####<p><strong>Explanation</strong>: A metric can contain many dimensions, such as response_code, reporter, source_workload, destination_workload, etc. If any of these dimensions are different, a new entry for that metric will be seen.</p>
}

// question: 7.7  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>What does the pilot_proxy_convergence_time metric in the control plane measure?</p>{
	~[moodle]The total uptime of the istiod component.#<p>Uptime is a simple status, not a convergence time.</p>
	=[moodle]The time taken to distribute configuration changes to the data-plane proxies.
	~[moodle]The number of connections between istiod and the Kubernetes API server.#<p>This metric is about pushing config to proxies, not istiod's internal connections to Kubernetes.</p>
	~[moodle]The amount of memory consumed by the istiod process.#<p>Memory consumption is a resource metric, not convergence time.</p>
	####<p><strong>Explanation</strong>: The pilot_proxy_convergence_time metric measures how long it takes for configuration to be pushed and synchronized with the data-plane proxies.</p>
}

// question: 7.8  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>When creating new custom metrics in Istio, what language is used for defining their value?</p>{
	~[moodle]YAML.#<p>YAML is used for Istio resource definitions, not the metric value expression.</p>
	~[moodle]JSON.#<p>JSON can be used for configuration, but CEL is for the expression.</p>
	=[moodle]Common Expression Language (CEL).
	~[moodle]Prometheus Query Language (PromQL).#<p>PromQL is for querying Prometheus, not defining metrics in Istio.</p>
	####<p><strong>Explanation</strong>: The value of a custom metric is a string that is a Common Expression Language (CEL) expression, which must return an integer for a COUNTER type.</p>
}

// question: 7.9  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>What is the role of the attribute-gen proxy plugin in Istio?</p>{
	~[moodle]To aggregate metrics from multiple services into a single dashboard.#<p>This is a function of visualization tools like Grafana or Kiali.</p>
	=[moodle]To create new attributes based on existing ones, which can then be used in metrics.
	~[moodle]To generate custom API endpoints for data retrieval.#<p>attribute-gen creates attributes for metrics, not API endpoints.</p>
	~[moodle]To automatically enforce authorization policies for all requests.#<p>Authorization policies are handled by security filters, not directly attribute-gen.</p>
	####<p><strong>Explanation</strong>: The attribute-gen proxy plugin is another WebAssembly (Wasm) extension used to customize the behavior of the proxy's metrics. It layers in before the stats plugin so that it can create new attributes based on existing ones, which can then be used in stats.</p>
}

// question: 7.10  name: Chapter 7: Observability: Understanding the behavior of your services
::Chapter 7\: Observability: Understanding the behavior of your services::[html]<p>What happens behind the scenes when you update an Istio installation with an IstioOperator configuration containing new metric dimensions?</p>{
	~[moodle]The istiod control plane restarts all application Pods.#<p>istiod aims for dynamic configuration updates, not always restarting Pods.</p>
	~[moodle]The istioctl CLI tool directly modifies the Prometheus configuration.#<p>istioctl applies Istio configurations, it doesn't directly modify Prometheus config files.</p>
	=[moodle]istiod updates the EnvoyFilter (stats-filter-1.13) that configures Istio metrics.
	~[moodle]All existing metrics are deleted and recreated.#<p>It modifies existing metrics to include new dimensions, it doesn't delete and recreate all.</p>
	####<p><strong>Explanation</strong>: After updating the Istio installation with IstioOperator configuration containing new dimensions, istiod updates the EnvoyFilter (e.g., stats-filter-1.13) that configures Istio metrics.</p>
}

// Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali

// question: 8.1  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>What is the primary role of Kiali within the Istio service mesh?</p>{
	~[moodle]To store long-term metrics and trace data from all services.#<p>Metric and trace data are stored in backends like Prometheus and Jaeger, not primarily by Kiali.</p>
	=[moodle]To provide a web-based console for visualizing network behavior, traffic flow, and Istio configurations.
	~[moodle]To manage and rotate workload certificates for mutual TLS.#<p>Certificate management and rotation are handled by Istiod.</p>
	~[moodle]To implement fine-grained traffic routing and resilience policies across the mesh.#<p>Traffic routing and resilience policies are defined using Istio resources like VirtualServices and DestinationRules, managed by the control plane.</p>
	####<p><strong>Explanation</strong>: Kiali offers a web console for the mesh, providing a visual representation of network behavior, including traffic flow, health, and Istio configurations, to aid in troubleshooting.</p>
}

// question: 8.2  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>Which three tools are often used together with Istio for observability, particularly for visualizing network behavior?</p>{
	~[moodle]Docker, Kubernetes, and Helm.#<p>These are foundational technologies for container orchestration and deployment, not primarily observability visualization tools.</p>
	=[moodle]Prometheus, Grafana, and Kiali.
	~[moodle]Envoy, Istiod, and Pilot Agent.#<p>These are core components of Istio's data plane (Envoy, Pilot Agent) and control plane (Istiod), not end-user visualization tools.</p>
	~[moodle]Spiffe, JWT, and mTLS.#<p>These are concepts and components related to security and identity within Istio.</p>
	####<p><strong>Explanation</strong>: The book explicitly mentions using Grafana, Jaeger (a distributed tracing system), and Kiali for visualizing network behavior, with Prometheus for scraping metrics.</p>
}

// question: 8.3  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>What concept in distributed systems helps diagnose misbehaving requests as they traverse multiple microservices?</p>{
	~[moodle]Load Balancing.#<p>Load balancing distributes requests among healthy instances.</p>
	~[moodle]Circuit Breaking.#<p>Circuit breaking prevents cascading failures by limiting requests to unhealthy services.</p>
	=[moodle]Distributed Tracing.
	~[moodle]Service Discovery.#<p>Service discovery allows services to find and communicate with each other.</p>
	####<p><strong>Explanation</strong>: Distributed tracing provides insights into the components of a distributed system involved in serving a request, allowing operators to understand what services are involved and how long each takes, which is critical for diagnosing issues.</p>
}

// question: 8.4  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>What is an Istio "Span" in the context of distributed tracing?</p>{
	~[moodle]A unique identifier for an entire request journey across multiple services.#<p>This describes a "Trace," which is a collection of Spans.</p>
	=[moodle]A collection of data representing a unit of work within a single service or component.
	~[moodle]A policy that defines how long a request is allowed to take before timing out.#<p>This describes a timeout policy.</p>
	~[moodle]A configuration for how traffic is distributed among different versions of a service.#<p>This describes traffic shifting using a VirtualService.</p>
	####<p><strong>Explanation</strong>: A Span is a collection of data representing a unit of work within a service or component, including start time, end time, operation name, tags, and logs.</p>
}

// question: 8.5  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>For distributed tracing to work across an entire request call graph, what responsibility lies with the application code itself, even when Istio is configured for tracing?</p>{
	~[moodle]To generate the initial trace ID and span ID for every new request.#<p>Istio's proxy can generate a new trace if one isn't already present.</p>
	~[moodle]To store all collected trace data in a local database before sending it to the tracing engine.#<p>Trace data is sent to a dedicated tracing engine like Jaeger.</p>
	=[moodle]To propagate the tracing headers (like Zipkin headers) to any outgoing requests it makes.
	~[moodle]To visually render the distributed trace data for end-users.#<p>Visualization is handled by tools like Jaeger UI or Kiali.</p>
	####<p><strong>Explanation</strong>: While Istio's service proxy can propagate tracing IDs and metadata between services and send span information to a tracing engine, applications are responsible for propagating the tracing metadata (e.g., HTTP headers) internally for outgoing requests to maintain the full trace context.</p>
}

// question: 8.6  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>Which Istio component is responsible for collecting metrics (like requests per second and latency) at the network level on behalf of applications?</p>{
	~[moodle]Istiod.#<p>Istiod is the control plane, configuring the data plane.</p>
	~[moodle]Kubernetes API Server.#<p>Kubernetes API Server manages Kubernetes resources.</p>
	=[moodle]Envoy Proxy.
	~[moodle]Helm.#<p>Helm is a package manager for Kubernetes.</p>
	####<p><strong>Explanation</strong>: Istio's data-plane proxy, Envoy, sits in the network request path between services and can capture important metrics related to request handling and service interaction without requiring application code changes.</p>
}

// question: 8.7  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>When configuring Istio for distributed tracing, which "Zipkin tracing headers" are commonly used by Istio's functionality?</p>{
	~[moodle]Accept, Content-Type, Host.#<p>These are standard HTTP headers, not specifically used for distributed tracing correlation by Istio.</p>
	=[moodle]x-request-id, x-b3-traceid, x-b3-spanid.
	~[moodle]Authorization, User-Agent, Referer.#<p>These are standard HTTP headers, not specifically used for distributed tracing correlation by Istio.</p>
	~[moodle]Cookie, Set-Cookie, Cache-Control.#<p>These are standard HTTP headers, not specifically used for distributed tracing correlation by Istio.</p>
	####<p><strong>Explanation</strong>: Istio uses a specific set of Zipkin tracing headers for its distributed tracing functionality, including x-request-id, x-b3-traceid, x-b3-spanid, x-b3-parentspanid, x-b3-sampled, x-b3-flags, and x-ot-span-context.</p>
}

// question: 8.8  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>What is the consequence of setting a low trace sampling rate for distributed tracing in a production environment?</p>{
	~[moodle]It guarantees 100% trace coverage for all requests.#<p>A low sampling rate means less than 100% coverage. 100% sampling increases overhead.</p>
	~[moodle]It significantly increases the performance overhead of the system.#<p>A low sampling rate is used to reduce performance overhead, not increase it.</p>
	=[moodle]It reduces the performance penalty but means fewer requests will have full trace data.
	~[moodle]It automatically forces tracing for all requests, regardless of headers.#<p>Force tracing is a separate mechanism triggered by a specific header, not a consequence of a low sampling rate.</p>
	####<p><strong>Explanation</strong>: Distributed tracing and span collection can impose a hefty performance penalty. Operators may restrict how frequently traces are collected by configuring a lower sampling rate, which reduces overhead but also means fewer traces are available for analysis.</p>
}

// question: 8.9  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>How does Kiali aid in debugging processes in an Istio mesh, beyond just showing a network graph?</p>{
	~[moodle]By automatically fixing misconfigurations in Istio resources.#<p>Kiali identifies and validates Istio configurations but does not automatically fix them.</p>
	~[moodle]By providing direct SSH access to all service proxies.#<p>Kiali does not provide direct SSH access.</p>
	=[moodle]By correlating metrics, traces, and application logs in a unified view.
	~[moodle]By generating new deployment manifests for broken services.#<p>Kiali's role is observation and validation, not generating deployment manifests.</p>
	####<p><strong>Explanation</strong>: Kiali enhances the debugging process by correlating telemetry such as metrics, traces, and application logs in a unified dashboard, eliminating the need to switch between different tools and cross-check timelines.</p>
}

// question: 8.10  name: Chapter 8: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali
::Chapter 8\: Observability: Visualizing network behavior with Grafana, Jaeger, and Kiali::[html]<p>Which Istio resource allows you to configure the tracing system for a specific workload rather than globally for the entire mesh?</p>{
	~[moodle]DestinationRule applied to the workload.#<p>DestinationRule is used for load balancing and resilience policies.</p>
	=[moodle]An annotation on the deployment's Pod template, specifically proxy.istio.io/config.
	~[moodle]A Gateway resource with tracing parameters.#<p>Gateway resources are for ingress traffic.</p>
	~[moodle]A ServiceEntry definition specifying the tracing backend.#<p>ServiceEntry is for adding external services to Istio's registry.</p>
	####<p><strong>Explanation</strong>: While tracing can be configured globally at installation, it can also be configured per workload by editing annotations for a deployment’s Pod template, specifically using proxy.istio.io/config to include tracing settings like the Zipkin address and sampling rate.</p>
}

// Chapter 9: Securing microservice communication

// question: 9.1  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>What is the primary method Istio uses to provide identity to workloads in dynamic and heterogeneous environments?</p>{
	~[moodle]Through Kubernetes Pod IP addresses.#<p>IP addresses are dynamic and not a reliable form of identity.</p>
	~[moodle]By assigning static DNS records to each service.#<p>Static DNS records are insufficient for dynamic identity management and authentication in microservices.</p>
	=[moodle]By implementing the SPIFFE (Secure Production Identity Framework For Everyone) specification.
	~[moodle]By requiring manual certificate installation and management.#<p>Istio automates certificate issuance and rotation, significantly reducing the need for manual management.</p>
	####<p><strong>Explanation</strong>: Istio uses the SPIFFE specification to provide identity to workloads, which includes generating an RFC 3986 compliant URI encoded in an X.509 certificate (SVID) for each workload.</p>
}

// question: 9.2  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>Which Istio resource configures the proxy to authenticate service-to-service traffic and is instrumental in implementing mutual TLS (mTLS)?</p>{
	~[moodle]RequestAuthentication.#<p>RequestAuthentication validates end-user credentials, like JWTs.</p>
	~[moodle]AuthorizationPolicy.#<p>AuthorizationPolicy defines access control rules after authentication.</p>
	=[moodle]PeerAuthentication.
	~[moodle]VirtualService.#<p>VirtualService is used for traffic routing.</p>
	####<p><strong>Explanation</strong>: The PeerAuthentication resource configures the proxy to authenticate service-to-service traffic, enabling features like auto mTLS. Upon successful authentication, it extracts information from the peer's certificate for authorization.</p>
}

// question: 9.3  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>What information is typically encoded in a SPIFFE Verifiable Identity Document (SVID) issued by Istio's control plane?</p>{
	~[moodle]The public IP address of the service.#<p>IP addresses are dynamic and not part of the identity.</p>
	~[moodle]The Git commit hash of the application code.#<p>This is deployment-specific metadata, not core to the cryptographic identity.</p>
	=[moodle]A SPIFFE ID (URI) identifying the workload, often based on its service account.
	~[moodle]The deployment timestamp of the workload.#<p>This is deployment-specific metadata, not core to the cryptographic identity.</p>
	####<p><strong>Explanation</strong>: The SPIFFE ID, an RFC 3986 compliant URI (e.g., spiffe://trust-domain/path), is encoded in an X.509 certificate, known as an SVID. Istio populates this path using the service account under which a workload runs.</p>
}

// question: 9.4  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>What is the main purpose of the RequestAuthentication resource in Istio's security model?</p>{
	~[moodle]To define which external authorization service to use for custom policies.#<p>External authorization uses an AuthorizationPolicy with a CUSTOM provider.</p>
	=[moodle]To validate JSON Web Tokens (JWTs) for end-user authentication and extract their claims.
	~[moodle]To configure mutual TLS between services within the mesh.#<p>Mutual TLS between services is configured by PeerAuthentication.</p>
	~[moodle]To redirect HTTP traffic to HTTPS for secure gateway access.#<p>HTTP to HTTPS redirection is handled by Gateway and VirtualService resources.</p>
	####<p><strong>Explanation</strong>: The primary purpose of RequestAuthentication is to validate JWTs, extract claims from valid tokens, and store them as filter metadata, which can then be used by authorization policies.</p>
}

// question: 9.5  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>When multiple AuthorizationPolicy resources are applied to a workload, how does Istio evaluate them to determine access?</p>{
	~[moodle]It evaluates policies based on a priority field defined by the user.#<p>Istio does not use a priority field for policy evaluation.</p>
	~[moodle]It applies all DENY policies first, then all ALLOW policies, and if neither matches, it allows the request.#<p>This describes an incorrect evaluation order.</p>
	~[moodle]It applies all ALLOW policies first, and if none match, it proceeds to DENY policies.#<p>This describes an incorrect evaluation order.</p>
	=[moodle]It follows a specific order: CUSTOM policies, then DENY policies, then ALLOW policies, with a catch-all policy if no explicit match.
	####<p><strong>Explanation</strong>: Istio uses a specific evaluation order for authorization policies: CUSTOM policies are evaluated first, followed by DENY policies. If no CUSTOM or DENY policy rejects the request, ALLOW policies are evaluated. If no ALLOW policy is matched and no catch-all policy exists, the request is allowed.</p>
}

// question: 9.6  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>What is "auto mTLS" in Istio, and what does it primarily secure?</p>{
	~[moodle]Automated end-user login using tokens.#<p>End-user authentication involves RequestAuthentication and JWTs.</p>
	=[moodle]Traffic between services that have the sidecar proxy injected, encrypting and mutually authenticating it by default.
	~[moodle]Access to external databases from within the mesh.#<p>This requires explicit configuration, typically using ServiceEntry resources, and mTLS might apply but isn't "auto" in the same way.</p>
	~[moodle]The control plane's communication with the Kubernetes API server.#<p>This refers to internal control plane security, not general service-to-service traffic for applications.</p>
	####<p><strong>Explanation</strong>: Auto mTLS refers to the default behavior where traffic between services with the sidecar proxy injected is automatically encrypted and mutually authenticated. This process is automated to issue and rotate certificates, making it secure by default.</p>
}

// question: 9.7  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>Which header is commonly used by an external authorization service (ExtAuthz) to determine if an incoming request is allowed, as demonstrated in the Istio samples?</p>{
	~[moodle]x-request-id.#<p>x-request-id is for tracing.</p>
	=[moodle]x-ext-authz.
	~[moodle]Authorization.#<p>Authorization header is typically for JWTs or other credentials.</p>
	~[moodle]Host.#<p>Host header is for virtual hosting.</p>
	####<p><strong>Explanation</strong>: In the provided example for integrating with custom external authorization services, the sample ExtAuthz service checks for the x-ext-authz header with a specific value (e.g., allow) to determine if a request is permitted.</p>
}

// question: 9.8  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>To allow requests originating from a single namespace, such as default, to a service in the istioinaction namespace, what needs to be specified in the AuthorizationPolicy?</p>{
	~[moodle]The to field with the destination service.#<p>The to field specifies the operations (e.g., paths, methods) on the target service.</p>
	~[moodle]The when field with a time-based condition.#<p>The when field specifies additional conditions that must be met.</p>
	=[moodle]The from field with a source block matching request.namespace to default.
	~[moodle]The action field set to DENY by default.#<p>The action field sets the policy to ALLOW or DENY, but doesn't define the source.</p>
	####<p><strong>Explanation</strong>: To allow requests from a specific namespace, the AuthorizationPolicy needs a from field with a source block that matches the request.namespace attribute to the desired namespace, for example, values: ["default"].</p>
}

// question: 9.9  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>What are the three key resources that configure the service proxy for authentication and authorization in Istio?</p>{
	~[moodle]ServiceEntry, Gateway, VirtualService.#<p>These are for traffic management and ingress.</p>
	=[moodle]PeerAuthentication, RequestAuthentication, AuthorizationPolicy.
	~[moodle]Sidecar, EnvoyFilter, WasmPlugin.#<p>These are for extending Istio's data plane.</p>
	~[moodle]Deployment, Service, Pod.#<p>These are standard Kubernetes resources for deploying applications.</p>
	####<p><strong>Explanation</strong>: Istio security is defined around three main resources: PeerAuthentication for service-to-service authentication, RequestAuthentication for end-user authentication (like JWTs), and AuthorizationPolicy for access control.</p>
}

// question: 9.10  name: Chapter 9: Securing microservice communication
::Chapter 9\: Securing microservice communication::[html]<p>What is the purpose of the CUSTOM action within an AuthorizationPolicy?</p>{
	~[moodle]To allow all requests by default, regardless of other policies.#<p>This is typically handled by the absence of DENY or ALLOW policies, or a catch-all ALLOW policy.</p>
	~[moodle]To explicitly deny all requests to a specific workload.#<p>This is done using an AuthorizationPolicy with action: DENY.</p>
	=[moodle]To delegate authorization decisions to an external authorization service.
	~[moodle]To apply the same policy to all namespaces in the mesh.#<p>Policy scope is defined by namespace and selector fields.</p>
	####<p><strong>Explanation</strong>: The CUSTOM action in an AuthorizationPolicy allows Istio to integrate with custom external authorization services (ExtAuthz). When this action is used, Istio's service proxy calls out to the configured external authorization service to determine if a request should be allowed.</p>
}

// Chapter 10: Troubleshooting the data plane

// question: 10.1  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>What is the most common reason for unexpected behavior in the Istio data plane after applying new Istio resources?</p>{
	~[moodle]A misconfigured Kubernetes cluster.#<p>While possible, this is a broader issue; data plane misconfiguration is more specific to Istio resources.</p>
	~[moodle]Incorrect networking between Pods.#<p>Istio aims to simplify this, so direct networking issues are less common unless related to misconfiguration.</p>
	=[moodle]A misconfigured data plane, where Istio resources are not correctly interpreted or applied.
	~[moodle]Outdated application code in the services.#<p>Application code issues are separate from data plane configuration issues, though they can manifest similar symptoms.</p>
	####<p><strong>Explanation</strong>: The most common mistake and cause of unexpected behavior in the data plane is a misconfiguration of Istio's human-readable resources (like VirtualService, DestinationRule), which are then incorrectly translated or applied to the Envoy proxy.</p>
}

// question: 10.2  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>Which istioctl command provides an overview of the data plane's synchronization state for all workloads, indicating whether they are "SYNCED" or "NOT SENT" for various xDS APIs?</p>{
	~[moodle]istioctl analyze.#<p>istioctl analyze diagnoses Istio configurations for issues.</p>
	~[moodle]istioctl describe.#<p>istioctl describe provides a workload-specific configuration summary.</p>
	=[moodle]istioctl proxy-status.
	~[moodle]istioctl dashboard.#<p>istioctl dashboard opens visualization tools like Kiali or Grafana.</p>
	####<p><strong>Explanation</strong>: The istioctl proxy-status command is used to verify whether the data plane is synchronized with the latest configuration by listing all workloads and their synchronization state for xDS APIs (CDS, LDS, RDS, EDS).</p>
}

// question: 10.3  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>When troubleshooting data plane issues, what does a 503 Service Unavailable response code typically indicate if Istio is configured to route traffic to non-existent subsets?</p>{
	~[moodle]The application is processing the request successfully.#<p>A 503 is a failure.</p>
	~[moodle]The upstream service is overloaded but still reachable.#<p>While related to availability, 503 specifically in this context points to a routing misconfiguration.</p>
	=[moodle]The virtual service is routing to clusters that do not exist or are unhealthy.
	~[moodle]A client-side load balancing error in the application.#<p>The issue lies with Istio's routing rules, not the application's client-side load balancing.</p>
	####<p><strong>Explanation</strong>: A 503 Service Unavailable response, especially when routing to non-existent subsets, indicates that the virtual service is attempting to route to clusters that either don't exist or don't have healthy endpoints, leading to the request failing at the proxy level.</p>
}

// question: 10.4  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>How can Kiali help in discovering misconfigurations in Istio resources?</p>{
	~[moodle]By automatically rolling back faulty deployments.#<p>Kiali identifies issues but does not automatically roll back deployments.</p>
	~[moodle]By providing a command-line interface to edit YAML files.#<p>Kiali is a web UI, not a command-line editor.</p>
	=[moodle]By highlighting misconfigured sections in the YAML view of Istio resources and showing warnings.
	~[moodle]By generating real-time performance reports for each service.#<p>Kiali shows performance metrics but its specific strength in misconfiguration is validation and highlighting.</p>
	####<p><strong>Explanation</strong>: Kiali's Istio Config view lists all applied Istio configurations and accompanies misconfigured resources with notifications. Clicking these warnings redirects to the YAML view, where misconfigured sections are highlighted to aid diagnosis.</p>
}

// question: 10.5  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>Which istioctl command is considered a powerful diagnostic tool for analyzing Istio configurations, capable of running on clusters with issues or validating configurations pre-application?</p>{
	~[moodle]istioctl proxy-config.#<p>proxy-config queries live proxy configurations.</p>
	~[moodle]istioctl manifest generate.#<p>manifest generate is for generating Istio installation manifests.</p>
	=[moodle]istioctl analyze.
	~[moodle]istioctl install.#<p>install is for deploying Istio.</p>
	####<p><strong>Explanation</strong>: The istioctl analyze command is a powerful diagnostic tool designed to analyze Istio configurations for detected issues. It can be used both to validate configurations before they are applied and to diagnose problems in existing clusters.</p>
}

// question: 10.6  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>What is the purpose of accessing Envoy's administration interface, usually on port 15000 of the service proxy?</p>{
	~[moodle]To deploy new application versions.#<p>Deployment is handled by Kubernetes.</p>
	=[moodle]To view the currently loaded Envoy configuration and modify aspects like logging levels.
	~[moodle]To manage Kubernetes Pods and Deployments.#<p>Kubernetes resources are managed via kubectl.</p>
	~[moodle]To initiate a distributed trace for a specific request.#<p>Distributed traces are initiated by Istio's proxy with the right configuration or via force-trace headers.</p>
	####<p><strong>Explanation</strong>: The Envoy administration interface (Admin API), typically exposed on port 15000 of the service proxy, allows users to view the current Envoy configuration (config_dump), query statistics (/stats), and modify certain aspects like increasing the logging level.</p>
}

// question: 10.7  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>When inspecting Envoy's access logs to troubleshoot an issue, what is the benefit of changing the accessLogEncoding to JSON format instead of the default TEXT format?</p>{
	~[moodle]It reduces the size of the access logs, improving performance.#<p>JSON logs generally increase the amount of logging, potentially straining logging infrastructure.</p>
	~[moodle]It automatically filters out non-error entries, making logs easier to read.#<p>It changes the format, not the filtering mechanism.</p>
	=[moodle]It associates values with explicit keys, making the meaning of each log entry clearer and more parsable.
	~[moodle]It redirects logs to a central logging service automatically.#<p>Log redirection requires separate configuration.</p>
	####<p><strong>Explanation</strong>: Changing the Envoy access log format to JSON associates values with keys, significantly improving readability and parsability for automated tools compared to the default text format.</p>
}

// question: 10.8  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>To retrieve the cluster configuration from a specific Envoy proxy using istioctl, which subcommand should be used?</p>{
	~[moodle]istioctl proxy-config listeners.#<p>listeners retrieves listener configuration.</p>
	~[moodle]istioctl proxy-config routes.#<p>routes retrieves route configuration.</p>
	=[moodle]istioctl proxy-config clusters.
	~[moodle]istioctl proxy-config endpoints.#<p>endpoints retrieves endpoint configuration.</p>
	####<p><strong>Explanation</strong>: The istioctl proxy-config command has several subcommands, each corresponding to an Envoy xDS API. istioctl proxy-config clusters is used to retrieve the cluster configuration of a workload.</p>
}

// question: 10.9  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>What Envoy xDS API is responsible for dynamically configuring routing rules that map virtual hosts to clusters?</p>{
	~[moodle]CDS (Cluster Discovery Service).#<p>CDS configures the backend services (clusters).</p>
	~[moodle]EDS (Endpoint Discovery Service).#<p>EDS configures the instances or endpoints within a cluster.</p>
	~[moodle]LDS (Listener Discovery Service).#<p>LDS configures listeners that accept incoming connections.</p>
	=[moodle]RDS (Route Discovery Service).
	####<p><strong>Explanation</strong>: RDS (Route Discovery Service) is one of the xDS APIs that allows the control plane to dynamically configure Envoy's routing rules. These rules match virtual hosts to clusters and are processed in order to route traffic.</p>
}

// question: 10.10  name: Chapter 10: Troubleshooting the data plane
::Chapter 10\: Troubleshooting the data plane::[html]<p>After a misconfiguration leads to 504 Gateway Timeout errors, what combination of tools would be most effective for understanding the root cause, focusing on telemetry?</p>{
	~[moodle]kubectl logs and istioctl proxy-config secrets.#<p>kubectl logs might show some errors, but proxy-config secrets is for secret management.</p>
	~[moodle]Kiali's network graph and tcpdump.#<p>Kiali's graph is visual, and tcpdump inspects raw traffic, but they don't directly query aggregated telemetry for root cause analysis.</p>
	=[moodle]Grafana for success rates and Prometheus for querying affected Pods.
	~[moodle]istioctl analyze and openssl verify.#<p>analyze checks configuration validity, and openssl verify checks certificates, not telemetry for runtime errors.</p>
	####<p><strong>Explanation</strong>: To understand the root cause of 504 errors using telemetry, one would typically use Grafana to view the rate of failing requests (e.g., client success rate) and Prometheus to query affected Pods and their specific metrics, such as response_flags="UT" (upstream timeout), to identify misbehaving instances.</p>
}

// Chapter 11: Performance-tuning the control plane

// question: 11.1  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>What is the primary goal of the Istio control plane in relation to the data plane?</p>{
	~[moodle]To directly handle all network traffic between services.#<p>The data plane (Envoy proxy) handles network traffic.</p>
	=[moodle]To keep the data plane synchronized to the desired configuration state.
	~[moodle]To store all service metrics and trace data.#<p>Metrics and trace data are stored by separate observability components like Prometheus and Jaeger.</p>
	~[moodle]To provide a user interface for managing microservices.#<p>Kiali provides a user interface for managing the service mesh.</p>
	####<p><strong>Explanation</strong>: The primary goal for the control plane (Istiod) is to maintain a correctly behaving mesh by listening to events from Kubernetes and updating the data plane's configuration to reflect the latest desired state in a timely fashion.</p>
}

// question: 11.2  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>Which metric from Istiod is critical for measuring the time taken to distribute configuration changes to the data-plane proxies, often visualized in Grafana dashboards?</p>{
	~[moodle]pilot_services.#<p>pilot_services counts known services.</p>
	~[moodle]pilot_push_triggers.#<p>pilot_push_triggers indicates why configuration pushes occur.</p>
	=[moodle]pilot_proxy_convergence_time.
	~[moodle]pilot_inbound_updates.#<p>pilot_inbound_updates tracks inbound configuration updates to Istiod.</p>
	####<p><strong>Explanation</strong>: pilot_proxy_convergence_time is a key metric that measures how long it takes for configuration to be pushed and synchronized with the data-plane proxies. It is often visualized in the Istio Control Plane Dashboard as "Proxy Push Time".</p>
}

// question: 11.3  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>What is "phantom workloads" a common phenomenon of, when control plane performance degrades?</p>{
	~[moodle]Workloads that generate excessive network traffic.#<p>While a problem, it's not the definition of phantom workloads.</p>
	=[moodle]Services configured to route traffic to endpoints that no longer exist, causing requests to fail.
	~[moodle]Applications that appear to be running but are not processing any requests.#<p>This describes an unhealthy workload, not necessarily a phantom one.</p>
	~[moodle]Virtual machines that are not correctly integrated into the mesh.#<p>VM integration is a separate concern, though it can suffer from similar issues.</p>
	####<p><strong>Explanation</strong>: Phantom workloads are a common phenomenon when control plane performance degrades, where services are configured to route traffic to endpoints that are already long gone, leading to failed requests because the target no longer exists.</p>
}

// question: 11.4  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>Which of the following is NOT one of the four golden signals for monitoring the Istio control plane?</p>{
	~[moodle]Latency.#<p>Latency is a golden signal.</p>
	~[moodle]Saturation.#<p>Saturation is a golden signal.</p>
	=[moodle]Throughput.
	~[moodle]Errors.#<p>Errors are a golden signal.</p>
	####<p><strong>Explanation</strong>: The four golden signals for monitoring the control plane are Latency, Saturation, Traffic (load), and Errors. Throughput is a measure of traffic, but "Traffic" is the specific term used here, encompassing both incoming and outgoing load.</p>
}

// question: 11.5  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>How does the Sidecar resource primarily help in performance tuning the control plane?</p>{
	~[moodle]By increasing the CPU and memory allocated to Istiod replicas.#<p>This is scaling up, not directly related to the Sidecar resource's function.</p>
	=[moodle]By reducing the configuration size pushed to proxies by defining which services a workload can access.
	~[moodle]By enabling autoscaling for Istiod based on traffic load.#<p>Autoscaling for Istiod has specific challenges and isn't directly controlled by the Sidecar resource.</p>
	~[moodle]By ignoring all events from Kubernetes, thus reducing processing.#<p>Ignoring events uses discovery selectors, not the Sidecar resource.</p>
	####<p><strong>Explanation</strong>: The Sidecar resource allows fine-tuning of inbound and outbound traffic configuration for sidecar proxies. By explicitly defining the services a workload requires access to, it enables Istio's control plane to discern relevant configuration, significantly reducing the size of the configuration pushed to individual proxies and the number of pushes.</p>
}

// question: 11.6  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>When dealing with control plane saturation where the incoming traffic (configuration changes) is the bottleneck, what tuning approach is recommended?</p>{
	~[moodle]Scaling out Istiod by increasing replica count.#<p>Scaling out (increasing replicas) is more effective when the bottleneck is outgoing traffic (many pushes).</p>
	=[moodle]Scaling up Istiod by allocating more CPU and memory per instance.
	~[moodle]Reducing the PILOT_DEBOUNCE_AFTER period.#<p>Reducing the debounce period would likely increase the rate of pushes, exacerbating the problem.</p>
	~[moodle]Disabling all monitoring metrics.#<p>Disabling monitoring prevents diagnosis.</p>
	####<p><strong>Explanation</strong>: If the bottleneck is incoming traffic (many resources processed to generate Envoy configuration), scaling up Istiod by allocating more CPU and memory per instance is recommended to provide more processing power.</p>
}

// question: 11.7  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>What is the purpose of "namespace discovery selectors" in Istio 1.10, in the context of control plane performance?</p>{
	~[moodle]To automatically scale Istiod replicas based on namespace activity.#<p>Autoscaling is a separate feature.</p>
	~[moodle]To encrypt configuration data for specific namespaces.#<p>Encryption is handled by mTLS and identity management.</p>
	=[moodle]To fine-tune exactly which inbound events (from Pods, services, etc.) the control plane processes and cares about.
	~[moodle]To prioritize configuration pushes for critical namespaces.#<p>Prioritization is not the primary function of discovery selectors.</p>
	####<p><strong>Explanation</strong>: Namespace discovery selectors allow users to fine-tune exactly what inbound events the control plane processes, for example, by labeling namespaces (istio-discovery: enabled). This reduces strain on the control plane by ignoring events from irrelevant or highly churning namespaces.</p>
}

// question: 11.8  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>When should you consider modifying event batching properties (like PILOT_DEBOUNCE_AFTER) for Istio's control plane?</p>{
	~[moodle]Routinely, for every Istio installation.#<p>It's not a routine change due to potential risks.</p>
	=[moodle]Only when the control plane is saturated and already has significant resources allocated.
	~[moodle]Never, as it always leads to data plane staleness.#<p>It can lead to staleness if set too high, but can improve performance when tuned carefully.</p>
	~[moodle]When integrating virtual machines into the mesh.#<p>VM integration is a separate feature.</p>
	####<p><strong>Explanation</strong>: Modifying event batching is an advanced tuning technique that should only be considered when the control plane is saturated and you have already allocated a lot of resources to it. It helps reduce push counts by merging events.</p>
}

// question: 11.9  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>What is a recommended guideline for performance tuning Istio, especially after identifying a bottleneck?</p>{
	~[moodle]Make large, aggressive changes to properties to see a significant impact quickly.#<p>This is an aggressive approach that can have adverse effects.</p>
	~[moodle]Immediately double or quadruple debounce periods to prevent push spikes.#<p>This is an aggressive approach that can have adverse effects.</p>
	=[moodle]Make incremental changes (e.g., 10% to 30% adjustments) and monitor their effects over time.
	~[moodle]Rely solely on Istio's default settings as they are always optimal.#<p>While Istio is performant by default, tuning is often necessary for specific organizational needs and scale.</p>
	####<p><strong>Explanation</strong>: The guideline emphasizes making incremental changes (e.g., 10% to 30% adjustments) after identifying a bottleneck, monitoring benefits or degradation for a few days, and then making informed decisions based on new data. This cautious approach is safer than making big changes.</p>
}

// question: 11.10  name: Chapter 11: Performance-tuning the control plane
::Chapter 11\: Performance-tuning the control plane::[html]<p>According to Istio's performance tests, how many virtual cores and memory does a single Istio Pilot instance typically consume to synchronize a mesh with 1,000 Kubernetes services and 2,000 workloads at 70,000 requests per second?</p>{
	~[moodle]4 virtual cores and 8 GB of memory.#<p>This value is too high compared to the published performance metrics.</p>
	=[moodle]1 virtual core and 1.5 GB of memory.
	~[moodle]10 virtual cores and 16 GB of memory.#<p>This value is too high compared to the published performance metrics.</p>
	~[moodle]Less than 0.5 virtual cores and 512 MB of memory.#<p>This value is too low compared to the published performance metrics.</p>
	####<p><strong>Explanation</strong>: Istio's performance tests show that synchronizing a mesh with 1,000 Kubernetes services and 2,000 workloads at 70,000 requests per second consumes only one virtual core and 1.5 GB of memory for a single Istio Pilot instance.</p>
}

// Chapter 12: Scaling Istio in your organization

// question: 12.1  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>What is a key benefit of adopting a multi-cluster service mesh compared to running all services in a single, large cluster?</p>{
	~[moodle]Reduced operational complexity due to fewer components.#<p>Multi-cluster setups often increase operational complexity, though Istio aims to simplify it.</p>
	=[moodle]Improved blast radius containment, as outages are scoped to individual clusters.
	~[moodle]Elimination of all network latency between services.#<p>Network latency can still exist, especially across different networks or regions.</p>
	~[moodle]Guaranteed 100% uptime for all applications.#<p>No architecture can guarantee 100% uptime, but multi-cluster setups improve availability.</p>
	####<p><strong>Explanation</strong>: One of the main benefits of using multiple, smaller clusters for a service mesh is improved blast radius containment. This means that outages are scoped to the clusters in which they occur, preventing a single failure from impacting the entire system.</p>
}

// question: 12.2  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>Which Istio multi-cluster deployment model involves a single control plane managing the mesh, with other clusters acting as remote clusters?</p>{
	~[moodle]Primary-Primary.#<p>Primary-Primary involves multiple control planes.</p>
	~[moodle]External Control Plane.#<p>External Control Plane has all clusters remote to the control plane.</p>
	=[moodle]Shared Control Plane (Primary-Remote).
	~[moodle]Replicated Control Plane.#<p>Replicated Control Plane involves multiple control planes.</p>
	####<p><strong>Explanation</strong>: The Primary-Remote deployment model, also known as the single control plane or shared control plane, has a single control plane (Istiod) managing the mesh, with other clusters joining it as remote clusters.</p>
}

// question: 12.3  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>How does Istio facilitate workload discovery in multi-cluster deployments with replicated control planes (Primary-Primary model)?</p>{
	~[moodle]By requiring manual configuration of each service's IP address in every cluster.#<p>Manual configuration is error-prone and doesn't scale.</p>
	=[moodle]By using service account credentials from remote clusters as secrets in the primary cluster to query workload information.
	~[moodle]By relying solely on DNS resolution provided by Kubernetes.#<p>While DNS is used, Istio needs to populate its service registry with cross-cluster services.</p>
	~[moodle]By broadcasting service endpoints to all connected clusters via a mesh-wide event bus.#<p>This isn't the primary mechanism; secure querying of the Kubernetes API is used.</p>
	####<p><strong>Explanation</strong>: In replicated control plane models, Istiod instances use service account credentials from remote clusters (stored as Kubernetes secrets) to query workload information (like Pods, Services, Endpoints) from the remote Kubernetes API servers, enabling cross-cluster workload discovery.</p>
}

// question: 12.4  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>What are "east-west gateways" in a multi-network, multi-cluster Istio setup?</p>{
	~[moodle]Gateways specifically for traffic originating from outside the organization (internet).#<p>Traffic from outside (internet) is typically north-south traffic handled by standard ingress gateways.</p>
	=[moodle]Special Istio ingress gateways that bridge clusters in different internal networks by proxying cross-cluster traffic.
	~[moodle]External API gateways that manage north-south traffic exclusively.#<p>API gateways can be used, but east-west gateways are Istio-specific components for inter-cluster traffic.</p>
	~[moodle]Gateways that only handle UDP traffic between services.#<p>East-west gateways handle various protocols, including mTLS traffic over TCP.</p>
	####<p><strong>Explanation</strong>: East-west gateways are special Istio ingress gateways located at the edge of internal networks. They are used to bridge clusters in multi-network meshes by proxying cross-cluster traffic, enabling connectivity when direct network peering is not possible.</p>
}

// question: 12.5  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>What is the sni-dnat router mode used for when configuring an east-west gateway in Istio?</p>{
	~[moodle]To disable SNI-based routing for security reasons.#<p>It enables SNI-based routing.</p>
	=[moodle]To automatically configure SNI clusters for proxying cross-cluster traffic in a fine-grained manner.
	~[moodle]To force all cross-cluster traffic to use clear-text HTTP.#<p>East-west gateways route encrypted (mTLS) traffic.</p>
	~[moodle]To only allow connections from specific IP ranges to the gateway.#<p>IP-based access control is handled by authorization policies or network policies.</p>
	####<p><strong>Explanation</strong>: Setting the ISTIO_META_ROUTER_MODE environment variable to sni-dnat for an east-west gateway automatically configures SNI clusters. This allows the gateway to read cluster information from the SNI header of incoming mTLS traffic and proxy it to the intended workload across clusters.</p>
}

// question: 12.6  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>To establish common trust between clusters in a multi-cluster Istio mesh, what is a recommended approach for configuring CA certificates?</p>{
	~[moodle]Generating a new root CA certificate for each cluster independently.#<p>Independent CAs would prevent common trust.</p>
	~[moodle]Manually distributing individual service certificates to all workloads.#<p>Manual distribution is not scalable or automated.</p>
	=[moodle]Using plug-in CA certificates (intermediate CAs and a shared root CA) stored as secrets in the istio-system namespace.
	~[moodle]Relying on self-signed certificates for all inter-cluster communication.#<p>Self-signed certificates lack a common trust root.</p>
	####<p><strong>Explanation</strong>: Common trust across clusters can be established using plug-in CA certificates. This involves creating a shared root CA and intermediate CAs for each cluster, then storing these CA certificates (as a secret named cacerts) in the istio-system namespace, which Istio's CA picks up for signing workload certificates.</p>
}

// question: 12.7  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>When setting up a multi-cluster Istio mesh, how does Istio gain an understanding of the network topology (e.g., west-network, east-network)?</p>{
	~[moodle]By inspecting the Kubernetes Pod IPs and automatically inferring their network.#<p>Automatic inference is less reliable than explicit configuration.</p>
	~[moodle]By requiring manual definition of network zones in the VirtualService resources.#<p>Network information is configured at the mesh level, not typically in VirtualService for topology awareness.</p>
	=[moodle]By labeling the Istio installation namespace with network topology information (e.g., topology.istio.io/network).
	~[moodle]By integrating with an external network management system.#<p>While possible for advanced cases, labeling the namespace is the simpler, standard approach.</p>
	####<p><strong>Explanation</strong>: Istio understands the network topology by labeling the Istio installation namespace (e.g., istio-system) with network information using labels like topology.istio.io/network. This metadata allows Istio to configure workloads to prioritize routing traffic locally or use east-west gateways for remote networks.</p>
}

// question: 12.8  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>In a multi-cluster, multi-network setup, what is the default load-balancing algorithm Istio uses when routing traffic between services across clusters?</p>{
	~[moodle]Least Connection.#<p>This is an alternative load balancing strategy.</p>
	~[moodle]Random.#<p>This is an alternative load balancing strategy.</p>
	=[moodle]Round Robin.
	~[moodle]Locality-aware.#<p>Locality-aware load balancing is enabled by default, but it prioritizes local endpoints; if all are equal and healthy across clusters, round-robin is still the base algorithm.</p>
	####<p><strong>Explanation</strong>: By default, Istio load-balances between workloads using the round-robin algorithm, which distributes traffic equally across available endpoints, including those in different clusters after cross-cluster discovery is enabled.</p>
}

// question: 12.9  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>What happens when an AuthorizationPolicy is applied to a service in one cluster that denies traffic from non-ingress sources, and a workload from another cluster attempts to communicate with it?</p>{
	~[moodle]The request will always be allowed due to cross-cluster trust.#<p>Trust is a prerequisite for authorization, not a bypass.</p>
	=[moodle]The request will be denied if it does not originate from an authorized source, such as the Istio ingress gateway.
	~[moodle]The request will bypass the policy due to being from a different cluster.#<p>Policies are enforced regardless of cluster origin.</p>
	~[moodle]The authorization policy will be ignored because mTLS is already established.#<p>mTLS provides authentication, but authorization determines access after authentication.</p>
	####<p><strong>Explanation</strong>: Istio's capabilities, including access control via AuthorizationPolicy, work across clusters in the same way they do within a single cluster. If a policy denies traffic from non-ingress sources, requests from other clusters (unless they originate from an authorized ingress gateway) will be denied. Mutual authentication provides reliable identity, but authorization policies define what an authenticated identity can do.</p>
}

// question: 12.10  name: Chapter 12: Scaling Istio in your organization
::Chapter 12\: Scaling Istio in your organization::[html]<p>In the primary-primary deployment model for a multi-cluster mesh, what is a key trade-off for its higher availability?</p>{
	~[moodle]It requires fewer computational resources.#<p>It consumes more resources, not fewer.</p>
	~[moodle]It scopes outages to the clusters in which they occur.#<p>This is a benefit, not a trade-off.</p>
	=[moodle]It incurs higher resource consumption due to multiple control planes.
	~[moodle]It mandates the use of an external certificate authority.#<p>While external CAs can be integrated, they are not strictly mandated by this deployment model.</p>
	####<p><strong>Explanation</strong>: The primary-primary (replicated control plane) deployment model provides higher availability because outages are scoped to individual clusters. However, its trade-off is that it requires more resources, as there are multiple Istio control planes running.</p>
}

// Chapter 13: Incorporating virtual machine workloads into the mesh

// question: 13.1  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>What is one of the key reasons enterprises might integrate Virtual Machines (VMs) into an Istio service mesh instead of migrating them entirely to Kubernetes?</p>{
	~[moodle]VMs offer superior performance compared to containers for all workloads.#<p>Performance depends on workload and configuration; containers are often preferred for specific use cases.</p>
	=[moodle]Regulatory compliance might require workloads to run on-premises in VMs.
	~[moodle]Kubernetes is not compatible with modern application frameworks.#<p>Kubernetes is designed for modern cloud-native applications.</p>
	~[moodle]VM integration completely eliminates the need for any application-level networking logic.#<p>While Istio offloads much networking logic, applications still have some responsibilities.</p>
	####<p><strong>Explanation</strong>: Enterprises often have to run workloads on-premises due to regulatory compliance or other constraints, where they might lack the expertise to set up and operate Kubernetes clusters, making VM integration into Istio a viable solution.</p>
}

// question: 13.2  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>Which three key features were implemented to simplify Istio's VM support, graduating it to beta in Istio 1.9.0?</p>{
	~[moodle]Automatic VM provisioning, dynamic IP allocation, and cloud-native storage.#<p>These are not core Istio features for VMs or general cloud/Kubernetes concepts.</p>
	=[moodle]Simplified sidecar proxy installation, VM high availability via WorkloadGroup/WorkloadEntry, and DNS resolution using a local DNS proxy.
	~[moodle]Native Kubernetes scheduling for VMs, integrated CI/CD pipelines, and unified log aggregation.#<p>These are not core Istio features for VMs or general cloud/Kubernetes concepts.</p>
	~[moodle]Hardware emulation, bare-metal access, and operating system virtualization.#<p>These are not core Istio features for VMs or general cloud/Kubernetes concepts.</p>
	####<p><strong>Explanation</strong>: Key features that improved Istio's VM support include simplified sidecar proxy installation and configuration using istioctl, VM high availability achieved by introducing WorkloadGroup and WorkloadEntry resources, and DNS resolution of in-mesh services from VMs using a local DNS proxy.</p>
}

// question: 13.3  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>What is the mechanism Istio uses to provision identity for VMs, particularly when Kubernetes is the source of trust?</p>{
	~[moodle]VMs are assigned a static IP that serves as their identity.#<p>This is not the mechanism Istio uses for VM identity provisioning.</p>
	=[moodle]A token is generated in Kubernetes, transferred securely to the VM, and used by istio-agent to authenticate to Istiod.
	~[moodle]VMs use hardcoded API keys to identify themselves to the control plane.#<p>This is not the mechanism Istio uses for VM identity provisioning.</p>
	~[moodle]Identity is automatically derived from the VM's hostname.#<p>This is not the mechanism Istio uses for VM identity provisioning.</p>
	####<p><strong>Explanation</strong>: When Kubernetes is the source of trust, Istio provisions VM identity by generating a token in Kubernetes (e.g., using a service account), which is then manually or securely transferred to the VM. The istio-agent in the VM picks up this token to authenticate to Istiod, which then issues an SVID (SPIFFE Verifiable Identity Document) for the VM.</p>
}

// question: 13.4  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>Which Istio resource is analogous to Kubernetes Deployments, defining common properties and a template for a group of VM workloads it manages?</p>{
	~[moodle]WorkloadEntry.#<p>WorkloadEntry represents individual VM instances within a WorkloadGroup.</p>
	~[moodle]ServiceEntry.#<p>ServiceEntry is for adding external services to the mesh.</p>
	=[moodle]WorkloadGroup.
	~[moodle]VirtualService.#<p>VirtualService is for traffic routing.</p>
	####<p><strong>Explanation</strong>: The WorkloadGroup resource is similar to Kubernetes Deployments. It defines the template for how VM workloads it manages are configured, specifying common properties like ports, labels, service accounts for identity, and health probe configurations.</p>
}

// question: 13.5  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>What role does the istio-agent play in a VM joining the service mesh?</p>{
	~[moodle]It runs the main application code on the VM.#<p>The application code is separate from the istio-agent.</p>
	~[moodle]It provides a web UI for monitoring the VM's health.#<p>Monitoring is typically done via external tools.</p>
	=[moodle]It starts the Envoy proxy, bootstraps its identity, maintains a connection with the control plane, and applies configuration.
	~[moodle]It replaces the operating system's kernel on the VM.#<p>This is incorrect; the istio-agent runs as a process on the OS.</p>
	####<p><strong>Explanation</strong>: The istio-agent (also known as the pilot agent) has several important functions: starting the Envoy proxy within the sidecar, bootstrapping its identity, maintaining a bidirectional connection with the control plane to receive mesh configuration, and applying that configuration to Envoy.</p>
}

// question: 13.6  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>When the VM and the cluster are in separate networks, how are Istiod and cluster services exposed to the VM to allow it to become part of the mesh?</p>{
	~[moodle]By directly connecting the VM's private IP to Istiod's private IP.#<p>Direct private IP connection is possible only in flat networks.</p>
	~[moodle]By requiring the VM to run a full Kubernetes API server.#<p>This is overly complex and not how Istio integrates VMs.</p>
	=[moodle]Through an east-west gateway that proxies traffic between the VM and the cluster.
	~[moodle]By installing a separate Istio control plane on the VM.#<p>This is overly complex and not how Istio integrates VMs.</p>
	####<p><strong>Explanation</strong>: If the VM and the cluster are in separate networks, an east-west gateway is required to proxy traffic to the Istio control plane (Istiod) and other cluster services. This gateway acts as a bridge, allowing the VM to connect to the mesh.</p>
}

// question: 13.7  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>What is the ISTIO_META_DNS_CAPTURE proxy metadata flag used for in Istio's VM integration?</p>{
	~[moodle]To disable DNS resolution entirely on the VM.#<p>It enables redirection, not disabling.</p>
	=[moodle]To ensure that DNS queries from the VM are captured and redirected to the local DNS proxy.
	~[moodle]To prevent the VM from making any outbound network calls.#<p>It's for DNS resolution, not general outbound traffic control.</p>
	~[moodle]To encrypt all DNS traffic originating from the VM.#<p>It redirects queries, but doesn't inherently encrypt them, though traffic to Istiod is mTLS.</p>
	####<p><strong>Explanation</strong>: The ISTIO_META_DNS_CAPTURE: "true" flag in the proxy metadata ensures that DNS queries originating from the VM are captured and redirected to the local DNS proxy running within the istio-agent sidecar for resolution.</p>
}

// question: 13.8  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>What is the difference between a WorkloadGroup and a WorkloadEntry in Istio's VM support?</p>{
	~[moodle]WorkloadGroup is for containerized workloads, while WorkloadEntry is for VMs.#<p>Both are for VM workloads.</p>
	=[moodle]WorkloadGroup defines the template for a group of VM workloads, and WorkloadEntry represents an individual VM instance with specific network attributes.
	~[moodle]WorkloadGroup is a policy for traffic management, and WorkloadEntry is for service discovery.#<p>WorkloadGroup is more than a policy, and WorkloadEntry provides specific endpoint details for service discovery.</p>
	~[moodle]WorkloadGroup is a legacy resource, while WorkloadEntry is a modern replacement.#<p>Both are current resources for VM integration.</p>
	####<p><strong>Explanation</strong>: A WorkloadGroup defines the common properties for a group of VM workloads (like a Deployment for Pods), acting as a template. A WorkloadEntry represents an individual instance of a VM workload within that group, including its specific IP address and health status.</p>
}

// question: 13.9  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>When integrating a VM into the mesh, what needs to be statically resolved in the VM's hosts file for the istio-agent to connect to Istiod initially, especially in multi-network setups?</p>{
	~[moodle]The public IP of the Kubernetes API server.#<p>The agent needs to talk to Istiod, not directly the Kubernetes API server.</p>
	=[moodle]The hostname istiod.istio-system.svc to the east-west gateway's IP address.
	~[moodle]The local IP address of the istio-agent itself.#<p>This is a local address and not helpful for external connectivity.</p>
	~[moodle]The hostname of the application running on the VM.#<p>This is the application's hostname, not Istiod's.</p>
	####<p><strong>Explanation</strong>: To enable the istio-agent to connect to Istiod when the VM is in a separate network, the VM's system hosts file is configured with a static entry that resolves the hostname istiod.istio-system.svc to the IP address of the east-west gateway, which then proxies the request to the Istiod instances.</p>
}

// question: 13.10  name: Chapter 13: Incorporating virtual machine workloads into the mesh
::Chapter 13\: Incorporating virtual machine workloads into the mesh::[html]<p>After a VM workload is registered and marked healthy in the mesh, what happens to the traffic flow from cluster services to this VM workload?</p>{
	~[moodle]Traffic is blocked due to security policies.#<p>Traffic is allowed once healthy.</p>
	=[moodle]Istiod configures the data plane to route traffic to the VM's endpoint.
	~[moodle]All traffic is redirected to another VM for load balancing.#<p>Traffic is routed based on Istio policies, not arbitrarily redirected.</p>
	~[moodle]The VM application must manually pull traffic from the cluster.#<p>Istio handles traffic routing transparently for the application.</p>
	####<p><strong>Explanation</strong>: Once a WorkloadEntry is healthy, Istiod configures the data plane (Envoy proxies) with its endpoint, allowing traffic from cluster services to be routed to the forum workload in the VM. This ensures that clients send traffic only to healthy instances.</p>
}

// Chapter 14: Extending Istio on the request path

// question: 14.1  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>What is the fundamental architecture of Envoy built around, which allows for its extensive extension capabilities?</p>{
	~[moodle]A monolithic, unchangeable core.#<p>Envoy is designed for modularity and extension, not a monolithic core.</p>
	=[moodle]Listeners and a chain of modular filters.
	~[moodle]Static configuration files and a fixed set of protocols.#<p>While it can use static config, its power comes from dynamic configuration and extensibility.</p>
	~[moodle]Direct integration with Kubernetes controllers.#<p>Envoy interacts with Kubernetes via Istio, but its internal architecture is distinct.</p>
	####<p><strong>Explanation</strong>: Envoy's internal architecture is fundamentally built around listeners (which accept incoming connections) and a chain of modular filters (network filters, HTTP filters). This filter chain architecture enables its extensive extension capabilities, allowing custom logic or existing functionality to be inserted into the request path.</p>
}

// question: 14.2  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>Which Istio resource is considered a "break glass" solution for advanced users, allowing direct configuration of Envoy's HTTP filter chain?</p>{
	~[moodle]VirtualService.#<p>VirtualService is for traffic routing.</p>
	~[moodle]DestinationRule.#<p>DestinationRule is for load balancing and resilience.</p>
	=[moodle]EnvoyFilter.
	~[moodle]ServiceEntry.#<p>ServiceEntry is for external services.</p>
	####<p><strong>Explanation</strong>: The EnvoyFilter resource is intended for advanced usage and is described as a "break glass" solution. It allows direct configuration of Envoy's filters and filter chains, enabling fine-grained customization of the data plane, but requires familiarity with Envoy's configuration specifics.</p>
}

// question: 14.3  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>What is the "tap filter" in Envoy, and how can it be used in Istio for debugging?</p>{
	~[moodle]It buffers all traffic for later replay.#<p>While it might buffer for streaming, its primary purpose is inspection.</p>
	~[moodle]It dynamically changes HTTP methods in requests.#<p>It's for observation, not modification of requests.</p>
	=[moodle]It allows streaming of requests and responses (headers, body, trailers) unmodified to a listening agent for introspection.
	~[moodle]It performs real-time traffic shifting based on request attributes.#<p>Traffic shifting is done via VirtualService.</p>
	####<p><strong>Explanation</strong>: Envoy's tap filter (envoy.filters.http.tap) allows streaming of requests and responses (including headers, body, and trailers) unmodified to a listening agent. This provides a powerful way to debug and introspect the data plane without impacting client or upstream services.</p>
}

// question: 14.4  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>When implementing service-side rate limiting with an external call-out in Istio, which component typically stores the rate-limit counters to ensure global rate limiting across multiple service replicas?</p>{
	~[moodle]Each service proxy's local memory.#<p>Local memory would not provide global consistency across replicas.</p>
	=[moodle]A distributed backend global key-value store like Redis.
	~[moodle]The Kubernetes API server.#<p>The Kubernetes API server is for cluster management, not real-time rate limit counters.</p>
	~[moodle]The client application itself.#<p>The client application is typically unaware of the service's rate limiting policies.</p>
	####<p><strong>Explanation</strong>: For service-side rate limiting with an external call-out, the rate-limit server (RLS) typically communicates with a distributed backend global key-value store, such as Redis or Memcache, to store rate-limit counters. This ensures that rate limits are enforced consistently across all replicas of a service.</p>
}

// question: 14.5  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>What programming language is commonly used with Envoy's Lua filter to implement custom logic on the request path?</p>{
	~[moodle]Java.#<p>While other languages are used for Wasm filters, Lua is specific to the Lua filter.</p>
	~[moodle]Python.#<p>While other languages are used for Wasm filters, Lua is specific to the Lua filter.</p>
	=[moodle]Lua scripting language.
	~[moodle]Go.#<p>While other languages are used for Wasm filters, Lua is specific to the Lua filter.</p>
	####<p><strong>Explanation</strong>: Envoy has a Lua filter that allows users to customize the behavior of the request or response path by writing and injecting Lua scripts into the proxy. These scripts can manipulate headers, inspect bodies, and make call-outs to other services.</p>
}

// question: 14.6  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>Why is WebAssembly (Wasm) considered a beneficial approach for writing new Envoy filters in Istio, compared to writing native Envoy filters?</p>{
	~[moodle]Wasm filters offer significantly higher performance than native C++ filters.#<p>While performant, Wasm's main advantage is flexibility and dynamic loading, not necessarily higher performance than optimized native C++.</p>
	~[moodle]Wasm modules can only be written in C++.#<p>This is incorrect; Wasm supports multiple languages.</p>
	=[moodle]Wasm allows writing filters in multiple languages (e.g., AssemblyScript, Rust) and dynamically loading them into the proxy without rebuilding Envoy.
	~[moodle]Wasm completely eliminates the need for Envoy proxies.#<p>Wasm extends Envoy, it doesn't replace it.</p>
	####<p><strong>Explanation</strong>: Wasm is beneficial because it allows developers to write Envoy filters in various supported languages (like C++, Rust, AssemblyScript, TinyGo) and dynamically load these modules into the proxy at runtime. This avoids the need to statically build changes into a custom C++ Envoy binary.</p>
}

// question: 14.7  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>Which Istio resource is used to declaratively deploy a WebAssembly (Wasm) filter module to workloads running in the service mesh?</p>{
	~[moodle]EnvoyFilter.#<p>EnvoyFilter is for direct Envoy configuration, but WasmPlugin is specific for Wasm modules.</p>
	=[moodle]WasmPlugin.
	~[moodle]Sidecar.#<p>Sidecar configures inbound/outbound traffic policies.</p>
	~[moodle]ServiceEntry.#<p>ServiceEntry is for external services.</p>
	####<p><strong>Explanation</strong>: Istio introduced the WasmPlugin resource (extensions.istio.io/v1alpha1) to declaratively load WebAssembly filters into the Istio data plane. This resource specifies the workload selector and the module URL (OCI, file, or HTTPS).</p>
}

// question: 14.8  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>When configuring a rate-limit service (RLS) with Envoy in Istio, what does Envoy terminology refer to the configuration for sending specific attributes for a particular request path as?</p>{
	~[moodle]Rate-limit policies.#<p>Policies are broader rules.</p>
	=[moodle]Rate-limit actions.
	~[moodle]Rate-limit descriptors.#<p>Descriptors are part of the RLS configuration, defining the rules.</p>
	~[moodle]Rate-limit thresholds.#<p>Thresholds are values within the rules.</p>
	####<p><strong>Explanation</strong>: Envoy terminology refers to the configuration specifying which attributes to send for a particular request, for the purpose of rate limiting, as "rate-limit actions." These actions define how the request path is processed to extract attributes (e.g., headers, path) that the RLS then evaluates against its rules.</p>
}

// question: 14.9  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>What is the purpose of Envoy's HttpConnectionManager (HCM) network filter?</p>{
	~[moodle]To provide service discovery for upstream services.#<p>Service discovery is a broader Envoy feature, but HCM focuses on HTTP processing and routing.</p>
	=[moodle]To convert a stream of bytes into HTTP requests and route them based on L7 properties.
	~[moodle]To manage mutual TLS certificates for all services.#<p>TLS management is part of the security features, often configured by Istiod, not HCM directly.</p>
	~[moodle]To offload all application-level business logic.#<p>HCM handles networking concerns, not application business logic.</p>
	####<p><strong>Explanation</strong>: HttpConnectionManager (HCM) is a popular and useful Envoy network filter. Its purpose is to convert a stream of bytes into higher-level HTTP (HTTP/1, HTTP/2) requests and route them based on Layer 7 properties, such as headers or body details.</p>
}

// question: 14.10  name: Chapter 14: Extending Istio on the request path
::Chapter 14\: Extending Istio on the request path::[html]<p>When using EnvoyFilter to add an HTTP filter, where in the filter chain is the filter typically inserted, relative to other existing filters like the http.filters.http.router?</p>{
	~[moodle]Always at the very beginning of the chain.#<p>While possible, it's not always the case; precise placement is a key feature.</p>
	~[moodle]Always at the very end of the chain.#<p>While possible, it's not always the case; precise placement is a key feature.</p>
	=[moodle]At a specific position, such as INSERT_BEFORE or INSERT_AFTER a named filter.
	~[moodle]Randomly, determined by Envoy at runtime.#<p>Envoy configurations are deterministic, not random.</p>
	####<p><strong>Explanation</strong>: When patching the Envoy configuration with an EnvoyFilter, you specify where in the filter chain the new configuration should apply (e.g., applyTo: HTTP_FILTER). The patch section allows precise placement using operations like INSERT_BEFORE or INSERT_AFTER a specific named filter (e.g., envoy.filters.http.router).</p>
}