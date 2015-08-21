.. warning:: This project has been deprecated and is no longer being actively developed.  We strongly suggest migrating to `llvmlite <http://llvmlite.pydata.org/>`_.

llvmpy is a Python wrapper around the `llvm <http://www.llvm.org>`_
C++ library which allows simple access to compiler tools.   It can be
used for a lot of things, but here are some ideas: 

- dynamically create LLVM IR for linking with LLVM IR produced by
  CLANG or dragonegg
- build machine code dynamically using LLVM execution engine
- use together with PLY or other tokenizer and parser to write a complete compiler in Python 

QuickStart
==========

1. Get and extract LLVM 3.3 (or LLVM 3.2) source tarball from
   `llvm.org <http://llvm.org/releases/download.html#3.3>`_.  Then, ``cd`` into
   the extracted directory.

2. Run ``./configure --enable-optimized --prefix=LLVM_INSTALL_PATH``.

    **Note**: Without the ``--enable-optimized`` flag, debug build will be
    selected.  Unless you are developing LLVM or llvmpy, it is recommended
    that the flag is used to reduce build time and binary size.
    
    **Note**: Use prefix to select the installation path.  It is recommended
    to separate your custom build from the default system package.  Please
    replace ``LLVM_INSTALL_PATH`` with your own path.

3. Run ``REQUIRES_RTTI=1 make`` to build.

    **Note**: With LLVM 3.2+, the default build configuration has C++ RTTI
    disabled.  However, llvmpy requires RTTI.

4. Get llvm-py and install it::

    $ git clone https://github.com/llvmpy/llvmpy.git
    $ cd llvmpy
    $ LLVM_CONFIG_PATH=LLVM_INSTALL_PATH/bin/llvm-config python setup.py install

   Run the tests::

    $ python -c "import llvm; llvm.test()"

5. See documentation at 'http://www.llvmpy.org' and examples
   under 'test'.


.. toctree::
   :hidden:

   doc
   download
