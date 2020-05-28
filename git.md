# Git

## General
- [GitHub Learning Lab](https://lab.github.com/)
- [Think Like a Git](http://think-like-a-git.net/) - Really good explanation for "medium" level users
- [Git Internals](https://github.com/pluralsight/git-internals-pdf/releases)

## Articles
- [How to Become a Git Expert](https://link.medium.com/yEfwpuWs8R)
- [Git Aliases](https://medium.freecodecamp.org/an-intro-to-git-aliases-a-faster-way-of-working-with-git-b1eda81c7747)
- [Syncing GitLab and GitHub Repos](https://everythingshouldbevirtual.com/git/syncing-gitlab-and-github-repos/)

## Notes
- git pull = git fetch + git merge origin/master
- `git log --oneline --abbrev-commit --all --graph --decorate --color`

- References are pointers to commits
  - Local branch
    - `commit`, `merge`, `rebase`, `reset`
  - Remote branch
    - `fetch`, `push`, `pull`
  - Tag
    - Never move

- `git commit --amend` is actually building a new commit, and pointing your local branch to that instead
- `git gc` - force garbage collections (e.g. cleaning up original commits from situation described above)
  - Does this through a graph traversal, cuts off everything it can't reach
    - Starts at every branch and every tag
    - References make commits reachable
- You can use a branch as a save point because it will make a reference to your commit, so it's reachable
  - Won't be undone by `git merge` or `git rebase`
- `git cherry-pick` will take a commit from another place and 'replay' it where you are
  - Takes the diff from commit to parent and applies it at current position
- `git reset foo` will force the current branch's pointer to foo (`--hard` will update the working directory as well)
- `git rebase` will move entire sections to somewhere else
  - `git rebase foo bar` is equivalent to:
    ```
    git checkout foo
    git checkout -b newbar
    git cherry-pick C D E
    git checkout bar
    git reset --hard newbar
    git branch -d newbar
    ```
- Commits point to trees
- Objects (immutable)
  - Blob - contents of a file
  - Tree - collection of blobs and other trees
  - Commit - collection of blobs and trees, with some added data (like parent commit)
  - Tag - shorthand for a specific commit
- References
  - Branch
    - Points to SHA of the most recent commit
  - Remote
  - HEAD - points to current branch
- Treeish
  - Date spec
    - `master@{yesterday}` or `master@{1 month ago}`
     - This example would refer to the value of that branch yesterday. Importantly, this is the value of that branch in your repository yesterday. This value is relative to your repo – your `master@{yesterday}` will likely be different than someone else’s, even on the same project, whereas the SHA-1 values will always point to the same commit in every copy of the repository.
  - Ordinal spec
    - `master@{5}``
    - This indicates the 5th prior value of the master branch. Like the Date Spec, this depends on special files in the .git/log directory that are written during commits, and is specific to your repository.
  - Caret Parent
    - `e65s46^2` or `master^2`
    - This refers to the Nth parent of that commit. This is only really helpful for - commits that merged two or more commits – it is how you can refer to a commit other than the first parent.
  - Tilde spec
    - `e65s46~5`
    - The tilde character, followed by a number, refers to the Nth generation grandparent of that commit. To clarify from the caret, this is the equivalent commit in caret syntax: `e65s46^^^^^``
  - Tree pointer
    - `e65s46^{tree}`
    - This points to the tree of that commit. Any time you add a `^{tree}` to any commit-ish, it resolves to its tree.
  - Blob spec
    - `master:/path/to/file44`
    - This is very helpful for referring to a blob under a particular commit or tree.
- Your configuration will be loaded first from this `.git/config`, then from a `~/.gitconfig` file and then from an `/etc/gitconfig` file, if they exist.
