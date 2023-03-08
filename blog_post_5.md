# Welcome to Blog Post 5: Doing Tasks Even Quicker (With Bash Scripts)

[Blogs](https://ashishsdalvi.github.io/cse15l-lab-reports/testing)

## An Idea for a Bash Script to do the Lab 4 Tasks Quicker

The lab 4 tasks involve logging into ieng6, forking the clone of the repository, running tests, fixing the tests, 
running the tests again so they succeed, and  committing/pushing the code to our Github account.

I will write two bash scripts to automate most of these tasks.
The first bash script will do the following: log into ieng6, fork the clone of the repo, and run the tests.

We will then fix the tests manually.

The second bash script will do the following: run the tests again and commit/push the code to our Github. 


## Bash Script #1 
In this bash scripts, I also write ```<< EOF COMMANDS <<``` and nest all my commands into within the <<'s.
This allows me to run my commands in a remote server from a script on my local computer.

Here is a picture of Bash script #1.
![Script #1](https://ashishsdalvi.github.io/cse15l-lab-reports/blog_5_script1.png)

## Intermediate Step
In this step, I go in and fix the code manually by changing a line in ListExamples.java. The line that was broken
was a line nested in a while loop counter that loops over List2 except that the broken code increments a counter for 
List1 instead of List2. Once this is fixed, I can run Bash Script #2. 


## Bash Script #2 
In this bash scripts, I also write ```<< EOF COMMANDS <<``` and nest all my commands into within the <<'s
This allows me to run my commands in a remote server from a script on my local computer.

Here is a picture of Bash script #1.
![Script #2](https://ashishsdalvi.github.io/cse15l-lab-reports/blog_5_script2.png)

Thanks for reading this post. Hope you learnt how to use Bash to semi-automate some tasks!
