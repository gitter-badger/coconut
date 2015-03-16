# Coconut Tutorial

This tutorial will teach you how to write clean, functional, Pythonic code using the [Coconut](https://github.com/evhub/coconut) programming language. It is assumed that the reader knows some basic Python, but no other prior knowledge or experience is required.

## I. Getting Started

### 1. Install Coconut

The first thing you're going to need to do is install Coconut. Since Coconut is hosted on the [Python Package Index](https://pypi.python.org/pypi/coconut), it can be installed easily using `pip`. Simply install [Python](https://www.python.org/downloads/), open up a command line prompt, and enter the following:
```
pip install coconut
```

To test that `coconut` is working, make sure the Coconut help appears when you enter into the command line:
```
coconut -h
```

_If the `pip` or `coconut` commands aren't working for you, try prefixing them with `python -m`, like so:_
```
python -m pip install coconut
python -m coconut -h
```

### 2. Set Up a Workspace

Now that you've installed Coconut, it's time to create your first Coconut program. Open up your favorite text editor and save a new file named `tutorial.coc`. It is recommended that you tell your text editor to treat all `.coc` files as Python source files for the purpose of syntax highlighting. All Coconut files should use the extension `.coc` so they can be recognized as such when compiling folders of many different files.

### 3. Start Coding!

If you're familiar with Python, then you're already familiar with most of Coconut. Coconut is nearly a strict superset of Python 3 syntax, with the sole exception of `lambda` statements, which will be later in this tutorial. For now, let's start with a simple `hello, world!` program:
```
print("hello, world!")
```

Now it's time to compile the file and run it to test that it works. Open up your command line and enter in:
```
cd <tutorial.coc directory>
coconut tutorial.coc
python tutorial.py
```

If everything is working properly, you should see something like this:
```
$ coconut tutorial.coc
Coconut: Compiling '<tutorial.coc directory>'...
Coconut: Compiled '<tutorial.py directory>'.
$ python tutorial.py
hello, world!
```

### 4. Understanding Compiled Code

You should now notice that a new file, `tutorial.py` was created in the `tutorial.coc` directory when you ran the compiler. That file contains the compiled Python code, which was why you had to enter `python tutorial.py` instead of `python tutorial.coc`.

Open `tutorial.py` and look inside. You should see two sections, `Coconut Header` and `Compiled Coconut`. The `Coconut Header` section contains code inserted into all compiled coconut files, whereas the `Compiled Coconut` section contains the specific code the compiler produced from your source file.

### 5. Understanding Compiled Folders

You might notice that the `Coconut Header` section in `tutorial.py` is rather large. This is because that section contains all the code necessary to set up the Coconut environment. Because Coconut needs to set up that environment in every file, it puts a header at the top.

It would be terribly innefficient, however, if Coconut put that entire header in every file of a module (or other folder of files that are intended to stay together). Instead, Coconut puts all of that code in a `__coconut__.py` file in each folder directory.

### 6. Compile a Folder!

To compile a module (or folder) this way, simply call the `coconut` command with the module (or folder) directory as the first argument. Go ahead and try it, like so:
```
coconut <tutorial.coc directory>
cd <tutorial.coc directory>
python tutorial.py
```

If everything is working properly, you should see exactly the same output as before.

If you now go into the `tutorial.coc` directory, however, you should see a new file, `__coconut__.py`, which contains the header from earlier in non-class form, and if you now open the `tutorial.py` file, you should see a significantly shortened header that imports the larger header file.

## II. Functions

## III. Iterators

## IV. Values

## V. Alternate Syntax