# 3D Slicer tutorial
3D Slicer learning material



## Contents

- [How to read this guide?](#how-to-read-this-guide)
- [What is 3D Slicer?](#what-is-3d-slicer)
- [Installation](#installation)
- [Directory structure](#directory-structure)
- [Python development](#python-development)
   - [Setting up an IDE](#setting-up-an-ide)
   - [Rapid prototyping](#rapid-prototyping)
   - [Installing additional packages](#installing-additional-packages)
- [Getting help](#getting-help)
- [Contributing](#contributing)



# How to read this guide?

This manual is written in [Markdown](https://en.wikipedia.org/wiki/Markdown). The simplest way to see its content rendered is by reading it on GitHub on the following link: https://github.com/BioTiM/Slicer_tutorial. Alternatively, you can read it locally on your machine using one of the many [Markdown editors](https://github.com/mundimark/awesome-markdown-editors).

The main sections seen in the table of contents above are generally independent from each other, so you can use this manual as a reference. Actually, this manual *is* more a reference than a step-by-step guide. Nevertheless, if you are a newbie to the programming of Slicer, consider advancing linearly. You can jump to any section through bookmarks, made visible by clicking on the ![toc_icon](images/toc_icon.png) icon in the top left corner of the guide (when browsing it on GitHub).

The manual is rich in inline references, which are hyperlinks that bring you to the web page where the information comes from. Apart from that, sections and subsections may have standalone references at the end, which let you further immerse in the topic.

If you notice typos, inaccurate or untrue information, or have questions or suggestions, please contact us (see section [**Contributing**](#contributing)) to improve this manual.



# What is 3D Slicer?

TBA



# Installation

TBA



# Directory structure

TBA



# Python development

TBA




## Setting up an IDE

Although using an [integrated development environment](https://en.wikipedia.org/wiki/Integrated_development_environment) (IDE) is not necessary, it provides several utilities that [make your development faster](#rapid-prototyping):
- Code completion; jumping among functions, classes, etc.; syntax highlighting; ...
- Integrates command line tools that enforce good Python programming habits
- Convenient debugging

In this tutorial, we provide instructions for [PyCharm](https://www.jetbrains.com/pycharm/), the leading IDE for Python development. The rest of the instructions apply to the following version: PyCharm 2022.1 (Community Edition). If you cannot find the settings described in this guide, [let us know](#contributing). First, download it from its website -- the Community Edition is free. Install PyCharm and perform the following steps to make it suitable for developing Slicer extensions:

1.  Create a new project

    *File* --> *New Project...* then select *Previously configured interpreter*. Navigate to the Python interpreter of Slicer, located at *<Slicer_root>/bin/PythonSlicer*. Once the project is created, PyCharm will create a hidden folder in your project root under the name *idea*. This is where it stores your IDE settings related to the newly created project.

2.  Configure the project

    By default, you will see the *Project* and *Structure* tabs on the left side bar. If you drop down the *External Libraries* menu within the *Project* tab, you can notice that the necessary packages that come with Slicer are automatically recognized.
    
    In older versions of PyCharm, the necessary libraries are not added to the path automatically. You can add them manually by clicking on *Add Content Root* in *File* --> *Settings* --> *Project Structure*:
    - *<Slicer_root>/bin/Python*
    - *<Slicer_root>/lib/Python*
    - *<Slicer_root>/lib/QtPlugins*
    - *<Slicer_root>/lib/Slicer-4.xx*

3. Test the configuration

    Create a new Python file (e.g. `test.py`) in the project and import some modules to check if everything works well:
    
    ```python
    import slicer.util
    import ctk
    import qt
    from DICOMLib import DICOMUtils
    ```
    
    Click on the `util` module while holding the Ctrl key. It should open the module, containing lots of functions. To navigate among those functions, activate the *Structure* tab on the left side bar.
    

This completes the basic configuration of PyCharm. Note that you cannot run your code from within PyCharm. The reason is that it requires dynamic libraries that are not found unless you run your code *from within* the Python interpreter of Slicer, as explained in the beginning of section [**Python development**](#python-development). Nevertheless, the properly configured Python environment allows you faster prototyping, as you will see next.

PyCharm comes with many useful bundled plugins. To catch even more potential bugs or coding style mistakes, here are some additional static analyzers we found useful over the years:

- [Pydantic](https://plugins.jetbrains.com/plugin/12861-pydantic)
- [Pylint](https://plugins.jetbrains.com/plugin/11084-pylint)
- [SonarLint](https://plugins.jetbrains.com/plugin/7973-sonarlint)
- [Sourcery](https://plugins.jetbrains.com/plugin/12631-sourcery)

For improved code completion, the following plugins proved to be handy:

- [AiXcoder Code Completer](https://plugins.jetbrains.com/plugin/13574-aixcoder-code-completer)
- [Tabnine AI Code Completion](https://plugins.jetbrains.com/plugin/12798-tabnine-ai-code-completion-js-java-python-ts-rust-go-php--more)



## Rapid prototyping

TBA



## Installing additional packages

TBA


# Getting help

If at any point in your development journey you get stuck, you can post your (well-formulated) question on the friendly [3D Slicer Discourse forum](https://discourse.slicer.org/).



# Contributing

If you are aware of other useful tricks for using Slicer or developing extensions, let us know by [creating an issue](https://github.com/BioTiM/Slicer_tutorial/issues), [opening a pull request](https://github.com/BioTiM/Slicer_tutorial/pulls) or [starting a discussion](https://github.com/BioTiM/Slicer_tutorial/discussions). The same applies if you find inaccuracies in this guide or if an explanation is not clear.
