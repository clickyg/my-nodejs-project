# Working with GitHub from Multiple Locations — Starter Pack

This pack helps you complete the assignment quickly. It includes:
- `README.md` (this file) with the exact commands to use
- `exercise/sample.txt` (for practicing pull/revert/reset)
- `answers.md` (short answers to the 3 questions)

---

## Part 1 — Getting code on a new machine

### Case A: You do **not** have the repo locally yet (use `git clone`)
```bash
git clone https://github.com/<YOUR_USERNAME>/<YOUR_REPO>.git
cd <YOUR_REPO>
```

### Case B: You already have the repo locally (use `git pull`)
```bash
cd <YOUR_REPO>
git pull origin main   # if your default branch is 'main'
# (use 'master' if your repo uses master)
```

---

## Part 2 — View commit history and roll back

### View commit history
```bash
git log
```
Copy the commit hash you want to target (the long hex string).

### Method 1: Roll back HARD to a prior commit (dangerous, deletes later commits)
```bash
git reset --hard <commit-hash>
```
> ⚠️ This **rewrites history** and removes commits after `<commit-hash>` from your current branch.
> Do **not** use this on shared branches unless you know what you’re doing.

### Method 2: Revert safely without deleting history
```bash
git revert <commit-hash>
```
This creates a new commit that undoes changes from `<commit-hash>` while preserving history — preferred for teamwork.

---

## Quick practice (optional)
1) Open `exercise/sample.txt` and change the last line (e.g., add today's date).
2) Save and commit:
```bash
git add .
git commit -m "Edit sample.txt for practice"
git push
```
3) Use `git log` to see your new commit.
4) Try `git revert <hash>` for that commit to undo it safely (creates a new commit).
5) Or try `git reset --hard <older-hash>` locally to jump back in time (then `git push -f` if you truly intend to overwrite remote — usually **avoid** on a shared repo).

---

## Hand-in
- Push this `README.md` and `answers.md` into your repository.
- Provide the GitHub repository link in Google Classroom.
