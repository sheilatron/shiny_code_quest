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

- [ ] Complete the tutorial [How To Package Your Python Code](http://www.scotttorborg.com/python-packaging/) 
- [ ] Convert the resulting codebase into a Git repository
    - [ ] Configure Git for line endings, author, etc.
    - [ ] Avoid committing useless auto-generated files
- [ ] Add additional source & tests
- [ ] Achieve 100% test coverage
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

This workshop assumes some pre-existing knowledge of Python,
though not much. It does require editing Python files, being
comfortable with the command line environment, and being willing
to explore the web to find relevant documentation.


#### Install Python

Python comes pre-installed on Linux and Mac, though the versions vary.  The
recommended Python versions are 2.7, 3.3, or 3.4, though you could probably
make due with 2.6. If you need to install it, try searching the web!

Note: This workshop has not yet been tested with Python 3.x or higher, but it
should be possible!

#### Install Your Favorite Text Editor or IDE

If you're just getting started programming, choose something easy
which you're comfortable working with. If in doubt, search the web for
suggestions!


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


#### Create Boilerplate Python Project Folder

- [ ] Create a folder somewhere; call it what you like
- [ ] Populate the folder with a basic Python project skeleton
      with a setup.py using setuptools (not distutils!)

At this point you have a number of options: create the project skeleton
manually, or use a tool, such as tooth.paste which does a lot of the work
for you.

Hint: Here's a Good Tutorial
    http://www.scotttorborg.com/python-packaging/everything.html

You could also try out tooth.paste
http://toothpaste.readthedocs.org/en/latest/

See also:
    https://pythonhosted.org/an_example_pypi_project/index.html
    http://peterdowns.com/posts/first-time-with-pypi.html
    https://hynek.me/articles/sharing-your-labor-of-love-pypi-quick-and-dirty/


#### Put Project Folder Under Git Version Control

GitHub has [nice docs for setting up Git](https://help.github.com/articles/set-up-git).

- [ ] Install Git for your platform
- [ ] Configure global Git settings
- [ ] Make your project folder into a Git repository
    - [ ] cd into the project folder
    - [ ] type "git init"
    - [ ] learn how to add & commit using Git
    - [ ] commit your files with comments!


#### Add Source Code to the Project

At this point, you can use whatever source code you like, either something
of your own, or something from a tutorial.

There are some requirements for purposes of this tutorial:

- [ ] There should be a "main" function somewhere
- [ ] The initial version of the code should be committed in Git



#### Create & Run Console Script

- [ ] create a console script entry in setup.py to execute
      the script 

Example setup.py excerpt:

```
entry_points={
  'console_scripts': [
      'approach_the_keeper = shiny.scripts:approach_the_keeper',
      ]}
```


#### Add Tests

A few sample tests are included to help you get started.
You'll need to make a few more to achieve 100% test coverage.

- [ ] Run the tests
- [ ] Fix the failing tests
- [ ] Run coverage report to find the missing test coverage
- [ ] Add the missing tests


#### Check Code: Run Code Checkers

Pick out a code checker such as Flake8 or pylint.

The easiest code checker to start out with the plain pep8 script.


#### Setup Sphinx for Documentation

- [ ] Create Sphinx project skeleton using [sphinx-quickstart](http://sphinx-doc.org/tutorial.html#setting-up-the-documentation-sources)
- [ ] Modify docs/conf.py and makefile with appropriate settings (TODO)
- [ ] Generate HTML docs by [running the Sphinx build](http://sphinx-doc.org/tutorial.html#running-the-build)
- [ ] Open generated index.html to behold rendered docs


#### Write Docs

Make sure you have docstrings for your modules, classes,
and functions. The exception would be private methods or functions,
prefixed with an "_" by convention.

Research the various docstring styles! Pick a style for your
docstrings and be consistent. Two popular styles are "Google style"
and "Numpy style" docstrings.

Next: Create Sphinx docs and render them as HTML.

- [ ] Fill in index.rst with some explanatory text.
- [ ] Create an api_doc.rst, add it to index.rst toctree
- [ ] Create a narrative.rst, add it to the index.rst toctree


#### Commit and Push Changes

You mean you haven't been doing commits this whole time? Better get
caught up with that!

- [ ] [Commit all the things!!!](http://i.stack.imgur.com/BxolD.jpg)
      With helpful comments.
- [ ] Create a repo on GitHub, BitBucket or similar.
- [ ] Add your remote Git repo as a git "remote"
`git remote add origin <your repo uri>
- [ ] Push the changes to the repo.
- [ ] Profit!


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

