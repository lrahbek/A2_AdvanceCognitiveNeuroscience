# How to set up and use GitHub in uCloud :)

I dont know how comfortable we all are in git, so I have made a very clear (I hope) step-by-step guide, to set it up. If anything is confusing, let me know:))

## Forking and Cloning the Repository 

To avoid mishaps and unnecessary issues when merging, I suggest that we each have a 'fork' that we work in, and that we then can merge while we are together if we have worked on the same parts of code (just because we are going to be looking at it at the same time). If anyone has suggestions that they think will work better, I am up for that as well :). 

To create a fork got to : https://github.com/lrahbek/A2_AdvanceCognitiveNeuroscience and click on the 'fork' button. This creates an identical repository, but owned by you. If any changes are made in the 'main' repo, these can be pulled to yours (by clicking 'sync fork' button). Additionally, the changes made by you can be pushed to main repository, but as said I suggest we do that together to be sure to not run into any merge-issues :)). 

To clone the repository, got to the wanted destination for the folder in uCloud (I have put mine in my memberfile, but anywhere is fine). Get the link to your repository by clicking the green 'code' button in the repository, navigate to 'HTTPS' and copy the link. Then write the following in the terminal: 

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