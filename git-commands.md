✅ Task 2: Branching Commands — Hands-On
🔹 1️⃣ List All Branches
git branch
Shows all local branches.
To see remote branches too:
git branch -a
🔹 2️⃣ Create a New Branch feature-1
git branch feature-1
This creates the branch but does NOT switch to it.
🔹 3️⃣ Switch to feature-1
git switch feature-1
Now check:
git branch
You should see * feature-1
🔹 4️⃣ Create and Switch in One Command (feature-2)
Modern way (recommended):
git switch -c feature-2
Old way:
git checkout -b feature-2
👉 Difference:
git switch is newer and only for switching branches.
git checkout does multiple things (switch branches + restore files), so it can be confusing.
🔹 5️⃣ Move Between Branches
git switch feature-1
git switch main

🔥 Difference Between switch and checkout
git switch	git checkout
Only for branch switching	Switch branches + restore files
Safer and clearer	Older and more powerful but confusing
Modern command	Legacy command
🔹 6️⃣ Make a Commit on feature-1
Switch to feature-1:
git switch feature-1
Edit a file (for example):
echo "Feature 1 work" >> branch-test.txt
Stage and commit:
git add .
git commit -m "Added work for feature-1"
🔹 7️⃣ Switch Back to main
git switch main
Now check:
cat branch-test.txt
👉 You will notice:
The changes from feature-1 are NOT here.
This proves branches are isolated.
🔹 8️⃣ Delete a Branch You Don’t Need
First move away from it:
git switch main
Then delete:
git branch -d feature-2
If Git refuses (because not merged):
git branch -D feature-2
✅ Add These to git-commands.md
Add this section:
Branching Commands
Create branch
git branch <branch-name>
Creates a new branch.
Switch branch
git switch <branch-name>
Switches to an existing branch.
Create + Switch
git switch -c <branch-name>
Creates and switches to branch in one command.
List branches
git branch
Shows local branches.
Delete branch
git branch -d <branch-name>
Deletes a branch.
🎯 What You Just Learned
Branches are isolated environments.
Commits in one branch don’t affect others.

switch is safer than checkout.

You must switch branches before deleting them.
