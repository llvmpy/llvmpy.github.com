llvmpy is a Python wrapper around the `llvm <http://www.llvm.org>`_
C++ library which allows simple access to compiler tools.   It can be
used for a lot of things, but here are some ideas: 

- dynamically create LLVM IR for linking with LLVM IR produced by
  CLANG or dragonegg
- build machine code dynamically using LLVM execution engine
- use together with PLY or other tokenizer and parser to write a complete compiler in Python 

QuickStart
==========

Get at least version 3.1 of LLVM, build it. Make sure '--enable-pic' is passed
to LLVM's 'configure' command (also ensure you build the correct
version for your version of Python (32-bit or 64-bit).   Here is an
example.

.. code-block:: bash

   wget http://llvm.org/releases/3.1/llvm-3.1.src.tar.gz
   tar zxvf llvm-3.1.src.tar.gz
   cd llvm
   ./configure --enable-pic --mar
   make
   sudo make install

Get llvm-py and install it...

.. code-block:: bash

   git clone https://github.com/llvmpy/llvmpy.git
   cd llvmpy
   python setup.py install

This project is maintained by `Continuum Analytics <http://www.continuum.io>`_

.. toctree::
   :hidden:

   doc
   download
