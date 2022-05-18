# GIT
## fsck
### DANGLING COMMITS/Stashes - Hashes - LINUX
git fsck --no-reflog | awk '/dangling commit/ {print $3}'


### DANGLING COMMITS/Stashes - Hashes - POWERSHELL WINDOWS
git fsck --no-reflog | select-string 'dangling commit' | foreach { $bits = $_ -split ' '; echo $bits[2];}

### rebase
git rebase -i <branch_name>
#### squash multiple commits into single one
git rebase -i HEAD~<count_of_commits> # git rebase -i HEAD~4

## garbage-collection
git gc --aggresive


# GITK
## Repository Browser
### gitk - REPOSITORY BROWSER -  every single commit in the repository ever, regardless of whether it is reachable or not - LINUX
gitk --all $( git fsck --no-reflog | awk '/dangling commit/ {print $3}' )

### gitk - REPOSITORY BROWSER -  every single commit in the repository ever, regardless of whether it is reachable or not - POWERSHELL WINDOWS
gitk --all $(git fsck --no-reflog | Select-String "(dangling commit )(.*)" | %{ $_.Line.Split(' ')[2] })


### Submodules-Pull
git submodule update --init --recursive