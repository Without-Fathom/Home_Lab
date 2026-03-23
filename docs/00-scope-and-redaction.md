# Scope & Redaction Policy

This repo documents **design intent and operational lessons**, not a live system.

## Explicitly in scope
- Network design rationale
- Service placement decisions
- Failure modes and mitigations
- UI / UX patterns for Home Assistant
- Sanitised configuration excerpts

## Explicitly out of scope
- Live IPs or hostnames
- WAN / ISP / NBN details
- Device inventories
- Credentials, tokens, certificates
- Copy‑pasteable firewall configs

## Placeholder conventions

| Item              | Placeholder                |
|-------------------|----------------------------|
| Subnet            | `10.10.10.0/24`            |
| Primary host IP   | `10.10.10.10`              |
| Hostname          | `pi-host.lab.local`        |
| Docker networks   | `docker_*`                 |

If a value could identify the environment, it is replaced.

## Screenshot hygiene
- Blur addresses, QR codes, tokens
- Diagrams preferred over screencaps
