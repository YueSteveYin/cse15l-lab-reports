# Lab Report 5 week 10
## How to find the tests with different results
First clone both of my repository and the class's repository to my remote. go into the `script.sh` file and add a line of `echo $file` to print the name of the test file before result. 
Then use command `bash script.sh>results1.txt` and `bash script.sh>results2.txt` in both files to run the script and store them into two different result file. Then run the command
`diff filepath filepath` to compare the two files and get the difference between them. 

## difference and fix
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
The 
