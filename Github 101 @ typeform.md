#Github 101 @Typeform

## Create a Local Repoitory

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

## Track new files

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

## Commit the changes

```bash
git commit // will open the default $EDITOR to include a message
git commit -m "This commits does something important"
```

## Git remote

```bash
git remote add origin https://github.com/franiglesias/repo.git
```

## Git pull

Get the changes, and merge into the local

```bash
git pull
```

## Git fetch

Get the changes, but no merge them

```bash
gut fetch
```

## Conflicts

