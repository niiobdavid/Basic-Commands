# Basic Git Commands

## Install Git
```bash
sudo dnf update
sudo dnf install git -y
```

| Command                          | Purpose                                  | Example                                                  |
| -------------------------------- | ---------------------------------------- | -------------------------------------------------------- |
| `git --version`                  | Check Git version                        | `git --version`                                          |
| `git config --global user.name`  | Set Git username                         | `git config --global user.name "John"`                   |
| `git config --global user.email` | Set Git email                            | `git config --global user.email "john@example.com"`      |
| `git config --list`              | View Git configuration                   | `git config --list`                                      |
| `git init`                       | Initialize a Git repository              | `git init`                                               |
| `git clone`                      | Clone a GitHub repository                | `git clone https://github.com/user/repo.git`             |
| `git status`                     | Check repository status                  | `git status`                                             |
| `git add`                        | Stage a file                             | `git add file.txt`                                       |
| `git add .`                      | Stage all changes in current directory   | `git add .`                                              |
| `git commit -m`                  | Commit staged changes                    | `git commit -m "Initial commit"`                         |
| `git log`                        | View commit history                      | `git log`                                                |
| `git log --oneline`              | View simplified commit history           | `git log --oneline`                                      |
| `git diff`                       | View unstaged changes                    | `git diff`                                               |
| `git diff --staged`              | View staged changes                      | `git diff --staged`                                      |
| `git branch`                     | List local branches                      | `git branch`                                             |
| `git branch <name>`              | Create a branch                          | `git branch feature-login`                               |
| `git switch`                     | Switch branches                          | `git switch main`                                        |
| `git switch -c`                  | Create and switch to a branch            | `git switch -c feature-login`                            |
| `git merge`                      | Merge branches                           | `git merge feature-login`                                |
| `git branch -d`                  | Delete a merged branch                   | `git branch -d feature-login`                            |
| `git remote -v`                  | Show remote repositories                 | `git remote -v`                                          |
| `git remote add origin`          | Connect to GitHub repository             | `git remote add origin https://github.com/user/repo.git` |
| `git push`                       | Upload commits to GitHub                 | `git push origin main`                                   |
| `git push -u`                    | Push and set upstream branch             | `git push -u origin main`                                |
| `git pull`                       | Download and integrate remote changes    | `git pull origin main`                                   |
| `git fetch`                      | Download remote changes without merging  | `git fetch origin`                                       |
| `git restore`                    | Discard unstaged changes                 | `git restore file.txt`                                   |
| `git restore --staged`           | Unstage a file                           | `git restore --staged file.txt`                          |
| `git reset --soft HEAD~1`        | Undo last commit, keeping changes staged | `git reset --soft HEAD~1`                                |
| `git revert`                     | Undo a commit with a new commit          | `git revert HEAD`                                        |
| `git stash`                      | Temporarily save changes                 | `git stash`                                              |
| `git stash pop`                  | Restore latest stashed changes           | `git stash pop`                                          |
| `git tag`                        | List tags                                | `git tag`                                                |
| `git tag <name>`                 | Create a version tag                     | `git tag v1.0`                                           |
| `git show`                       | Display commit details                   | `git show HEAD`                                          |
| `git rm`                         | Remove a tracked file                    | `git rm file.txt`                                        |
| `git mv`                         | Rename or move a tracked file            | `git mv old.txt new.txt`                                 |
| `git clean -n`                   | Preview removal of untracked files       | `git clean -n`                                           |
| `git help`                       | Display Git documentation                | `git help commit`                                        |

