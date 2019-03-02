# Workflow Reference

## Prerequisites

- You know how to inspect and understand the state of your repository.
- You know how to stage and commit changes.
- You know how to resolve conflicts.
- You have a GitHub account.


## Workflow

This is a more detailed version of GitHub's fork-pull-request workflow: a.k.a. GitHub-Flow. It's different in that it prescribes how to use the issue tracker and how contributors should manage their forks and local repositories.

1. There is a centralized repository on GitHub, we'll call `upstream` that holds the official copy of the project in a stable branch named `master`. For consistency, we recommend creating an organization in GitHub, and then create the `upstream` repository for the project within the organization. This will allow the creator to act as a contributor in the same way that other contributors do (as described below). Maintainers are added to the project by granting people write permissions to the repository. GitHub may be configured to protect the `master` branch so that it can be changed only through reviewed pull-requests. This is a good idea.
2. Contributors claim issues in `upstream`'s issue tracker before starting work on an issue. If no issue exists for what they want to work on, they first create an issue, claim it, and then begin work.
3. Contributors work in separate forks of `upstream` and contribute changes back to `upstream` through pull-requests.
4. Contributors clone their forks locally. When they clone their fork, their fork on GitHub becomes the remote `origin` in their local repository. They also create a remote named `upstream` that refers back to the `upstream` repository on GitHub.

    ```
    $ git clone <URL_TO_FORK>
    $ cd <DIRECTORY_CREATED_BY_PREVIOUS_COMMAND>
    $ git remote add upstream <URL_TO_UPSTREAM>
    ```

5. Contributors never work on `master`. Changes to `master` are only made through pull-requests to `upstream` and are received in a contributor's local repository by pulling thing from `upstream`.
6. Contributors create feature branches from master to work on features. One feature branch per feature. All feature branches are created off of master; never from another feature branch.

    ```
    $ git checkout master
    $ git branch <FEATURE_BRANCH>
    $ git checkout <FEATURE_BRANCH>
    (do work, stage and commit as you go)
    ```

7. Contributors publish their feature branches to their forks, and issue pull-requests from the feature branch in their fork back to `master` in `upstream`. The first time you publish your feature branch, use the `-u` option as follows.

    ```
    $ git push -u origin <FEATURE_BRANCH>
    ```

    This creates a branch in `origin` with the same name as the local feature branch and creates a connection between the two. Subsequent changes are published to this branch without the `-u` option.

    ```
    $ git push origin <FEATURE_BRANCH>
    ```

8. Contributors update their repository with changes from `upstream` by pulling changes from `upstream`'s `master` into their local repository's `master`, rebasing all their feature branches onto `master`, and then pushing all their branches to `origin`. Note: conflicts may occur when rebasing feature branches onto master. Handling of conflicts is not show below.

    ```
    $ git fetch upstream
    $ git checkout master
    $ git merge upstream/master
    $ git push origin master
    $ git checkout <FEATURE_BRANCH_1>
    $ git rebase master
    $ git push -f origin <FEATURE_BRANCH_1>
    $ git checkout <FEATURE_BRANCH_2>
    $ git rebase master
    $ git push -f origin <FEATURE_BRANCH_2>
    (...)
    ```

9. Contributors delete unneeded branches. Once a pull-request has been accepted and merged, or rejected or abandoned and closed, the feature branch on which the pull-request was based is no longer needed.

    ```
    $ git checkout master
    $ git branch -D <UNNEEDED_BRANCH>
    $ git push --delete <UNNEEDED_BRANCH>
    ```

10. Maintainers are anyone with write access to upstream. They review pull-requests. After reviewing they can either merge the pull-request into `master`, request revisions from the contributor, or reject the pull-request by closing the pull-request. Maintainers should ensure that pull-requests are of quality, address a single logical issue, pass all tests, and have good commit messages. If accepted, maintainers often ask contributors to squash their commits into a single commit before merging. However, GitHub now allows the maintainer to squash and merge the pull-request at the same time. This is usually preferred. Once merged, maintainers must also close all issues in the tracker that the pull-request resolved.

## Copyright and Licensing

Copyright 2016 Darci Burdge and Stoney Jackson SOME RIGHTS RESERVED

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
International License. To view a copy of this license, visit
http://creativecommons.org/licenses/by-sa/4.0/ .
