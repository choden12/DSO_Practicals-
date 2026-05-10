# Containerization and Docker

## What is Containerization?
- At first, when I heard the concept of containerization during class, I did not understand it. According to the slides, containerization refers to "the packaging of applications with all dependencies into one isolated package.

- Containerization is basically all elements needed for the execution of an application  code, system tools, libraries, are included into the container along with the application itself. This software is guaranteed to work on any computer supporting containerization, no matter which software is installed there. Containers don’t influence one another.

- Through my research, I also learned that containerization is not a new idea. Linux has had container-like features for many years, including chroot, namespaces, and cgroups. What Docker did was package these existing Linux features into a user-friendly tool that made containers accessible to everyone. Docker did not invent containers, but it popularized them.

### Limitations of Containerization 
- Shared Kernel: All containers use the same host’s kernel. This implies that a bug in the kernel can have repercussions on all containers. For strict isolation, virtual machines are still preferred.
- Operating System Constraint: Linux-based containers need a Linux kernel. This implies that in Windows and Mac, Docker runs its own Linux VM under the hood. Windows containers exist but are rare.

## Containerization vs. Virtualization (key differences)

### What is Virtualization?
- Virtualization refers to the process whereby different virtual machines can be run on a single physical machine. In the virtual machine, there is a full guest OS, virtual hardware, and the application. The virtualization software (hypervisor), which comes in forms like VMware, Virtual Box, or Hyper-V, is what bridges the gap between the hardware and the virtual machine.

- Large (gigabytes – often 5GB to 20GB per VM)

- Limited (VM must be compatible with hypervisor)

### What is Containerization?
- Containerization refers to a process whereby an application and all the necessary files needed to run the application are packaged together inside a single unit referred to as a container. Containerized applications differ from virtual machines since they do not have their own guest operating systems.

- Small (megabytes – often 50MB to 500MB per container)

- High (runs anywhere with Docker installed)

## What is Docker?
- Docker is an open source technology that enables developers to deploy, scale, and manage applications using containers. Docker is the most widely adopted containerization technology globally.

### Characteristics of Docker

**Lightweight**
- Containers in Docker lack an entire operating system. Instead, the containers share the kernel with the host operating system. As a result, the containers are very small (in megabytes rather than gigabytes) and quick to initialize.

**Portable**
- Docker containers will behave the same way regardless of whether it is Windows, Mac, Linux, or even cloud-based (AWS, Azure, Google Cloud). This helps to solve the problem of "it works on my machine."

**Version Controlled**
- A Docker image can be given a version tag. This will make it possible for you to rollback to earlier versions and run different versions of the same application at the same time.
