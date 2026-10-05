# Two-Tier Architecture

A two-tier architecture splits an application into two layers: an application (web) tier that users talk to, and a database tier that stores the data. The tiers communicate over a network.

## The Web/Application Tier
This tier runs the application logic and serves the user interface. It handles HTTP requests from browsers, processes user actions (logging in, uploading files), and queries the database when it needs data. In this lab, the Nextcloud container is the web tier.

## The Database Tier
This tier stores persistent data such as user accounts, credentials, and file metadata. It only accepts requests from the application tier and is not exposed to users directly. In this lab, the MariaDB container is the database tier.

## Why Separate Them?
Separating them lets each container be scaled, updated, backed up, and secured independently. If the web container crashes or is upgraded, the database and its data are unaffected. Keeping the database off the public-facing container also reduces the attack surface and follows the single-responsibility principle of container design.