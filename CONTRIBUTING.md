# Contributing

Thanks for helping improve the NTUST thesis template! Contributions from NTUST
students and anyone else are welcome.

## Ways to help
- Report a bug or a formatting mismatch with the official NTUST spec (open an issue).
- Add department variants, more example elements, or documentation.
- Improve portability (fonts, Overleaf, CI).

## Before you open a pull request
1. **Build it.** From the repo root: `latexmk -xelatex my_ntust_thesis.tex`. It must
   finish with 0 errors. CI runs the same build on every PR.
2. **No personal data.** Never commit real names, student IDs, signed
   recommendation/qualification forms, or copyrighted PDFs. The template ships with
   placeholders only.
3. **Class file changes.** `ntust_report.cls` is under the LPPL (see LICENSE-CLASS).
   If you modify and redistribute it, LPPL asks you to rename it so it can't be
   confused with the original.
4. **Keep it scannable.** Match the existing file layout and comment style.

## Local setup
- TeX Live 2023 or newer with XeLaTeX.
- Fonts for the default profile: `TeX Gyre Termes` (in TeX Live) and `AR PL UKai TW`
  (Debian/Ubuntu: `sudo apt-get install fonts-arphic-ukai`). See `fonts/README.md`.

## Code of conduct
This project follows the [Contributor Covenant](CODE_OF_CONDUCT.md).
