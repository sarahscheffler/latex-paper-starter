# Paper template

### Guide to the files and folders

Please note this is basically all convention.  If you have a good reason to deviate from this, or if
you prefer different conventions, please use those.  This is just what I use.  I've found many
students I work with like this structure, and I know I do too.

Top level directory:
* `main.tex` should be pretty skeletal and should just contain whatever imports you need for
  templates, import your preamble, and have pointers to all the actual content.
* `preamble.tex` should contain all `\usepackage` calls, as well as defined commands/macros. It is
  also fine to split these across multiple files if you prefer but I find it's usually not
  necessary.
* Whatever template, cls, etc files you need for your paper template.  Get these from the
  conference/journal website.
* Additional files like `.gitignore`, relevant scripts, etc.

* `src` should contain your main text source, one section per file.  I number these with BASIC-style
  `10_firstfile`, `20_secondfile` conventions so that they are sorted alphabetically and also so
  that you can insert a `15_first-and-a-half-file` if you need to.
  If the paper has a lot of appendices sometimes I will put these in a separate `app` folder but
  usually I will just put appendices in this folder.
* `img` should contain images that are imported with `\inputgraphics`.  It is important these are
  all in the same place because inputgraphics uses global filepaths for import.
* `fig` should contain big figure code, like tikz code or macros needed for figures.  (I put the
  actual `\begin{figure} ...\input{fig/...} ... \caption{...} ... \end{figure}` code inline in
  whatever `src` file calls the figure, that way if I click to edit the caption, it goes to the
  right place in the context of the surrounding text.)
* `bib` for `.bib` files.  If there is only one bib file it is fine to have it in the TLD but I
  often find myself adding multiple bib files (primarily in grants where I have to separately cite
  both related work, and my own past work, and co-PIs' past work...), so I usually like containing
  it within a folder.
* `cutting_board` is either a folder or a file that i use to store content I am cutting but want to
  keep around.  Realistically I basically end up throwing this content out 99% of the time, but the
  mental boost of hedging my bets against the 1% of times I will actually need it later is huge.
