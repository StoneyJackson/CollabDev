# Activity 10: Pull-Requests


## Form teams

Form as many 2-person teams as you can, and 3-person teams when you cannot.

Assign team members roles such that each team member participates in each
role across configurations.


### Roles

- Maintainer:
- Contributor:
- Recorder and spokesperson (in 2-person team, same as maintainer):


## Part 1 - Setup and Contribution

1. Maintainer:
    - [GitHub] Create a project, initialized with a license and/or a .gitignore file.
   Write the URL below.
        ```






        ```
2. Contributor:
    - [GitHub] Fork maintainer's project
    - [Local] Clone your fork
    - [Local] Make a change locally and commit it
    - [Local] Push your change to your fork
    - [GitHub] Issue a pull-request from your fork to maintainer's project (upstream).
        ```
        (notes and questions here)
















        ```
3. Maintainer:
    - [GitHub] Review changes in pull-request.
    - [GitHub] Accept and merge the pull-request.
        ```
        (notes and questions here)
















        ```
4. Contributor:
    - [Local] Follow directions for "[Configuring a remote for a fork](https://help.github.com/articles/configuring-a-remote-for-a-fork/)"
      to create a remote named `upstream` that refers to the maintainer's repository. This only has to be done once on your local repository.
      Of course if you delete the local repository, you would have to do it again.
    - [Local] Follow directions for "[Syncing a Fork](https://help.github.com/articles/syncing-a-fork/)", including the ***Tip***, to update your local and fork
      repositories with upstream.
        ```
        (notes and questions here)
















        ```
    - Why was it necessary to synchronize your local and fork with upstream? I.e., what was different about your repositories from that of upstream's?
        ```






        ```

### Questions

1. List any new commands or concepts along with a brief definition below.
    ```










    ```

***STOP. Wait for instructor before continuing.***


## Part 2 - Do it again

Swap roles and repeat Part 1 again.

### Roles:

- Maintainer:
- Contributor(s):

3-person teams: The contributor in part 1 becomes the maintainer in this part. Create and manage two different projects, one per contributor.


## Part 3 - Work in progress

In GitHub, a Pull-Request is a bit of a misnomer. It is more than a request for the maintainer to pull your changes
into their repository. It is also a way of making your intentions visible early. Developers sometimes create a
pull-request as soon as they start working on something, way before the idea or the code is complete. This let's
others know what they are working on, and allows them to provide feedback as the developer works. This makes it
more likely that what they do is what the community and maintainer wants. Otherwise, a developer may waist
a lot of time on something that will never be merged into upstream.

A pull-request is also a tool for code reviews. Folks can review and comment on your commits. Updating a pull-request
is as simple as making additional commits on the same branch and pushing it to your fork. Let's try it...

### Project and Roles

Choose one of the projects to work on that you created in the previous two parts. Return to the corresponding roles.
Note the pertinate information below:

- Project URL:
- Maintainer:
- Contributor:
- Recorder and spokesperson:

### Instructions

1. Contributor:
    - Make a change to you local repository
    - Push it to your fork
    - Create a pull-request back to the maintainer's repo
2. Maintainer:
    - Review the changes in the pull-request, making at least one comment
    - Feel free to make other suggestions in the pull-request
3. Contributor:
    - Read the feedback in the pull-request
    - Make changes in your local repository to address the maintainer's comments
    - Push your changes to your fork (note: the pull-request is autimatically updated!)
4. Maintainer and contributor:
    - Repeat steps 2 and 3 until you are satisfied
5. Maintainer:
    - Either accept and merge the pull-request, or reject it by closing it.
    - If you rejected it, you can always go back and re-open it and accept it later.

```
(notes and questions here)
























```

### Questions

1. List any new commands or concepts along with a brief definition below.
    ```










    ```

## Part 4 - Do it again

Swap roles as you did in part 2 and repeat part 3 in the new roles.

```
(notes and questions here)
























```
