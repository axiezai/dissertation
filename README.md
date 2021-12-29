# My PhD Dissertation
Model based analysis of multimodal neuroimaging: from neural masses to spectral graph theory.

The PDF file viewable at `main/dissertation.pdf`.

Students are welcomed to look at each tex file and use the main documents as a template for their own thesis. Hopefully this saves you from hours of formatting and reading some awful formatting requirements document.

### How to compile:
For beginners that's never touched LaTeX before, you will need:

- LaTeX compilers like `pdflatex` and `bibtex` to turn text files into a beautiful PDF. MacOS users familiar with the commandline should have `brew` setup and follow [this](https://formulae.brew.sh/cask/mactex-no-gui) to install the necessary compilers. More details can be found at [https://www.latex-project.org/get/](https://www.latex-project.org/get/).

- A plain text editor of any sort, there are ones made for LaTeX specifically.
    - I personally used [`texmaker`](https://www.xm1math.net/texmaker/), remember to go to Preferences and edit <em>Quick Build</em> to `pdflatex + bib(la)tex + pdflatex + View PDF` for a smooth experience. Change the font size and other preferences while you are at it for your comfort.
    - For coders, use [`VSCode`](https://code.visualstudio.com/) with the [`LaTeX Workshop`](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension, it's quite lightweight and you can add a bunch of other text editing extensions for quite a good experience.
    - Here's quite a large list of other options: https://tex.stackexchange.com/questions/339/latex-editors-ides


You will only `build` the `main/dissertation.tex` file. It includes everything you will need. For experienced `git` users, feel free to `clone` this repository and start your own project by copying over `main/{dissertation.tex,hangcaption.sty,cornell.cls}` to your repo. Then create a blank `References.bib` and copy over from a citation manager your desired references in `bibtex` format.

Notice all files are placed with relative paths (ex: `../chapter1/introduction` from `main/dissertation.tex` for `chapter1/introduction`). So follow the folder structure or modify the paths to match your own.


### Add-On's to make your life easier AND to accomodate dumb formatting requirements that nobody wants to read:
 - `\usepackage{subfiles}` to separate chapters into digestable files.
 - `\usepackage{indentfirst}` indents first paragraph after `\section` tags
 - `\usepackage[all]{nowidow}` to eliminate widow/orphan sentences.
 - `\usepackage[justification=centerlast]{caption}` to uniformly justify figure captions.
 - `begin{tabular*}{\textwidth}` to fit fat tables to text width with the `tabular*` environment instead of the simpler `tabular` environment.
 - For long figures or captions that span more than one page:
    - First delcare a new command to label the figure as ***Continued***: `\DeclareCaptionLabelFormat{adja-page}{\hrulefill\\#1 #2 \emph{(Continued)}}`
    - For the large figure, declare 2 figure environments, and use `\ContinuedFloat` and `\captionsetup{labelformat=adja-page}` for continuation. 
    - Make sure the figure caption is alone with no other text with `\clearpage` before and after inserting the caption.

These changes are already implemented in `main/dissertation.tex`, do not edit the preamble unless you know what you are doing, and you are certain your edits will still follow formatting guidelines.

For LaTeX newcomers that's never created documents in plain text before, google `overleaf how to x` for simple guidelines on how to do certain things if following my `.tex` files are not instructive.


### How to create slides with jupyter:
Install [rise](https://rise.readthedocs.io). This only works with `jupyter notebook` right now, and is not compatible with `jupyter lab`.

### License:
This work is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.
