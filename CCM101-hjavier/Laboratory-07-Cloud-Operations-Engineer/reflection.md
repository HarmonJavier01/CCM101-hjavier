# Reflection: Mission 7 - The Cloud Operations Engineer

## 1. Why is it important to check the host server's resources even if your containers are running perfectly?


- Containers share the host's CPU, RAM, and disk
- A healthy container can hide a host that is nearly out of memory or disk
- Full disk or low memory can crash services all at once
- My host baseline: 1.9 GiB RAM, 1487 MiB available, 97.7% CPU idle

## 2. If a user complains that they cannot log into a web application, how would the docker logs command help you solve the problem?


- Shows what the app received and returned (401, 403, 500, stack traces)
- Find the log lines around the time of the complaint
- Shows whether the request reached the app at all
- Example from my lab: the 404 line for /hidden-admin-page

## 3. What is the difference between monitoring logs (Checkpoint 4) and monitoring metrics (Checkpoint 5)?


- Logs = records of individual events (what happened)
- Metrics = numbers over time (how much, how fast)
- Metrics show that something is wrong, logs show why
- My metrics: CPU 0.00%, memory 2.754MiB

## 4. How do you think large enterprise companies monitor thousands of containers at the same time?


- Can't check containers manually, so they automate
- Prometheus collects and stores metrics from all containers
- Grafana turns the data into dashboards and alerts
- Mention any tools from my Chapter 7 notes

## 5. How has your ability to troubleshoot Linux environments improved?


- Commands I can now use: free, df, top, docker logs, docker stats, grep
- What I would check first if a server were slow or a site were down
- Any problem I hit in this lab and how I fixed it