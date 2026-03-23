# Network Topology (Abstracted)

This lab uses a deliberately simple topology. IPv6 & VLANS are intentionally excluded for this lab, but will be deployed and documented in future.

The goal is not maximum segmentation, but **clear intent boundaries**.

## Logical segments (example)

- Infrastructure / services
  - `10.10.10.0/24`
  - Hosts core services only

Other segments (e.g. clients, guest, IoT) are described conceptually,
but not enumerated or diagrammed here. Over-documenting endpoints adds risk.
