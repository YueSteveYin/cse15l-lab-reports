## Install VSCode
1. Fist go to the website [Link](https://code.visualstudio.com/) and download the corresponding version
2. then open the file and do as the instruction of the software says
3. you should set up the environment of whatever language you intended to use for the code to work.
4. This is what it suppose to look like once successfully set up ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/Capture%20lab.PNG)

## Remotely Connection
1. follow the instruction on the website [Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
2. go on school account/host/server to set up the accound and password[Link](https://sdacs.ucsd.edu/~icc/index.php)(here i encountered a little problem. the username should be the "sub-account" that the school gave me for the course but it won't work, what's working is the main account, which is the username(school email).)
4. type ssh username@serveranme in the terminal, type yes, and put in your password(the password won't show for security reason). It should look like this once successfully connected: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE12%20Lab%20report%20screenshot2.PNG)

## Run Some Commands
1. After ssh-ing, you can run commands in the terminal
2. here are some commonly used command: 
  * `cd`: Change directory
  * `ls`: show directory contents
  * `pwd`: show current directory
  * `mkdir`: Create a new folder
  * `cp`: Copy file or folder
  * `cat`: show content of a file
  * `exit` / `ctrl D`: exit ssh
3. here are some commends on the run (there are several command in the example that I have not permission to, I suspect that it's beacause the different system. It should work if I am on Linux system but I am in Windows System): ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE12%20Lab%20report%20screenshot3.PNG)

## Moving Files over SSH with scp
1. Creating file on the code editor end
2. in the terminal put in code `scp filename username@server:~/` and put in the password when propmt
3. log into the ssh, put in command `ls` and you can see your file already been added to the directory
4. here is the screenshot of the terminal when doing these proccess: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE12%20Lab%20report%20screenshot4.PNG)

## setting an SSH Key
1. At terminal, follow the instruction of [Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation) to set up the SSHKeys. Once succeed the full terminal should look like this: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE12%20Lab%20report%20screenshot5.PNG)
2. in the client terminal, login ssh, enter command `mkdir .ssh` and log out, then use command `scp publickeylocation username@servername:~/.ssh/authorized_keys` 
3. the key should be set up and you can ssh login and scp without putting in password every time. The result should look like this: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE12%20Lab%20report%20screenshot6.PNG)

## Optimizing Remote Running
1. up brings up last comment put (can use for faster ssh log in)
2. append command like ls in "" after ssh login command works
3. use semicolons to seperate each command to run multiple command
4. I am able to copy and check it and run it in a single line of code using the technique above and copy&paste. during the time I try, I found out that when I try to copy the file and run it right after copying it would be a time out and disconnection, ends up not able to copy the file but still runs the file. Here are the final result of my terminal(The first one is a success one, the second one is hte situation I a talking about)![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE12%20Lab%20report%20screenshot7.PNG)
