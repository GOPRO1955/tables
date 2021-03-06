Introduction
------------

Tables is a c++ library which allows arbitrary data to be stored as rows in a table with column headers.

Dependencies
------------
* We rely on functionality from the Boost C++ libraries, currently the
  tables build-tool will automatically download these dependencies.
* We are migrating to C++11 and currently use a few features, you therefore
  have to supply the appropiate C++11 compiler switch when using tables.

Platforms
---------
We have tested tables on various versions of Windows, Linux and Mac. You can
see the status by selecting the tables project on the Steinwurf `buildbot
page <http://176.28.49.184:12344/>`_:

Build
-----
We use the ``waf`` build-system to build the tables static library.
With some additional tools which may be found at external-waf_

.. _external-waf: https://github.com/steinwurf/external-waf

To build tables run the following command:
::
  ./waf configure --bundle=ALL --bundle-path=~/dev/bundle_dependencies
  ./waf build

Substitute the ``~/dev/bundle_dependencies`` with the path where you wish
waf to download tables's dependencies. You may omit this option then waf
will download the dependencies into the tables project folder.

You should now have the ``libtables.a`` static lib. It also build the boost
dependencies as static libs. In the tables directory type ``find . -name "*.a"``
to see the libraries produced. We need to use the path to the libraries when
using tables with our own applications as shown in the following.

License
-------
tables is available under the BSD license, see the LICENSE.rst file.
