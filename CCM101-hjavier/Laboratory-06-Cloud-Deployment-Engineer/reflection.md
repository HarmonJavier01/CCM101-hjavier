# Mission 6 Reflection

## 1. Docker Compose vs. manual commands
Writing a docker-compose.yml file makes a cloud engineer's job easier because the whole setup lives in one readable file instead of several long commands. In earlier missions, I had to type each docker run command with its flags and hope I didn't miss anything. With Compose, a single command, docker-compose up -d, deploys everything. The file can also be reused, edited, and saved in GitHub, which makes the deployment repeatable.

## 2. Indentation errors in YAML
YAML uses indentation to define structure, and it does not allow tabs. If I use a Tab instead of spaces, Compose cannot parse the file and shows an error, so the containers never start. Even one misplaced space can put a setting under the wrong block, so careful formatting matters.

## 3. Why use environment variables?
Environment variables like MYSQL_PASSWORD pass configuration into containers without changing the image itself. This keeps settings separate from the code and lets the same image run in different setups. In this lab, both services use the same values so Nextcloud can authenticate with MariaDB. In a real deployment, passwords should not be hardcoded in a file pushed to GitHub.

## 4. Deploying Nextcloud in minutes
It felt surprising and rewarding to see an enterprise-grade storage system running within minutes. Two containers were pulled, linked, and started with one command. Normally, installing a web app and setting up its database would take much longer, but a short YAML file handled it all.

## 5. How my understanding has evolved
In Mission 1, I mostly saw cloud computing as online services and storage that I used. Now I understand it as infrastructure that can be defined in code, deployed repeatedly, and torn down cleanly. I moved from running single containers to building a multi-tier system, and I now see why Infrastructure as Code is such an important skill for cloud engineers.