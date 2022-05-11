# Unicode VGA font - TTF

[source: https://www.inp.nsk.su/~bolkhov/files/fonts/univga/](https://www.inp.nsk.su/~bolkhov/files/fonts/univga/)  

`px-` variant: traced pixel outlines  
`mx-` variant: traced pixel outlines + embedded bitmap font + [Windows CJK hack](https://stackoverflow.com/questions/43999875/prevent-anti-aliasing-or-sub-pixel-rendering-of-a-truetype-font)  

This wouldn't be possible without [int10h's oldschool fonts writeup](https://int10h.org/oldschool-pc-fonts/readme/).

For good measure, a copy of original source package is included in this repository in `uni_vga` subdirectory.

TODO: Embed actual Hiragana glyphs instead of empty placeholders in the `mx-` variant.

* * *
UNI-VGA is a Unicode VGA font for X11 and console. It is primarily intended to be the single source of fonts for console and for XDosEmu.

The font (`u_vga16`) is distributed in BDF format, and can be used in X11 as is. For use on console, the `bdf2psf.pl` script is included, which performs (BDF+SFM)->PSF conversion, using .sfm file as encoding table.

One of the aims while creating the font was its internal consistency. For example, accented glyphs shouldn't differ too much from unaccented ones, as it was in original IBM's VGA font. It also allowed to render _Latin Extended Additional_ glyphs with two accents, which was impossible with IBM's accents' size.

This font was designed to be usable both in 9-pixel (VGA text console) and in 8-pixel (framebuffer console and X11) modes, with VGA 8th->9th pixel expansion accurately taken into account.

The UNI-VGA font can be distributed and modified freely, according to the X license.

The _Basic Latin_ block was taken almost unchanged from DosEmu's `vga.bdf`. All the other blocks (except noted) were created mainly from scratch by me, Dmitry Bolkhovityanov.

Letters in the _Hebrew_ block were taken unchanged from a public domain hebrew console font.

Glyphs in _Arabic_, _Arabic Presentation Forms-A_, _Arabic Presentation Forms-B_ and U+262B _Farsi symbol_ were kindly donated by Behdad Esfahbod.

Thanks to Birger Langkjer for idea, to Mark Leisher for his wonderful XmBDFEd, and to many others for their support.
* * *
Copyright © 2001 by [Dmitry Yu. Bolkhovityanov](mailto:bolkhov@inp.nsk.su)  
TTF port by Illyan Garte 2022