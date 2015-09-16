.. _docs_getting_started:

OSF Feature Docs
===============

Contributions to this documentation are welcome. Documentation is written in `reStructured Text`_ (rST). A quick rST reference can be found `here <http://docutils.sourceforge.net/docs/user/rst/quickref.html>`_. Builds are powered by Sphinx_ and are hosted by `ReadTheDocs <http://readthedocs.org>`_.

Fork, clone, install
********************

First, `fork the OSFDocs repo <https://github.com/jlcohoon/OSFDocs>`_, clone it, and install the requirements (requires Python 2.7 or 3.4 with pip):  ::

    # After forking jlcohoon/OSFDocs
    $ git clone https://github.com/<your_github_username>/OSFDocs.git
    $ cd OSFDocs
    $ pip install -r requirements.txt

Be sure to replace ``<your_github_username>`` with your Github username.

Build the docs
**************

To build docs: ::

    $ invoke docs -b

The ``-b`` (for "browse") automatically opens up the docs in your browser after building. Alternatively, you can open up the ``docs/_build/index.html`` file manually.

Autobuilding on File Changes
----------------------------

You can use ``sphinx-autobuild`` to automatically build the docs when you change a file in the ``docs`` directory.

To install ``sphinx-autobuild``: ::

    $ pip install sphinx-autobuild


You can now start the livereload server with: ::

    $ invoke watch

Point your browser to http://localhost:8000 to see your docs.

Send a PR!
**********

Once you are done making your edits, send a pull request on Github to the `OSFDocs <https://github.com/jlcohoon/OSFDocs>`_ repo.

.. _Sphinx: http://sphinx.pocoo.org/
.. _`reStructured Text`: http://docutils.sourceforge.net/rst.html


Style Conventions
******************

Use the following underlining conventions for heading levels:

- ``=`` for h1
- ``*`` for h2
- ``-`` for h3
- ``^`` for h4

Refer to the person doing the action as "the user." For example: "If the user clicks..." or "The user can upload..."

Separate all modal content by introducing it with a double colon. For example: "A modal opens that reads::"
Keep a line of space between the content and the introductory line and indent all content. Your text should be formatted like this::

    Woah, cool!

Refer to buttons by their title in quotes. For example: the "Upload" button.