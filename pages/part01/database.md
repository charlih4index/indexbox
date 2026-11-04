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
title: Database
abstract: ""
authors:
  - name: Charlih Chen
exports:
  - format: typst
    template: lapreprint-typst
    output: _build/exports/typst/
---

# Database

MySQL, MariaDB, PostgreSQL, MongoDB, and SQLite are all popular open-source relational databases.

# Input by you

Find a way to have user to input to tagging as many as possible for the "word" AKA. "object" on database.

The tag is just like to hashtag.

The more tagging will define more clarify the "object".

{numref}`fig-tagging` Tagging to define the "object".

```{figure} ../images/tags.png
:name: fig-tag
:alt: Tagging

Tagging.
```

---
Every object has a reciprocal relationship. 

For example, A=B, B=Tag#1, B=Tag#2...B=Tag#n, etc. 

B defines and describes A with more Tag#1...Tag #n for assistance.

{numref}`fig-eq2` EQ2.

```{figure} ../images/tagseq2.png
:name: fig-eq2
:alt: EQ2

EQ2.
```

```
{
  "A": {
    "eq2": "B",
    "tag1": "4tag1",
    "tag2": "4tag2",
    "tag3": "4tag3",
    "tag4": "4tag4",
    "tag5": "4tag5",
    "others": "4others"
  }
}
```

Help me to modify the ZhuyinTable.html under GitHub.com/charlih4index/Chinese
Here is the sampler html code to update:

From:
```
      ㄇ
      <br/>
      ㄧ
      <br/>
      ㄝ
      <br/>
      ˊ
```
To:
```
   <a href="␢ㄇㄧㄝˊ.md" target="_blank">ㄅ
      <div>
      ㄧ
      <div>
      ㄝ
      <div>
      ˊ</a>
```
