## Basic Commands in Linux

(1) Present working directory:

ubuntu@dheen:~\$ pwd

= /home/upuntu

Version:

ubuntu@dheen:~\$ uname -a

= version will appear

- Username:

ubuntu@dheen:~\$ whoami

= uopuntu

- (4) Clearing the screen:

ubuntu@dheen:~\$ clear

(ctrl +L)

= Terminal will be cleared.

(5) Viewing command history:

ubuntu@dheen:~\$ history

= Total history can be viewed.


## Creating Directory and Files in Linux

(1) Make directory:

ubuntu@dheen:~\$ mkdir data

- = Data file will be created.

- (2) Entering into a directory:

- = We will be enter into ‘data’ file.

- € Creating a text file:

- = “hello” text file will be created.

## Text file creation

- = In the editor, you have to give “i” for inserting a text.

- = Enter some text.

- = Give Escape button.

- = Forsavingafile = :wq — save

- (4) List of files:

ubuntu@dheen:~/data\$ 1s

= hello.txt.


## (5) Quit file without saving:

- In the editor — give Escape.

## Installing a package: (Linux)

ubuntu@dheen:~/data\$ sudo apt-get install vim

sudo = root user

apt-get = getting any application

vim = upgrading vi editor

## Auto-completing a command:

- Press Tab for auto-complete a file.

- (If we create two or more files).

## In data directory:


## (6) Nano Text Editor:

ubuntu@dheen:~/data\$ nano test.txt

ubuntu@dheen:~/data\$ ls

= Htest.py hello.txt hellol hello.ho test.txt

- Nano editor is simple, easy to use.

## (7) Creating a dummy file:

ubuntu@dheen:~/data\$ touch foo.txt

(After Is)

hello.txt hellol

= Htest.py

foo.txt test.txt

## (8) File manipulation: ®

- remove (deleting) a file: v/

ubuntu@dheen:~/data\$ rm foo.txt

(After Is)

= Htest.py hello.txt hellol test.txt

ubuntu@dheen:~/data\$ 1s *.txt

= hello.txt test.txt

ubuntu@dheen:~/data\$ ls he*

= hello.txt hellol

ubuntu@dheen:~/data\$ rm *

= Total files be deleted.


## Viewing and Copying a File

ubuntu@dheen:~/data\$ vi hello.txt

(hello.txt will some text is created).

Displaying content in command prompt:

ubuntu@dheen:~/data\$ cat hello.txt

= This is a file that is created.

## Copying a file: ®

~/data\$ cp hello.txt new-hello.txt

~/data\$ 1s

= hello.txt

Renaming a file: ®

~/data\$ hello.txt demo.txt

mv

~/data\$ 1s

= demo.txt

~/data\$ cat demo.txt

= This is a file that is created.

new-hello.txt

new-hello.txt

// cat

// cp

// mv


(4) Copying a file with ‘cat’ command:

Append symbol (>>):

ubuntu@dheen:~/data\$ cat demo.txt >> nfile.txt

(After ls)

= demo.txt

new-hello.txt

nfile.txt

(Copies the text from one file to another).


## File Navigation System

## 1. ls and cd commands:

## 3. Going Back from a directory:

## 4. Copying a file with ‘cat’ command:

Append symbol (>>):


## List Functionalities: (ls)

(1) Basic Is command:

ubuntu@dheen:~\$ 1s

abc

airflow

data

## (2) ls options:

print_time.py

hadoop2-din

| Option | Description |
| --- | --- |
| -1 | long list format |
| -s | shows file size in blocks |
| -t | sorts by modification time (newest first) |
| 5 | reverses the sorting order |
|   | sorts by file size (largest first) |

## ubuntu@dheen:~\$ 1s -lstrS

Output => total 885076

404908

ubuntu

May 31

abc

ubuntu

1

-rw-r--r--

189406

drwxr-xr-x

3

1414

logs

ubuntu

## (3) Is -a (shows hidden files):

ubuntu@dheen:~\$ 1s -a

(shows the hidden files)

bash-history

.bashrc

data

abc

Note:

- a option shows hidden files (files starting with dot “.”)

- Without -a, hidden files are not shown.

ubuntu

501

Jun 10

print_time.py

hadoop2-din

| Hidden files | Description |
| --- | --- |
| .bash_history | Bash command history |
| | |   |
|   | User profile settings |
| print_time.py | Python file (visible file) |
| .bashrc | Bash configuration file |
| data.log | Log file (visible file) |
| hadoop2-din | Directory (visible) |


## (4] .bashrc file usage

- = In .bashrc file, if we install any Python on Java we will give environment variables in it.

## Opening .bashrc file:

ubuntu@dheen:~\$ vi .bashrc

## Executing .bashrc file:

(1)

ubuntu@dheen:~\$ source .bashrc

[2]

ubuntu@dheen:~\$

.bashrc

.

List manipulations (cont.):

[1]

1s * .py

= print_time.py

(2

:~\$ ls data

= data.log

data

4

Note:

«is a wildcard.

®

« matches zero or more characters.

## List manipulations (cont.):

:~\$ 1s * .py

= print_time.py

2)

:~\$ ls datax

= data.log

data


## Hardlink and Softlink

## 1. Create a file:

:~\$ echo "hello linux" >> original.txt

:~\$ cat original.txt

= hello linux

:~\$ ls

-lstr

= total 4

4 -rw-r-—-r-- 1 ubuntu Jan 9 original.txt

\# write content

\# view content

\# list with details

## 2. Hardlink:

:~\$ ln original.txt team2-data.txt

:~\$ ls -lstr

= Total 8

-rw-r—r-- 2

4

4

\# create hardlink

\# list with details

ubuntu

ubuntu

2

## 3. Softlink (Symbolic link):

:~\$ ln -s original.txt new-data.txt

ls -lstr

= Total 4

ubuntu

4

1

-rw-r--r--

ubuntu

lrwxrwxrwx

1

0

\# create softlink

{ but (In copy gitlab file i deleted didn't original get deleted) file

\# list with details

......

new-data.txt -> original.txt

......

## Important Notes:

- \* If we update in one file, it also update another but if we delete source file, child fil also be deleted

- \* Hardlink and Softlink are useful for backup, sharing files, and saving space.

## Quick Summary

- Hardlink — points to the same data (same inode). Deleting one name does not delete the data.

- Softlink — points to the path of the original file. Deleting original file breaks the link.


## Background run & process monitor

```
import time
```

Running a program / command in the background without stopping the terminal.

L

```
b=5
while True:
a+=b
```

For every 3 seconds, a value will be printed.

```
print(f"Updated value of a: {a}")
```

)

```
time.sleep(3)
```

## Running Python in background

\# Create / edit Python file |

:~\$ vi data.py

:~\$ python3 data.py &

\# Run in background

| @ Python3 installed by will default be

|

|

|

|

in Linux.

## Output:

Updated value of a: 5

Updated value of a: 10

## EE

- e If we run this line (command), it will print the values of output, but it is not permanent.

- e If we close the Linux system (or) if someone stops the environment run, it will be deleted .

- e The process will stop and will be deleted, we have to run every time.

Is

\


(2) nohup command:

(3) Rack gl

(top

ny

)

- = All running applications will be displayed in the task manager.

(4) Process status: (ps)

= Shows current running processes.

(5) Detailed status:

(

:~\$ ps

-aux

[oem Jee

[en se]

00:00

start time

python3

## (5) Killing the run:

(

i~\$ kill -9

115966

{

kill forcefully.

A Note:

kill -9 sends SIGKILL signal and stops the process

immediately.

( PID of the file ) ]

-> command being executed

data-processing.log

argument / file name

- a = show process from all users

- u > show the user who owns the process

- Xx => show processes attached to terminal

Q Tip:

- nohup command allows the process to continue running even after logout.

- \* Use & to run process in background and save output to a file.


## Downloading Image (or) File from internet

wget

## Example:

= Copy the link of the image in website

:~\$ wget "https://........

1s

i

=

po

oa ?

\# wget

- \* This command downloads the file from the given URL and saves it in the current directory.

I

- For normal command, we have to give repeated the same path and same command.

it will become simpler.

= If we use “Alias”

## Example:

= alias dheen='cd /home/ubuntu/abc..... ']

dheen

= It will go to the path directly.

- If we want to use Alias name permanently, we have to save it in “bashrc” file and to execute it.

## \* Summary:

- wget => Download file from internet using URL.

- alias = Shortcut for long command or path.

- Temporary alias Works only in current terminal session.

- Permanent alias — Save in ~/.bashrc and execute.

- \* Alias is a shortcut for a command or path.

- « It saves time and makes work easier.

]

@ How to make Alias permanent?

- 1. Open the file

- 2. Add alias at the end of the file

( alias dheen='cd /home/ubuntu/abc.....

- 3. Save and close the file.

- 4. Execute the file to apply changes

J

[:~s source ~/.bashrc

- 5. Now alias name can be used anywhere.


## Data - Management

## Disk free-space:

- = df — disk

- = -h — human readable format

- = Shows file-system disk space usage.

| File-system | Size | Used | Mounted on |
| --- | --- | --- | --- |
| /dev/nvmeOn1p2 | 8.9G | 4.0K | / (root) |

## © Particular file usage:

:~\$ du -sh scripts/

= du — disk usage

= -sh — summary / human-readable

- = Shows total size of “scripts/” directory.

= 12K scripts/

\# du -sh

## RAM - usage:

## @ Free-up cache:

## What it does:

- \* sync = flushes all file system buffers to disk.

- \* echo 3 > /proc/sys/vm/drop_caches — clears pagecache, dentries and inodes.

—

- =» Shoes disk: space usage in

- Use df -h to check disk space.

- du -sh <dir/file> — Shows total size of a directory/file.

- Use du -sh to check size of a file or directory.

- o free -m / free -g = S RAM a MB B. in

- ® Use free -m or free -g to check RAM usage.

- Clear cache only if system is slow due to memory, pressure.

- \* sudo sh -c "sync; echo 3 > /proc/sys/vm/drop_caches” — Frees up memory cache.

)


## Zip and Unzipping a File


## GREP - Advanced Usage


## SECURE SHELL (SSH)

% Used to connect one server to another server.

(We can connect our friend's Ubuntu system with our server using SSH)

- (1) Installation:

(

:~\$ sudo apt-get install openssh-server

(SSH will be installed)

:~\$ sudo apt-get update openssh-server

(Updates the SSH)

( :~\$

ifconfig — command gives details about our server.

- 2) Entering into another server: v/

[+s ssh

\* after password, we can login into our friend's system.

- 3) Login using user-name:

:~\$ ssh ubuntu@dheen

(Login to user ubuntu whose name is dheen)

\# openssh-server

(

## install

J

]

J

(IP also) v/

]

192.20.124.118

## Tips:

- \+ SSH uses port 22 by default.

- \+ Make sure SSH service is running on both systems.

- Use ifconfig / ip a to get IP.

## SECURE COPY (SCP)

- % Used to one file to another server. copy

- From server to server copying.

scp <source_file> <user>@<ip>xdestination_path>

J

(with host name):

hy buntu/copy. bile

\# scp (secure copy)

## Example:

(

scp /h b logs/ job.bile

(It will ask password ond it will copy)

with IP):

: <destination_path>

<source_file> <user>@<hostname>

| No. | Command | Description | Example / Output | Tag |
| --- | --- | --- | --- | --- |
|   | scp (copy file) | Copy file from local to remote | scp file. txt ubuntu@server: /home/ubuntu/ |   | # copy file |
|   | scp (copy directory) | Copy directory from local to remote| scp -r dirl ubuntu@server:/home/ubuntu/ |   | # copy directory |
|   | scp (remote to local) | Copy file from remote to local | ubuntu@server: /home/ubuntu/file. txt ./ | # download file |
| scp (remote to local dir) | Copy directory from remote to local | scp -r ubuntu@server: /home/ubuntu/dirl |   |   | ./ | # download directory |

## SO

recursive (for directory)

copy

-P <port> : specify port (default 22)

compress data while copying

:

: preserve file permissions, time etc.

## Important: Notes

- \+ SCP uses SSH, so authentication is required.

- \+ Make sure the remote path and file name are correct.

- \+ Use -r option when copying directories.


|

(1)

find

## FIND COMMAND

Used to find a file.

\# find

--name

-name logl.txt

.

\# find

--name

(finds the file with name)

©

|

\# --name "*.txt"

(find the file that ends with ".txt")

(find

|

-type f -size +10M

.

\# --type

-size

(type with file, size with >10MB)

\# --mtime

(finds the file that are created within 1 day)

|

find

-empty

.

\# --empty

(finds the empty file in whole system)

(6)

]

| find

-name "*.tmp"

-delete

.

\# --name "*.tmp" -delete

(deletes the file that ends with .tmp)

Find

Feature

grep

Searches

Files and directories

Text inside files

Searching for matching lines

Locating files by name,

Used for

(content) inside files.

size, type, time etc.

Filesystem level

Search level

File content level

Example

-name logl.txt

grep "ERROR" logl.txt

find

.

## Common find Options

find . -name "*.txt"

-name PATTERN : search by name

= find all .txt files

file (f) or directory (d)

/ d

:

find .

-type f -size +10M

«

-size +10M / -10M : size greater than / less than

find files larger than 10MB

modified within 1 day

-mtime -1

find .

-empty

:

— find empty files

find empty files/directories

:

-delete

¢

delete matched files

delete all .tmp files

## Notes:

- \+ The dot (.) means current directory. Use / for root directory.

- You can combine multiple options with find for advanced searches.

- Be careful with -delete option.

- Use man find to see all available options.

|

|


## AWK (Command-line Tool)

AWK: (Alfred, Weinberger, Kernighan)

\* Processing columns in text.

% Performs calculations.

% Extract and format data from files.

a file

:~\$ vi data.txt

Developer

John

25

Asha

Designer

30

:~\$ cat data.txt

Ravi

& = awk ‘{print \$0}' data. txt |

Developer

John

25

=

Asha

Designer

(same output will appear)

Ravi

awk ‘{print \$1}’ data txt |

John

=

Asha

(column 1 data will be printed)

Ravi

awk ‘{print \$1 , \$3}’ data. txt |

Developer

Designer

(column 1 and column 3 data will be printed)

Tester

Common awk Print Variables

|

delim

|

Entire line

voi

\$1, \$2, \$3, ... | Fields (columns) of the line

—

|

— —

BEGIN { | Execute before reading input

1

Current line number

EE I

|

Execute after reading input

Current line number in the current file

...}

|

|

|

28

Tester

|

awk

30

28

Tester

("2 ]

‘print \$1’

Ed

(5 ]

‘print \$1 ,

=

\$0

Set field

separator

(delimiter)

16

NF

NR

FNR

## Notes:

- \+ Default field separator is any space or tab.

- \+ Columns in data are separated by space or tab.

- \+ Use quotes around awk programs: '{ .

- \+ Very useful for text processing, data extraction and calculations.


## awk [options] ‘pattern input-file > output-file

awk

— Starts the AWK text-processing program.

[options]

Control AWK behaviour (e.g., set field separator).

pattern

— Specifies which lines to process.

{action}

— Defines what to do with matching lines (usually print).

input-file

File that awk reads line by line.

\> output-file — Redirects processed output into a file.

## Notes:

- Default field separator is any space or tab.

- Columns in data are separated by space or tab.

- Use quotes around awk programs: ‘{ }'.

- Very useful for text p "9, data


- = If we have to change the mode for any one to read - , write and execute , we use chmod.

- = Permission based command.

Who it is

User

The user who owns the file.

2 Group

Members of the file's group.

-

=

Everyone else (excluding owner ard group).

Others

=

Root

## Example:

-

The superuser - not affected by regular file permission.

drwx

n-x

n-x

(User , group , others)

rwx —> read write , execute. ,

## chmod Nu ic Notation

| Permission | Symbol | | | Value |
| --- | --- | --- | --- |
|   | | |   |   |
| Read (r) |   |   | 4 |
| Write (w) |   |   | — 2 |
|   | w | |   |   |
| Execute (x) | x |   | 1 |
|   | | |   |   |
|   | 1 |   |   |
| No Permission ( -) | - | |   | 0 |

+1

6

+1 =5

+0

4

+1

+0=0

## [ notes |

- \+ chmod changes the permission (mode) of files and directories.

- \+ Use numeric mode (e.g., 755) or symbolic mode

- « Root user can override permissions.

- \+ Be careful while using chmod -R on directories.

## Common chmod Exampl

~~ —

chmod 755 file.sh

rwxr-xr-x

chmod 644 file.txt

chmod 700 script.sh

chmod -R 755 dir/

=>

(file.sh)

(file.txt)

rw-r--r--

=

rwx------

Apply recursively 755 to all files

(script.sh)

in directory

J

|


## GRANTING PERMISSION TO A FILE

| | Permission | Symbol | Value |
| --- | --- | --- |
| Read | I |   |
|   |   | 4 v |
| Write | [| | | 2 v | |
| Execute |   | 1 v |

- @ For (read + write + Execute) = 4 +2 +1 = 7.

- @ For No permission = 0.

(directory)

dummy

= drwxr-xr-x

(file)

script.sh

2 -rw-r--r--

## A For files:

(1)

rwxrwxrwx script.sh (fu

.

chmod 755 script : .sh | = 755

e

-rwxr-xr-x script.sh

{

chmod 777 script.sh

i

<<

|

I access)

rwx

|

Corer)

i

i

## For directories:

(1) (

chmod -R 777 dummy

drwxrwxrwx dummy (full access)

|

drwxr-xr-x

| —

d

rwx

r-x

others

type

group

user

\# chmod [number] filename —

H

777

full

read + write + execute

|

acess

rwx

rwx

| H

(others)

I

(Recursive)

-R

Apply the permission to the directory and all #s contents (files and subdirectories) recursively.

J

## [ Tips |

- Use ls -l to see current permissions.

- « chmod changes the mode (permission) of files ond directories. " 2

- Use numeric mode (e.g., 755) or symbolic mode utx, gw).

- \* Be careful while using -R on directories.

- « Root user can override permissions.
