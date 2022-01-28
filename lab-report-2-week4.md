# Lab report2
Here is the overall changes I made to the file: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot1.1.PNG)
below are the three bugs I fixed from the original file
1) I fixed the prantecies: when there are prantecies in the website URL the original file would be caught in a infinite loop here is how I fixed it: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot2.2PNG.PNG)
2) Link to the test file for a failure-inducing input that prompted me to make the change [link](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/test-3.md)
3) The failure input and output: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot3.PNG)
4) The bug is that if there are prantecies in the website URL, the loop will never break since `indexOf("[")` is -1 and the file does not end. This cause the current index will always be -1 Thus created the symptom of the out of memory since the infinite loop keep adding to the toReturn arrayList. 
**************
1) When there is a image link, the original program will recognize it as a website here is how I fixed it: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot4.4PNG.PNG)
2) Link to the test file for a failure-inducing input that prompted me to make the change [link](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/test-2.md)
3) The failure input and output: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot5.PNG)
4) The bug is that when the input contains a image link the program will take it as a website link and print it out. the original program only look at "[", "]", "(", and")" thus when the file contains a image link , the program will print out the image link as a websit link.
****************
1) When there is no link, just a set of bracket, the program will stil searching for prantecies to find website here is the fix:![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot4.4PNG.PNG)
2) Link to the test file for a failure-inducing input that prompted me to make the change [link](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/test-file3.md)
3) The failure input and output: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot6.PNG)
4) The input only have a brakect, but since the original program recognize the brackets it starts to search for prantecies, which will have a index of -1. Thus when the program run it will out put `indexOutOfBoundsException()` since it's trying to use `substring()`. 
