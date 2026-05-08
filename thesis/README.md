# Thesis template

This folder contains the thesis template organized in a modular structure:

- `Thesis.tex`: main entry point for the thesis version.
- `FrontMatter/`: abstract, dedication, acknowledgements, supervisor opinion, and contents.
- `MainMatter/`: introduction, background, proposal, and implementation chapters.
- `BackMatter/`: conclusions, recommendations, and bibliography.
- `Graphics/`: images and other visual assets.

The idea is to keep the folder structure clean and reusable while preserving the document identity through the title page, logos, and document settings.

### File roles

- `Thesis.tex`: main entry point for the thesis version.
- `thesis.cls`: document class that defines the title page and thesis environments.
- `cover-layout.tex`: shared cover design used by the class and the root report cover.
- `\maketitle`: builds the cover page from the metadata set in `Thesis.tex`.
- `latexmkrc`: tells `latexmk` which file to compile.
- `make.sh` and `make.bat`: build the thesis and regenerate the logo asset.
- `make_logo.sh` and `make_logo.bat`: regenerate the logo PDF from the SVG source.
- `Bibliography.bib`: bibliography entries used by the thesis.
- `babplain.bst`: legacy bibliography style kept with the template.
- `FrontMatter/`: abstract, dedication, acknowledgements, supervisor opinion, and contents.
- `MainMatter/`: introduction, background, proposal, and implementation chapters.
- `BackMatter/`: conclusions, recommendations, and bibliography.
- `Graphics/`: images, logos, and other visual assets.
