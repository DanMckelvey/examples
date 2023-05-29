This subroutine was created for a specefic data upload essential for various financial reports
The data upload subroutine (importCFSData on line 100) requires the data to be in a specedic format.
The need for this addition was that the source data changed their export.
The changes included a different data format, column position changes, line break changes, and comma deliminated instead of tab.

The subroutine uses a user inputed date to delete all data that would be repeated in the next upload, then uploads data from the file.

To get the data in the right format, I created two workbooks, and copy only the required data over in the right positions.
Then I use a different funciton I created (ReplaceWith), which opens the file and replaces the windows line break (CrLf) with the Unix line break (Lf).
Using the same function, I replace the commas with tabs.
Lastly I iterate through the months of the year to change teh date from YY-Mon to Mon-YY.
