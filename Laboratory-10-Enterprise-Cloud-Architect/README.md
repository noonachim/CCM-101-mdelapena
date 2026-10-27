# Laboratory 10 – Mission 10: The Enterprise Cloud Architect

**Course:** CCM101 – Cloud Computing | **Student:** cbadongen

A persistent, two-tier private cloud stack: **WordPress** (web tier) + **MySQL 8.0** (data tier) on Docker Compose, running in an Ubuntu Server VM (VirtualBox), hardened with UFW and protected by scheduled backups.

## Quick start

```bash
cp .env.example .env && nano .env && chmod 600 .env   # set strong passwords
docker compose up -d
sudo ./setup-ufw.sh
./automation-script.sh health
```

Browse to `http://localhost:8080` on the host laptop (VirtualBox NAT forwards 8080 → VM 8080; SSH 2222 → 22).

## Contents

| File | Purpose |
|---|---|
| `architecture-diagram.png` | Network topology and architecture |
| `docker-compose.yml` | Infrastructure as Code for the stack |
| `.env.example` | Secrets template |
| `setup-ufw.sh` | Host firewall (default deny; allow 22, 8080) |
| `automation-script.sh` | Backup, restore, health check (cron at 2:00 AM) |
| `operational-manual.md` | Deploy / secure / maintain guide for the client IT team |
| `final-reflection.md` | Mission 1–10 reflection |
