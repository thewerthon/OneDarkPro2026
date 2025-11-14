## One Dark Pro 2026 - Dark theme for Visual Studio 2026

**One Dark Pro 2026** is an updated and corrected adaptation of the popular *One Dark Pro* theme, adjusted specifically for **Visual Studio 2026**.

This version preserves the original aesthetic, but includes:

* fixes for outdated or deprecated theme keys
* adjustments for the new VS2026 color engine
* slightly refined contrast and accent tones
* improved visibility across tool windows and editor areas
* compatibility fixes for the updated Visual Studio UI
* **a full VSIX build script for easy editing and rebuilding**

---

## Repository Contents

```
build_vsix.py        – Python script that builds a .vsix theme from the YAML config
OneDarkPro2026.yaml  – Theme configuration with updated color sections
OneDarkPro2026.png   – Theme icon image for extension tab/marketplace page
```

The repository **includes a standalone VS theme build script**, allowing you to:

* edit colors directly in YAML
* rebuild a complete VSIX with one command
* tweak, fork, or customize the theme quickly


---

## Building the VSIX

Requires **Python 3.8+** and the **PyYAML** library.

### 1. Install dependency:

```sh
pip install pyyaml
```

### 2. Build the theme:

```sh
python build_vsix.py -i OneDarkPro2026.yaml -o OneDarkPro2026
```

The script produces VS extension (theme):

```
OneDarkPro2026.vsix
```

---

## Theme Preview

![Preview](doc/screenshot-cs.png)
![Preview](doc/screenshot-cpp.png)

---

## Customizing the Theme

Edit everything inside:

```
OneDarkPro2026.yaml
```

Then rebuild:

```sh
python build_vsix.py -i OneDarkPro2026.yaml -o OneDarkPro2026
```

You can modify:

* individual colors
* entire sections
* GUIDs
* metadata (name, author, version)
* tags and description

The Python builder handles the packaging.

---

## Credits

* This theme is based on the **One Dark Pro** theme by Adrian Wilczyński:
  [https://marketplace.visualstudio.com/items?itemName=adrianwilczynski.one-dark-pro](https://marketplace.visualstudio.com/items?itemName=adrianwilczynski.one-dark-pro)
* This version updates, tweaks, and stabilizes it for Visual Studio 2026.
