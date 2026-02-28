# CS2 Autoexec Generator

## Overview

The **CS2 Autoexec Generator** is a fully client-side, browser-based tool that allows players to import, merge, edit, and export Counter-Strike 2 configuration files.

It supports modern CS2 `.vcfg` files as well as legacy `.cfg` files and generates a clean, well-structured `autoexec.cfg` without requiring any installation, backend services, or external dependencies.

All processing happens locally in the browser.

---

## Key Features

### Configuration Import
- Import multiple files at once
- Supported formats:
  - `.vcfg`
  - `.cfg`
  - `.txt`
- Drag and drop support
- File picker support

### Intelligent Parsing and Merging
- Automatic format detection
- Supported parsers:
  - KV3 (CS2 VCFG format)
  - KV1
  - Classic CFG syntax
  - Partial JSON support
- Known CVars are mapped to the visual editor
- Key bindings are extracted and displayed separately
- Unknown or additional settings are preserved and can be optionally included

### Visual Configuration Editor
The UI provides structured sections for common CS2 settings:
- Crosshair
- Mouse and sensitivity
- Viewmodel
- Network
- Audio
- HUD and radar
- Performance and miscellaneous settings

All values update in real time and are reflected in the generated output.

### Key Bind Management
- Displays all imported key bindings
- Automatically resolves duplicates
- Optional inclusion or exclusion in the final autoexec

### Custom Commands
- Add custom commands, aliases, or binds manually
- Content is appended cleanly to the generated configuration

### Preview and Export
- Live preview of the generated `autoexec.cfg`
- Download as `autoexec.cfg`
- Copy directly to clipboard

### Privacy and Security
- 100% client-side
- No backend
- No uploads
- No tracking
- Works offline after loading

---

## Supported File Locations

Typical Counter-Strike 2 configuration directories:

Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg
Steam\userdata<STEAM_ID>\730\local\cfg\


Common supported files include:
- `cs2_user_convars.vcfg`
- `user_keys.vcfg`
- `cs2_video.vcfg`
- `cs2_machine_specific.vcfg`
- Existing `autoexec.cfg`
- Any legacy `.cfg` file

---

## Usage

1. Clone the repository or download it as a ZIP
2. Open `index.html` (or `cs2-autoexec-generator.html`) in a browser
3. Import your CS2 configuration files
4. Adjust settings using the visual editor
5. Review the generated configuration in the preview
6. Download or copy the `autoexec.cfg`
7. Place the file in your CS2 `cfg` directory

No additional setup is required.

---

## Technical Details

### Tech Stack
- HTML5
- CSS3
- Vanilla JavaScript

No frameworks or libraries are used.

### Parsing Capabilities
- Nested KV3 parsing with fallback handling
- KV1 parsing for older formats
- Line-based CFG parsing
- JSON flattening for compatibility
- Automatic classification of:
  - Known CVars
  - Key bindings
  - Additional settings

### Output Structure
The generated `autoexec.cfg` is:
- Cleanly formatted
- Sectioned with comments
- Deterministic and reproducible
- Safe to edit manually after export

---

## Hosting with GitHub Pages

This project can be hosted using GitHub Pages.

Steps:
1. Rename the HTML file to `index.html` (recommended)
2. Push to the `main` branch
3. Enable GitHub Pages (Deploy from branch, root folder)


---

## License

This project is licensed under the MIT License.  
See the `LICENSE` file for details.

---

## Contributing

Contributions are welcome.

You may contribute by:
- Reporting bugs
- Suggesting features
- Improving parsing logic
- Improving UI or UX
- Submitting pull requests

Please keep contributions focused and well-documented.

---

## Project Goals

- Provide a reliable CS2 autoexec generator
- Maintain full transparency and offline capability
- Avoid unnecessary complexity
- Preserve user control over configuration files
