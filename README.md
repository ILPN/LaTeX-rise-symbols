# LaTeX transition rise symbols

This small repository contains a LaTeX file, that defines two commands based on the [AMS math](https://ctan.org/pkg/amsmath?lang=en) LaTeX package.

The newly defined commands allow you to use a left/right half-filled triangle as a superscript symbol. These symbols were used in the [Token Trail Semantics – Modeling Behavior of Petri Nets with Labeled Petri Nets](https://link.springer.com/chapter/10.1007/978-3-031-33620-1_16) paper to define the rise of a transition (Definition 6).

## How to use

Add the `rise_symbols.tex` file to your LaTeX project and use the `\include{rise_symbols}` command before the `\begin{document}` command to include it. The provided LaTeX file uses the `\usepackage` commands to include the necessary dependencies and defines two new commands, one for each symbol.

To use the symbol as a superscript in a math environment simply use the two new commands as follows:

```latex
t^{\trianglepafillhlsup}

t^{\trianglepafillhrsup}
```

The unfilled triangle, that represents the rise itself is not defined by this file, since a corresponding `\vartriangle` symbol exists in the AMS math package. The rise of a transition should therefore be defined as follows:

```latex
The rise $t^\vartriangle$ of a transition $t$ is $t^\vartriangle = t^{\trianglepafillhrsup} - t^{\trianglepafillhlsup}$
```

## Other options

The [oPlotSymbl](https://ctan.org/pkg/oplotsymbl?lang=en) LaTeX package defines half-filled triangle symbols. Our commands use the same naming schema, but add the `sup` suffix to denote the superscript. The symbols defined by this package can be used, but don't look good as superscript in our opinion.

Do note that our commands don't render correctly outside of superscript! Should you need to use a half-filled triangle anywhere else, we recommend the oPlotSymbl package and their `\trianglepafillhl` and `\trianglepafillhl` commands.

## Contributing to the repository

If you encounter any issues with our file, feel free to open a pull-request, or to create a GitHub issue in this repository.
