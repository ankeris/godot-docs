:github_url: hide

.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the RayCast.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_RayCast:

RayCast
=======

**Inherits:** :ref:`Spatial<class_Spatial>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

**Category:** Core

Brief Description
-----------------

Query the closest object intersecting a ray.

Properties
----------

+-------------------------------+------------------------------------------------------------------------+---------------------+
| :ref:`Vector3<class_Vector3>` | :ref:`cast_to<class_RayCast_property_cast_to>`                         | Vector3( 0, -1, 0 ) |
+-------------------------------+------------------------------------------------------------------------+---------------------+
| :ref:`bool<class_bool>`       | :ref:`collide_with_areas<class_RayCast_property_collide_with_areas>`   | false               |
+-------------------------------+------------------------------------------------------------------------+---------------------+
| :ref:`bool<class_bool>`       | :ref:`collide_with_bodies<class_RayCast_property_collide_with_bodies>` | true                |
+-------------------------------+------------------------------------------------------------------------+---------------------+
| :ref:`int<class_int>`         | :ref:`collision_mask<class_RayCast_property_collision_mask>`           | 1                   |
+-------------------------------+------------------------------------------------------------------------+---------------------+
| :ref:`bool<class_bool>`       | :ref:`enabled<class_RayCast_property_enabled>`                         | false               |
+-------------------------------+------------------------------------------------------------------------+---------------------+
| :ref:`bool<class_bool>`       | :ref:`exclude_parent<class_RayCast_property_exclude_parent>`           | true                |
+-------------------------------+------------------------------------------------------------------------+---------------------+

Methods
-------

+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`add_exception<class_RayCast_method_add_exception>` **(** :ref:`Object<class_Object>` node **)**                                           |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`add_exception_rid<class_RayCast_method_add_exception_rid>` **(** :ref:`RID<class_RID>` rid **)**                                          |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`clear_exceptions<class_RayCast_method_clear_exceptions>` **(** **)**                                                                      |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`force_raycast_update<class_RayCast_method_force_raycast_update>` **(** **)**                                                              |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Object<class_Object>`   | :ref:`get_collider<class_RayCast_method_get_collider>` **(** **)** const                                                                        |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`         | :ref:`get_collider_shape<class_RayCast_method_get_collider_shape>` **(** **)** const                                                            |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`       | :ref:`get_collision_mask_bit<class_RayCast_method_get_collision_mask_bit>` **(** :ref:`int<class_int>` bit **)** const                          |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>` | :ref:`get_collision_normal<class_RayCast_method_get_collision_normal>` **(** **)** const                                                        |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_Vector3>` | :ref:`get_collision_point<class_RayCast_method_get_collision_point>` **(** **)** const                                                          |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`       | :ref:`is_colliding<class_RayCast_method_is_colliding>` **(** **)** const                                                                        |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`remove_exception<class_RayCast_method_remove_exception>` **(** :ref:`Object<class_Object>` node **)**                                     |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`remove_exception_rid<class_RayCast_method_remove_exception_rid>` **(** :ref:`RID<class_RID>` rid **)**                                    |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+
| void                          | :ref:`set_collision_mask_bit<class_RayCast_method_set_collision_mask_bit>` **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)** |
+-------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------+

Description
-----------

A RayCast represents a line from its origin to its destination position, ``cast_to``. It is used to query the 3D space in order to find the closest object along the path of the ray.

RayCast can ignore some objects by adding them to the exception list via ``add_exception`` or by setting proper filtering with collision layers and masks.

RayCast can be configured to report collisions with :ref:`Area<class_Area>`\ s (:ref:`collide_with_areas<class_RayCast_property_collide_with_areas>`) and/or :ref:`PhysicsBody<class_PhysicsBody>`\ s (:ref:`collide_with_bodies<class_RayCast_property_collide_with_bodies>`).

Only enabled raycasts will be able to query the space and report collisions.

RayCast calculates intersection every physics frame (see :ref:`Node<class_Node>`), and the result is cached so it can be used later until the next frame. If multiple queries are required between physics frames (or during the same frame), use :ref:`force_raycast_update<class_RayCast_method_force_raycast_update>` after adjusting the raycast.

Property Descriptions
---------------------

.. _class_RayCast_property_cast_to:

- :ref:`Vector3<class_Vector3>` **cast_to**

+-----------+---------------------+
| *Default* | Vector3( 0, -1, 0 ) |
+-----------+---------------------+
| *Setter*  | set_cast_to(value)  |
+-----------+---------------------+
| *Getter*  | get_cast_to()       |
+-----------+---------------------+

The ray's destination point, relative to the RayCast's ``position``.

----

.. _class_RayCast_property_collide_with_areas:

- :ref:`bool<class_bool>` **collide_with_areas**

+-----------+---------------------------------+
| *Default* | false                           |
+-----------+---------------------------------+
| *Setter*  | set_collide_with_areas(value)   |
+-----------+---------------------------------+
| *Getter*  | is_collide_with_areas_enabled() |
+-----------+---------------------------------+

If ``true``, collision with :ref:`Area<class_Area>`\ s will be reported.

----

.. _class_RayCast_property_collide_with_bodies:

- :ref:`bool<class_bool>` **collide_with_bodies**

+-----------+----------------------------------+
| *Default* | true                             |
+-----------+----------------------------------+
| *Setter*  | set_collide_with_bodies(value)   |
+-----------+----------------------------------+
| *Getter*  | is_collide_with_bodies_enabled() |
+-----------+----------------------------------+

If ``true``, collision with :ref:`PhysicsBody<class_PhysicsBody>`\ s will be reported.

----

.. _class_RayCast_property_collision_mask:

- :ref:`int<class_int>` **collision_mask**

+-----------+---------------------------+
| *Default* | 1                         |
+-----------+---------------------------+
| *Setter*  | set_collision_mask(value) |
+-----------+---------------------------+
| *Getter*  | get_collision_mask()      |
+-----------+---------------------------+

The ray's collision mask. Only objects in at least one collision layer enabled in the mask will be detected.

----

.. _class_RayCast_property_enabled:

- :ref:`bool<class_bool>` **enabled**

+-----------+--------------------+
| *Default* | false              |
+-----------+--------------------+
| *Setter*  | set_enabled(value) |
+-----------+--------------------+
| *Getter*  | is_enabled()       |
+-----------+--------------------+

If ``true``, collisions will be reported.

----

.. _class_RayCast_property_exclude_parent:

- :ref:`bool<class_bool>` **exclude_parent**

+-----------+--------------------------------+
| *Default* | true                           |
+-----------+--------------------------------+
| *Setter*  | set_exclude_parent_body(value) |
+-----------+--------------------------------+
| *Getter*  | get_exclude_parent_body()      |
+-----------+--------------------------------+

If ``true``, collisions will be ignored for this RayCast's immediate parent.

Method Descriptions
-------------------

.. _class_RayCast_method_add_exception:

- void **add_exception** **(** :ref:`Object<class_Object>` node **)**

Adds a collision exception so the ray does not report collisions with the specified node.

----

.. _class_RayCast_method_add_exception_rid:

- void **add_exception_rid** **(** :ref:`RID<class_RID>` rid **)**

Adds a collision exception so the ray does not report collisions with the specified :ref:`RID<class_RID>`.

----

.. _class_RayCast_method_clear_exceptions:

- void **clear_exceptions** **(** **)**

Removes all collision exceptions for this ray.

----

.. _class_RayCast_method_force_raycast_update:

- void **force_raycast_update** **(** **)**

Updates the collision information for the ray.

Use this method to update the collision information immediately instead of waiting for the next ``_physics_process`` call, for example if the ray or its parent has changed state.

**Note:** ``enabled == true`` is not required for this to work.

----

.. _class_RayCast_method_get_collider:

- :ref:`Object<class_Object>` **get_collider** **(** **)** const

Returns the first object that the ray intersects, or ``null`` if no object is intersecting the ray (i.e. :ref:`is_colliding<class_RayCast_method_is_colliding>` returns ``false``).

----

.. _class_RayCast_method_get_collider_shape:

- :ref:`int<class_int>` **get_collider_shape** **(** **)** const

Returns the shape ID of the first object that the ray intersects, or ``0`` if no object is intersecting the ray (i.e. :ref:`is_colliding<class_RayCast_method_is_colliding>` returns ``false``).

----

.. _class_RayCast_method_get_collision_mask_bit:

- :ref:`bool<class_bool>` **get_collision_mask_bit** **(** :ref:`int<class_int>` bit **)** const

Returns ``true`` if the bit index passed is turned on.

**Note:** Bit indices range from 0-19.

----

.. _class_RayCast_method_get_collision_normal:

- :ref:`Vector3<class_Vector3>` **get_collision_normal** **(** **)** const

Returns the normal of the intersecting object's shape at the collision point.

----

.. _class_RayCast_method_get_collision_point:

- :ref:`Vector3<class_Vector3>` **get_collision_point** **(** **)** const

Returns the collision point at which the ray intersects the closest object.

**Note:** This point is in the **global** coordinate system.

----

.. _class_RayCast_method_is_colliding:

- :ref:`bool<class_bool>` **is_colliding** **(** **)** const

Returns whether any object is intersecting with the ray's vector (considering the vector length).

----

.. _class_RayCast_method_remove_exception:

- void **remove_exception** **(** :ref:`Object<class_Object>` node **)**

Removes a collision exception so the ray does report collisions with the specified node.

----

.. _class_RayCast_method_remove_exception_rid:

- void **remove_exception_rid** **(** :ref:`RID<class_RID>` rid **)**

Removes a collision exception so the ray does report collisions with the specified :ref:`RID<class_RID>`.

----

.. _class_RayCast_method_set_collision_mask_bit:

- void **set_collision_mask_bit** **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)**

Sets the bit index passed to the ``value`` passed.

**Note:** Bit indexes range from 0-19.

