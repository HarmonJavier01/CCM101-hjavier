cat > reflection.md <<'EOF'
# Mission Reflection

**1. Why automation matters.** With hundreds of servers, nobody can log into each one and type the same commands. It would take all day, and sooner or later someone would skip a step or mistype something. A script does the same thing every time, and cron makes sure it actually happens.

**2. Dangers of automation.** A mistake gets repeated just as fast as a correct command. If a script had a typo in a delete command and ran on 1,000 servers, they would all lose data at the same time. Cron also runs quietly in the background, so the problem might not be noticed until much later. At the very least, a script should be tested on one machine first.

**3. Bash vs. Docker Compose.** In `backup.sh` I told the computer each step in order: make the folder, compress the data, print a message. In Mission 6, the Compose file only described what I wanted running, like the image and the ports, and Docker worked out the steps. Bash gave me more control but I had to think about the order. Compose was shorter but felt more like filling in a form.

**4. How my understanding changed.** In Lab 1 I thought the cloud was basically someone else's computer. [Add 2 or 3 sentences: which lab changed your mind, and what you struggled with, like the git authentication problems or a command that failed.] By Lab 9 I could see how deploying, monitoring, securing, and automating all connect.

**5. Favorite role.** My favorite was [role] because [your real reason, like what you actually built or saw working]. [One more sentence about something specific from that lab.]
EOF

wc -w reflection.md