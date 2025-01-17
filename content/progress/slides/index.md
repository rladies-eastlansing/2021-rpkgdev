---
outputs:
- Reveal
title: How to improve your R package
hidden: true
layout: list
weight: 11
output: hugodown::md_document
countdown: true
rmd_hash: 23e43a9930a2cf70

---

# How to improve your R package

Automatically ✨, and not 🧠

------------------------------------------------------------------------

# Workflow automation tools

:robot:

------------------------------------------------------------------------

## Assessing your package

-   [R CMD check or `devtools::check()`](http://r-pkgs.org/check.html), [`BiocCheck`](https://bioconductor.org/packages/release/bioc/html/BiocCheck.html)

-   [`goodpractice`](http://mangothecat.github.io/goodpractice/) and [`lintr`](https://www.tidyverse.org/blog/2017/12/workflow-vs-script/) (possibly via [CodeFactor](https://www.codefactor.io)).

-   [`covr::package_coverage()`](http://covr.r-lib.org/reference/package_coverage.html)

-   [`devtools::spell_check()`](http://devtools.r-lib.org/reference/spell_check.html)

------------------------------------------------------------------------

## Improve metrics by hand?!

Yes and no!

{{< figure src="yellow-latex-gloves-on-dish-rack-4039452.jpg" alt="Gloves on dish rac" caption="Picture by [Lisa Fotios](https://www.pexels.com/photo/yellow-latex-gloves-on-dish-rack-4039452/)" width=200 >}}

------------------------------------------------------------------------

## Tools for improving

-   [`styler`](https://styler.r-lib.org/). Better paired with [version control](https://happygitwithr.com/).

-   [`roxygen2`](https://roxygen2.r-lib.org/articles/rd.html) NAMESPACE generation. Switching: [`Rd2roxygen`](https://yihui.org/rd2roxygen/).

-   [`pkgdown`](https://pkgdown.r-lib.org/). Work on reference index & navbar!

-   `usethis` e.g. [`usethis::use_test()`](https://usethis.r-lib.org/reference/index.html#section-package-development).

------------------------------------------------------------------------

## When and where to use the tools?

Right after my talk (not now 😜), but then?

{{< figure src="photo-of-planner-and-writing-materials-760710.jpg" alt="Planner" caption="Picture by [Bich Tran](https://www.pexels.com/photo/photo-of-planner-and-writing-materials-760710/)" width=300 >}}

------------------------------------------------------------------------

## Continuous integration

**Run something every time you make a change**

> "The idea behind continuous integration is that CI will automatically run R CMD check (along with your tests, etc.) every time you push a commit to GitHub. You don't have to remember to do this; CI automatically checks the code after every commit." [Julia Silge](https://juliasilge.com/blog/beginners-guide-to-travis/)

Travis, GitHub Actions, Circle CI, [`tic` package](https://docs.ropensci.org/tic/)...

------------------------------------------------------------------------

## Continuous integration

How to learn?

[Julia Silge's post](https://juliasilge.com/blog/beginners-guide-to-travis/) - [Jim Hester's GitHub Actions talk](https://www.jimhester.com/talk/2020-rsc-github-actions/) - [`usethis` helpers](https://usethis.r-lib.org/reference/index.html#section-continuous-integration)

{{< tweet 1205183124868681728 >}}

------------------------------------------------------------------------

## More with continuous integration

Couple a thing (R CMD check? pkgdown site building?) to

... each commit,

... every Monday,

... applying a label to a pull request?

------------------------------------------------------------------------

## Pre-commit

{{< figure src="mara.jpg" alt="Tired: Always remember to do things well. Wired: Use continuous integration to notice wrong stuff" caption="Illustration by [Mara Averick](https://twitter.com/dataandme/status/1255510799273132032)" width=400 >}}

------------------------------------------------------------------------

## Pre-commit

[`precommit` R package](https://lorenzwalthert.github.io/precommit/) -- Python [precommit framework](https://pre-commit.com/)

-   Setup hooks

-   Hooks for styling, parsable R code, spell checks, etc.

------------------------------------------------------------------------

## Pre-commit

🤫 You can still skip the checks.

------------------------------------------------------------------------

## Check things before show time

CRAN release! 🐉 Checks on different platforms, URLs, spell checks...

-   [submission checklist](https://cran.r-project.org/web/packages/submission_checklist.html)

-   [`usethis::use_release_issue()`](https://usethis.r-lib.org/reference/use_release_issue.html) creating a GitHub issue with important items.

-   or [`devtools::release()` function](https://github.com/r-lib/devtools/blob/b166195be72927a003e6937de5c3239881095a9f/R/release.R#L39)

------------------------------------------------------------------------

## Improve workflow vs. procrastinate

Risk of spending too much time on [meta-work](https://youtu.be/dIjKJjzRX_E?t=633).

As a beginner, easier to create good habits. :wink:

{{< figure src="pedro-da-silva-unEmGQqdO7Q-unsplash.jpg" alt="Stop sign with photoshoped street names: 'Homework Ave' and 'Procrastination Pk'." caption="Picture by [Pedro da Silva](https://unsplash.com/photos/unEmGQqdO7Q)" width=200 >}}

------------------------------------------------------------------------

# Reading code & about code

------------------------------------------------------------------------

## Why read source code

-   You want to know what is going on.

-   You want to build on the function/package for your own goals.

-   You're just curious.

-   You need examples of a thing in the wild.

------------------------------------------------------------------------

## How to read source code

-   [`lookup` package](https://github.com/jimhester/lookup#readme)

-   [GitHub search](https://help.github.com/en/articles/about-searching-on-github)

-   Mirrors of [CRAN packages](https://github.com/cran) and [R-source](https://github.com/wch/r-source), on GitHub.

------------------------------------------------------------------------

## Reading code...

And trying things out!

Fork, clone, and explore!

[Podcast episode "Learning a new codebase", with Patricia Aas](https://www.allthingsgit.com/episodes/learning_a_new_codebase_with_patricia_aas.html)

------------------------------------------------------------------------

## Read blogs and fora

Blog posts: digested information.

-   [R-hub blog](https://blog.r-hub.io/), rOpenSci [blog](https://ropensci.org/blog) and [tech notes](https://ropensci.org/technotes)

-   [tidyverse blog](https://www.tidyverse.org/blog/2020/04/self-cleaning-test-fixtures/)

-   [R Weekly](https://rweekly.org/)

-   *Your* blog?

------------------------------------------------------------------------

## Read blogs and fora

Fora: Help and learn.

[R-package-devel](https://stat.ethz.ch/mailman/listinfo/r-package-devel), [RStudio community "package development" category](https://community.rstudio.com/c/package-development/11), [rOpenSci forum](https://discuss.ropensci.org/).

💡 Manage your subscriptions & involvement wisely!

------------------------------------------------------------------------

## rOpenSci Software Peer Review

[Transparent, constructive, non adversarial and open review process](https://devguide.ropensci.org/softwarereviewintro.html#whatissoftwarereview) for packages [in scope](https://devguide.ropensci.org/policies.html#aims-and-scope).

Interesting for authors, and reviewers!

[Online book of best practice](https://devguide.ropensci.org/) for the reviews and package development.

------------------------------------------------------------------------

## rOpenSci Software Peer Review

🚀 Even more review and best practice on the way! [rOpenSci Statistical Software Peer Review](https://ropensci.org/stat-software-review/)

------------------------------------------------------------------------

## Other venues

See also JOSS, R Journal, JSS.

------------------------------------------------------------------------

## Questions?

Write them in the shared doc.

------------------------------------------------------------------------

## Time for a break! :tea:

<!--html_preserve-->

<div id="timer_hugo" class="countdown" style="top:100;left:0;" data-warnwhen="0">

<code class="countdown-time"><span class="countdown-digits minutes">05</span><span class="countdown-digits colon">:</span><span class="countdown-digits seconds">00</span></code>

</div>

<!--/html_preserve-->

