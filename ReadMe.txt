━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PROFESSIONAL SUMMARY (Short and Table-Focused)
QUICK EXPLANATION (Mid-Level Explanation)
ZERO-LEVEL GUIDE (Assumes No Prior Knowledge)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
──────────────────────────────────────────────────────────────── ──────────────── 1) PROFESSIONAL SUMMARY ──────────────── ────────────────────────────────────────────────────────────────

A concise, professional “cheat sheet” of Git, advanced workflows, and PyCharm integration. Refer to the table for commands and quick references.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ A. GIT & GITHUB CRASH COURSE TABLE ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Command/Topic	Explanation/Usage	Example
git config --global user.name	Sets global name for commits	git config --global user.name "Alice"
git config --global user.email	Sets global email for commits	git config --global user.email "alice@company.com"
git init	Initializes a new Git repository	git init
git clone <url>	Clones an existing repository	git clone https://github.com/user/repo.git
git remote add origin <url>	Links local repo to a remote	git remote add origin https://...
git add <file>	Stages changes for commit	git add hello.txt
git commit -m "msg"	Commits staged changes with a message	git commit -m "Add greeting"
git push -u origin main	Pushes local changes to remote origin on branch main, sets upstream	git push -u origin main
git pull	Fetches and merges remote changes	git pull
git checkout -b <branch>	Creates and switches to a new branch	git checkout -b feature/new-feature
git merge <branch>	Merges specified branch into current branch	git merge feature/new-feature
git rebase <branch>	Applies commits on top of another branch	git rebase main
git stash	Stashes uncommitted changes away temporarily	git stash
git stash pop	Re-applies stashed changes	git stash pop
git log	Displays commit history	git log
git diff	Shows changes between commits or working tree	git diff HEAD~1 HEAD
git branch -d <branch>	Deletes a branch	git branch -d feature/new-feature
git tag <tagname>	Tags a commit (useful for releases)	git tag v1.0.0
git revert <commit>	Reverts a specific commit by creating a new commit	git revert d869cd4
git cherry-pick <commit>	Applies a single commit from one branch to another	git cherry-pick f32ac12
git bisect start / good / bad	Binary hunts for commit causing a bug	git bisect start → git bisect good <commit> → etc.
.gitignore	File listing patterns to ignore (not committed)	See the official docs for examples
SSH Keys / Personal Tokens	Secure authentication	Use SSH or PAT for git push
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ B. ADVANCED TOPICS ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Rebase vs Merge
• Rebase rewrites commit history for a linear history.
• Merge creates a new merge commit, preserving branches’ histories.

Submodules
• Allows linking external repos inside a parent Git repo.
• Use for large, modular projects.

Git Hooks
• Scripts that run on certain events (pre-commit, post-merge, etc.).
• Automate tasks (linting, tests).

Aliases
• Shorten common commands, e.g.:

bash
git config --global alias.co checkout
git config --global alias.st status
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ C. QUICK PYCHARM REFERENCE ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ • Enable Git: VCS → Enable Version Control Integration
• Commit & Push: Git widget bottom → Commit → Push
• Branching: Bottom bar → Branch name → New Branch
• Pull Requests: Typically done on GitHub website (PyCharm can assist but often simpler to use the browser)

──────────────────────────────────────────────────────────────── ──────────────── 2) QUICK EXPLANATION ──────────────── ────────────────────────────────────────────────────────────────

Here’s a mid-level explanation of what’s happening at each stage, focusing on workflow clarity.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ A. GIT CLI QUICK FLOW ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Initialize/Clone
• Start a local repo with “git init” or copy a remote with “git clone”.
Stage & Commit
• “git add” to stage modifications, “git commit” to record them.
Branches
• Create new branches (git checkout -b), do work, then merge (git merge) or rebase as needed.
Push & Pull
• Push changes to GitHub, pull changes from others.
• Use a secure method (SSH keys or tokens).
Collaboration
• Use pull requests on GitHub to review and merge code.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ B. PYCHARM QUICK FLOW ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Setup
• Open or clone repo in PyCharm, enable Git in VCS settings.
Track Changes
• The Version Control panel shows changed files; click + to stage, commit.
Push & Pull
• Use VCS > Git > Push / Pull or the up/down arrows.
Branch Management
• Bottom-right branch indicator → create or switch branches easily.
Merge Conflicts
• PyCharm has a visual merge tool for conflict resolution when pulling or merging.
──────────────────────────────────────────────────────────────── ──────────────── 3) ZERO-LEVEL GUIDE ──────────────── ────────────────────────────────────────────────────────────────

If you’re new to everything, follow this step-by-step guide. We’ll cover from zero to advanced usage.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ A. INSTALLATION & SETUP ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Install Git

Windows/Mac: Download from https://git-scm.com/downloads
Linux:
bash
sudo apt install git
Verify installation:
bash
git --version
Configure Git (name, email)

bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
Install PyCharm

Get it from https://www.jetbrains.com/pycharm/download
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ B. CREATE OR CLONE A REPO ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1) Create a Local Repo
bash
mkdir myproject
cd myproject
git init
mkdir myproject makes a folder.
cd myproject enters that folder.
git init turns it into a Git repository.
2) Link to GitHub
Create a new repo on GitHub. Don’t initialize if you already started locally.
Connect local to remote:
bash
git remote add origin https://github.com/username/myproject.git
git push -u origin main
3) Or Clone an Existing Repo
bash
git clone https://github.com/username/someproject.git
This copies the remote repo locally.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ C. MAKING CHANGES & COMMITTING ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Edit or Create Files
bash
echo "Hello World" > hello.txt
Stage & Commit
bash
git add hello.txt
git commit -m "Add hello.txt with greeting"
Push to GitHub
bash
git push
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ D. USING BRANCHES ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Create & Switch
bash
git checkout -b feature/cool-idea
Work and Commit
bash
# make changes
git add .
git commit -m "Implement cool idea"
Push Branch
bash
git push -u origin feature/cool-idea
Open a Pull Request on GitHub to merge into main.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ E. MANAGING MERGES & REBASES ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Merge
Switch to the branch you want to merge into (e.g., main), then:
bash
git merge feature/cool-idea
Rebase
“Replay” commits from one branch onto another (advanced topic).
Example:
bash
git checkout feature/cool-idea
git rebase main
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ F. PYCHARM WALKTHROUGH ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Open Project

File > Open → Select your local repo folder.
Enable Git

VCS > Enable Version Control Integration → Choose “Git”.
Look at Version Control Panel

Bottom bar → “Version Control”.
Shows changed files, logs, and branches.
Commit & Push

Make changes in code.
In Version Control panel, stage your changes (or it auto-stages in newer versions).
Click “Commit”, type a message, then “Commit and Push” to send to GitHub.
Pull

VCS > Git > Pull if changes live on GitHub.
Branch Creation

Bottom-right, click current branch → “New Branch”.
Commit changes on that new branch, push, do a Pull Request.
Conflict Resolution

If there’s a conflict when pulling or merging, PyCharm will open a merge tool to select sections of code to keep.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ G. NEXT STEPS & BEST PRACTICES ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ • Commit often, use meaningful messages.
• Use branches for new features.
• Regularly pull from the main branch to avoid big merge conflicts.
• Leverage PyCharm’s Git integration for code reviews, merges, and conflict resolution.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ H. CONCLUSION ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ You now have:

A quick table-based summary.
A medium-depth quick explanation.
A full zero-to-hero step-by-step guide.