# latex-cursed

Scripts and snippets for LaTeX (extremely cursed)

## ltxkeepaux

Restores content of auxiliary files if a compile run fails.

Normally, after a syntax error, you are left with an empty .aux file, and therefore, after fixing the error, you have to rebuild the document 2 to 5 files because LaTeX forgot about all the references.

This wrapper simply restores the original .aux and .out files after an unsuccessful run, which makes it look like the faulty compile run never happened.

Use as: `ltxkeepaux pdflatex ...`

## filterlatex

Produces a filtered output of a LaTeX process. There are already tons of these tools, so how is this one different?

- Interactive input to the LaTeX process is still possible, like when it asks what to do on an error, or if you are using the [unravel](https://ctan.org/pkg/unravel) package.
  (`texfot` cannot do this.)
- (Currently) filters only the list of loaded filenames (which is usually the largest and also least interesting part of output) and preserves all other output.
  (Again, `texfot` filters much more, sometimes this is too much, though, and also sometimes truncates warnings)

Use as: `filterlatex pdflatex ...`
