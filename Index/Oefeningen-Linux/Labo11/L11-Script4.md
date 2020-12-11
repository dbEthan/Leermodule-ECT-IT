```bash

#!/bin/bash

function readInput {
 clear
 read -p "Geef een username: " username
 read -p "Geef een groepnaam: " groupname
 read -p "Geef een filenaam: " filename
}

until chown $username:$groupname $filename 2>> errors.txt
do
 readInput
done