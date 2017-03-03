# Activity 3: .gitignore

## Roles

- Manager & Driver:
- Recorder:
- Reflector & Spokesperson:

## Model: Project A

```
$ ls -a
.       ..      .git    A.class A.java
$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	A.class
	A.java

nothing added to commit but untracked files present (use "git add" to track)

```

## Model: Project B

```
$ ls -a
.          ..         .git       .gitignore A.class    A.java
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	A.java

nothing added to commit but untracked files present (use "git add" to track)
$ cat .gitignore
*.class

```

## Questions: 15 minutes

1. How many files are in Project A?

```




```

2. How many files are in Project B?

```




```

3. What file does Project B have that Project A does not?

```




```

4. What is the contents of that file?

```




```

5. In Project A, how many files are "untracked" by git?

```




```

6. In Project B, how many files are "untracked" by git?

```




```

7. In Project B, which file is being ignored by git?

```




```

8. Why do you think git in Project B is ignoring those files?

```




```

9. What do you need to do to make git ignore that same file in Project B?

```




```

10. Perform that operation and observe the results. Do they confirm or reject your hypothesis?

```




```

11. Suppose you want git to ignore JAR files (files that end in .jar) as well as class files.
    How do you think you would do that?

```




```

12. Confirm your hypothesis.

```




```

13. What kinds files do you think should and should not be stored in the repository?

```




```
