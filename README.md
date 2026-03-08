# Communication Logbook

This project is set up so you can compile either the full report or an individual lab.

## Folder layout

- `main.tex`: master document for the full lab notes
- `sections/`: introduction and conclusion shared by the full report
- `labs/labX/main.tex`: standalone lab files
- `labs/labX/figures/`: images that belong only to that lab

## Compile commands

Compile the full report from the project root:

```bash
latexmk -pdf main.tex
```

Compile an individual lab from the project root:

```bash
latexmk -pdf labs/lab1/main.tex
latexmk -pdf labs/lab2/main.tex
latexmk -pdf labs/lab3/main.tex
latexmk -pdf labs/lab4/main.tex
```

## Contributor rules

- Keep package imports and formatting in `main.tex`
- Do not add `\documentclass`, `\usepackage`, or a separate bibliography to a lab body unless you intentionally want it to diverge
- Put every figure for Lab `N` into `labs/labN/figures/`
- Use labels prefixed by the lab name, such as `lab2_fig_setup`
- If a figure is not present yet, the project still compiles and shows a placeholder box
