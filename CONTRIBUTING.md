# Contributing

This is the loneliest account on Github, but in case anyone who is reading this who is not me, this is too big of a project to be handled by one person. So if you have the skills please consider contributing code.
Put the fonts and the example in the respective directories and follow the naming convention.
If an issue is to be created, please include many images as this is a very visual project.

Possible ways you can help:
+ Create a new pandoc template from an existing Typora theme. Stick as close as possible to the original source. If you want to do this I would recommend copying any template here and editing it to create the new one as it maintains code consistency.
+ Solve any one of the known issues are strike the issue in this document`.
+ Review the code and recommend a simplification.

## Resources

+ [typora-free](https://aur.archlinux.org/packages/typora-free) - free version of Typora available for arch-based distros
+ [codemirror.css](https://github.com/codemirror/CodeMirror/blob/master/lib/codemirror.css) - Codemirror default syntax highlighting
+ [Existing themes for Typora](https://theme.typora.io/)
+ [Github Markdown.md](https://github.com/cab-1729/Random-host/blob/main/Github%20Markdown.md) - Markdown file used for examples
+ [Typora's official guide for writing themes](https://theme.typora.io/doc/Write-Custom-Theme/)
+ [woff2ttf](https://archlinux.org/packages/extra/x86_64/woff2/) -  for converting woff2 to ttf, for arch based distros
+ [woff2otf.py](https://github.com/hanikesn/woff2otf) -  for converting woff to otf
+ [File from old, deprecated project](https://github.com/cab-1729/SchoolStuff/blob/main/School%20material/Program.cs) - a file using for testing syntax highlighting
+ svg images are converted to tikz using [this inkscape extension](https://github.com/xyz2tex/svg2tikz) and then modified accordingly
+ 1px is taken to be 0.010416667inches
+ Default color for checkbox background is #0075ff, border is #a8a8a8.
+ Command used for testing and compiling : ```pandoc --verbose --pdf-engine=xelatex --template={}.tex -f markdown+inline_code_attributes+implicit_header_references+footnotes+definition_lists -t pdf Github\ Markdown.md | zathura -```

## Known issues

+ evangelion, solarized, rubrication - ```pdfborder``` has too much padding. The underline needs to be closer to the text to better resemble ```href``` in html.
+ ~~cobalt - ```marginpar``` needs to be aligned with the heading.~~
+ all - formatting needs to be applied on level 6 headings. Pandoc does [not](https://github.com/jgm/pandoc/issues/8069) support it yet.
+ ~~all - switch back to ```longtable``` instead of tabular.~~
+ ~~all - inline code highlighting causes rest of paragraph to lose color.~~
+ mo, mo-dark - table full width and column alignment shifted towards right in order to achieve rounded corners
+ all - no github actions that would create the ```examples``` directory automatically on each merge/commit.
+ ~~all - no support for task list, highlight, definition list, superscript, subscript~~
+ ~~all - original theme github repo not mentioned as comment~~
+ ~~all - inline code box encompassing next character.~~
+ ~~all - make pixel a variable and use it for pixel lengths~~
+ ~~newsprint - table leaves box after it~~
+ torillic - theme not possible, texlive does not include [pdfinlimg](https://github.com/zerotoc/pdfinlimg), the package needed to add images to a theme
+ haru - theme not possible, italic version of version of Glow Sans not found
