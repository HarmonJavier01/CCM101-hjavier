# Cloud Storage Research: Block, File, and Object Storage

Before building the storage server, I looked into how the three main
types of cloud storage actually differ, since picking the right one
matters a lot once you're dealing with millions of files.

| Storage Type | How does it store data? | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Chops data into fixed-size blocks, each addressed individually, then attaches directly to a server like a raw hard drive would | Databases, boot volumes, anything needing fast, low-latency reads/writes | AWS EBS |
| File Storage | Keeps data in a familiar folder/file hierarchy, shared out over a network protocol like NFS or SMB | Shared drives, home directories — situations where multiple users or servers need the same files | AWS EFS |
| Object Storage | Treats each item as a standalone "object" — the file itself plus metadata and a unique ID — sitting in a flat bucket instead of nested folders | Huge volumes of unstructured data: photos, videos, backups, static assets | AWS S3 |

## Why Object Storage Wins Here

Millions of photos is exactly the kind of problem Object Storage was
built for. There's no folder tree to get bogged down in — everything
lives as a flat object with its own ID and metadata attached, so the
system doesn't care whether it's holding a thousand files or a billion.
Block and File Storage both start to strain once you're past a certain
scale (deep folder structures, filesystem limits, that kind of thing),
but Object Storage just keeps adding more nodes. It's also accessed
over plain HTTP through an API rather than needing to be mounted like a
disk, which lines up naturally with how a web app actually uploads and
serves images to users.