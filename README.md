# Linux Backup Automation Project


<br/>
# Screenshot
<img src="/Screenshots/linux-final-project.png" alt="inux-final-project.png" style="height: 100%; width:100%;"/>
<br/>

This script is a backup utility that takes in two command-line arguments: a target directory and a destination directory. 

- The script starts by checking if the number of arguments passed is correct, which should be exactly 2. 
  - If the number of arguments is incorrect, the script will print an error message and exit.
- The script then checks if the directories provided as arguments are valid directories. 
  - If either of the arguments provided is not a valid directory, the script will print an error message and exit.
- The script then assigns the first argument to a variable named 'targetDirectory' and the second argument to a variable named 'destinationDirectory'. 
  - It then proceeds to print the value of these two variables to the console, so the user can confirm that the correct directories were provided as arguments.
- The script then takes the current timestamp using the command `date +%s` and assigns it to a variable named 'currentTS'. 
  - This timestamp will be used to create a unique name for the backup file.
- The script then creates a backup file name using the format "backup-timestamp.tar.gz" and assigns this to a variable named 'backupFileName'.
- The script then defines some useful variables such as 'origAbsPath' and 'destDirAbsPath' which are used to store the absolute path of the target directory and destination directory respectively. 
  - And then it change to Target directory and check whether modified files are greater than 24 hours old and added into an array called 'toBackup'
- Finally, the script compresses the files in the 'toBackup' array into a .tar.gz file with the name 'backupFileName' and moves this file to the destination directory. 
- The script ends with the message "Congratulations! You completed the final project for this course!"

