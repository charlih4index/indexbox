---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
kernelspec:
  display_name: Python 3
  language: python
  name: python3
title: English
abstract: ""
authors:
  - name: Author Name
exports:
  - format: typst
    template: lapreprint-typst
    output: _build/exports/typst/
---

# English

## Uppercase

| [A](A.md) | [B](B.md) | [C](C.md) | [D](D.md) | [E](E.md) | [F](F.md) | [G](G.md) | [H](H.md) | [I](I.md) | [J](J.md) | [K](K.md) | [L](L.md) | [M](M.md) | [N](N.md) | [O](O.md) | [P](P.md) | [Q](Q.md) | [R](R.md) | [S](S.md) | [T](T.md) | [U](U.md) | [V](V.md) | [W](W.md) | [X](X.md) | [Y](Y.md) | [Z](Z.md) |

## Lowercase

| [a](lowercase/a.md) | [b](lowercase/b.md) | [c](lowercase/c.md) | [d](lowercase/d.md) | [e](lowercase/e.md) | [f](lowercase/f.md) | [g](lowercase/g.md) | [h](lowercase/h.md) | [i](lowercase/i.md) | [j](lowercase/j.md) | [k](lowercase/k.md) | [l](lowercase/l.md) | [m](lowercase/m.md) | [n](lowercase/n.md) | [o](lowercase/o.md) | [p](lowercase/p.md) | [q](lowercase/q.md) | [r](lowercase/r.md) | [s](lowercase/s.md) | [t](lowercase/t.md) | [u](lowercase/u.md) | [v](lowercase/v.md) | [w](lowercase/w.md) | [x](lowercase/x.md) | [y](lowercase/y.md) | [z](lowercase/z.md) |

## Note

```
Help me to find an newest and complete Excel that can downlaod for an English to Chinese dictionary.
```
```
Short answer:  
The newest and most complete English→Chinese dictionary you can download in Excel (or easily convertible to Excel) is the 103,976‑word bilingual dataset from CSDN, which includes a ready-made Excel version. It is the only large, recent (2026) dataset explicitly offering SQL + CSV + Excel formats with full Chinese definitions, parts of speech, phonetics, and cleaned data.
```

✅ Best Option for You (Excel-ready)
103,976-word English–Chinese dictionary (SQL / CSV / Excel package)
Format: Includes Excel version, CSV, and SQL.

Size: 103,976 entries.

Content: English word, phonetic, part of speech, Chinese definitions (multiple senses).

Quality: Cleaned, deduplicated, encoding fixed, phonetic errors corrected.

Release: Updated 2026‑09‑06 (very recent).

Use case: Perfect for Excel filtering, tagging, building your own dictionary workbook, or feeding into scripts.

[Download](https://github.com/1eez/103976): Provided directly in the CSDN resource pack. 

Why this is the best match:  
You specifically asked for a newest and complete Excel dictionary. This is the only dataset in the search results that explicitly includes an Excel file and is recently updated.

🥈 Second-best (convertible to Excel)
ECDICT (MIT-licensed English–Chinese dictionary)
Format: SQLite, CSV, StarDict (no native Excel, but CSV opens in Excel).

Size: ~770k English entries + 125k Chinese entries (very large).

Source: Open-source, widely used in dictionary apps.

[Download](https://sourceforge.net/projects/ecdict.mirror/?utm_source=copilot.com): SourceForge mirror updated 2025‑11‑13. 

Use case: If you want maximum completeness, you can open the CSV in Excel, but you must clean/reshape it yourself.

Why not #1:  
It’s extremely complete but not provided as Excel, and requires manual conversion.

🥉 Other related tools (not Excel dictionaries)
These are not downloadable dictionaries but may appear in search results:

EnZhDict (desktop dictionary app)
Uses ECDICT internally; can export CSV, but not a full Excel dictionary. 

Excel Offline Translator (GitHub)
Translates Excel files but does not provide a dictionary dataset. 

Translate for Excel (Marketplace add-in)
Machine translation inside Excel; not a dictionary download. 

📌 Recommendation Based on Your Workflow
You’ve previously worked with Excel automation, word-class extraction, and dictionary processing.
Given your workflow, the 103,976-word Excel dataset is the most practical:

Already in Excel format

Cleaned and structured

Easy to extend with your own columns (詞類, 釋義拆分, etc.)

Lightweight (4.63 MB)

Updated in 2026, newer than ECDICT

```
Just upload 2 Excel files "ecdictA-L.xlsx" and "ecdictM-ZwNo.xlsx" which is the English words database on GitHub.com/charlih4index/english/
Please grab word from column A and write those word as 1st column on MD table on .md file at /indexbox/english/ 
Please check the A.md as sampler file with word "above" by MD table syntax for rest of work extract from those 2 Excel files.
The column F on Excel file should fall into 2nd column table syntax on MD file. The 3rd, 4th, 5th, 6th column table syntax on MD file are very easier to just replace the word "above" on existing URL. 
For example, /above?src=search-dict-box, /english/above?q=Above, ?p=Above, and the /wiki/Above.
```


