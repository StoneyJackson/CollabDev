# Activity 12: Workflow


## Form teams

This should work for a 2 or 3 person team. Each team member will sometimes be a maintainer and sometimes a contributor.


## Overview

In this activity your team will play out several scenarios following steps
described in _Workflow Reference_ (at the end of this document).


## Create an organization on GitHub

- Name it what you like.
- Set the default permissions so that all organization members can create projects and write to any project in the organization.
- Add all team members to the organization.


## Create official upstream repository in organization

- Name it `favorites`
- Give it a default README.md file.


## Contributor setup

Have each team member follow the _Setup_ instructions in the workflow to prepare to work on the project.

## First contribution

Select one team member to make the first contribution. Call them contributor-1.
Select a different team member to act as maintainer.

- Help contributor-1 to follow _Starting your contribution_ to add a
  new file `favorite-foods.txt` that contains a couple of contributor-1's
  favorite foods.
- Help the maintainer to accept contributor-1's pull-request on GitHub.
- Help contributor-1 to follow _Update your master_ and
  _Delete unneeded branches_ to clean up.

Congratulations, your team has made its first contribution! Celebrate.


## Contributor-2 setup and second contribution

Select a team member who is not contributor-1, and call them contributor-2.
Select a team member other than contributor-2 to act as maintainer.

- Help Contributor-2 to follow _Update your master_ and _Starting your contribution_ to contribute a new file
  `favorite-movies.txt` with a couple of his/her favorite movies.
- Make sure that the maintainer has accepted contributor-2's pull-request and contributor-2 has updated their master and cleaned up.
- Help Contributor-1 to update their master branch.

Celebrate again.

(If you have a 3-person team, have the person who has not contributed yet to make add another favorites file.)


## Contribute conflicting changes

Each contributor can act as maintainer for the other contributor.

- Have contributor-1 and contributor-2 independently follow the contribution
  workflow to add another favorite food to the end of `favorite-foods.txt`.
- Maintainer, accept one of the pull-requests. Try to accept the other. You
  won't be able to because changes in the pull-request conflict with the other
  that you already accepted.
- Help the contributor with the unresolved pull-request to follow
  _Keep your repositories up-to-date_ to synchronize his/her
  repositories and resolve the conflicts.
- Maintainer, note that the conflicted pull-request is automatically updated and
  should be acceptable. Accept the pull-request.
- Have contributors clean up.

Celebrate enthusiastically. That was challenging.


## Multi-round contribution

- Have contributor-1 add another food, and contributor-2 another movie.
- Have the maintainer ask for a modification through the pull-request
  (e.g., "Please pick another flavor. I don't like chocolate.").
- Have contributors make, commit, and push the new changes.
- If the maintainer is satisfied, accept the pull-requests.
- Contributors, don't forget to clean up.

Notice how pull-requests provide a way for a contributor and a maintainer to
communicate about a proposed change. Also notice how the pull-request updates
automatically as new changes are pushed to the same branch.


## Squash

- Repeat the multi-round contribution until both contributors have made multiple
  commits.
- Maintainer, through the pull-request, ask contributors to squash their work
  into a single commit.
- Help contributors to follow _Squash your commits_ to squash their
  commits into a single commit and push it.
- Maintainer, accept the pull-requests once it contains the same work, but only
  a single commit.
- Contributors, don't forget to clean up.

This is another moment for an enthusiastic celebration. Well done!  


## Copyright and Licensing

Copyright 2016 Darci Burdge and Stoney Jackson SOME RIGHTS RESERVED

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
International License. To view a copy of this license, visit
http://creativecommons.org/licenses/by-sa/4.0/ .
