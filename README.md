
### CV with Asciidoctor (PDF)

Generate a clean, maintainable CV from an `*.adoc` file, then export it to **PDF** using **Asciidoctor**.

- Official website: [Asciidoctor](https://asciidoctor.org/)
- Based on (fork): [poznachowski/cv](https://github.com/poznachowski/cv)

#### Features

- CV written in **Asciidoc** (plain text, easy to version with Git)
- **PDF** export via `asciidoctor-pdf`
- Customizable theme and fonts (`themes/`, `fonts/`)

### Requirements

#### Linux

```bash
sudo apt update
sudo apt install ruby-asciidoctor-pdf
```

#### macOS

```bash
brew install asciidoctor
```

> Note: To generate a PDF you need `asciidoctor-pdf`.
> If `asciidoctor-pdf` is not available after installation, you can install it via RubyGems:
```bash
gem install asciidoctor-pdf
```

### Usage

#### Generate the PDF

From the repository root:

```bash
asciidoctor-pdf \
  -a pdf-theme=cv \
  -a pdf-themesdir=themes \
  -a pdf-fontsdir=fonts \
  jpo.adoc
```

The output file is usually `jpo.pdf` (depending on the input `.adoc` filename).

#### Customize for your own CV

- Edit `jpo.adoc` (or rename it, e.g. `cv.adoc`)
- Adjust if needed:
  - the theme in `themes/`
  - the fonts in `fonts/`
  - the command (input filename, `-a` options)

### Project structure (example)

- `jpo.adoc`: CV content
- `themes/`: Asciidoctor PDF themes (e.g. `cv.yml`)
- `fonts/`: fonts used by the theme

### Copyright / Credits

This project is forked from: [poznachowski/cv](https://github.com/poznachowski/cv).  
Please refer to the original repository for licensing details, and keep the required attributions if you redistribute this project.
