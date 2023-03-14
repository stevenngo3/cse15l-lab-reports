# Lab Report Week 9
## Lab 6 Grading Script
Below is my grading script: 
```CPATH='.;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar'

rm -rf student-submission
git clone $1 student-submission
echo 'Finished cloning'

cd student-submission
if [[ -f ListExamples.java ]]
then echo "ListExamples found"
else echo "need file ListExamples.java"
exit 1
fi

cp ListExamples.java ../
javac -cp ".;../lib/hamcrest-core-1.3.jar;../lib/junit-4.13.2.jar" *.java
if [[ $? == 0 ]]
then echo "ListExamples compiled"
else echo "ListExamples failed to compile"
exit 1
fi

java -cp ".;../lib/junit-4.13.2.jar;../lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore TestListExamples > junitresult.txt
JRESULT=`grep -c Failures: junitresult.txt`
echo $JRESULT
if [[ $JRESULT -ne 0 ]]
then echo "Grade: 100%, every test passed"
else echo "Grade: 0%, there is a test failure"
exit 1
fi
```

Repositories that were used to test the grader script (sources from Week 6) and the output from the grader script:

https://github.com/ucsd-cse15l-f22/list-methods-lab3: 

![lab61](lab61.PNG)

This repository has the same code as the starter from lab 3, and all tests pass as intended, getting a 100%.

https://github.com/ucsd-cse15l-f22/list-methods-corrected:

![lab62](lab62.PNG)

This repository has the methods corrected and is expected to get full credit. All the tests pass as intended, getting a 100% as well.

https://github.com/ucsd-cse15l-f22/list-methods-compile-error:

![lab63](lab63.PNG)

This repository has a syntax error of a missing semicolon and with the grader script, it will say that the compiler has failed, as well as state what the error is. Since it failed to compile, no grade is given.
