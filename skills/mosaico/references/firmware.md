# Firmware update and recovery

Use this reference for Vibe Mode updates, factory firmware, BOOT download mode, or recovery.

## Before changing firmware

- Identify the hardware revision and current firmware/Vibe Mode version when possible.
- Back up important IDEAs and data. An update or storage format may erase them.
- Keep the device powered and connected with a data-capable USB cable.
- Use the current official firmware page and repository instructions; firmware procedures are version-sensitive.

## Official update flow

The official web updater at https://mosaico.ai/en/firmware currently instructs the user to power off the device, connect USB, hold BOOT, and briefly press POWER to enter ROM Download Mode. The screen remaining black in this mode is normal. Use the site's `Connect Device` flow and keep the cable connected until completion.

Changing firmware or formatting storage is destructive enough to require explicit confirmation immediately before execution.

## Factory firmware development

The factory firmware source is https://github.com/esp-mosaico/esp-mosaico-claw and uses ESP-IDF with ESP32-S31 support. Follow the selected revision's README, dependency, board-manager, partition, and submodule instructions exactly. Do not mix its low-level firmware flash procedure with the application-level `.irisfw` installation workflow.

If the goal is merely to build or install an IDEA, return to the Vibe repository workflow instead of rebuilding factory firmware.

## Recovery discipline

- Prefer official recovery tooling over full-chip erase.
- Do not erase the whole chip or replace retained Recovery/Vibe partitions unless the user explicitly requests that outcome and has a verified restore path.
- After recovery, verify the target version and actual behavior; factory firmware and ESP-Claw components can have independent version numbers.
