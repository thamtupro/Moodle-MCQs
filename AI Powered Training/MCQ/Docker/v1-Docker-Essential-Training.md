// Chapter 1: Overview and Core Concepts of Docker
// question: 1.1  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>Which problem does Docker primarily solve in application development and deployment?</p>{
	~[moodle]Managing distributed databases and data synchronization.#<p>Managing distributed databases is not Docker's primary goal; Docker focuses on packaging and running applications.</p>
	=[moodle]Ensuring applications operate consistently across different environments.
	~[moodle]Optimizing hardware performance through full system virtualization.#<p>Docker does not optimize hardware performance through full system virtualization; that is the role of virtual machines (VMs) and hypervisors. Docker uses Linux kernel features to create lighter virtual operating system instances.</p>
	~[moodle]Compiling source code from various programming languages into a common format.#<p>Docker is not a multi-language source code compilation tool. It focuses on packaging and deploying compiled applications.</p>
	####<p><strong>Explanation</strong>\: Docker solves the challenge of making code work correctly on multiple machines by ensuring the application behaves the same regardless of the host machine running it. Problems include differences in operating systems, assumptions about hardware files or other attributes, or dependencies on specific hardware.</p>
}

// question: 1.2  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>What is the main difference between Docker containers and virtual machines (VMs)?</p>{
	~[moodle]VMs do not need their own operating system, while containers do.#<p>Virtual machines require their own operating system, while containers leverage the host operating system's kernel features to create virtual environments.</p>
	~[moodle]Containers emulate physical hardware, while VMs do not.#<p>Containers do not emulate hardware; they use the host's hardware. Virtual machines are what emulate hardware through a hypervisor.</p>
	=[moodle]Containers run only a single application and use the same hardware as the host, while VMs are complete computers that can run multiple applications and do not interact directly with the host.
	~[moodle]VMs use Dockerfiles for configuration, while containers use hypervisors.#<p>Dockerfile is used to configure and build Docker images for containers. Virtual machines do not use Dockerfiles. Hypervisors are used by virtual machines, not containers.</p>
	####<p><strong>Explanation</strong>\: Containers do not emulate hardware but use the same hardware as other applications on the host. They are designed to run only one application at a time. In contrast, virtual machines use a hypervisor to connect software-emulated hardware to the actual hardware below, acting like real computers and capable of running multiple applications at once without direct interaction with the host.</p>
}

// question: 1.3  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>What are the two core components that Docker uses to package and run applications?</p>{
	~[moodle]YAML configuration files and installation directories.#<p>YAML configuration files (e.g., Docker Compose) and installation directories are supporting tools but not core components of Docker.</p>
	~[moodle]Dockerfile and Container Registry.#<p>Dockerfile is a configuration file used to create images, and Container Registry is a place to share and store images. These are important factors that make Docker easier to use, but images and containers are the two most fundamental components.</p>
	~[moodle]Hypervisors and guest operating systems.#<p>Hypervisors and guest operating systems are components of virtual machines, not Docker containers.</p>
	=[moodle]Images and Containers.
	####<p><strong>Explanation</strong>\: Docker uses images and containers to package and run applications anywhere.</p>
}

// question: 1.4  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>What is a Dockerfile described as in the context of Docker?</p>{
	~[moodle]A command-line tool for managing network services.#<p>A Dockerfile is not a command-line tool.</p>
	=[moodle]A lightweight configuration file format for building and configuring container images.
	~[moodle]A standard communication protocol between containers.#<p>A Dockerfile is not a communication protocol; it is a configuration file.</p>
	~[moodle]A persistent data storage mechanism for applications.#<p>A Dockerfile is not a data storage mechanism; Volumes or bind mounts fulfill that role.</p>
	####<p><strong>Explanation</strong>\: A Dockerfile is a lightweight configuration file format used to build and configure applications into Docker images.</p>
}

// question: 1.5  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>Which two Linux kernel features do Docker containers use to create virtual operating system instances?</p>{
	~[moodle]Swap space and temporary file systems.#<p>These are concepts related to the Linux kernel but are not the two core features used by Docker to create lightweight virtualization like cgroups and namespaces.</p>
	~[moodle]Kernel modules and system calls.#<p>These are concepts related to the Linux kernel but are not the two core features used by Docker to create lightweight virtualization like cgroups and namespaces.</p>
	=[moodle]Control groups (cgroups) and namespaces.
	~[moodle]Interrupt handlers and device drivers.#<p>These are concepts related to the Linux kernel but are not the two core features used by Docker to create lightweight virtualization like cgroups and namespaces.</p>
	####<p><strong>Explanation</strong>\: Containers combine control groups (cgroups) and namespaces – two Linux kernel features – to create virtual operating system instances.</p>
}

// question: 1.6  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>Which of the following is NOT one of the three main ways Docker makes container and image concepts easier to use and understand?</p>{
	~[moodle]Configuring containers and images with Dockerfile.
	~[moodle]Sharing images via Container Registry.
	=[moodle]Tight integration with popular hypervisors.
	~[moodle]Providing an easy-to-use command-line interface (CLI).
	####<p><strong>Explanation</strong>\: Docker makes concepts easier to use by: 1) configuring with Dockerfile, 2) sharing images via Container Registry, and 3) providing a powerful CLI. Docker does not tightly integrate with hypervisors because it does not use them to create containers.</p>
}

// question: 1.7  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>What is the main function of Control groups (cgroups) in the context of Docker containers?</p>{
	~[moodle]Defining the resources a container can access on the host system.#<p>This function belongs to namespaces, not control groups.</p>
	=[moodle]Limiting the specific amount of resources a container can consume.
	~[moodle]Creating a complete copy of the operating system for each container.#<p>Control groups do not create an operating system copy; that is the overall result of the combination of cgroups and namespaces.</p>
	~[moodle]Ensuring secure network communication between different containers.#<p>Control groups are not directly related to ensuring secure network communication; that is a separate aspect of Docker networking.</p>
	####<p><strong>Explanation</strong>\: Control groups (cgroups) dictate the specific amount of resources that containers can consume.</p>
}

// question: 1.8  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>What is the main role of Namespaces in the context of Docker containers?</p>{
	~[moodle]Limiting the CPU and memory usage of a container.#<p>This function belongs to control groups.</p>
	=[moodle]Specifying what resources a container can access on a Linux system.
	~[moodle]Controlling access to fake root directories.#<p>Namespaces help create isolation, including for the file system, but the main role is to regulate general resource access.</p>
	~[moodle]Defining the data storage format of image layers.#<p>The data storage format of image layers is managed by storage drivers (e.g., OverlayFS), not namespaces.</p>
	####<p><strong>Explanation</strong>\: Namespaces specify what a container can access on a Linux system.</p>
}

// question: 1.9  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>What is the relationship between Container Runtimes and Container Engines?</p>{
	=[moodle]Container Runtimes are part of Container Engines, providing functionality to create, manage, and delete containers, while Engines provide the overall experience around container usage and interaction APIs.
	~[moodle]Container Engines are used to emulate hardware, while Container Runtimes manage guest operating systems.#<p>This is an incorrect description of both concepts; hardware emulation is related to virtual machines.</p>
	~[moodle]They are completely interchangeable terms and have identical functions.#<p>As stated, they are similar but not technically identical.</p>
	~[moodle]Container Runtimes only work on Windows, while Container Engines only work on Linux.#<p>This is a false operating system limitation; both operate on multiple operating systems.</p>
	####<p><strong>Explanation</strong>\: While these terms are often used interchangeably in communication, they are not entirely the same. Container runtimes create, manage, and delete containers. Container engines work with container runtimes to provide components and tools that make container management easier, including pulling images from registries and providing APIs for interacting with containers.</p>
}

// question: 1.10  name: Chapter 1: Overview and Core Concepts of Docker
::Chapter 1\: Overview and Core Concepts of Docker::[html]<p>What is runc and what is its role in Docker?</p>{
	~[moodle]runc is a network management tool for Docker containers.#<p>runc is not a network management tool.</p>
	~[moodle]runc is a type of hypervisor used by Docker to virtualize the entire host.#<p>runc is a container runtime, not a hypervisor, and it does not virtualize the entire host.</p>
	=[moodle]runc is Docker's original container controller and one of the most popular OCI-compliant runtimes.
	~[moodle]runc is a programming language used to write Dockerfiles.#<p>runc is not a programming language; Dockerfile is a configuration language for images.</p>
	####<p><strong>Explanation</strong>\: runc is Docker's original container controller (container runtime). It is one of the most popular OCI (Open Container Initiative) compliant runtimes.</p>
}

// Chapter 2: Container Creation Process and Docker File Structure
// question: 2.1  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>What was the first step in the manual container creation process before Docker became popular?</p>{
	~[moodle]Assigning the container to a control group.#<p>Assigning to a control group is for resource limiting, which happens after namespaces are created.</p>
	=[moodle]Mounting a directory for the container's file system.
	~[moodle]Using the chroot command to set up a fake file system.#<p>The chroot command is used to set the created directory as the fake file system, which happens after the user namespace is created.</p>
	~[moodle]Creating a user namespace using unshare.#<p>Creating a user namespace is the second step after mounting the directory.</p>
	####<p><strong>Explanation</strong>\: The first step is to mount a directory for the container's file system, which ideally would contain all the files and directories the application needs to run.</p>
}

// question: 2.2  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>What is the purpose of the chroot command in the manual container creation process?</p>{
	~[moodle]To execute the application inside the container.#<p>Executing the application is the final step after everything has been set up.</p>
	~[moodle]To create a new namespace for the user.#<p>User namespaces are created using the unshare command.</p>
	=[moodle]To set up a directory as a fake file system for the application.
	~[moodle]To limit the application from consuming too many system resources.#<p>Resource limiting is the function of control groups.</p>
	####<p><strong>Explanation</strong>\: The chroot command is used to set the created directory as a fake file system for the application, helping to isolate the application and prevent it from modifying real files on the host's file system.</p>
}

// question: 2.3  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>Where is most of Docker's data, including containers, container images, and metadata, stored by default on a Linux system?</p>{
	~[moodle]/etc/docker.#<p>/etc/docker contains the Docker daemon.json configuration file.</p>
	~[moodle]/var/run/docker.sock.#<p>/var/run/docker.sock is the location of the Unix socket that the Docker CLI uses to communicate with the Docker engine.</p>
	=[moodle]/var/lib/docker.
	~[moodle]/usr/local/bin/docker.#<p>This is a directory that typically contains executable binaries, not Docker's data.</p>
	####<p><strong>Explanation</strong>\: Most of Docker's data, including containers, container images, and metadata used by the Docker client and runtime, resides in the /var/lib/docker directory.</p>
}

// question: 2.4  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>By default, where are Docker container volumes stored on the system?</p>{
	~[moodle]Directly in the container's root directory.#<p>Data saved in the container's root directory will be lost when the container is deleted.</p>
	~[moodle]In the /var/lib/docker/volumes directory.#<p>Although related to volumes, the specific location mentioned in the source is /var/lib/docker/overlay. Volumes are mounted within Docker's overlay directory.</p>
	=[moodle]In the /var/lib/docker/overlay directory.
	~[moodle]In the /tmp directory of the host.#<p>The /tmp directory is a temporary directory and should not be used for persistent Docker data storage.</p>
	####<p><strong>Explanation</strong>\: Container volumes are stored in the /var/lib/docker/overlay directory.</p>
}

// question: 2.5  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>Where is the Docker daemon's configuration file (daemon.json) located by default on a Linux system?</p>{
	~[moodle]/usr/bin/docker.#<p>This is the location of the Docker client or daemon executable.</p>
	~[moodle]/var/run/docker.sock.#<p>This is the location of the Unix socket.</p>
	=[moodle]/etc/docker.
	~[moodle]/opt/docker.#<p>This is an optional directory often used for third-party software, not Docker's default configuration location.</p>
	####<p><strong>Explanation</strong>\: Docker expects to rely on /etc/docker/daemon.json for configuration and other properties like HTTP proxy and runtime configuration.</p>
}

// question: 2.6  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>How does the Overlay2 storage driver manage container image layers?</p>{
	~[moodle]It unpacks all layers into a single temporary directory for each container.#<p>Although it unpacks, it's not into a single directory per container, but each layer has its own directory and is combined using OverlayFS to avoid data duplication.</p>
	~[moodle]It compresses all layers into a large tar file before providing it to the container.#<p>Image layers are compressed as tar files, but the storage driver unpacks them into directories.</p>
	=[moodle]It unpacks each image layer into a separate directory and uses OverlayFS to combine them into a single virtual file system.
	~[moodle]It stores image layers as individual objects in a database.#<p>This storage method is not described for Overlay2; Overlay2 is based on a file system.</p>
	####<p><strong>Explanation</strong>\: Overlay2 unpacks each layer in a container image into the container runtime's configuration directory (usually /var/lib/docker/overlay2) and uses OverlayFS to combine them into a single directory for the container to use.</p>
}

// question: 2.7  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>When a Docker container creates new files that do not exist in the original image, or modifies/deletes an existing file in the read-only layers, what happens to these changes according to OverlayFS?</p>{
	~[moodle]Changes are written directly to the lowerdir.#<p>The lowerdir is read-only and cannot be written to.</p>
	=[moodle]Changes are written to a separate read/write layer called upperdir.
	~[moodle]The container is forced to create a complete copy of the image.#<p>Creating a complete copy would be inefficient; OverlayFS is designed to avoid that.</p>
	~[moodle]Changes are synchronized back to the Container Registry.#<p>Changes are not automatically synchronized to the Container Registry; they only exist in the container's upperdir.</p>
	####<p><strong>Explanation</strong>\: Any changes to the file system (creating new files, modifying, or deleting) are made to the upperdir (read/write layer) without affecting the read-only layers below.</p>
}

// question: 2.8  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>When does the "copy-up" phenomenon occur in OverlayFS?</p>{
	~[moodle]When a container creates a new file from scratch.#<p>Creating a new file simply involves writing to the upperdir.</p>
	~[moodle]When a file is deleted from the upperdir layer.#<p>Deleting a file from upperdir typically involves "whiteout".</p>
	=[moodle]When a container wants to modify or delete a file that exists in the lowerdir layer.
	~[moodle]When a container is started from a new image.#<p>The copy-up phenomenon is not directly related to starting a container, but rather to file system write behavior.</p>
	####<p><strong>Explanation</strong>\: "Copy-up" occurs when a container wants to modify or delete a file that exists in one of the lower layers but is not present in the upperdir. To do this, OverlayFS will copy the missing file from the lower directory to the upperdir so the container can interact with it.</p>
}

// question: 2.9  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>What is the main disadvantage of data being stored in a Docker container's OverlayFS?</p>{
	~[moodle]Data can only be accessed by a single container.#<p>Data in OverlayFS can be accessed by the container, but it's not a solution for persistent data storage.</p>
	~[moodle]Read/write performance is significantly degraded.#<p>While copy-ups can slow down I/O performance, the main disadvantage emphasized is data loss.</p>
	=[moodle]Data will be deleted after the container is removed.
	~[moodle]Data cannot be backed up or restored.#<p>There are ways to back up and restore data from containers via Volumes or bind mounts.</p>
	####<p><strong>Explanation</strong>\: A major disadvantage of the overlay file system is that any data persisted within it will be deleted when the container is removed.</p>
}

// question: 2.10  name: Chapter 2: Container Creation Process and Docker File Structure
::Chapter 2\: Container Creation Process and Docker File Structure::[html]<p>What are the two easiest ways to overcome the data loss disadvantage of OverlayFS when a container is removed?</p>{
	~[moodle]Using configuration management tools like Chef or Ansible.#<p>Configuration management tools do not solve the problem of persistent data loss from containers.</p>
	~[moodle]Using Dockerfile to create new image layers for each change.#<p>Creating new image layers for each change would increase image size and is not a way to persist data after a container is removed.</p>
	=[moodle]Using Volumes or Bind Mounts.
	~[moodle]Increasing the size of the upperdir to store more data.#<p>Increasing the upperdir size only increases temporary storage capacity, it does not solve the data loss problem when the container is removed.</p>
	####<p><strong>Explanation</strong>\: The easiest ways to overcome these limitations are to use Volumes or Bind Mounts. Volumes have better performance than bind mounts, but bind mounts are easier to use.</p>
}

// Chapter 3: Dockerfile Language and Image Building
// question: 3.1  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>What is the purpose of the FROM instruction in a Dockerfile?</p>{
	~[moodle]To execute shell commands inside the container image.#<p>Executing shell commands is the function of the RUN instruction.</p>
	~[moodle]To copy files and directories from the host to the image.#<p>Copying files is the function of the COPY or ADD instructions.</p>
	=[moodle]To specify the base image from which the new Docker image will be created.
	~[moodle]To define environment variables for the container.#<p>Defining environment variables is the function of the ENV instruction.</p>
	####<p><strong>Explanation</strong>\: The FROM instruction specifies the base image from which your new Docker image will be created. This is a mandatory instruction and must be the first line in your Dockerfile (excluding comments and ARG/ENV).</p>
}

// question: 3.2  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>What is the main difference between the COPY and ADD instructions in a Dockerfile, and what is the current recommended usage?</p>{
	~[moodle]COPY only copies files, while ADD can automatically extract tar files and download URLs. ADD is recommended.#<p>ADD is not recommended; COPY is preferred for its simplicity and security.</p>
	~[moodle]ADD only copies files, while COPY can automatically extract tar files and download URLs. COPY is recommended.#<p>This is incorrect; ADD has the additional functionality, not COPY.</p>
	~[moodle]COPY can automatically extract tar files and download URLs, while ADD only copies files. COPY is recommended.#<p>This is incorrect; ADD has the additional functionality, not COPY.</p>
	=[moodle]COPY only copies files, while ADD can automatically extract tar files and download URLs. COPY is recommended.
	####<p><strong>Explanation</strong>\: COPY only copies files and directories. ADD is an older version of COPY with two key differences: it can automatically extract tar files from a URL and it can automatically download files from a URL. Dockerfile maintainers recommend using COPY instead of ADD because COPY is a newer and more secure version of ADD.</p>
}

// question: 3.3  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>What happens if a RUN instruction in a Dockerfile is placed before a COPY instruction that it needs files to be copied into?</p>{
	~[moodle]Docker will automatically adjust the order of instructions to ensure the RUN instruction succeeds.#<p>Docker processes Dockerfiles from top to bottom and does not automatically reorder instructions.</p>
	~[moodle]The RUN instruction will execute successfully because it uses the base image.#<p>The RUN instruction uses the image from the previous Dockerfile instruction. If files have not been copied yet, it will fail.</p>
	=[moodle]The RUN instruction will fail and the Docker image build process will stop.
	~[moodle]Docker will skip the RUN instruction and continue with subsequent instructions.#<p>Docker will not skip a failed instruction; it will stop the build process.</p>
	####<p><strong>Explanation</strong>\: Instruction order is crucial when creating a Dockerfile. If a RUN instruction is placed before a COPY instruction it depends on, the RUN instruction will fail because the necessary directory/file is not yet in the base image used for that layer, and the Docker build process will stop.</p>
}

// question: 3.4  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>What is the purpose of the WORKDIR instruction in a Dockerfile?</p>{
	=[moodle]To define the default working directory for the container when it starts.
	~[moodle]To set permissions for non-root users.#<p>Setting user permissions is the function of the USER instruction or user management commands.</p>
	~[moodle]To install necessary software packages for the application.#<p>Installing software packages is the function of the RUN instruction.</p>
	~[moodle]To declare environment variables only available during the build process.#<p>Declaring build environment variables is the function of the ARG instruction.</p>
	####<p><strong>Explanation</strong>\: The WORKDIR instruction allows you to configure a working directory for RUN commands in your Dockerfile and/or containers created from your image. It is also the default working directory for the container upon initialization.</p>
}

// question: 3.5  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>When both ENTRYPOINT and CMD are defined in a Dockerfile (and both are in exec form), what happens when the container launches?</p>{
	~[moodle]The CMD instruction will be executed first, then ENTRYPOINT.#<p>This describes incorrect behavior of ENTRYPOINT and CMD when both are used.</p>
	=[moodle]The ENTRYPOINT instruction will be executed with arguments provided by CMD.
	~[moodle]Both instructions will run in parallel as independent processes.#<p>This describes incorrect behavior of ENTRYPOINT and CMD when both are used.</p>
	~[moodle]CMD will be completely ignored if ENTRYPOINT is defined.#<p>This describes incorrect behavior of ENTRYPOINT and CMD when both are used.</p>
	####<p><strong>Explanation</strong>\: When both ENTRYPOINT and CMD are defined (and in exec form), anything provided to CMD will be passed into ENTRYPOINT as arguments. ENTRYPOINT will run as the container's top-level process and receive those arguments.</p>
}

// question: 3.6  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>What is the main security benefit of using USER in a Dockerfile to run the container as a non-root user?</p>{
	~[moodle]Allows the container to directly access host hardware.#<p>USER does not provide direct access to hardware; that privilege is typically associated with the --privileged flag.</p>
	~[moodle]Improves application performance within the container.#<p>Changing the user typically does not directly affect application performance.</p>
	=[moodle]Significantly reduces security concerns.
	~[moodle]Enables default Docker debug logging.#<p>Enabling debug logging is done via Docker daemon configuration (e.g., daemon.json), not the USER instruction.</p>
	####<p><strong>Explanation</strong>\: Using USER to prevent containers from running as root by default significantly reduces security concerns that arise when running Docker in production environments. This makes security teams much happier.</p>
}

// question: 3.7  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>How do ARG (build arguments) variables in a Dockerfile differ from ENV (environment variables)?</p>{
	~[moodle]ARG is only available at runtime, while ENV is only available at build time.#<p>This order is reversed.</p>
	=[moodle]ARG is set at build time and is not passed down to containers, while ENV is set at runtime and is passed down to containers.
	~[moodle]Both ARG and ENV can be overridden with docker build, but ENV cannot be overridden with docker run.#<p>ARG is set using --build-arg with docker build, ENV cannot be overridden with docker build. ENV can be overridden with docker run.</p>
	~[moodle]ARG can only be used in RUN instructions, while ENV can be used in any Dockerfile instruction.#<p>Both ENV and ARG can only be used in RUN instructions within a Dockerfile.</p>
	####<p><strong>Explanation</strong>\: ARG is a variable set at build time and is not passed down to containers created from the image. In contrast, ENV is a variable defined for every container started from the image, and can be overridden with the --env or -e flags with docker run.</p>
}

// question: 3.8  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>What is the function of the EXPOSE instruction in a Dockerfile?</p>{
	~[moodle]Automatically opening a network port on the host and mapping it to the container.#<p>To automatically open and map a port, you need to use the --publish or -p flag with docker run. EXPOSE is just documentation.</p>
	=[moodle]Documenting the network ports that the container should expose at runtime.
	~[moodle]Allowing the container to communicate with external services via the specified port.#<p>EXPOSE does not directly enable communication; it's just port information.</p>
	~[moodle]Activating the Docker firewall to protect the container's network ports.#<p>EXPOSE does not activate a firewall; it's just a declaration.</p>
	####<p><strong>Explanation</strong>\: This useful EXPOSE instruction documents the network ports that containers created from your image should expose at runtime. It's important to know that EXPOSE does not automatically expose ports.</p>
}

// question: 3.9  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>When Docker rebuilds an image and the lines in the Dockerfile have not changed, what happens regarding image layers?</p>{
	~[moodle]Docker will skip the entire build process and use the existing image.#<p>Docker will still perform the check, but will use the cache.</p>
	~[moodle]Docker will be forced to rebuild all layers from scratch to ensure consistency.#<p>Forcing a rebuild from scratch would be time-consuming and negate the benefits of caching.</p>
	=[moodle]Docker will use cached layers from previous builds.
	~[moodle]Docker will re-download all layers from the Container Registry for updates.#<p>Docker will not re-download from the registry if layers are already in cache and there are no changes in the Dockerfile.</p>
	####<p><strong>Explanation</strong>\: The reason is that layers from previous docker build runs are cached, and since no lines in the Dockerfile changed, Docker simply fetches those layers and reuses them instead of having to completely rebuild from scratch.</p>
}

// question: 3.10  name: Chapter 3: Dockerfile Language and Image Building
::Chapter 3\: Dockerfile Language and Image Building::[html]<p>During the Docker image build process, if you want to provide a default value for a variable but also allow users to change it when running docker build, which instruction should you use?</p>{
	~[moodle]CMD.#<p>CMD provides default arguments to ENTRYPOINT or the container startup command, but operates at runtime, not build time.</p>
	~[moodle]ENTRYPOINT.#<p>ENTRYPOINT configures the main command the container will run when it starts.</p>
	=[moodle]ARG.
	~[moodle]ENV.#<p>ENV defines environment variables for the container at runtime, and cannot be overridden with docker build.</p>
	####<p><strong>Explanation</strong>\: The ARG instruction (build arguments) allows you to define variables that you provide to docker build. You can set default values and users can override them with the --build-arg flag when running docker build.</p>
}

// Chapter 4: Optimization and Cross-platform Building
// question: 4.1  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>What is the main benefit of using multi-stage builds in a Dockerfile?</p>{
	~[moodle]Only allows using a single base image in the Dockerfile.#<p>Multi-stage builds allow the use of multiple FROM instructions (multiple base images).</p>
	=[moodle]Creates smaller and more secure final container images.
	~[moodle]Increases container image size by adding all development tools to it.#<p>On the contrary, the main goal is to reduce image size by eliminating unnecessary tools and libraries.</p>
	~[moodle]Limits the ability to run applications on different processor architectures.#<p>Multi-stage builds are not directly related to cross-platform compatibility, but rather to image size and security optimization.</p>
	####<p><strong>Explanation</strong>\: Multi-stage builds allow you to create smaller and more secure final container images by only copying what your application needs to run.</p>
}

// question: 4.2  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>How do you copy files or directories between different stages in a multi-stage Dockerfile build?</p>{
	~[moodle]Use the ADD command with a URL to the previous stage.#<p>The ADD command is not used for copying between stages but for copying from a URL or extracting tar files.</p>
	~[moodle]Use a regular COPY command without any special flags.#<p>A regular COPY command will look for files in the build context, not in other stages.</p>
	=[moodle]Use the COPY command with the --from flag to specify the source stage.
	~[moodle]Create a temporary volume and copy files into it.#<p>This is an older "builder pattern" approach that multi-stage builds were created to replace, which is more complex and leaves temporary resources.</p>
	####<p><strong>Explanation</strong>\: In a multi-stage build, you can copy files or directories between stages by using the COPY command with the --from flag to specify the stage containing your files (by index or alias).</p>
}

// question: 4.3  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>Which of the following is a significant security benefit of using multi-stage builds?</p>{
	~[moodle]Ensuring all applications running in containers are continuously monitored.#<p>Multi-stage builds do not provide continuous monitoring.</p>
	~[moodle]Eliminating all security vulnerabilities from the base image.#<p>It does not eliminate all vulnerabilities, but significantly reduces risk by minimizing the attack surface.</p>
	=[moodle]Reducing the number of unnecessary image layers and operating system tools/libraries, thereby reducing the opportunity for vulnerabilities to appear.
	~[moodle]Automatically encrypting all data stored in container images.#<p>Multi-stage builds do not automatically encrypt data in images.</p>
	####<p><strong>Explanation</strong>\: The biggest reason to use multi-stage builds is to enhance security. By eliminating unnecessary image layers and operating system tools/libraries, we can create extremely secure images with fewer opportunities for vulnerabilities to appear.</p>
}

// question: 4.4  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>By default, how are Docker container images limited in terms of processor architecture?</p>{
	~[moodle]They can run on any architecture as long as there is enough memory.#<p>Not just related to memory, but also to ISA.</p>
	~[moodle]They can only run on the Linux kernel, regardless of architecture.#<p>Although Linux containers only run on the Linux kernel, there are still processor architecture limitations.</p>
	=[moodle]They are specific to the processor instruction set on which they are built.
	~[moodle]They require a hypervisor to translate between architectures.#<p>Docker uses other mechanisms like binfmt and QEMU for emulation, not conventional hypervisors.</p>
	####<p><strong>Explanation</strong>\: By default, container images are also specific to the processor instruction set on which they are built.</p>
}

// question: 4.5  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>What is the purpose of an "image index" or "manifest list" in Docker related to multi-platform images?</p>{
	~[moodle]Listing all layers of an image for debugging purposes.#<p>A manifest list is not for listing layers for debugging.</p>
	=[moodle]Mapping image manifests to specific processor types and operating systems.
	~[moodle]Storing environment variables used during the image build process.#<p>Environment variables are not stored in a manifest list.</p>
	~[moodle]Providing a summary of the history of a Docker image.#<p>Image history is viewed using the docker image history command, not a manifest list.</p>
	####<p><strong>Explanation</strong>\: An "image index" or "manifest list" allows you to map image manifests to specific processor types and even operating systems. This allows you to specify Docker to use a specific image for X86 systems and another for ARM systems.</p>
}

// question: 4.6  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>To build container images for processor architectures you don't have available (e.g., building an ARM image on an X86 machine), which tool does Docker use in conjunction with Linux's binfmt?</p>{
	~[moodle]VirtualBox.#<p>This is a hypervisor, not a tool used by Docker to emulate CPU architecture during container image builds.</p>
	~[moodle]VMware.#<p>This is a hypervisor, not a tool used by Docker to emulate CPU architecture during container image builds.</p>
	=[moodle]QEMU.
	~[moodle]Hyper-V.#<p>This is a hypervisor, not a tool used by Docker to emulate CPU architecture during container image builds.</p>
	####<p><strong>Explanation</strong>\: Docker has a clever way to address this by using an emulator called QEMU along with Linux's binfmt program. qemu-user-static allows Docker to emulate various processor types during the image build process.</p>
}

// question: 4.7  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>What is the effect of the --privileged flag when running docker run?</p>{
	~[moodle]Enables detailed debugging mode for the container.#<p>This flag does not enable debugging mode; that is done via Docker daemon configuration.</p>
	=[moodle]Grants the container full access to the host's devices and files.
	~[moodle]Limits the container to use a single CPU.#<p>CPU limiting is done using the --cpus flag.</p>
	~[moodle]Forces the container to run as a non-root user.#<p>Forcing the container to run as a non-root user is done using the --user flag.</p>
	####<p><strong>Explanation</strong>\: The --privileged flag tells Docker to configure the container so it can use the host's devices and files. This is generally very dangerous and should be used with caution.</p>
}

// question: 4.8  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>What is the main disadvantage of building cross-platform Docker images by emulating CPU architecture (e.g., ARM on an X86 machine)?</p>{
	~[moodle]The resulting image will be significantly larger in size.#<p>Image size is not directly affected by the emulation process, but by the content of the Dockerfile.</p>
	=[moodle]The image build process will be significantly slower due to code translation.
	~[moodle]The image can only be pushed to public registries.#<p>Cross-platform images can be pushed to both public and private registries, provided the registry supports manifest lists.</p>
	~[moodle]The created container will not be able to access the network.#<p>Network access is not affected by CPU architecture emulation.</p>
	####<p><strong>Explanation</strong>\: One of the drawbacks of this is that code translation will be slower than native code. Therefore, cross-platform image builds can take significantly longer on non-native platforms.</p>
}

// question: 4.9  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>What is the purpose of FROM scratch in a multi-stage build?</p>{
	~[moodle]To create a base image containing all development tools.#<p>Conversely, it creates an empty image.</p>
	=[moodle]To create a minimal Docker image containing only the final application, without a basic operating system.
	~[moodle]To use the oldest version of a base image.#<p>scratch is not related to the oldest version.</p>
	~[moodle]To ensure that the image is built on an X86 architecture.#<p>scratch is not related to the X86 architecture.</p>
	####<p><strong>Explanation</strong>\: FROM scratch is used to create your own base image. In multi-stage builds, it's particularly useful to create a final stage where you copy the final application artifact into a scratch image, making the image almost no larger than your application and completely self-contained.</p>
}

// question: 4.10  name: Chapter 4: Optimization and Cross-platform Building
::Chapter 4\: Optimization and Cross-platform Building::[html]<p>When creating multi-platform images, why is the image digest of each image in the manifest list important, and when is it generated?</p>{
	~[moodle]The image digest is used to identify the architecture of the image and is generated during the docker build process.#<p>The digest does not directly identify the architecture; it is a unique identifier of the image's content at that architecture. It is generated when pushing to the registry, not when building.</p>
	~[moodle]The image digest is a unique identifier of the image and is generated when the image is pulled from the registry.#<p>The digest is an identifier, but it is generated when pushed to the registry, not when pulled.</p>
	=[moodle]The image digest is a hash of the image's content and is generated by the registry when the image is pushed to it.
	~[moodle]The image digest is used to track changes between layers and is generated by the Dockerfile.#<p>The digest does not track changes between layers in that sense; it is a hash of the entire image.</p>
	####<p><strong>Explanation</strong>\: An image digest (the long string starting with sha256:) is a hash of the image's content. It is generated by the registry when we push the image to it. The docker manifest create command needs to query the registry to get the digest of the images it wants to include in the manifest list.</p>
}

// Chapter 5: Container Data Management
// question: 5.1  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>What is the main problem with Docker's default container file system when dealing with persistent data?</p>{
	~[moodle]Files can only be read, not written to.#<p>The file system has a read/write layer (upperdir) that allows writing.</p>
	=[moodle]Data is deleted when the container is removed.
	~[moodle]The file system size is strictly limited.#<p>Although there are limitations, the main issue is data persistence.</p>
	~[moodle]Data cannot be shared between different containers.#<p>Data can be shared between containers via networking or shared mounted volumes, but that's not the main limitation of the default file system.</p>
	####<p><strong>Explanation</strong>\: The file system presented to containers is an overlay file system, and when the container disappears, that file system also disappears along with all its data.</p>
}

// question: 5.2  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>What problem do Docker Volumes solve?</p>{
	~[moodle]Ensuring the application runs with root privileges.#<p>Volumes are not related to root privileges; that is a separate issue solved by the USER instruction or --user flag.</p>
	=[moodle]Providing a safe way to handle data into and out of containers and store persistent data.
	~[moodle]Speeding up the Docker image build process.#<p>Volumes do not speed up the image build process; that is the function of caching and multi-stage builds.</p>
	~[moodle]Reducing the Docker image size on disk.#<p>Volumes store data outside the image, not directly reducing image size.</p>
	####<p><strong>Explanation</strong>\: Volumes allow you to safely handle data going into and out of containers, and more importantly, they allow you to persist data from containers so you have less to worry about containers restarting or becoming unavailable during the application's lifecycle.</p>
}

// question: 5.3  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>By default, which volume driver does Docker use?</p>{
	~[moodle]json-file.#<p>json-file is the default logging driver.</p>
	~[moodle]bridge.#<p>bridge is the default network driver.</p>
	=[moodle]local.
	~[moodle]overlay2.#<p>overlay2 is the default storage driver for image layers.</p>
	####<p><strong>Explanation</strong>\: By default, Docker uses the local volume driver. The local driver simply creates a directory within Docker's system directory and mounts it into the container as a kind of virtual disk.</p>
}

// question: 5.4  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>The shorthand way (-v) to mount a volume into a container requires which arguments, separated by a colon?</p>{
	~[moodle]Volume name:destination directory in container.#<p>This lacks the options field, which is part of the shorthand syntax.</p>
	~[moodle]Source directory on host:volume name.#<p>This has incorrect order/syntax.</p>
	=[moodle]Volume name:destination directory in container:options (ro/volume-opt).
	~[moodle]Source directory on host:destination directory in container.#<p>This is the syntax for bind mounts, not volumes, and lacks the options field.</p>
	####<p><strong>Explanation</strong>\: The -v option (shorthand) accepts three colon-separated arguments: volume name (or source), the directory where the volume will be mounted inside the container (destination), and options such as ro (read-only) or volume-opt.</p>
}

// question: 5.5  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>What is the main purpose of Bind Mounts in Docker?</p>{
	~[moodle]Creating copies of data from the container to the host.#<p>While it can be used for backup, the primary purpose of a bind mount is direct mapping.</p>
	=[moodle]Mapping directories on the host directly into directories within the container.
	~[moodle]Persisting application data after the container is removed.#<p>Volumes are primarily designed for persisting data.</p>
	~[moodle]Downloading tar files and extracting them into the container.#<p>This functionality belongs to the ADD instruction in a Dockerfile.</p>
	####<p><strong>Explanation</strong>\: Bind mounts map directories on your computer directly into directories within your containers. This allows you to work with source code or data directly from the host without needing to copy it into an image or volume.</p>
}

// question: 5.6  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>What is one of the advantages of Bind Mounts over copying source code into a volume for application testing?</p>{
	~[moodle]Bind mounts automatically compress data to save space.#<p>Bind mounts do not compress data.</p>
	=[moodle]No need to manage volumes and no temporary containers are left behind.
	~[moodle]Ensures that the application always runs with root privileges.#<p>Bind mounts are not related to running applications with root privileges.</p>
	~[moodle]Significantly improves I/O performance on non-Linux systems.#<p>On the contrary, bind mounts can cause performance degradation on non-Linux systems due to the directory sharing mechanism.</p>
	####<p><strong>Explanation</strong>\: With bind mounts, you simply map your source code directory into a directory within the container and run tests. No volume management is needed and no temporary containers need to be cleaned up after completion.</p>
}

// question: 5.7  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>When using the shorthand way (-v) to mount a Bind Mount, what happens if the source directory on the host does not exist?</p>{
	~[moodle]Docker will report an error and stop the container run process.#<p>Docker will not report an error but will automatically create the directory.</p>
	=[moodle]Docker will automatically create an empty directory on the host at that location.
	~[moodle]Docker will use a hidden volume instead of a bind mount.#<p>It will still be a bind mount, not a hidden volume.</p>
	~[moodle]The container will run without the directory mounted.#<p>The directory will be created and mounted.</p>
	####<p><strong>Explanation</strong>\: If you try to mount a non-existent source directory using the shorthand (-v), Docker will automatically create a directory for you on your computer. This often causes confusion when users intend to mount a specific file.</p>
}

// question: 5.8  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>When running Docker on non-Linux operating systems (e.g., macOS, Windows), what problem can Bind Mounts encounter?</p>{
	~[moodle]Inability to access files larger than 1GB.#<p>There is no specific file size limitation as such.</p>
	=[moodle]Read/write performance can be significantly slow.
	~[moodle]Data will not be persisted after the container is stopped.#<p>Bind mounts do persist data on the host; the issue is performance.</p>
	~[moodle]Only system directories can be mounted, not user directories.#<p>Both system and user directories can be mounted.</p>
	####<p><strong>Explanation</strong>\: When running Docker outside of Linux (such as on macOS or Windows), Bind Mounts can experience performance issues. Working directories are often shared with a virtual machine, and every read/write operation to a bind mount needs to go through a driver, causing significant slowdown when working with large files or many small files.</p>
}

// question: 5.9  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>To back up data from a Docker Volume to the host, which command combination with docker run should you use?</p>{
	~[moodle]Use docker cp to copy directly from the volume directory on the host.#<p>It's not recommended to rely on copying directly from the volume directory on the host because the location and storage mechanism can vary depending on the driver.</p>
	~[moodle]Mount that volume into a container, then use docker cp to copy from the container to a bind-mounted directory.#<p>docker cp can be used, but the tar method inside the container is described as "one step" and more efficient.</p>
	=[moodle]Mount the volume and a target directory on the host (via bind mount) into the same container, then use tar to compress data from the volume into the target directory.
	~[moodle]Simply copy the entire /var/lib/docker/volumes directory from the host.#<p>Copying the entire /var/lib/docker/volumes directory may not be efficient and suitable for all types of volume drivers.</p>
	####<p><strong>Explanation</strong>\: The recommended way to back up and restore volumes is to run a temporary container, mount the volume to be backed up and a target directory on the host (via bind mount) into that container, then use a tool like tar to compress the data from the volume into the target directory.</p>
}

// question: 5.10  name: Chapter 5: Container Data Management
::Chapter 5\: Container Data Management::[html]<p>When restoring data to a new Docker Volume from a backup file (e.g., .tar), how do you ensure the data is extracted into the correct directory within the volume?</p>{
	~[moodle]Extract the backup file directly into the /var/lib/docker/volumes directory on the host.#<p>Extracting directly into the system directory may not be reliable or suitable for every driver.</p>
	=[moodle]Mount the new volume and the backup file (via bind mount) into a container, then use tar with the -C flag to extract into the mounted directory of the volume.
	~[moodle]Rename the backup file to the name of the new volume.#<p>Renaming the backup file does not affect the extraction location inside the volume.</p>
	~[moodle]Use the docker load command to load the backup file into the volume.#<p>docker load is used to load Docker images, not volume data.</p>
	####<p><strong>Explanation</strong>\: To restore, you would run a container, mount the new volume (destination) and the backup file (via bind mount) into that container. Then, use tar with the -C /restore flag (change directory into the mounted volume directory) and a dot (.) to ensure files are extracted into the correct root directory of the volume.</p>
}

// Chapter 6: Container Networking
// question: 6.1  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>What is the default network driver used by Docker containers?</p>{
	~[moodle]host.#<p>host is another driver but not the default.</p>
	~[moodle]none.#<p>none is another driver used to disable networking.</p>
	~[moodle]macvlan.#<p>macvlan is an advanced network driver, not the default.</p>
	=[moodle]bridge.
	####<p><strong>Explanation</strong>\: The bridge network driver is the default network driver used by Docker containers. Docker also automatically creates a default bridge network named Bridge.</p>
}

// question: 6.2  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>When containers are connected to Docker's default bridge network, how can they communicate with each other?</p>{
	~[moodle]They can communicate directly by service name without needing IP addresses.#<p>The ability to communicate by service name is usually easier with custom bridge networks.</p>
	=[moodle]They must know each other's IP addresses to communicate.
	~[moodle]They use a single port published from the host.#<p>Publishing ports is for external access to the container, not between containers on the same network.</p>
	~[moodle]They communicate through an external DNS server.#<p>Docker's embedded DNS server works internally, not as an external DNS server.</p>
	####<p><strong>Explanation</strong>\: While containers connected to the default bridge network can talk to each other, they must know each other's IP addresses. Although Docker Engine has an embedded DNS server, it does not easily provide service name resolution on the default bridge network like custom bridge networks do.</p>
}

// question: 6.3  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>What is the purpose of the --publish (or -p) flag when running docker run?</p>{
	~[moodle]Automatically adding the container to a network security group.#<p>--publish does not add to a security group; it configures port mapping.</p>
	~[moodle]Documenting the ports used by the application inside the container.#<p>Documenting ports is the function of the EXPOSE instruction in a Dockerfile.</p>
	=[moodle]Mapping a port from inside the container to a port on the host.
	~[moodle]Forcing the container to use a static IP address.#<p>publish is not related to static IPs.</p>
	####<p><strong>Explanation</strong>\: The --publish flag allows you to map a port from inside your container to a port on your host. This enables access to the service running inside the container from outside.</p>
}

// question: 6.4  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>When using the --publish flag with the syntax HOST_PORT:CONTAINER_PORT, what does HOST_PORT (the left port) signify?</p>{
	~[moodle]The port inside the container that will be exposed.#<p>The port inside the container is CONTAINER_PORT (the right port).</p>
	=[moodle]The port on the host that will be used to access the container.
	~[moodle]The version number of the network protocol.#<p>This is not related to the publish syntax.</p>
	~[moodle]The default port automatically assigned by Docker.#<p>This is not related to the publish syntax.</p>
	####<p><strong>Explanation</strong>\: HOST_PORT (the left port) is the port on your host machine to access the container from outside.</p>
}

// question: 6.5  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>What characteristic does the host network driver (--net=host) allow for a container?</p>{
	~[moodle]The container has a completely separate network from the host.#<p>This describes the bridge driver or virtualized networking.</p>
	=[moodle]The container shares the same network stack as the host.
	~[moodle]The container is assigned a virtual IP address and a virtual NIC.#<p>This describes how bridge works.</p>
	~[moodle]The container is completely disabled from network access.#<p>This describes the none driver.</p>
	####<p><strong>Explanation</strong>\: The host driver allows containers to share the same network stack as its host (Host Mode Networking).</p>
}

// question: 6.6  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>What is the main benefit of using host network mode compared to bridge network mode?</p>{
	~[moodle]Provides stronger network isolation between the container and the host.#<p>Conversely, host mode reduces network isolation.</p>
	=[moodle]No need to worry about publishing ports because the container directly accesses the host's ports.
	~[moodle]Ensures that each container has a separate and unique IP address on the physical network.#<p>Host mode does not ensure separate IPs on the physical network; containers use the host's IP.</p>
	~[moodle]Automatically encrypts all network traffic between the container and the host.#<p>Host mode does not provide network traffic encryption.</p>
	####<p><strong>Explanation</strong>\: A much larger advantage of using host network mode is no need to worry about publishing ports. Since containers use the host's network stack, they also have access to the host's ports.</p>
}

// question: 6.7  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>What is the function of the none network driver?</p>{
	~[moodle]Allows containers to communicate with other containers on the same network.#<p>This function belongs to the bridge driver.</p>
	=[moodle]Creates containers without any external network connectivity.
	~[moodle]Assigns a single static IP address to each container.#<p>none does not assign static IPs; it disables external networking.</p>
	~[moodle]Automatically configures DNS for containers.#<p>none does not automatically configure DNS.</p>
	####<p><strong>Explanation</strong>\: The none network driver is used to create containers without any external network connectivity. These containers will not be able to communicate with other containers on any network or with the outside world.</p>
}

// question: 6.8  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>What is the main difference between macvlan and ipvlan network drivers?</p>{
	~[moodle]macvlan only works on Linux, while ipvlan works on all operating systems.#<p>Both are drivers for Linux.</p>
	=[moodle]macvlan assigns each container its own random MAC address, while ipvlan assigns the same MAC address to every container and uses the host's network driver to handle traffic.
	~[moodle]ipvlan requires manual configuration for each IP address, while macvlan automatically assigns IPs.#<p>Both drivers automatically handle IP address management.</p>
	~[moodle]macvlan is used for internal networks, while ipvlan is for public networks.#<p>Both can be used for various networking purposes, not limited by "internal" or "public".</p>
	####<p><strong>Explanation</strong>\: The biggest difference between them is how they handle MAC addresses. macvlan gives each Docker container its own random MAC address, while ipvlan solves this by giving every container the same MAC address and using the host's network driver to handle traffic.</p>
}

// question: 6.9  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>What is the purpose of the overlay network driver in Docker?</p>{
	~[moodle]Creating a separate network for each application within a container.#<p>An overlay network does not create a separate network for each application within a container.</p>
	~[moodle]Allowing containers to communicate directly with each other without any configuration.#<p>While they enable communication, it's not without configuration; they require more complex setup.</p>
	=[moodle]Creating a virtual network across two or more nodes running Docker Engine or a Swarm.
	~[moodle]Supporting the mapping of network ports between containers and the host.#<p>Port mapping is done via publishing ports or host mode.</p>
	####<p><strong>Explanation</strong>\: The overlay driver allows you to create a virtual network across two or more nodes running Docker Engine, or a Swarm. The goal of an overlay network is to make containers running on multiple machines, and potentially across multiple networks, appear as if they are on a single network.</p>
}

// question: 6.10  name: Chapter 6: Container Networking
::Chapter 6\: Container Networking::[html]<p>What are the main components that overlay networks typically use to operate?</p>{
	~[moodle]Physical routers, hardware firewalls, and DNS servers.#<p>These are general networking components, not core components of overlay networks.</p>
	~[moodle]Virtual network switches, load balancer controllers, and discovery services.#<p>These are not core components of overlay networks.</p>
	=[moodle]A network tunnel, virtual network interfaces, and agents running on the host.
	~[moodle]Proxy servers, caches, and logging drivers.#<p>These are not core components of overlay networks.</p>
	####<p><strong>Explanation</strong>\: Most overlay networks use three things: a network tunnel, virtual network interfaces, and agents running on the host. The agents are responsible for sending network packets from the container across the virtual network interfaces and through the tunnel.</p>
}

// Chapter 7: Container Registry
// question: 7.1  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>What main problem does a Container Image Registry solve?</p>{
	~[moodle]Automatically checking the source code quality of applications.#<p>A registry does not automatically check source code quality.</p>
	=[moodle]Providing an easy way to share and manage container images.
	~[moodle]Reducing the disk space needed to store containers.#<p>A registry stores images, it does not directly reduce the disk space needed for running containers.</p>
	~[moodle]Enforcing security policies for running applications.#<p>A registry does not enforce security policies for running applications, but manages access to images.</p>
	####<p><strong>Explanation</strong>\: An Image Registry is a web server that serves container images, making it much easier to share and manage container images compared to manually using docker save and docker load.</p>
}

// question: 7.2  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>By default, which image registry does the Docker client use?</p>{
	~[moodle]GitHub Container Registry.#<p>These are other types of registries you can use, but not the default.</p>
	~[moodle]AWS Elastic Container Registry.#<p>These are other types of registries you can use, but not the default.</p>
	=[moodle]Docker Hub.
	~[moodle]A self-created local registry.#<p>These are other types of registries you can use, but not the default.</p>
	####<p><strong>Explanation</strong>\: By default, the Docker client uses Docker Hub, the most popular registry in the world.</p>
}

// question: 7.3  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>Why do teams and organizations often choose to use a registry other than Docker Hub?</p>{
	~[moodle]To gain access to exclusive Docker features.#<p>Exclusive features are not the primary reason; other registries offer better image management.</p>
	=[moodle]To avoid Docker Hub's pull rate limits and enhance security/privacy.
	~[moodle]To only store images on physical servers.#<p>Different registries can store images in various locations, not just physical servers.</p>
	~[moodle]To be able to use any programming language to create images.#<p>A registry does not limit the programming languages used to create images.</p>
	####<p><strong>Explanation</strong>\: There are three main reasons: enhanced security and privacy, overcoming Docker Hub's pull rate limits, and environment compatibility (e.g., running offline or in an internal network).</p>
}

// question: 7.4  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>To push an image to a local registry (e.g., localhost:5000/my-image:latest), what step do you need to perform before using docker push?</p>{
	~[moodle]Run docker login to authenticate with the registry.#<p>docker login is necessary for registries requiring authentication, but not for an insecure local registry.</p>
	~[moodle]Change the current working directory to the directory containing the image.#<p>No need to change the working directory to push an image.</p>
	=[moodle]Tag the image with the registry's name and port.
	~[moodle]Delete all existing images from the local machine.#<p>Deleting images is not a necessary step to push an image to a registry.</p>
	####<p><strong>Explanation</strong>\: Before pushing an image, you need to tag the image so Docker knows that the image will reside in a specific registry, including the registry's DNS name and port (e.g., localhost:5000/my-image:latest).</p>
}

// question: 7.5  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>Why must a manifest list for multi-platform images exist in a Container Registry to function?</p>{
	~[moodle]A manifest list is a configuration file only generated by the Container Registry.#<p>A manifest list is not a configuration file exclusively generated by the registry.</p>
	=[moodle]Due to technical limitations, images in the manifest list must exist in the registry for Docker to query their digests.
	~[moodle]A manifest list is used to store registry authentication information.#<p>A manifest list does not store authentication information.</p>
	~[moodle]The registry needs to compress manifest lists to optimize network performance.#<p>The registry does not compress manifest lists; it is a list of references to digests.</p>
	####<p><strong>Explanation</strong>\: Due to the technical limitations of how manifest lists work, the images in this list must exist in a Container Registry (like Docker Hub). The docker manifest create command will query the registry to get the digest of the images added to the list.</p>
}

// question: 7.6  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>To secure a local Docker registry, what is the recommended approach?</p>{
	~[moodle]Only use docker push from within an isolated container.#<p>Pushing only from an isolated container does not solve the problem of unauthorized access to the registry.</p>
	=[moodle]Place a reverse proxy (e.g., Nginx) in front of the registry and configure HTTPS/basic authentication.
	~[moodle]Delete the registry after each use to prevent unauthorized access.#<p>Deleting the registry after each use is impractical for continuous use cases.</p>
	~[moodle]Use a none network driver to disable all external connections.#<p>Disabling all external connections would make the registry inaccessible for pulling/pushing images.</p>
	####<p><strong>Explanation</strong>\: To secure a local Docker registry, the recommended approach is to place a reverse proxy (e.g., Nginx) in front of the registry. This allows configuring security such as self-signed HTTPS certificates and basic authentication (HTPasswd).</p>
}

// question: 7.7  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>When configuring self-signed certificates for a local registry secured by a reverse proxy, where do you need to add the CA certificate (e.g., cert.pem) on the VM/host running Docker?</p>{
	~[moodle]The /var/lib/docker/volumes directory.#<p>This is where volumes are stored, not related to certificates.</p>
	~[moodle]The /usr/local/bin directory.#<p>This is where executable binaries are located, not CA certificates.</p>
	=[moodle]The /usr/local/share/ca-certificates directory and then update the root certificates.
	~[moodle]The /etc/docker/daemon.json file.#<p>daemon.json is the Docker daemon's configuration file, not where CA certificates are stored.</p>
	####<p><strong>Explanation</strong>\: To avoid insecure certificate errors, you need to add cert.pem to the virtual machine's list of root certificate authorities (usually /usr/local/share/ca-certificates with a .crt file extension) and then run a script to update the root certificates (e.g., update-ca-certificates).</p>
}

// question: 7.8  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>Which type of registry is provided by source-code hosting platforms like GitHub and GitLab?</p>{
	~[moodle]Enterprise registries.#<p>Enterprise registries are commercial solutions for deployment within an organization's internal network or cloud.</p>
	~[moodle]Cloud provider registries.#<p>Cloud provider registries are provided by cloud service providers like AWS, Azure.</p>
	=[moodle]Source-code hosting registries.
	~[moodle]Local registries.#<p>Local registries are self-installed registries on a local machine.</p>
	####<p><strong>Explanation</strong>\: Source-code hosting registries are registries provided by source-code hosting platforms, such as GitHub and GitLab. Their main purpose is to facilitate the publication of container images for projects hosted on these platforms.</p>
}

// question: 7.9  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>Which characteristic is NOT an advantage of Cloud Provider Registries (e.g., AWS ECR) compared to other registry types?</p>{
	~[moodle]Good integration with other cloud services from the provider.
	~[moodle]Often offers free tiers.
	~[moodle]Easy to manage through the provider's user interface (UI).
	=[moodle]Always completely free after the free tier expires.
	####<p><strong>Explanation</strong>\: Most of these providers have free tiers, but are generally not free after the free tier expires, so you need to monitor monthly spending to avoid unexpected bills.</p>
}

// question: 7.10  name: Chapter 7: Container Registry
::Chapter 7\: Container Registry::[html]<p>Which type of registry is typically used by large companies when they need a registry operating within their internal network and environment, complying with industry standards and regulations?</p>{
	~[moodle]Docker Hub.#<p>Docker Hub is the default public registry, not suitable for sensitive data or internal networks.</p>
	~[moodle]Source-code hosting registries.#<p>Source-code hosting registries focus on integration with source-code hosting platforms, not necessarily for large enterprise internal environments.</p>
	=[moodle]Enterprise registries.
	~[moodle]Insecure local registries.#<p>Insecure local registries are not suitable for enterprise environments and sensitive data.</p>
	####<p><strong>Explanation</strong>\: Enterprise registries are an excellent choice for companies that need a registry operating within their internal network and environment. They are built to comply with many industry standards and regulations, making them easily approved by security and compliance departments.</p>
}

// Chapter 8: Advanced Concepts and Docker Management
// question: 8.1  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>To enable debug logging for the Docker daemon, which configuration file and value do you need to change?</p>{
	~[moodle]/var/run/docker.sock file to log_level: debug.#<p>/var/run/docker.sock is a Unix socket, not a configuration file.</p>
	~[moodle]/var/lib/docker/overlay2/logs.json file to debug: true.#<p>There is no such log file to configure debug mode.</p>
	=[moodle]/etc/docker/daemon.json file by adding the debug: true property.
	~[moodle]The base image's Dockerfile and add RUN debug_mode=true instruction.#<p>Docker daemon configuration is at the system level, not within an image's Dockerfile.</p>
	####<p><strong>Explanation</strong>\: To enable debug logging, you need to modify the /etc/docker/daemon.json file by adding the property "debug": true to the JSON object. Afterwards, the Docker daemon needs to be restarted.</p>
}

// question: 8.2  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>Which main program powers the Docker Engine on the system?</p>{
	~[moodle]containerd.#<p>containerd is a container runtime that Docker Engine uses by default, but it's not the main program of the Engine.</p>
	~[moodle]runc.#<p>runc is another popular container runtime, often used by containerd.</p>
	=[moodle]dockerd.
	~[moodle]docker-cli.#<p>docker-cli is the command-line tool to interact with the Docker Engine, not the main program of the Engine.</p>
	####<p><strong>Explanation</strong>\: The Docker Engine is powered by a program called dockerd.</p>
}

// question: 8.3  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>What is the --cpus flag in docker run used for?</p>{
	~[moodle]Specifying the number of CPU cores the container must use.#<p>Incorrect description; it does not directly assign cores or physical CPUs.</p>
	=[moodle]Setting the maximum percentage of processor time a container can consume.
	~[moodle]Enabling multi-threading for the application in the container.#<p>--cpus does not enable multi-threading; that's how the application is written.</p>
	~[moodle]Assigning a specific physical CPU to the container.#<p>Incorrect description; it does not directly assign cores or physical CPUs.</p>
	####<p><strong>Explanation</strong>\: The --cpus flag allows you to define the maximum amount of processor time a container can have, expressed as a decimal number. It does not mean using that many CPU cores, but a percentage of the total CPU time.</p>
}

// question: 8.4  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>What is the main purpose of Linux Capabilities in the context of Docker?</p>{
	~[moodle]To control how image layers are stored on disk.#<p>How image layers are stored is managed by storage drivers.</p>
	=[moodle]To restrict the set of system calls that processes inside the container can perform.
	~[moodle]To map the container's network ports to the host.#<p>Port mapping is done using the --publish flag.</p>
	~[moodle]To monitor the container's CPU and memory usage.#<p>Monitoring CPU/memory is a function of control groups and monitoring tools.</p>
	####<p><strong>Explanation</strong>\: Linux Capabilities are groups of privileges that can be granted to an application, allowing administrators to restrict the set of system calls that processes inside a namespace can make.</p>
}

// question: 8.5  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>What is the effect of the --privileged flag in docker run on a container?</p>{
	~[moodle]It automatically installs all necessary software packages into the container.#<p>--privileged does not install software.</p>
	=[moodle]It makes the container behave like a real process on the system, with access to everything including host devices.
	~[moodle]It limits the container to run only a single application to enhance security.#<p>--privileged allows deeper access, not to limit applications. Furthermore, containers are inherently designed to run a single application.</p>
	~[moodle]It disables all CPU and memory resource limits for the container.#<p>--privileged does not disable resource limits; it bypasses security measures related to device/file access permissions.</p>
	####<p><strong>Explanation</strong>\: The --privileged flag essentially tells Docker: "treat this container like a real process on your system." It can do anything and access everything, including devices on your system like hard drives. This is extremely dangerous.</p>
}

// question: 8.6  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>What is the recommended method for running "Docker in Docker" (running Docker commands inside a Docker container)?</p>{
	~[moodle]Installing the entire Docker Engine inside the container.#<p>Installing the entire Docker Engine inside the container has many issues and is not recommended.</p>
	=[moodle]Bind mounting the Docker Engine's Unix socket into the container and only installing the Docker client.
	~[moodle]Using a virtualized hypervisor inside the container.#<p>This approach is not "Docker in Docker" but nested virtualization, and is not recommended for Docker in Docker.</p>
	~[moodle]Rebuilding the Docker Engine from source code inside the container.#<p>Rebuilding from source code is impractical and unnecessary.</p>
	####<p><strong>Explanation</strong>\: The recommended and much simpler method is to configure your container to communicate with an existing Docker Engine by bind mounting the Docker Engine's Unix socket (usually /var/run/docker.sock) into the container, and only installing the Docker client inside the container.</p>
}

// question: 8.7  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>What is the main disadvantage of running "Docker in Docker" by bind mounting the Docker Engine's Unix socket?</p>{
	~[moodle]Child containers will not be able to access the internet.#<p>Child containers can still access the internet if networking is configured correctly.</p>
	~[moodle]Child containers will not be persisted after the parent container is removed.#<p>Child containers are created directly by the host's Docker Engine, so they will exist independently of the parent container unless --rm is used.</p>
	=[moodle]The parent container will be able to see and interact with all Docker Engine resources (other containers, volumes, networks) on the host.
	~[moodle]The parent container will require too much CPU and memory resources.#<p>While it can consume resources, this is not the main disadvantage highlighted in this context.</p>
	####<p><strong>Explanation</strong>\: A drawback of this approach is that the parent container can see other containers, volumes, networks, and other resources managed by the Docker Engine you are sharing. This can pose security problems if sensitive information is present.</p>
}

// question: 8.8  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>Why is running multiple applications in a single container generally not recommended?</p>{
	~[moodle]The container will not be able to communicate with external services.#<p>Communication ability is not affected by the number of applications in a container.</p>
	=[moodle]It is more difficult to recover from failures, and can lead to extended downtime.
	~[moodle]Significantly increases the size of the container image.#<p>Increased image size is not the primary reason, but rather complexity in management and recovery.</p>
	~[moodle]The container will always run with root privileges, posing security risks.#<p>Root privileges are default, but not due to running multiple applications.</p>
	####<p><strong>Explanation</strong>\: Containers are designed to start and stop at will. Containers with multiple applications often have more complex startup procedures than single-application containers. This makes recovery more difficult, which can lead to extended downtime.</p>
}

// question: 8.9  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>Which solution is provided by Docker to easily manage multiple related containers on a single machine?</p>{
	~[moodle]Kubernetes.#<p>These are container orchestrators used to manage containers across multiple machines, not on a single machine.</p>
	~[moodle]Docker Swarm.#<p>These are container orchestrators used to manage containers across multiple machines, not on a single machine.</p>
	=[moodle]Docker Compose.
	~[moodle]HashiCorp Nomad.#<p>These are container orchestrators used to manage containers across multiple machines, not on a single machine.</p>
	####<p><strong>Explanation</strong>\: Docker Compose is a tool provided by Docker that makes it very easy to run and connect multiple containers on a single machine. It uses a single manifest file to define all the containers and their relationships.</p>
}

// question: 8.10  name: Chapter 8: Advanced Concepts and Docker Management
::Chapter 8\: Advanced Concepts and Docker Management::[html]<p>When an application inside a container sends messages to standard streams (stdout or stderr), which component does Docker use to collect and forward that data?</p>{
	~[moodle]Container runtimes.#<p>Container runtimes create, manage, and delete containers.</p>
	=[moodle]Logging drivers.
	~[moodle]Control groups.#<p>Control groups limit resource consumption.</p>
	~[moodle]Unix sockets.#<p>Unix sockets are used for communication between applications on the same machine, e.g., Docker CLI and daemon.</p>
	####<p><strong>Explanation</strong>\: When an application runs inside a container, Docker uses logging drivers to collect data sent to stdout or stderr streams. These drivers forward the data elsewhere, such as a directory on disk or an online log aggregation platform.</p>
}

// Chapter 9: Best Practices and Scaling with Docker
// question: 9.1  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>Which best practice is recommended when pulling images from Docker Hub or a private registry?</p>{
	~[moodle]Always pull the latest version to ensure it's up-to-date.#<p>Avoid using the latest tag because the version can change unexpectedly.</p>
	=[moodle]Only use verified images.
	~[moodle]Pull images from any source to increase diversity.#<p>Pulling images from any source is very risky and can lead to using malicious images.</p>
	~[moodle]Automatically recompile images from source code before use.#<p>Automatically recompiling is unnecessary and not a way to ensure image safety.</p>
	####<p><strong>Explanation</strong>\: One of the best practices is to always use verified images from Docker Hub or a trusted private registry. Verified images have the "Official Docker image" badge on Docker Hub, indicating they have been scanned and inspected by Docker.</p>
}

// question: 9.2  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>Why should you avoid tagging your Docker images as latest when pushing to a registry?</p>{
	~[moodle]The latest tag is automatically deleted after 24 hours.#<p>The latest tag is not automatically deleted.</p>
	=[moodle]You don't know which application version you will get when pulling the image, and the version can change unexpectedly.
	~[moodle]The latest tag is not supported by private registries.#<p>Most registries support the latest tag.</p>
	~[moodle]This increases the size of the Docker image on the registry.#<p>Tagging as latest does not increase image size.</p>
	####<p><strong>Explanation</strong>\: There are three reasons to avoid tagging images as latest: 1) you don't know which application version you will get when pulling a latest-tagged image. 2) the version can change unexpectedly when you pull the image again in the future. 3) version tags can be overwritten when pushing to Docker Hub, making rollbacks difficult.</p>
}

// question: 9.3  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>Which best practice related to users is recommended when running Docker containers?</p>{
	~[moodle]Always run containers with root privileges to ensure maximum compatibility.#<p>Running with root privileges is default but not recommended for security reasons.</p>
	~[moodle]Only use the nobody user to limit access.#<p>While nobody is a privileged user, the general recommendation is to run with a non-root user, not necessarily nobody specifically.</p>
	=[moodle]Run containers with a non-root user to avoid security concerns.
	~[moodle]Use the default docker user for all containers.#<p>There is no default docker user for containers. Containers run as root by default.</p>
	####<p><strong>Explanation</strong>\: A best practice is to use a non-root user when running containers. This keeps security teams happy and avoids a significant number of security concerns that arise when running Docker in production environments.</p>
}

// question: 9.4  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>Which tool provided by Docker helps easily run and connect multiple related containers on a single machine?</p>{
	~[moodle]Kubernetes.#<p>These are container orchestrators designed to manage applications across multiple machines.</p>
	~[moodle]Docker Swarm.#<p>These are container orchestrators designed to manage applications across multiple machines.</p>
	=[moodle]Docker Compose.
	~[moodle]Mesos.#<p>These are container orchestrators designed to manage applications across multiple machines.</p>
	####<p><strong>Explanation</strong>\: Docker Compose is a tool provided by Docker that makes it very easy to run and connect multiple containers on a single machine. It uses a single manifest file to define all the containers and their relationships.</p>
}

// question: 9.5  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>When should you consider using a container orchestrator like Kubernetes?</p>{
	~[moodle]When you only need to run a single application on one host.#<p>Docker Compose is more suitable for these use cases.</p>
	~[moodle]When you want to simplify the deployment of applications that only run locally.#<p>Docker Compose is more suitable for these use cases.</p>
	=[moodle]When you are running hundreds or thousands of containers in a production environment and need to scale, migrate, and route traffic.
	~[moodle]When you want to minimize the CPU and memory resource usage of containers.#<p>Minimizing resources is done by configuring resource limits (control groups) or optimizing Dockerfiles (multi-stage builds), not by using an orchestrator.</p>
	####<p><strong>Explanation</strong>\: While Docker works well for single applications, things get complicated very quickly when you are running hundreds or thousands of containers in a production environment. Container orchestrators solve these problems by using scheduling, networking, and service discovery tools to make scaling, migrating, and routing traffic to containers very easy.</p>
}

// question: 9.6  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>Which of the following is a key feature that Kubernetes provides?</p>{
	~[moodle]Tight integration with configuration management tools like Chef and Puppet.#<p>Kubernetes can integrate with configuration management tools, but that is not its primary feature.</p>
	=[moodle]The ability to seamlessly run hundreds of thousands of containers across multiple machines.
	~[moodle]Default persistent data storage functionality for all containers.#<p>Kubernetes provides persistent storage mechanisms (e.g., Persistent Volumes), but not default functionality for all containers.</p>
	~[moodle]A simple graphical user interface (GUI) for container management.#<p>Kubernetes has powerful CLI tools and many third-party GUIs, but Kubernetes itself is not a simple GUI.</p>
	####<p><strong>Explanation</strong>\: Kubernetes is a distributed system designed to seamlessly run and connect hundreds of thousands of containers as if they were all running on a single machine.</p>
}

// question: 9.7  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>Which tools are mentioned as being able to help you check for security vulnerabilities in each layer of a Docker image?</p>{
	~[moodle]Wireshark.#<p>These options are general network security or vulnerability scanning tools, but not specific Docker image scanning tools mentioned.</p>
	~[moodle]Nessus.#<p>These options are general network security or vulnerability scanning tools, but not specific Docker image scanning tools mentioned.</p>
	=[moodle]Clair, Trivy, and Dagda.
	~[moodle]Snort.#<p>These options are general network security or vulnerability scanning tools, but not specific Docker image scanning tools mentioned.</p>
	####<p><strong>Explanation</strong>\: Container image-scanning tools like Clair, Trivy, and Dagda inspect each layer of a Docker image and alert you to layers known to be malicious, as well as layers containing potentially harmful files.</p>
}

// question: 9.8  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>What problem can overwriting a latest tag on Docker Hub cause?</p>{
	~[moodle]Significantly increases image storage costs.#<p>Overwriting a tag does not significantly increase storage costs.</p>
	=[moodle]Makes it difficult to roll back to previous versions if you only use latest as the version tag.
	~[moodle]Prevents other users from pulling images from Docker Hub.#<p>It does not prevent users from pulling the image, but changes the default version they will receive.</p>
	~[moodle]Automatically converts the image to a multi-platform build.#<p>Not related to multi-platform builds.</p>
	####<p><strong>Explanation</strong>\: latest tags can be overwritten when you push them to Docker Hub. This makes it difficult to roll back to previous versions if you only use latest as the version tag.</p>
}

// question: 9.9  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>In what situations can running multiple applications in a single container be useful, although generally not recommended?</p>{
	~[moodle]When complete isolation between applications is needed.#<p>Running multiple applications in a single container would reduce isolation, not enhance it.</p>
	=[moodle]To emulate a virtual machine or a simple service cluster within a single container.
	~[moodle]When applications do not require any network resources.#<p>Not related to network resource requirements.</p>
	~[moodle]To simplify the continuous update and deployment process.#<p>This makes the startup process more complex, making recovery difficult and thus not simplifying continuous updates/deployments.</p>
	####<p><strong>Explanation</strong>\: Although generally not recommended, running multiple applications in a single container can be useful for emulating a virtual machine (e.g., for testing Ansible playbooks) or emulating a service cluster within a single container for simplicity (e.g., Kubernetes in Docker).</p>
}

// question: 9.10  name: Chapter 9: Best Practices and Scaling with Docker
::Chapter 9\: Best Practices and Scaling with Docker::[html]<p>When an application inside a container runs as PID 1 (the parent process), what happens regarding signal handling (e.g., Ctrl+C) if the application is launched using ENTRYPOINT in shell form?</p>{
	~[moodle]The application will receive signals directly and handle them correctly.#<p>This is the desired behavior when using exec form.</p>
	~[moodle]Provided arguments will be processed directly by the application.#<p>Arguments passed will also be sent to the shell, not the application, when using shell form.</p>
	=[moodle]The shell will trap signals instead of the application, preventing the application from handling them.
	~[moodle]The container will automatically restart after receiving a signal.#<p>The container does not automatically restart; the signal handling behavior will be affected.</p>
	####<p><strong>Explanation</strong>\: If ENTRYPOINT uses shell form, your program will be spawned as a child process of CMD or sh. This means that any signals sent to your application from the terminal (like Ctrl+C) will be trapped by the shell instead of your program, and any code in your application that runs when these events occur will not be executed.</p>
}