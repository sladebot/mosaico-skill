# Mosaico skill

A reusable Codex skill for working with ESP-Mosaico devices and the [mosaico.ai](https://mosaico.ai/) ecosystem.

This is an independent community resource and is not affiliated with or endorsed by Espressif.

It helps an agent:

- connect to and troubleshoot an ESP-Mosaico over LAN, Wi-Fi, or USB;
- enter Vibe Mode and install or run IDEAs;
- build, simulate, package, install, and validate `.irisfw` applications;
- update or recover firmware while preserving the Vibe Mode/Recovery layout; and
- apply appropriate local-network and credential-safety precautions.

The skill routes detailed tasks to focused references instead of loading the entire guide for every request.

## Install with Codex

Ask Codex:

```text
$skill-installer Install the mosaico skill from https://github.com/sladebot/mosaico-skill
```

Or install it manually by copying `skills/mosaico` into your user skills directory:

```text
~/.codex/skills/mosaico
```

Restart Codex if the skill does not appear automatically, then invoke it with `$mosaico`.

## Mobile use

Codex Remote on a phone can use this skill when the connected host has it installed. The repository also contains a skills-only plugin manifest for submission to the universal plugin directory. Until that submission is approved and published, a GitHub repository by itself does not install the skill into ChatGPT mobile.

## Sources

The workflow is based on the official resources linked from the skill, including:

- [ESP-Mosaico quick-start guide](https://mosaico.ai/en/guide)
- [IDEA installation guide](https://mosaico.ai/en/guide/install)
- [IDEA development guide](https://mosaico.ai/en/guide/develop)
- [ESP-Mosaico FAQ](https://mosaico.ai/en/faq)
- [esp-mosaico-vibe](https://github.com/esp-mosaico/esp-mosaico-vibe)
- [esp-mosaico-claw](https://github.com/esp-mosaico/esp-mosaico-claw)

Verify version-sensitive firmware and tooling instructions against the current official documentation before acting.

## License

MIT
