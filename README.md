feathers
================

<!-- badges: start -->

![](https://img.shields.io/badge/colours-feathers-D5114E.svg)

<!-- badges: end -->

This package contains colour palettes inspired by the plumage of
Australian birds. For species exhibiting sexual dimorphism (i.e. males
and females look different), I have used female colours. Research on
birds has historically been biased towards males, and the choice to use
female colours in this package is my way of highlighting the
often-overlooked beauty of female birds.

## Installation

This package is hosted on GitHub and can be installed using the devtools
package:

``` r
devtools::install_github(repo = "shandiya/feathers", ref = "main")
```

## How to use `feathers`

Colour palettes are stored as a list called `feathers_palettes`, and can
be accessed thus:

``` r
library(feathers)
names(feathers_palettes)
```

    ##  [1] "spotted_pardalote"       "plains_wanderer"        
    ##  [3] "bee_eater"               "rose_crowned_fruit_dove"
    ##  [5] "eastern_rosella"         "oriole"                 
    ##  [7] "princess_parrot"         "blue_faced_parrot_finch"
    ##  [9] "superb_fairy_wren"       "cassowary"              
    ## [11] "yellow_robin"            "galah"

`get_pal` returns the chosen palette as a vector of hex colour codes.

``` r
get_pal("eastern_rosella")
```

    ## [1] "#cd3122" "#f4c623" "#bee183" "#6c905e" "#2f533c" "#b8c9dc" "#2f7ab9"

`print_pal` displays the colour palette.

``` r
eastern_rosella <- get_pal("eastern_rosella")
print_pal(eastern_rosella)
```

<img src="README_files/figure-gfm/unnamed-chunk-5-1.png" style="display: block; margin: auto;" />

## Examples

Colour palettes can be used for data visualisation in base `R` and
`ggplot2`.

``` r
# base R
library(palmerpenguins)
plot(penguins$flipper_length_mm, penguins$body_mass_g, col = get_pal("rose_crowned_fruit_dove")[factor(penguins$species)], pch = 19)

# ggplot2
library(ggplot2)
library(palmerpenguins)
ggplot(penguins) +
  geom_point(aes(flipper_length_mm, body_mass_g, colour = species)) +
  scale_colour_manual(values = get_pal("rose_crowned_fruit_dove"))
```

<img src="README_files/figure-gfm/unnamed-chunk-6-1.png" width="50%" /><img src="README_files/figure-gfm/unnamed-chunk-6-2.png" width="50%" />

## Colour palettes

The images below show each palette and the bird that inspired it.

### Eastern Rosella (*Platycercus eximius*)

<img src="README_files/figure-gfm/rosella_pal-1.png" style="display: block; margin: auto;" />

<img src="images/eastern_rosella_plot.png" width="65%" /><img src="images/eastern_rosella_img.png" width="35%" />

<font size="2">Image: [Duncan
McCaskill](https://commons.wikimedia.org/wiki/File:Platycercus_eximius_-Canberra,_Australia-8.jpg)</font>

### Plains-wanderer (*Pedionomus torquatus*)

<img src="README_files/figure-gfm/wanderer_pal-1.png" style="display: block; margin: auto;" />

<img src="images/plains_wanderer_plot.png" width="65%" /><img src="images/plains_wanderer_img.png" width="35%" />

<font size="2">Image: [JJ
Harrison](https://en.wikipedia.org/wiki/Plains-wanderer#/media/File:Plains-wanderer_female_8173.jpg)</font>

### Spotted Pardalote (*Pardalotus punctatus*)

<img src="README_files/figure-gfm/spotty_pal-1.png" style="display: block; margin: auto;" />

<img src="images/spotted_pardalote_plot.png" width="65%" /><img src="images/spotted_pardalote_img.png" width="35%" />

<font size="2">Image:
[Patrick_K59](https://commons.wikimedia.org/wiki/File:Spotted_Pardalote_(Pardalotus_punctatus)_female_(23113043855).jpg)</font>

### Rose-crowned Fruit-Dove (*Ptilinopus regina*)

<img src="README_files/figure-gfm/rcf_dove_pal-1.png" style="display: block; margin: auto;" />

<img src="images/rose_crowned_fruit_dove_plot.png" width="65%" /><img src="images/rose_crowned_fruit_dove_img.png" width="35%" />

<font size="2">Image:
[Sheba_Also](https://commons.wikimedia.org/wiki/File:Rose_crowned_Fruit_Dove_at_Australia_Zoo-1_(9098717408).jpg)</font>

### Rainbow Bee-eater (*Merops ornatus*)

<img src="README_files/figure-gfm/bee_eater_pal-1.png" style="display: block; margin: auto;" />

<img src="images/bee_eater_plot.png" width="65%" /><img src="images/bee_eater_img.png" width="35%" />

<font size="2">Image: [Jim
Bendon](https://commons.wikimedia.org/wiki/File:Rainbow_bee_eater_m%26f.jpg)</font>

### Superb Fairy-wren (*Malurus cyaneus*)

<img src="README_files/figure-gfm/superb_fw_pal-1.png" style="display: block; margin: auto;" />

<img src="images/superb_fairy_wren_plot.png" width="65%" /><img src="images/superb_fairy_wren_img.png" width="35%" />

<font size="2">Image:
[Patrick_K59](https://commons.wikimedia.org/wiki/File:Superb_Fairy-wren_(Malurus_cyaneus)_(18115879009).jpg)</font>

### Princess Parrot (*Polytelis alexandrae*)

<img src="README_files/figure-gfm/princess_pal-1.png" style="display: block; margin: auto;" />

<img src="images/princess_parrot_plot.png" width="65%" />

### Olive-backed Oriole (*Oriolus sagittatus*)

<img src="README_files/figure-gfm/oriole_pal-1.png" style="display: block; margin: auto;" />

<img src="images/oriole_plot.png" width="65%" /><img src="images/oriole_img.png" width="35%" />

<font size="2">Image:
[Patrick_K59](https://commons.wikimedia.org/wiki/File:Olive-backed_Oriole_(Oriolus_sagittatus)_(16640844194).jpg)</font>

### Southern Cassowary (*Casuarius casuarius*)

<img src="README_files/figure-gfm/cassowary_pal-1.png" style="display: block; margin: auto;" />

<img src="images/cassowary_plot.png" width="65%" /><img src="images/cassowary_img.png" width="35%" />

<font size="2">Image: [Nick
Hobgood](https://commons.wikimedia.org/wiki/File:Casuarius_casuarius_Southern_Cassowary_Papua_New_Guinea_by_Nick_Hobgood.jpg)</font>

### Eastern Yellow Robin (*Eopsaltria australis*)

<img src="README_files/figure-gfm/yellow_robin_pal-1.png" style="display: block; margin: auto;" />

<img src="images/yellow_robin_plot.png" width="65%" /><img src="images/yellow_robin_img.png" width="35%" />

<font size="2">Image:
[Patrick_K59](https://commons.wikimedia.org/wiki/File:Eastern_Yellow_Robin_(Eopsaltria_australis)_(42280188404).jpg)</font>

### Galah (*Eolophus roseicapilla*)

<img src="README_files/figure-gfm/galah_pal-1.png" style="display: block; margin: auto;" />

<img src="images/galah_plot.png" width="65%" /><img src="images/galah_img.png" width="35%" />

<font size="2">Image:
[Calistemon](https://commons.wikimedia.org/wiki/File:Galah_(Eolophus_roseicapilla)_at_Coalseam_Conservation_Park,_August_2022_16.jpg)</font>

## Continuous palettes

The qualitative colour palettes in `feathers` may be converted into
sequential or diverging palettes for different types of data
visualisation using the `colorRampPalette()` function.

### Sequential palette

``` r
# choose end colours
seq_col <- get_pal("eastern_rosella")[c(2,7)]  

# create a gradient of 50 shades in between the selected colours 
colorRampPalette(seq_col)(50)
```

<img src="README_files/figure-gfm/unnamed-chunk-8-1.png" style="display: block; margin: auto;" />

### Diverging palette

``` r
# choose end and middle colours
div_col <- get_pal("oriole")[c(1,5,10)]

# create a gradient of 50 shades in between the selected colours 
colorRampPalette(div_col)(50)
```

<img src="README_files/figure-gfm/unnamed-chunk-10-1.png" style="display: block; margin: auto;" />

## Accessibility

There are many tools and packages which simulate different types of
colour vision deficiency, such as [Viz
Palette](https://projects.susielu.com/viz-palette),
[colorblindcheck](https://jakubnowosad.com/colorblindcheck/index.html),
[prismatic](https://emilhvitfeldt.github.io/prismatic/), and
[colorblindr](https://github.com/clauswilke/colorblindr). You may find
these helpful in guiding your decisions about which colours to include
in your visualisation to make it accessible to as many people as
possible. Happy plotting!

## Contribute

If you would like to contribute to this package or have suggestions for
improvement, please contact [ShandiyaB](https://twitter.com/ShandiyaB)
on Twitter or submit a pull request.
