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
title: First Example
abstract: ""
authors:
  - name: Author Name
exports:
  - format: typst
    template: lapreprint-typst
    output: _build/exports/typst/
---

# First Example

This chapter walks through a complete example.

## Setting Up

Describe the setup steps here.

## Sample Figure

{numref}`fig-sample` shows a sample bar chart generated with Matplotlib.

```{figure} ../images/sample_figure.png
:name: fig-sample
:alt: A sample bar chart

A sample bar chart showing values for five categories.
```

## Sample Dropdown

:::{dropdown} 2025
:open:

- Item 1
- Item 2
- Item 3

:::

:::{dropdown} 2024

- Item 1
- Item 2
- Item 3

:::

## Running the Example

```{code-cell} ipython3
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 2 * np.pi, 100)
y = np.sin(x)

fig, ax = plt.subplots()
ax.plot(x, y)
ax.set_xlabel("x")
ax.set_ylabel("sin(x)")
ax.set_title("A Simple Plot")
plt.show()
```

## Summary

This example demonstrated the basic workflow.

## World language

<img width="3264" height="2448" alt="TimePhoto_20260926_095105" src="https://github.com/user-attachments/assets/d976409c-d988-4451-9fa7-cb9ee21a7e9c" />

## Database

MySQL, MariaDB, PostgreSQL, MongoDB, and SQLite are all popular open-source relational databases.

## Input by you

Find a way to have user to input to tagging as many as possible for the "word" AKA. "object" on database.

The tag is just like to hashtag.

The more tagging will define more clarify the "object".

All object has bidirectional relationship. Eg. A=B, A=C, A=Z etc. A is defined / described by B, C and Z.

