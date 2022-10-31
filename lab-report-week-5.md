_Week 5: Researching Commands_

We've been doing a lot of work with the terminal and terminal commands. Below I will showing some different and perhaps new to you ways on how to use some of these commands and some alternate ways to use them. 

<h3>The "Grep" command</h3>
We will be exploring different ways to use the grep command and its alternates 

Different uses of the ```$``` sign:

If we use the ```$``` after a keyword, it shows any lines in the file or directory we're searching in that end in that word.

For example:

```arshkaur@Arshs-Air docsearch % grep -r today$ ./technical```
This command will give us any lines in ./technicals that end in "today".

Here's the output below:
```

/technical/government/About_LSC/Progress_report.txt:increase in the number of people who enter the justice system today
./technical/government/Gen_Account_Office/d03419sp.txt:However, there is a lot of dialogue taking place today
./technical/government/Gen_Account_Office/Oct15-1999_gg00026t.txt:management improvement initiatives that we have discussed today
./technical/government/Gen_Account_Office/d01591sp.txt:and stronger economic growth over the long term. Saving today
./technical/government/Gen_Account_Office/d01591sp.txt:return depends not only on their preferences about spending today
./technical/government/Gen_Account_Office/d01591sp.txt:increasing saving are intertwined national goals. Saving more today
./technical/government/Media/Workers_aid_center.txt:Workers' aid center open today
./technical/biomed/1476-069X-2-4.txt:        benefits, retrofitting one million existing homes today
./technical/biomed/1476-069X-2-4.txt:        new homes per year), this implies that a code change today
./technical/biomed/1472-6947-2-7.txt:          Information technology in healthcare today
./technical/biomed/1472-6750-2-2.txt:        extended to many crops far beyond what is possible today

```
This is useful for if you want to filter a bunch of files. Or 



