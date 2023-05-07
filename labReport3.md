# Lab Report 3

## Researching Commands (grep) 

**-c : returns count of matching lines**

```
$ grep -c "report" technical/911report/preface.txt
10
```
```
$ grep -c "public" technical/911report/preface.txt
3
```
This command-line option counts how many lines in the file contains the specific word and returns it. 
It could be useful when you are trying to find how many times a certain word repeats and if desired, you could edit the words to reduce repetition. 

**-i : ignores cases in patten**

``` 
$ grep -i "services" technical/government/Media/5_Legal_Groups.txt
services to the poor, ethnic minorities, seniors and people with
services. "And Justice for All," which solicits donations primarily
campaign of legal services agencies in the country, and the
Project and Utah Legal Services will share the new facility, and
efficient for those needing legal services. No longer will a woman
```
```
$ grep -i "law" technical/government/Media/5_Legal_Groups.txt
from Utah lawyers and foundations, was the first joint fund-raising
service law groups.
The Legal Aid Society of Salt Lake, the Disability Law Center,
the Multi-Cultural Legal Center, the Senior Lawyer Volunteer
```

This command-line option returns the lines that contain the words in quotations and ignores any uppercase or lowercase distinction. 
It could be useful when you are tyring to find where you used the specific word regardless of how you wrote it. 
You could also use it to check if there are words where you mistakenly capitalized or did not capitalize. 

**-n : shows line number as well as the output**
```
$ grep -n "report" technical/911report/preface.txt
5:            We present the narrative of this report and the recommendations that flow from it to
9:                partisan division-have come together to present this report without dissent.
47:                We hope that the terrible losses chronicled in this report can create something
58:            As we complete our final report, we want to begin by thanking our fellow
60:                together over every page, and the report has benefited from this remarkable
64:                Philip Zelikow, has contributed innumerable hours to the completion of this report,
78:                & Company for helping to get this report to the broad public.
85:                This final report is only a summary of what we have done, citing only a fraction of
89:                inevitably will come to light. We present this report as a foundation for a better
103:                considered the views of others. We hope our report will encourage our fellow
```
```
$ grep -n "individuals" technical/911report/preface.txt
24:                individuals in ten countries. This included nearly every senior official from the
```
This command-line option returns the lines that contain the words in quotations as well as the line number. 
It could be useful when you are trying to find the paragraph or line about a certain topic. 
It almost acts as an index so that you can look through all of the line numbers if needed. 

**--color : the words in quotations will be a different color compared to the rest of the text**
!! I couldn't figure out how to show the colored text here, so I added screenshots. !! 
```
$ grep --color "report" technical/911report/preface.txt
            We present the narrative of this report and the recommendations that flow from it to
                partisan division-have come together to present this report without dissent.
                We hope that the terrible losses chronicled in this report can create something
            As we complete our final report, we want to begin by thanking our fellow
                together over every page, and the report has benefited from this remarkable
                Philip Zelikow, has contributed innumerable hours to the completion of this report,
                & Company for helping to get this report to the broad public.
                This final report is only a summary of what we have done, citing only a fraction of
                inevitably will come to light. We present this report as a foundation for a better
                considered the views of others. We hope our report will encourage our fellow
```
```
$ grep --color "United States" technical/911report/preface.txt 
                the President of the United States, the United States Congress, and the American
                the United States. The nation was unprepared. How did this happen, and how can we
                Commission on Terrorist Attacks Upon the United States (Public Law 107-306, November
```
This command-line option changes the color of the words that matched the pattern and returned the lines where the word is included. 
This could be useful when the text is long and you want to easily identify the word in the text. 
Since it differentiates the word with the rest of the text in a different color, it is easier to notice them. 
