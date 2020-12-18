```bash

#!/bin/bash
clear

echo "a) bestanden aanmaken"
echo "b) bestand checken"
echo "c) bestand wissen"
read -p "Kies een optie: " choice

case $choice in
 'a')
   clear
   read -p "Geef een naam: " name
   read -p 'Geef een getal: ' getal
   
   until [ $getal -eq 0 ]
   do
	touch $name$getal.txt
	getal=$(($getal - 1))
   done

   ls
   ;;

 'b')
   clear
   read -p "In welke directory moeten bestanden gechekt worden? " dir
   read -p "Geef de bestandsnaam: " filename

   cd $dir
   if [ -e $filename ]; then
	echo "Bestaat"
   else
	echo "Bestaat niet"
   fi
   ;;

 'c')
   clear
   read -p "In welke directory moet een bestand gewist worden? " directory
   read -p "Geef de naam van het bestand: " bestand
   cd $directory
   rm $bestand
   ;;
esac