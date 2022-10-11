# Lab1 tutorial
* Installing VScode<br>
Because I have already downloaded VS code when I took CSE 8A, I didn't follow the step from the lab instruction.Link for download VS code:[Link](https://code.visualstudio.com/)<br>
![Image](screenshot1.png)
* Remotely Connecting<br>
Firstly, change your password by going to [Link](https://sdacs.ucsd.edu/~icc/index.php)<br>
Wait the system to update your new password. <br>
type ssh cs15lfa22zz@ieng6.ucsd.edu in your terminal to connect to the remote server. zz should be replaced by your unique course account.<br>
![Image](screenshot2.png)
* Trying Some Commands<br>
Try different commands both on the client and server. Observe the difference<br>
For example, you can try $cd, which means change directory. "ls" will print out the content of the directory you are in.<br>
Type "exit" to logout from the server.<br>
![Image](screenshot3.png)
* Moving Files with scp<br>
Create a new file and try to use it by use command "javac" and "java".<br>
Then, copy the file to server by using the command "scp". Run this command with your username:scp WhereAmI.java cs15lfa22zz@ieng6.ucsd.edu:~/ Remember, do this in the directory you create the file.<br>
![Image](screenshot4.png)
![Image](screenshot5.png)
* Setting an SSH Key<br>
Type in command $ssh-keygen in your terminal, then press enter by three times:<br>
Enter file in which to save the key (/Users/joe/.ssh/id_rsa): /Users/joe/.ssh/id_rsa <br>
Enter passphrase (empty for no passphrase): <br>
Enter same passphrase again: <br>
Login to remote <br>
Type "mkdir .ssh".(If your .ssh already exists as mine, skip this step.） <br>
Logout <br>
Type "scp /Users/joe/.ssh/id_rsa.pub cs15lfa22@ieng6.ucsd.edu:~/.ssh/authorized_keys". Then, you can login and run scp without entering your password.
![Image](screenshot6.png)
![Image](screenshot7.png)
* Optimizing Remote Running<br>
To save time, you can type $ ssh cs15lfa22zz@ieng6.ucsd.edu "xx" where xx is the command you want to enter. In this way, you directly run the command onserver and then exit. We can run two commands at the same time by using semicolon to connect them.<br>
![Image](screenshot8.png)


