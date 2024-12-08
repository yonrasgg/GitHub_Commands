### Extended Git Bash Commands and Their Functions

#### General Commands
- **`pwd`**: Displays the current directory path.
- **`cd`**: Navigates between directories. Use `..` to move up a level or `.` to stay in the current directory.
- **`ls` / `ll`**: Lists files and directories. `ll` includes file permissions and details.
- **`mkdir`**: Creates a new directory.
- **`touch`**: Creates a new, empty file.
- **`clear`**: Clears the terminal screen.
- **`rm` / `rmdir`**: Deletes a file or directory, respectively.

#### Repository Initialization and Cloning
- **`git init`**: Creates a new local Git repository.
- **`git clone [URL]`**: Copies a remote repository to your local machine.

#### File Management and Version Control
- **`git add [file]`**: Moves changes to the staging area for the next commit.
- **`git status`**: Displays the status of files in the working directory and staging area.
- **`git commit -m "[message]"`**: Records changes to the repository with a descriptive message.

#### Branch Management
- **`git branch [branch_name]`**: Creates a new branch.
- **`git checkout [branch_name]`**: Switches to the specified branch.
- **`git checkout -b [branch_name]`**: Creates a new branch and switches to it.
- **`git stash`**: Temporarily saves changes in the working directory without committing.
- **`git branch -d [branch_name]`**: Deletes a branch locally.

#### Synchronization
- **`git push [remote]`**: Sends committed changes to the remote repository.
- **`git pull [remote]`**: Retrieves and merges changes from a remote repository into the local one.
- **`git remote`**: Manages connections to remote repositories (add, view, or remove remotes).
- **`git fetch`**: Retrieves changes from the remote repository without merging them into the current branch.

#### Undo Changes
- **`git log`**: Lists the commit history.
- **`git diff [commit1] [commit2]`**: Shows differences between two commits.
- **`git reset [commit]`**: Reverts to a specific commit. Modes include:
  - `--soft`: Retains changes in the staging area.
  - `--mixed` (default): Retains changes in the working directory.
  - `--hard`: Discards all changes after the specified commit.
- **`git revert [commit]`**: Creates a new commit that undoes changes from a specified commit.

#### Rewriting History
- **`git commit --amend`**: Modifies the last commit by adding changes or updating its message.
- **`git rebase -i`**: Allows reordering, editing, or combining past commits.
- **`git cherry-pick [commit]`**: Applies a specific commit from another branch to the current branch.
- **`git merge --squash`**: Combines multiple commits into a single one before merging.

#### Tagging
- **`git tag [tag_name]`**: Creates a lightweight tag at the current commit.
- **`git tag -a [tag_name] -m "[message]"`**: Creates an annotated tag with a message.

#### Pull Requests (GitHub Feature)
- Notifies team members about new changes.
- Serves as a platform for code review and collaboration before merging changes.

#### Branch Integration
- **`git merge [branch_name]`**: Merges the specified branch into the current branch.
- **`git rebase [branch_name]`**: Reorganizes commit history by applying commits on top of the target branch.

