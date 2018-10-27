
X-Obj
=====
| This is the main object which is associated with the one exported obj file.
  The scene must contain at least one that object.
| All the options in this object affects whole obj file i.e. the options are global for the obj file.


Shading
---------------------
- **Path prefix:** The textures can be in any folder relative the obj file, so you can specify that folder as prefix.
  *For example:* if you want to put your textures into the folder ``map/cabin`` near your obj file you 
  have to specify in this field the following text: ``map/cabin``.
- **Diffuse:** The diffuse texture of the object. 
  See `TEXTURE <http://developer.x-plane.com/?article=obj8-file-format-specification#TEXTURE_lttex_file_namegt>`_ in the obj specification. 
  The plug-in doesn't change the texture it only uses the texture’s name.
- **Lit:** The LIT texture of the object. 
  See `TEXTURE_LIT <https://developer.x-plane.com/?article=obj8-file-format-specification#TEXTURE_LIT_lttex_file_namegt>`_  in the obj specification. 
  The plug-in doesn't change the texture it only uses the texture’s name.
- **Normal:** The normal texture of the object. 
  See `TEXTURE_NORMAL <https://developer.x-plane.com/?article=obj8-file-format-specification#TEXTURE_NORMAL_lttex_file_namegt>`_ in the obj specification. 
  The plug-in doesn't change the texture it only uses the texture’s name.
- **Normal Metalness:** See ``NORMAL_METALNESS`` in the obj specification.
- **Blend Glass:** See ``BLEND_GLASS`` in the obj specification.
- **Blend:** See ``GLOBAL_no_blend`` and ``GLOBAL_shadow_blend`` and ``GLOBAL_specular`` in the obj specification.
- **Specular:** See ``GLOBAL_specular`` in the obj specification.
- **Tint:** See ``GLOBAL_tint`` in the obj specification.

Other attributes
---------------------
- **No shadow:** See `GLOBAL_no_shadow <http://developer.x-plane.com/?article=obj8-file-format-specification#GLOGAL_no_shadow>`_ in the obj specification.
- **Tilted:** See `TILTED <https://developer.x-plane.com/?article=obj8-file-format-specification#TILTED>`_ in the obj specification.
- **Slope limit:** See `SLOPE_LIMIT <https://developer.x-plane.com/?article=obj8-file-format-specification#SLOPE_LIMIT_ltmin_pitchgt_ltmax_pitchgt_ltmin_rollgt_ltmax_rollgt>`_ in the obj specification.
- **Slung load:** See `slung_load_weight <https://developer.x-plane.com/?article=obj8-file-format-specification#slung_load_weight_ltmass_weight_in_poundsgt>`_ in the obj specification.
- **Layer Group:** See `ATTR_layer_group <https://developer.x-plane.com/?article=obj8-file-format-specification#ATTR_layer_group_ltnamegt_ltoffsetgt>`_ in the obj specification.
- **LOD Draped:** See `ATTR_LOD_draped <https://developer.x-plane.com/?article=obj8-file-format-specification#ATTR_LOD_draped_ltmax_LODgt>`_ in the obj specification.
- **Layer Group Draped:** See `ATTR_layer_group_draped <https://developer.x-plane.com/?article=obj8-file-format-specification#ATTR_layer_group_draped_ltgroupgt_ltoffsetgt>`_ in the obj specification.
- **Wet/Dry:** See 
  `REQUIRE_WET <https://developer.x-plane.com/?article=obj8-file-format-specification#REQUIRE_WETREQUIRE_DRY>`_ 
  and `REQUIRE_DRY <https://developer.x-plane.com/?article=obj8-file-format-specification#REQUIRE_WETREQUIRE_DRY>`_ in the obj specification.
  
Cockpit
---------------------
- **Cockpit Lit:** See `GLOBAL_cockpit_lit <https://developer.x-plane.com/?article=obj8-file-format-specification#GLOBAL_cockpit_lit>`_ in the obj specification.
- **Cockpit regions:** See `COCKPIT_REGION <https://developer.x-plane.com/?article=obj8-file-format-specification#COCKPIT_REGION_ltleftgt_ltbottomgt_ltrightgt_lttopgt>`_ in the obj specification.
    
Obj Options
---------------------
These options are for the exporter itself.

- **Enable Meshes:** Enables meshes exporting.
- **Enable Lines:** Enables lines exporting.
- **Enable Lights:** Enables lights exporting.
- **Enable Animation:** Enables animation exporting.
- **Optimization:** Does some optimization to avoid losing the FPS. 

.. warning::
    This functional is not implemented yet.

- **Instancing:** Enables checking whether the object is instance friendly.
  The current algorithm does not check all the use cases but the X-Plane can check more ones.
  If the debug option is enabled the log file will contain a printout about your object.
  If the word ``complex`` is not present and the word ``additive`` is (or your object does not contain multiple LODs) then your object can be instanced.
  For more information about instancing read the X-Plane obj format specification.
- **Debug:** Prints the obj text in friendly form and prints ``DEBUG`` attribute in the obj file. 
- **Scale:** The scene scale. You can use the system units In the 3Ds Max as you wish but the X-Plane uses meters. 
  So you can set the scale which is needed for the transformation your scene size to the X-Plane’s scene size. 
  It doesn't work automatically yet. 
  For example: if you use centimeters then the scale must be 0.01. 
  Pay attention that the system units in the 3Ds Max aren't the same as the Display units.

Useful for the debug options:

.. code-block:: text

    TRIS 6 6 ## My mesh object name here
    LINES 6 6 ## My line object name here
    ## My light object name here
    LIGHT_NAMED
    ## My dummy object name here
        
- **Name Meshes:** Enables the mesh name printing near the ``TRIS``.
- **Name Lines:** Enables the lines name printing near the ``LINES``.
- **Name Lights:** Enables the light name printing near the ``LIGHT_XXX``.
- **Name Dummies:** Enables the dummies name printing.
- **Tree Hierarchy:**  Enables text line indent corresponding the tree hierarchy.
    
Display
---------------------
- **Scale:** The scale of icon it also depends on the system units.