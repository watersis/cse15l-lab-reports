# Lab1 tutorial
* Installing VScode
Because I have already downloaded VS code when I took CSE 8A, I didn't follow the step from the lab instruction.
![Image](screenshot1.png)
* Remotely Connecting
Firstly, change your password by going to [Link](https://sdacs.ucsd.edu/~icc/index.php)
Wait the system to update your new password. 
type ssh cs15lfa22zz@ieng6.ucsd.edu in your terminal to connect to the remote server. zz should be replaced by your unique course account.
![Image](screenshot2.png)
* Trying Some Commands
Try different commands both on the client and server. Observe the difference
For example, you can try $cd ~.
Type "exit" to logout from the server.
![Image](screenshot3.png)
* Moving Files with scp
Create a new file and try to use it by use command "javac" and "java".
Then, copy the file to server by using the command "scp". Remember, do this in the directory you create the file.
![Image](screenshot4.png)
![Image](screenshot5.png)
* Setting an SSH Key
Type in command $ssh-keygen in your terminal, then press enter by three times. If your .ssh already exists as mine, skip this step. Then, logout and type in $scp /Users/joe/.ssh/id_rsa.pub cs15lfa22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys on your client.
![Image](screenshot6.png)
![Image](screenshot7.png)
* Optimizing Remote Running
To save time, you can type $ ssh cs15lfa22@ieng6.ucsd.edu "ls" where ls is the command you want to enter. In this way, you directly run the command on server and then exit. We can run two commands at the same time by using semicolon to connect them.
![Image](screenshot8.png)


