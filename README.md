# NIU Xaringan

A minimalist `xaringan` theme based on [Northern Illinois University](https://www.niu.edu)'s branding. There are two flavors:
1. A light theme (`niu.css` and `niu-fonts.css`) suitable for viewing on the web and small in-person presentations
2. A dark theme (`niudark.css` and `niudark-fonts.css`) suitable for projecting on large screens.

All relevant files can be found in the `/assets/` folder. Minimially, `niu.css`, `niu-fonts.css`, and
`NIU_horz_3Clr.png` are required to build the light (default) theme.

## Prerequisites

* A distribution of `R` - If you're here, I think that's a given. But just in case, grab the latest version [here](https://www.r-project.org).
* RStudio IDE - `xaringan` uses RMarkdown and `knitr` so [RStudio](https://rstudio.com) is pretty much required.
* `xaringan` - either from CRAN or the development version from Github.
```
install.packages(xaringan)
```
or
```
devtools::install_github('yihui/xaringan')
```

## Using `niu_xaringan`
Include the following information in the YAML preamble to your presentation.

Light theme:
```
output:
  xaringan::moon_reader:
    lib_dir: libs
    css: [default, "assets/niu.css", "assets/niu-fonts.css"]
```

Dark theme:
```
output:
  xaringan::moon_reader:
    lib_dir: libs
    css: [default, "assets/niudark.css", "assets/niudark-fonts.css"]
```

There are far more options that can be found in the example presentations [here](https://raw.githack.com/cbgoodman/niu_xaringan/master/light.html) for the light theme and [here](https://raw.githack.com/cbgoodman/niu_xaringan/master/dark.html) for the dark theme.

## Acknowledgements

Big shoutout to [Garth Tarr](https://github.com/garthtarr)'s [`sydney_xaringan`](https://github.com/garthtarr/sydney_xaringan) for the inspiration (which appears loosely based on the [`hygge.css`](https://github.com/yihui/xaringan/blob/master/inst/rmarkdown/templates/xaringan/resources/hygge.css) template in `xaringan`). Much of the boilerplate display/testing slides are from Garth. Many thanks.
