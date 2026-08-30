# NTUST format compliance

This template follows the official NTUST layout rules. Verify the current rules
yourself before submitting, since they change and your department may add its own.

**Sources (official):**
- 學位論文撰寫、編排規則及注意事項 (applies from academic year 112 onward), NTUST
  Office of Academic Affairs: https://www.academic.ntust.edu.tw/p/412-1048-9660.php
- Thesis upload / binding / watermark rules, NTUST Library:
  https://etheses.lib.ntust.edu.tw/zh-hant/help/download/

## What the spec requires, and what this template does

| Rule (official spec) | Spec value | This template |
|---|---|---|
| Paper size | A4 (21 x 29.7 cm), white | `a4paper` |
| Margins | top 3 cm, bottom 2 cm, left 3 cm, right 3 cm | `common_env.tex` geometry (exact cm) |
| Line spacing | 1.5x line height (行距 1.5 倍行高) | `\baselinestretch{1.5}` in `common_env.tex` |
| Chinese font | 標楷體 (Kai) or 新細明體 | `AR PL UKai TW` (Kai), by name |
| English font | Times New Roman (as principle) | `TeX Gyre Termes` (Times-metric); the Times New Roman profile is provided (commented) in `my_ntust_thesis.tex` |
| Body text size | 12 pt or 13 pt | document class `12pt` |
| Page numbers | front matter Roman uppercase (I, II, III); main text Arabic (1, 2, 3); centered at bottom | `\pagenumbering{Roman}` then `\pagenumbering{arabic}`; `\pagestyle{plain}` |
| Watermark / PDF security | do NOT add your own; the ETD system inserts them on upload | watermark off by default |

## Required order of pages (spec section 三)

1. Cover (封面, with spine)
2. Title page (書名頁)
3. Advisor recommendation form (指導教授推薦書)
4. Committee qualification form (學位考試委員審定書)
5. Chinese abstract + 5-7 keywords (中文摘要)
6. English abstract + 5-7 keywords (英文摘要)
7. Acknowledgements (誌謝)
8. Table of contents (目錄)
9. Symbol index (符號索引) - only if you use symbols
10. List of figures (圖目錄) - required if 5 or more figures
11. List of tables (表目錄) - required if 5 or more tables
12. Main text (正文)
13. References (參考文獻)
14. Appendix (附錄)

The important library rule: **no blank page between the first three pages**
(cover, recommendation, qualification). See the SIGNED FORMS block in
`frontpages/ntust_frontpages.tex`.

## Notes and department-dependent items

The spec repeatedly states that the cover/title-page format is "for reference; the
department's rules prevail" (格式僅供參考，以各系所規定為準). Treat these as
department-dependent and adjust if needed:

- **Cover layout** (this template includes the NTUST logo and student ID, matching
  a common department variant; the spec's reference sample omits them).
- **Title page (書名頁)** as a page separate from the cover, if your department wants
  one. On the inner title page the spec sets the thesis title at 24 pt bold.
- **Heading sizes** (spec: chapter/section headings 20 pt, subsection 18 pt) and the
  spec's rule that chapters and sections are centered while subsections are
  left-aligned. This template keeps the document class's default heading treatment,
  which passed a real NTUST examination; adjust in `ntust_report.cls` if your
  department enforces the exact point sizes.
- **References style** is per department/advisor (APA, MLA, Chicago, IEEE, ...). The
  default here is `ieeetr` (numeric); change `\bibliographystyle{...}` in
  `backpages/ntust_backpages.tex` (see issue on bibliography styles).
- **Generative-AI disclosure**: if you use generative AI beyond simple wording
  polish, the spec requires you to clearly disclose what was AI-generated, why, and
  its scope, and to verify it. Follow your department's citation guidance.
