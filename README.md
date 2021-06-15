# RetroCRT 240p RetroPie Theme

This theme is under active development and will be changing regularly for the forseeable future

This is a theme I've designed for [RetroCRT](https://github.com/xovox/RetroCRT), my customized toolset to run [RetroPie](https://retropie.org.uk) on CRT TVs & arcade cabinets.

* Supports
  * Basic View with MASSIVE TEXT
  * Detailed View
  * Video View

* Unsupported
  * Grid View, but this may come at some point

# Unsupported Main Systems

These will be supported soon

```
atarijaguarcd
atarifalcon
atarixe
```

# Gallery

* [The big gallery](https://github.com/xovox/RetroCRT-Media/blob/master/RetroCRT-240p/GALLERY.md) has all of my pics.
![alt text](https://raw.githubusercontent.com/xovox/RetroCRT-Media/master/RetroCRT-240p/NES_Mockup.png)

# Generating Logos

For the MAME logos with rotated text
```
convert mame.png \
	-fuzz 1% \
	-trim +repage \
	-scale x329 \
		/tmp/mame.png

convert \
	-size 329x120 xc:transparent \
	-font zorque \
	-fill "#296ca2" \
	-pointsize 135 \
	-gravity center \
	-annotate +0+0 "${year}" \
	-rotate 90 \
		/tmp/${year}.png

montage \
	-background none \
	/tmp/mame.png \
	/tmp/$year.png \
	-geometry +1+1 \
		mame-${year}.png
```

# Framebuffer Screenshots

* https://github.com/AndrewFromMelbourne/raspi2png
