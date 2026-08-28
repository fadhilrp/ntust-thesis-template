NTUST Thesis LaTeX Template
===========================

This is the plain-text quick pointer. The full guide is in README.md.

Compiler: XeLaTeX (required for Chinese via xeCJK). Main file: my_ntust_thesis.tex

You edit only:
  frontpages/my_names.tex      -- title, author, advisor, department, dates
  frontpages/my_eabstract.tex  -- English abstract
  frontpages/my_cabstract.tex  -- Chinese abstract
  frontpages/my_ackn.tex       -- acknowledgements
  sections/*.tex               -- your chapters (list them in my_ntust_thesis.tex)
  backpages/my_appendix.tex    -- appendices
  my_bib.bib                   -- your references

Do not edit the ntust_* files (they carry the NTUST format) unless you know why.

Build locally:  latexmk -xelatex my_ntust_thesis.tex
On Overleaf:    upload the repo ZIP, set Compiler = XeLaTeX, Main document = my_ntust_thesis.tex

See README.md for the full Overleaf tutorial, fonts, forms, and FAQ.
