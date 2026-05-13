# CLAUDE.md - SunFounder Shared Documentation (French)

## Project Overview
This is a **shared documentation content repository** for SunFounder Raspberry Pi, Arduino, and ESP32 educational kits. It is a content-only repo (no build system) designed to be included as a submodule or content fragment by a parent Sphinx documentation project.

## Language Role
This `sf-shared-fr` repo is the **French translation**. It must stay in sync with the English source repo (`sf-shared-en`) in terms of file structure, anchors, and conditional tags. Content is in French; structural elements (anchors, tags, image paths) are identical to EN.

## Repository Structure
```
sf-shared/
  appendix/       # 7 files: Blynk, FileZilla, I2C/SPI config, SSH, VNC, remote desktop
  component/      # 54 files: Electronic component reference docs (prefixed cpn_)
  pi_start/       # 6 files: Raspberry Pi getting-started guides
  img/            # Images per subdirectory
```

## Key RST Conventions

### Conditional Tags (pi_start/ files only)
Used for multi-version content assembly. Must be at column 0 with no indentation:
- `install_os_trixie.rst`: `imager`, `install_os`, `storage`, `cutomization_os`, `enable_connection`, `write_os`
- `set_up_pi.rst`: `setup_pi`, `setup_pi_screen`, `setup_pi_headless`, `setup_pi_troubleshooting`, `setup_pi_remote_desktop`
- `run_installer_fusion_hat.rst`: `install_fusion_hat`, `configure_safe_shutdown`
- `need_components_fusion_hat.rst`: `need_components_fusion_hat`

All start tags MUST have matching end tags. Both MUST be at column 0. Keep in sync with EN repo.

### Anchors (Cross-References)
Format: `.. _anchor_name:` at column 0. Must exactly match EN version names.
- Component files: `.. _cpn_xxx:` (e.g., `.. _cpn_led:`, `.. _cpn_gpio_board:`)
- Some files have dual anchors (e.g., `.. _cpn_gpio_extension_board:` and `.. _cpn_gpio_board:`)
- pi_start anchors: `.. _install_os:`, `.. _imager_custom:`, `.. _install_all_modules_fusion_hat:`

### Community Note
French: "Bonjour et bienvenue dans la Communauté Facebook des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder !"
Files `cpn_ws2812_module.rst` and `cpn_stepper_motor.rst` intentionally omit this note (matching EN).

### Image Paths
Identical to EN (images are shared, not translated).

## Syncing with EN
1. File names, anchors, and conditional tags must match EN exactly
2. Technical terms kept in English (I2C, PWM, GPIO, etc.)
3. Community notes use the French standard text
4. Image paths/attributes must match EN

## File Counts: 67 total (7 + 54 + 6)
