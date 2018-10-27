
X Base Attributes
====================
This options is only allowed for the mesh oriented geometric objects. *(Primitives, editable mesh, editable poly etc..)*

- **Tree:** It should be turned on for all trees. Checked state turns off the reaction on the sun light, so the trees looks better, as the native simulator’s ones. 
- **Two sided:** It replaces ``ATTR_no_cull`` which is deprecated. If it is checked the exporter will make the geometry copy at the same place and reverse its normals while exporting, it doesn't affect the 3Ds Max’s scene.
- **Draped:** See `ATTR_draped <http://developer.x-plane.com/?article=obj8-file-format-specification#ATTR_draped>`_ in the obj specification.
- **Shadow:** See `ATTR_shadow and ATTR_no_shadow <https://developer.x-plane.com/?article=obj8-file-format-specification>`_ in the obj specification.
- **Solid Camera:** See `ATTR_solid_camera and ATTR_no_solid_camera <https://developer.x-plane.com/?article=obj8-file-format-specification>`_ in the obj specification.
- **Draw:** See `ATTR_draw_enable and ATTR_draw_disable <https://developer.x-plane.com/?article=obj8-file-format-specification>`_ in the obj specification.
- **Shiny:** See `ATTR_shiny_rat <https://developer.x-plane.com/?article=obj8-file-format-specification#ATTR_shiny_rat_ltratiogt>`_ in the obj specification.
- **Cockpit:** See `ATTR_cockpit and ATTR_cockpit_region <https://developer.x-plane.com/?article=obj8-file-format-specification#ATTR_cockpit>`_ in the obj specification.
- **Hard:** See `ATTR_hard and ATTR_no_hard <https://developer.x-plane.com/?article=obj8-file-format-specification>`_ in the obj specification.
- **Blend:** See `ATTR_blend and ATTR_no_blend and ATTR_shadow_blend <https://developer.x-plane.com/?article=obj8-file-format-specification#ATTR_shadow_blend_ltratiogt>`_ in the obj specification.
- **Poly offset:** See `ATTR_poly_os <https://developer.x-plane.com/?article=obj8-file-format-specification#ATTR_poly_os_ltngt>`_ in the obj specification.
- **Light Level:** See `ATTR_light_level <https://developer.x-plane.com/?article=obj8-file-format-specification#ATTR_light_level_ltv1gt_ltv2gt_ltdatarefgt>`_ in the obj specification.

X Manipulator
-----------------
One object may have only one manipulator.
For more information about the manipulators see `manipulation commands <https://developer.x-plane.com/?article=obj8-file-format-specification#MANIPULATION_COMMANDS>`_ in the obj specification.