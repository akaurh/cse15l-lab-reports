<h1>_Week 9 Lab Report Autograder</h1>

Here's my `grade.sh` block

```json
set -e

rm -rf student-submission
git clone $1 student-submission

cd student-submission/
FILE=ListExamples.java
echo "Starting grading for: $1"

SCORE=0

JPATH='.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar'

if [[ -f "$FILE" ]]
then
    echo "ListExamples.java exists!"
else
    echo "Cannot find ListExamples.java!"
    echo "Your score is 0 out of 3!"
    echo "Try Again !"

    exit
fi

cp ../TestListExamples.java ./

set +e

javac -cp ".;../lib/*" ListExamples.java TestListExamples.java

if [[ $? -eq 0 ]]
then
    SCORE= $(($SCORE+1))
else
    echo "Your score is" $SCORE "out of 3!"
    exit
fi

FAILED=$(java -cp ".;../lib/*" org.junit.runner.JUnitCore TestListExamples | grep -oP "(?<=,  Failures: )[0-9]+")

if [[ $? -eq 1 ]]
then
    SCORE=$(($SCORE+2))
else
    SCORE=$(($SCORE+2-$FAILED))
fi

echo "Your score is" $SCORE "out of 3"
```