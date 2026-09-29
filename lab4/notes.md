# Lab 4 Notes

## Question 1
The `--global` flag sets user configuration globally across all repositories on your system account. If omitted, the settings apply only locally to the current repository (`.git/config`).

## Question 2
`ls -a` reveals the hidden `.git` directory. Inside, Git stores repository configuration settings, object databases, branch references, and the staging index.

## Question 3
Git offers to track all untracked files in the directory, which can count in the thousands if a virtual environment exists. Files in `.venv/` represent third-party library code not written by the user.

## Question 4
The `.venv/` directory and temporary files disappeared from the "Untracked files" list in `git status`. Only `.gitignore` and project source files remain listed.

## Question 5
`.gitignore` should be committed so that exclusion rules are shared across all clones and collaborators. This prevents teammates from accidentally committing virtual environments and cache files.

## Question 6
`README.md` moved from "Untracked files" to "Changes to be committed". In the three-places model, the file's current state moved from the working directory into the staging area (index).

## Question 7
`git commit` output the commit's short hash, branch name (`main`), commit message, and summary details including the number of files changed, insertions, and deletions.

## Question 8
The first seven characters are the short SHA hash of the commit. They serve as a unique identifier to reference, inspect, or revert to that exact snapshot in history.

## Question 9
The four steps of the cycle are: 1) Edit files in the working directory, 2) Check repository status (`git status`), 3) Stage changes (`git add <file>`), and 4) Save the snapshot (`git commit -m "message"`).

## Question 10
`README.md` is placed at the root directory because hosting platforms like GitHub automatically render it as the formatted homepage documentation for the repository.

## Question 11
`gh auth login` authenticates via an OAuth token or SSH key pair stored locally. Git automatically uses these credentials for remote operations, eliminating future password prompts.

## Question 12
`README.md` is rendered on the repository's front page. GitHub looks for this specific file in the root directory by default and formats its Markdown as styled HTML.

## Question 13
Running `git push` uploads local commits to the remote repository without altering local commit history. It only updates the local tracking reference (`origin/main`) to match your current branch tip.

## Question 14
A private repository exists securely on GitHub's servers with full commit history, accessible only to the owner and invited collaborators. A non-existent repository does not exist online at all, meaning no remote access or history exists.
