.. title: hello
.. slug: hello
.. date: 2016-10-19 10:25:08 UTC+08:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text

- a

  - b

- c ::

    COMPILERS = {
        "rest": ('.rst', '.txt'),
        "markdown": ('.md', '.mdown', '.markdown'),
        "textile": ('.textile',),
        "txt2tags": ('.t2t',),
        "bbcode": ('.bb',),
        "wiki": ('.wiki',),
        "ipynb": ('.ipynb',),
        "html": ('.html', '.htm'),
        # PHP files are rendered the usual way (i.e. with the full templates).
        # The resulting files have .php extensions, making it possible to run
        # them without reconfiguring your server to recognize them.
        "php": ('.php',),
        # Pandoc detects the input from the source filename
        # but is disabled by default as it would conflict
        # with many of the others.
        # "pandoc": ('.rst', '.md', '.txt'),
    }

sdf