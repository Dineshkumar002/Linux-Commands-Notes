Basic Commands in Linux SS Ee 2 

1) Present working directory: 

ubuntu@dheen:~$ pwd 

=> /home/uountu 

2) Version: 

ubuntu@dheen:~$ uname -a 

=> version will appear 

B&B Username: 

ubuntu@dheen:~$ whoami 

=> uountu 

4) Clearing the screen: ubuntu@dheen:~$ clear (ctrl+ L) = Terminal will be cleared. 

5] Viewing command history: 

ubuntu@dheen:~$ history 

= Total history can be viewed. 

###### Creating Directory and Files in Linux 

———EEEEss e —— 

@ Make directory: 

ubuntu@dheen:~$ mkdir data 

=> Data file will be created. 

& Entering into a directory: 

ubuntu@dheen:~$ cd data/ 

= Wewill be enter into ‘data’ file. 

& Creating a text file: 

ubuntu@dheen:~/data$ vi hello 

=> “hello” text file will be created. 

Text file creation 

= Inthe editor, you have to give “i” for inserting a text. 

= Enter some text. 

= Give Escape button. 

=> Forsavingafile => :wq — save > :q > quit 

0 List of files: 

ubuntu@dheen:~/data$ 1s 

=> hello.txt. 

#### 5) Quit file without saving: 

e In the editor > give Escape. 

:q! 

Installing a package: (Linux) 

ubuntu@dheen:~/data$ sudo apt-get install vim 

sudo = root user apt-get = getting any application vim = upgrading vi editor 

###### Auto-completing a command: 

e Press Tab for auto-complete a file. 

¢ (If we create two or more files). 

###### In data directory: 

hello. txt hello1 hello.py e If we give => vi hello - output > hello.txt hello1 hello.py e If we give => viP hello - output => hello.txt hello.py e If we give => VP hello - output => hello.txt hello.py 

###### 6) Nano Text Editor: 

ubuntu@dheen:~/data$ nano test.txt 

ubuntu@dheen:~/data$ ls => Htest.py hello.txt hellol hello.ho test.txt e Nano editor is simple, easy to use. 



<!-- Start of picture text -->
7) Creating a dummy file:<br><!-- End of picture text -->

ubuntu@dheen:~/data$ touch foo.txt 

(After Is) 

=> Htest.py hello.txt hellol foo.txt test.txt 

8) File manipulation: () ¢ remove (deleting) a file: Y 

1) ubuntu@dheen:~/data$ rm foo.txt 

(After Is) => Htest.py hello.txt hellol test.txt 

2) ubuntu@dheen:~/data$ Is *.txt = hello.txt test.txt 

3) ubuntu@dheen:~/data$ 1s he* = hello.txt hello1 

4) ubuntu@dheen:~/data$ rm * => Total files be deleted. 

###### Viewing and Copyinga File 

ns e ————E 

ubuntu@dheen:~/data$ vi hello.txt 

(hello.txt will some text is created). 

i) Displaying content in command prompt: 

ubuntu@dheen:~/data$ cat hello.txt // cat 

=> This is a file that is created. 

2) Copying a file: (3) ~/data$ cp hello.txt new-hello.txt ~/data$ 1s => hello.txt new-hello.txt 



<!-- Start of picture text -->
//cp<br><!-- End of picture text -->

3) Renaminga file: ®) ~/data$ mv hello.txt demo.txt // mv ~/data$ 1s => demo.txt new-hello.txt ~/data$ cat demo.txt => This is a file that is created. 

###### 4) Copying a file with ‘cat’ command: 

Append symbol ( >> ) : 

ubuntu@dheen:~/data$ cat demo.txt >> nfile.txt 

(After ls) 

= demo.txt new-hello.txt nfile.txt 

(Copies the text from one file to another). 

5) Printing texts in prompt: 1) ~/data$ echo "dheen" // echo => dheen 

2) ~/data$ echo "dheen" >> nfile.txt // store in file (The text will be stored in file). 

©) ~/data$ echo "mohamed" >> nfile.txt ~/data$ cat nfile.txt 

// append in file 



<!-- Start of picture text -->
= This is a file that is created<br>dheen<br>mohamed<br><!-- End of picture text -->

22-02-2026 



<!-- Start of picture text -->
File¢ Navigation° . System<br><!-- End of picture text -->

###### 1. ls and cd commands: 

ubuntu@dheen:~$ ls 

=> untitled.pnb data print_time.py airflow data. log retal.txt 

###### Shortcut for “home/ubuntu”: 

Shortcut for “home/ubuntu”: 2. Creating nested Directory: ubuntu@dheen:~$ cd data/ If we want to create directory (or) file in the file that doesn’t exist (or) created ubuntu@dheen:~/data$ data. log log * we have to create it one by one into a file. No such file directory « Instead we use "-p". 

ubuntu@dheen:~/data$ data. log log 

* No such file directory :~/data $ cd. N ~ Home directory :~$ vi data.log > cd ~ 

ibanei@dhesn:=sigwa /* Hp /home/ubuntu ubuntu@dheen:@ ~$ nkdir[-p] abc/test/demo(-r] / / ~$ cd abc/ ~$ ls 5 pest 

Give > “This is a log file” and save it. => :~$ cd data/ 

:~/data $ cd .. :~$ cd data (home/ubuntu/data. log ) “This is a log file” * => :~/data ~ /data.log (/~) "This is a log file”. 

###### 3. Going Back from a directory: 

###### 4. Copying a file with ‘cat’ command: 

ubuntu@dheen:~$ cd abc/test/demo ubuntu@dheen:~$ pwd 

Append symbol ( >> ) : 

ubuntu@dheen:~/data$ cat demo.txt >> nfile.txt ubuntu@dheen:~$ pwd (After Is) => demo.txt new-hello.txt nfile.txt /home/ubuntu/abc/test/demo (Copies the text from one file to another). 

ubuntu@dheen:~$ cd .. (home/ubuntu/abc/test) 

###### 5. Printing texts in prompt: 

@ ~ /data$ echo "“dheen” // echo ubuntu@dheen:~$ cd ../.. — (home/ubuntu) => dheen @ ~ /data$ echo "dheen” >> nfile.txt // store in file ubuntu@dheen:~$ cd - (will go to previous cd command) (The text will be stored in file). /home/ubuntu/abc/test ® ~ /data$ /data$ echo “mohamed” >> nfile.txt // append 

® ~ /data$ /data$ echo “mohamed” >> nfile.txt // append in file ~ /data$ cat nfile.txt => This is a file that is created dheen mohamed 

10/03/2026 

List° Functionalities:. int (ls) 

###### 1) Basic ls command: 

ubuntu@dheen:~$ 1s 

abc data. log print_time.py airflow data hadoop2-din 

###### 2) ls options: 

|-1|long list format|
|---|---|
|-s|shows file size in blocks|
|-t|sorts by modification time (newest first)|
|-r|reverses the sorting order|
|-S|sortsbyfilesize(largestfirst)|



ubuntu@dheen:~$ 1s -lstrS Output => total 885076 404908 -rw-r--r-1 ubuntu ubuntu 1414 May 31 abc 189406 = drwxr-xr-x 3 ubuntu) ubuntu 501 Jun 10 logs 

###### 3) 

###### ls -a (shows hidden files): 

ubuntu@dheen:~$ ls -a (shows the hidden files) . bash-history «profile print_time.py . -bashre data. log hadoop2-din abe data . 

% Note: ¢ -a option shows hidden files (files starting with dot “.”) e Without -a, hidden files are not shown. 

|. bash_history|Bash command history|
|---|---|
|«profile|User profile settings|
|print_time.py|Python file (visible file)|
|-bashre|Bash configuration file|
|data.log|Log file (visible file)|
|hadoop2-din|Directory(visible)|



###### 4) -bashrc file usage 

=> In .bashrc file, if we install any Python on Java we will give environment variables in it. 

Opening .bashrc file: 

ubuntu@dheen:~$ vi .bashre 

Executing .bashrc file: 

@ ubuntu@dheen:~$ source .bashrc 2) ubuntu@dheen:~$ . .bashrc 

###### 53) List manipulations 

manipulations | ls command: ubuntu@dheen:~$ ls data. log log print_time.py airflow data hadoop options: Option Description | -1 long list format -s shows file size in blocks -t sorts by modification time (newest first) aid reverses the sorting order | s sorts by file size (largest first) 

e Basic ls command: 

ubuntu@dheen:~$ ls 

abc data. log log print_time.py airflow data hadoop 

###### 2) List options: 

###### Option Description 

ubuntu@dheen:~$ 



<!-- Start of picture text -->
ls -LstrS<br><!-- End of picture text -->



<!-- Start of picture text -->
List manipulations (cont.):<br>e i~$ ls * .py<br>=> print_time.py<br><!-- End of picture text -->



<!-- Start of picture text -->
i?) i~$ Is datax<br>=> data.log data<br><!-- End of picture text -->



<!-- Start of picture text -->
Bs Note:<br>e * is a wildcard.<br>@ * matches zero or more characters.<br><!-- End of picture text -->



<!-- Start of picture text -->
List manipulations (cont.):<br><!-- End of picture text -->



<!-- Start of picture text -->
1) i~$ ls * .py<br><!-- End of picture text -->



<!-- Start of picture text -->
=> print_time.py<br><!-- End of picture text -->

Output => total 885076 404908 = -rw-r--r-1° ubuntu ubuntu 1414 May 31 abc 189406 drwxr-xr-x 3 ubuntu ubuntu 501 Jun 10 logs 

ten 



<!-- Start of picture text -->
(2) i~$ ls data<br><!-- End of picture text -->

=> data.log data 



<!-- Start of picture text -->
|<br>Hidden File / Item Description<br><!-- End of picture text -->

###### (3)<sup>ls-a(showshiddenfiles):</sup> 

ubuntu@dheen:~$ ls -a (shows the hidden files) : bash_history -profile print_time.py ee -bashre data. log hadoop2-din abe data . 



<!-- Start of picture text -->
-bash_histeer Bashcobb helaid histacini<br>-profile User profile settings<br>print_time.py Python file (visible file)<br>zhashre Bash, configuration file<br>data. log Log file (visible file)<br>| hadoop2-din Directory (visible)<br><!-- End of picture text -->

###### Hardlink and Softlink 

———— 

###### 1. Create a file: 

:~$ echo “hello Linux" >> original.txt 

# write content 

:~$ cat original.txt 

# view content 

=> hello Linux 

:~$ ls -lstr 

# list with details 

=> total 4 

4 -rw-r--r-4 ubuntu Jan 9 original.txt 

###### 2. Hardlink: 

:~$ In original.txt team2-data.txt # create hardlink :~$ ls -lstr # list with details 

# list with details 

=> Total 8 

4 -rw-r--r-2 ubuntu seeeee team2-data.txt 4 -rw-r--r-2 ubuntu seeeee Original.txt 

{ey => If we update anything in "Original.txt”, it applies (also) on “team2-data.txt”. || => If we delete one file, another file will exist. ; 

i eee ee 

###### 3. Softlink (Symbolic link): 

:~$ In -s_ original.txt new-data.txt :~$ ls -lstr 

# create softlink 

# list with details Gn In gigitlabi deleted originaloriginal fifile but copy file didn’t get deleted) 

=> Total 4 

4 -rw-r--r-4 ubuntu ...... original.txt O lrwxrwxrwx 1 ubuntu ...... new-data.txt -> original.txt 

###### Important Notes: 

###### Hardlink vs Softlink 

aioe se teat| ia [a 

+f 

- Oak© Hardlink Sema—— points 

- © Hardlink Sema—— points to the same data (same inode). 

Deleting one name does not delete the data. 

- Softlink > points to the path of the original file. Deleting original file breaks the link. 

###### Background run & process monitor 

###### Background Run 

###### Example - Python code 

Running a program / command in the background without stopping the terminal. 

import time : a= rc . b=5 For every while;; True: a3 valueseconds,will at=b be printed. print(f"Updated value of a: {a}") \ 



<!-- Start of picture text -->
while;; True:<br>at=b<br><!-- End of picture text -->

print(f"Updated value of a: {a}") time.sleep(3) 

###### 1) Running Python in background 

:~$ vi data.py # Create / edit Python file :~$ python3 data.py & # Run in background 

"7 Python3 willbe '| installedin Linux. by default || 

Output: 

Updated value of a: 5 

Updated value of a: 10 

###### ye Remember: 

- ;: . - a — —_ —_ ay e If we run this line (command), it will printthe values of output, but it is not permanent. 

   - @ If we close the Linux system (or) if someone stopsenvironmentthe run, it will be deleted. 

   - @ The process will stop and will be deleted, we have to run every time. 

###### 2) nohup command: 



<!-- Start of picture text -->
:~$ nohup python3 data.py >> data. py. log (&)<br>J |<br>can't stop the run will be saved to<br><!-- End of picture text -->



<!-- Start of picture text -->
(7) Displaying the file (Running file):<br>@ | :-$ tail -F data-process.log # tail -f<br>=> It will give last 10 lines and displays<br><!-- End of picture text -->



<!-- Start of picture text -->
running file (live).<br><!-- End of picture text -->



<!-- Start of picture text -->
3) Background checker (top command):<br>i~$ to<br>[+<br><!-- End of picture text -->

=> All running applications will be displayed in the task manager. 



<!-- Start of picture text -->
PID | USER | ee | NI | nes | cpu | TIME+ |COMMAND<br>522 | deven | 20 | 0 j|}4681 i1 37.00 LL|=z0.3. | python3<br><!-- End of picture text -->

###### 4)<sup>Processstatus:(ps)</sup> 



<!-- Start of picture text -->
(2) >i~$It willtailgive-20lastdata-py.log20 lines (live).<br>OoNowe 1<br>* tail -f — follows the file and shows updates. |<br>* tail -n N > shows last N lines once. J<br><!-- End of picture text -->



<!-- Start of picture text -->
3) Killing the run:<br>i~$ kill -9 115966 (PID of the file )<br><!-- End of picture text -->



<!-- Start of picture text -->
kill forcefully.4<br><!-- End of picture text -->

###### => Shows current running processes. 



<!-- Start of picture text -->
kill -9 sends SIGKILL signal and stops the process<br>immediately.<br><!-- End of picture text -->

## wae| wer | wm | mato | 

###### | © Pattern matching: 



<!-- Start of picture text -->
i~$ ps -aux | grep data-processing.py<br>=> Twisted command (one command binds with another)<br>ps -aux I grep data-processing.py |<br>gives detailedt status gives onlytL the file<br>of all processes that is matching<br><!-- End of picture text -->

e Detailed ‘status: [is ps aux [ even: | eters [00 [03 | seat | 3700 > | s | 00:00 | pythons - 

00:00 > start time pinata 9 ii hg tied data-processing.log -> argument / file name 

###### SS)eet 

||Summary of Command<br><br>|s<br><br>|
|---|---|---|
|Command<br>|<br>'<br>|Purpose<br>|<br>'<br>|Example<br><br>|
|pohup|Run process in background<br>even after logout|nohup python3 data.py<br>>>data.py.log&|
|&<br><br>|Sendprocessto background<br>| <br>|wee<sup>&</sup>|
|| <br>top<br><br>|and save output<br>Displayallrunning<br><br><br>|top<br>|
|t<br>—_<br>pe<br><br><br><br>|<br>—<br>—<br>-<br>Show current running<br><br>|—_—_—<br>pe<br>|
|4<br><br>pone<br>| <br>|_|Processes<br> Bwde<br>all processes<br>||—<br>|
|tail -F<br>Vii<br>__|_<br>|Shave jast, 20: nes<br>(twaupdates)<br> <br>|tail-f file.log<br>—<br><br>|
|<br><br>tail<nN<br><br>|<br>Show lastN lines once<br><br>|tail-20 file.log<br>|
|| | | 1 9 pip<br>| <br>-—_—|tla proce<br><br>———|aussee<br>_———|
||<br>ps~aux | grep|<br>|<br>|<br>||Filter output based on<br>pattern (matching)|Ps aux<br>| grep<br>file_name|



- a > show process from all users u > show the user who owns the process 

- x > show processesattached to terminal 

a C6)<sup>Displayingthefilethatcontains(nohupoutputs):</sup> [[xt-$ catcat<sup>data.py-t08_]</sup> dati 

- as, Vi i iC) Tip: + nohup command allows the process to continue running | | even after logout. 

- * Use & to run process in background and save output to a file. | 

Downloading Image (or) File from internet ———————————————————— 0 

###### @ wget 

###### Example: 

- => Copy the link of the image in website 



<!-- Start of picture text -->
Copy the link of the image in website praponcnneecescennenenecccnneceteecneny@<br>:~$ wget "https://........" # wget 1' ? Notes:zs iH<br>| This command downloads the file t<br>: H the current directory. '<br>=> linux. jpg SSSee Oe<br><!-- End of picture text -->

Alias in Linux: / 

- 1) For normal command, we have to give repeated the same path and same command. 



<!-- Start of picture text -->
=> If we use “Alias” it will become simpler. H & Note:<br>' '<br>Example: H * Alias is a shortcut for a command '<br>| or path. {<br>:~$ alias dheen='cd /home/ubuntu/abc.....' © It saves time and makes work i<br>: easier. i<br>=> It will go to the path directly.<br>@ If we want to use Alias name permanently, | 1. Open the file '<br>we have to save it in “bashrc” file and ' [:-$ vi ~/.bashre | H<br>—S ' i<br>to execute it. 2. Add alias at the end of the file '<br>i alias dheen='cd /home/ubuntu/abc.....' '<br>Ht<br>H3. Save and close the file. H<br>! 4. Execute the file to apply changes !<br>H 5. Now alias name can be used anywhere.<br><!-- End of picture text -->

- Summary: 



<!-- Start of picture text -->
° wget > Download file from internet using URL.<br>* alias -> Shortcut for long command or path.<br>* Temporary alias > Works only in current terminal session.<br>* Permanent alias > Save in ~/.bashrc and execute.<br><!-- End of picture text -->

###### Data - Management 

$$$. 

###### e Disk free-space: 

i~$ df -h 

# dfaf -h 

=> df > disk 

=> -h — human readable format 

=> Shows file-system disk space usage. 

###### © Particular file usage: 

ra Ab 

:~$ du -sh_ scripts/ 

= du — disk usage 

=> -sh —> summary / human-readable 

=> Shows total size of “scripts/” directory. 

=> 12K — scripts/ 

###### RAM - usage: 

###### @ Display with mb/gb: X 

1 @ Free-up cache: 

> mb details | 

:~$ sudo sh -c “sync; echo 3> /proc/sys/vm/drop_caches” What it does: | 

| What it does: 

###### Quick Nee 

* df -h > Shows disk space usage in human readable format. 

* du -sh <dir/file> —> Shows total size of a directory/file. * free -m / free -g -> ShowsRAM usage in MB / GB. 

* sudo sh -c “sync; echo 3 > /proc/sys/vm/drop_caches” —> Frees up memory cache. 

«Use dF hicte disk space. 

* Use du -sh to check size of a file or directory. 

- ¢ Use free -m or free -g to checkRAM usage. 

- . , 

- * Clear cache only if system is slow due to memory, pressure. 

##### Zip and Unzipping a File a<sup>ee</sup> . 

=> “zip” and “unzip” commands. 

###### C1) Zipping a file: 



<!-- Start of picture text -->
:~$ zip file.zip scripts/<br>=> a CO<br>If zip is not installed.<br><!-- End of picture text -->

:~$ sudo apt-get install zip 



<!-- Start of picture text -->
=> If any error comes for installing<br>we > :~$ sudo apt-get update<br><!-- End of picture text -->



<!-- Start of picture text -->
—— ae<br>1 g What it does? |<br>{ '<br>H i<br>© Creates a zip archive of the given |<br>i file / directory. i<br>H i<br>' '<br>H :<br><!-- End of picture text -->



<!-- Start of picture text -->
After installation:<br>:~$ zip -r filel.zip scripts/<br>¥v v \<br>SS _<br>-r (recursive) filel.zip scripts/<br>sone all files and Destination Source file /<br>pat aheieeles zip file name directory to zi<br>(contents of folder) P OY SHEP<br><!-- End of picture text -->

###### 2) Unzipping the file: 



<!-- Start of picture text -->
:~$ unzip filel.zip ragrocterncnecne ccc e tne cnceeeenneenesceenenyy<br>.— = a: Es | E What it does? '<br>(i$ ls -lstr | tail -f H H<br>== | © unzip filel.zip > Extracts the zip i<br>4 -rwer--r-- 1 ubuntu | ..... filet.zip'| | © Is -Istr | tail -f > Shows the latest |<br>4 -rwer--r-- 1 ubuntu | ..... | scripts/ | files and directories live. |<br>© filet.zip > Zip archive file<br>© scripts/ > Extracted folder (contents of zip) |<br><!-- End of picture text -->

###### Summary 

1. Zipping | e zip <zipname.zip> <file/folder> | err > Create zip archive. | > Include all files and subdirectories | 

© Install zip (if not installed): sudo apt-get install zip 

© Update (if any error): i sudo apt-get update H 



<!-- Start of picture text -->
2. Unzipping<br><!-- End of picture text -->



<!-- Start of picture text -->
e unzip <zipfile.zip> > Extract the zip file.<br>¢ Us -Istr | tail -F > Show the latest files<br>(live).<br><!-- End of picture text -->

- (live). 



<!-- Start of picture text -->
Notes:<br><!-- End of picture text -->



<!-- Start of picture text -->
© zip > Compress files / folders.<br>© unzip > Extract files from zip archive.<br><!-- End of picture text -->



<!-- Start of picture text -->
ee ° °<br>——————————<br>EETAR - Archiving and Extracting Files<br># tar<br>1) Creating (Archiving) a File a aa<br><!-- End of picture text -->

# tar -cvzf 

###### :~$ tar -cvzf sample.tar scripts/ 

aprececneceseeceatesececteseateseasemensenenentans Option Summary H H H+ -c — Create a new archive i| i = the archive (gzip) | i -v Verbose output (show files) i 2%) Usearchive’ file ‘nome | 

-¢ — compress archive v or<sup>4</sup> — gzip compression: v -v > verbose (show files being archived) 

-f > use archive file name ¥ 

scripts/ — directory to archive scripts/wrapper_script.sh > file to archive 

\necnnensnnennnseennennntnnesnnsnnesnncennnennned 

###### 2) Deleting (Removing) Files or Directories 

i~$ rm -rf scripts/ 

rm -—> remove (delete) -rf — recursive force (deletes folders and their contents) 

### ————————n 

oe i | Use =rf carefully, It removesthe folder | and all. its y. i I pcos eamiga sane caeenpaeagmanmiesaeaeaspen 

###### 3) Extracting (Untarring) a File 

###### # tar -zxvf 



<!-- Start of picture text -->
:~$ tar -zxvf sample.tar Option ‘Simarnary (ution)<br>=x extract (untar) | -z — Decompress (gzip) Hi<br>:~$ ls -lstr | tail: -f Showand directoriesthe latest (live)files |H x Extract files from archive H<br>F | =v Verbose (show files) H<br>| |<br>: | =f — Use archive file name i<br><!-- End of picture text -->



<!-- Start of picture text -->
EeES ee<br><!-- End of picture text -->

###### Quick Summary 

- Extract Archive (untar) 

- — Archive (untar) v Tips sorchive.tar.gz> © Use -v to see what is being | decompress (gzip) archived/ extracted. © Always check files after verbose (show files) extraction using ls. archive file name ||. tar is useful for backup, | t transfer and compression. | ws) 



<!-- Start of picture text -->
| Create Archive (tar) Delete (rm)<br>tar -cvzf <archive.tar.gz> <file/dir> rm =r <file/dir><br>~c : create archive rm: remove<br>-z : compress (gzip) -rf : recursive<br>-v : verbose (show files) (no prompt)<br>-f : specify archive file name Unc ith “ccuaeal<br>2<br>J<br>\ ad<br><!-- End of picture text -->



<!-- Start of picture text -->
| | tar -zxvF sorchive.tar.gz><br><!-- End of picture text -->

rm =r <file/dir> 

rm: remove (delete) -rf : recursive force **|** (no prompt) 

-z : decompress (gzip) **|** -x + extract -v + verbose (show files) -f + specify archive file name t ———_ ws) 

Unc ith “ccuaeal 

11th April 2026 

Word Count 

— 

——_____{_{_{_+ 

###### Counting the words, 

characters and lines. 



<!-- Start of picture text -->
:~$ vi sample.txt aT,| Note: |<br>Example content: | 6 we stands for “word count’, |<br>Linux } * It is used to count: |<br>user is good — Words H<br>I am a person - Characters |<br>(save it) ; - Lines }<br><!-- End of picture text -->



<!-- Start of picture text -->
(| emet— oaceaee [ee [ee<br>|<br>1) :~$ we sample.txt * Defaultwe command | ¢ Words # we [file name]<br>* Prints number of ° Characters<br>3 8 42 sample.txt words, characters<br>bod od and lines. ane.<br>(Words) (Characters) (Lines)<br>2) ~$ we -w sample.txt | * Gives the number | » Words # we -w<br>of words in the file.<br>8  sample.txt |<br>3 :~$ we -1 sample.txt © Gives the number « hives<br>of lines in the file.<br>3 sample.txt<br>6 «Giof charactersantein | + am<br>42 sample.txt the file.<br><!-- End of picture text -->



<!-- Start of picture text -->
Summary<br>| Command | What it does Example Output<br>| we [file] Counts words, characters and lines 3. 8 42 — sample.txt<br>| we -w [file] Counts number of words 8 — sample.txt<br>we -1 [file] Counts number of lines 3 sample.txt<br>| we -c [file] Counts number of characters 42. sample.txt<br><!-- End of picture text -->



<!-- Start of picture text -->
Sorting the Lines<br>—_—_—_—_—___"_""___"""""""""“e<br><!-- End of picture text -->



<!-- Start of picture text -->
# sort<br><!-- End of picture text -->

###### 1. Sort in Alphabetical Order (Default) 



<!-- Start of picture text -->
Sort with Numerical Order: # sort -n<br>Kinssaie:xample @Mldinacal otesi’iw): i;<br>| Example:<br>Mango | | ———=9 |<br>| zebra 11<br>: Apple a Sa| 124 | —<br>:$ sort file.txt . => Applea | ||1 ——es = er) |a| 9 )<br>——— — ~ aes | :$ sort -n file.txt > rr<br>zebra | 2<br>J ! | 24<br>| If we give sort -n file.txt it will give in reverse order (numerical ascending order). |<br>Head & Tail Commands<br>—— oe<br>Cif we have to display first 10 or last 10 lines)<br>Command SS SSS SSS SS SSS SSS<br>What it does Example Output / Explanation Tag |<br>[s$f svactetevexe— Displayij the content (Opensawethe file in Shows all lines in file. #vi<br>A | of the file. vi editor)<br>+4 Heod. Hilectst ) Display first 10 lines (Shows first 10 First 10 lines of the baad<br>_—_ J | (default). lines) file will be displayed.<br>| 4 raWei filets= Displayisplay |last 10 lilines (Shows last 10 Last 10 linesi of the een<br>( | (default). lines) file will be displayed.<br>——=56 2) Shows first5 First5 lines will be a<br>‘hand Sp $i GA| Dislay Hee Sites, | COE fia he<br>lines) displayed. # tail -5<br>| (Shows last 5 Last 5 lines will be # tail -n 5<br>:$ tail -n 5 file.txt Display last 5 lines. lines) displayed. # tail -5<br>| Sorting Summary | Head & Tail Summary<br>iceeen Mations Result | (Commened Meaning | Displays<br>sort file.txt Sort alphabetically || AppleMango | viv file. txt | Open file in editor Entire file<br>|r eae head file.txt Show first 10 lines First 10 lines<br>|<br>it tail file.txt Show last 10 lines Last 10 lines<br>| | sorbents xe.) Samal? |) 2 head -n 5 file.txt | Show first 5 lines First 5 lines<br>(ascending order) | 11 |<br>| 24 | tail -n 5 file.txt Show last 5 lines Last 5 lines<br>|<br>FE te ial Sia si te AS (taal ena<br><!-- End of picture text -->

###### Pattern Matching. & Finding's Matches OO 

###### 1. Grep Command (grep) 

###### # grep 

Used to find / identify a file or text lines that are getting matched 

with the given pattern (string or expression). 

###### Example: 

%* Create two files with some log texts 

File: logl.txt 

- [INFO] Server started 

- [DEBUG] Connection success 

(ERROR] File not found 

- [INFO] Job completed [WARNING] Low memory 

- [ERROR] Timeout reached 

Fuel ‘Yoga vext 

###### Note: 

* grep searches for the given pattern in files and prints the matching lines. 

- Pattern matching is CASE SENSITIVE by default. 

(INFO] Server started 

- [DEBUG] Connection success 

[ERROR] File not found 

- [INFO] Job completed 

- [WARNING] Low memory 

- [ERROR] Timeout reached 

Save the files with file names: logl.txt and log2.txt H 

###### 2. Common grep Usage 

||{|L|e||
|---|---|---|---|---|
|®|grep ERROR log2.txt<br>(Searches for “ERROR”)|Displays lines that<br>;<br>contain the pattern<br>seRnoR?:|[ERROR] File not found<br>;<br>[ERROR] Timeout reached|q<br># grep<br>[find text]|
|2)|grep -i error logl.txt<br>(Searches for “error”,<br>case insensitive)|Displays lines that<br>match “error” (case<br>insensitive).|t<br>1 File not found<br>(ada) ‘<inachit ‘esanea|# grep -i [find text]|
|3)|grep -i<br>“error”<br>logl.txt | <br>Gerrog”<br>(Searches for exact word<br>“error”, | <br>caseinsensitive)|pisplays lines that<br>“error”<br> match the word<br>“error”<br>(case<br>insensitive).|;<br>i pits notefousd<br>penon) timeout reached|#<br>-i<br>[find<br>text:<br>grep|



Tips: 

+ By default, grep is case sensitive. 

* Use -i to ignore case (case insensitive search). 

* You can search in multiple files also: grep pattern filel.txt file2.txt 

###### GREP - Advanced Usage 



<!-- Start of picture text -->
3) grep -v ERROR logi.txt # grep -v<br>(It will give inverted) except that lines [rrr c enc n cence nec nenens,<br>(INFO) ... |! =v > Invert match (show lines |f<br>! that do NOT match the pattern) |<br>ee |<br>ee ae REN<br>(WARNING) ...<br><!-- End of picture text -->



<!-- Start of picture text -->
4) grep WARNING *.txt # grep *[pattern]<br>(gives matched lines within the file matched ) ee ag eee<br>| * > Matches ony file names H<br>{ f<br>logi.txt: [WARNING] .... HI (wildcard). Searches all H<br>t<br>log2.txt: [WARNING] .... ee a matchingeefil e s. eeH|<br>© rep WARNING *.txt | tail -f # -f > file<br>cc.<br>(gives9 last 10 lines (records)) ' tail -f > Follow the file and show |<br>!<br>'eeePlates © aren kDlastecg10 lines nat(records).oa|<br>@ ls -lstr | tail -f with -lstr<br>c ss<br>(gives last 10 files) |H=Lstr > long listing, sort by time (newest |'<br>|Hrer fi r st),e Seeltnianaehthen show last hein10 lines. |<br>=> [Example Directory Structure |<br>If we are having a file that contains matched item /legs<br>=> In thot directory itself having matched items I sampledat:<br>H demo |<br>LL kit Y j<br>(7) grep -r "Timeout" ~ /logs # -r<br>a OE TEEN<br>{ . _ ; |<br>/home/ubuntu/logs/test/list : Timeout i ~Y + Recursive search in directories. i<br>/home/ubuntu/logs/data.txt : Timeout ' Searches in all files under /logs. i<br>nS<br><!-- End of picture text -->

© rep "*[ERROR]" logi.txt eeea (gives the line that start with pattern) ' “> Matches the beginning of the line. 1 Shows lines that start with [ERROR]. ! 



<!-- Start of picture text -->
Quick Reference |<br><!-- End of picture text -->

###### Common Pattern Examples 



<!-- Start of picture text -->
© -i + Case insensitive search<br>_ Pattern Meaning<br>* -v > Invert match (exclude matching lines) ERROR — Lines containing the word ERROR<br>° > Wildcard (match ony file name) [ERROR] — Lines starting with [ERROR]<br>°© -f-r >+ FollowRecursivefilesearch(tail) in directories WARNS |e Einssstagting. - unis. WARN =<br>7” > Match beginning of line .#timeout.* | > Lines containing timeout<br><!-- End of picture text -->

### et 

| % Used to connect one server to another server. | (We can connect our friend’s Ubuntu system with our server using SSH) 

- @ installation: install 



<!-- Start of picture text -->
t~$ sudo opt-get install openssh-server<br>(SSH will be installed)<br>:~$ sudo apt-get update openssh-server<br>(Updates the SSH)<br>i~$ ifconfig —> command gives details obout our server. CIP also)<br>Entering into another server: “ | a RR RE |<br>t~$ ssh 192.20.124.118 + SSH uses port 22 by default. j<br>% after password, we can login into our friend’s system. i * Make sure SSH service is running |<br>Login using user-name: H H<br>| * Use ifconfig/ ip a to get IP. H<br><!-- End of picture text -->

- (2) Entering into another server: “ 



<!-- Start of picture text -->
t~$ ssh 192.20.124.118<br>% after password, we can login into our friend’s system.<br>Login using user-name:<br>:~$ ssh ubuntu@dheen<br>(Login to user ubuntu whose name is dheen)<br><!-- End of picture text -->

- (3) Login using user-name: 

###### ————— 



<!-- Start of picture text -->
| %& Used to copy one file to another server. |<br>%& From server to server copying. |<br>Example:<br><!-- End of picture text -->

|<br>%& From server to server c<br>|<br>opying.||<br>f<br>ome<br>Caiite<br>||<br><br><br>|
|---|---|---|---|
|Example:|||scp<source_file><user>@<||<br>ip>xdestination_path><br>|<br>|
|||<br>|||
|5<br>=|S|=||
|<br>@| scp (copy fite)|<br>Copy filefrom local toremote ||scp file.txt ubuntu@server: /home/ubuntu/|# copy file|
|sep (copy directory)|Copy directoryfrom local toremote!|scp -r dirl ubuntu@server: /home/ubuntu/|# copy directory|
|CommonSCPOptions||ImportantNotes|||
|<br>o-r<br>:<br>recursive copy (<br>+<br>=P <port><br>:<br>specify port (d<br><5<br>+compressdata|for directory)<br>efault 22)<br>whilecopying|<br>+<br>SCP uses SSH, so authentication is required.<br>+<br>Make sure the remote path and file name ore<br>*<br>Use-roptionwhencopyingdirectories.||<br> correct.|



|Comm|on|SC|P|Options||
|---|---|---|---|---|---|
|o-r|||<br>:|<br>recursive|copy (for directory)|
|+<br>=P|<por|t>|:|specifyp|ort(default22)|
|<br><5|||+|<br>compress|<br>datawhilecopying|
|--?P|||<br>:|<br>preserve|<br>file<br>permissions,<br>timeete.|





<!-- Start of picture text -->
%& Used to find a file. | # find --name<br>(1) find . -name log1.txt nha ae<br>(finds the file with name)<br>2) find . -name “*.txt" # --name "*.txt"<br>(find the file that ends with ".txt")<br>3) find . -type f -size +10M # --type -size<br>(type with file, size with >10MB)<br>4) find . -mtime -1 | # --mtime<br>(finds the file that are created within 1 day)<br>C5] | find . -empty # --empty<br>(finds the empty file in whole system)<br>6] | find . -name "*.tmp" -delete<br>i # --name “*.tmp" -delete<br>(deletes the file that ends with .tmp)<br>Feature Find grep |<br>aX Searches Files and directories Text inside files<br>Vad Used for || Locating files by name, Searching for . matching lines<br>| size, type, time etc. | (content) inside files.<br>= Search level | Filesystem level | File content level<br>Example find . -name logi.txt grep "ERROR" log1.txt<br>5 a — 1 ss<br>-name PATTERN : search by name ¢ find . -name "*.txt"<br>-typeype f /d 2 filnaif) of directory:directory. (a)(4. + find >.. -typefind allf .txt-sizefiles+10M<br>-size +10M / -10M: size greater than / less than — find files larger than 10MB<br>-mtime -1 : modified within 1 day © find . -empty<br>-empty : find empty files/directories — find empty files<br>a ” ¢ find . -name "*.tmp" -delete<br>| -delete : delete matched files — delete all .tmp files<br><!-- End of picture text -->

Notes: 

* The dot (.) means current directory. Use / for root directory. 

* You can combine multiple options with find for advanced searches. 

* Be careful with -delete option. 

* Use man find to see all available options. 

###### AWK (Command-line Tool) SS SS— 

AWK: (Alfred, Weinberger, Kernighan) 

% Processing columns in text. % = Performs calculations. 

% Extract and format data from files. 

| Examples: | a — — —_—___<§£— am (Creating a file) | | $ vi data. txt John 25 Developer | :~$ cat data. txt => Asha=e 30 Designeri ———_—_—__—_. Ravi 28 «Tester 

## == 

:~$ awk ‘{print $0}' data.txt © 5 ork “dorinn{p $6}409° dare 

(same output will appear) 



<!-- Start of picture text -->
=> John 25 Developer “ve<br>Asha 30 Designer<br>Ravi 28 Tester<br><!-- End of picture text -->



<!-- Start of picture text -->
e :~$ awk ‘{print $1}’ data.txt<br>John<br>= > Asha<br>(column 1 data will; be printed); Rianct<br>3] :~$ awk ‘{print $1 , $3}’ data.txt<br>John<br>=> Asha<br>(columni  _11 and columnI 3 data willi be printed)i Ravi<br><!-- End of picture text -->



<!-- Start of picture text -->
print $1<br><!-- End of picture text -->

ere $1, $3° John Developer Asha Designer Ravi Tester 



<!-- Start of picture text -->
VariableaMeaning Option | Meaning———<br>| $0 Entire line -F ‘delim’ Set field separator (delimiter)<br>| eeSSSR,ze. || rammuth enedddentisiaace|<br>| oF em Se ee<br>NF Number of fields (columns) in a line -—_<br>pe BEGIN { ... } Execute before reading input |<br>nnNR Current7 ‘neline numberin the fle boeaEND { ...a} camExecute a fterwmnpeereading input<br><!-- End of picture text -->

###### Notes: 

+ Default field separator is any space or tab. 

+ Columns in data are separated by space or tab. + Use quotes around awk programs: ‘{ }’ . + Very useful for text processing, data extraction and calculations. 



<!-- Start of picture text -->
4) awk ‘$2 > 27 {print $1, $3}’ data.txt # condition<br><!-- End of picture text -->

> Asha Designer: . : Ravi Tester 

6 awk ‘printf "Name : %s | Age: %s | Role : %s\n", # formatted output $1, $2, $3’ data.txt > Name: John | Age : 25 | Role : Designer Name: Asha | Age : 30 | Role : Developer Name: Ravi | Age: 28 | Role: Tester 

6) awk ‘NR==3, NR==6 {print NR, $0}’ employee.txt # print line range > 3 varun manager sales 50000 4 5 6 deepak clerk sales 23000 

Syntax of awk 

awk [options] ‘pattern {action}’ input-file > output-file 

awk — Starts the AWK text-processing program. 

[options] - Control AWK behaviour (e.g., set field separator). pattern — Specifies which lines to process. {action} - Defines what to do with matching lines (usually print). input-file - File that awk reads line by line. 

> output-file — Redirects processed output into a file. 

||||||
|---|---|---|---|
|-F ‘delim’|Set field separator (delimiter)|$0|| Entire line|
|-v varsvalue<br>|San<br>value to<br>vert|$1, $2, $3, ...|| Fields (columns) oF theline<br>|<br>|
|BEGIN<br>{...} <br>Eeentsa|]<br> |Execute<br>before reading input<br>:<br>ofter<br>9input|NF<br>poo<br>NR<br>FNR|Number<br>of fields (columns) in a line<br>f |<br>**Current**l**inenumber**<br>l<br>inthecurrentfile<br>||



Notes: 

© Default field separator is any space or tab. 

- Columns in data are separated by space or tab. 

- © Use quotes around awk programs: ‘{ }’. 

- Very useful for text processing, data extraction and calculations. 



<!-- Start of picture text -->
CHANGE MODE (chmod) 18 April 2024<br><!-- End of picture text -->



<!-- Start of picture text -->
=> If we have to change the mode for any one to read , write and execute ,<br>we use chmod.<br>=> Permission based command.<br>Team Who it is<br>a User = The user who owns the file.<br>2 Group - Members of the file's group.<br>2 Others “ Everyone else (excluding owner and group).<br>|] _—_—Root - The superuser - not affected by regular file permission.<br>Patterns for the file:<br>Example:<br>drwx n-x n-x<br>i$ Is -lstr (User , group , others)<br>drwx on-x n-x rwx — read , write , execute.<br>d: directory<br>wx: permissions for User<br>n-x : permissions for Group<br>n-x : permissions for Others<br>drwx n-x n-x -rw- rw- r--<br>L_. User Pspermission<br>(read , write , execute) file (read and write for user)<br>Group<br>(read , execute) Group<br>Others (read and write)<br>(read , execute) Others<br>Directory (read only)<br>chmod Numeric Notation<br>| Permission | Symbol . Value | rwx = 4+2+15: 7<br>Read (r) | r 4 | rw- = 4+2+026<br>Write (w) | w 2 | r-xee == 44 +0+02404125<br>Execute (x) | x 1 -wx = O+F24+123<br>No Permission (-) | = ° --x = O+F0+4121<br>ee ee =F = 0+0+0F0<br>|<br>chmod 755 file.sh > orwxr-xr-x — (file.sh) | + chmod changes the permission (mode) of files and directories.<br>chmod 644 file.txt > rwer--r--  (file.txt) * Use numeric mode (e.g., 755) or symbolic mode (e.g.,<br>chmod 700 script.sh > rwx------  (script.sh) | * Root user can override permissions.<br>| chmod -R 755 dir/ > Apply 755 to all files in directory * Be careful while using chmod -R on directories.<br>recursively<br><!-- End of picture text -->



<!-- Start of picture text -->
+ chmod changes the permission (mode) of files and directories.<br><!-- End of picture text -->



<!-- Start of picture text -->
* Use numeric mode (e.g., 755) or symbolic mode (e.g., u+x).<br><!-- End of picture text -->

————eeeeeeeeeeeeeee 

# Se 



<!-- Start of picture text -->
Permission Symbol Value }<br>Read og 4 v<br>Write | ‘w | 2 v<br>| Execute se 4 v<br><!-- End of picture text -->

@ For (read + write + Execute) > 44+2+1 5 7. 

@ For No permission = 0. 



<!-- Start of picture text -->
Permission string format<br>in$ Is -Istr drwxr-xr-x<br>=> drwxr-xr-x dummy — (directory) 1 SS Sy Se<br>d rwx r-x r-x<br>> -rw-r--r-- script.sh (file) type ine others<br><!-- End of picture text -->



<!-- Start of picture text -->
# chmod [number] filename<br>4) :~$ chmod 777 script.sh 777<br>| rwx rwx rwx |<br>. | et™ i<br>-rwxrwxrwx  script.sh (full access) H (user) (group) (others) access |<br>Ce |<br>e :~$ chmod 755 script.sh H oes, user read + write + execute<br>-rwxr-xr-x — script.sh| Hi (user)Twx (group) P-x (others)Px ) groupothers:: readread ++ executeexecute<br><!-- End of picture text -->



<!-- Start of picture text -->
-R_ (Recursive)<br>| 4) :~$ chmod -R 777 dummy Apply the permission to the directory and<br>| all its contents (files and subdirectories)<br>drwxrwxrwx dummy (full access) recursively.<br>eeae ae |<br><!-- End of picture text -->



<!-- Start of picture text -->
(emeaes ei)F Peres |f  Mecningi al © Use Is -1 to see current permissions.<br>} ™ | rwxrwerwx Full accessfor all- * chmod changes as Mlata permissiontperliativg)oF eei<br>755 rwxr-xr-x | Full access to user, | ‘aiid i .<br>read & execute to group & others irectories.<br>| |<br>bea ewrerse | Reed & wite for user, | + Use numeric mode (e.g., 755) or symbolic mode<br>| | _ read for group & others | (eg, utx, g-w)-<br>600<br>|__ |<br>a0 r --—-~_|o = Rend &Read for writeuser foronly user only |! 1.* RootBe carefuluser canwhileoverride using -Rpermissionson directories.<br>° --------- No permission<br><!-- End of picture text -->


