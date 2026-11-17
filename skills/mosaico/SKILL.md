---
name: mosaico
description: "Work with ESP-Mosaico devices: connect to the local web interface, troubleshoot Wi-Fi or USB access, install and run IDEAs, develop and test .irisfw applications with Vibe Mode, or update and recover firmware. Use for ESP-Mosaico hardware and mosaico.ai workflows, not unrelated products named Mosaic."
---

# ESP-Mosaico

Use the official Mosaico guide and repositories as the source of truth. Verify current instructions online when versions, ports, commands, or firmware behavior could have changed.

## Route the request

- For LAN, Wi-Fi, web control, or USB detection problems, read [references/connectivity.md](references/connectivity.md).
- For running or installing an existing IDEA, read [references/install-ideas.md](references/install-ideas.md).
- For creating, building, simulating, installing, or debugging an IDEA, read [references/development.md](references/development.md).
- For firmware update, recovery, BOOT mode, or factory firmware work, read [references/firmware.md](references/firmware.md).

Read only the references needed for the current request.

## Shared operating rules

- Confirm the device state that matters: powered on, current mode or running IDEA, Wi-Fi status, and whether a data-capable USB cable is connected.
- Treat the device IP and USB serial port as discovered values. Do not assume a previous IP or port remains valid.
- Prefer the project-pinned `mosaico.py` and ESP-Iris/Vibe Mode workflow for application installation and maintenance.
- Preserve Vibe Mode unless the user explicitly requests low-level firmware replacement and understands the recovery path. Do not substitute `esptool` or a generic `idf.py flash` for an ESP-Iris application install.
- Use read-only checks first. Before changing configuration, installing firmware, restarting the device, formatting storage, or uploading/deleting files, state the impact and obtain any required approval.
- Keep the Mosaico control plane on a trusted LAN. Never expose it to the public internet. Do not print, store, or transmit API keys found in device configuration.
- When reporting a result, distinguish what was verified on the physical device from what passed only in the simulator or build tooling.

## Authoritative sources

- Quick-start guide: https://mosaico.ai/en/guide
- Install/run guide: https://mosaico.ai/en/guide/install
- Development guide: https://mosaico.ai/en/guide/develop
- FAQ: https://mosaico.ai/en/faq
- Firmware updater: https://mosaico.ai/en/firmware
- Vibe development repository: https://github.com/esp-mosaico/esp-mosaico-vibe
- Factory firmware: https://github.com/esp-mosaico/esp-mosaico-claw
