# Laboratory 02 – Build the Cloud Infrastructure Blueprint

## Mission Overview
CloudNova Technologies has onboarded me for my first official project. Before any servers are deployed, I was tasked with investigating a Linux cloud server (via KillerCoda) to identify its infrastructure components — compute, storage, networking, and identity — and to prepare a Cloud Infrastructure Assessment Report for senior engineers to reference when designing the final cloud architecture.

## Objectives
- Explain the major components of cloud infrastructure.
- Investigate the hardware and software resources available in a Linux environment.
- Differentiate compute, storage, networking, and identity resources.
- Interpret the relationship between cloud infrastructure components.
- Create professional technical documentation using Markdown.
- Continue building a structured GitHub Cloud Computing Portfolio.

## Cloud Infrastructure Components
- **Compute** – the CPU and processing power that runs applications (see `cloud-components.md`).
- **Storage** – the disk capacity and file systems that persist data.
- **Networking** – the hostname/IP that connects the server to users and other services.
- **Operating System** – the Linux OS that manages hardware and runs software.

Full details and analysis are documented in `cloud-components.md`.

## Tools Used
- KillerCoda Playground (Linux environment)
- Draw.io (cloud architecture diagram)
- GitHub (version control and documentation)
- Markdown

## Linux Commands Executed
| Command | Purpose |
|---|---|
| `cat /etc/os-release` | Identify OS |
| `uname -r` | Identify kernel version |
| `cat /proc/cpuinfo` | View CPU model |
| `nproc` | Count CPU cores |
| `free -h` | Check RAM |
| `df -h` | Check disk capacity |
| `findmnt` | List mounted file systems |
| `hostname` | Get hostname |
| `ip a` | Get IP address |

## Skills Learned
- Investigating a Linux server's hardware and software specs from the command line.
- Mapping cloud infrastructure concepts (compute, storage, networking, IAM) to real observed resources.
- Comparing equivalent services across AWS, Azure, and GCP.
- Creating a cloud architecture diagram in Draw.io.
- Structuring and maintaining a GitHub documentation portfolio.

## Challenges Encountered
- KillerCoda sessions are temporary, so all documentation had to be captured and saved outside the environment before it expired.
- Understanding the naming differences for equivalent services across the three major cloud providers.