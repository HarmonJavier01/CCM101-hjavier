# Mission Reflection

## 1. Which cloud infrastructure component do you think is the most important? Why?
Of the four components I explored, I believe networking is the most important. Compute and storage resources are only useful if they can be accessed and connected — without networking, a virtual machine with the best CPU or the largest disk would be isolated and unusable. Networking is what allows compute, storage, and users to communicate, which is the entire point of "cloud" computing as opposed to running an isolated local machine. It's also the layer where most cloud outages and security issues originate, which reinforced how critical it is to get right during infrastructure design.

## 2. How does Linux support cloud computing?
Linux plays a foundational role in cloud computing because most cloud servers, containers, and infrastructure tools are built on it. It's open-source, lightweight, and highly configurable, which makes it ideal for provisioning at scale. During this lab, I used core Linux commands to inspect the KillerCoda server's OS, CPU, memory, and network details — the same type of investigation a real cloud engineer would perform before deployment. Linux's scriptability also makes it easy to automate cloud provisioning, which is essential for managing large, dynamic infrastructure.

## 3. Why is technical documentation important before deploying infrastructure?
Documentation ensures that infrastructure decisions are understood, repeatable, and auditable. Before deployment, documenting server specs, network details, and architecture diagrams helps teams catch misconfigurations early, communicate clearly across engineers, and maintain accountability. Without it, troubleshooting becomes guesswork, and onboarding new team members becomes far harder.

## 4. What new skills did you learn during this laboratory activity?
I strengthened my Linux command-line skills for gathering system information, improved my Markdown documentation formatting, and learned how to compare equivalent services across AWS, Azure, and GCP. I also practiced structuring a professional GitHub repository and creating a basic cloud architecture diagram.

## 5. How has your GitHub portfolio improved after completing this mission?
My portfolio now includes a well-organized, documented laboratory folder that demonstrates not just coding ability but technical writing and cloud reasoning skills — qualities recruiters value beyond raw code.