# Mission 5 Reflection

Object storage makes way more sense than block storage once you're
talking about millions of photos. There's no folder tree to worry
about — each photo just becomes an object with its own ID and metadata,
sitting in a flat bucket. That means the system doesn't slow down or
hit some folder-depth wall as it scales, which is exactly the problem a
photo-sharing app would eventually run into with block storage. Photos
also get pulled in and out over a plain HTTP API instead of needing to
be mounted like a disk, which fits how a web app actually works.

Docker made the whole deployment a lot less painful than it could have
been. Instead of manually installing MinIO and hoping all its
dependencies lined up right, one command pulled a ready-to-go image and
had a server running in seconds. It's also isolated from the host
machine, so nothing about my setup gets messy, and the exact same
command would work on basically any machine with Docker installed.

A bucket is basically the top-level container for objects — like a
root folder, except there's no real nesting underneath it. Names have
to be unique, and permissions usually get set at the bucket level
rather than on individual files.

For redundancy, big companies spread copies of data across multiple
physical servers and often multiple data centers entirely, sometimes
using erasure coding on top of that. That's the whole idea behind AWS
S3 promising such extreme durability numbers.

Running into a dead Docker image mid-lab and having to figure out why
actually helped more than it hurt — it forced me to read logs and
error messages instead of just copy-pasting, and I feel noticeably more
comfortable in the command line now than when this lab started.