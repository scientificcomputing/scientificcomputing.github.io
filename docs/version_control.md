# Version control

Using version-control might sound overwhelming the first time you hear about it.
What is [git](https://git-scm.com/)? How does it differ from [Dropbox](https://www.dropbox.com/) and [Google Drive](drive.google.com/)? Why do even bother learning yet another tool?

Long story short, you can use git to track changes of your code, either locally on your computer, or synced through a web-service, such as [Github](https://github.com/).

An extensive tutorial of the most important features of `git` can be found [here](https://git-scm.com/docs/gittutorial).

In this section we will cover a few basic commands.

## Creating a new project from an existing folder and syncing with Github
To push the repository to Github see one of the following tutorial:
- [Using the GitHub CLI](https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github#adding-a-local-repository-to-github-with-github-cli)
- [Using git](https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github#adding-a-local-repository-to-github-using-git)

## Making changes to files
If you have modified some files, say `file1.py`, `file2.txt` you can make the changes ready for committing (making a checkpoint of the files) by calling

```bash
git add file1.py file2.txt
```

Next, you call `git commit`

```bash
git commit -m "Replace this text with information about the changes"
```

The files are now added to the local version control on your computer.
Every commit has a hash and you can find these hashes by calling 
```bash
git log
```

## Syncing changes with the online repository
To sync your changes with the web service (for instance Github), you need to call `git push`.

If you have made changes to the repository on another computer, that has pushed these to Github, you can get the changes by calling `git pull`.

## Starting from scratch 
If you want to start a new project, and you have no files to commit yet, you can follow the guide from Github on how to crate your first repository:
[Github Hello World](https://docs.github.com/en/get-started/quickstart/hello-world).