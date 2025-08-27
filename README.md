# Git Version Control System

<img src="https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png" alt="Git Logo" width="200">

A simple guide to Git - the world's most popular version control system.

## What is Git?

Git is a free and open-source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

## Key Features

✅ **Distributed** - Every clone is a full backup  
✅ **Fast** - Lightning-fast branching and merging  
✅ **Secure** - Data integrity with SHA-1 checksums  
✅ **Flexible** - Supports various workflows  
✅ **Open Source** - Free and community-driven  

## Basic Commands

```bash
# Initialize a repository
git init

# Clone a repository
git clone <repository-url>

# Check status
git status

# Add files to staging
git add .

# Commit changes
git commit -m "Your commit message"

# Push to remote
git push origin main

# Pull latest changes
git pull origin main
```

## Working with Tags

### List Tags
```bash
# List all tags
git tag

# List tags with pattern
git tag -l "v1.*"

# Show tag details
git show <tag-name>
```

### Create Tags
```bash
# Create lightweight tag
git tag v1.0

# Create annotated tag with message
git tag -a v1.0 -m "Version 1.0 release"
```

### Delete Tags
```bash
# Delete tag locally
git tag -d <tag-name>

# Delete tag remotely
git push origin --delete <tag-name>

# Alternative way to delete remote tag
git push origin :refs/tags/<tag-name>
```

### Push Tags
```bash
# Push specific tag
git push origin <tag-name>

# Push all tags
git push origin --tags
```

## Why Use Git?

- **Track Changes**: Keep history of all file modifications
- **Collaborate**: Work with teams seamlessly
- **Backup**: Distributed nature means multiple backups
- **Branching**: Create feature branches without affecting main code
- **Rollback**: Easily revert to previous versions

## Quick Setup

1. Install Git from [git-scm.com](https://git-scm.com/)
2. Configure your identity:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```
3. Start using Git in your projects!

---

📚 **Learn More**: [Git Documentation](https://git-scm.com/doc)  
🎯 **Practice**: [Git Tutorial](https://learngitbranching.js.org/)
