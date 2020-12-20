```bash

#!/bin/bash
read -p "geef een zin: " zin
read -p "geef een woord: " woord

for input in $zin
do
        if [ $woord = $input ]; then
        echo "$woord is gevonden"
        fi
done