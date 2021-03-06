.. _troubleshooting-faq:

***************
Troubleshooting
***************

.. contents::
   :backlinks: none

.. _sunpy-version:

Obtaining sunpy version
============================

To find out your sunpy version number, import it and print the
``__version__`` attribute::

    import sunpy
    sunpy.__version__

.. _locating-sunpy-install:

System Info
===========

To quickly collect information on your system, you can use our convienience function
``system_info`` which you can run through: ::

    import sunpy
    sunpy.util.system_info()

The output should look something like: ::

    ==========================================================
     SunPy Installation Information
    
     Sunday, 18. November 2012 11:06PM UT
    ==========================================================
    
    ###########
     General
    ###########
    OS: Mac OS X 10.8.2 (i386)
    Python: 2.7.3 (64bit)
    
    ####################
     Required libraries
    ####################
    SunPy: 0.1
    NumPy: 1.6.2
    SciPy: 0.10.1
    Matplotlib: 1.2.x
    PyFITS: 3.0.8
    pandas: 0.8.1
    
    #######################
     Recommended libraries
    #######################
    beautifulsoup4: 4.1.1
    PIL: NOT INSTALLED
    PyQt: 4.9.4
    SUDS: 0.4'

This information is especially useful if you are running into a bug and need help.

:file:`sunpy` install location
===================================

You can find what directory sunpy is installed in by importing it
and printing the ``__file__`` attribute::

    import sunpy
    sunpy.__file__
 
.. _locating-matplotlib-config-dir:

:file:`.sunpy` directory location
======================================

Each user should have a :file:`.sunpy/` directory which should contain a
:ref:`sunpyrc <customizing-with-sunpyrc-files>` file. To locate your :file:`.sunpy/`
directory, use :func:`sunpy.print_config`::

    import sunpy as sun
    sun.print_config()

The output should look something like: ::

    FILES USED:
        sunpy/data/sunpyrc

    CONFIGURATION:
    [general]
    working_dir = /Users/schriste/sunpy

    [downloads]
    download_dir = /Users/schriste/sunpy/data

On unix-like systems, this directory is generally located in your
:envvar:`HOME` directory.  On windows, it is in your documents and
settings directory by default.

If you would like to use a different configuration directory, you can
do so by specifying the location in your :envvar:`SUNPY_CONFIGDIR`
environment variable.

.. _reporting-problems:

Report a problem
================

If you are having a problem with sunpy, search the mailing
lists first: it is possible that someone else has already run into
your problem.

If not, please provide the following information in your e-mail to the
`mailing list <http://groups.google.com/forum/#!forum/sunpy>`_:

  * your operating system; (Linux/UNIX users: post the output of ``uname -a``)

  * sunpy version::

        import sunpy
        sunpy.util.system_info()

  * how you obtained sunpy.

  * any customizations to your ``sunpyrc`` file (see
    :ref:`customizing-sunpy`).

  * Please try to provide a *minimal*,
    standalone Python script that demonstrates the problem.  This is
    *the* critical step.  If you can't post a piece of code that we
    can run and reproduce your error, the chances of getting help are
    significantly diminished.  Very often, the mere act of trying to
    minimize your code to the smallest bit that produces the error
    will help you find a bug in *your* code that is causing the
    problem.

You will likely get a faster response writing to the mailing list than
filing a bug in the `bug tracker <http://github.com/sunpy/sunpy/issues>`_.  
If your problem has been determined to be a bug and can not be quickly solved, the issues 
may be filed a bug in the tracker so the issue doesn't get lost.