**Lab Report 1**

![Profile](cd.PNG)
<br />
When I typed "cd" into the terminal with no arguments while in the home directory, nothing happened and there was no input. This is not an error on the terminal but rather a human error as I did not declare a directory to change into. If we were to be already in, for example, the lecture1 directory or another directory, the command would change it back to the larger encompassing directory of lecture1. for example, if i were in /home/lecture1, and I cd with no argument, I would revert back to the /home directory.
When I typed cd lecture1, there was no output but on the contrary the new terminal line directory indicated that I had changed into the Lecture1 folder (this is not an error). 
Lastly, when I tried to cd into README file, we came across an error that essentially indicated that the README file was not a directory. This is because the README file is not a folder and is a txt file, the working directory in this scenario would be /home/lecture1/README, and therefore there are no embedded files within that we can access. 

![Image](ls.PNG)
<br />
When I simply input the ls command in the terminal without any arguments, the terminal outputs a list of all the files and directories that are included within the existing directory.
However, when we ls into the embedded messages directory, we get a list of all the Hello txt files that we were given and created.
Lastly, when we try to ls into a file, in this case the README file, we simply get the file name that we listed as the output.
Overall, there are no errors when using ls as long as a directory or file exists within the argument .

![Image](cat1.PNG)
<br />
![Image](cat2.PNG)
<br />
When I first used cat alone, we were simply given a user prompt to type in an input which would then have the terminal output what we inputted.
Next, when trying to cat lecture1 we ran into an error that essentially stated that lecture1 is a directory. This makes sense because directories host other files which contain content within them, it wouldn't make sense to print the output of a directory which would just be the list of files.
Lastly, when I used cat on README the terminal outputted and printed the contents of the README file. This is probably the most conventional way of using cat as it allows for the user to quickly access the written contents of certain files.
