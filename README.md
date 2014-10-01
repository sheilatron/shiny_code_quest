Tools & Tests: A Python Quest
=============================

A Half-Day (hopefully!) Workshop for Python Beginner to Intermediate Level


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

#### Prerequisites

Prior to starting the workshop, it would help to have the following
in place:

* Know at least a little Python programming
* Have a text editor and be ready to use it
* Have Python installed (recommended versions 2.7, 3.3, or 3.4)


###### Tip for Windows Users

Sometimes it's not easy being a Windows user in an open source world.
To make it a little easier to get by, try out the
[Chocolatey package manager](https://chocolatey.org/)!
Chocolatey provides a convenient command line installer for free software
devoid of bloatware barnacles! While not as extensively stocked as
Linux-based software repositories, it's a huge improvement over tedious GUI
install wizards which require you to manually download and run each installer
individually. For purposes of preparing for this workshop, it can save
you a lot of time.

With Chocolatey, here are some of the things you could install:

```
choco install python2
choco install python3
choco install 7zip
choco install git
choco install gitextensions
choco install GitHub
choco install notepadplusplus
choco install SublimeText3
choco install KickAssVim
choco install vim
choco install Emacs
```

The above are only examples; Windows users should window-shop for packages
on the (chocolatey repository](https://chocolatey.org/packages)


#### Install Package Management Tools

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


#### Set Up Python Sandbox Using Virtualenv

- [ ] Create a folder to store your virtualenv subfolders 
- [ ] Create a virtualenv called "questdev"
- [ ] Activate "questdev" within your console shell

Links for Learning virtualenv:

    * [Official virtualenv docs](http://virtualenv.readthedocs.org/en/latest/virtualenv.html)
    * [Hitchhiker's Guide to Virtualenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/) 
    * [A non-magical introduction to Pip and Virtualenv for Python beginners](http://www.dabapps.com/blog/introduction-to-pip-and-virtualenv-python/)


#### Create Project Folder

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

See also:
    Funniest: http://www.scotttorborg.com/python-packaging/everything.html
    https://pythonhosted.org/an_example_pypi_project/index.html
    http://peterdowns.com/posts/first-time-with-pypi.html
    https://hynek.me/articles/sharing-your-labor-of-love-pypi-quick-and-dirty/

If you get stuck on this, download the sample skeleton and use that
instead. TODO

#### Set Up Git

GitHub has [nice docs for setting up Git](https://help.github.com/articles/set-up-git) on how to set up Git.

- [ ] Install Git for your platform
- [ ] Configure global Git settings
- [ ] Make your project folder into a Git repository
    - [ ] cd into your shiny_code_quest folder
    - [ ] type "git init"


#### Add Source Code to the Project

- [ ] Download the grubby_grail.tar.gz file TODO add URI
- [ ] Decompress grubby_grail using "tar -xvf grubby_grail.tar.gz"
- [ ] Populate the 


#### Make It Run

- [ ] create a console script entry in setup.py to execute
      the script 

```python
entry_points={
  'console_scripts': [
      'approach_the_keeper = shiny.scripts:approach_the_keeper',
      ]}
```

- [ ] run the console script: approach_the_keeper


#### Add Tests

A few sample tests are included to help you get started.
You'll need to make a few more to achieve 100% test coverage.

- [ ] Run the tests
- [ ] Fix the failing tests
- [ ] Run coverage report to find the missing test coverage
- [ ] Add the missing tests


#### Improve Coding Style

- [ ] install PEP8 code checker
- [ ] run PEP8 checker

TODO other code checkers, flake8 etc.


#### Setup Sphinx for Documentation

- [ ] Create Sphinx project skeleton using [sphinx-quickstart](http://sphinx-doc.org/tutorial.html#setting-up-the-documentation-sources)
- [ ] Modify docs/conf.py and makefile with appropriate settings (TODO)
- [ ] Generate HTML docs by [running the Sphinx build](http://sphinx-doc.org/tutorial.html#running-the-build)
- [ ] Open generated index.html to behold rendered docs


#### Write Docs

- [ ] Add missing docstrings marked with "TODO"
- [ ] Fill in index.rst with some explanatory text.
- [ ] Create an api_doc.rst, add it to index.rst toctree
- [ ] Create a narrative.rst, add it to the index.rst toctree


#### Commit and Push Changes

You mean you haven't been doing commits this whole time? Better get
caught up with that!

- [ ] [Commit all the things!!!](http://i.stack.imgur.com/BxolD.jpg)
      With helpful comments.
- [ ] Create a repo on GitHub, BitBucket or similar. One option is to fork
      [shiny_code_quest](https://github.com/sheilatron/shiny_code_quest)
- [ ] Add your remote Git repo as a git "remote"
`git remote add origin <your repo uri>
- [ ] Push the changes to the repo.


#### Test Installation

- [ ] Create distributions for common formats (take your pick)
    - [ ] wheel
    - [ ] sdist
    - [ ] msi
    - [ ] egg

Examples:
```
python setup.py sdist
python setup.py bdist_msi
python setup.py bdist_egg
```
See also [docs on creating built distributions](https://docs.python.org/2/distutils/builtdist.html)

- [ ] Open a new console shell window
- [ ] Create a new virtualenv called "questtest"
- [ ] Activate questtest
- [ ] Navigate to the directory where you created the distribution
      (usually the 'dist' directory of your project folder)
- [ ] Install the package using "questtest" Python interpreter
- [ ] Validate that the command line script works "approach_the_keeper"



#### Publish a Release on the Test Packaging Server

- [ ] Publish the package using twine to the test package server

https://wiki.python.org/moin/TestPyPI
https://testpypi.python.org/pypi

- [ ] Create another virtualenv, and attempt to install from the
      test package server

