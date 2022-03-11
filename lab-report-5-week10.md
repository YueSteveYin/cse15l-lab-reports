# Lab Report 5 week 10
## How to find the tests with different results
First clone both of my repository and the class's repository to my remote. go into the `script.sh` file and add a line of `echo $file` to print the name of the test file before result. 
Then use command `bash script.sh>results1.txt` and `bash script.sh>results2.txt` in both files to run the script and store them into two different result file. Then run the command
`diff filepath filepath` to compare the two files and get the difference between them. 

## Output for diff
this is the ooutput I got from running `diff filepath filepath` 
```
157a158
> []
211c212
< []
---
> [url]
229c230
< []
---
> [baz]
269c270
< [/bar\* "ti\*tle"]
---
> []
491c492
< [/f&ouml;&ouml; "f&ouml;&ouml;"]
---
> []
691c692
< [url &quot;tit&quot;]
---
> []
849c850
< [/uri "title"]
---
> []
861c862
< [/my uri]
---
> []
863c864
< [</my uri>]
---
> []
865,866c866
< [foo
< bar]
---
> []
870,871c870
< [<foo
< bar>]
---
> []
879c878
< [\(foo\]
---
> [\(foo\)]
881c880
< [foo(and(bar]
---
> [foo(and(bar))]
883c882
< [foo(and(bar]
---
> []
885c884
< [foo\(and\(bar\]
---
> []
887c886
< [<foo(and(bar]
---
> []
903c902
< [/url "title", /url 'title', /url (title]
---
> []
905c904
< [/url "title \"&quot;"]
---
> []
909c908
< [/url "title "and" title"]
---
> []
911c910
< [/url 'title "and" title']
---
> []
913,914c912
< [   /uri
<   "title"  ]
---
> []
918c916
< []
---
> [/uri]
920c918
< []
---
> [/uri]
922c920
< []
---
> [/uri]
1042c1040
< [not a link]
---
> []
1056c1054
< []
---
> [/url]
1064c1062
< []
---
> [train.jpg]
1068c1066
< []
---
> [<url>]
1072c1070
< []
---
> [/url]
1121a1120
> []
```
## first Difference:
The output for file 577 is not intended for the class's program, while the output for our program is correct. 
```
1064c1062
< []
---
> [train.jpg]
```
while our programm output nothing for getlink, the class's file regard an image link as a link, which is not intended for this program: the image link should not be outputed as a link.
Since the only difference between a link format and a image format is the exclamation mark before the bracket. And in the class's program there is no condition check for the exclamation mark before the bracket, thus the program recognized the image link as a link. The fix for this is to add a condition in the program to check if there exist an excalamation mark right in fornt of a bracket `[link]`. If there is a excalamtion mark that is right in front of the bracket that is used to be declearing a link(`![link]`), the rest is not considered a link thus will return nothing for the link inside the prentacies right after that notion. \

## second Difference:
The output for file 32 is not intended for the class's program, while the output for our program is also not intended 
```
491c492
< [/f&ouml;&ouml; "f&ouml;&ouml;"]
---
> []
```
In this case My program produced the wrong output and the class's program did not even produced an output. According to the VScode preview, VScode got a link for the file as `föö`. There is no fix for our program for this situation since we don't knwo how to implement the rules for the special characters and induce a result witht eh special charachters. While for the class's implementation, it did not produce any result since the program simply just broke when there is a space in the "link". As I said, there is no fix for the special charachters part unless we learn the rules for outputing special characters and knows how to output them, but for the space error, we can introduce an if statement and passit it through conditions to detect if there is space in the potential link(between the prentacies), so that the prgram won't broke and output nothing in the case of space. 
