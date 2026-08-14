# Overview 
This lab covers core virtualization concepts (hypervisors, virtual machines, and containers) and applies them in a hands-on scenario of creating VM, Incident Response — Email Outage

## Concept Covered

### Why Virtualization?
Before virtualization, the standard was "one server = one application," which led to:
- High cost —       separate physical hardware for every service
- Low utilization — most servers ran at only 5–20% capacity
- Slow deployment — new servers took days or weeks to provision
- Poor scalability — scaling meant buying more hardware
  
Virtualization solves this by letting multiple isolated systems share one physical server safely.

### Hypervisors
A hypervisor divides a physical machine into multiple virtual ones, allocating CPU, memory, and storage while keeping each VM isolated.

There are 2 types of hypervisors:
Type1: Directly on hardware best for production servers, database, date centers
Type2: Within the existing OS best for Testing, learning, malware analysis, running tools like Kali Linux

### Lab Machines (VMs)
- Each VM has its own virtual CPU, RAM, storage, and network.
- Runs any OS independently of the host.
- Fully isolated — one VM failing doesn't affect others.

### Containers
- Lightweight, isolated environments that run a single application.
- Share the host's kernel instead of running a full OS, so they start almost instantly and use fewer resources.
- Must match the host system's OS type (e.g., no Windows containers on a Linux host).
- Commonly deployed with Docker.

## Lab Walkthrough
### Incident Response — Email Outage
- Company-wide email outage reported.
- Investigated the Lab Machines section and found Mail-SERVER in an Error state.
- Restarted the VM; service was restored with no further errors.

### Provisioning a New VM
Created a VM for the marketing team's website with the following specs:

Name: 	Marketing-VM
CPU:    Cores	4
Memory: 	8 GB
Disk Size:	100 GB
