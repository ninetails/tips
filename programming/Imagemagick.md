# Programming/Imagemagick

## Batch

### Image diff (folders)

```sh
#!/usr/bin/env bash
path1="/path/orig"
path2="/path/new"
path3="/path/diff"
cd $path1
img_list=`ls`
for img1 in $img_list; do
img2=`find $path2 | grep "$img1"`
convert $img1 $img2 -gravity center -compose difference -composite ${path3}/$img1
done
```

[Source](https://www.imagemagick.org/discourse-server/viewtopic.php?t=29411#p131628)
