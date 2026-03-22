---
{"dg-publish":true,"permalink":"/installing-pcf-fonts-in-x/","tags":["programming"],"created":"2010-01-07"}
---


As I keep forgetting, here is how to install `pcf` fonts in X

1.  Create a new directory for the fonts, usually under /usr/share/fonts:

``` {.bash org-language="sh"}
$> mkdir /usr/share/fonts/
```

1.  Copy the `pcf` file(s) into it (sometimes the `pcf` files are gzipped):

``` {.bash org-language="sh"}
$> cp /path/to/pcf/*.pcf* /usr/share/fonts/
```

1.  Run mkfontdir, to create a fonts.dir file, used by X to find font files

``` {.bash org-language="sh"}
$> mkfontdir /usr/share/fonts/
```

1.  Add the new dir to X font path. The easiest way to do it is to stick this line in your `.xinitrc`:

``` {.bash org-language="sh"}
xset fp+ /usr/share/fonts/
```

Now your new font should compare in `xfontsel` and you should be able to use it as normal.

By the way, [this](http://www.proggyfonts.com/) is a very nice font for programming!
