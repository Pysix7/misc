1. ```
      $ git status
   ```

   Gives a list of which files are staged, unstaged, and untracked

2. ```
   $ git log
   ```

Gives version history of commit for the branch

3. ```
   $ git diff
   ```

Displays the unstaged changes between index and working directory

4. ```
   $ git revert <commit>
   ```

Undoes all the changes made in <commit> and applies it to the current branch by creating a new commit

5. ```
   $ git reset
   $ git reset <file>
   $ git reset --hard
   ```

Removes changes from staging area to unstaged without overwriting any changes by keeping the working directory unchanged

- `<file>` from a staging area

- `--hard` removes staged and working directory changes (Be Cautious)

6. ```
   $ git clean -f -d # remove untracked
   $ git clean -f -x -d # CAUTION: as above but removes ignored files like config.
   $ git clean -fxd :/ # CAUTION: as above, but cleans untracked and ignored files through the entire repo (without :/, the operation affects only the current directory) T
   ```

7. ```
   $ git restore .
   ```

Removes/Discard unstaged tracked files changes, new files won't be discarded

8. ```
   $ git add <filename>
   $ git add .
   ```

Add a unstaged file to staging <file> adds a specific file, `.` adds all files

9. ```
   $ git commit -a
   $ git commit -m <commit message>
   $ git commit -a -m <commit message>
   $ git commit -am <commit message>
   ```

Commits staged files with a commit-message.

- `-a` commits changes to tracked files only (not new files) this opens editor where we need to specify the message.
- `-a -m` commits changes with message along with `-a` rule.
- `-am` commits changes message along with `-a` rule.
- `-m` commits all changes with a message

10. ```
    $ git checkout <branch-name>
    $ git checkout -b <branch-name>
    ```

Checkout to a branch with branch name.

- already existing branch with first command
- create new branch and checkout to newly created with second command `-b`

11. ```
    $ git branch -m <old-branch-name> <new-branch-name>
    ```

Rename a branch from `<old-branch-name>` to `<new-branch-name>`

12. ```
    $ git pull origin <branch-name>
    ```

Pull Remote repo (origin) changes of a branch to local repo branch.

12. ```
    $ git push origin <branch-name>
    $ git push origin <branch-name> -f
    ```

Push changes of local repo branch to Remote repo (origin).

- `-f` force pushed changes (this may overwrite some changes)(Be Cautious)