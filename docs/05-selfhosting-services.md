# Self‑Hosting Services

All services run on a single Raspberry Pi 4B using Docker.
There are no high‑availability assumptions.

This is deliberate.

## Host

- Raspberry Pi 4B
- USB‑attached storage for media and backups
- Treated as disposable hardware with monitored failure modes

## Services

### Home Assistant
- Containerised
- Host networking where required
- Uses documented, supported integration paths

### Pi‑hole
- Central DNS for the lab
- Exposed to Home Assistant for visibility, not control theatre

### Audiobookshelf
- Media served from USB storage
- Non‑critical, easy to rebuild

### Folding@home
- CPU‑limited so it can’t starve Home Assistant
- Considered expendable under load

## Trade‑offs

- Single node keeps recovery simple
- USB storage is cheap and imperfect, so it’s monitored and backed up on separate hardware & cloud
