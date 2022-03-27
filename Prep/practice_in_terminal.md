## prep: practice in the terminal

- **The command line:**

the command line is the terminal which we can open more than one tab and run multiple commands which makes it very practical.
the order of the command lines is as follows:
first comes the prompt, then the command itself and lastly the arguments all seperated with spaces, there are alsi something called options which are used to modify the commands and come before the argument usually starting with "-"
, after the command line comes the output that could not appear sometimes unless with an error. after the command run we should see the prompt again.
you.

- **Basic navigation:**


the first command here is (pwd) which means Print Working Directory, it gives you the exact path you're in
(ls) used to show the list of files/directories you have at this path, if we want a long listing we add an option (-l)
if we used (/etc) as an option it shows us the list the inside directories content.
(cd) is the command resposible for moving around in the system, it changes the directory when you folllow it by its name, if you ran cd alone you will be at home.

- **More about files:**


*surprisingly* everyhting is a file, and linux can know file type through its content without the need of extenions, by running (file [path]), linux is case sesitive, and to spaces in files names.
using quotes or escape characters can give a valid output when having spacing in names.
whenever we start naming a file with (.) its hidden by default, to show them run (ls -a)

- **Manual pages:**


they are pages that contain all the commands in the system and their functionalities, manual pages are shown by running (man<command name>),
if you want to search on the command effect you should use (man -k <search>), to select the next found item (n) ,to exit press q.
longhand commands begin with -- such as --a to find hidden files, and shorthand commands start with one dash - such as -a to find all files. 

- **File manipulation:**
  
  
refering to a file or directory is refering to a path.
to create new directory run (mkdir <name>)
to remove one use (rmdir <name>)
to create a blank file (touch)
to copy a file (cp)
to move a file (mv)
to delete a file use (rm <name>)

- **Cheat sheet:**
  
  
everything is explained above.
