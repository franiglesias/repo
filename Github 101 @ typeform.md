#Github 101 @Typeform

## Create a Local Repository

1. Move to the desired folder
2. Init the repository

```bash
git init
```

This creates a .git folder that contains info needed by Git to manage the repo and its versions.

```
➜  repo git:(master) ls -al
total 0
drwxr-xr-x  3 franiglesias  staff   96 24 abr 19:38 .
drwxr-xr-x  7 franiglesias  staff  224 24 abr 19:38 ..
drwxr-xr-x  9 franiglesias  staff  288 24 abr 19:39 .git
```

## See the status of a repo

This tells us the current state of our repo

```bash
git status
```

## Clone an existing repository to work with

```bash
git clone repository.git

git clone https://github.com/WomenWhoCode/WWCodeBarcelona.git
```

This keeps track of the changes and you can send this changes to the remote repository

## Fork

Creates a derivation from a repository that itself is a new independent repository but with the same contents.

Changes in the forked repo belong to it. The original remains untouched.

## Clone vs Fork

Clone an existing repo to local so you can work with that project. Changes will be applied to the original repository.

Fork: copy a repo to your own space, so your changes are separated from those on the original repo.

## Track new files and changes

You need to add files to be tracked by git.

```bash
git add . // all changes
git add --all // all changes
git add path/to/file.ext  // this file
git add path/to/folder. // the contents of this folder
```

If we check for status we'll see the files added to the stage

```bash
git status
```

Result

```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   Github 101 @ typeform.md
	new file:   myfile.md
```

## Commiting the changes

```bash
git commit // will open the default $EDITOR to include a message
git commit -m "This commits does something important"
```

## Git remote

```bash
git remote add origin https://github.com/franiglesias/repo.git
```

### Sending changes to remote

```bash
git push
```

### Git pull

Get the changes, and merge into the local

```bash
git pull
```

### Git fetch

Get the changes, but no merge them

```bash
gut fetch
```

## Conflicts

1. Resolve conflicts
2. Add changed files
3. Commit the changes
4. Push to remote

## Branches

### Create a new local branch

```bash
git branch "Name_of_the_branch"
git checkout "Name_of_the_branch"


git checkout -tb "Name_of_the_branch" // new branch and set remote up-stream
```
Existing changes will be moved to the new branch leaving the original untouched.

Each branch can evolve separately and even you can make branches from a branch.

Always will be a master branch.

### Move to a branch

```bash
git checkout target_branch

git checkout master
```

### Push changes in a branch to remote

We need to track upstream branch.

If we try to push, git will tell us how to set the upstream and track the remote branch.

### Merge branches to master (or another branch)

(Introducing Pull Request)

1. Open a pull request
2. Merge changes (when approved)
3. Delete the branch after merge
4. (should delete the local branch also)

## Rebase

Rebase is a way to merge the changes of a branch into another one keeping the history chronological order of commits.

