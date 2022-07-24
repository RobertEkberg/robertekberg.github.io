---
title: IBM Z Xplore - Cultural harmony - COBOL and JSON, together.
date: 2022-07-24 10:01:47 +07:00
modified: 2020-07-24 16:49:47 +07:00
tags: [IBM Z Xplore]
description: Here you can find clues and answers how to solve steps in this course from IBM. Course - IBM Z XPLORE COURSE - COBOL AND JSON.
---

**INTRODUCTION**

In this blog post you can find clues and the correct answers to solve the course. I advise you to first try to solve the course yourself then look at the clues, and then the answers.

This is NOT a step to step guide how to solve the challenge, you should do it yourself.

You can find the PDF for this challange here:
[COBOL-JSON PDF](https://ibmzxplore-static.s3.eu-gb.cloud-object-storage.appdomain.cloud/COBOL-HTML.pdf)



If you want to see how i solve the challanges in this course you can check my youtube video out.
You can find my youtube video here:

<a href="https://youtu.be/2tKAz82kEyU
" target="_blank"><img src="{{site.baseurl}}../assets/img/IBM Z XPLORE COURSE - COBOL AND JSON.png" 
alt="IMAGE ALT TEXT HERE" width="500" height="260" border="10" /></a>

**CLUES**

***Step 5***

There is a syntax error in the code and there is a function missing as you can see on the picture below.

<img src="{{site.baseurl}}../assets/img/somethingmissinghere-clue.png">

***Step 9***

The error you are looking for is in the JCL file.

***Step 11***

The error you are looking for is in the JCL file (you should convert it from text to html).

***Step 16***

You need to Add "$" to something in the COBOL file.

***Step 17***

What can store images?

<img src="{{site.baseurl}}../assets/img/add-product-images.png">

**ANSWERS**

Before you check answers try to solve it yourself first!

***Step 5***

The line is indented on the "if".

<img src="{{site.baseurl}}../assets/img/syntax-error-ind1.png">

"INTERGER-OF-DATE" is the correct answer.

```
Compute todays-date-int =
function INTEGER-OF-DATE(todays-date)
```

***Step 9***

You should add this line on row 18 in the JCL file.

```
 //FLYYFILE  DD SYSOUT=*,OUTLIM=15000
 ```

***Step 11***

You should modify the line from 'TEXT' to 'HTML' in the JCL file.
```
//RUNPROG   EXEC PGM=CBLJSON,PARM=('HTML')
```

***Step 16***

Add "$" in front of currencies.

<img src="{{site.baseurl}}../assets/img/add-currency-symbols-answer.png">

***Step 17***

This step is vaguely explained but should be enought for you to complete the step.

1) Remove the picture link.

2) Add "prod-img" to "inv-records"

3) Add "productimg" to "data items for currenccies"

4) Find this code "initialize flyer-file" then add "productimg" to that string and also to the else string.

```
 Initialize flyer-file
                 If flyerformat = 'TEXT' then
                    String productimg productname saleprice
                       " Was: " pricefrmt
                        delimited by size
                    into flyer-file
                 Else
                    String
                      htmltablestart productimg htmlprice saleprice
                      htmldiscount discount htmlproduct productname
                      htmloldprice pricefrmt htmltableend
                      delimited by size
                  into flyer-file
                 End-if
                 Write flyer-file
              End-if
              Add 1 to inv-rec-cnt
           End-perform
```

**Step 18**

Now you should have completed the HTML document. You can now copy paste the code, create a new member called cobol.html and paste the code into that file.

Please let me know if something is wrong!