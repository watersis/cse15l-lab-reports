# Labreport4
We can use the find tool to search for files and directories within system using a specified expression
-size n: The files will be shown on terminal if the file's size, rounded up, in 512-byte blocks is n.<br> Here only the files whose size rounded up in 512-byte blocks are 100 are shown.
```
wangluowei@wangluoweideMacBook-Air technical % find . -size 100
./biomed/1471-2377-3-4.txt
./biomed/gb-2003-4-6-r39.txt
./biomed/gb-2003-4-3-r20.txt
```
 Here since no file's size rounded up in 512-byte blocks is 10000, nothing is returned.
```
wangluowei@wangluoweideMacBook-Air technical % find . -size 10000
```
Here only the files with size rounded up in 512-byte blocks are 20 are shown.
```
wangluowei@wangluoweideMacBook-Air technical % find . -size 20   
./government/Gen_Account_Office/og97052.txt
./government/Gen_Account_Office/og96023.txt
./government/Gen_Account_Office/og96047.txt
./government/Gen_Account_Office/og97039.txt
./plos/journal.pbio.0020156.txt
./plos/journal.pbio.0020224.txt
./plos/journal.pbio.0030131.txt
./plos/journal.pbio.0020042.txt
./plos/journal.pbio.0020297.txt
./plos/journal.pbio.0020215.txt
./biomed/1472-6769-1-4.txt
```
-type will show the files of a specified type. -type d will list all the directory and sub-directory names.
```
wangluowei@wangluoweideMacBook-Air technical % find . -type d
.
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Gen_Account_Office
./government/Post_Rate_Comm
./government/Media
./plos
./biomed
./911report
```
 -type d -empty will list all the empty directories. Here there is no empty directory.
```
wangluowei@wangluoweideMacBook-Air technical % find . -type d -empty
```
-type f list all files in 911report.
```
wangluowei@wangluoweideMacBook-Air technical % cd 911report
wangluowei@wangluoweideMacBook-Air 911report % find . -type f
./chapter-13.4.txt
./chapter-13.5.txt
./chapter-13.1.txt
./chapter-13.2.txt
./chapter-13.3.txt
./chapter-3.txt
./chapter-2.txt
./chapter-1.txt
./chapter-5.txt
./chapter-6.txt
./chapter-7.txt
./chapter-9.txt
./chapter-8.txt
./preface.txt
./chapter-12.txt
./chapter-10.txt
./chapter-11.txt
```
-atime lets you find files based on their last access time.This option also supports the less than (-) and greater than (+) operators.<br> 
Here we search for files accessed later than one day ago
```
wangluowei@wangluoweideMacBook-Air 911report % find . -atime +1
.
./chapter-13.4.txt
./chapter-13.5.txt
./chapter-13.1.txt
./chapter-13.2.txt
./chapter-13.3.txt
./chapter-3.txt
./chapter-2.txt
./chapter-1.txt
./chapter-5.txt
./chapter-6.txt
./chapter-7.txt
./chapter-9.txt
./chapter-8.txt
./preface.txt
./chapter-12.txt
./chapter-10.txt
./chapter-11.txt
```
Here we search for files accessed less than 100 day ago
```
wangluowei@wangluoweideMacBook-Air 911report % find . -atime -100
.
./chapter-13.4.txt
./chapter-13.5.txt
./chapter-13.1.txt
./chapter-13.2.txt
./chapter-13.3.txt
./chapter-3.txt
./chapter-2.txt
./chapter-1.txt
./chapter-5.txt
./chapter-6.txt
./chapter-7.txt
./chapter-9.txt
./chapter-8.txt
./preface.txt
./chapter-12.txt
./chapter-10.txt
./chapter-11.txt
```
No file was modified 1 day ago.
```
wangluowei@wangluoweideMacBook-Air 911report % find . -atime 1
```
