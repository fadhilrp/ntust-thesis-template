# Fonts

This template compiles with **XeLaTeX**, which resolves fonts **by name through
the operating system's font database** (fontconfig on Linux/Overleaf), not the
TeX Live tree.

## Default profile (what ships)

`my_ntust_thesis.tex` sets, by name:

- **Latin:** `TeX Gyre Termes`, a Times-metric font that ships with every TeX
  Live, so it resolves on Overleaf, GitHub Actions, and local machines with no
  setup.
- **CJK:** `AR PL UKai TW`, the NTUST-canonical Kai (楷) font, available on
  Overleaf by name. For **local** or **CI** builds install it via your package
  manager, e.g. Debian/Ubuntu: `sudo apt-get install fonts-arphic-ukai`.

This directory is intentionally empty by default (no bundled font binaries) to
keep the repository small; the default profile needs no files here.

## Offline / fully self-contained profile (optional)

If you need byte-identical output on a machine with no internet and no font
packages, bundle a font here and load it by path. Uncomment profile (b) in the
FONTS block of `my_ntust_thesis.tex`, then drop the files in this folder:

- **TeX Gyre Termes** (Latin): copy the four `texgyretermes-*.otf` files from
  your TeX Live tree (`kpsewhich texgyretermes-regular.otf`).
- **A Kai CJK font**, openly licensed and redistributable. Good options:
  - **TW-Kai / 全字庫正楷體**, Taiwan government open data (標楷體, full glyph
    coverage). Download: https://data.gov.tw/dataset/5961
  - **cwTeX Q Kai** (OFL 1.1, smaller ~8.5 MB):
    https://github.com/l10n-tw/cwtex-q-fonts

Put each bundled font's own license file next to it in this folder. Do **not**
relicense fonts under the repository's MIT license.
