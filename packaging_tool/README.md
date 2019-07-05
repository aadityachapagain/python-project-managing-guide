## MAKEFILE WITH PYTHON

 like easy life. I like to open some repository and as simply as possible to run the example and see how the project works. Ideally, just calling one script and that’s it.

Python is awesome, Python makes a lot of things very easy. But tooling around, mostly packaging, is not working well. It has a lot of flaws. I’m used to fix this with Makefile. Some people are furious about that and argue that it’s only for building C codes. Well… maybe. But I prefer to be practical.

Please proceed to the code to know better about code.Its in Makefile (here)[https://github.com/aadityachapagain/python-project-managing-guide/blob/master/packaging_tool/Makefile]

It’s a very simple Makefile which I like to start with any project. It helps me to install all dependencies I need without searching and run the project (or tests, or lints or whatever) without remembering how the tool for it look like.

The best feature is how Makefile works. Notice venv target. It says that it needs to have script venv/bin/activate which needs setup.py. Makefile will run venv target only when you remove (or don’t have yet) virtual environment or you change setup.py. Because I use venv as a dependency for all tasks, I can change my Python dependencies and just run the tests. Makefile will ensure that a virtual environment is updated.

So… maybe Makefile is only for compiling codes… but anyway I think this is very clever. I could use normal bash scripts, sure, but why? It’s hard to keep them executable in git repository, not fast to type and I would need to write logic which Makefile already provides.