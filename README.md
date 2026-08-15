# ASCII Tree to ZIP Generator

Convert any ASCII directory tree (with `├──`, `└──`, and `│` symbols) into a downloadable ZIP archive containing the exact folder and file structure.

![Screenshot](screenshot.png) *(You can add a screenshot later)*

**Live demo:** [https://ivan825707.github.io/ASCII-Tree-to-ZIP/](https://ivan825707.github.io/ASCII-Tree-to-ZIP/)

## Features

- 🧩 **Parse ASCII trees** – copy a tree from a chat, documentation, or file listing.
- 📦 **Generate ZIP** – get a ready‑to‑use archive with all folders and empty files.
- 🌗 **Dark / Light theme** – switch themes; your preference is saved in the browser.
- 🌍 **5 languages** – Ukrainian, English, German, Spanish, and French (UI fully translated).
- 💾 **Local storage** – remembers your language and theme choices.
- 🚀 **No server needed** – works completely in your browser.

## How to Use

1. Open the `index.html` file in any modern browser, or visit the [live demo](https://ivan825707.github.io/ASCII-Tree-to-ZIP/).
2. Paste your ASCII tree into the text area.  
   (You can also click **“Insert example”** to load a sample tree.)
3. Optionally switch the theme (☀️/🌙) or change the language from the dropdown.
4. Click **“Generate ZIP”**.
5. A ZIP archive named `your-project-structure.zip` will be downloaded automatically.

## Example Tree
demo/
├── backend/
│ ├── server.py
│ ├── routes/
│ │ ├── api.py
│ │ └── auth.py
│ └── models/
│ └── user.py
├── frontend/
│ ├── app.js
│ └── assets/
│ ├── logo.png
│ └── style.css
└── docker-compose.yml

When you generate the ZIP, the archive will contain:

- All folders (even empty ones) – each folder includes a `.keep` file to preserve it in the archive.
- All files – empty, but ready to be filled.

## How It Works

1. The parser reads each line and detects the indentation level using `│` symbols and spaces.
2. It builds a full path for every entry, respecting parent‑child relationships.
3. Folders are identified by a trailing `/` in the tree.
4. The script then creates a ZIP archive using [JSZip](https://stuk.github.io/jszip/) and triggers a download with [FileSaver.js](https://github.com/eligrey/FileSaver.js).

## Technologies

- **HTML5 / CSS3** (with CSS custom properties for theming)
- **Vanilla JavaScript** (no frameworks)
- **JSZip** – for generating ZIP files
- **FileSaver.js** – for saving files client‑side

All dependencies are loaded from CDN; no installation is required.

## License

This project is open‑source and available under the **MIT License**.  
Feel free to use, modify, and distribute it as you like.

---

**Enjoy building your project structures!**  
If you find this tool useful, give it a ⭐ on GitHub.