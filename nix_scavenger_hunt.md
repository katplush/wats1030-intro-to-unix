# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:* **C:/Users/Katerina/suCode/wats1030-intro-to-unix**
* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?* **LICENSE  challenge_files nix_scavenger_hunt_stretch.md README.md  nix_scavenger_hunt.md  super_scavengers.md**
* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?* **More detail is provided about the files ie. time and date**
* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*  **`-a` with ls will display all entries and not ignore entries starting with `.` .`l` will list in long format. `h` will print sizes in human readable format.**
* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*  **LICENSE.txt bin  dev  git-bash.exe  mingw64  tmpunins001.exe  usr  ReleaseNotes.html  cmd  etc  git-cmd.exe   proc      unins001.dat  unins001.msg**
* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*  **`/`**
* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*  **/c/Users/Katerina**
* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*  **3**
* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?* **~/suCode/wats1030-intro-to-unix**
* Press the up arrow on your keyboard. *What just happened?* **Auto generated a `cd ..`**
* Press the up arrow a few more times. *What do you see?*  **The program runs through a bunch of command options.**
* Run the `history` command. *What do you see?* **A list of every command I've ever excuted.**

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*  **Katerina**
* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:* **No one else showed up.**
* How long has your system been running? Use `uptime` to see, and *paste the result here:* **`uptime` command did not work with git bash.  Used `systeminfo` command to see System Boot Time: 1/19/2019, 8:13:14 AM.  Not sure if this is the same information I would get with `uptime`.**
* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*  **Displays information about a selection of the active processes. Result:  PID PPID PGID WINPID TTY UID STIME COMMAND** **Not sure what all this means**
* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?* **bash: top: command not found**

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?* **2**
* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*  **bash: more: command not found**
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*  
**$ ps aux | grep <Katerina>** 
**bash: syntax error near unexpected token `newline'**
