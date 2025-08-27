My Project
Welcome to My Project! This repository demonstrates a complete Git workflow with branches, merging, and clean-up.
📋 Project Overview
This project shows how to:

Create and manage Git branches
Work with remote repositories
Merge changes between branches
Clean up branches after merging

🌳 Git Workflow Diagram
                    Remote Repository (GitHub)
                           origin
                             │
                ┌─────────────┼─────────────┐
                │             │             │
         ┌─────master─────┬───dev────┬───test────┐
         │               │          │           │
         │               │          │           │
    Local Repository     │          │           │
         │               │          │           │
    ┌─────────┐     ┌─────────┐ ┌─────────┐ ┌─────────┐
    │ master  │     │   dev   │ │  test   │ │ feature │
    │ branch  │────▶│ branch  │ │ branch  │ │ branch  │
    └─────────┘     └─────────┘ └─────────┘ └─────────┘
         │               │          │           │
         │               │          │           │
    Working Directory    │          │           │
         │               │          │           │
    ┌─────────────────────┼──────────┼───────────┤
    │                    │          │           │
    │  📁 README.md      │          │           │
    │  📁 dev-file.txt ──┘          │           │
    │  📁 test-file.txt ────────────┘           │
    │  📁 other files ──────────────────────────┘
    └────────────────────────────────────────────┘
🔄 Git Flow Process
Step 1: Initial Setup
bashgit init
git add README.md
git commit -m "Initial commit"
git remote add origin https://github.com/username/repo.git
git push -u origin master
Step 2: Branch Creation & Development
master ──●──●──●──●──●── (merge dev & test)
          │     │     │
          │     └── dev ──●──● (dev-file.txt)
          │              
          └── test ──●──● (test-file.txt)
Step 3: Merge & Cleanup
Before Merge:           After Merge:
                        
master ──●──●           master ──●──●──●──●
         │                       │     │
         dev ──●                 │     │
         │                       │     │  
         test ──●                │     │
                                dev (deleted)
                                test (deleted)
📂 Project Structure
my-project/
│
├── README.md          # This file
├── dev-file.txt       # Created in dev branch
├── test-file.txt      # Created in test branch
└── .git/             # Git repository data
🚀 Getting Started

Clone the repository:
bashgit clone https://github.com/username/my-project.git
cd my-project

Check available branches:
bashgit branch -a

View commit history:
bashgit log --oneline --graph


🔧 Git Commands Used
CommandDescriptiongit initInitialize new repositorygit checkout -b <branch>Create and switch to new branchgit merge <branch>Merge branch into current branchgit push origin <branch>Push branch to remotegit branch -d <branch>Delete local branchgit push origin --delete <branch>Delete remote branch
📊 Branch History

master: Main production branch
dev: Development branch (merged & deleted)
test: Testing branch (merged & deleted)

🎯 Key Learning Points
✅ Branch Management: Created separate branches for development and testing
✅ Remote Sync: Kept local and remote repositories synchronized
✅ Clean Merging: Successfully merged all changes without conflicts
✅ Cleanup: Removed unused branches to keep repository clean
📈 Visual Git Log
* commit abc123 (HEAD -> master, origin/master) Merge test branch
|\  
| * commit def456 Add test file
|/  
* commit ghi789 Merge dev branch
|\  
| * commit jkl012 Add dev file
|/  
* commit mno345 Initial commit
🤝 Contributing

Fork the repository
Create your feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request

📝 Notes

Always pull latest changes before creating new branches
Use meaningful commit messages
Test your changes before merging
Clean up branches after successful merge


Happy Coding! 🎉
Made with ❤️ using Git workflow best practices
