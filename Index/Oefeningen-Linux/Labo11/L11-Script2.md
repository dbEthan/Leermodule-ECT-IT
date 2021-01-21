## Oplossing 1
```bash

#!/bin/bash
read -p "geef een dir " dir

for bestanden in $(ls -p  $dir | grep -v /)
do
        echo $bestanden
        read -p "copy? " copy
                if [ $copy = "j" ]; then
                        mkdir -p kopiedir
                        cp $dir/$bestanden kopiedir/.
                fi
                read -p "verdergaan  j/n " verder
                if [ $verder = "n" ]; then
                        exit
                fi
done
echo "alle bestanden doorlopen"

```
## Oplossing 2
```bash

#!/bin/bash
read -p "geef een dir " dir

for bestanden in $(ls $dir)

do
if [ ! -d $dir/$bestanden ]; then
        echo $bestanden
        read -p "copy? " copy
                if [ $copy = "j" ]; then
                        mkdir -p kopiedir
                        cp $dir/$bestanden kopiedir/.
                fi
                read -p "verdergaan  j/n " verder
                if [ $verder = "n" ]; then
                        exit
                fi
fi
done

echo "alle bestanden doorlopen"
