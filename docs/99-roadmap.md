# Roadmap / Future Work

- Introduce VLAN separation for IoT devices
  - Isolate untrusted devices from the main network
  - Allow access to required services only (e.g. Home Assistant, DNS)
  - No blanket east‑west access

- Improve backup automation for USB‑attached storage

- Revisit Bluetooth architecture if direct BLE becomes unreliable
  - BLE proxies preferred over host‑level hacks if complexity increases

- Add better service health checks rather than more services

## Wireless infrastructure (future work)

- Convert existing Cisco APs from CAPWAP to Mobility Express
- Remove the need for an external wireless controller
- Keep wireless management local and self‑contained

This is primarily about reducing complexity and external dependencies,
not expanding feature set. Conversion details and firmware specifics
are intentionally out of scope for this repo.
