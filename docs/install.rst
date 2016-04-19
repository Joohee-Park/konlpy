Installation
============

.. note::

    For troubleshooting information, see these pages:
    `Linux <https://github.com/konlpy/konlpy/issues?q=label%3Alinux>`_.
    `Mac OS <https://github.com/konlpy/konlpy/issues?q=label%3A"mac+os">`_.
    `Windows <https://github.com/konlpy/konlpy/issues?q=label%3Awindows>`_.
    Please record a `"New Issue" <https://github.com/konlpy/konlpy/issues/new>`_ if you have an error that is not listed.
    You can also see testing logs `here <https://docs.google.com/spreadsheets/d/1Ii_L9NF9gSLbsJOGqsf-zfqTtyhhthmJWNC2kgUDIsU/edit#gid=0>`_.


Ubuntu
------

1. Install dependencies

    .. sourcecode:: bash

        $ sudo apt-get install g++ openjdk-7-jdk python-dev python3-dev   # Install Java 1.7 or up
        $ pip install JPype1        # Python 2.x
        $ pip3 install JPype1-py3   # Python 3.x

2. Install KoNLPy

    .. sourcecode:: bash

        $ pip install konlpy        # Python 2.x
        $ pip3 install konlpy       # Python 3.x

3. Install MeCab (*optional*)

    .. sourcecode:: bash

        $ sudo apt-get install curl
        $ bash <(curl -s https://raw.githubusercontent.com/konlpy/konlpy/master/scripts/mecab.sh)


CentOS
------

1. Install dependencies

    .. sourcecode:: bash

        $ sudo yum install gcc-c++ java-1.7.0-openjdk-devel python-devel

        $ wget http://peak.telecommunity.com/dist/ez_setup.py               # Python 2.x
        $ sudo python ez_setup.py
        $ sudo easy_install pip

        $ wget https://www.python.org/ftp/python/3.4.3/Python-3.4.3.tar.xz  # Python 3.x
        $ tar xf Python-3.* 
        $ cd Python-3.*
        $ ./configure
        $ make # Build
        $ sudo make altinstall

        $ pip install JPype1        # Python 2.x
        $ pip3 install JPype1-py3   # Python 3.x

2. Install KoNLPy

    .. sourcecode:: bash

        $ pip install konlpy        # Python 2.x
        $ pip3.4 install konlpy     # Python 3.x

3. Install MeCab (*optional*)

    .. sourcecode:: bash

        $ sudo yum install curl
        $ bash <(curl -s https://raw.githubusercontent.com/konlpy/konlpy/master/scripts/mecab.sh)


Mac OS
------

1. Install dependencies

    .. sourcecode:: bash

       $ pip install JPype1         # Python 2.x
       $ pip3 install JPype1-py3    # Python 3.x

2. Install KoNLPy

    .. sourcecode:: bash

       $ pip install konlpy         # Python 2.x
       $ pip3 install konlpy        # Python 3.x

3. Install MeCab (*optional*)

    .. sourcecode:: bash

        $ bash <(curl -s https://raw.githubusercontent.com/konlpy/konlpy/master/scripts/mecab.sh)


Windows
-------

1. Does your Python installation's "bit version" match your Windows OS? If you're using a 64 bit Windows you need a 64 bit Python, and if you have a 32 bit Windows, you need a 32 bit Python. Reinstall your Python if your bit versions do not match.
    - How to check your Windows bit version

        .. image:: images/windows-bits.png
            :width: 600px

    - How to check your Python bit version

        .. image:: images/python-bits.png
            :width: 400px

2. Do you have a Java of version 1.7 or above installed, that matches your OS bit version? If not, `download and install a JDK <http://www.oracle.com/technetwork/java/javase/downloads/index.html>`_. Note again, that the bit versions must match.
3. Set `JAVA_HOME <http://docs.oracle.com/cd/E19182-01/820-7851/inst_cli_jdk_javahome_t/index.html>`_.
4. Download and install the `py4j`

    .. sourcecode:: guess

        > pip install --upgrade pip
        > pip install py4j

5. From the command prompt, install KoNLPy.

    .. sourcecode:: guess

        > pip install konlpy

.. warning::

    - KoNLPy's ``Mecab()`` class is not supported on Windows machines.
