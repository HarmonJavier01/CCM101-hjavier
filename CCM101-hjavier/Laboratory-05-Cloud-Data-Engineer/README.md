# Laboratory 5: Cloud Data Engineer

## Mission Overview
This lab was built around a fictional client's problem: they're building
a photo-sharing app, and containers aren't a safe place to keep
user-uploaded images long-term since they get wiped. The task was to
stand up a proof-of-concept Object Storage server using MinIO, confirm
it works end-to-end, and show that files can actually be uploaded and
retrieved through it.

## Objectives
- Tell Block, File, and Object Storage apart and know when each makes sense
- Get an S3-compatible object storage server (MinIO) running in Docker
- Reach a cloud service's web UI through port forwarding, not just the terminal
- Create a bucket and upload something into it
- Write up the process in Markdown as I went
- Keep building out my GitHub Cloud Computing Portfolio

## Tools Used
- KillerCoda (Ubuntu Playground)
- Docker
- MinIO (S3-compatible Object Storage)
- GitHub
- Markdown

## Skills Learned
- Running a containerized service with Docker — port mapping and
  environment variables specifically
- Actually understanding, not just memorizing, the differences between
  Block, File, and Object Storage
- Accessing something running on a remote sandbox through a
  port-forwarding panel instead of assuming `localhost` will just work
- Creating and managing a bucket through a web console
- Troubleshooting a real deployment problem (a Docker image getting
  discontinued mid-lab) instead of assuming my command was just wrong
- Writing up technical steps clearly enough that someone else could
  follow them