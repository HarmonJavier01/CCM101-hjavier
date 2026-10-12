
# Mission Reflection

**1. Why automation matters.** With hundreds of servers, nobody can log into each one and type the same commands. It would take all day, and sooner or later someone would skip a step or mistype something. A script does the same thing every time, and cron makes sure it actually happens.

**2. Dangers of automation.** A mistake gets repeated just as fast as a correct command. If a script had a typo in a delete command and ran on 1,000 servers, they would all lose data at the same time. Cron also runs quietly in the background, so the problem might not be noticed until much later. At the very least, a script should be tested on one machine first.

**3. Bash vs. Docker Compose.** In `backup.sh` I told the computer each step in order: make the folder, compress the data, print a message. In Mission 6, the Compose file only described what I wanted running, like the image and the ports, and Docker worked out the steps. Bash gave me more control but I had to think about the order. Compose was shorter but felt more like filling in a form.

**4. How my understanding changed.** In Lab 1 I thought the cloud was basically someone else's computer. The early labs showed me there is much more to it, and I struggled at first with Git, especially authentication errors and setting the right remote URL when pushing to GitHub. Fixing those problems taught me to read error messages instead of guessing. By Lab 9 I could see how deploying, monitoring, securing, and automating all connect.

**5. Favorite role.** My favorite was the Cloud Security Engineer because I could see the firewall change what the server allowed in. Before UFW was on, everything was open, and after I set default deny, only SSH and port 8080 got through. It felt like I was actually protecting something, not just running commands.


