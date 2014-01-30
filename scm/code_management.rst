===============
Code Management
===============

Best Practices
--------------

1. Set up abstract Layer between your Version Control System system and the entire SCM Toolkit.
2. Atomicity, so every operation is atomic, 0 or 1, True or False, there are no states in between.
3. Avoid storing different types of data than the actual source code (for instance: binary files, executables, media, pdf..).

.. todo:: add missing 7 points

Common Problems
---------------

Performance & Scaling
^^^^^^^^^^^^^^^^^^^^^

* Facebook and Git performance issues: facbook-git_
* Facebook and Mercurial scaling: facebook-mercurial_ 

.. _facbook-git: http://thread.gmane.org/gmane.comp.version-control.git/189776
.. _facebook-mercurial: https://code.facebook.com/posts/218678814984400/scaling-mercurial-at-facebook/

Binary Files
^^^^^^^^^^^^

For every Distributed Version Control System (DVCS) handling (especially large) binary files is an issue. 

* Using Git to Manage the Storage and Versioning of Digital Objects richard-anderson-stanford_
* Git & Perforce comparison: git-perforce-bin-files_
* Linus Torvalds about big objects in Git: linus-big-objects_

.. _richard-anderson-stanford: http://www.google.pl/url?sa=t&rct=j&q=git%20large%20binary%20issue&source=web&cd=7&cad=rja&ved=0CFYQFjAG&url=http%3A%2F%2Flib.stanford.edu%2Ffiles%2FUsing-Git-to-Manage-the-Storage-and-Versioning-of-Digital-Objects.doc&ei=kNnBUZL2HI3sO4KXgJgB&usg=AFQjCNEDHSuJFY0_kaT_2r8DqoNaHtzrgQ
.. _git-perforce-bin-files: _http://osdir.com/ml/git/2009-05/msg00051.html
.. _linus-big-objects: http://kerneltrap.org/mailarchive/git/2006/2/8/200591



Creating Workspace
^^^^^^^^^^^^^^^^^^

For every Distributed Version Control System (DVCS) creating a workspace operation may be an issue, especially for big repositories or repositories with a big number of projets (subrepositories).

* Facebook: "it takes about 10 minutes to begin discovering commits in Facebook's 350,000-commit primary repository, and about 18 hours to import it all with 64 taskmasters on modern hardware." Source: facebook-creating-workspace_.

.. _facebook-creating-workspace: http://www.phabricator.com/docs/phabricator/article/Diffusion_User_Guide.html


VCS/DVCS Migrations
^^^^^^^^^^^^^^^^^^^

* Eight key points to consider: clearvision-migrations_

.. _clearvision-migrations: http://www.clearvision-cm.com/blog/migrating-your-scm-tool-8-key-points-to-consider-2/


Large Changes in Code Review
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Most of Code Review tools do not support large changes.

* How Facebook deals with the problem: facebook-large-changes1_ and  _facebook-large-changes2_

.. _facebook-large-changes1: http://www.phabricator.com/docs/phabricator/article/Differential_User_Guide_Large_Changes.html
.. _facebook-large-changes2: http://www.phabricator.com/docs/phabricator/article/Configuring_File_Upload_Limits.html


Versioning
^^^^^^^^^^

Android
"""""""

Starting with Cupcake, individual builds are identified with a short build code, e.g. FRF85B. The first letter is the code name of the release family, e.g. F is Froyo. The second letter is a branch code that allows Google to identify the exact code branch that the build was made from, and R is by convention the primary release branch. The next letter and two digits are a date code. The letter counts quarters, with A being Q1 2009. Therefore, F is Q2 2010. The two digits count days within the quarter, so F85 is June 24 2010. Finally, the last letter identifies individual versions related to the same date code, sequentially starting with A; A is actually implicit and usually omitted for brevity.

* Versioning - an Underrated Discipline: versioning-underrated-discipline_

.. _versioning-underrated-discipline: http://lgiordani.github.io/blog/2013/03/20/versioning-an-underrated-discipline/


