# Git Reset

## What is Git Reset?
Git reset is a command used to undo changes by moving the HEAD pointer to a previous commit.

## Types of Git Reset

### 1. Soft Reset
Moves HEAD to a previous commit but keeps changes staged.
```bash
git reset --soft HEAD~1
```

### 2. Mixed Reset (Default)
Moves HEAD and unstages changes, but keeps them in the working directory.
```bash
git reset HEAD~1
```

### 3. Hard Reset
Moves HEAD and completely discards all changes.
```bash
git reset --hard HEAD~1
```

## Example Workflow
```bash
# Make some commits
git commit -m "commit 1"
git commit -m "commit 2"

# Undo last commit but keep changes staged
git reset --soft HEAD~1

# Undo last commit and unstage changes
git reset HEAD~1

# Undo last commit and delete changes permanently
git reset --hard HEAD~1
```

## Important Note
> Avoid using `git reset --hard` on shared branches as it permanently deletes changes.