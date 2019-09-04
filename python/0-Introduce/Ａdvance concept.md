PEP{
Python Enhancement Proposals (PEP) are suggestions for improvements to the language, made by experienced Python developers. 
PEP 8 is a style guide on the subject of writing readable code. It contains a number of guidelines in reference to variable names, which are summarized here:
- modules should have short, all-lowercase names; 
- class names should be in the CapWords style; 
- most variables and function names should be lowercase_with_underscores; 
- constants (variables that never change value) should be CAPS_WITH_UNDERSCORES;
- names that would clash with Python keywords (such as 'class' or 'if') should have a trailing underscore.
PEP 8 also recommends using spaces around operators and after commas to increase readability. 

Other PEP 8 suggestions include the following:
- lines shouldn't be longer than 80 characters; 
- 'from module import *' should be avoided; 
- there should only be one statement per line.

It also suggests that you use spaces, rather than tabs, to indent. However, to some extent, this is a matter of personal preference. If you use spaces, only use 4 per line. It's more important to choose one and stick to it.


}

Major 3rd-Party Libraries{
The Python standard library alone contains extensive functionality. 
However, some tasks require the use of third-party libraries. Some major third-party libraries:
Django: The most frequently used web framework written in Python, Django powers websites that include Instagram and Disqus. It has many useful features, and whatever features it lacks are covered by extension packages. 
CherryPy and Flask are also popular web frameworks.

For scraping data from websites, the library BeautifulSoup is very useful, and leads to better results than building your own scraper with regular expressions.

A number of third-party modules are available that make it much easier to carry out scientific and mathematical computing with Python.
The module matplotlib allows you to create graphs based on data in Python. 
The module NumPy allows for the use of multidimensional arrays that are much faster than the native Python solution of nested lists. It also contains functions to perform mathematical operations such as matrix transformations on the arrays. 
The library SciPy contains numerous extensions to the functionality of NumPy.

Python can also be used for game development. 
Usually, it is used as a scripting language for games written in other languages, but it can be used to make games by itself. 

For 3D games, the library Panda3D can be used. For 2D games, you can use pygame.

}

Packaging{
In Python, the term packaging refers to putting modules you have written in a standard format, so that other programmers can install and use them with ease. 
This involves use of the modules setuptools and distutils. 
The first step in packaging is to organize existing files correctly. Place all of the files you want to put in a library in the same parent directory. This directory should also contain a file called __init__.py, which can be blank but must be present in the directory.
This directory goes into another directory containing the readme and license, as well as an important file called setup.py. 

After creating the setup.py file, upload it to PyPI, or use the command line to create a binary distribution (an executable installer).
To build a source distribution, use the command line to navigate to the directory containing setup.py, and run the command python setup.py sdist.
Run python setup.py bdist or, for Windows, python setup.py bdist_wininst to build a binary distribution. 
Use python setup.py register, followed by python setup.py sdist upload to upload a package.

The previous lesson covered packaging modules for use by other Python programmers. However, many computer users who are not programmers do not have Python installed. Therefore, it is useful to package scripts as executable files for the relevant platform, such as the Windows or Mac operating systems. This is not necessary for Linux, as most Linux users do have Python installed, and are able to run scripts as they are. 

For Windows, many tools are available for converting scripts to executables. For example, py2exe, can be used to package a Python script, along with the libraries it requires, into a single executable.
PyInstaller and cx_Freeze serve the same purpose.

For Macs, use py2app, PyInstaller or cx_Freeze.

Standard Library{
Many third-party Python modules are stored on the Python Package Index (PyPI)
The best way to install these is using a program called pip
pip install library_name

}
