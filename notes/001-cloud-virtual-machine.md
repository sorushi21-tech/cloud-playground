# Virtualization Notes

## What Is Virtualization?

Virtualization is the process of creating a virtual version of a physical computing resource, such as a server, operating system, storage device, or network. It allows one physical machine to run multiple isolated virtual environments.

In cloud computing, virtualization is one of the core technologies that makes it possible to create and manage virtual machines, storage, and networks on demand.

## Why Virtualization Is Used

Virtualization helps cloud providers and organizations use hardware more efficiently. Instead of dedicating one physical server to one application, multiple virtual machines can run on the same physical server.

Main purposes:

- Better use of physical hardware
- Faster creation of servers and environments
- Lower infrastructure cost
- Easier backup, migration, and recovery
- Isolation between applications and users
- Support for scalable cloud services

## Hypervisor

A hypervisor is software that creates and manages virtual machines. It sits between the physical hardware and the virtual machines.

The hypervisor allocates CPU, memory, storage, and network resources to each virtual machine.

## Types Of Hypervisors

### Type 1 Hypervisor

A Type 1 hypervisor runs directly on the physical hardware.

It is also called a bare-metal hypervisor.

Examples:

- VMware ESXi
- Microsoft Hyper-V
- KVM
- Xen

Advantages:

- High performance
- Strong isolation
- Commonly used in data centers and cloud platforms

### Type 2 Hypervisor

A Type 2 hypervisor runs on top of an existing operating system.

It is also called a hosted hypervisor.

Examples:

- VirtualBox
- VMware Workstation
- Parallels Desktop

Advantages:

- Easy to install and use
- Good for learning, testing, and development

Limitations:

- Lower performance than Type 1 hypervisors
- Depends on the host operating system

## Virtual Machine

A virtual machine, or VM, is a software-based computer that runs inside a physical machine. Each VM has its own virtual CPU, memory, storage, network interface, and operating system.

Example:

A single physical server can run:

- One Linux VM for a web server
- One Windows VM for an application
- One database VM
- One test environment VM

Each VM behaves like an independent computer.

## Host And Guest

The host is the physical machine that provides the actual hardware resources.

The guest is the virtual machine running on the host.

Example:

- Host: Physical server
- Guest: Ubuntu VM, Windows Server VM, or any other virtual machine

## Resource Allocation

The hypervisor divides physical resources among virtual machines.

Common virtual resources:

- vCPU: Virtual CPU assigned to a VM
- RAM: Memory allocated to a VM
- Virtual disk: Storage used by a VM
- Virtual NIC: Network interface used by a VM

Resources can often be increased or decreased depending on workload needs.

## Types Of Virtualization

### Server Virtualization

Server virtualization allows multiple virtual servers to run on one physical server.

This is widely used in cloud platforms such as AWS, Azure, and Google Cloud.

### Storage Virtualization

Storage virtualization combines physical storage from multiple devices and presents it as a single storage resource.

Benefits:

- Easier storage management
- Better utilization
- Flexible data allocation

### Network Virtualization

Network virtualization creates virtual networks, routers, switches, firewalls, and load balancers using software.

Benefits:

- Faster network setup
- Better isolation
- Easier security control

### Desktop Virtualization

Desktop virtualization allows users to access a desktop environment remotely from another device.

Example:

A user logs in from a laptop and accesses a virtual desktop hosted in a data center.

### Application Virtualization

Application virtualization allows applications to run in isolated environments without being fully installed on the user's operating system.

## Virtualization In Cloud Computing

Cloud computing depends heavily on virtualization. Cloud providers use virtualization to offer computing resources as services.

For example, when a user creates an EC2 instance in AWS or a virtual machine in Azure, the cloud provider creates a VM on its physical infrastructure.

Virtualization enables:

- Infrastructure as a Service
- Rapid provisioning
- Multi-tenancy
- Elastic scaling
- Pay-as-you-go resource usage

## Multi-Tenancy

Multi-tenancy means multiple customers can share the same physical infrastructure while remaining isolated from each other.

Virtualization makes this possible by separating each customer's workloads into isolated virtual machines or containers.

## Benefits Of Virtualization

- Reduces hardware cost
- Improves server utilization
- Makes server deployment faster
- Supports disaster recovery
- Simplifies testing and development
- Allows workload migration
- Improves scalability
- Provides isolation between systems

## Limitations Of Virtualization

- Performance may be lower than physical hardware
- Requires proper resource management
- Hypervisor failure can affect many VMs
- Security misconfiguration can create risk
- Some workloads may need dedicated hardware

## Virtual Machine Lifecycle

Common VM lifecycle steps:

1. Create a VM
2. Select an operating system image
3. Allocate CPU, memory, storage, and network resources
4. Start the VM
5. Install or run applications
6. Monitor performance
7. Resize or migrate if needed
8. Stop, restart, or delete the VM

## Virtualization Vs Containerization

Virtual machines virtualize the hardware and run a full operating system.

Containers virtualize the operating system environment and share the host OS kernel.

| Feature       | Virtual Machine      | Container          |
|---------------|----------------------|--------------------|
| Virtualizes   | Hardware             | Operating system   |
| OS            | Full guest OS        | Shares host kernel |
| Startup       | Slower               | Faster             |
| Size          | Larger               | Smaller            |
| Isolation     | Strong               | Process-level      |
| Example tools | VMware, Hyper-V, KVM | Docker, Kubernetes |

## Common Virtualization Terms

- Hypervisor: Software that creates and manages VMs
- VM: Virtual machine
- Host: Physical machine running VMs
- Guest: VM running on the host
- Snapshot: Saved state of a VM
- Image: Template used to create a VM
- Migration: Moving a VM from one host to another
- Provisioning: Creating and configuring a VM
- vCPU: Virtual CPU assigned to a VM