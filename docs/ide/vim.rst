.. _ide_vim:

VIM
===

`VIM <http://www.vim.org/>`_ is an open-source, powerful and configurable text
editor. Vim is designed for use both from a command-line interface and as a
standalone application in a graphical user interface.

This software can be used with:

* all availalbe :ref:`platforms`
* all availalbe :ref:`frameworks`

Integration
-----------

Recommended bundles:

* Syntax highlight - `Arduino-syntax-file <https://github.com/vim-scripts/Arduino-syntax-file>`_
* Code Completion - `YouCompleteMe <https://github.com/Valloric/YouCompleteMe>`_ (see configuration example by **Anthony Ford** `PlatformIO/YouCompleteMe Integration <https://gist.github.com/ajford/f551b2b6fd4d6b6e1ef2>`_)
* Syntax checking - `Syntastic <https://github.com/scrooloose/syntastic>`_

Put to the project directory ``Makefile`` wrapper with contents:

.. code-block:: make

    # Uncomment lines below if you have problems with $PATH
    #SHELL := /bin/bash
    #PATH := /usr/local/bin:$(PATH)

    all:
        platformio run -t upload

    clean:
        platformio run -t clean


Now, in VIM ``cd /path/to/this/project`` and press ``Ctrl+B`` or ``Cmd+B``
(Mac). *PlatformIO* should compile your source code from the ``src`` directory,
make firmware and upload it.

Screenshot
----------

.. image:: ../_static/ide-platformio-vim.png
