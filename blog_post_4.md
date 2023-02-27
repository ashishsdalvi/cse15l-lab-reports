# Welcome to Blog Post 4: Competition

[Blogs](https://ashishsdalvi.github.io/cse15l-lab-reports/testing)

## Here I Will Be Replicating the Competition Tasks With Everything I type 

### Log into ieng6
What I typed: 
```ssh cs15lwi23aeg@ieng6.ucsd.edu```
```<enter>```

I typed in the command to ssh into my ieng6 remote server and pressed enter 
to run the command. 

![SSH](https://ashishsdalvi.github.io/cse15l-lab-reports/ssh_step_blog4.png)


### Clone your fork of the repository from your Github account
What I typed:
Copy the url of the lab7 fork from the Github website using
```<ctrl + c>```

and paste what you copied after typing git clone using ```<ctrl + v>```so it looks like: 
```git clone https://github.com/ashishsdalvi/lab7.git```
```<enter>```

You want to run git clone in order to copy the repository onto your remote server


![Cloning Repo](https://ashishsdalvi.github.io/cse15l-lab-reports/clone_repo_blog4.png)

### Run the tests, demonstrating that they fail
What I typed:
```cd lab7``` in order to access files in lab7 then ```<enter>```

Copy and paste the javac and java commands for compiling and running the Java code
using the JUnit tester given in the Week 7 page.

This is done using
```<ctrl + c>``` and ```<ctrl + v>```

The final commands looked like this
```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```
and 
```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTest```

![Tests Failing](https://ashishsdalvi.github.io/cse15l-lab-reports/test_fail_blog4.png)

### Edit the code file to fix the failing test
What I typed:
Pressed ```<i>``` to go into edit move in Vim and then pressed
```<down>``` till I reached line 43 and changed ```index1``` to ```index2``` using
the ```<delete>``` key.

Then I pressed the ```<esc>``` key and typed ```:wq``` to write and quit the file
and pressed the ```<enter>``` key.  

The issue with the test was that instead of updating the index counter for list2
under the list2 while loop, it was updating the counter for list1 (index1). 

![Editing Tests](https://ashishsdalvi.github.io/cse15l-lab-reports/edit_code_blog4.png)

### Run the tests, demonstrating that they now succeed
What I typed:
```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java``` then ```<enter>```
and then typed
```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests```
and then ```<enter>```. 

This code is used for recompiling the files I changed and rerunning ListExamplesTests. Heres a picture
of the output below.

![Tests Passing](https://ashishsdalvi.github.io/cse15l-lab-reports/test_pass_blog4.png)

### Commit and push the resulting change to your Github account (you can pick any commit message!)
What I typed:
```git add .``` then ```<enter>``` which selects the files I want to commit and then I typed
```git commit -m "Fixed code"``` then ```<enter>``` which allows me to document what changes I made and finally
```git push origin main``` then ```<enter>```. which uploads the specified files and comment to my Github account.

Here is an image of the process below:
![Git Commands](https://ashishsdalvi.github.io/cse15l-lab-reports/git_stuff_blog4.png)


