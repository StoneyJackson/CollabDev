# Activity 8: GitHub

## Part 1

### Objectives

- Create a GitHub account
- Create a new project on GitHub
- Clone a repository you own from GitHub
- Explain the difference between a project URL and a repository URL
- Push changes from a local repository to a remote repository
- Explain the meaning of a remote
- Explain the significance of the remote named origin
- Delete a repository you own on GitHub

### Instructions

1. **Watch this 4 minute video on GitHub.**
    - http://boingboing.net/2017/01/03/video-explains-what-github-is.html
    - Note any questions or items of interest here.
        ```






        ```
2. **Create an account on GitHub.**
    - Note that this account is public. Any code you publish using this account
      will be public. In this class, you may be asked to publish example
      repositories that may identify that you belong to a particular school or
      are in a particular class (although the instructor will do his or her
      best to avoid this). To avoid leaking such information, you may choose to
      use a publicly anonymized account.
    - Have each team member create a GitHub account.
3. **Email your instructor your account name on GitHub.**
    - Your instructor may asked you to "hand in" work by creating a particular
      project on GitHub. Your instructor needs to know what account belongs to
      you on GitHub.
    - Have each team member email the instructor the GitHub account they will be
    using for this class along with their full name.
4. **Create a new project on GitHub.**
    - Call it anything you like.
    - Direct GitHub to create a default README file.
5. **Clone your repository locally.**
    - `git clone URL` is the command to clone a repository to your local filesystem.
    - Try cloning your repository using the URL in the browser's location bar. Write the URL you used here. Does this work?
        ```






        ```
    - Try cloning your repository using the URL found in the "Clone or download" button, using HTTPS.
    Write the URL you used here. Does this work?
        ```






        ```
    - What do you think is the difference between the URL in the browser's
    location bar and the URL in "Clone or download"? What do they refer to?
        ```






        ```
6. **Make a change to your local repository.**
    - Edit the README file, adding a one sentence description of your project.
    Save, stage, and commit your change. Use `git log` to confirm that your have
    committed your change.
    - View your project on GitHub. If it is still open in your browser, refresh/reload
    the page. Has your project changed on GitHub?
        ```




        ```
7. **Publish your changes to GitHub.**
    - Use `git push` to publish your changes to GitHub. You will prompted for
    your username and password on GitHub.
    - View your project on GitHub. If it is still open in your browser, refresh/reload
    the page. Has your project changed on GitHub?
        ```




        ```
8. **Run `git remote -v`.**
    - Past the commands output here.
    - What do you recognize in the output of the command?
        ```




        ```
    - What do you think "origin" means?
        ```




        ```
    - How does git know where to send its changes when you run `git push`?
        ```




        ```
8. **Draw two diagrams.**
    - Draw a diagram of the commit histories in your local and remote repositories
    *before* you ran `git push`.
        ```










        ```
    - Draw a diagram of your commit histories in your local and remote repositories
    *after* you ran `git push`.
        ```










        ```
10. **Delete your local repository and working directory and clone it again.**
    - Do you have all the changes you had before?
        ```





        ```
    - Suppose you have uncommitted changes in your local repository and you deleted
    your local copy and cloned your remote. Would you lose anything? If so what?
        ```





        ```
    - Suppose you have committed new changes in your local repository that you have
    not yet pushed to GitHub. Would you lose anything? If so what?
        ```





        ```
11. **Create a publish policy for your team.**
    - When should team members to push their code to a public/shared location and
    why?
        ```









        ```
12. **Delete your repository on GitHub.**
    - How did you do it?
        ```






        ```

## Part 2

### Objectives

- Create a new project on GitHub from existing local repository
- Explain the effect and purpose of `git remote add`
- Setup local system and GitHub for authenticating via SSH


### Instructions

1. Project.zip contains a git repository. Unzip it.

2. **Inspect `Project`.**
    - Take a look at the local `Project` repository. Use `git log`, `git status`, `git branch`, and `git remote -v` to learn what you can about the repository.
    - Is there a remote defined?
        ```



        ```
2. **Create a new repository on GitHub based on a local repository.**
    - Name it anything you like. ***Do not*** allow GitHub to create a default
      README or license file.
    - Follow GitHub's directions to "... push an existing repository from the
      command line" to load content from and connect the local repository in
      `Project`.
    - Explain what you think the following command is doing: `git remote add origin URL`
        ```






        ```
    - Explain what you think the following command is doing: `git push -u origin master`
        ```






        ```
    - Look up what `-u`, `origin`, and `master` means for the `git push` command
    issued above. Adjust your answer to the previous question as necessary.
3. **Test that you can make changes to your new repository.**
4. **If time allows, have each team member complete the above steps individually.**
