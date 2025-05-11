#!/usr/bin/bash
# a silly script that, creates a garbage file, cleans the file, then sorts the output
#

#./DeleteUtil

printf "Enter S for Silent Mode, enter  V for Verbose Mode: "
read x

#rm -v TempFiles/Value.txt
printf "%s\n" $x > TempFiles/Value.txt #Submitting User input to a file to be read back by the other sub programs. This will set them into either silent or verbose mode.
	
if [ $x = 'S' ] || [ $x = 's' ]; then #If the user entered S, then it will run the all the sub programs in silent mode.
	printf
	./GarbageGen #Runs the GarbageGen module, creates a garbage file.
	sleep 1
	./FileCleaner #Runs the FileCleaner module, cleans the file and preps it for the sorting module.
	sleep 1
	./FileSorter #Runs the FileSorter Module, sorts the contents of the file in alphabetical order. 
	sleep 1
	printf 'Output file is TempFiles/Sorted.txt'
	sleep 1
	./FileAnalyser # Runs the FileAnalyzer Module, allows for analysis of the final output


elif [ $x = 'V' ] || [ $x = 'v' ]; then
	# creating garbage file
	printf "\n"
	printf "Creating silly garbage file!"
	printf "\n"
	sleep 4
	#running GarbageGen
	./GarbageGen
	# shows garbage file
	sleep 4
	more TempFiles/Junk.txt # displying the output of GarbageGen
	./Div
	# running FileCleaner to clean the file
	printf "\n"
	printf " [*] Cleaning GarbageFile"
	printf "\n"
	sleep 4
	printf "\n"
	#running file cleaner
	./FileCleaner
	printf "\n"
	sleep 4
	more TempFiles/Clean.txt #Displaying the output of FileCleaner
	./Div
	# sorting garbage file
	printf "\n"
	printf " [*] Sorting The File"
	printf "\n"
	sleep 4
	echo
	./FileSorter
	sleep 4
	echo
	more TempFiles/Sorted.txt #Displaying the output of FileSorter, the final output of this program
	./Div
	echo
	sleep 4
	printf " [+] Script complete"
	printf "\n"
	printf ' [+] Output file is TempFiles/Sorted.txt'
	sleep 1
	./FileAnalyser
else
	echo $x  ": Expected S/s or V/v"

fi
