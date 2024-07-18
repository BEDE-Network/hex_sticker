BEDE Hex Sticker
================
2024-07-18

# Code for creating the BEDE Network hex sticker

1.  First, we need to install and load the requisite packages.

``` r
#install.packages(c("remotes", "magick"))   
#remotes::install_github("GuangchuangYu/hexSticker")
library(hexSticker)
library(magick)
```

    ## Linking to ImageMagick 6.9.12.93
    ## Enabled features: cairo, fontconfig, freetype, heic, lcms, pango, raw, rsvg, webp
    ## Disabled features: fftw, ghostscript, x11

2.  We need to read in the logo image as an object.

``` r
img <- image_read("BEDE_logo.png", strip = TRUE)
```

3.  Use the `sticker()` function to create the sticker.

``` r
output <- sticker(img, package = "", 
                  s_x = 1, s_y = 1,
                  s_width = 1.5, s_height = 1.5,
                  h_fill = "#FFFFFF", h_color = "#76b823",
                  h_size = 3, filename = "BEDE_hex_sticker.png")
output
```

![](BEDE_hex_sticker_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->
