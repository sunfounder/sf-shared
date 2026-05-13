# CLAUDE.md - SunFounder Shared Documentation (German)

## Project Overview
This is a **shared documentation content repository** for SunFounder Raspberry Pi, Arduino, and ESP32 educational kits. Content-only repo, designed as Sphinx submodule.

## Language Role
This `sf-shared-de` repo is the **German translation**. Must stay in sync with `sf-shared-en` for file structure, anchors, and conditional tags. Content in German; structural elements identical to EN.

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
Format: `.. _anchor_name:` at column 0. Must match EN exactly. No extras, no renames.

### Community Note
German: "Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von..."
Standard version uses "Gemeinschaft" and "erkunden und zu erschaffen". Files `cpn_ws2812_module.rst` and `cpn_stepper_motor.rst` omit the note (matching EN).

### Image Paths
Identical to EN (images are shared, not translated).

## File Counts: 67 total (7 + 54 + 6)
