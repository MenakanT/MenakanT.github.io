# Portfolio site and resume

This repo is Menakan's portfolio site (GitHub Pages, served from `main`) and the source of their resume.

## Site

- Everything is in `index.html`: one page with hash routing (`#home`, `#experience`, `#projects`, `#hobbies`, `#contact`).
- Images and videos live in `images/`. Projects without a photo use the inline SVG placeholders (`data-art="..."`).
- Keep the site and the resume saying the same things (project names, roles, numbers).

## Resume

- Source: `resume/MenakanT_resume.tex`. Built PDF: `MenakanT_resume.pdf` at the repo root (the site links to it).
- Edit the `.tex`, then rebuild and copy the PDF to the root:

  ```bash
  cd resume && pdflatex -interaction=nonstopmode -output-directory=/tmp/resume-build MenakanT_resume.tex \
    && cp /tmp/resume-build/MenakanT_resume.pdf ../MenakanT_resume.pdf
  ```

  Needs `texlive-latex-extra`, `texlive-fonts-recommended` and `cm-super` (apt).
- Rules:
  - Never put a phone number in the resume. This repo is public.
  - Keep it to one page. Check the page count after every rebuild. The Technical Skills block can't split across pages, so a small overflow pushes the whole block to page 2.
  - The email link and the displayed email are both `menakan.thamil@gmail.com`.
