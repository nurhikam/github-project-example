# 📚 Git & GitHub Basics

Panduan dasar Git dan GitHub untuk GitHub Project Management.

## 📋 Daftar Isi

- [Apa itu Git & GitHub?](#apa-itu-git--github)
- [Setup Awal](#setup-awal)
- [Basic Commands](#basic-commands)
- [Repository Operations](#repository-operations)
- [Branching & Merging](#branching--merging)
- [Collaboration Workflow](#collaboration-workflow)
- [Best Practices](#best-practices)

---

## 🔍 Apa itu Git & GitHub?

### Git

**Git** adalah version control system untuk tracking perubahan kode.

**Fungsi:**

- 📝 Track history perubahan
- 🔄 Revert ke versi sebelumnya
- 👥 Collaboration dengan team
- 🌿 Branching untuk feature development

### GitHub

**GitHub** adalah platform hosting untuk Git repositories.

**Fungsi:**

- ☁️ Cloud storage untuk code
- 👥 Collaboration tools (Issues, PRs, Projects)
- 🔍 Code review
- 🤖 CI/CD dengan GitHub Actions

---

## 🚀 Setup Awal

### Install Git

**Windows:**

```bash
# Download dari https://git-scm.com/download/win
# Atau via Chocolatey
choco install git
```

**Mac:**

```bash
# Via Homebrew
brew install git
```

**Linux:**

```bash
# Ubuntu/Debian
sudo apt-get install git

# Fedora
sudo dnf install git
```

### Konfigurasi Git

```bash
# Set username
git config --global user.name "Nama Anda"

# Set email
git config --global user.email "email@example.com"

# Check konfigurasi
git config --list

# Set default editor (optional)
git config --global core.editor "code --wait"  # VS Code
```

### Setup SSH Key (Recommended)

```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "email@example.com"

# Start SSH agent
eval "$(ssh-agent -s)"

# Add SSH key
ssh-add ~/.ssh/id_ed25519

# Copy public key (paste ke GitHub Settings → SSH Keys)
cat ~/.ssh/id_ed25519.pub
```

---

## 💻 Basic Commands

### Check Status

```bash
# Lihat status repository
git status

# Status ringkas
git status -s
```

### Add & Commit

```bash
# Add file tertentu
git add filename.txt

# Add semua perubahan
git add .

# Add dengan pattern
git add *.js

# Commit dengan message
git commit -m "feat: add new feature"

# Add dan commit sekaligus (tracked files only)
git commit -am "fix: bug fix"

# Amend commit terakhir
git commit --amend -m "Updated message"
```

### View History

```bash
# Lihat commit history
git log

# History ringkas (1 line per commit)
git log --oneline

# History dengan graph
git log --graph --oneline --all

# History file tertentu
git log filename.txt

# Lihat perubahan di commit
git show commit-hash
```

### View Changes

```bash
# Lihat perubahan yang belum di-add
git diff

# Lihat perubahan yang sudah di-add
git diff --staged

# Compare branches
git diff branch1..branch2

# Compare dengan commit tertentu
git diff commit-hash
```

---

## 📦 Repository Operations

### Clone Repository

```bash
# Clone via HTTPS
git clone https://github.com/username/repo.git

# Clone via SSH
git clone git@github.com:username/repo.git

# Clone ke folder tertentu
git clone https://github.com/username/repo.git my-folder

# Clone branch tertentu
git clone -b branch-name https://github.com/username/repo.git
```

### Initialize Repository

```bash
# Buat repository baru
git init

# Buat dengan default branch 'main'
git init -b main

# Add remote
git remote add origin https://github.com/username/repo.git

# Push pertama kali
git push -u origin main
```

### Remote Operations

```bash
# Lihat remote
git remote -v

# Add remote
git remote add origin https://github.com/username/repo.git

# Change remote URL
git remote set-url origin new-url

# Remove remote
git remote remove origin

# Fetch from remote (tidak merge)
git fetch origin

# Pull from remote (fetch + merge)
git pull origin main

# Push to remote
git push origin main

# Push semua branches
git push --all origin
```

---

## 🌿 Branching & Merging

### Branch Operations

```bash
# Lihat branch
git branch

# Lihat semua branch (termasuk remote)
git branch -a

# Buat branch baru
git branch feature-name

# Switch ke branch
git checkout feature-name
# atau (Git 2.23+)
git switch feature-name

# Buat dan switch ke branch baru
git checkout -b feature-name
# atau
git switch -c feature-name

# Rename branch
git branch -m old-name new-name

# Delete branch
git branch -d feature-name

# Force delete branch
git branch -D feature-name

# Delete remote branch
git push origin --delete feature-name
```

### Merging

```bash
# Merge branch ke current branch
git merge feature-name

# Merge dengan no fast-forward (create merge commit)
git merge --no-ff feature-name

# Abort merge jika conflict
git merge --abort
```

### Rebasing

```bash
# Rebase current branch ke main
git rebase main

# Continue rebase setelah resolve conflict
git rebase --continue

# Skip commit saat rebase
git rebase --skip

# Abort rebase
git rebase --abort

# Interactive rebase (edit last 3 commits)
git rebase -i HEAD~3
```

---

## 👥 Collaboration Workflow

### Fork Repository

**Via GitHub Web:**

1. Go to repository
2. Click **Fork** button
3. Select your account
4. Clone forked repository

```bash
# Clone your fork
git clone https://github.com/your-username/repo.git
cd repo

# Add upstream remote
git remote add upstream https://github.com/original-owner/repo.git

# Verify remotes
git remote -v
```

### Sync Fork

```bash
# Fetch upstream changes
git fetch upstream

# Switch to main branch
git checkout main

# Merge upstream changes
git merge upstream/main

# Push to your fork
git push origin main
```

### Pull Request Workflow

```bash
# 1. Create feature branch
git checkout -b feature/new-feature

# 2. Make changes
# ... edit files ...

# 3. Commit changes
git add .
git commit -m "feat: add new feature"

# 4. Push to your fork
git push origin feature/new-feature

# 5. Create Pull Request via GitHub web
# Go to your fork → "Compare & pull request"

# 6. After PR merged, cleanup
git checkout main
git pull upstream main
git branch -d feature/new-feature
git push origin --delete feature/new-feature
```

### Keep Branch Updated

```bash
# Method 1: Merge
git checkout main
git pull origin main
git checkout feature-branch
git merge main

# Method 2: Rebase (cleaner history)
git checkout feature-branch
git rebase main
```

---

## 🎯 Common Scenarios

### Undo Changes

```bash
# Undo changes di working directory
git checkout -- filename.txt
# atau (Git 2.23+)
git restore filename.txt

# Undo staged changes (keep changes in working directory)
git reset HEAD filename.txt
# atau
git restore --staged filename.txt

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Undo last commit (discard changes)
git reset --hard HEAD~1

# Revert commit (create new commit)
git revert commit-hash
```

### Stash Changes

```bash
# Stash perubahan
git stash

# Stash dengan message
git stash save "work in progress"

# List stashes
git stash list

# Apply latest stash (keep in stash)
git stash apply

# Apply latest stash (remove from stash)
git stash pop

# Apply specific stash
git stash apply stash@{2}

# Drop specific stash
git stash drop stash@{0}

# Clear all stashes
git stash clear
```

### Fix Mistakes

```bash
# Change last commit message
git commit --amend -m "New message"

# Add forgotten files to last commit
git add forgotten-file.txt
git commit --amend --no-edit

# Cherry-pick commit dari branch lain
git cherry-pick commit-hash

# Reset to remote state
git fetch origin
git reset --hard origin/main
```

---

## ✅ Best Practices

### Commit Messages

**Format:**

```
<type>: <subject>

<body>

<footer>
```

**Types:**

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation
- `style:` Formatting
- `refactor:` Code refactoring
- `test:` Tests
- `chore:` Maintenance

**Examples:**

```bash
git commit -m "feat: add user authentication"
git commit -m "fix: resolve login button bug"
git commit -m "docs: update README with setup instructions"
```

### Branch Naming

```
feature/feature-name
fix/bug-description
hotfix/critical-fix
release/version-number
docs/documentation-update
```

**Examples:**

```bash
git checkout -b feature/user-authentication
git checkout -b fix/login-button-bug
git checkout -b docs/readme-update
```

### Git Workflow Tips

1. **Commit Often**

   - Small, focused commits
   - Easy to review
   - Easy to revert

2. **Pull Before Push**

   ```bash
   git pull origin main
   git push origin main
   ```

3. **Use Branches**

   - Don't work directly on main
   - One branch per feature/fix
   - Delete after merge

4. **Review Before Commit**

   ```bash
   git status
   git diff
   ```

5. **Write Good Commit Messages**
   - Clear and descriptive
   - Explain why, not just what

---

## 🔗 Integration dengan GitHub Projects

### Link Commits ke Issues

```bash
# Di commit message, reference issue number
git commit -m "fix: resolve login bug

Fixes #123"

# Multiple issues
git commit -m "feat: add feature

Closes #45, closes #67"
```

**Keywords:**

- `fixes` / `fixed` / `fix`
- `closes` / `closed` / `close`
- `resolves` / `resolved` / `resolve`

### Link PRs ke Project Items

Di PR description:

```markdown
## Description

Fix authentication bug

## Related Issues

Fixes #123
Related to #124

## Project Board

- Moves to "In Review" when opened
- Moves to "Done" when merged
```

---

## 📚 Resources

### Official Documentation

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/)
- [Pro Git Book](https://git-scm.com/book/en/v2) (Free)

### Interactive Learning

- [Learn Git Branching](https://learngitbranching.js.org/)
- [GitHub Learning Lab](https://lab.github.com/)
- [Git Immersion](https://gitimmersion.com/)

### Cheat Sheets

- [GitHub Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Atlassian Git Cheat Sheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)

### Visual Tools

- [GitHub Desktop](https://desktop.github.com/) - GUI untuk Git
- [GitKraken](https://www.gitkraken.com/) - Visual Git client
- [Sourcetree](https://www.sourcetreeapp.com/) - Free Git GUI

---

## ❓ Troubleshooting

### Common Issues

**Problem: Merge Conflict**

```bash
# 1. Lihat conflicted files
git status

# 2. Edit files, resolve conflicts
# Look for <<<<<<< HEAD markers

# 3. Mark as resolved
git add resolved-file.txt

# 4. Complete merge
git commit
```

**Problem: Accidentally committed to wrong branch**

```bash
# 1. Stash changes
git reset --soft HEAD~1
git stash

# 2. Switch to correct branch
git checkout correct-branch

# 3. Apply stash
git stash pop
git commit -m "message"
```

**Problem: Need to undo pushed commit**

```bash
# Create revert commit (safe, recommended)
git revert commit-hash
git push origin main

# Force push (dangerous, use with caution)
git reset --hard HEAD~1
git push origin main --force
```

---

## 🎓 Next Steps

Setelah menguasai Git basics:

1. **Practice**: Buat test repository dan practice commands
2. **Learn GitHub Flow**: Understand PR workflow
3. **Explore GitHub Projects**: Integrate Git dengan project management
4. **Setup Automation**: GitHub Actions untuk CI/CD
5. **Team Collaboration**: Practice dengan team

**Related Guides:**

- [GitHub Flow](https://guides.github.com/introduction/flow/)
- [Team Collaboration Guide](../exercises/06-team-collaboration.md)
- [Contributing Guidelines](../CONTRIBUTING.md)

---

**Happy Git-ing! 🚀**

Need help? Open an issue atau discussion di repository ini!
