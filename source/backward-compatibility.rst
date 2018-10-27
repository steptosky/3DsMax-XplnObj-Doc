.. _bcw_version_2.2.0:


Backward Compatibility
====================================

.. note::
    - Old plug-in versions don’t support scenes which are made with newer ones.
    - if it is possible new plug-in versions support scenes which are made with the previous versions not older then 1.8.5.  
      If new version breaks backward compatibility you will be informed in this documentation and in the change log.

      
Version 2.4.0
-------------------------
| In this version bug with LODs' values was fixed. 

.. attention::
    This change may need your attention:
        - **Previous behavior:** If 3Ds Max's system units were different than meters the LOD's values were scaled in the obj file. https://github.com/steptosky/3DsMax-XplnObj/issues/10
        - **New behavior:** The LOD's values are printed into obj file exactly as they were set.


    
Version 2.2.0
-------------------------

| In this version the cockpit and manipulators state machine was changed. Previous behavior worked incorrectly.
  The plug-in will ask you to update your scene. The update will add the ``panel`` manipulator to all objects that 
  have ``cockpit`` or ``cockpit region`` attribute except the objects that have already another manipulator.
| After the update you have to check the affected objects manually because it isn't possible to do the correct
  updating programmatically in some cases, so if some objects don’t need the enabled ``panel`` manipulator just disable it. 

.. attention::  
    - **Previous behavior:** The ``panel`` manipulator was enabled implicitly with the ``cockpit`` or ``cockpit region`` attribute and was incorrectly disabled in some cases (it is the bug). 
      There was also incorrect interaction between ``cockpit/cockpit region`` and manipulators.

    - **New behavior:** The ``panel`` manipulator have to be enabled explicitly if you need it. The bugs were fixed.

