---
caption: #what displays in the portfolio grid:
  title: Q7 | HW3
  
  thumbnail: https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/question-mark-icon-on-white-puzzle-royalty-free-image-917901148-1558452934.jpg
  
#what displays when the item is clicked:
title: Q7 | HW3
subtitle: Write an awk script to show difference between FNR and NR variables.
image: https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/question-mark-icon-on-white-puzzle-royalty-free-image-917901148-1558452934.jpg
alt: image alt text

---
*In awk, NR and FNR are built-in variables. NR tells us the total number of records that we’ve read so far, while FNR gives us the number of records we’ve read in the current input file.*<br/>
*e.g. let there be 2 text files:*<br/>
**t7_1**{: style="color: red; opacity: 0.80;"}<br/>
This is line1 of t7_1<br/>
This is line2 of t7_1<br/>
This is line3 of t7_1<br/>
This is line4 of t7_1<br/>
<br/>
**t7_2**{: style="color: red; opacity: 0.80;" }<br/>
This is line1 of t7_2<br/>
This is line2 of t7_2<br/>
This is line3 of t7_2<br/>
This is line4 of t7_2<br/>



awk one liner to differentiate between these two:<br/>
`$ awk '{ printf "Line:%s, NR:%d, FNR:%d\n", $0, NR, FNR}' q7_1 q7_2`<br/>
After running this command output would be follows<br/>

| Line                        | NR       | FNR    |
| :---                        | :----:   |   ---: |
| Line:This is line1 of t7_1, | NR:1,    | FNR:1  |
| Line:This is line2 of t7_1, | NR:1,    | FNR:1  |
| Line:This is line3 of t7_1, | NR:1,    | FNR:1  |
| Line:This is line4 of t7_1, | NR:1,    | FNR:1  |
| Line:This is line1 of t7_2, | NR:1,    | FNR:1  |
| Line:This is line2 of t7_2, | NR:1,    | FNR:1  |
| Line:This is line3 of t7_2, | NR:1,    | FNR:1  |
| Line:This is line4 of t7_2, | NR:1,    | FNR:1  |



