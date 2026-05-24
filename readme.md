# GitHub for Absolute Beginners

A step-by-step guide for students using **VS Code** or **Google Antigravity** with the GitHub extension.

---

## What is Git? What is GitHub?

| Term | What it means |
|---|---|
| **Git** | Software installed on your computer that tracks every change you make to your files — like an unlimited "undo" for your entire project. |
| **GitHub** | A website that stores your Git-tracked project online so your whole team can share, sync, and collaborate. |
| **Repository (repo)** | A project folder that Git is tracking. Think of it as a special project folder that remembers its own history. |
| **Commit** | A saved snapshot of your changes, with a short message describing what you did. |
| **Push** | Uploading your local commits to GitHub so teammates can see them. |
| **Pull** | Downloading the latest changes from GitHub to your computer. |
| **Branch** | A parallel copy of the project where you can work without affecting the main version. |
| **Pull Request (PR)** | A request to merge your branch's changes into the main branch, usually reviewed by a teammate first. |

---

## Step 0 — Create a GitHub Account

1. Go to [https://github.com](https://github.com)
2. Click **Sign up**
3. Enter your email, create a password, and choose a username
4. Verify your email address
5. Keep your username professional — it goes on your resume

---

## Step 1 — Install Your IDE and the GitHub Extension

Choose **one** of the two options below. Both work identically for the rest of this guide — the steps are the same unless noted otherwise.

---

### Option A — VS Code

1. Download VS Code from [https://code.visualstudio.com](https://code.visualstudio.com) and install it
2. Open VS Code
3. Click the **Extensions** icon in the left sidebar (it looks like four squares)
4. Search for **GitHub Pull Requests**
5. Click **Install** on the extension published by **GitHub**
6. Restart VS Code when prompted

> VS Code already has Git support built in — you do not need a separate Git extension.

---

### Option B — Google Antigravity

1. Download Antigravity from [https://antigravity.google](https://antigravity.google) and install it
2. Open Antigravity
3. Click the **Extensions** icon in the left sidebar
4. Search for **GitHub Pull Requests**
5. Click **Install** on the extension published by **GitHub**
6. Restart Antigravity when prompted

> Antigravity is built on VS Code, so all menus, panels, and keyboard shortcuts in this guide work the same way.

---

## Step 2 — Install Git on Your Computer

The IDE uses Git behind the scenes, so Git must be installed on your machine.

1. Go to [https://git-scm.com/downloads](https://git-scm.com/downloads)
2. Download and run the installer for your operating system
3. Accept all the default settings during installation
4. To confirm Git installed correctly:
   - In your IDE, open the Terminal: **View → Terminal** (or press `` Ctrl+` ``)
   - Type `git --version` and press Enter
   - You should see something like `git version 2.x.x` — if so, you are good to go

---

## Step 3 — Sign In to GitHub Inside Your IDE

1. Click the **Accounts** icon (bottom left corner of VS Code. top right corner of Antigravity).
2. Click **Sign in with GitHub**
3. Your browser will open and ask you to authorize the IDE
4. Click **Authorize** and follow the prompts
5. Return to your IDE — you should now see your GitHub username in the bottom bar

---

## Step 4 — Clone the Class Repository

"Cloning" means downloading a copy of a GitHub repository to your computer.

1. Go to the class repository on GitHub and click the green **Code** button
2. Make sure **HTTPS** is selected, then click the copy icon to copy the URL
3. In your IDE, open the Terminal: **View → Terminal** (or press `` Ctrl+` ``)
4. Navigate to the folder where you want to save the project. For example, to save it on your Desktop:
   ```
   cd Desktop
   ```
5. Run the clone command, replacing the URL with the one you copied:
   ```
   git clone https://github.com/username/repo-name.git
   ```
6. Move into the newly created project folder:
   ```
   cd repo-name
   ```
7. Open the folder in your IDE:
   ```
   code .
   ```

You will now see the project files in the left sidebar.

---

## Step 5 — Make a Change to a File

1. In the left sidebar, click on any file to open it
2. Make a small edit — for example, add your name to a line in the file
3. Save the file: **File → Save** or `Ctrl+S`

You will notice the file name in the sidebar turns **yellow/orange** with an **M** beside it. That **M** stands for "Modified" — Git has noticed your change.

---

## Step 6 — Commit Your Change (Save a Snapshot)

Committing saves a permanent snapshot of your changes in your local Git history.

1. Click the **Source Control** icon in the left sidebar (looks like a branch/fork)
2. You will see your modified file listed under **Changes**
3. Hover over the file and click the **+** button to **stage** it — this tells Git "include this file in my next commit"
4. The file moves up to **Staged Changes**
5. Click into the text box at the top that says **Message** and type a short description of what you changed — for example: `Add my name to the contributors list`
6. Click the **Commit** button (the checkmark ✓) or press `Ctrl+Enter`

Your change is now saved as a commit in your local history.

---

## Step 7 — Push Your Commit to GitHub

Pushing sends your local commits up to GitHub so your teammates can see them.

1. In the Source Control panel, click the **three-dot menu (...)** at the top right
2. Click **Push**
3. If prompted to sign in or authorize, follow the on-screen steps
4. Go to your repository on GitHub.com and refresh the page — you should see your change

> **Shortcut:** The blue **Sync Changes** button at the bottom status bar does a Pull + Push in one click. This is the easiest option for most situations.

---

## Step 8 — Pull Changes from Teammates

Before you start working each session, always download the latest version from GitHub first.

1. In the Source Control panel, click the **three-dot menu (...)**
2. Click **Pull**
3. Your local files will update with any changes your teammates pushed

> If you skip this step and a teammate has pushed changes, Git may warn you about conflicts. Get into the habit of pulling first thing every time.

---

## Step 9 — Work on a Branch (Team Collaboration)

Branches let each team member work independently without breaking the main project. **Never commit directly to `main` or `master`** on a team project.

### Create a new branch

1. Click the **branch name** shown in the very bottom-left of your IDE window (it probably says `main` or `master`)
2. Click **Create new branch...**
3. Type a short descriptive name — for example: `feature/add-login-page` or `fix/typo-in-readme`
4. Press Enter — you are now on your new branch

### Work and commit on your branch

Follow Steps 5–7 as normal. Your commits go onto your branch and do not affect `main` or `master`.

### Push your branch to GitHub

1. Source Control panel → three-dot menu → **Push**
2. If prompted to publish the branch, click **OK**

---

## Step 10 — Open a Pull Request

A Pull Request (PR) lets a teammate review your work before it is merged into `main` or `master`.

1. Go to your repository on [GitHub.com](https://github.com)
2. GitHub will show a yellow banner: **"Your branch had recent pushes"** — click **Compare & pull request**
3. Write a clear title and description of what you changed and why
4. On the right side, assign a **Reviewer** (a teammate)
5. Click **Create pull request**

Your teammate will review the changes, leave comments if needed, and click **Merge pull request** when it is approved.

---

## Step 11 — Merge a Pull Request (Reviewer's job)

1. Open the Pull Request on GitHub
2. Read through the **Files changed** tab to review what was modified
3. Leave comments on any lines that need clarification (click the **+** that appears when hovering over a line)
4. If everything looks good, click **Review changes → Approve → Submit review**
5. Click **Merge pull request → Confirm merge**
6. Click **Delete branch** to keep the repository tidy

---

## Common Issues and Fixes

| Problem | What to do |
|---|---|
| `git --version` shows an error | Git is not installed — go back to Step 2 |
| Push is rejected ("non-fast-forward") | You forgot to Pull first — run a Pull, then Push again |
| File shows **U** (Untracked) in Source Control | The file is new and has never been committed — stage it with **+** |
| Merge conflict warning | Two people edited the same lines — open the file, look for `<<<< HEAD` markers, choose which version to keep, save, stage, and commit |
| "Author identity unknown" error in terminal | Run these two commands once: `git config --global user.email "you@example.com"` and `git config --global user.name "Your Name"` |
| Changes disappeared after switching branches | Your changes were not committed — always commit before switching branches |

---

## Quick Reference — Most Used Commands

| Action | How to do it in the IDE | Terminal shortcut |
|---|---|---|
| Clone a repo | Command Palette → `Git: Clone` | `git clone <url>` |
| See what changed | Source Control panel | `git status` |
| Stage a file | Click **+** next to the file | `git add filename` |
| Commit | Type message + click checkmark | `git commit -m "message"` |
| Push | Source Control ··· → Push | `git push` |
| Pull | Source Control ··· → Pull | `git pull` |
| Create branch | Click branch name → New branch | `git checkout -b branch-name` |
| Switch branch | Click branch name → select branch | `git checkout branch-name` |

---

> **Remember:** Git tracks history — you can almost always recover from mistakes. When in doubt, commit early and often, and always Pull before you start working.

---

---

# Team Exercises

Work through these exercises in order with your team of 3–4 people. Assign roles before you start.

| Role | Who does it |
|---|---|
| **Team Lead** | One person — responsible for setup and inviting teammates |
| **Member B** | Second person |
| **Member C** | Third person |
| **Member D** | Fourth person (if your team has 4) |

---

## Exercise 1 — Fork the Class Repo and Invite Your Team

**Who does this:** Team Lead only

Your team needs its own copy of the class repo that everyone can push to. The cleanest way to do this is to **fork** it — forking creates a copy of the repo under your own GitHub account, making you the owner.

### Team Lead steps

1. Go to the class repository on GitHub (your instructor will share the URL)
2. Click **Fork** (top-right corner of the page)
3. Leave all settings as default and click **Create fork**
4. You now have your own copy at `https://github.com/YOUR-USERNAME/repo-name`
5. Clone your forked repo to your computer (follow Step 4 of the main guide, but use your fork's URL)

### Add teammates as collaborators

6. On your forked repo page on GitHub, click **Settings**
7. In the left menu click **Collaborators**
8. Click **Add people**
9. Search for each teammate's GitHub username and click **Add [username] to this repository**
10. Set their permission level to **Write** (this gives full push access)
11. Each teammate will receive an email invitation — they must accept it before they can push

### Teammates — accept the invitation

12. Check your email for an invitation from GitHub, or go to `https://github.com/notifications`
13. Click **Accept invitation**
14. Confirm with the Team Lead that all invitations are accepted before moving on

---

## Exercise 2 — Everyone Clones and Introduces Themselves

**Who does this:** All team members (including Team Lead)

Each person clones the Team Lead's forked repo and adds their name to a shared file.

> **Important:** The Team Lead already cloned the repo in Exercise 1. Skip the clone step and start from step 3.

### Steps for Members B, C, and D

1. Get the Team Lead's forked repo URL (ask them to share it, or find it on GitHub)
2. Clone it to your computer:
   ```
   git clone https://github.com/TEAM-LEAD-USERNAME/repo-name.git
   cd repo-name
   code .
   ```

### All team members (including Team Lead)

3. Create a new file named `team/YOUR-STUDENT-ID-NAME.md` — for example `team/113403999-mike.md`
4. Inside the file, write two lines:
   ```
   # Hi, I'm Mike
   I am a student in IM2002 and this is my first GitHub commit.
   ```
5. Save the file, stage it, commit it with the message `Add intro for [your name]`, and push
6. Once all team members have pushed, everyone should run a **Pull** to get the full set of intro files

**Check:** Go to the repo on GitHub. You should see a `team/` folder with one file per person.

---

## Exercise 3 — Branch Workflow: Everyone Works in Parallel

**Who does this:** All team members simultaneously

This exercise practices the correct team workflow — each person works on their own branch so no one blocks anyone else.

### Each team member does the following independently

1. Pull the latest changes first:
   ```
   git pull
   ```
2. Create your own branch. Use your name in the branch name:
   ```
   git checkout -b feature/YOUR-NAME-update
   ```
3. Open your intro file from Exercise 2 (`team/YOUR-STUDENT-ID-NAME.md`)
4. Add a third line describing one thing you want to learn in this course — for example:
   ```
   I want to learn how to manage a database-backed project as a team.
   ```
5. Save, stage, commit, and push your branch:
   ```
   git add team/YOUR-STUDENT-ID-NAME.md
   git commit -m "Update intro with learning goal"
   git push -u origin feature/YOUR-NAME-update
   ```
6. Go to the repo on GitHub and open a Pull Request from your branch into `main` or `master` (follow Step 10 of the main guide)
7. In the Pull Request description, tag a specific teammate as reviewer using `@their-username`

**Check:** The repo on GitHub should now have 3–4 open Pull Requests, one from each team member.

---

## Exercise 4 — Review and Merge a Teammate's Pull Request

**Who does this:** All team members — each person reviews someone else's PR

1. Go to the **Pull Requests** tab on the repo's GitHub page
2. Open a PR that was opened by a teammate (not your own)
3. Click the **Files changed** tab to see what they edited
4. Leave at least one comment on a specific line — click the **+** icon that appears when you hover over a line, and write something like: `Looks good! I'd also like to learn that.`
5. Click **Review changes**, select **Approve**, and click **Submit review**
6. Click **Merge pull request → Confirm merge**
7. Click **Delete branch** after merging

**Coordinate with your team so each PR gets reviewed by a different person — nobody merges their own PR.**

**Check:** All branches should be merged and deleted. The `main` or `master` branch should now contain all four updated intro files.

---

## Exercise 5 — Create and Resolve a Merge Conflict

**Who does this:** Two team members (pick any two — call them Person X and Person Y)

A merge conflict happens when two people edit the exact same line of the same file. This exercise makes one happen on purpose so you can learn to fix it.

### Setup — both Person X and Person Y do this independently at the same time

1. Pull the latest `main` or `master`:
   ```
   git pull
   ```
2. Create a new branch:
   - Person X: `git checkout -b conflict/person-x`
   - Person Y: `git checkout -b conflict/person-y`
3. Both open the file `team/shared-notes.md` (create it if it does not exist yet with just a heading: `# Shared Notes`)
4. Both add a line **at the very end of the file** — but write different things:
   - Person X writes: `Person X was here first.`
   - Person Y writes: `Person Y was here first.`
5. Both save, stage, commit, and push their branch
6. Both open a Pull Request into `main` or `master`

### Resolving the conflict

7. Whoever opens their PR **second** will see a message: **"This branch has conflicts that must be resolved"**
8. Click **Resolve conflicts**
9. GitHub will highlight the conflict with markers:
   ```
   <<<<<<< conflict/person-y
   Person Y was here first.
   =======
   Person X was here first.
   >>>>>>> main
   ```
   > Note: your repo may show `master` instead of `main` — both are correct.
10. Edit the file to keep **both lines** (delete the `<<<<<<<`, `=======`, and `>>>>>>>` markers):
    ```
    Person X was here first.
    Person Y was here first.
    ```
11. Click **Mark as resolved**, then **Commit merge**
12. The PR can now be merged normally

**Check:** The `team/shared-notes.md` file on `main` or `master` should contain both lines.

---

## Exercise Completion Checklist

At the end of all exercises, verify the following on the GitHub repo:

- [ ] A `team/` folder exists with one intro file per team member
- [ ] All intro files contain a learning goal (added in Exercise 3)
- [ ] The commit history shows commits from every team member
- [ ] All feature branches have been merged and deleted
- [ ] `team/shared-notes.md` contains a line from both Person X and Person Y
- [ ] Every team member has at least one merged Pull Request in the repo history
Hello I am Kiki