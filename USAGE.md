# How to Use Git Bash

Hi, this is Captain Liv speaking, and we'll learn how to use one of software developer's backbone: Git Bash!

To do your weekly submission and final project, I recommend using Git Bash to change your repository. Compared to Github for Windows, Git Bash is easy to learn yet hard to master, and there's a lot of tools that will help you in the future (like mastering bash commands of squashing unnecessary commits).

Also, by using Git Bash, you can publish a lot of files in one commit, instead of having 21 commits just to edit one README.md. If you have me as your supervisor, I'll fire you for having _that much_ unnecessary commits.

Oh, and one important thing: as I usually work with Linux more than Windows, the steps I've written might be lacking for Windows users. Anyone can improve this guide. **If your improvements are accepted, you will receive extra points**, so do your best!

## Installation
- Download and install [Git Bash](https://git-scm.com/downloads)
- Open Git Bash (it is recommended to add Git Bash into your PATH variables)
- Setup your username and email  
  ```
  git config --global user.name <your username here>
  git config --global user.email <your email here>
  ```

## Weekly Submission
- Open your repo, where you put your weekly submission
- On the right side, there's a green button named `Clone or download`. Copy the link.
- Clone your git repo `git clone <copied link>`
- Change your working directory to your repo `cd <repo name>`. This is why we should not use space in file and folder names.
- Create new folder according to the convention `mkdir Week##-<topic>`
- Change your working directory to the newly-created folder `cd Week##-<topic>`
- Create your README.md `touch README.md`
- Now that the folder has existed, you can insert your source codes into the folder.
- Use your favorite text editor to edit your README.md. My editor is Sublime Text with these plugins: MarkdownEditing and MarkdownPreview, but you can definitely use the ol' plain Notepad if you want to. Here's a format you can follow:
```
# Week <week number>- <topic> by <your name here>

## [<Name of the problem>](<link to your solution>)

<thought process>
```
- Here's where you might realize you need to create `.gitignore`.
  - Change your working directory to your repo
  - Create the gitignore `.gitignore`. It's usually invisible from your explorer, so you'll probably need a dedicated text editor to access it.
  - Open your `.gitignore` in your favorite text editor (or you can use Vim directly from Git Bash if you want to).
  - Insert every file with certain extension you don't want to include in your repo. For example, if you're working with Code::Blocks, you might want to include these  
  ```
  ### CodeBlocks ###
  # specific to CodeBlocks IDE
  *.layout
  *.depend
  *.cbp
  # generated directories
  bin/
  obj/
  ```
- After you've finished editing, make Git tracks your new files `git add .`. This will make Git tracks every files, except for ones you've specified in `.gitignore`. You can do this multiple time before committing.
- Before commit, make sure you run `git pull` first. This will update your local files with the newest ones. If someone has created a new commit, you'll know!
- When you're sure, commit them! `git commit -m "<your message here>`.
  - If you feel like you've done a minor mistake, you can use `git commit --amend --no-edit`. This will update your last commit, but only use it _for minor edits_ like fixing typos.
- It's finally the time for your submission to air! Run `git push origin master`, fill in the username and password, and you're good to go.

GLHF!
