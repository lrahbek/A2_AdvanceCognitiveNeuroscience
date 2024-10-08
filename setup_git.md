# How to set up and use GitHub in uCloud :)

I dont know how comfortable we all are in git, so I have made a very clear (I hope) step-by-step guide, to set it up. If anything is confusing, let me know:))

## Forking and Cloning the Repository 

To avoid mishaps and unnecessary issues when merging, I suggest that we each have a 'fork' that we work in, and that we then can merge while we are together if we have worked on the same parts of code (just because we are going to be looking at it at the same time). If anyone has suggestions that they think will work better, I am up for that as well :). 

To create a fork got to : https://github.com/lrahbek/A2_AdvanceCognitiveNeuroscience and click on the 'fork' button. This creates an identical repository, but owned by you. If any changes are made in the 'main' repo, these can be pulled to yours (by clicking 'sync fork' button). 

Additionally, the changes made by you can be pushed to main repository, but as said I suggest we do that together to be sure to not run into any merge-issues :)). 

Alternatively, as long as the name of the notebook or other document isn't identical to one that already exists in the main repository, you can merge to the main repository without issue. This can be done by clicking the 'contribute' button in your repository. 

To clone the repository into uCloud got to the wanted destination for the folder in uCloud (I have put mine in my memberfile, but anywhere is fine). Get the link to your repository by clicking the green 'code' button in the repository, navigate to 'HTTPS' and copy the link. Then write the following in the terminal: 

```
git clone 'the link to your repo goes here'
```

## Connect to GitHub 
To easily connect with github everytime you open uCloud, create a bash file that does it in one run. 
You should call the bash file 'gitsetup.sh' (I have added this filename to the .gitignore, so we won't run into any problems). 

The bash file should include the following text: 


    git config --global user.email "your email adress goes here"
    
    git config --global user.name "your github user name goes here"


Everytime you open a run in Ucloud, you can the run the bash file in the terminal like so: 

```
$ bash gitsetup.sh
```

## Add, Commit and Push changes 

When finishing up in uCloud you can check what changes you have made (and make sure that it is the correct changes) by writting ```git status``` in the terminal. OBS: make sure to not push any virtual environments you have made in the folder, as they are too large for GitHub (and it is just not good practice;))

To add the changes to what you want to push to your fork of the repository, you can either write ```git add .``` in the terminal - this adds all the changes. This can be risky if you haven't checked with ```git status``` first - but is the easiest way to get everything. Otherwise you can write ```git add "name of file you want to add"``` in the terminal to only add specific files. 

When the changes have been added, they should then be commited, with a message that describes the changes, by writting; ```git commit -m "the message you want to include"``` in the terminal. 

Finally, you can push the changes to your remote repository (the one you can see on the GitHub website) by writing ```git push origin main``` in the terminal. 


## Repository Structure 

In the README.md file there is an overview of the repository structure, which is just the standard. I suggest that we have all notebooks, scripts etc. in the 'scr' folder. If we are working on the same notebook at the same time, it can sometimes be annoying and a hassle to merge them (this is at least my experience), so I suggest that when working on the same notebooks we either call them different names, or wait with merging forks until we are sitting together so we can decide what we want to keep at and what we don't want to keep :). 

The 'out' folder is for all plots, graphs and figures produced by the scripts. The 'in' folder is for the data used in the analysis notebooks etc. I have added all possible contents (except the .gitkeep file) within the 'in' folder to the .gitignore file, so we don't accidentally make sensitive data public. Also, the data is very large and GitHub won't allow us to push it anyways :). 


## Overview of Steps when Opening a run on Ucloud

1. Make sure that you in your remote repository (the one on the Github website) have synced your fork with the main one. 
2. Open a run on uCloud and from your local repository (the folder of the repository you have on uCloud) run ```bash gitsetup.sh``` script from the terminal. 
3. Update your local repository by writting ```git pull``` in the terminal. 
4. Make some edits or analysis in the folder. 
5. When finished add the changes, commit them and push them. 
6. If relevant go to the remote repository and push your changes to the main repository :)) (Here we can potentially do this together if we are afraid of conflicts:)))
