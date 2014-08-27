---
layout: page
title: R package primer
tagline: a minimal tutorial
---

R packages are the best way to distribute R code and documentation,
and, despite the impression that the official manual
([Writing R Extensions](http://cran.r-project.org/doc/manuals/r-release/R-exts.html))
might give, they are really are rather simple to create.

Even for code that you don't plan to distribute, you'll find it is
easier to keep track of your own personal R functions if they are in a
package. And it's good to write documentation, even if it's just for
your future self.

[Hadley Wickham](http://had.co.nz/) is writing
[a book about the basics of R packages](http://r-pkgs.had.co.nz/). You might just
jump straight there. But there is value in having a diversity of
resources, so I thought I'd go ahead and write my own minimal tutorial.

- [Why write an R package?](pages/why.html)
- [The minimal R package](pages/minimal.html)
- [Building and installing an R package](pages/build.html)
- [Making it an proper package](pages/proper.html)
- [Writing documentation with Roxygen2](pages/docs.html)
- [Checking an R package](pages/check.html)
- [Software licenses](pages/licenses.html)
- [Putting it on GitHub](pages/github.html)
- [Getting it on CRAN](pages/cran.html)
- [Writing vignettes](pages/vignettes.html)
- [Writing tests](pages/tests.html)
- [Including datasets](pages/data.html)
- [Including compiled code](pages/compiled.html)
- [Resources](pages/resources.html)

If anything here is confusing (or _wrong_!), or if I've missed
important details, please
[submit an issue](https://github.com/kbroman/pkg_primer/issues), or (even
better) fork [this repository](http://github.com/kbroman/pkg_primer),
make modifications, and submit a pull request.

---

The source for this tutorial is [on github](http://github.com/kbroman/pkg_primer).

Also see my
[git/github guide](http://kbroman.org/github_tutorial) and
[knitr in a knutshell tutorial](http://kbroman.org/knitr_knutshell),
[minimal make tutorial](http://kbroman.org/minimal_make),
and [simple site tutorial](http://kbroman.org/simple_site).