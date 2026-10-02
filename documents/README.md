# Documents and PDFs

[← Back to all awesomes](../README.md)

## Contents

1. [Accessible PDFs](#accessible-pdfs)
2. [Viewing and Programming PDFs](#viewing-and-programming-pdfs)
3. [Typesetting](#typesetting)
4. [Word Processing](#word-processing)
5. [Presentations](#presentations)

## Accessible PDFs

These resources help with producing PDFs in modern, accessible formats, including features like embedded files that many PDF readers don't support.

### Modern Standards

The ISO standards from 2020 on are worth targeting, especially for documents you're archiving, like a dissertation. Many workflows and viewers still don't follow them. Older standards fall short most on making math, figures, and tables accessible to screen readers.

1. **PDF 2.0** ([ISO 32000-2](https://www.pdfa.org/resource/iso-32000-2/))
2. **PDF/UA-2** for accessibility ([ISO 14289-2](https://www.pdfa.org/resource/iso-14289-pdfua/))
3. **PDF/A-4** (or **A-4f** for embedded files) for archiving ([ISO 19005-4](https://www.pdfa.org/resource/iso-19005-pdfa/))

### Tools

- [veraPDF](https://verapdf.org) is an open-source validator for PDF/A and PDF/UA. It runs on Windows, macOS, and Linux, from the command line or a GUI.
- [texlive.net tag viewer](https://texlive.net/showtags) is a very useful checker that shows the accessibility tag structure of a PDF.

### LaTeX

- [LaTeX Tagging Project usage instructions](https://latex3.github.io/tagging-project/documentation/usage-instructions) cover the document metadata setup you need for tagged PDFs.
- [word-and-local-zotero-to-latex](https://github.com/tctco/word-and-local-zotero-to-latex) converts Word documents to LaTeX and keeps the structure, [Zotero](https://www.zotero.org) citations, and figures.
- **Tip: Alt text for SVG figures.** One way to tag an SVG (instead of a PNG or PDF graphic) with alt text using the [svg](https://ctan.org/pkg/svg) package:

  ```latex
  \begin{figure}
      {
        \setkeys{Gin}{alt={The invisible alt text for the image goes here}}
        \includesvg[]{some/path/to/svg/image}
      }
      \caption{The visible caption for the image goes here}
      \label{cross-reference-label-goes-here}
  \end{figure}
  ```

## Viewing and Programming PDFs

- [Firefox](https://www.mozilla.org/firefox/) is the preferred way to view modern PDFs. Its built-in viewer handles features that many readers don't, such as embedded files.
- [PDF.js](https://mozilla.github.io/pdf.js/) ([GitHub](https://github.com/mozilla/pdf.js)) is the preferred way to work with PDFs in browser code. It's the engine behind Firefox's PDF viewer.

## Typesetting

- [Typst](https://typst.app) ([GitHub](https://github.com/typst/typst)) is a modern typesetting system that's great for many documents.
  - It's also really good for making quick SVGs of code (Bash, Python, and so on) with `typst compile --format svg`.
- [Overleaf](https://www.overleaf.com) is a great collaborative LaTeX editor that runs in the browser.

## Word Processing

- [Microsoft Word](https://www.microsoft.com/microsoft-365/word) is an important research tool. See also [Research](../research/README.md).

## Presentations

- [Microsoft PowerPoint](https://www.microsoft.com/microsoft-365/powerpoint) is not bad for presentations.
- [Typst](https://typst.app) also works for slides, using packages from [Typst Universe](https://typst.app/universe).
