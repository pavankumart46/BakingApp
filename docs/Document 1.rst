===========================================
Document 1
===========================================

- Quick start
- Assuming you have Python already, install Sphinx:

::

    pip install sphinx
    
    
Create a directory inside your project to hold your docs:
::

    cd /path/to/project
    mkdir docs
    Run sphinx-quickstart in there:

cd docs
sphinx-quickstart
This quick start will walk you through creating the basic configuration; in most cases, you can just accept the defaults. When it’s done, you’ll have an index.rst, a conf.py and some other files. Add these to revision control.

Now, edit your index.rst and add some information about your project. Include as much detail as you like (refer to the reStructuredText syntax or this template if you need help). Build them to see how they look:

make html
Your index.rst has been built into index.html in your documentation output directory (typically _build/html/index.html). Open this file in your web browser to see your docs.

../_images/sphinx-hello-world.png
Your Sphinx project is built

Edit your files and rebuild until you like what you see, then commit your changes and push to your public repository. Once you have Sphinx documentation in a public repository, you can start using Read the Docs by importing your docs.

Using Markdown with Sphinx
You can use Markdown and reStructuredText in the same Sphinx project. We support this natively on Read the Docs, and you can do it locally:

pip install recommonmark
Then in your conf.py:

extensions = ['recommonmark']
Warning

Markdown doesn’t support a lot of the features of Sphinx, like inline markup and directives. However, it works for basic prose content. reStructuredText is the preferred format for technical documentation, please read this blog post for motivation.
