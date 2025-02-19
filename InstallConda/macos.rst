===================
Installing on macOS
===================

#. Download the installer:

   * `Miniconda installer for macOS <https://conda.io/miniconda.html>`_.

   * `Anaconda installer for macOS <https://www.anaconda.com/download/>`_.

#. Install:

   * Miniconda---In your terminal window, run:

     .. code::

        bash Miniconda3-latest-MacOSX-x86_64.sh

   * Anaconda---Double-click the ``.pkg`` file.

#. Follow the prompts on the installer screens.

   If you are unsure about any setting, accept the defaults. You
   can change them later.

#. To make the changes take effect, close and then re-open your
   terminal window.


#. To test your installation, in your terminal window or Anaconda Prompt, run the command ``conda list``.

For a successful installation, a list of installed packages
appears.

.. _install-macos-silent:

Installing in silent mode
=========================

.. note::
   The following instructions are for Miniconda. For Anaconda,
   substitute ``Anaconda`` for ``Miniconda`` in all of the commands.

To run the :ref:`silent installation <silent-mode-glossary>` of
Miniconda for macOS or Linux, specify the -b and -p arguments of
the bash installer. The following arguments are supported:

* -b---Batch mode with no PATH modifications to ``~/.bashrc``.
  Assumes that you agree to the license agreement. Does not edit
  the ``.bashrc`` or ``.bash_profile`` files.
* -p---Installation prefix/path.
* -f---Force installation even if prefix -p already exists.

EXAMPLE:

.. code-block:: bash

    wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
    bash ~/miniconda.sh -b -p $HOME/miniconda
    export PATH="$HOME/miniconda/bin:$PATH"

.. note::
   This sets the PATH only for the current session, not
   permanently. Trying to use conda when conda is not in your
   PATH causes errors such as "command not found."

In each new bash session, before using conda, set the PATH and
run the activation scripts of your conda packages by running::

  source $HOME/miniconda/bin/activate

.. note::
   Replace ``$HOME/miniconda/bin/activate``
   with the path to the activate script in your conda installation.

To set the PATH permanently, you can add a line to your
``.bashrc`` file. However, this makes it possible to use conda
without running the activation scripts of your conda packages,
which may produce errors.

EXAMPLE::

  export PATH="$HOME/miniconda/bin:$PATH"


Updating Anaconda or Miniconda
==============================

#. Open a terminal window.

#. Navigate to the ``anaconda`` directory.

#. Run ``conda update conda``.


Uninstalling Anaconda or Miniconda
==================================

#. Open a terminal window.

#. Remove the entire Miniconda install directory with::

     rm -rf ~/miniconda

#. You may also:

#. OPTIONAL: Edit ``~/.bash_profile`` to remove the Miniconda
   directory from your PATH environment variable.

#. Remove the following hidden file and folders that may have
   been created in the home directory:

   * ``.condarc`` file
   * ``.conda`` directory
   * ``.continuum`` directory

   By running::

     rm -rf ~/.condarc ~/.conda ~/.continuum

