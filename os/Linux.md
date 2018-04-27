# OS/Linux

## Change fonts for user

```sh
mkdir ~/.local/share/fonts
cp *.ttf ~/.local/share/fonts
fc-cache -fv
```

## Batch resize using Imagemagick

```sh
for i in $( ls *.png); do convert -resize 50% $i re_$i; done
```

[Sauce](https://linuxconfig.org/batch-image-resize-using-linux-command-line)
