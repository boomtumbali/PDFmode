# PDFmode

**Notes, slides and handouts. One PDF, made for reading.**

PDFmode turns Markdown, Word, PowerPoint, PDF and plain-text files into one clean PDF. It can keep each file's own formatting and pages, merge several files in the order you choose, or flow everything into one continuous page you can scroll without a single page break. It's built for students reading reviewers, lecture slides and handouts on a phone, tablet or laptop.

🔗 **Live:** [pdfmode.vercel.app](https://pdfmode.vercel.app)
👤 **By:** [@boomtumbali](https://www.linkedin.com/in/boomtumbali)

![PDFmode](og-image.png)

---

## What it does

- **Opens almost any class file:** Markdown (`.md`), Word (`.docx`), PowerPoint (`.pptx`), PDF, plain text (`.txt`) and web pages (`.html`). It detects the format from the file itself, so there's nothing to choose.
- **Keeps the original formatting** of Word and PowerPoint files: fonts, sizes, colors, alignment, spacing, lists, tables, pictures, headers, footers and page numbers. Slides keep their backgrounds, shapes and layout.
- **Or switches to Reading style:** the text is reflowed in a reading typeface at your chosen size and page color, and speaker notes from slides are included.
- **Merges files in order.** Open several at once and they're combined in the order shown. Drag, or use the arrows, to reorder.
- **Three layouts:**
  - **Auto** (default): Word, PowerPoint and PDF keep their pages; Markdown and text become one continuous page.
  - **Continuous:** everything becomes one long page.
  - **Pages:** regular pages for everything.
- **Fits the device.** Auto width makes phone-width pages on phones, tablet width on tablets, and 8.5 in on computers. You can also pick a fixed size:

  | Size | Dimensions |
  | --- | --- |
  | Letter | 8.5 × 11 in |
  | Legal | 8.5 × 13 in (Philippine long bond) |
  | A4 | 8.27 × 11.69 in |
  | Tablet | 6 in wide |
  | Phone | 4.5 in wide |

- **Reading typefaces:** Slab (Arvo), Serif (Literata) and Sans (Atkinson Hyperlegible Next), plus **Original** for Office files.
- **Page colors and app appearance:**
  - **Page color:** Light, Sepia or Dark, applied to the PDF itself.
  - **Appearance:** System, Light or Dark (the default), for the app around the document.
- **Searchable output.** Text in the PDF is real, selectable text, and every file and heading becomes a bookmark.
- **Exact preview.** For Word, PowerPoint and merged files, the preview *is* the exported PDF.

## Privacy

Everything runs in your browser. Your files are **never uploaded** to a server. The app only downloads its own code libraries (from the jsDelivr CDN) when it loads.

## How to use

1. Go to [pdfmode.vercel.app](https://pdfmode.vercel.app).
2. Click **Choose files**, drop files anywhere on the page, or **Paste text**.
3. Adjust the settings if you like: Formatting, Layout, Width, Typeface, Text size, Page color.
4. Click **Export PDF**.

**Keyboard shortcuts:**
- `⌘O` / `Ctrl+O`: open files
- `⌘E` / `Ctrl+E` (or `⌘S` / `Ctrl+S`): export

## Good to know

- **Office fonts are replaced by free fonts with the same letter widths,** so lines break where they do in Office. For example, Calibri uses Carlito, Cambria uses Caladea, and Arial and Times New Roman use the Liberation fonts. Microsoft's own fonts are licensed and can't be bundled.
- **Some layouts are simplified:**
  - Word: columns, footnotes, SmartArt, and text wrapped around floating pictures.
  - PowerPoint: charts, complex shapes, gradients, shadows and animations.
- **Older `.doc` and `.ppt` files aren't supported.** Save them as `.docx` / `.pptx` first.
- **Very long continuous pages** open fine in Chrome, Edge, Safari and most phone PDF viewers. Adobe Reader can't open single pages longer than 200 in; use **Pages** layout for Adobe Reader.
- **Maximum file size** is 40 MB per file.

## Run or host it yourself

PDFmode is a single self-contained `index.html` with no build step.

**Run locally:** open `index.html` in a browser.

**Host on Vercel:**
1. Put `index.html`, `og-image.png` and this `README.md` in a GitHub repository.
2. On [vercel.com](https://vercel.com), choose **Add New → Project**, import the repository, leave the **Framework Preset** as **Other**, and click **Deploy**.
3. Every commit to the repository redeploys the site automatically.

> If your site address isn't `pdfmode.vercel.app`, update the `og:url`, `og:image`, `twitter:image` and `canonical` tags in `index.html` so link previews work.

### Repository contents

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: interface, conversion engine, and embedded fonts |
| `og-image.png` | Link-preview image for Messenger, Facebook, X and others |
| `README.md` | This file |

## Built with

| Purpose | Library |
| --- | --- |
| PDF layout | [pdfmake](https://github.com/bpampuch/pdfmake) |
| Merging, stitching and bookmarks | [pdf-lib](https://github.com/Hopding/pdf-lib) |
| Markdown | [marked](https://github.com/markedjs/marked) |
| Word → HTML (Reading style) | [mammoth.js](https://github.com/mwilliamson/mammoth.js) |
| HTML → Markdown | [Turndown](https://github.com/mixmark-io/turndown) + GFM plugin |
| Reading Office files | [JSZip](https://github.com/Stuk/jszip) |
| Exact PDF preview | [PDF.js](https://github.com/mozilla/pdf.js) |

**Fonts:** Arvo, Literata, Atkinson Hyperlegible Next, Inter (interface), JetBrains Mono, Carlito, Caladea, Liberation Sans and Serif, and DejaVu Sans (symbols). All are free, open-licensed fonts.

---

Made by [@boomtumbali](https://www.linkedin.com/in/boomtumbali).
