# Lab Report3
## Streamlining ssh Configuration

1. ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report3%20Screenshot1.PNG)
I found the `~/.ssh` in my computer, the path is `C:\Users\mrmus\.ssh`. Then I open the .ssh folder using Vscode. In VsCode, I created a file called config without any suffix. 

2. ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report3%20Screenshot%202.PNG)
In file config, I put in text <br /> `Host ieng6`<br /> >>`HostName ieng6.ucsd.edu`<br /> >>`User yuy045` <br />and save the file <br /> 
Then in the terminal I successfully logged into ssh just by using the comand`ssh ieng6`

3. ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report3%20Screenshot%203.PNG)
Then I created a java file called `cse15llabfile.java` and using the command `scp cse15llabfile.java ssh ieng6:~/` to copy the file into ssh's general directory. <br />
Then I logged into my ssh account, use command `ls` to check if the copy is successful, and the file appeared.  
