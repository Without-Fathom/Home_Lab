# Home Assistant UI

The Home Assistant UI is set up to be usable at a glance and boring to maintain
(in a good way).

It runs a Mushroom dashboard via HACS. No YAML gymnastics, no novelty layouts.

The Mushroom dashboard is displayed on two iPad Air 2 running HA Dashboard in Kiosk Mode.

## General approach

- Fewer entities, more summaries
- Surfaces “is something broken?” quickly
- Designed to work on a wall-mounted display (i.e. repurposed iPads) without constant tweaking

## Layout

Top section:
- Status / summary chips (network, DNS, basic system load)

Middle:
- Room-level controls
- Broad actions instead of per-device micromanagement

Bottom:
- Infrastructure health
- Pi-hole status, system load, container health

This avoids the classic **huge wall‑of‑toggles failure mode** and keeps the UI readable
without scrolling through dozens of entities.

## Notes

- Supported integrations are preferred over clever hacks
- If something requires constant babysitting, it doesn’t belong on the main dashboard
