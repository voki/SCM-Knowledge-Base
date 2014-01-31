===============
Code Management
===============

Best Practices
--------------

1. Build an abstract Layer between your Version Control System system and the entire SCM Toolkit.
2. Atomicity, so every operation is atomic, 0 or 1, True or False, there are no states in between.
3. Avoid storing different types of data than the actual source code (no binfiles, media, etc..).

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
.. _git-perforce-bin-files: http://osdir.com/ml/git/2009-05/msg00051.html
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

* How Facebook deals with the problem: facebook-large-changes1_ and facebook-large-changes2_

.. _facebook-large-changes1: http://www.phabricator.com/docs/phabricator/article/Differential_User_Guide_Large_Changes.html
.. _facebook-large-changes2: http://www.phabricator.com/docs/phabricator/article/Configuring_File_Upload_Limits.html


Versioning
^^^^^^^^^^

Android
"""""""

Starting with Cupcake, individual builds are identified with a short build code, e.g. FRF85B. The first letter is the code name of the release family, e.g. F is Froyo. The second letter is a branch code that allows Google to identify the exact code branch that the build was made from, and R is by convention the primary release branch. The next letter and two digits are a date code. The letter counts quarters, with A being Q1 2009. Therefore, F is Q2 2010. The two digits count days within the quarter, so F85 is June 24 2010. Finally, the last letter identifies individual versions related to the same date code, sequentially starting with A; A is actually implicit and usually omitted for brevity.

* Versioning - an Underrated Discipline: versioning-underrated-discipline_

.. _versioning-underrated-discipline: http://lgiordani.github.io/blog/2013/03/20/versioning-an-underrated-discipline/

Tools
-----

Centralized VS Distributed
^^^^^^^^^^^^^^^^^^^^^^^^^^

* Attlassian blog: atlassian-blog_

.. _atlassian-blog: http://blogs.atlassian.com/2012/02/version-control-centralized-dvcs/?utm_source=wac-dvcs&utm_medium=text&utm_content=dvcs-options-git-or-mercurial


Git, Mercurial and Bazaar domination
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Clearvision: clearvision-dvcs_
* RedMonk: redmonk-dvcs_
* Ian Skerrett: ianskerrett-dvcs_
* Atlassian: atlassian-dvcs_
* Why switch to Bazaar: bazaar-switch_

.. _clearvision-dvcs: http://www.clearvision-cm.com/clearvision-news/is-2013-the-year-for-dvcs-domination.html
.. _redmonk-dvcs: http://redmonk.com/sogrady/2012/11/05/dvcs-2012/
.. _ianskerrett-dvcs: http://ianskerrett.wordpress.com/2012/06/08/eclipse-community-survey-result-for-2012/
.. _atlassian-dvcs: http://www.atlassian.com/dvcs/overview/dvcs-options-git-or-mercurial
.. _bazaar-switch: http://doc.bazaar.canonical.com/migration/en/why-switch-to-bazaar.html

Git
^^^

* How to Deal with mess in Git?: deal-with-git-mess_
* Useful Tips: useful-tips_
* Gitflow - branching model: gitflow-branching-model_

.. _deal-with-git-mess: http://justinhileman.info/article/git-pretty/git-pretty.png
.. _useful-tips: http://justinhileman.info/article/changing-history/
.. _gitflow-branching-model: http://nvie.com/posts/a-successful-git-branching-model/


Tools and Plugins
"""""""""""""""""

* Sexy bash prompt: sexy-bash-prompt_
* Gittle: gittle_

.. _sexy-bash-prompt: https://github.com/twolfson/sexy-bash-prompt
.. _gittle: https://github.com/FriendCode/gittle


Git Propaganda
""""""""""""""

* Microsoft announces Git support: http://techcrunch.com/2013/01/30/microsoft-announces-git-support-for-visual-studio-team-foundation-server-and-service/
* Google announces Git support: http://googlecode.blogspot.de/2011/08/announcing-git-support-for-google-code.html
* Bitbucket announces Git support: http://blog.bitbucket.org/2011/10/03/bitbucket-now-rocks-git/
* CodePlex: http://blogs.msdn.com/b/bharry/archive/2010/01/27/codeplex-now-supports-mercurial.aspx

.. _microsoft-announces-git: http://techcrunch.com/2013/01/30/microsoft-announces-git-support-for-visual-studio-team-foundation-server-and-service/
.. _google-announces-git: http://googlecode.blogspot.de/2011/08/announcing-git-support-for-google-code.html
.. _bitbucket-announces-git: http://blog.bitbucket.org/2011/10/03/bitbucket-now-rocks-git/
.. _codeplex-announces-git: http://blogs.msdn.com/b/bharry/archive/2010/01/27/codeplex-now-supports-mercurial.aspx

Git Branching
"""""""""""""

* Stackoverflow: stackoverflow-branching_
* Reinh: reinh-branching_
* nvie: nvie-branching_
* Github Flow: github-branching_

.. _stackoverflow-branching: http://stackoverflow.com/questions/2621610/what-git-branching-models-actually-work
.. _reinh-branching: http://reinh.com/blog/2009/03/02/a-git-workflow-for-agile-teams.html
.. _nvie-branching: http://nvie.com/git-model/
.. _github-branching: http://scottchacon.com/2011/08/31/github-flow.html

Git on Windows
""""""""""""""

* Mercurial as a workaround: mercurial-git-workaround_ 

.. _mercurial-git-workaround: http://hg-git.github.com

Git & Multiple Projects
"""""""""""""""""""""""

* Gitslave: gitslave_
* Submodules: submodules_

.. _gitslave: http://gitslave.sourceforge.net/
.. _submodules: http://git-scm.com/book/en/Git-Tools-Submodules


Online Tutorials
""""""""""""""""

* Pro Git book: pro-git_
* Interactive Git Tutorial: interactive-git_
* Git Immersion: git-immersion_
* Git Howto: git-howto_
* Git Pro [lang=PL]: git-pro_
* SAP documentation about Git & Gerrit: sap-gerrit_
* Bare vs non-bare repositories: bare-vs-nonbare_
* Git by Example: git-by-example_
* Visual Git Guide: visual-git-guide_
* Git Tutorial: git-tutorial_
* Git bisect: git-bisect_
* Video tutorial: video-tutorial_
* Git Pocket Guide: git-pocket_
* Code School: code-school_
* How to quickly to start with Git: how-to-start_

.. _pro-git: http://git-scm.com/book
.. _interactive-git: http://pcottle.github.com/learnGitBranching/
.. _git-immersion: http://gitimmersion.com/
.. _git-howto: http://githowto.com/
.. _git-pro: http://lab.mzr.jp/progit/progit.pl.pdf
.. _sap-gerrit: http://gerrit-training.scmforge.com/
.. _bare-vs-nonbare: http://www.bitflop.com/document/111
.. _git-by-example: http://marakana.com/training/git/git_by_example.html
.. _visual-git-guide: http://marklodato.github.io/visual-git-guide/index-en.html
.. _git-tutorial: http://schacon.github.io/git/gittutorial.html
.. _git-bisect: http://schacon.github.io/git/git-bisect-lk2009.html
.. _video-tutorial: https://www.youtube.com/watch?v=GYnOwPl8yCE
.. _git-pocket: http://chimera.labs.oreilly.com/books/1230000000561/index.html
.. _code-school: http://try.github.io/levels/1/challenges/1
.. _how-to-start: http://sixrevisions.com/web-development/easy-git-tutorial/


