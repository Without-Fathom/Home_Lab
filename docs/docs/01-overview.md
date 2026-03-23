## Background and motivation

This lab originally grew out of an exercise to repurpose an enterprise
router appliance (Meraki MX64) by replacing the vendor firmware with
OpenWrt.

The goal was not performance optimisation, but control and understanding:
owning the full routing and firewall stack, gaining an understanding of SQM config to mitigate HFC buffer-bloat, removing cloud dependencies,
and treating the network as something observable and explainable rather
than opaque.

The current layout reflects that origin: conservative firewalling,
explicit routing intent, and a preference for boring, debuggable systems.
