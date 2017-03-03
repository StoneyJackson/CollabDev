# Workflow Reference


## Prerequisites

- You have a GitHub account and you know your username and password. If you
  don't have one, create one now.
- You have Git 2+ installed and configured.
- You know how to open a terminal and generally work from the command-line.
- You know enough of vi or vim to edit, move around in, save, and quit files.


## Workflow Overview

The workflow description below covers the typical operations in the order
they are often performed to develop and contribute work to another project.
Most of the operations are issued from the command-line. These lines start with`$`.
Do not type `$`. This is the prompt that the command-line displays to you to
indicate that it is ready for you to type a command. Lines that start with `###`
are performed using GitHub through a browser. The numbers at the end of each
line are for quick reference and should not be typed either. When you see a term in all capital letters surrounded by angle
brackets, e.g., `<MY_URL>`, replace it with a value appropriate to the project
you are working on. A list of these placeholders and their meaning is below:

- `<MY_URL>` - The URL to your GitHub hosted repository. To find it, navigate to
  your repository on GitHub. Click on the green "New Pull Request"
  button. You get a pop-up that contains a URL in a text-box. Unless you have configured your GitHub account to authenticate with SSH, you'll want a URL that starts with https://. If the URL starts with git@github... click `Use HTTPS`.
- `<THEIR_URL>` - The URL for the project's repository that you would like to
  contribute to. Find it by navigating to their repository on GitHub and copy
  the URL in the box right of the `SSH` or `HTTPS` button. Use `HTTPS` since
  this is not your repository.
- `<DIR>` - This is any directory name you like. But use the same directory for
  each occurrence of `<DIR>`.
- `<BRANCH_NAME>` - This is a branch name of your choosing. Choose one that is
  related to the bug your are fixing or the feature you are implementing.
  Whatever you choose, use the same branch name throughout the example.

Also note, lines marked with `*` represent modifications being made to files in
the project. The exact modifications you might make, and the tools that you use
to make them, depend on what you are trying to do and your preferences. In
short, these lines should not be typed in literally, but must be interpreted in
terms of the task you are performing.


## Prepare to work on a project

When you first start working on a project, you'll need to fork their project
(1), clone your fork locally (2-3), and create a remote back to their project in
your local repository (4). Once you've done this setup for a project, you will
not need to do it again unless you delete the fork, your local clone, or the
remote.

```bash
### Use GitHub to fork their repository.                (1)
$ git clone <MY_URL> <DIR>                              (2)
$ cd <DIR>                                              (3)
$ git remote add upstream <THEIR_URL>                   (4)
```


## Starting your contribution

When you start working on a contribution, you should create a branch to hold
your work, do a little work, commit it, push it to your repository on GitHub, and create a pull-request from the branch in your repository to master in the project's repository on GitHub.

<aside>
**Pull-requests**
The purpose of the pull-request isn't to get the maintainer to accept your work
(yet). It starts a conversation with the maintainer. They can review what you
are trying to do and give you feedback early. That way, if you are on the wrong
track or the maintainer is not interested in your idea, you can find out before
you waste too much time implementing your idea.
</aside>

Also, remember, lines (6-8) are marked with `*`, so must be interpreted for the
task you are performing.

```bash
$ git branch <BRANCH_NAME>
$ git checkout <BRANCH_NAME>
### Do a little work
$ git add .
$ git commit -v
$ git push -u origin <BRANCH_NAME>
### Use GitHub to open a PR from <BRANCH_NAME> to master on upstream.
```


## Work

Keep working on your idea, committing and publishing your work as you go. The pull-request will automatically be updated with the new commits you
push to your repository on GitHub, allowing the maintainer to follow your
progress as you go.

```bash
### Do a little work
$ git add .
$ git commit -v
$ git push origin <BRANCH_NAME>
```


## Keep your repositories up-to-date

While you are working on your idea, the maintainer may have accepted work from
other contributors. As that happens, the project's master branch will contain
commits that yours do not. You'll need to fetch these commits into your local
master, rebase your work on top of those commits, and push your
branches to your repository on GitHub. When you rebase your work you
might find that your changes are incompatible with those you fetched from
upstream. You will need to resolve any conflicts that git identifies.
GitHub has a lovely tutorial on resolving conflicts [1].

It's a good idea to update your repositories regularly so that your work does
not become too stale.

Again, as you push your work to your repository on GitHub, the pull-request
is updated automatically.

```bash
$ git checkout master
$ git pull upstream master
$ git push origin master
$ git checkout <BRANCH_NAME>
$ git rebase master
### Resolve any conflicts and complete the rebase
$ git push -f origin master <BRANCH_NAME>
```

Do the above for each branch that needs to be updated with changes from master.


## Squash your commits

If you are following best practices, you will make many small commits as you
develop your idea. Sometimes earlier commits are invalidated/corrected by later
commits as you refine your solution. Your commit log becomes a diary of how you
developed your solution. This log is sometimes useful to you as you develop your
idea, but usually maintainers will ask you to squash your commits into just
a few (often one) logical commit that implements your feature, or fixes the bug.
That helps keep the log of the main project cleaner, and more clearly identifies
which commits are responsible for implementing which features or fixing which
bugs. Usually you squash when you near completion of your implementation, but a
maintainer may ask you to squash periodically as you go because it may make it
easier for them to review your changes.

In any case, you will periodically squash your commits and push the
squashed version to your repository on GitHub. Again, the pull-request will
be updated automatically.

To squash commits, we perform an interactive rebase. This will put us into
and editor (vim most likely) with a list of the commits that we are rebasing at
the top. To squash them into one commit, change the first word in every line
after the first from `pick` to `squash`. Save and quit. Git will combine all the
commits into the first and will again put you into an editor to create the final
commit message for the newly squashed commit. If you have been providing good
commit messages as you go along, writing a good final commit message should be
relatively easy.

GitHub has a nice article on interactive rebases [2].

```bash
$ git checkout <BRANCH_NAME>
$ git rebase -i master
$ git push -f origin <BRANCH_NAME>
```


## Maintainer accepts your pull-request

After all your hard work, hopefully the maintainer will eventually accept your
pull-request, which will merge your changes into their master branch.


## Update your master

After the maintainer has accepted your pull-request, your need to update your
master with the new changes in upstream, which are yours! Follow the same procedure as in "Keeping your repositories up-to-date", except that you
don't need to rebase. That's because your work is already included in master.


## Delete unneeded branches

Now that your work has been accepted in upstream, you can safely delete the
branches you were working on both in your local and remote repositories. If you ever abandon your effort before
a pull-request is accepted, you can also delete your branch; but you'll need
to use -D (capital D) with the `git branch` command.

```bash
$ git checkout master
$ git branch -d <BRANCH_NAME>
$ git push origin :<BRANCH_NAME>
```


## References

[1] GitHub. _Resolving a Merge Conflict from the Command Line_. Accessed April
2016.
<https://help.github.com/articles/resolving-a-merge-conflict-from-the-command-line/>.

[2] GitHub. _About Git Rebase_. Accessed April 2016. <https://help.github.com/articles/about-git-rebase/>.


## Copyright and Licensing

Copyright 2016 Darci Burdge and Stoney Jackson SOME RIGHTS RESERVED

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
International License. To view a copy of this license, visit
http://creativecommons.org/licenses/by-sa/4.0/ .
