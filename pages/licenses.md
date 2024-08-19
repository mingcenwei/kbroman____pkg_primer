---
layout: page
title: Software licenses
description: Choose a license for your R package
---

The last thing you need to do before your package is a _proper_ R
package is to choose a license for your software and specify the
license within the `DESCRIPTION` file.

Software licenses are about two things: _copyright_, and _protecting
yourself_ from being held liable if your software screws something up
somewhere down the line.

I know next to nothing about copyright law outside the United States,
but in the US, [copyright](https://www.copyright.gov/circs/circ01.pdf)
is _automatic_ (you don't need to write &ldquo;&copy; 2014
A. Pendantic Person, All Rights Reserved&rdquo; all over the place, or
even once), and it gives you exclusive rights to copy your code. So if
you don't choose a license for your software, _no one else can use it!_

So, [pick a license, any license](https://blog.codinghorror.com/pick-a-license-any-license/).

There are
[lots of different software licenses](https://tldrlegal.com/) to
choose from. That's part of why this is such a painful topic. (That they are almost
all really boring to read is another part of the pain. The
[WTFPL](http://www.wtfpl.net/) is one of the few that is not boring.)

Personally, I choose between the
[Apache-2.0 license](https://www.apache.org/licenses/LICENSE-2.0) and the
[GNU General Public License (GPL)](https://www.gnu.org/copyleft/gpl.html). The
Apache-2.0 license is among the more permissive. The GPL is
&ldquo;viral&rdquo; in that it extends to derivative works: software
that incorporates code that was licensed under the GPL must also be
licensed under the GPL. So I use the GPL _if I have to_ (that is, if
I've incorporated others' GPL code), and I use the Apache-2.0 license
otherwise.

### Don't use a Creative Commons license for software

An important thing to remember: **don't use a
[Creative Commons](https://creativecommons.org/) (CC) license for
software**. Creative Commons licenses (like [CC-BY](https://creativecommons.org/licenses/by/3.0/))
are great, but they're for things like articles, books, and
videos, **but not software**. As
[they say in their FAQ](https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software):

> We recommend against using Creative Commons licenses for software.

Use CC licenses for your lecture notes, slides, and articles, but not
for your software.

### What about CC0?

[CC0](https://creativecommons.org/publicdomain/zero/1.0/) (public
domain) seems appropriate for software: you're just saying that anyone
can do anything with the code.

But in some states (e.g., Maryland, I think), software is treated as a
&ldquo;good&rdquo; (like a car), and so if your code causes something
terrible to happen, you could be sued for damages. Using a lenient
license, like the
[Apache-2.0 license](https://www.apache.org/licenses/LICENSE-2.0), eliminates
that potential problem through the &ldquo;no warranty&rdquo; clause.

So, use [CC0](https://creativecommons.org/publicdomain/zero/1.0/) for
your lecture notes, slides, and web sites, but use a lenient license,
like the [Apache-2.0 license](https://www.apache.org/licenses/LICENSE-2.0), for
your software.

### Indicating your choice in your package

So, pick a license, any license. And then indicate your choice in the
`DESCRIPTION` file for your R package.

#### GNU General Public License (GPLv3)

If you choose the GPL, note that there are multiple
versions. [GPLv2](https://www.gnu.org/licenses/gpl-2.0.html) is the old
version. Don't choose that. Choose the newer one,
[GPLv3](https://www.gnu.org/copyleft/gpl.html). The newer one fixes
some loopholes in the older one.

To use the GPLv3 with your R package, include the following line in
your `DESCRIPTION` file.

    License: GPL-3

If you also want to license your package under future versions of the GPL license, which is generally considered [good practice](https://usethis.r-lib.org/reference/licenses.html#arg-include-futured) because 'your package will automatically include "bug" fixes in licenses', you should include the following line in your `DESCRIPTION` file instead.

    License: GPL (>= 3)

#### Apache-2.0 license

If you're not incorporating code that is licensed under the GPL, I
recommend going with the Apache-2.0 license.

To use the Apache-2.0 license with your R package, include the following line in
your `DESCRIPTION` file.

    License: Apache License (== 2)

If you also want to license your package under future versions of the Apache license, which is generally considered [good practice](https://usethis.r-lib.org/reference/licenses.html#arg-include-futured) because 'your package will automatically include "bug" fixes in licenses', you should include the following line in your `DESCRIPTION` file instead.

    License: Apache License (>= 2)

### Including a copy of the license in your package source code

You must include a copy of your chosen license in your package source code. However, since CRAN prohibits the inclusion of standard licenses within packages, [you should save your license as `LICENSE.md` and add it to `.Rbuildignore`](https://usethis.r-lib.org/reference/licenses.html#details) to prevent the file from being sent to CRAN. For example, if you choose to use the Apache-2.0 license, you should include a `LICENSE.md` file like [this example](https://github.com/kbroman/pkg_primer/tree/gh-pages/example/stage5/LICENSE.md), and create a `.Rbuildignore` file like [this example](https://github.com/kbroman/pkg_primer/tree/gh-pages/example/stage5/.Rbuildignore).

With these changes, our package looks
[like this](https://github.com/kbroman/pkg_primer/tree/gh-pages/example/stage5),
and it is now a _proper R package_.

### Modern way of licensing a package

This process may seem tedious, but specific packages have been developed to streamline it. You can install the [`usethis`](https://usethis.r-lib.org/index.html) package and use its [functions](https://usethis.r-lib.org/reference/licenses.html) to automatically update your `DESCRIPTION`, `.Rbuildignore`, and `LICENSE.md` files. For example, if you want to license your package under the Apache-2.0 license and allow for future versions, simply run the following command in your package directory.

    usethis::use_apache_license(version = 2, include_future = TRUE)

---

### Homework

Pick a license for your software, make the appropriate changes to your
`DESCRIPTION` and `.Rbuildignore` files, and add a `LICENSE.md` file.

Then go to the page about [checking an R package](check.html).
