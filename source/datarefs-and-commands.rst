
DataRefs and Commands
========================

The plug-in provides a dialog for working with the X-Plane's DataRefs and Commands.
It can be opened with buttons ``DRF:`` and ``CMD:``.

X-Plane's 
-----------------

For using X-Plane's DataRefs and Commands you have to specify the X-Plane's folder with the plug-in's menu ``X-Plane -> Settings``
The files ``DataRefs.txt`` and ``Commands.txt`` from X-Plane's folder will be loaded into plug-in.

.. warning::
    Some 3Ds Max's version can't save last specified X-Plane's folder properly if it contains non ASCII characters.

Project's
-----------------

.. warning::
    It is still experimental feature! You can use it on your risk.

.. note::
    The plug-in's ``DataRef.txt`` reader ignores the first line. This is because the reader for X-Plane's DateRefs and Project's DataRef is the same and this format assumes that the first line just an information line.
    
| For using project's DataRefs and Commands you have to put files ``DataRefs.txt`` and ``Commands.txt`` in the same place where your 3Ds Max's scene file is saved. The format of those data files the same as X-Plane's ones, but it has an extension.
| The extended format contains unique ID for each DataRef or Command. The plug-in manages such DataRefs and Commands by their ID only! If ID isn't assigned then when you select a DataRef or Command for using the plug-in will auto-assign it and use that ID as the data key. If you want to see the real key associated with the ID you have to open dialog for working with DataRefs and Commands.
| In other words there is the association ``unique ID -> data key`` (DataRef/Command) and the plug-in uses ID in your 3Ds Max's scene. While exporting the ID will be replaced with the associated with it data (DataRef/Command).

| This extension allows you to change DataRefs and Commands outside your 3Ds Max scene in their ``.txt`` files.
| It helps for interaction between developer and 3D designer. 3D designer can create and use any key-name for DataRef or Command and when developers are ready to provide the correct keys they should only change project's DataRafs and Commands ``.txt`` files. Then those changes will be pulled into 3Ds Max's scene while it is loading and will be used while exporting. 
