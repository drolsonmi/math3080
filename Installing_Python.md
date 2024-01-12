# Installing Python
Note: Since MacOS is unix-based, python is automatically installed on your machine. Open a terminal and run python. You may still want to run a good IDE, such as VisualStudioCodeLinks to an external site..

## Options for Windows:
1. Anaconda or Miniconda (Installation process outlined in the beginning of Data Science from Scratch, Chapter 2)  
    * [Installing Anaconda and Miniconda on Windows](https://docs.conda.io/projects/conda/en/latest/user-guide/install/windows.html)
      * [Installing on Windows — Anaconda documentation](https://docs.anaconda.com/anaconda/install/windows/)
    * [User guide — Anaconda documentation](https://docs.anaconda.com/anaconda/user-guide/)
    * [Miniconda — conda documentation](https://docs.conda.io/en/latest/miniconda.html)
2. Install Python directly
    * [Python For Beginners | Python.org](https://www.python.org/about/gettingstarted/)
3. WSL
    * [Set Up Python on Windows Subsystem for Linux (WSL) | by Fahadul Shadhin | Python in Plain English](https://python.plainenglish.io/setting-up-python-on-windows-subsystem-for-linux-wsl-26510f1b2d80)
4. Google CoLab
    * [https://colab.research.google.com/](https://colab.research.google.com/)
    * Need a Google account to save work
    * CoLab works by processing your code on a centralized processor which all CoLab users share. This means that if it is busy, you have to wait your turn to execute your code. 
    * This will work for this class, but if you intend to do more Data Science work, I recommend installing it directly on your computer

## Running Python
### from the Command Line
From the command line, run `python`.
```python
1+4
print('Hello World!')
print('I am',30 + 5,'years old!')
To exit, type exit()
```

### from a file
Alternatively, save code in a file. For example, save the following in the file *Hello.py*:
```python
print('Hello World! My name is Michael.')
```

Then from the command line, type `python Hello.py`.

### IPython
The best way to write a program is to use an IDE (integrated development environment). An alternative to python from the command line or from a file is __IPython__. Here are some advantages:
* Tab-Completion
    * Press `Tab` to complete a command, filename, variable, etc.
* Magic Functions
    * Certain command-line functions can be completed within python.
    * Preface with `%`. For example, within iPython, type
      ```python
      %pwd
      %mkdir tmp
      %cd tmp
      ```
    * Magic Functions also make coding easier. For example, if you want to copy-paste a block of code, try:
      ```python
      %paste
      %cpaste
      ```
* Introspection
    * If you want to know more about a function, type a ? after the command:
      ```python
      print?
      ```
      This also works for variables and other objects within python. Any information available within your python installation will be displayed.

If you use `??`, source-code will also be displayed.

### Jupyter Notebook / Lab (Google CoLab uses Jupyter Notebook format)
Jupyter Notebook runs just like IPython. They were originally one and the same. In Jupyter Notebook, your code is separated in cells. This is a happy balance between command-line and file-stored programs. You have other advantages:
* HTML based
    * Output is HTML based, so is much cleaner than a text-based command-line output.
* Inline images
    * When we talk about images, you will be able to see your images within Notebook. You would not be able to see these images in the command-line.
* More on Introspection
    * Just like IPython, you can use the introspection commands (? and ??) to learn more of a function. But if you are wanting that information without leaving your work, you can type Shift-Tab. This will produce a pop-up window with the same information as ?. This allows quick reference while typing your program.
* Markdown
    * Some cells can be turned into Markdown cells. This is simplified HTML coding, providing an easy way to annotate your work.
* Lab
    * Jupyter Lab is based on Notebook, but provides a setup with the following in one window:
      * File Directory
      * Tabs for all open files
        * Tabs can be tiled
      * Console (Like command-line input, but with HTML output)
      * Terminal (for file browsing purposes, or for executing file-stored python programs…)
      * Markdown files

## Interrupting
If you have a run-away code (e.g. infinite loop), you can
1. use `Ctrl-c` to interrupt the command (command-line, IPython, or Jupyter)
2. go to the “Kernel” menu and select “Interrupt”

## Closing Jupyter Notebook or Jupyter Lab
When you started Notebook/Lab, you saw that a terminal window opened. To close Notebook or Lab,
1. Shutdown all running Kernels
2. Quit from Notebook/Lab in the File Menu
3. Press Ctrl-C twice in the terminal window

You could just do step (3), but could cause problems with the hardware of the computer, leaving stacks of information in memory and processes in the processor. It is best to properly close every time.