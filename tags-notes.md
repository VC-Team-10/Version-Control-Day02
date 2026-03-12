# Git Tags

## What is a Git Tag?
A tag is a reference that points to a specific commit, commonly used to mark release versions or important milestones in a project.

## Types of Tags

### 1. Lightweight Tag
A simple pointer to a commit with no extra information.
```bash
git tag v1.0
```

### 2. Annotated Tag
Stores extra metadata like author name, date, and message. Recommended for releases.
```bash
git tag -a v1.0 -m "Version 1.0 release"
```

## Common Commands
```bash
# List all tags
git tag

# Create a lightweight tag
git tag v1.0

# Create an annotated tag
git tag -a v1.0 -m "Version 1.0 release"

# Push a specific tag to remote
git push origin v1.0

# Push all tags to remote
git push origin --tags

# Delete a tag locally
git tag -d v1.0

# Delete a tag from remote
git push origin --delete v1.0

# View tag details
git show v1.0
```

## Example Workflow
```bash
# After finishing a feature, tag the release
git add .
git commit -m "Release version 1.0"
git tag -a v1.0 -m "First stable release"
git push origin main --tags
```

## Important Notes
> Annotated tags are preferred over lightweight tags for releases as they store additional metadata.
> Tags are not pushed automatically with git push — you must push them explicitly.