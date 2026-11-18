# ☁️ Nimbus

Nimbus started from a simple need: keeping the photos and files that matter most to me on hardware I own, instead of relying only on iCloud. It has since become the place where I self-host my own side projects.

## What it does

- **Personal cloud**: photos, documents, code, games and media, accessible from my Windows PCs and my iPhone
- **Remote access**: private access from anywhere, with no admin interface exposed to the internet
- **Self-hosting**: backends for my side projects, running in Docker

## Stack

| | |
|---|---|
| Hardware | UGREEN NASync DXP4800 Plus + UPS |
| OS | UGOS |
| Storage | RAID 5, Btrfs |
| Remote access | Tailscale |
| File access | SMB (Windows, iOS Files) |
| Services | Docker |

## Data & backups

Data is organized in one shared folder per category (Documents, Photos, Dev, Games, Media), each with its own snapshot rules.

RAID is not a backup, so the important data also lives in an independent copy outside the NAS.

## Roadmap

- [x] NAS setup, RAID 5 pool, shared folders
- [x] Remote access via Tailscale
- [ ] Move to 4 × 12 TB drives
- [x] Host the backend of [Flip](#), my mobile app (Go + PostgreSQL, Docker)
- [ ] Quality-of-life services: AdGuard Home, Syncthing, PairDrop
- [ ] Media server (Jellyfin)
- [ ] Automated external backups
