

Overall, make sure you have at least 3 screenshots, one for each of the steps below
For each step include 2-3 sentences or bullet points describing what you did. 


Installing VScode
Remotely Connecting
Trying Some Commands

# How to use VSCode to remotely connect to the ieng6 servers

## Installing VSCode
If you already have VSCode installed on your computer, you are free to skip this step.

Otherwise, head to this [Link](https://code.visualstudio.com/) and install VSCode
for your respective operating system. 

When you open VSCode, it should look a little something like this.
![image](https://user-images.githubusercontent.com/97487846/211931263-38efbb30-962b-43f9-98d2-a2b7a18b08ca.png)


## Remotely Connecting

Go ahead and open a new terminal and type in the following command:

`$ ssh cs15lwi23zz@ieng6.ucsd.edu`

Do not include the $, and replace the `zz` with your specific three-letter sequence.

It will prompt you to enter your password.
After inputting your password, you should get a message that looks like this:
![image](https://user-images.githubusercontent.com/97487846/211931213-1fbfb647-7545-4104-9af3-fb997c15a6e7.png)

## Trying Some Commands
Now that we're logged into the remote server, we can go ahead and try some commands to navigate the directories.

Here is a table of commands to navigate/modify the directories:
```
cd <directory> -change directory to desired path
ls             -lists all directories in the current working directory
ls -lat        -try this command out
```
When using ls -lat, you should see the following output:
![image](https://user-images.githubusercontent.com/97487846/211931126-0f7c1b43-525b-4991-ba7a-1a67ad64aa2e.png)
