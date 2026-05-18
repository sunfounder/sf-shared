# CLAUDE.md - SunFounder Shared Documentation (English)

## Project Overview
This is a **shared documentation content repository** for SunFounder Raspberry Pi, Arduino, and ESP32 educational kits. It is a content-only repo (no build system) designed to be included as a submodule or content fragment by a parent Sphinx documentation project.

## Language Role
This `sf-shared-en` repo is the **English source / reference version**. All other language repos (`sf-shared-fr`, `sf-shared-de`, `sf-shared-ja`, `sf-shared-es`, `sf-shared-it`, `sf-shared-cn`) should be kept in sync with this repo in terms of file structure, anchors, and conditional tags.

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

All start tags MUST have matching end tags. Both MUST be at column 0.

### Anchors (Cross-References)
Format: `.. _anchor_name:` at column 0. Used for `:ref:\`anchor_name\`` cross-references.
- Component files: `.. _cpn_xxx:` (e.g., `.. _cpn_led:`, `.. _cpn_gpio_board:`)
- Some files have dual anchors (e.g., `.. _cpn_gpio_extension_board:` and `.. _cpn_gpio_board:`)
- pi_start anchors: `.. _install_os:`, `.. _imager_custom:`, `.. _install_all_modules_fusion_hat:`

### Title Underlines

RST titles use `====` (main title) or `----` (subsection) underlines. The underline **must be longer than the title text** — not equal, not shorter. When translating titles, always check and extend the underline accordingly.

- Use `====` for document-level titles, `----` for subsections.
- After translating a title, count the characters and ensure the underline is at least 2 characters longer.
- Watch for edge cases: duplicate underline lines (two consecutive `====` lines) should be removed.

### Community Note
Most files start with a `.. note::` block. EN files `cpn_ws2812_module.rst` and `cpn_stepper_motor.rst` intentionally omit this.

### Image Paths
Use `/_shared/` prefix for build-time resolution. Images are shared across languages.

All language repos must have **identical image files** to the English reference. The English `appendix/img/` (30 files) and `component/img/` (187 files) are the canonical set. When adding images to English, copy them to every other language repo as well.

### Substitution References
`|link_sf_facebook|`, `|shared_link_rpi_imager|`, `|shared_link_fusion_hat|`, `|shared_link_rpi_connect|`, `|shared_link_filezilla|`, `|shared_link_putty|`, `|link_fusion_hat|`

## Syncing Other Language Repos
1. Same file names in all repos (67 each)
2. Same `.. _anchor:` names
3. Same `.. start_xxx` / `.. end_xxx` tags
4. Image paths in RST files identical (images shared, not translated)
5. Image files in `appendix/img/` and `component/img/` must be identical to English (copy new images to every language)
6. Title underlines must be longer than the title — check after translating
7. Community notes translated

## File Counts: 67 total (appendix/7 + component/54 + pi_start/6)
