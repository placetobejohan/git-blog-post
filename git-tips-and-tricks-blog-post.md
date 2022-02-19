# Git tips & tricks
`By Johan Maes`

I'm Johan, software developer at Lemonade. In this blog post I'd like to talk about an awesome versioning tool we all use as developers: Git. While I'm not an expert by any means, I do like to think I've picked up a few things over the years as an enthousiastic user.

I'll start with exploring a few basic concepts and the most common Git commands before moving onto a few more advanced Git features, some of which I only recently discovered myself. I wouldn't dare to call this a deep dive but it will help you to understand what's going on behind the scenes, which could prove useful, especially if something went wrong. Let's err...snorkel in!

## Basic concepts

### Local repository
Git is a distributed version control system, which means that all code, including its full history, can be found in your local repository. 

To make a change, you start editing your code. The changes will first be made in your `working tree` (also called working directory). Then you add them (or some of them) to the `staging area` with `git add`. Finally, with `git commit`, the changes in the staging area are officially added to your repository.

>  working tree &rarr; `git add` &rarr; staging area &rarr; `git commit` &rarr; repository

### The staging area
So what's the point of the staging area? Mainly it provides an extra buffer between working tree and repository. It gives you the chance to reconsider and to answer the question `Are you sure?` for each change you've made. If the answer is yes, you can commit the change. If the answer is no, you can simply unstage with `git reset`.

However, the staging area also allows you to make several changes and then decide which of your changes you add to the staging area to commit. In this way you can split up your work into meaningful commits. After all, the Git history is commit-based - every commit is a snaphot of the entire repository - and there a number of advantages to keeping a clean history with meaningful commits. For example, if a bug was introduced, it's easier to pinpoint the guilty commit, or reviewing a big pull request can be simplified by reviewing the commits instead.

For completeness, let me add that the staging area can be skipped with the `--all` flag if you only need to modify or delete existing files: `git commit -a`.

### Branches and HEAD
Git supports the idea of branching. This allows one or more developers to work on several features or bugfixes at the same time. Whenever you make code changes you need to make them on a branch. When you create a new repository with `git init` you will initially have only one branch `master` or `main`. 

A branch is defined by its commit history. Let's say we start out on master and have made 2 commits A en B.



how does git know which code to show (local repo)

### Remote repository
As soon as you want to share your code with other developers, you need a central repository which is then the official version of the codebase. It's where a new developer gets his local copy from with `git clone`. Every developer .



## Common commands
Yikes! That was one lengthy introduction, perhaps we should come up for a bit of air - I hope you're not in a `detached HEAD` state yet. Either way I think it shows that even with the basics of Git there's already a lot going on behind the scenes, and that it's worth it to take a closer look at what's really going on and how we can make the most of how Git works. Now let's move on to some of the basic Git commands you're all familiar with.

### git commit

### git fetch

### git merge

### git pull

## Advanced features

### Cleaning up branches

### git worktree

### Git hooks

## There's a lot more to (G)it

Tools: Posh Git, VSCode extensions

## References

https://rogerdudler.github.io/git-guide/