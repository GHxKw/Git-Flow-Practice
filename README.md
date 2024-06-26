# Git-Flow-Practice
Practice
## Initalizing
So you want to run Git Flow ?

- Open git bash at your desire directory and run `git clone` either via HTTPS or SSH
- `cd Git-Flow-Practice`
- `git checkout develop` or `git switch develop` to go to the developer branch
- `git flow init` to init the git flow on your local machine

And you are set to go!!!

## Pulling/Merging, Feature branch and Pushing
### Pulling

When there are new updates on GitHub be sure to *pull* the latest changes down onto the local machine. Not compulsory but it is always advised to work on the `develop` branch so:

`git checkout develop` or `git switch develop` if you haven't

Merging
- `git fetch` to get the latest update from remote

If you did not have a branch on your local machine but the remote does:
`git checkout -b branch-name remote/branch-name` this command will *create* a new branch `branch-name` and *track* the `remote/branch-name` and *checkout* to that branch on your local machine
If you already have this branch on your machine:
- `git diff local-branch remote/remote-branch` this goes something like `git diff develop origin/develop` for most machines
- `git merge remote/remote-branch`

Pulling (fetch and merge into 1 line) (not advised)
- `git pull remote local-branch` 
you can't really use `get diff` to see the different here so be warry here or just YOLO.

### Starting a feature branch
Now to start your own feature:

- `git flow feature start name-of-your-feature` to start a new feature branch
- `git flow feature finish name-of-your-feature` to *merge* and *delete* the feature branch into the develop branch 

### Pushing a new branch for the first time
Normally you would:

`git push remote local-branch` after you have already done with your work on local machine

but first time pushing would not be possible because we haven't initialize a branch on remote, so:

`git push --set-upstream remote local-branch` where
`remote`: usually is `origin`
`local-branch`: the new branch that you have just created on you local machine
