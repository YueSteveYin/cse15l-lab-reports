# CSE 15L lab report 4
## Linkes
1. [Link of my implementation](https://github.com/YueSteveYin/MarkDownParseGroup.git)
2. [Link of reviewed implementation](https://github.com/jordan-nishi/markdown-parse.git)

## the expected output
1. snippet1 expected output, `['google.com, google.com, ucsd.edu]`
2. snippet2 expected output, `[a.com, a.com(()), example.com]`
3. snippet3 expected output, `[https://www.twitter.com, https://ucsd-cse15l-w22.github.io/, https://cse.ucsd.edu/]`

## The test method code
![the Code 1](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2015l%20lab%20report4%20screenshot%204.PNG)
![the Code 2](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2015l%20lab%20report4%20screenshot%205.PNG)
![the Code 3](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2015l%20lab%20report4%20screenshot%206.PNG)

## the test results
![the result 1](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2015l%20lab%20report4%20screenshot%201.PNG)
![the result 2](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2015l%20lab%20report4%20screenshot%202.PNG)
![the result 3](https://raw.githubusercontent.com/YueSteveYin/cse15l-lab-reports/main/CSE%2015l%20lab%20report4%20screenshot%203.PNG)
All of the code, the one of our group and the one I review, have failed all of the three tests. 

## About debugging
1. the problem about the first snippet on my code is that it took in `url.com` as a website as well but it's not. since in my code we are just counting the `[`, `]`, `(`, and `)`
and did not take in account for the case of the black ticks, thus to fix this a whole chunck of code have to be updated to detect for back ticks, deterct for the position of the backticks, remove the chunk within the backtick, and than run the code again and thus there is no short fix for that
2. the problem about the second snippet on my code is that there is a pair of prentacies inside a pair prentacies in side the link, which is a triple prentacies situation. For this case my thought is to add a few lines that detect inadvace how many prentacies there are in the line, and than run through the link according to the number of the prentacies I got using a loop so that the program knows when to cut out to prevent such situation in the test from happening.  The fix could possibly take shorter than 10 lines. 
3. The problem about the third snippet on my code is that there is different lines for the code and one of the codehave  no end prentaciese. For this bug first I need to add a few conditions to detect `/n` between the prentacies and exclude them from the output of the program. And for the does not have closing prentacies case, I have to set up a series of complicated conditions, to First to make sure that the link have a complete prentacies, (including the case where the link does not have prentacies for a while), then run it through the code to sort out any edge cases, like the multiple space and lines inside prantecies. The detection and the conditions will be complicated, and thus cannot be complete by a short line change 
