### Search files and replace

    ack "search term" -l --print0 | xargs -0 sed -i '' 's/search term/replacement term/g'

### Search filenames and rename

    $ ls -1 IMG_*

    IMG_2378.JPG
    IMG_2379.JPG
    IMG_2380.JPG

    $ for filename in IMG_*; do echo mv \"$filename\" \"${filename//IMG_/Fireworks}\"; done

    mv "IMG_2378.JPG" "Fireworks2378.JPG"
    mv "IMG_2379.JPG" "Fireworks2379.JPG"
    mv "IMG_2380.JPG" "Fireworks2380.JPG"

    ls -1 *foo* | awk '{print("mv "$1 " " $1)}' | sed 's/foo/bar/2' > rename.txt

### Calc lines of code

    find . -name "*.m" -or -name "*.h" -or -name "*.mm* -or -name "*.c* -or -name "*.xib" |xargs wc -l





