# Comprehensive Guide to Git Bash Commands and Best Practices

## General Commands
- **`pwd`**: Displays the current directory path.
- **`cd`**: Navigates between directories. Use `..` to move up a level or `.` to stay in the current directory.
- **`ls` / `ll`**: Lists files and directories. `ll` includes file permissions and details.
- **`mkdir`**: Creates a new directory.
- **`touch`**: Creates a new, empty file.
- **`clear`**: Clears the terminal screen.
- **`rm` / `rmdir`**: Deletes a file or directory, respectively.

## Repository Configuration
- **`git config --global user.name "[name]"`**: Sets the global username for commits.
- **`git config --global user.email "[email]"`**: Sets the global email for commits.
- **`git config --global`**: Displays the current global configuration for Git.

## Repository Initialization and Cloning
- **`git init`**: Initializes a new local Git repository.
- **`git clone [URL]`**: Clones a remote repository to your local machine.

## File Management and Version Control
- **`git add [file]`**: Moves changes to the staging area for the next commit.
  - Options:
    - **`-a`**: Adds all changes (modified, new, deleted).
    - **`-u`**: Stages modified and deleted files.
    - **`.`**: Adds all changes in the current directory.
- **`git commit -m "[message]"`**: Records changes to the repository with a descriptive message.
  - **`--amend`**: Edits the most recent commit.
- **`git status`**: Displays the status of files in the working directory and staging area.

## Branch Management
- **`git branch [branch_name]`**: Creates a new branch.
- **`git checkout [branch_name]`**: Switches to the specified branch.
- **`git checkout -b [branch_name]`**: Creates a new branch and switches to it.
- **`git branch -d [branch_name]`**: Deletes a branch locally.
- **`git stash`**: Temporarily saves uncommitted changes.

## Branch Types
- **Master Branch**: The main production-ready codebase.
- **Develop Branch**: A stable branch for continuous development.
- **Feature Branch**: Created for implementing a specific feature or bug fix.
- **Release Branch**: Used to prepare for a new production release.
- **Hotfix Branch**: Quickly patches critical issues in production.

## Synchronization
- **`git push [remote] [branch]`**: Sends committed changes to the remote repository.
- **`git pull [remote] [branch]`**: Retrieves and merges changes from a remote repository into the local one.
- **`git fetch`**: Retrieves changes from the remote repository without merging them into the current branch.
- **`git remote add [name] [URL]`**: Adds a remote repository.
- **`git remote -v`**: Lists remote connections.

## Undo Changes
- **`git reset [commit]`**: Reverts to a specific commit.
  - **`--soft`**: Retains changes in the staging area.
  - **`--mixed`**: Retains changes in the working directory.
  - **`--hard`**: Discards all changes after the specified commit.
- **`git revert [commit]`**: Creates a new commit that undoes changes from a specified commit.

## Rewriting History
- **`git commit --amend`**: Modifies the last commit by adding changes or updating its message.
- **`git rebase -i`**: Allows reordering, editing, or combining past commits.
- **`git cherry-pick [commit]`**: Applies a specific commit from another branch to the current branch.
- **`git merge --squash`**: Combines multiple commits into a single one before merging.

## Branch Integration
- **`git merge [branch_name]`**: Merges the specified branch into the current branch.
- **`git rebase [branch_name]`**: Reorganizes commit history by applying commits on top of the target branch.
- **Conflict Resolution**: Resolve merge conflicts manually in files before completing a merge.

## Tagging
- **`git tag [tag_name]`**: Creates a lightweight tag at the current commit.
- **`git tag -a [tag_name] -m "[message]"`**: Creates an annotated tag with a message.
- **`git tag`**: Lists all tags in the repository.

## Remote Branch Management
- **`git push origin [branch_name]`**: Pushes a branch to the remote repository.
- **`git pull origin [branch_name]`**: Pulls changes from a specific branch in the remote repository.
- **`git fetch origin`**: Fetches updates from the remote repository without merging.
- **Fast-Forward Merge**: Automatically updates a branch if no changes diverge.

## Workflow Strategies
- **Gitflow Workflow**: Uses specific branches (master, develop, feature, release, hotfix) to manage development.
- **Feature Isolation**: Use feature branches to isolate development.
- **Hotfixes**: Quickly fix critical issues by creating hotfix branches from the master.

## Pull Requests (GitHub Feature)
- Notifies team members about new changes.
- Serves as a platform for code review and collaboration before merging changes.

## Best Practices
- **Commit Regularly**: Keep commits small and related to simplify collaboration and rollbacks.
  - Avoid committing incomplete work; commit logical chunks of work.
- **Write Useful Commit Messages**: Provide clear and descriptive messages for easier collaboration and revision history.
  - Limit messages to 50-72 characters for better readability.
- **Use Branches**: Leverage Git’s branching capabilities to isolate development lines for features, bug fixes, and experiments.
- **Update Before Push**: Always `git pull` to sync your local repository with the remote before pushing changes.
- **Divide Work Into Repositories**: Use separate repositories for distinct projects, large files, or shared code to optimize development workflows.

## Additional Notes
- **`git log`**: Views the commit history.
- **`git diff`**: Displays changes between commits or the working directory and staging area.
- **`git show [commit]`**: Shows details about a specific commit.
