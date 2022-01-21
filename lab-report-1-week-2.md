## Install VSCode
1. Fist go to the website [Link](https://code.visualstudio.com/) and download the corresponding version
2. then open the file and do as the instruction of the software says
3. This is what it suppose to look like once successfully set up ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/Capture%20lab.PNG)

## Remotely Connection
1. follow the instruction on the website [Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
2. go on school account/host/server to set up the accound and password[Link](https://sdacs.ucsd.edu/~icc/index.php)
3. type ssh username@serveranme in the terminal, type yes, and put in your password(the password won't show for security reason). It should look like this once successfully connected: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE12%20Lab%20report%20screenshot2.PNG)

## Run Some Commands
1. After ssh-ing, you can run commands in the terminal
2. here are some commonly used command: 
  * cd: Change directory
  * ls: show directory contents
  * pwd: show current directory
  * mkdir: Create a new folder
  * cp: Copy file or folder
  * cat: show content of a file
  * exit: exit ssh
3. here are some commends on the run: ![Image](https://github.com/YueSteveYin/cse15l-lab-reports/blob/main/CSE12%20Lab%20report%20screenshot3.PNG)

## Moving Files over SSH with scp
1. Creating file on the code editor end
2. in the terminal put in code `scp filename username@server:~/` and put in the password when propmt
3. log into the ssh, put in command `ls` and you can see your file already been added to the directory
4. here is the screenshot of the terminal when doing these proccess: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE12%20Lab%20report%20screenshot4.PNG)

## SSHKeys
1. At terminal, follow the instruction of [Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation) to set up the SSHKeys. Once succeed the full terminal should look like this: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE12%20Lab%20report%20screenshot5.PNG)
2. in the client terminal, login ssh, enter command `mkdir .ssh` and log out, then uce command `scp publickeylocation username@servername:~/.ssh/authorized_keys` 
3. the key should be set up and you can ssh login and scp without putting in password every time. The result should look like this: ![Image](https://github.com/YueSteveYin/cse15l-lab-reports/blob/main/CSE12%20Lab%20report%20screenshot6.PNG)
