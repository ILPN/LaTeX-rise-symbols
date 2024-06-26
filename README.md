# LaTeX transition rise symbols

This small repository contains a LaTeX package file, that defines two commands based on the [AMS math](https://ctan.org/pkg/amsmath?lang=en) LaTeX package.

The newly defined commands allow you to use a left/right half-filled triangle as a superscript symbol. These symbols were used in the [Token Trail Semantics – Modeling Behavior of Petri Nets with Labeled Petri Nets](https://link.springer.com/chapter/10.1007/978-3-031-33620-1_16) paper to define the rise of a transition (Definition 4).

## How to use

Add the `risesymbols.sty` file to your LaTeX project and use the `\usepackage{risesymbols}` command to include it. The provided LaTeX file defines two new commands, one for each symbol.

To use the symbols as a superscript in a math environment simply use the two new commands as follows:

```latex
$ t^{\trianglepafillhlsup} $

$ t^{\trianglepafillhrsup} $
```

The unfilled triangle, that is used in the paper to represents the rise itself, is not defined by this file, since a corresponding `\vartriangle` symbol exists in the AMS math package. The rise of a transition should therefore be defined as follows:

```latex
The rise $t^\vartriangle(m)$ of a transition $t$ in a marking $m$ is $t^\vartriangle(m) = t^{\trianglepafillhrsup}(m) - t^{\trianglepafillhlsup}(m)$
```

## Other options

The [oPlotSymbl](https://ctan.org/pkg/oplotsymbl?lang=en) LaTeX package defines half-filled triangle symbols. Our package uses the same naming scheme, and adds the `sup` suffix to denote the superscript. The symbols defined by the oPlotSymbl package can be used instead, but don't look good as superscript in our opinion.

Note, the symbols declared in our package don't render correctly if not used as superscripts! Should you need to use a half-filled triangle anywhere else, we recommend the oPlotSymbl package and their `\trianglepafillhl` and `\trianglepafillhr` commands.

## Contributing to the repository

If you encounter any issues with the package, feel free to open a pull-request, or to create a GitHub issue in this repository.
