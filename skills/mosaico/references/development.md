# Develop an IDEA

Use this reference for creating, simulating, building, installing, testing, or publishing an ESP-Mosaico IDEA.

## Starting point

- Put ESP-Mosaico in Vibe Mode and connect it with a data-capable USB cable.
- Use the official `esp-mosaico-vibe` repository and its pinned dependencies: https://github.com/esp-mosaico/esp-mosaico-vibe
- Work in an application workspace and follow that revision's README. Prefer its root `mosaico.py` entry point and project configuration over globally installed or guessed commands.

## Development loop

1. Clarify controls, device modules, start/pause/error states, and physical-device acceptance criteria.
2. Implement and build the IDEA.
3. Preview and refine the interface in the PC simulator.
4. Build the standard `.irisfw` package and run the repository's self-checks.
5. Install through the ESP-Iris/Vibe Mode tooling.
6. Validate on the physical device, including display, touch/buttons, sensors, audio/camera, and runtime behavior relevant to the project.
7. Report the `.irisfw` path, checks passed, installation result, and any behavior that still needs physical verification.

Use the repository's debugging tools when available to capture the device screen and runtime data and to perform interactive testing. Do not describe a simulator-only result as hardware validation.

## Installation invariant

An IDEA installation is not the same as a raw ESP-IDF flash. Preserve the retained Vibe Mode/Recovery layout and use the documented Iris installer. A generic `esptool` or `idf.py flash` can overwrite partitions needed by Vibe Mode.

## Publishing

Publication is optional and requires explicit user intent. Build and validate the package first. On mosaico.ai, create a draft with the IDEA name, cover, description, version, and `.irisfw`; let the user handle sign-in or authorization challenges, and do not submit for public review without explicit confirmation. Return the draft link, version, and checksum when available.
