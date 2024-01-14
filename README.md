# BibLaTeX: Council of Science Editors style

Support for **Council of Science Editors** style in BibLaTeX.

Please notice that this is a _hacked_ approach (starting from `authoryear` style) and not a proper BibLaTeX style.  Still, I believe it works quite well.

## How to use

1. Download the `biblatex-cse.sty` file.
1. *Do not* load the `biblatex` package yourself.  Instead use `\usepackage{biblatex-cse}`, and the package will load `biblatex`.
1. If you want to enforce some options for `biblatex`, use `\PassOptionsToPackage{YOUR_OPTIONS}{biblatex}` **before** the `\usepackage{biblatex-cse}`.

## How to contribute

* If you find out somo non-conformance with CSE, let me know by opening and issue here in GitHub (or, even better, submit a pull request).
* If you know how to convert this into a proper BibLaTeX style, let me know… and we can work on it together.

<!-- --------

<picture>
  <source
    media="(prefers-color-scheme: dark)"
    srcset="
      https://api.star-history.com/svg?repos=joaomlourenco/biblatex-cse&type=Date&theme=dark
    "
  />
  <source
    media="(prefers-color-scheme: light)"
    srcset="
      https://api.star-history.com/svg?repos=joaomlourenco/biblatex-cse&type=Date
    "
  />
  <img
    width="500"
    alt="Star History Chart"
    src="https://api.star-history.com/svg?repos=joaomlourenco/biblatex-cse&type=Date"
  />
</picture>

**If you opt for using this project, please give it a star by clicking the (⭐️) at the top right of the [project's page](https://github.com/joaomlourenco/biblatex-cse).**

-------- -->