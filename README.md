# RetroCRT 240p RetroPie Theme

This is a theme I've designed for [RetroCRT](https://github.com/xovox/RetroCRT), my customized toolset to run [RetroPie](https://retropie.org.uk) on CRT TVs & arcade cabinets.

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
