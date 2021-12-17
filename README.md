# My PhD Dissertation
Model based analysis of multimodal neuroimaging: from neural masses to spectral graph theory.

The PDF file viewable at `main/dissertation.pdf`.

Students are welcomed to look at each tex file and use the main documents as a template for their own thesis. Hopefully this saves you from hours of formatting and reading some awful formatting requirements document.

### How to compile:
I recommend downloading TexMaker or installing LaTeX workshop extension with VSCode, then compiling the `dissertation.tex` file. Note that if you've never used LaTeX before and don't have any LaTeX compilers installed, you'd need to do so in addition to the editors. 

### Add-On's to make your life easier AND to accomodate dumb formatting requirements that nobody wants to read:
 - `\usepackage{subfiles}` to separate chapters into digestable files.
 - `\usepackage{indentfirst}` indents first paragraph after `\section` tags
 - `\usepackage[all]{nowidow}` to eliminate widow/orphan sentences.
 - `\usepackage[justification=centerlast]{caption}` to uniformly justify figure captions.
 - `begin{tabular*}{\textwidth}` to fit fat tables to text width with the `tabular*` environment instead of the simpler `tabular` environment.
 - For long figures or captions that span more than one page:
    - First delcare a new command to label the figure as ***Continued***: `\DeclareCaptionLabelFormat{adja-page}{\hrulefill\\#1 #2 \emph{(Continued)}}`
    - For the large figure, declare 2 figure environments, and use `\ContinuedFloat` and `\captionsetup{labelformat=adja-page}` for continuation. 

### How to create slides with jupyter:
Install [rise](https://rise.readthedocs.io). This only works with `jupyter notebook` right now, and is not compatible with `jupyter lab`.

### License:
This work is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.
