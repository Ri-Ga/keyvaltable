The keyvaltable Package
=======================

Copyright (C) 2016-2020 Richard Grewe

Released under the [LaTeX Project Public License](http://www.latex-project.org/lppl/) version 1.2 or later

## Purpose

The main goal of the `keyvaltable` package is to offer means for
typesetting tables easily and yet still looking rather nicely in a way
that separates content from presentation and with re-usable layout for
tables of the same type. For this purpose, the package provides the
environment `KeyValTable`, which allows one to typeset tables that have
a previously defined column layout and whose rows can be produced in a
key-value fashion.

## Availability

The `keyvaltable` package is on [CTAN](http://www.ctan.org/pkg/keyvaltable),
where you can also find the [documentation](http://mirrors.ctan.org/macros/latex/contrib/keyvaltable/keyvaltable.pdf),
as well as on [github](https://github.com/Ri-Ga/keyvaltable).
Since March 2016, `keyvaltable` is part of TeX Live (package `texlive-latex-extra`) and
is included in [MiKTeX](http://miktex.org/packages/keyvaltable).

## Manual Installation

The `keyvaltable` package comes with (at least) the following files
* keyvaltable.ins
* keyvaltable.dtx
* README.md

and possibly also with
* Makefile
* keyvaltable.pdf (generated from keyvaltable.dtx)
* keyvaltable.sty (generated from keyvaltable.dtx)

To install the `keyvaltable` package, you additionally need
* docstrip.tex

To build the package (`keyvaltable.sty`), run one of the following
```
    latex keyvaltable.ins
    make package (needs Makefile)
```

Put the resulting `keyvaltable.sty` somewhere where LaTeX can find it.
Read the documentation of your LaTeX system to find out where this
might be.

## Building Documentation

To build the documentation of the `keyvaltable` package, you additionally
need the following classes and packages (including their dependencies)
* ltxdoc
* idxlayout
* xcolor
* showexpl
* enumitem
* xkeyval
* booktabs
* longtable
* tabu
* etoolbox
* hypdoc
* xintexpr
* makecell

as well as
* pdflatex

To build the documentation (`keyvaltable.pdf`), either run
```
    make docs
```
or the following sequence of commands
```
    pdflatex keyvaltable.dtx
    makeindex -s gind.ist -o keyvaltable.ind keyvaltable.idx
    makeindex -s gglo.ist -o keyvaltable.gls keyvaltable.glo
    pdflatex keyvaltable.dtx
    pdflatex keyvaltable.dtx
```

Happy TeX'ing
