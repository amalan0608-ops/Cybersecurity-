# SecureKit: Cyber Security Tools

A single-page website that lists 39 well-known cyber security tools, with category filters and two small utilities that run entirely in your browser.

## Features

- **Tool directory:** 39 tools across 9 categories (Network, Defense, Web, Forensics, Crypto, Malware, Cloud, Identity), with a short description and a link to each project.
- **Category filter:** show all tools or one category at a time.
- **Password strength check:** estimates strength from length and character variety. Nothing you type is sent anywhere.
- **SHA-256 hash generator:** hashes text so you can compare it with a published checksum (uses the browser's built-in Web Crypto API).
- **Light and dark themes:** follows your device setting.
- **Responsive and accessible:** works on phones and desktops, with keyboard focus styles and labelled inputs.
- **Security habits:** a short list of five practices that stop most attacks.

## Project structure

```
cybersecurity-tools.html   The whole site: HTML, CSS and JavaScript in one file
README.md                  This file
```

## How to run

1. Download `cybersecurity-tools.html`.
2. Open it in any modern browser (Chrome, Firefox, Safari, Edge).

No build step, server or dependencies are needed. An internet connection is used only to load the Google Font (Schibsted Grotesk); without it the page uses your system font.

The SHA-256 tool needs a secure context, so it works from `https://` pages and `file://` in most browsers. If it shows a message about HTTPS, serve the file over HTTPS or `localhost`.

## How to customize

**Add or edit a tool.** Open the file and find the `TOOLS` array in the `<script>` section. Each entry has four values:

```js
["Name", "Category", "Short description.", "https://example.com"]
```

A new category appears in the filter buttons automatically.

**Update the tool count.** The heading "Tool directory (39 tools)" is typed by hand. Change the number if you add or remove tools.

**Change colors.** Edit the CSS variables at the top of the `<style>` block (`--bg`, `--ink`, `--acc` and so on). Dark-mode values are in the two `prefers-color-scheme` and `data-theme="dark"` blocks.

## Responsible use

This is an educational directory. Scanning, testing and forensic tools should only be used on systems you own or have written permission to test. Tool descriptions are brief summaries; check each project's website for its current features and licence.

## Limitations

- The password checker is an estimate and does not check against breach lists or full dictionaries. Do not treat its score as a guarantee.
- Links point to official project sites at the time of writing and may change.
