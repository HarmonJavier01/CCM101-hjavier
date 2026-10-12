
# Mission Reflection

**1. Host-based firewall.** A host firewall runs on the server itself, so it still works even if someone gets past the network firewall or is already inside the network. The server checks every connection against its own rules and drops what is not allowed. No single layer has to stop everything.

**2. Managing open ports.** Each open port is a service waiting for connections, and attackers can scan it, guess passwords, or look for bugs. If I close the ports I do not need, there are fewer ways in. In this lab only 22 and 8080 stayed open.

**3. Database port on the internet.** If port 3306 is open to everyone, anybody can try to log in to MySQL or use a known bug. Bots scan the internet for these ports all the time. If the database is breached, customer data can leak. It should only be reachable from the app server or a private network.

**4. Change in perspective.** Before this lab, I thought a server was only at risk if someone was specifically targeting it. When I first ran curl on my container, it failed with "Connection reset by peer" because nginx was not ready yet, which showed me how many things can go wrong even with a simple setup. After I deployed the app, the server was reachable on every port until I turned on UFW. That made me realize one forgotten setting is enough to leave a server open.

**5. My GitHub portfolio.** My repo now has eight lab folders, each with a README, notes in Markdown, and screenshots. Looking back, the early labs look simpler than the later ones, and I can see my documentation getting more organized as I went. I am happiest with this lab and the earlier Docker labs because I could show my work with real terminal screenshots.


