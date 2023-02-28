# Lab Report Week 7
## Part 4
Logged into ieng6 by using `ssh cs15lwi23zzz@ieng6.ucsd.edu` into the terminal. I had my account marked down on a google doc, so I `<ctrl><c>` to copy it and then `<ctrl><v>` to paste the account into the terminal. Typed my password and then got into ieng6.
![lab4step4](lab7s4.PNG)
## Part 5
To clone the fork of repository from my GitHub account, I `<ctrl><c>` to copy the repository link, and did `git clone` with the link pasted in using `<ctrl><v>`.

![lab4step5](lab7s5.PNG)

## Part 6
To run the tests, first I had to change to the lab7 directory so I typed the `ls` to locate lab7 and then typed `cd lab7` to get to that directory. I had the JUnit Mac commands on a google doc, so I `<ctrl><c>` the command `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`, and `<ctrl><v>` the command to paste it into the terminal. After that, I did the same with the command `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`. Tests will fail when you run them.
