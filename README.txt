To run this application properly you must perform prep steps...

1.  Run the "deletes" extract in your RBX,
2.  Double click the FTP... icon, that's in this folder - Each and every time,
3.  Then open the Check Delete Batches application...

If you don't perform steps one and two then step three will be corrupted to some degree.

Corruptions include but are not reserved to...

	- filtering/displaying old data,
	- if the initial window doesn't provide data then the "filter" button will cause an error...  
	  This isn't a problem because it's simply caused by data not being present,
	- 

IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!
IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!  IMPORTANT!!!

The FTP file contains hard coded information.

You need to right click on the ftp file or its shortcut... select edit and change one line.

The following is how it reads currently, without being changed...
##########################################

%windir%\system32\ftp.exe -s:"%~f0"
open MWxxx
rbxusr
111111
hash
binary
cd /usr/acct/rbx/host/gencomm
lcd %cd%
get HSdeletes
delete HSdeletes
bye
:done
@echo off
cls
exit

##########################################
The line that needs to be changed is the second one.  It currently reads "open MWxxx" but you should change the 
xxx to read you store abbreviation. 

