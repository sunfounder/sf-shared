# CLAUDE.md - SunFounder Shared Documentation (Italian)

## Project Overview
This is a **shared documentation content repository** for SunFounder Raspberry Pi, Arduino, and ESP32 educational kits. Content-only repo, designed as Sphinx submodule.

## Language Role
This `sf-shared-it` repo is the **Italian translation**. Must stay in sync with `sf-shared-en` for file structure, anchors, and conditional tags. Content in Italian; structural elements identical to EN.

## Repository Structure
```
sf-shared/
  appendix/       # 7 files
  component/      # 54 files (prefixed cpn_)
  pi_start/       # 6 files
```

## Key RST Conventions

### Conditional Tags (pi_start/ only, column 0, no indentation)
- `install_os_trixie.rst`: `imager`, `install_os`, `storage`, `cutomization_os`, `enable_connection`, `write_os`
- `set_up_pi.rst`: `setup_pi`, `setup_pi_screen`, `setup_pi_headless`, `setup_pi_troubleshooting`, `setup_pi_remote_desktop`
- `run_installer_fusion_hat.rst`: `install_fusion_hat`, `configure_safe_shutdown`
- `need_components_fusion_hat.rst`: `need_components_fusion_hat`

### Anchors
Format: `.. _anchor_name:` at column 0. Must match EN exactly.
- `cpn_gpio_board.rst`: MUST have both `.. _cpn_gpio_extension_board:` AND `.. _cpn_gpio_board:`

### Community Note
Italian: "Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati."
Files `cpn_ws2812_module.rst` and `cpn_stepper_motor.rst` omit the note (matching EN).

### Image Paths
Identical to EN (images are shared, not translated).

## File Counts: 67 total (7 + 54 + 6)
