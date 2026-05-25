# CLAUDE.md - SunFounder Shared Documentation (Japanese)

## Project Overview
This is a **shared documentation content repository** for SunFounder Raspberry Pi, Arduino, and ESP32 educational kits. Content-only repo, designed as Sphinx submodule.

## Language Role
This `sf-shared-ja` repo is the **Japanese translation**. Must stay in sync with `sf-shared-en` for file structure, anchors, and conditional tags. Content in Japanese; structural elements identical to EN.

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
- `cpn_gpio_board.rst`: anchors MUST be `.. _cpn_gpio_extension_board:` first, then `.. _cpn_gpio_board:`

### Community Note
Japanese: "こんにちは、SunFounderのRaspberry Pi & Arduino & ESP32愛好家コミュニティへようこそ！Facebook上でRaspberry Pi、Arduino、ESP32についてもっと深く掘り下げ、他の愛好家と交流しましょう。"
Files `cpn_ws2812_module.rst` and `cpn_stepper_motor.rst` omit the note (matching EN).

### Inline Markup Spacing (CJK)

When an RST inline markup **closing** delimiter is immediately followed by a non-ASCII character (CJK, fullwidth punctuation like `：` `（` `。）`, etc.), the RST parser may fail to recognize the delimiter end, causing "Inline strong start-string without end-string" warnings.

**Rule**: Insert `\ ` (escaped space) between the closing delimiter and the non-ASCII character.

| Markup | Wrong | Correct |
|---------|-------|---------|
| `**bold**` | `**特別割引**：` | `**特別割引**\ ：` |
| `*italic*` | `*斜体*（` | `*斜体*\ （` |
| `__bold__` | `__text__日本語` | `__text__\ 日本語` |
| `\|sub\|` | `\|link\|\ 。` | `\|link\|\ 。` |
| `` `code` `` | `` `cmd`： `` | `` `cmd`\ ： `` |
| `:ref:`...`` | `` :ref:`anchor`： `` | `` :ref:`anchor`\ ： `` |

**What NOT to do**:
- Do NOT add space/`\ ` before the **opening** delimiter
- Do NOT add space/`\ ` **inside** the markup content
- If the closing delimiter is already followed by an ASCII space/newline, no fix is needed

**Fix regex** (apply line-by-line, never across newlines — use `[^*\\r\\n]` not `[^*]`):
```
Find:    \\*\\*([^*\\r\\n]+?)\\*\\*([^\\x00-\\x7F\\s])
Replace: **$1**\\ $2
```
Similarly for `|text|`, `` `text` ``, ` ``text`` `, `__text__`, and single `*text*` (with negative lookbehind for `**`).

### Image Paths
Identical to EN (images are shared, not translated).

## File Counts: 67 total (7 + 54 + 6)
