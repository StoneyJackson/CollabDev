*Version 2019-Spring-1.0, Revised 13 February 2019*

Activity 4:

Undoing Your Changes With Git

Sometimes you make changes to your files that you don’t want to keep.
How you undo them when working with Git varies by what state your file
is in.

## Content Learning Objectives

*After completing this activity, students should be able to:*

  - > Undo changes to files in the working state.

  - > Undo changes to files in the staged state.

  - > Undo changes to files in the committed state.

##  Process Skill Goals

*During the activity, students should make progress toward:*

  - > Carefully reading Git command messages for understanding.
    > (Information Processing)

## Team Roles

*Decide what role each of you will play for today. Choose a role that
you have not played before, or recently. The goal should be to have all
team members rotate through the roles on a regular basis to become
comfortable with all the roles. If you have only three people, one
should have two roles. If you have five people, two may share the same
role. Record role assignments here.*

| Manager   |  |
| --------- |  |
| Presenter |  |
| Recorder  |  |
| Reflector |  |

# Model 1: Undoing a change you made to a file.

<table>
<tbody>
<tr class="odd">
<td><p><strong>1</strong></p>
<p><strong>2</strong></p>
<p><strong>3</strong></p>
<p><strong>4</strong></p>
<p><strong>5</strong></p>
<p><strong>6</strong></p>
<p><strong>7</strong></p>
<p><strong>8</strong></p>
<p><strong>9</strong></p>
<p><strong>10</strong></p></td>
<td><p>$ <strong>ls</strong></p>
<p>A.java</p>
<p>$ <strong>git log</strong></p>
<p>commit db967767f9ab675dba21e08c5d20627b34cbe133 (HEAD -&gt; master, origin/master, origin/HEAD)</p>
<p>Author: Karl R. Wurst &lt;karl@w-sts.com&gt;</p>
<p>Date: Fri Jan 18 14:25:44 2019 -0500</p>
<p>Add Feature X.</p>
<p>$ <strong>git status</strong></p>
<p>On branch master</p>
<p>Nothing to commit, working tree clean</p>
<p>$ <strong>cat A.java</strong></p>
<p>This is change #1.</p>
<p>$ <strong>edit A.java</strong></p>
<p>$ <strong>git status</strong></p>
<p>On branch master</p>
<p>Changes not staged for commit:</p>
<p>(use "git add &lt;file&gt;..." to update what will be committed)</p>
<p>(use "git checkout --&lt;file&gt;..." to discard changes in working directory)</p>
<p>modified: A.java</p>
<p>no changes added to commit (use "git add" and/or "git commit -a")</p>
<p>$ <strong>cat A.java</strong></p>
<p>This is modification #1.</p>
<p>This is modification #2.</p>
<p>$ <strong>git checkout -- A.java</strong></p>
<p>$ <strong>git status</strong></p>
<p>On branch master</p>
<p>Nothing to commit, working tree clean</p>
<p>$ <strong>cat A.java</strong></p>
<p>This is change #1.</p></td>
</tr>
</tbody>
</table>

## Questions (10 min)

1.  > For command \#1 through command \#4, which of the three states
    > (Working, Staging, Committed) is A.java in?

2.  > What are the contents of A.java before command \#5?

3.  > For command 6 through command \#7, which of the three states is
    > A.java in?

4.  > What are the contents of A.java between command \#5 and command
    > \#8?

5.  > What was the effect of the editing in command \#5?

6.  > After listing the contents of A.java in command \#7, you decide
    > that you didn’t want to make those changes. What is the effect ot
    > command \#8? Be sure your explanation refers to at least one of
    > the three states.

7.  > If you couldn’t remember command \#8, how could you figure out
    > what command to give (without resorting to checking the Internet)?

8.  > Describe a situation where you would find command \#8 useful - and
    > probably not possible to accomplish in any other way?

# Model 2: Remove changes from a commit to be made.

<table>
<tbody>
<tr class="odd">
<td><p><strong>1</strong></p>
<p><strong>2</strong></p>
<p><strong>3</strong></p>
<p><strong>4</strong></p>
<p><strong>5</strong></p>
<p><strong>6</strong></p>
<p><strong>7</strong></p>
<p><strong>8</strong></p>
<p><strong>9</strong></p>
<p><strong>10</strong></p>
<p><strong>11</strong></p>
<p><strong>12</strong></p></td>
<td><p>$ <strong>git log</strong></p>
<p>commit 63b66cf74632ab3f2ebabb333e71d13938d7f2d4</p>
<p>Author: Karl R. Wurst &lt;karl@w-sts.com&gt;</p>
<p>Date: Fri Jan 18 16:02:12 2019 -0500</p>
<p>Add Feature Y</p>
<p>commit db967767f9ab675dba21e08c5d20627b34cbe133 (HEAD -&gt; master, origin/master, origin/HEAD)</p>
<p>Author: Karl R. Wurst &lt;karl@w-sts.com&gt;</p>
<p>Date: Fri Jan 18 14:25:44 2019 -0500</p>
<p>Add Feature X.</p>
<p><strong>$ git status</strong></p>
<p>On branch master</p>
<p>Nothing to commit, working tree clean</p>
<p>$ <strong>cat A.java</strong></p>
<p>This is change #1</p>
<p>$ <strong>edit A.java</strong></p>
<p>$ <strong>cat A.java</strong></p>
<p>This is modification #1.</p>
<p>This is modification #2.</p>
<p>$ <strong>edit B.java</strong></p>
<p>$ <strong>git status</strong></p>
<p>On branch master</p>
<p>Changes not staged for commit:</p>
<p>(use "git add &lt;file&gt;..." to update what will be committed)</p>
<p>(use "git checkout --&lt;file&gt;..." to discard changes in working directory)</p>
<p>modified: A.java</p>
<p>modified: B.java</p>
<p>no changes added to commit (use "git add" and/or "git commit -a")</p>
<p>$ <strong>git add .</strong></p>
<p>$ <strong>git status</strong></p>
<p>git status</p>
<p>On branch master</p>
<p>Changes to be committed:</p>
<p>(use "git reset HEAD &lt;file&gt;..." to unstage)</p>
<p>modified: A.java</p>
<p>modified: B.java</p>
<p>$ <strong>git reset HEAD A.java</strong></p>
<p>Unstaged changes after reset:</p>
<p>M A.java</p>
<p>$ <strong>git status</strong></p>
<p>On branch master</p>
<p>Changes to be committed:</p>
<p>(use "git reset HEAD &lt;file&gt;..." to unstage)</p>
<p>modified: B.java</p>
<p>Changes not staged for commit:</p>
<p>(use "git add &lt;file&gt;..." to update what will be committed)</p>
<p>(use "git checkout -- &lt;file&gt;..." to discard changes in working directory)</p>
<p>modified: A.java</p>
<p>$ <strong>cat A.java</strong></p>
<p>This is change #1</p></td>
</tr>
</tbody>
</table>

## Questions (12 min)

1.  > What is the effect of command \#8?

2.  > After issuing command \#9, you decide that you do not want to
    > commit your changes to A.java. What is the effect of command \#10?
    > Be sure your explanation refers to at least two of the three
    > states.

3.  > What does HEAD refer to in command \#10? How did you figure that
    > out?

4.  > Explain why command \#8 is a dangerous command. Or, at least, why
    > you should always follow command \#8 with command \#9.

5.  > If you couldn’t remember command \#10, how could you figure out
    > what command to give (without resorting to checking the Internet)?

6.  > Describe a situation where you would find command \#10 useful?

# Model 3: Removing changes that have already been committed.

<table>
<tbody>
<tr class="odd">
<td><p><strong>1</strong></p>
<p><strong>2</strong></p>
<p><strong>3</strong></p>
<p><strong>4</strong></p>
<p><strong>5</strong></p>
<p><strong>6</strong></p>
<p><strong>7</strong></p>
<p><strong>8</strong></p>
<p><strong>9</strong></p>
<p><strong>10</strong></p>
<p><strong>11</strong></p>
<p><strong>12</strong></p></td>
<td><p>$ <strong>ls</strong></p>
<p>A.java</p>
<p>$ <strong>git log</strong></p>
<p>commit db967767f9ab675dba21e08c5d20627b34cbe133 (HEAD -&gt; master, origin/master, origin/HEAD)</p>
<p>Author: Karl R. Wurst &lt;karl@w-sts.com&gt;</p>
<p>Date: Fri Jan 18 14:25:44 2019 -0500</p>
<p>Add Feature X.</p>
<p>$ <strong>git status</strong></p>
<p>On branch master</p>
<p>Nothing to commit, working tree clean</p>
<p>$ <strong>cat A.java</strong></p>
<p>This is change #1.</p>
<p>$ <strong>edit A.java</strong></p>
<p>$ <strong>cat A.java</strong></p>
<p>This is modification #1.</p>
<p>This is modification #2.</p>
<p>$ <strong>git add A.java</strong></p>
<p>$ <strong>git commit -m”Add Feature Y.”</strong></p>
<p>[master (root-commit) 63b66cf] Add Feature Y.</p>
<p>1 files changed, 2 insertions(+)</p>
<p>create mode 100644 A.java</p>
<p>$ <strong>git log</strong></p>
<p>commit 63b66cf74632ab3f2ebabb333e71d13938d7f2d4 (HEAD -&gt; master, origin/master, origin/HEAD)</p>
<p>Author: Karl R. Wurst &lt;karl@w-sts.com&gt;</p>
<p>Date: Fri Jan 18 16:02:12 2019 -0500</p>
<p>Add Feature Y.</p>
<p>commit db967767f9ab675dba21e08c5d20627b34cbe133</p>
<p>Author: Karl R. Wurst &lt;karl@w-sts.com&gt;</p>
<p>Date: Fri Jan 18 14:25:44 2019 -0500</p>
<p>Add Feature X.</p>
<p>$ <strong>git revert HEAD</strong></p>
<p>[master 685f4ab] Revert "First commit"</p>
<p>1 files changed, 2 deletions(-)</p>
<p>delete mode 100644 A.java</p>
<p>$ <strong>git log</strong></p>
<p>commit 685f4abfccda64d68145bae6a6123bf1e8a88021 (HEAD -&gt; master)</p>
<p>Author: Karl R. Wurst &lt;karl@w-sts.com&gt;</p>
<p>Date: Fri Jan 18 16:19:36 2019 -0500</p>
<p>Revert "Add Feature Y."</p>
<p>This reverts commit 63b66cf74632ab3f2ebabb333e71d13938d7f2d4.</p>
<p>commit 63b66cf74632ab3f2ebabb333e71d13938d7f2d4</p>
<p>Author: Karl R. Wurst &lt;karl@w-sts.com&gt;</p>
<p>Date: Fri Jan 18 16:02:12 2019 -0500</p>
<p>Add Feature Y.</p>
<p>commit db967767f9ab675dba21e08c5d20627b34cbe133</p>
<p>Author: Karl R. Wurst &lt;karl@w-sts.com&gt;</p>
<p>Date: Fri Jan 18 14:25:44 2019 -0500</p>
<p>Add Feature X.</p>
<p>$ <strong>cat A.java</strong></p>
<p>This is change #1.</p></td>
</tr>
</tbody>
</table>

## Questions (15 min)

1.  > What are the contents of A.java before command \#5?

2.  > What are the contents of A.java after command \#5?

3.  > Explain what happens in command \#7 through command \#9.

After issuing command \#9, you decide that you should not have committed
your changes to A.java.

4.  > What are the contents of A.java after command \#10?

5.  > What is the effect of command \#10? Be sure your explanation
    > refers to at least one of the three states, and to the log.

6.  > What is the default commit message from command \#10?

7.  > How does **revert** relate to **HEAD** in command \#10? How did
    > you figure that out?

8.  > Are the changes you made to A.java in command \#5 really undone?
    > Explain your answer. Why do you think git works this way?

9.  > Describe a situation where you would find command \#10 useful?

![](media/image1.png)Copyright © 2019 Karl R. Wurst. This work is
licensed under a Creative Commons Attribution-ShareAlike 4.0
International License.
