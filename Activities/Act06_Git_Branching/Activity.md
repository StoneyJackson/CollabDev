# Activity 6: Branching

## Objective

Upon completion of this activity you will be able to:

- Use `git branch` to create a new branch.
- Use `git checkout` to checkout a working copy of a given branch.
- Use `git checkout` to detach HEAD.
- Use `git merge` to merge one branch into another.
- Use `git rebase` to rebase one branch onto another.
- Explain the difference between rebase and merge.
- Explain why one might prefer rebase over merge.
- Explain the relationship between HEAD and `git commit`.
- Use commit hash values to refer to commits in git commands.
- Use relative references to refer to commits in git commands.
- Use `git reset` to undo a commit on a branch.
- Use `git revert` to create a new commit that undoes a commit on a branch.
- Explain the difference between `git reset` and `git revert`.
- Identify when one should prefer `git reset` over `git revert` and vice-versa.

## Instructions

Navigate to http://learngitbranching.js.org/ and complete:

- All 4 levels of *Introduction Sequence*
- All 4 levels of *Ramping Up*

## Questions

1. Give a command that adds a commit node to the current commit or branch.

```



```

2. Give a command that creates a new branch named "crazy".

```




```

3. Give a command that changes the working copy to the last commit on the
   branch named "crazy".

```





```

4. Alice is currently on the `master` branch. She has an idea for a new feature,
   but isn't sure if it will work. Not wanting to mess up the `master` branch
   until she is sure her idea will work, she wants to work on a separate branch
   named `newIdea`. She creates the `newIdea` shown below and begins to work.
   Besides a bad commit message, what's wrong with what Alice has done?
   What should have Alice done?

```
$ git branch newIdea
DOES SOME WORK
$ git add . ; git commit -m "A little work on my new idea"









```

5. Draw a diagram of Alice's repository.

```





```

6. Give a sequence of commands that will fix Alice's repository and put her
   working copy in a state ready to continue her work. Don't lose any of her
   work.

```





```

7. Alice is now finished with her work on `newIdea`. Give a command sequence to
   merge her work into `master` and return her working copy to the `master`
   branch.

```





```

8. Draw a diagram of Alices repository after merging `newIdea` into `master`.


```





```

9. In a parallel universe, Alice has just finished her work on `newIdea`, and
   is ready to merge her work into `master`. However, she wants her commit
   history to be a nice clean straight line (no nodes with multiple parents).
   Give a command sequence that accomplishes her goals and returns her working
   copy to `master`. She is currently on `newIdea`.

```





```

10. Bob isn't happy with his last commit. Give a command to undo this commit
    as if it never existed.

```





```

11. In a parallel universe, Bob isn't happy with his last commit. But he
    already published his current commit. Bob has heard that it is a really bad
    idea to rewrite history after it has published (something about ripping a
    wormhole in time-space... or maybe it creates a bridge into a parallel
    universe). Write a command sequence to "undo" his last commit that he can
    safely publish.

```





```
