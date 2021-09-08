# How to use Git

## Clone the repository

Once you are on the repository's github page, copy the repository's address (The one finishing in `.git`. For the current repository, the address looks like `https://github.com/ynwbape/git.git`)

In your terminal, type `git clone {the_repository_s_address}`

All the repository's files should download. You'll be automatically on the branch named `master` (Default branch).

## Create a new branch

There are two ways of creating a new branch:

1. create the branch, then checkout:
   1. `git branch XXX` (Where XXX is your branch's name)
   2. `git checkout XXX` to go on the created branch
2. create and checkout at the same time:
   1. `git checkout -b XXX`

## List local branches

To list local branches and see which one is currently active (It will be displayed prefixed by an asterisk):  `git branch`

## Check the current files status

`git status` lists the files which are not commited to the branch yet.

- Untracked files are shown in red
- Updated files are shown in red
- Tracked files are shown in green

## Adding files to the commit

1. `git add {path_to_file}` to add a single file, without verification
2. `git add .` to add all modified or untracked files at once
3. `git add -p` to see all the modifications to tracked files. The modifications will be listed one by one, with these options:
   - `y` to add the current modification to the commit
   - `n` to ignore the modification
   - `a` to add this modification and every other from the same file
   - `d` to ignore this modification and every other from the same file
   - `q` to stop and exit the process

## Creating the commit

`git commit -m "commit message"`

## Pushing the commit to the repository

1. First commit: `git push --set-upstream origin {your_branch_name}`
2. Any other commits (When the first commit is already done): `git push`
