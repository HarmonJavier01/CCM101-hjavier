# MinIO Deployment Documentation

## Docker Command Used
```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  -e "MINIO_BROWSER=on" \
  bitnamilegacy/minio:2025.7.23-debian-12-r5
```

> The original lab sheet called for `minio/minio`, but that image stopped
> being freely available on Docker Hub as of October 2025. I switched to
> `bitnamilegacy/minio` instead, which meant adding `MINIO_BROWSER=on` —
> without it the web console never starts, and you just get a 502 error
> trying to reach it.

## Web Console Port
Port **9001** is where the web console lives. It's separate from port
9000, which handles the actual S3 API traffic. 9001 is what you'd point
a browser at if you want the visual dashboard instead of hitting the API
directly.

## Bucket Created
**Bucket name:** `client-photos`

This is where the client's photos get stored for this proof-of-concept.

## What the `-e` Flags Actually Do
- `MINIO_ROOT_USER` — the admin username for logging into the console
- `MINIO_ROOT_PASSWORD` — the password that goes with it
- `MINIO_BROWSER` — turns the web console on or off; had to set this to
  `on` manually since the Bitnami image ships with it disabled by default

Passing these in as environment variables instead of baking them into
the image means the credentials aren't hardcoded anywhere — you set them
fresh each time you run the container.