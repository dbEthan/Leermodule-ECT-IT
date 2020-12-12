```bash

#!/bin/bash
clear

until chown $username:$groupname $filename 2>> errors.txt
do
 read -p "Geef een username: " username
 read -p "Geef een groepnaam: " groupname
 read -p "Geef een filenaam: " filename
done