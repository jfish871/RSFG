#!/usr/bin/bash
#Simple script that will allow the user to delete the contents of the TempFiles folder.

echo -n 'Do you want to clean out the temp files? y/N: ' 	# asks for user input 
read d							# records the what the user entered to the d varible 
printf

if [ $d = 'Y' ] || [ $d = 'y' ]; then #if the user enters yes, it will  delete all the text files in the folder.
				      # uses the || or operator to allow both upper and lower case Y as a valid responce.

        rm -i Downloads/*.txt # uses the rm command with the verbose flag to delete every file ending in .txt in the TempFiles directory.

elif [ $d = 'N' ] || [ $d = 'n' ]; then

	printf "No files deleted \n"

else
	printf "%s: Expected y\N" "$d"

