Tools & Tests: A Python Quest
=============================

A Half-Day Workshop for Python Beginner to Intermediate Level


Is This For Me?
---------------

You've gone through a few Python tutorials, maybe a book or two...
maybe you've written some code. What next?

You might want to think about:

* Leveraging 3rd party Python libraries from the vast PyPI "Cheeseshop"
    - Without cluttering up your "system Python" environment
* Putting your code under version control
    - Versus manually backing up versions of source code files
* Putting your code up on Github where it can be reviewed and possibly
  improved by others ("social coding")...and safely backed up.
* Write automated tests to provide quick feedback about whether
  your code does what you expect
* Publish your code as a 3rd party library in a way that is convenient
  for others to install.
    - with documentation!
    - with metadata! (keywords, author, declared dependencies, etc.)
* Polish your code with checkers to help you achieve a consistent
  and readable coding style, clean out useless bits, code duplication, common
  antipatterns, meet Python community standards (PEP8), etc.  To understand why
  this matters, try Googling "benefits of having a coding style"

Maybe you already know this stuff, but could benefit from filling in a few gaps
in your knowledge. The parts you already know won't take much time to
complete, and you can get help to speed your learning on the parts you don't know.

This workshop hits a lot of high points, without going deeply into one area,
enabling students to become familiar with an end-to-end toolchain. More
importantly, students will have overcome obstacles in understanding and
using the various tool, thus gaining confidence and ability to apply the
tools to their own projects.

Caveat/Disclaimer: This workshop "quest" format is experimental.
                   PyTexas 2014 is the first iterations. The instructor
                   requests your assistance in making this a successful
                   learning experience for all participants, present
                   and future.


The Quest
---------


You might not be able to finish this quest during the workshop!
That's ok...do the best you can, and keep pestering the instructor
afterwards until you have completed it.


To complete the quest, students must achieve the following:


- [ ] Download the "shiny_code_quest.tar.gz" blob of messy code
- [ ] Reorganize it into a standard Python project structure
- [ ] Convert it into a Git repository and commit initial + changes
    - [ ] Configure Git for line endings, author, etc.
    - [ ] Avoid committing useless auto-generated files
- [ ] Add tests and achieve 100% test coverage
- [ ] Manually verify working command line scripts
- [ ] Pass PEP8 checker
- [ ] Use Sphinx to generate docs from text files and docstrings
- [ ] Publish source on GitHub, BitBucket, or similar
- [ ] Build installable distribution with appropriate metadata
- [ ] Clone and test in a local virtualenv
- [ ] Publish on the PyPI test site
- [ ] Install from the PyPI test site into a local virtualenv

Does this seem like a lot to figure out? Quests aren't supposed to be easy! But
you'll have help when you need it from teachers and other students.

Instead of spelling out detailed instructions, this quest will provide pointers
on the way to help you figure out the solution using various documentation
links on the web.



Tasks Checklist
---------------

Prerequisites
+++++++++++++

Prior to starting the workshop, it would help to have the following
in place:

* Know at least a little Python programming
* Have a text editor and be ready to use it
* Have Python installed (recommended versions 2.7, 3.3, or 3.4)


Install Package Management Tools
++++++++++++++++++++++++++++++++

These need to be installed in your Python executable environment,
whether you're using a pre-installed system Python, or a special
Python you installed yourself.

Here's a nice set of ["all in one instructions"](https://packaging.python.org/en/latest/tutorial.html#installing-the-tools) on the official Python Packaging Authority website, to help you install all of the following:

- [ ] Install [setuptools](https://packaging.python.org/en/latest/projects.html#setuptools)
- [ ] Install [pip](http://pip.readthedocs.org/en/latest/installing.html)
- [ ] Install [twine](https://packaging.python.org/en/latest/projects.html#twine)
- [ ] Install virtualenv (only needed if Python < 3.3)
      Python 3.3 includes venv which can be used instead
- [ ] Install wheel


Set Up Python Sandbox Using Virtualenv
++++++++++++++++++++++++++++++++++++++

- [ ] Create a folder to store your virtualenv subfolders 
- [ ] Create a virtualenv called "questdev"
- [ ] Activate "questdev" within your console shell

Links for Learning virtualenv:

    * [Official virtualenv docs](http://virtualenv.readthedocs.org/en/latest/virtualenv.html)
    * [Hitchhiker's Guide to Virtualenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/) 
    * [A non-magical introduction to Pip and Virtualenv for Python beginners](http://www.dabapps.com/blog/introduction-to-pip-and-virtualenv-python/)


Create Project Folder
+++++++++++++++++++++

- [ ] Create a folder somewhere called shiny_code_quest
- [ ] Populate the folder with a basic Python project skeleton

At this point you have a number of options: create the project skeleton
manually, or use a tool, such as tooth.paste which does a lot of the work
for you.

http://toothpaste.readthedocs.org/en/latest/

This one could be tricky...don't be afraid to ask for help
if it fails to install correctly!

Most things from PyPI are pretty easy to install..."pip install whatever".
But sometimes you may run across something that needs a compiler, or has
a broken dependency, etc.


Add Source Code to the Project
++++++++++++++++++++++++++++++

- [ ] Download the grubby_grail.tar.gz file TODO add URI
- [ ] Decompress grubby_grail using "tar -xvf grubby_grail.tar.gz"
- [ ] Populate the 


Make It Run
+++++++++++

- [ ] 
This source code has some depe

Add Tests
+++++++++

TODO
- [ ] Run coverage report to find the missing test coverage



Improve Coding Style
++++++++++++++++++++

- [ ] install PEP8 code checker
- [ ] run PEP8 checker

TODO other code checkers, flake8 etc.


Publish a Release on the Test Packaging Server
++++++++++++++++++++++++++++++++++++++++++++++

https://wiki.python.org/moin/TestPyPI
https://testpypi.python.org/pypi

