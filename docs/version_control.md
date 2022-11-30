# Version control

Using version-control might sound overwhelming the first time you hear about it.
What is [git](https://git-scm.com/)? How does it differ from [Dropbox](https://www.dropbox.com/) and [Google Drive](https://drive.google.com/)? Why do even bother learning yet another tool?

Long story short, you can use git to track changes of your code, either locally on your computer, or synced through a web-service, such as [Github](https://github.com/).

An extensive tutorial of the most important features of `git` can be found [here](https://git-scm.com/docs/gittutorial).

## Creating a new project from an existing folder and syncing with Github
To push the repository to Github see one of the following tutorial:
- [Using the GitHub CLI](https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github#adding-a-local-repository-to-github-with-github-cli)
- [Using git](https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github#adding-a-local-repository-to-github-using-git)

## Starting from scratch 
If you want to start a new project, and you have no files to commit yet, you can follow the guide from Github on how to crate your first repository:
[Github Hello World](https://docs.github.com/en/get-started/quickstart/hello-world).

## Sharing single files with others
If you have stand-alone scripts that you want to share with others, we recommend using [Github Gist](https://gist.github.com/), a service linked to your Github account. Here you can share single-file scripts (you can choose to make the file secret or public), make comments and look at file revisions.

## Working with others
If you are on a project with others, you should preferably work on [branches](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell).
and use [pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) to merge your work with the main code.

(versioning-main)=
## Tagging specific versions of your repository
Some commits in your repository are more important than others.
For example, the version of your repository when you submit the paper after you addressed the first review of your paper, and the final version that contains the code for the journal publication. Being able to easily go back to these versions is a good idea. You can achieve this by creating a tag, see [Git Basics -Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging) for an extensive explanation.


## Changelog
It is also good practice to keep track of the changes you make between two version. You can do this by writing a [changelog](https://en.wikipedia.org/wiki/Changelog).

You can either write this by hand, or automatically generate then using Github, as described at [Github-Automated release notes](https://docs.github.com/en/repositories/releasing-projects-on-github/automatically-generated-release-notes).

If you want to write them by hand, it is recommended to call the file `CHANGELOG.md`, and it could like
```markdown
# Changelog

---

## Final version
- tag: `v_final`

### Changes
- Added figure 3.1
- Rewritten section about ..

---

## Second submission
- tag: `v_second_submission`

### Changes
- Run new experiments
    - Added descriptions in section 2.4
    - Added results in Section 3.4
- Change Table 2.1

---

## First submission
- tag: `v_first_submission`


---

```
Note that if you write descriptive commit messages you can use these messages in your changelog. For example to get all commit messages between the `v_first_submission` and `v_second_submission` tags you can e.g

```bash
git log --pretty=oneline v_first_submission...v_second_submission
```
If you need to get all commit messages from the very beginning to e.g `v_first_submission` you can do
```bash
git log --pretty=oneline $(git rev-list --max-parents=0 HEAD)...v_first_submission
```
