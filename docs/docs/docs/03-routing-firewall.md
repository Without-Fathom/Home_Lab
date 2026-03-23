# Routing & Firewalling

Firewalling is handled by OpenWrt (fw4 / nftables) using a simple
zone‑based model.

This is intentionally conservative. The goal is predictable behaviour,
not clever rule sets.

## High‑level posture

- Trusted LAN, untrusted WAN
- Default deny on the WAN
- Explicit forwarding only
- No inbound WAN exposure

There are currently no additional internal zones (e.g. IoT or guest).
Those are future work.

---

## Zones (sanitised)

| Zone | Input  | Output | Forward | Notes |
|-----:|--------|--------|---------|-------|
| lan  | ACCEPT | ACCEPT | ACCEPT  | Trusted internal network |
| wan  | REJECT | ACCEPT | REJECT  | Masqueraded, MTU fix enabled |

Interface bindings and physical details are intentionally omitted.

---

## Forwarding

Allowed inter‑zone forwarding:

- `lan → wan`

No reverse forwarding is permitted.

---

## Rule intent

Most firewall rules are stock OpenWrt defaults for WAN hygiene
(DHCP renew, ICMP, IPv6 control traffic, IPSec passthrough).

Additional intent‑based rules:

- Rate‑limit or restrict SSH access from the LAN to the router itself

Rule mechanics (ports, limits, protocols) are not published.
Only intent is documented.

---

## Remote access (Cloudflare Tunnel)

Remote access is provided via a Cloudflare Tunnel.

The tunnel is outbound‑only from the LAN and is used to avoid exposing
any services directly to the WAN. No inbound ports are forwarded to
internal hosts.

Only authenticated access is permitted. Public endpoints, hostnames,
and access policy details are intentionally not documented here.

From a firewall perspective, this is treated as regular egress traffic
from the LAN to the WAN.


---

## Notes

- No port forwards or exposed services (handled via tunnel)
- No attempt is made to “micro‑segment” a flat LAN
- I spend a **lot** of time troubleshooting complex rules in our PAN, "simpler is betterer" at home
