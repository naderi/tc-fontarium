# Fontarium

**English** | [Deutsch](README.de.md)

A font viewer (Lister plugin) for [Total Commander](https://www.ghisler.com), 32 and 64 bit.
Press F3 on a font file (TTF, OTF, TTC, WOFF, WOFF2, and Windows bitmap fonts: FON) and see it right there – drawn with DirectWrite, so Persian, Arabic and other scripts are rendered correctly. Variable fonts get sliders for their axes, OpenType features can be switched on and off, and a glyph inspector shows every character. Native, no runtime, nothing to install besides the plugin.

Fontarium was inspired by the FontMaster plugin. I wrote it because I wanted full support for right-to-left languages such as Persian and Arabic.

![Fontarium showing the variable font Bahnschrift with its axes](docs/screenshot.png)

![Color emoji in the Characters tab](docs/screenshot-emoji.png)

## Features

- **Preview:** uppercase, lowercase, digits & symbols, a sample sentence, your own text and a size ladder; one button per face of the font. A slider sets the preview size, and an *Install* button installs the font for the current user or for all users
- **Variable fonts:** a slider for every axis (weight, width, …) with *Reset*
- **OpenType features:** only the features the font actually contains are listed; a click cycles *default → on → off*
- **Custom text:** several lines are possible, and every line is set on its own with its own direction and language – so Persian and German can be mixed. Direction and language can also be fixed in the settings
- **Characters:** an *All* button (selected by default) shows every character of the font in one grid; below it all Unicode blocks of the font, coverage (e.g. *120 of 256 characters*), *Show missing*, and a glyph inspector that draws the outline with its on-curve and control points, the metric lines (ascender, cap height, x-height, baseline, descender) and the glyph numbers (glyph index, units per em, advance, bearings, bounding box, contours and nodes; a *Nodes* button shows or hides the nodes), plus the isolated / initial / medial / final forms. Color glyphs such as emoji are drawn in color. Double-click or Enter opens the detail view; right-click opens a menu to copy the character, code point, glyph name or HTML entity. The *Go to* box jumps straight to a character or code (`€`, `20AC` or `U+20AC`)
- **Coverage:** which writing systems the font can set (Latin, Cyrillic, Greek, Arabic, Persian, Hebrew, Thai, CJK, …) as bars with percentages, and the scripts it does not cover
- **Details:** names, legal information (copyright, designer, license, with links), technical data (format, file size, glyphs, faces in the file, variable axes, metrics) and the languages the font supports; click a value to copy it to the clipboard, right-click offers *Copy value* and *Copy name and value*
- **Installed:** all fonts installed on this PC, with preview on the right
- **Folder:** the fonts in the folder of the opened file, or in a folder you choose (optionally with subfolders)
- **Install, uninstall, activate, deactivate** fonts from the *Installed* and *Folder* tabs. *Install* offers *Install for current user* and *Install for all users* (Windows asks for administrator rights once, for all selected fonts). Web fonts (WOFF, WOFF2) cannot be installed; system fonts can only be removed with administrator rights
- **Bitmap fonts (.fon):** Windows raster fonts such as those in `C:\Windows\Fonts` are shown pixel by pixel, with all tabs; a file with several sizes gets one button per size. Vector `.fon` files are not supported; `.fon` files cannot be installed
- **Next / previous font:** Left / Right (or PgUp / PgDn at the end of the page) open the previous / next font file of the folder, like an image viewer
- Light and dark design (automatic like Windows, fixed, or like Total Commander) in the Windows 11 look; anti-aliasing ClearType, grayscale or off; color glyphs on or off; interface size from 100 % to 200 %
- English and German user interface (follows the Windows language, or choose it in the settings)

## Keys

| Key | Action |
|---|---|
| Ctrl+Tab | Next tab |
| Ctrl+PgUp / PgDn | Previous / next face |
| Ctrl + mouse wheel, Ctrl + + / − | Size |
| Arrow keys, PgUp / PgDn, Home / End | Scroll |
| Left / Right (not in *Characters*), PgUp / PgDn at the end of the page | Previous / next font file in the folder |

## Download and installation

1. Download **`Fontarium.zip`** from the [latest release](https://github.com/naderi/tc-fontarium/releases/latest).
2. Open the ZIP in Total Commander (Enter on the file) and confirm the question whether to install the plugin.

Settings are stored in `Fontarium.ini` next to the plugin (in `%APPDATA%\Fontarium` if that folder is read-only) and can be changed in the *Settings* tab. To open on another tab (e.g. *Characters*) instead of *Preview*, set `starttab=1` in the ini (0 Preview, 1 Characters, 2 Details, 3 Installed, 4 Folder, 5 Coverage). To hide the outline nodes in the glyph view, set `nodes=0` (default 1; the *Nodes* button in the glyph view switches it, too). To switch off the file switching with Left / Right, set `filenav=0` (default 1). Requires Windows 10 version 1803 or newer.

## License

Freeware – free to use, but **not for sale**. See [LICENSE](LICENSE). Fontarium contains [Brotli](https://github.com/google/brotli) and [woff2](https://github.com/google/woff2) by Google (MIT license) to read WOFF and WOFF2 fonts.

## Support

If Fontarium saves you time, you can support its development on Ko‑fi. ☕

<a href='https://ko-fi.com/N7N123QIX0' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

---

© 2026 [Ali Naderi](https://github.com/naderi) · [digitalent.dev](https://digitalent.dev/en/)
