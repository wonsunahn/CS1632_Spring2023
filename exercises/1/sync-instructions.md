These instructions assume that you have an existing private repository as we set up in class, and that you have it cloned locally. If you don't, [set up a new repo](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/overview/creating-your-first-repository-using-github-desktop), clone the canonical repository ([wonsunahn/CS1632_Spring2023](github.com/wonsunahn/CS1632_Spring2023)) into a separate directory and copy all of the contents of the repository _**except for the hidden `.git` directory**_ into your new repository.

To manually set up a syncing channel for your "fork", do the following: 

Open a terminal in the directory of your repository and run this:

```shell
git remote add upstream https://github.com/wonsunahn/CS1632_Spring2023.git
git fetch upstream main
```

This [adds](https://git-scm.com/docs/git-remote) a new [remote channel](https://github.com/git-guides/git-remote) to your local git repository, which means you can synchronize with changes from the original repository, called "upstream changes." (Note: you can name the remote anything you want by replacing `upstream` with another name, but it is standard to name it upstream if it refers to the original copy of a fork.)

To "pull", or incorporate, changes from the original repository into your fork, you can use
```shell
git pull upstream main
```
This will work as long as you have not made (and committed) any changes since the last time the original repository was updated. If you have, you might get a message similar to this when you try to pull:

```shell
$ git pull upstream main
From https://github.com/wonsunahn/CS1632_Spring2023
 * branch            main       -> FETCH_HEAD
fatal: Not possible to fast-forward, aborting.
```

In that case, you'll have to merge the changes together manually. You can do that by either merging or rebasing. To merge, run

```shell
git fetch upstream main
git merge upstream/main
```

(Note the `/` symbol in the second command.)

This should cover basic use cases, but sometimes merges can be very complex, and even a `git merge` command will not resolve the problem. In these cases, there is a **merge conflict.** Merge conflict resolution is beyond the scope of these instructions, so ask for help if `git merge` reports an error. 
