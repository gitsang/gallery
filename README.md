# gallery

## markdown usage

```md
![](https://github.com/gitsang/gallery/raw/master/20210328-111805.png)
```

## upload

```bash
git clone https://github.com/gitsang/gallery.git
cd gallery
# git pull
cp path/to/picture ./$(date +%Y%m%d-%H%M%S).png
git add all .
git commit -m "pic: new"
git push origin master
```

## bash alias

```sh
#!/bin/bash
#.bash_aliases
GALLERY_PATH=/root/project/gallery
upimg() {
    IMG_FILE=$1
    cp ${IMG_FILE} ${GALLERY_PATH}/$(date +%Y%m%d-%H%M%S).${IMG_FILE#*.}
    cd ${GALLERY_PATH}
    # git pull
    git add all .
    git commit -m "pic: new"
    git push origin master
}
```
