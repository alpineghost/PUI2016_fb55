# PUI 2016 HW 1.  

## On NYU classes please turn in your github account name where the repositories you will create in this and the following homework sets will be hosted.

# Assigned Reading:

What is the question? Jeff Leek & Roger D. Peng
http://moscow.sci-hub.bz/4d3cf57483ccf211f66cad18440023cd/10.1126%40science.aaa6146.pdf

### GRADING: questions on the readout will appear in the pre-class quizzez. 


# Assignment 1: Finish Lab 1

### Finish the lab started in the first lab session if you have not in class:
https://github.com/fedhere/PUI2016_fb55/blob/master/Lab1_fb55/github_create_repo_cmds.md
If you were able to follow along you should have a repository set up on your local machine as well as on your github account named gittest_<netID>, with a single file in it named myfirstfle.txt, and you should have a resolved merge conflict. Because your repo is public we can access it, and see the history of your file, and the conflict in it. If you fell behind, please take yourself to this point, and feel free to work with others, but remember that it is your responsibility to learn, and be able to reproduce by yourself the work that you do in groups. 

### Create a conflict:

Pair with a classmate and fork each other’s repository. You need to first "fork" the repo, and then "clone" the repo on your machine. Further instructions on how to do it are on the github website, if you need. 
Make changes to your local copy of their file (whichever changes you wish to make). 
Commit your modified file and push the changes to your fork of the repo.
Request a merge from your classmate whose repo you forked.
Accept the merge request from your class mate.

### GRADING: 
-On your github account we must be able to see .

	1. our own repo, and in its history we need to see the merge. 

	2. your fork of your class mate repo and the changes you made to their file in its history

On your classmate repo we need to see your merge request.

## Assignment 2: Set up your environment: 

1. Generate a directory on compute called PUI2016_<netID>. 

2. Create an environmental variable on your compute account called PUI2016 that points to the directory PUI2016_<netID> by its full directory path: starting with /home [/home on a linux box, and with /Users on a mac if you want to replicate it on your machine] so that typing 

		$echo $PUI2016 

returns the full path to the directory. Save  it in the .bashrc [.bashrc for (linux) or .bash_profile (OS X) if you want to replicate it on your machine] so that every time you open a new terminal the terminal knows what the $PUI2016 environmental variable (env var) is set to.
3. Create an alias such that typing 
 		$ pui2015 
takes you to that directory. The alias must use the 'cd' command, and the env var $PUI2015 to do so. 

4. Take a screenshot of your .bashrc/.bash_profile file so that we can see the alias and env var you created. 

6. Type this series of commands on the terminal:
		$ pwd
		$ pui2015
		$ pwd
Take a screenshot of your terminal that shows this series of commands and their output. 

7. Once your environment is set up go to github online and CREATE A NEW GITHUB REPO CALLED PUI2015_<netID> ( this for me would be PUI2015_fbianco: https://github.com/fedhere/PUI2015_fbianco ). Follow the github directions to create a repository on the command line on your local machine.  Notice that in this case you are working in the reverse order compared to the lab: you create the first instance of the repository on the remote server (on the web) and then you create a local repo to link to it on your machine. Follow the steps indicated by github to create the repo, a README file, and to link the online and local repos. 

Now modify your README.md file: edit the copy on your machine to have it describe what you did to set up your enviroment and upload the screenshots I directed you to take above, so that they are displayed in your README.md (like in the image below). The README.md is a “markdown”file. To see what the syntax to upload an image in a markdown file, or in general to format the text, you can look at the README.md file in my PUI2015_fbianco repository (link above, and image below) and if you look at the raw file by clicking the Raw button on the top right you can see the syntax. 
Remember that you also need to upload the images in your remote directory for them to be displayed in your README! just like any file you add them by git add and git commit, git push.

NOTE: after you modify your .bashrc or .bash_profile you will have to rerun it: 
$ source .bashrc 
for the new set up to be incorporated in your environment. However, every new bash terminal you open will automatically read the .bashrc/.bash_profile and know about your new alias/env variables

### GRADING: 
We will grade you based on the README file you create in the github directory as described above. The screen shots need to show the appropriate lines in the .bashrc and that running the commands takes you to the right directory.

## Assignment 3 - Extra Credit. This may be hard, but figuring it out will greatly help you get the most out of the next several lectures. We keep track of your EC assignments and they will help your final grade.

1. Go to the PUI2015 directory you created in Assignment 1 and set up as a repo in Assignment 2.
2. Download the nontebook https://github.com/fedhere/PUI2016_fb55/blob/master/HW1_fb55/HW1_3_fb55.ipynb
. To do so click on Raw on the top right of the notebook. 
Now you have 2 choices: you can copy and paste the entire RAW Jupyter notebook (which is  a JSON file) onto a new file on your own machine (name the file HW1_3_<netID>.ipynb) or you can use the <i>wget</i> command on the terminal: typing 
		$ wget https://raw.githubusercontent.com/fedhere/PUI2016_fb55/master/HW1_fb55/HW1_3_fb55.ipynb

will save a version of the notebook in the directory where you were when you typed the command. wget, which stands for web get, downloads any files, or even entire directories, from a web URL. You must change the name of the notebook to HW1_3_<netID>.ipynb

3. Fill in the code cells that i left empty following the directions.

4. Once the notebook is done and rendered (you see the plots at the end of it) “stage it” so that git can track it (hint: follow the procedure in the lab assignment and use git add and git commit)

5. Link the current directory to your new github repo which you created in assignment 2 if you bave not done so yet, (PUI2015_<netID> on your github account, just like in the lab assignment you will need to use use 
 		$git remote add origin 
		$git push -u  using the URL of your new repo

6. Push the notebook into the github repo and check that it renders ok. Remember to check that it runs ok as well: before you commit open a new instance of Jupyter notebook (or restart your kernel!) and go through the notebook cell by cell to assure that there are no problems








## References: 
markdown syntax - http://daringfireball.net/projects/markdown/syntax
basic bash commands - http://www.tldp.org/LDP/abs/html/basic.html
environment setup - http://tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_01.html#sect_03_01_02
additional references were provided in the class slides.

Text Editors. 

#### -m

remember to add the -m “my commit message” when you commit to github, otherwise github will automatically open a text editor for you to type your message in , and then you have to deal with it. If github opened a text editor it is either emacs or vi, depending on your setup. If you are using emacs or vi, either because github opened them or to edit files, this is how you save your work and exit:

#### emacs 

Save: Ctrl+x Ctrl+s
Exit: Ctrl+x Ctrl+c
(if your emacs is running on the terminal you have to use these shortcuts, if it is running in its own X window you can use the dropdown menu)

#### vim (vi)

Save: esc :w
Exit: esc :q


## Key Concepts: 

falsifiability and law of parsimony
types of scientific questions
reproducible research
PEP8 and style standards 

work with github 
basic bash commands
understand how to setup your environment
creating and checking into github an Jupyter notebook

