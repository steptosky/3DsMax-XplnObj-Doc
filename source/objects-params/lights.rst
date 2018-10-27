
X Light Attributes
====================
This options is only allowed for the light objects.


Named Light
----------------------------------------
| See `LIGHT_NAMED <https://developer.x-plane.com/?article=obj8-file-format-specification#LIGHT_NAMED_ltnamegt_ltxgt_ltygt_ltzgt>`_ in the obj specification.
| See `More about named light. <https://developer.x-plane.com/article/named-lights-for-scenery/>`_
| You can locate the master list of named lights in the file ``Resources/bitmaps/world/lites/lights.txt``. Do not edit this text file!



Param Light
----------------------------------------
| See `LIGHT_PARAM <https://developer.x-plane.com/?article=obj8-file-format-specification#LIGHT_PARAM_ltnamegt_ltxgt_ltygt_ltzgt_ltadditional_paramsgt>`_ in the obj specification.
| See `More about param light. <https://developer.x-plane.com/?article=airplane-parameterized-light-guide>`_ 
| You can locate the master list of named lights in the file ``Resources/bitmaps/world/lites/lights.txt``. Do not edit this text file! 

| Param light supports text variables, the following variables may be used: 

- ``$rgb`` Reads RGB color from the light. 
- ``$direction`` Reads target direction from the light. If the light is omni direction it will be ``0.0 0.0 0.0``. As the direction value also depends on the param light type the plug-in detects the type reading end of the light name ``_sp`` means light is spill.
- ``$width`` Reads ``falloff`` value of the 3Ds Max's spot light. This will be ``1.0`` if the light is omni.

| The ``$direction`` and ``$width`` values are transformed to the correct ones for the obj file depending on the param and 3Ds max lights types.
| Example:

- `airplane_strobe_sp` ``$rgb 0 1.0 $direction $width``. 
- `airplane_landing_core` ``$direction:a+10.0 0 1.0``.

| The ``$direction`` Also has addition parameters for the billboard light. As the 3Ds Max's spot light may have maximum cone angle 180 degrees but billboard light may have up to 360 you can use the following syntax to make cone angle greater:

- ``$direction:a+10`` where 10 is any value and this value will be added to the light cone angle. Assume your spot light has 90 degrees cone angle then cone for the billboard light will be ``90 + 10 = 100``.
- ``$direction:a-10`` the same as above but subtract the value ``90 - 10 = 80``.
- ``$direction:a120`` exactly set the cone angle ``120``



Custom Light
----------------------------------------
| See `LIGHT_CUSTOM <https://developer.x-plane.com/?article=obj8-file-format-specification#LIGHT_CUSTOM_ltxgt_ltygt_ltzgt_ltrgt_ltggt_ltbgt_ltagt_ltsgt_lts1gt_ltt1gt_lts2gt_ltt2gt_ltdatarefgt>`_ in the obj specification.
| See `More about custom light. <https://developer.x-plane.com/?article=custom-lights>`_



Spill Custom Light
----------------------------------------
| See `LIGHT_SPILL_CUSTOM <https://developer.x-plane.com/?article=obj8-file-format-specification#LIGHT_SPILL_CUSTOM_ltxgt_ltygt_ltzgt_ltrgt_ltggt_ltbgt_ltagt_ltsgt_ltdxgt_ltdygt_ltdzgt_ltsemigt_ltdrefgt>`_ in the obj specification.
| See `More about spill custom ight. <https://developer.x-plane.com/2013/04/customizing-spill-lights-two-ways/>`_
| You have to use 'Target Spot' light for this light type. The plug-in reads the Falloff/Field parameter and the target direction to calculate necessary values for the X-Plane.