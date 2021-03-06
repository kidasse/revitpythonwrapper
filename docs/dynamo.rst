.. revitpythonwrapper documentation master file, created by
   sphinx-quickstart on Mon Oct 31 13:57:34 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


===============
Dynamo
===============

The Revit Python Wrapper can easily be used within dynamo.
The package distributed through Dynamo's Package Manager
has everything you need to use it.

    1. Install the RevitPythonWrapper Dynamo Package
    2. Find the Package Directory, and open the Getting Started File in the `extra` folder

The package includes a Node that helps you find the location of the RPW library (see image below).
Once you have the location, just add it to your ``sys.path``, and you should be able to import the library.
You can always manually add the library path; the node is only included for convenience.

.. Note::
    Be sure the checkout the ``RPW_GetStarted.dyn`` file that is installed with the Package
    for practical examples.

    :file:`.../Dynamo/1.X/packages/RevitPythonWrapper/extra/RPW_GetStarted.dyn`

>>> rpw_path = IN[0] # Assumes output of RPW_GetFilePath node is plugged into IN[0]
>>> import sys
>>> sys.path.append(rpw_path)
>>> from rpw import doc, uidoc
>>> from rpw.collector import Collector

.. image:: _static/dynamo/package.png
.. image:: _static/dynamo/intro.png
