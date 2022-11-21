---
id: oofsw2vduzfhbonj7tnwolp
title: Bash
desc: ''
updated: 1658021212534
created: 1658020164965
---
## String Manipulation
robproject@hppav:~/playlist$ echo $stro
asdlm
robproject@hppav:~/playlist$ str=$(echo $stro | rev)
robproject@hppav:~/playlist$ echo $str
mldsa
robproject@hppav:~/playlist$ echo $var
asdf-12345679012.mp3
robproject@hppav:~/playlist$ str=$(echo $var | rev)
robproject@hppav:~/playlist$ $str
3pm.21097654321-fdsa: command not found
robproject@hppav:~/playlist$ strc=${str:0:4}${str:15}
robproject@hppav:~/playlist$ echo $strc
3pm.-fdsa
robproject@hppav:~/playlist$ strc=${str:0:4}${str:16}
robproject@hppav:~/playlist$ echo $strc
3pm.fdsa
robproject@hppav:~/playlist$ strm=$(echo $strc | rev)
robproject@hppav:~/playlist$ echo $strm
asdf.mp3
### Rename folder of files
(files='path/to/files')
for f in $files; do
frev=$(echo $f | rev)
fcut=${frev:0:4}${frev:16}
fback=$(echo $fcut | rev)
mv "$f" "$fback"
done


## Functions
### For loop
for f in files; do
	echo $f
done