# Git: The Board Game

The goal is to create a board game for teaching git.

## Requirements

- Must accurately model git
- Must use readily available materials
- Must be usable by students in a classroom

## Equipment

- Hex paper
  - Scale 1/2 inch spacing, letter sized (12 longways)
    - [Downloadable version](https://www.printablepaper.net/preview/hexagon-portrait-letter-2)
- Sticky notes
  - Scale: the small skinny ones (TODO: link)
  - Writable (i.e., not the glossy ones)
- Tokens (almost anything will do; pennies, checkers, pebbles, etc.)

## `git init`
The command `git init` is used to set up a local repository.

In this section we will set up the game board that represents the local git repository. The game board consists of two sheets of paper - one representing the Repository, and the other representing the Staging Area and the Working Directory.

<table>
<tr><td>Repository<br>(hex paper)<br><br></td></tr>
<tr><td>Staging Area<br>
(blank paper)<br>
Working Directory</td></tr>
</table>

### The Repository
The Repository is represented by a sheet of hex paper (in landscape orientation) at the top of the game board. Label this sheet of paper "Repository".

### The Staging Area and The Working Directory
The Staging Area and the Working Directory is represented as a single sheet of blank paper (in landscape orientation).

1. Draw a line across the middle of the sheet of paper from left to right.
2. Label the top half of this sheet of paper "Staging Area".
3. Label bottom half of this sheet of paper "Working Directory".

## `git add`

Use to add changes in working copy to stage.

Move any number of change tokens from the working directory to the staging area.

## `git commit`

Use to commit staged changes to the local repository.

1. Remove all of the change tokens in the staging area
2. If this is the first commit
  1. Write a 1 in a hex cell midway down on the left side of your paper.
      This is your first commit.
  2. Write *master* on a sticky note and attach it to the new commit node.
      This is the master branch.
  3. Write *HEAD* on a sticky note and attach it to the master branch. *HEAD*
      now refers to *master*, which refers to commit 1, and therefore refers to
      commit 1 indirectly through *master*.
3. If this is not the first commit
  1. Write the next unused integer in any unused hex cell adjacent to the
      commit *HEAD* refers to (prefer unused cells in the same direction
      established by the previous two commits, or to the right). This is the
      new commit.
  2. Draw an arrow from the new commit to the commit *HEAD* refers to.
  3. Move the branch *HEAD* refers to to the new commit along with *HEAD*.
      If *HEAD* does not refer to a branch, move *HEAD* to the new commit.

## `git branch NAME`

Use to create a new branch named NAME.

1. If a branch named NAME exists, stop.
2. Write NAME on a sticky note and attach it to the commit that *HEAD* refers to.

## `git checkout BRANCH|COMMIT`

Use to update working directory with files from BRANCH or COMMIT and update *HEAD*
to refer to the BRANCH or COMMIT.

1. If restoring files from the commit BRANCH refers to or by COMMIT would overwrite
    any local changes (in staging area or working directory), stop.
    ***TODO: How do we model this?***
2. Replace files in working directory with those from BRANCH or COMMIT.
    ***TODO: How do we model this?***
3. Detach *HEAD* from whatever it's attached to.
4. Attach *HEAD* to BRANCH or COMMIT.

## `git merge BRANCH`

Use to merge BRANCH into commit referred to by *HEAD*.

1. Merge all files from BRANCH and *HEAD* in the working directory.
    ***TODO: How do we model this?***
2. If any mergers syntactically conflict, mark the conflict in the working directory
   and stop.
    ***TODO: How do we model this?***
3. Write the next unused integer in an unused cell adjacent to *HEAD*. This is
    the merge commit.
4. Draw an arrow from the merge commit and *HEAD*.
5. Draw an arrow from the merge commit and BRANCH.
6. Move the branch referred to by *HEAD* to the merge commit along with *HEAD*.
    If *HEAD* does not refer to a branch, just move *HEAD*.
