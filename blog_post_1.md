# Welcome to Blog Post 1: Remote Server

[Blogs](https://ashishsdalvi.github.io/cse15l-lab-reports/testing)

## How to connect to the Remote Server

**Installing VSCode** 

Go to the VSCode website and download the version for your respective operating system. I already have VSCode installing on my mac but your download page should look something like this. 

![VSCode](https://ashishsdalvi.github.io/cse15l-lab-reports/VSCode_Download.png)

Once you are finished downloading, go to the next step listed below. 


**Remotely Connecting**

Once you are in VSCode, open up a terminal.

In your terminal, type: ```ssh cs15lwi23zz@ieng6.ucsd.edu```

Your terminal should look similar to this picture when you ssh.
![SSH-ing Using the Terminal](https://ashishsdalvi.github.io/cse15l-lab-reports/ssh-ing.png)

Replace zz with the 3 letters corresponding to your specific CSE 15L student account. 
This information can be found at [Account Lookup](https://sdacs.ucsd.edu/~icc/index.php).

You will then be prompted to enter a password. After entering the password, you will be remotely connected to the server 
and some stats will be displayed. 

Your page should look similar to this image.
![Remote Server Output](https://ashishsdalvi.github.io/cse15l-lab-reports/Remote_Server_Output.png)

Once you are finished, try running some commands!

**Trying Some Commands**

The following are some commands you can try.
```
ls
pwd
cd
```
You can also add various flags to these commands as well (Ex: 'ls -lah')

'ls' is used to display all the files and directories in your working directory, 'pwd' outputs the path to your working directory, and 'cd' is used to move to another directory.

Here is some of the output from my commands. 
![Output From Commands](https://ashishsdalvi.github.io/cse15l-lab-reports/Command_Output.png)
