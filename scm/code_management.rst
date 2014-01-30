===============
Code Management
===============

Best Practices
--------------

1. Abstract Layer between your Version Control System system and the entire SCM Toolkit.
2. Atomicity, so every operation is atomic, 0 or 1, True or False, there are no states in between.

.. todo:: add missing 8 points

Common Problems
---------------

Performance & Scaling
=====================

* Facebook and Git performance issues: facbook-git_
* Facebook and Mercurial scaling: facebook-mercurial_ 

.. _facbook-git: http://thread.gmane.org/gmane.comp.version-control.git/189776
.. _facebook-mercurial: https://code.facebook.com/posts/218678814984400/scaling-mercurial-at-facebook/
