# lab 3 changes
Here is the overall changes I made to the file: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot1.PNG)
below are the three bugs I fixed from the original file
1) I fixed the prantecies: when there are prantecies in the website URL the original file would be caught in a infinite loop here is how I fixed it: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot2.PNG)
2) Link to the test file for a failure-inducing input that prompted me to make the change [link](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/test-3.md)
3) The failure input and output: ![Image](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2012%20Lab%20Report2%20Screenshot3.PNG)
4) The bug is that if there are prantecies in the website URL, the loop will never break since indexOf("[") is -1 and the file does not end, thus the current index will always be -1 Thus created the symptom of the out of memory since the infinite loop keep adding to the toReturn arrayList. 

1) Whe
