What is a Git Stash?
A stash is like a temporary storage for your uncommitted changes. It allows you to “shelve” your work and return to a clean working directory.
Later, you can bring back your changes exactly as they were.

Basic Commands

Save your changes to a stash
    git stash

List all stashes
    git stash list


Apply a stash
    git stash apply stash@{1}
This brings back the latest stash but keeps it in the stash list. If you want a specific stash, use:


Pop a stash
    git stash pop
This applies the latest stash and removes it from the stash list.

Drop a stash
    git stash drop stash@{0}


Clear all stashes
    git stash clear
