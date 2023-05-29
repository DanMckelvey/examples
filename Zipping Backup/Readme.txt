This is taken from a larger backup script which saves specefic datasets in a .gdb
Due to a change in storage location, it was advised that all files should be saved as zip files.

The zipGDB Function takes the created .gdb file and compresss it into a .zip file
Line 7 makes sure that if there is a .lock file in the gdb, that it is not saved.



The delete_zip function is used for cleaning the backup folder of any older backups.
line 15 - 19 reference config, which is the configuration file.
This file lets us easily control how long, and which backups we should keep or delete.

The function is setup so that it iterates through every file in the folder, and proceeeds with only zip files and the correct date format
Based on the date of the zip file, and how the configuration file is setup, it checks if it should be removed.
The try except block allow the script to coninue iterating throught the folder when an error occurs.

Common errors are caused by permission issues with some folders created by other users.
