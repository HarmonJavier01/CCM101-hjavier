# Reflection Prep Notes — Laboratory 04: Cloud-Native Engineer

*These are talking points and prompts to help you think through each question —
not answers to copy. Use them to write your own 250–350 word reflection in
`reflection.md`, based on what you actually observed in your KillerCoda terminal.*

---

## 1. Boot time & setup: Docker container vs. installing an OS on a VM

- A VM has to boot an entire OS kernel before anything else can run.
- A container skips that step — it's really just an isolated process that
  shares the host's already-running kernel.
- That's the core reason for the "minutes vs. seconds" gap mentioned in the
  handout.
- **Prompt to answer yourself:** How long did it actually take from
  `docker run` to your `curl` succeeding? Compare that to what you know (or
  have read) about installing and configuring an OS on a VM from scratch.

## 2. Why is port mapping (`-p 8080:80`) necessary?

- The container has its own isolated network namespace.
- Nginx inside the container is listening on port 80 of *that* namespace —
  not the host's.
- Without `-p 8080:80`, nothing outside the container (including your
  `curl` command) can reach it.
- **Prompt to answer yourself:** What do you think would have happened if
  you ran `curl http://localhost:8080` *without* including `-p 8080:80` in
  your `docker run` command? Why?

## 3. What happens to the data when you `docker rm` a container?

- Anything written inside the container's writable layer is deleted along
  with the container.
- The original image (`nginx`) is untouched — it's read-only and stays on
  the host, which is why you could run a new container from it again
  without re-pulling.
- Data would only survive if it had been placed in a volume or bind mount
  (something you'll cover in a future checkpoint/lab).
- **Prompt to answer yourself:** Did you notice the `nginx` image was still
  there (`docker images`) even after you removed the container? What does
  that tell you about the difference between an image and a container?

## 4. How does containerization change how developers and IT ops teams work together (DevOps)?

- A container packages the app *and* its environment (dependencies,
  config, runtime) together.
- That closes the gap between what a developer tests locally and what
  operations deploys to production — the classic "works on my machine"
  problem.
- Deployment becomes more about running a known image consistently, rather
  than manually configuring a server to match a developer's setup.
- **Prompt to answer yourself:** In your own words, why would a client like
  the one in the mission brief care about this — beyond just "faster boot
  times"?

## 5. How is your GitHub portfolio evolving?

- This one is really about you looking at your own repo across
  Labs 1 through 4.
- **Prompts to answer yourself:**
  - What's different about your repo structure now compared to after Lab 1?
  - What skills or artifact types have you accumulated (diagrams, Markdown
    docs, screenshots, multi-cloud comparisons, now containerization)?
  - If a future employer opened your repo, what story would it tell about
    your growth?

---

## Before you submit

- Combine your answers into one reflection (either flowing prose or short
  paragraphs per question — check your instructor's preferred format).
- Aim for 250–350 words total.
- Answer based on what *you* observed running the commands, not just the
  general concepts above.