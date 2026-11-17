# Connectivity and local control

Use this reference for LAN access, Wi-Fi setup, USB detection, web-control access, or an apparently unreachable ESP-Mosaico.

## Web control page

1. Confirm that ESP-Mosaico is powered on and running the firmware or IDEA that provides the control page, such as Mosaico-Claw.
2. If it is not on Wi-Fi, connect the computer or phone to the device hotspot and open `http://192.168.4.1`.
3. If it is already on Wi-Fi, put the computer or phone on the same local network and open `http://<device-ip>`.
4. On the device, find the current address under `Settings > Network`, then open `Settings > AI Model`. The displayed QR code can also encode the control-page address.

A device visible in ARP but refusing TCP port 80 is reachable at layer 2 but is not currently serving the expected web control page. Check the running IDEA/mode and the IP shown on the device before scanning more ports. A timeout instead suggests routing, client isolation, firewalling, power, or a stale address.

Use concise, read-only diagnostics such as ARP inspection, a TCP connect to the documented endpoint, and an HTTP HEAD/GET request. Do not perform a broad port scan unless the user explicitly asks and owns or administers the target.

## USB

- Use a data-capable USB-C cable; charge-only cables do not expose the device.
- Both USB-C-to-C and USB-A-to-C data cables are supported.
- If no serial/device connection appears, reconnect the cable and restart ESP-Mosaico.
- Development should normally start with the device in Vibe Mode and connected by USB.
- If detection still fails, follow the official recovery/update instructions rather than guessing flash commands.

## Security

The device's configuration and agent services may be intended for a trusted local network. Avoid guest networks and AP/client isolation when local access is required. Do not expose device HTTP or MCP services through router port forwarding, tunnels, or public proxies. Redact keys and credentials from logs and screenshots.
