Purpose: This revision sheet gives the commands in practical order, with a simple explanation of what each command does.

Use your own project folder, file names, GitHub username and repository URL during the exam.

1. Check Git installation

git --version

Shows whether Git is installed and displays its version.

2. Configure your Git identity

git config --global user.name "Your Name"

git config --global user.email "your@email.com"

git config --list

Meaning: Sets the name and email recorded with your commits.

--global applies these settings to all Git projects for your user account.

git config --list displays configured settings.

3. Open your project folder

cd ~/Downloads/MyFirstGitProject

pwd

cd means Change Directory; it moves into the project folder.

pwd means Present Working Directory; it displays your current location.

Replace the example path with your actual folder path.

4. Initialize a Git repository

git init

Initializes Git in the current folder and creates the hidden .git directory, which stores repository information and history.

5. Check repository status

git status

Shows the current branch and files that are untracked, modified, staged, or already committed.

Working tree clean means there are no pending changes.

6. Add files to the staging area

git add student.txt

git add about.txt

git add hobbies.txt

Or stage all changes:

git add .

git add stages selected changes so they can be included in the next commit.

Use the actual file names in your project.

The dot in git add . means all changes in the current directory and its subdirectories.

7. Create the first commit

git commit -m "Initial Commit"

Creates a saved snapshot of the staged changes in the local repository.

-m supplies a short commit message describing the change.

Slide 2
8. Check status and commit history

git status

git log

git log --oneline

git log displays detailed commit history.

git log --oneline displays a compact one-line summary for each commit.

Remember: git log --oneline is correct; git --oneline is incorrect.

9. Connect the local repository to GitHub

git remote add origin https://github.com/USERNAME/REPOSITORY.git

git remote -v

First create a repository on GitHub and copy its HTTPS URL.

remote manages remote connections; add adds one; origin is the conventional nickname for the remote repository.

git remote -v displays the configured remote URL for fetch and push.

Important: Do not use the sample URL literally.

Replace it with your own GitHub repository URL.

If origin is already configured, do not add it again.

10. Rename the current branch to main

git branch -M main

git branch

git branch -M main renames the current branch to main.

git branch lists local branches; the asterisk marks the current branch.

11. Push the first commit to GitHub

git push -u origin main

Uploads the local main branch to the remote named origin.

-u sets the upstream tracking relationship, so later pushes can usually use just git push.

GitHub may open a browser sign-in/authorization window.

12. Modify a file and inspect the changes

git diff

After editing a tracked file, git diff shows differences between the working copy and the staged/committed version.

Lines beginning with + are additions.

Lines beginning with - are removals.

13. Stage, commit and push the update

git add about.txt

git status

git commit -m "Update about file"

git push

Stages the modified file, checks its status, saves a new commit, and uploads that commit to GitHub.

Replace about.txt with the file you actually edited.

14. Final verification

git log --oneline

git status

Check that the new commit appears in the history and that the working tree is clean.

You can also open your GitHub repository in a browser to confirm the uploaded files and latest commit.
