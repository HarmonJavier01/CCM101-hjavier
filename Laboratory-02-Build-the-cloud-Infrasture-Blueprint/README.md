# Laboratory Activity 2: Build the Cloud Infrastructure Blueprint

## Mission Overview
As a newly onboarded cloud engineer at CloudNova Technologies, this mission involved investigating the infrastructure components of a Linux server running on the KillerCoda Playground before any cloud services are deployed. The goal was to identify how compute, storage, networking, and identity services work together, and to document these findings as if preparing technical documentation for a client.

## Objectives
- Explain the major components of cloud infrastructure.
- Investigate the hardware and software resources available in a Linux environment.
- Differentiate compute, storage, networking, and identity resources.
- Interpret the relationship between cloud infrastructure components.
- Create professional technical documentation using Markdown.
- Continue building a structured GitHub Cloud Computing Portfolio.

## Cloud Infrastructure Components
- **Compute:** Provides the processing power to run workloads (see cloud-components.md).
- **Storage:** Persistently stores data and files, decoupled from compute.
- **Networking:** Connects compute and storage to users and the internet.
- **Operating System:** Manages hardware and provides the platform for all software.

## Tools Used
- KillerCoda Playground (Linux terminal environment)
- GitHub (version control and documentation hosting)
- Markdown (technical documentation)
- Draw.io (cloud architecture diagram)

## Linux Commands Executed

| Command | Purpose |
|---|---|
| `cat /etc/os-release` | Identify the operating system |
| `uname -r` | Check kernel version |
| `lscpu \| grep "Model name"` | Get CPU model |
| `nproc` | Count CPU cores |
| `free -h` | Check total RAM |
| `df -h` | Check disk capacity |
| `mount \| grep "^/dev"` | List mounted filesystems |
| `hostname` | Get server hostname |
| `hostname -I` | Get IP address |

## Skills Learned
- Using core Linux commands to inspect system, storage, and network information
- Structuring and formatting technical documentation in Markdown
- Comparing equivalent infrastructure services across AWS, Azure, and GCP
- Designing a basic cloud architecture diagram
- Maintaining an organized, professional GitHub repository through structured commits

## Challenges Encountered
[Fill in anything that actually gave you trouble — e.g., interpreting certain command outputs, formatting Markdown tables correctly, or KillerCoda session timeouts requiring a restart.]