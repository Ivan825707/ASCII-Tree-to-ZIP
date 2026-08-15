
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