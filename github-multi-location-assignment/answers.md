# Short Answers

**1) `git clone` vs `git pull`**
- `git clone`: copies an entire remote repository to your computer for the first time.
- `git pull`: updates your existing local repository with the latest changes from the remote.

**2) `git revert` vs `git reset`**
- `git revert`: creates a new commit that undoes a previous commit without deleting history (safe for shared work).
- `git reset`: moves the current branch pointer to a previous commit and discards later commits from that branch (can rewrite history).

**3) Team scenario — which to use?**
- Use **`git revert`**. It preserves history and avoids breaking others' clones.
