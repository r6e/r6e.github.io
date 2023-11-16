---
layout: default
title: "Print"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: Print
---

Configuration options for a configuration file with `"type": "process"`.

## Enable accel_to_decel

Klipper's max_accel_to_decel will be adjusted automatically

**Key:** `accel_to_decel_enable`

**Type:** `Bool`

**Default** `true`

### Example

```json
"accel_to_decel_enable": true
```


## accel_to_decel

Klipper's max_accel_to_decel will be adjusted to this %% of acceleration

**Key:** `accel_to_decel_factor`

**Type:** `Percent`

**Min:** `1`

**Max:** `100`

**Default** `50`

### Example

```json
"accel_to_decel_factor": "44%"
```


## Adaptive layer height [deprecated]

Enabling this option means the height of every layer except the first will be automatically calculated during slicing according to the slope of the model's surface.
Note that this option only takes effect if no prime tower is generated in current plate.

**Key:** `adaptive_layer_height`

**Type:** `Bool`

**Default** `false`

### Example

```json
"adaptive_layer_height": false
```


## Bottom shell layers

This is the number of solid layers of bottom shell, including the bottom surface layer. When the thickness calculated by this value is thinner than bottom shell thickness, the bottom shell layers will be increased

**Key:** `bottom_shell_layers`

**Type:** `Int`

**Min:** `0`

**Default** `3`

### Example

```json
"bottom_shell_layers": 3
```


## Bottom shell thickness

The number of bottom solid layers is increased when slicing if the thickness calculated by bottom shell layers is thinner than this value. This can avoid having too thin shell when layer height is small. 0 means that this setting is disabled and thickness of bottom shell is absolutely determained by bottom shell layers

**Key:** `bottom_shell_thickness`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"bottom_shell_thickness": 3.78
```


## Bottom surface flow ratio

This factor affects the amount of material for bottom solid infill

**Key:** `bottom_solid_infill_flow_ratio`

**Type:** `Float`

**Min:** `0`

**Max:** `2`

**Default** `1`

### Example

```json
"bottom_solid_infill_flow_ratio": 1.23
```


## Bottom surface pattern

Line pattern of bottom surface infill, not bridge infill

**Key:** `bottom_surface_pattern`

**Type:** `Enum`

**Default** `Monotonic`

**Enum values:**


### Example

```json
"bottom_surface_pattern": "monotonic"
```


## Acceleration (bridge)

Acceleration of bridges. If the value is expressed as a percentage (e.g. 50%), it will be calculated based on the outer wall acceleration.

**Key:** `bridge_acceleration`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `50%`

### Example

```json
"bridge_acceleration": "52%"
```


## Bridge infill direction

Bridging angle override. If left to zero, the bridging angle will be calculated automatically. Otherwise the provided angle will be used for external bridges. Use 180°for zero angle.

**Key:** `bridge_angle`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"bridge_angle": 4.51
```


## Bridge density

Density of external bridges. 100% means solid bridge. Default is 100%.

**Key:** `bridge_density`

**Type:** `Percent`

**Min:** `10`

**Max:** `100`

**Default** `100`

### Example

```json
"bridge_density": "93%"
```


## Bridge flow

Decrease this value slightly(for example 0.9) to reduce the amount of material for bridge, to improve sag

**Key:** `bridge_flow`

**Type:** `Float`

**Min:** `0`

**Max:** `2`

**Default** `1`

### Example

```json
"bridge_flow": 1.03
```


## Don't support bridges

Don't support the whole bridge area which make support very large. Bridge usually can be printing directly without support if not very long

**Key:** `bridge_no_support`

**Type:** `Bool`

**Default** `false`

### Example

```json
"bridge_no_support": false
```


## Speed (outer bridge)

Speed of bridge and completely overhang wall

**Key:** `bridge_speed`

**Type:** `Float`

**Min:** `1`

**Default** `25`

### Example

```json
"bridge_speed": 19.89
```


## Brim ear detection radius

The geometry will be decimated before dectecting sharp angles. This parameter indicates the minimum length of the deviation for the decimation.\n0 to deactivate

**Key:** `brim_ears_detection_length`

**Type:** `Float`

**Min:** `0`

**Default** `1`

### Example

```json
"brim_ears_detection_length": 1.09
```


## Brim ear max angle

Maximum angle to let a brim ear appear. \nIf set to 0, no brim will be created. \nIf set to ~180, brim will be created on everything but straight sections.

**Key:** `brim_ears_max_angle`

**Type:** `Float`

**Min:** `0`

**Max:** `180`

**Default** `125`

### Example

```json
"brim_ears_max_angle": 119.11
```


## Brim-object gap

A gap between innermost brim line and object can make brim be removed more easily

**Key:** `brim_object_gap`

**Type:** `Float`

**Min:** `0`

**Max:** `2`

**Default** `0.0`

### Example

```json
"brim_object_gap": 0
```


## Brim type

This controls the generation of the brim at outer and/or inner side of models. Auto means the brim width is analysed and calculated automatically.

**Key:** `brim_type`

**Type:** `Enum`

**Default** `AutoBrim`

**Enum values:**


### Example

```json
"brim_type": "outer_and_inner"
```


## Brim width

Distance from model to the outermost brim line

**Key:** `brim_width`

**Type:** `Float`

**Min:** `0`

**Max:** `100`

**Default** `0.0`

### Example

```json
"brim_width": 4.68
```


## Acceleration (default)

The default acceleration of both normal printing and travel except initial layer

**Key:** `default_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `500.0`

### Example

```json
"default_acceleration": 462.64
```


## Jerk (default)

Default jerk

**Key:** `default_jerk`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"default_jerk": 0.36
```


## Detect overhang wall

Detect the overhang percentage relative to line width and use different speed to print. For 100%% overhang, bridge speed is used.

**Key:** `detect_overhang_wall`

**Type:** `Bool`

**Default** `true`

### Example

```json
"detect_overhang_wall": true
```


## Detect thin wall

Detect thin wall which can't contain two line width. And use single line to print. Maybe printed not very well, because it's not closed loop

**Key:** `detect_thin_wall`

**Type:** `Bool`

**Default** `false`

### Example

```json
"detect_thin_wall": false
```


## Draft shield

With draft shield active, the skirt will be printed skirt_distance from the object, possibly intersecting brim.
Enabled = skirt is as tall as the highest printed object.
Limited = skirt is as tall as specified by skirt_height.
This is useful to protect an ABS or ASA print from warping and detaching from print bed due to wind draft.

**Key:** `draft_shield`

**Type:** `Enum`

**Default** `Disabled`

**Enum values:**


### Example

```json
"draft_shield": "enabled"
```


## Elephant foot compensation layers

The number of layers on which the elephant foot compensation will be active. The first layer will be shrunk by the elephant foot compensation value, then the next layers will be linearly shrunk less, up to the layer indicated by this value.

**Key:** `elefant_foot_compensation_layers`

**Type:** `Int`

**Min:** `1`

**Default** `1`

### Example

```json
"elefant_foot_compensation_layers": 1
```


## Arc fitting

Enable this to get a G-code file which has G2 and G3 moves. And the fitting tolerance is same with resolution

**Key:** `enable_arc_fitting`

**Type:** `Bool`

**Default** `false`

### Example

```json
"enable_arc_fitting": true
```


## Speed (overhang)

Enable this option to slow printing down for different overhang degree

**Key:** `enable_overhang_speed`

**Type:** `Bool`

**Default** `true`

### Example

```json
"enable_overhang_speed": true
```


## Enable prime tower

The wiping tower can be used to clean up the residue on the nozzle and stabilize the chamber pressure inside the nozzle, in order to avoid appearance defects when printing objects.

**Key:** `enable_prime_tower`

**Type:** `Bool`

**Default** `false`

### Example

```json
"enable_prime_tower": false
```


## Enable support

Enable support generation.

**Key:** `enable_support`

**Type:** `Bool`

**Default** `false`

### Example

```json
"enable_support": true
```


## Enforce support for the first

Generate support material for the specified number of layers counting from bottom, regardless of whether normal support material is enabled or not and regardless of any angle threshold. This is useful for getting more adhesion of objects

**Key:** `enforce_support_layers`

**Type:** `Int`

**Min:** `0`

**Max:** `5000`

**Default** `0`

### Example

```json
"enforce_support_layers": 3
```


## Exclude objects

Enable this option to add EXCLUDE OBJECT command in g-code

**Key:** `exclude_object`

**Type:** `Bool`

**Default** `true`

### Example

```json
"exclude_object": true
```


## Extra perimeters on overhangs

Create additional perimeter paths over steep overhangs and areas where bridges cannot be anchored.

**Key:** `extra_perimeters_on_overhangs`

**Type:** `Bool`

**Default** `false`

### Example

```json
"extra_perimeters_on_overhangs": true
```


## Filter out tiny gaps

Filter out gaps smaller than the threshold specified

**Key:** `filter_out_gap_fill`

**Type:** `Float`

**Default** `0`

### Example

```json
"filter_out_gap_fill": 2.69
```


## Flush into objects' infill

Purging after filament change will be done inside objects' infills. This may lower the amount of waste and decrease the print time. If the walls are printed with transparent filament, the mixed color infill will be seen outside. It will not take effect, unless the prime tower is enabled.

**Key:** `flush_into_infill`

**Type:** `Bool`

**Default** `false`

### Example

```json
"flush_into_infill": true
```


## Flush into this object

This object will be used to purge the nozzle after a filament change to save filament and decrease the print time. Colours of the objects will be mixed as a result. It will not take effect, unless the prime tower is enabled.

**Key:** `flush_into_objects`

**Type:** `Bool`

**Default** `false`

### Example

```json
"flush_into_objects": true
```


## Flush into objects' support

Purging after filament change will be done inside objects' support. This may lower the amount of waste and decrease the print time. It will not take effect, unless the prime tower is enabled.

**Key:** `flush_into_support`

**Type:** `Bool`

**Default** `true`

### Example

```json
"flush_into_support": true
```


## Fuzzy Skin

Randomly jitter while printing the wall, so that the surface has a rough look. This setting controls the fuzzy position

**Key:** `fuzzy_skin`

**Type:** `Enum`

**Default** `None`

**Enum values:**


### Example

```json
"fuzzy_skin": "all"
```


## Fuzzy skin point distance

The average diatance between the random points introducded on each line segment

**Key:** `fuzzy_skin_point_distance`

**Type:** `Float`

**Min:** `0`

**Max:** `5`

**Default** `0.8`

### Example

```json
"fuzzy_skin_point_distance": 0.96
```


## Fuzzy skin thickness

The width within which to jitter. It's adversed to be below outer wall line width

**Key:** `fuzzy_skin_thickness`

**Type:** `Float`

**Min:** `0`

**Max:** `1`

**Default** `0.3`

### Example

```json
"fuzzy_skin_thickness": 0.26
```


## Speed (gap infill)

Speed of gap infill. Gap usually has irregular line width and should be printed more slowly

**Key:** `gap_infill_speed`

**Type:** `Float`

**Min:** `1`

**Default** `30`

### Example

```json
"gap_infill_speed": 29.69
```


## Add line number

Enable this to add line number(Nx) at the beginning of each G-Code line

**Key:** `gcode_add_line_number`

**Type:** `Bool`

**Default** `false`

### Example

```json
"gcode_add_line_number": false
```


## Verbose G-code

Enable this to get a commented G-code file, with each line explained by a descriptive text. If you print from SD card, the additional weight of the file could make your firmware slow down.

**Key:** `gcode_comments`

**Type:** `Bool`

**Default** `false`

### Example

```json
"gcode_comments": true
```


## Label objects

Enable this to add comments into the G-Code labeling print moves with what object they belong to, which is useful for the Octoprint CancelObject plugin. This settings is NOT compatible with Single Extruder Multi Material setup and Wipe into Object / Wipe into Infill.

**Key:** `gcode_label_objects`

**Type:** `Bool`

**Default** `true`

### Example

```json
"gcode_label_objects": true
```


## Convert holes to polyholes

Search for almost-circular holes that span more than one layer and convert the geometry to polyholes. Use the nozzle size and the (biggest) diameter to compute the polyhole.\nSee http://hydraraptor.blogspot.com/2011/02/polyholes.html

**Key:** `hole_to_polyhole`

**Type:** `Bool`

**Default** `false`

### Example

```json
"hole_to_polyhole": false
```


## Polyhole detection margin

Maximum defection of a point to the estimated radius of the circle.\nAs cylinders are often exported as triangles of varying size, points may not be on the circle circumference. This setting allows you some leway to broaden the detection.\nIn mm or in % of the radius.

**Key:** `hole_to_polyhole_threshold`

**Type:** `FloatOrPercent`

**Default** `0.01`

### Example

```json
"hole_to_polyhole_threshold": 0.01
```


## Polyhole twist

Rotate the polyhole every layer.

**Key:** `hole_to_polyhole_twisted`

**Type:** `Bool`

**Default** `true`

### Example

```json
"hole_to_polyhole_twisted": true
```


## Independent support layer height

Support layer uses layer height independent with object layer. This is to support customizing z-gap and save print time.This option will be invalid when the prime tower is enabled.

**Key:** `independent_support_layer_height`

**Type:** `Bool`

**Default** `true`

### Example

```json
"independent_support_layer_height": true
```


## Sparse infill anchor length

Connect an infill line to an internal perimeter with a short segment of an additional perimeter. If expressed as percentage (example: 15%) it is calculated over infill extrusion width. Slic3r tries to connect two close infill lines to a short perimeter segment. If no such perimeter segment shorter than infill_anchor_max is found, the infill line is connected to a perimeter segment at just one side and the length of the perimeter segment taken is limited to this parameter, but no longer than anchor_length_max. \nSet this parameter to zero to disable anchoring perimeters connected to a single infill line.

**Key:** `infill_anchor`

**Type:** `FloatOrPercent`

**Default** `400%`

**Enum values:**


### Example

```json
"infill_anchor": "332%"
```


## Maximum length of the infill anchor

Connect an infill line to an internal perimeter with a short segment of an additional perimeter. If expressed as percentage (example: 15%) it is calculated over infill extrusion width. Slic3r tries to connect two close infill lines to a short perimeter segment. If no such perimeter segment shorter than this parameter is found, the infill line is connected to a perimeter segment at just one side and the length of the perimeter segment taken is limited to infill_anchor, but no longer than this parameter. 
If set to 0, the old algorithm for infill connection will be used, it should create the same result as with 1000 & 0.

**Key:** `infill_anchor_max`

**Type:** `FloatOrPercent`

**Default** `20.0`

**Enum values:**


### Example

```json
"infill_anchor_max": "23%"
```


## Infill combination

Automatically Combine sparse infill of several layers to print together to reduce time. Wall is still printed with original layer height.

**Key:** `infill_combination`

**Type:** `Bool`

**Default** `false`

### Example

```json
"infill_combination": false
```


## Infill direction

Angle for sparse infill pattern, which controls the start or main direction of line

**Key:** `infill_direction`

**Type:** `Float`

**Min:** `0`

**Max:** `360`

**Default** `45`

### Example

```json
"infill_direction": 52.29
```


## Jerk (infill)

Jerk for infill

**Key:** `infill_jerk`

**Type:** `Float`

**Min:** `1`

**Default** `9`

### Example

```json
"infill_jerk": 9.59
```


## Infill/Wall overlap

Infill area is enlarged slightly to overlap with wall for better bonding. The percentage value is relative to line width of sparse infill

**Key:** `infill_wall_overlap`

**Type:** `Percent`

**Default** `15`

### Example

```json
"infill_wall_overlap": "18%"
```


## Acceleration (initial layer)

Acceleration of initial layer. Using a lower value can improve build plate adhesive

**Key:** `initial_layer_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `300`

### Example

```json
"initial_layer_acceleration": 368.86
```


## Infill speed (initial layer)

Speed of solid infill part of initial layer

**Key:** `initial_layer_infill_speed`

**Type:** `Float`

**Min:** `1`

**Default** `60.0`

### Example

```json
"initial_layer_infill_speed": 63.44
```


## Jerk (initial layer)

Jerk for initial layer

**Key:** `initial_layer_jerk`

**Type:** `Float`

**Min:** `1`

**Default** `9`

### Example

```json
"initial_layer_jerk": 8.63
```


## Line width (initial layer)

Line width of initial layer. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `initial_layer_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"initial_layer_line_width": "2%"
```


## First layer minimum wall width

The minimum wall width that should be used for the first layer is recommended to be set to the same size as the nozzle. This adjustment is expected to enhance adhesion.

**Key:** `initial_layer_min_bead_width`

**Type:** `Percent`

**Min:** `0`

**Default** `85`

### Example

```json
"initial_layer_min_bead_width": "77%"
```


## Layer height (initial layer)

Height of initial layer. Making initial layer height to be thick slightly can improve build plate adhension

**Key:** `initial_layer_print_height`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"initial_layer_print_height": 0.23
```


## Speed (initial layer)

Speed of initial layer except the solid infill part

**Key:** `initial_layer_speed`

**Type:** `Float`

**Min:** `1`

**Default** `30`

### Example

```json
"initial_layer_speed": 26.21
```


## Travel speed (initial layer)

Travel speed of initial layer

**Key:** `initial_layer_travel_speed`

**Type:** `FloatOrPercent`

**Min:** `1`

**Default** `100%`

### Example

```json
"initial_layer_travel_speed": "105%"
```


## Acceleration (inner walls)

Acceleration of inner walls

**Key:** `inner_wall_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `10000`

### Example

```json
"inner_wall_acceleration": 11924.71
```


## Jerk (inner wall)

Jerk of inner walls

**Key:** `inner_wall_jerk`

**Type:** `Float`

**Min:** `0`

**Default** `9`

### Example

```json
"inner_wall_jerk": 9.66
```


## Inner wall

Line width of inner wall. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `inner_wall_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"inner_wall_line_width": 0.35
```


## Speed (inner wall)

Speed of inner wall

**Key:** `inner_wall_speed`

**Type:** `Float`

**Min:** `1`

**Default** `60`

### Example

```json
"inner_wall_speed": 61.46
```


## Interface shells

Force the generation of solid shells between adjacent materials/volumes. Useful for multi-extruder prints with translucent materials or manual soluble support material

**Key:** `interface_shells`

**Type:** `Bool`

**Default** `false`

### Example

```json
"interface_shells": true
```


## Speed (inner bridge)

Speed of internal bridge. If the value is expressed as a percentage, it will be calculated based on the bridge_speed. Default value is 150%.

**Key:** `internal_bridge_speed`

**Type:** `FloatOrPercent`

**Min:** `1`

**Default** `150%`

### Example

```json
"internal_bridge_speed": "174%"
```


## Acceleration (internal solid infill)

Acceleration of internal solid infill. If the value is expressed as a percentage (e.g. 100%), it will be calculated based on the default acceleration.

**Key:** `internal_solid_infill_acceleration`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `100%`

### Example

```json
"internal_solid_infill_acceleration": "105%"
```


## Internal solid infill

Line width of internal solid infill. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `internal_solid_infill_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"internal_solid_infill_line_width": "2%"
```


## Internal solid infill pattern

Line pattern of internal solid infill. if the detect nattow internal solid infill be enabled, the concentric pattern will be used for the small area.

**Key:** `internal_solid_infill_pattern`

**Type:** `Enum`

**Default** `Monotonic`

**Enum values:**


### Example

```json
"internal_solid_infill_pattern": "octagramspiral"
```


## Speed (internal solid infill)

Speed of internal solid infill, not the top and bottom surface

**Key:** `internal_solid_infill_speed`

**Type:** `Float`

**Min:** `1`

**Default** `100`

### Example

```json
"internal_solid_infill_speed": 103.67
```


## Ironing angle

The angle ironing is done at. A negative number disables this function and uses the default method.

**Key:** `ironing_angle`

**Type:** `Float`

**Min:** `-1`

**Max:** `359`

**Default** `-1`

### Example

```json
"ironing_angle": -0.87
```


## Ironing flow

The amount of material to extrude during ironing. Relative to flow of normal layer height. Too high value results in overextrusion on the surface

**Key:** `ironing_flow`

**Type:** `Percent`

**Min:** `0`

**Max:** `100`

**Default** `10`

### Example

```json
"ironing_flow": "10%"
```


## Ironing Pattern

The pattern that will be used when ironing

**Key:** `ironing_pattern`

**Type:** `Enum`

**Default** `Rectilinear`

**Enum values:**


### Example

```json
"ironing_pattern": "concentric"
```


## Ironing line spacing

The distance between the lines of ironing

**Key:** `ironing_spacing`

**Type:** `Float`

**Min:** `0`

**Max:** `1`

**Default** `0.1`

### Example

```json
"ironing_spacing": 0.09
```


## Speed (ironing)

Print speed of ironing lines

**Key:** `ironing_speed`

**Type:** `Float`

**Min:** `1`

**Default** `20`

### Example

```json
"ironing_speed": 23.98
```


## Ironing Type

Ironing is using small flow to print on same height of surface again to make flat surface more smooth. This setting controls which layer being ironed

**Key:** `ironing_type`

**Type:** `Enum`

**Default** `NoIroning`

**Enum values:**


### Example

```json
"ironing_type": "top"
```


## Default line width

Default line width if other line widths are set to 0. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"line_width": "2%"
```


## Make overhang printable

Modify the geometry to print overhangs without support material.

**Key:** `make_overhang_printable`

**Type:** `Bool`

**Default** `false`

### Example

```json
"make_overhang_printable": false
```


## Make overhang printable maximum angle

Maximum angle of overhangs to allow after making more steep overhangs printable. 90° will not change the model at all and allow any overhang, while 0 will replace all overhangs with conical material.

**Key:** `make_overhang_printable_angle`

**Type:** `Float`

**Min:** `0`

**Max:** `90`

**Default** `55.0`

### Example

```json
"make_overhang_printable_angle": 60.02
```


## Make overhang printable hole area

Maximum area of a hole in the base of the model before it's filled by conical material.A value of 0 will fill all the holes in the model base.

**Key:** `make_overhang_printable_hole_size`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"make_overhang_printable_hole_size": 2.41
```


## Max bridge length

Max length of bridges that don't need support. Set it to 0 if you want all bridges to be supported, and set it to a very large value if you don't want any bridges to be supported.

**Key:** `max_bridge_length`

**Type:** `Float`

**Min:** `0`

**Default** `10`

### Example

```json
"max_bridge_length": 10.71
```


## Avoid crossing wall - Max detour length

Maximum detour distance for avoiding crossing wall. Don't detour if the detour distance is large than this value. Detour length could be specified either as an absolute value or as percentage (for example 50%) of a direct travel path. Zero to disable

**Key:** `max_travel_detour_distance`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `0.0`

### Example

```json
"max_travel_detour_distance": "3%"
```


## Extrusion rate smoothing

This parameter smooths out sudden extrusion rate changes that happen when the printer transitions from printing a high flow (high speed/larger width) extrusion to a lower flow (lower speed/smaller width) extrusion and vice versa.

It defines the maximum rate by which the extruded volumetric flow in mm3/sec can change over time. Higher values mean higher extrusion rate changes are allowed, resulting in faster speed transitions.

A value of 0 disables the feature. 

For a high speed, high flow direct drive printer (like the Bambu lab or Voron) this value is usually not needed. However it can provide some marginal benefit in certain cases where feature speeds vary greatly. For example, when there are aggressive slowdowns due to overhangs. In these cases a high value of around 300-350mm3/s2 is recommended as this allows for just enough smoothing to assist pressure advance achieve a smoother flow transition.

For slower printers without pressure advance, the value should be set much lower. A value of 10-15mm3/s2 is a good starting point for direct drive extruders and 5-10mm3/s2 for Bowden style. 

This feature is known as Pressure Equalizer in Prusa slicer.

Note: this parameter disables arc fitting.

**Key:** `max_volumetric_extrusion_rate_slope`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"max_volumetric_extrusion_rate_slope": 1.81
```


## Smoothing segment length

A lower value results in smoother extrusion rate transitions. However, this results in a significantly larger gcode file and more instructions for the printer to process. 

Default value of 3 works well for most cases. If your printer is stuttering, increase this value to reduce the number of adjustments made

Allowed values: 1-5

**Key:** `max_volumetric_extrusion_rate_slope_segment_length`

**Type:** `Int`

**Min:** `1`

**Max:** `5`

**Default** `3`

### Example

```json
"max_volumetric_extrusion_rate_slope_segment_length": 2
```


## Minimum wall width

Width of the wall that will replace thin features (according to the Minimum feature size) of the model. If the Minimum wall width is thinner than the thickness of the feature, the wall will become as thick as the feature itself. It's expressed as a percentage over nozzle diameter

**Key:** `min_bead_width`

**Type:** `Percent`

**Min:** `0`

**Default** `85`

### Example

```json
"min_bead_width": "77%"
```


## Minimum feature size

Minimum thickness of thin features. Model features that are thinner than this value will not be printed, while features thicker than the Minimum feature size will be widened to the Minimum wall width. It's expressed as a percentage over nozzle diameter

**Key:** `min_feature_size`

**Type:** `Percent`

**Min:** `0`

**Default** `25`

### Example

```json
"min_feature_size": "19%"
```


## One wall threshold

If a top surface has to be printed and it's partially covered by another layer, it won't be considered at a top layer where its width is below this value. This can be useful to not let the 'one perimeter on top' trigger on surface that should be covered only by perimeters. This value can be a mm or a % of the perimeter extrusion width.
Warning: If enabled, artifacts can be created is you have some thin features on the next layer, like letters. Set this setting to 0 to remove these artifacts.

**Key:** `min_width_top_surface`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `300%`

### Example

```json
"min_width_top_surface": "350%"
```


## Minimum sparse infill threshold

Sparse infill area which is smaller than threshold value is replaced by internal solid infill

**Key:** `minimum_sparse_infill_area`

**Type:** `Float`

**Min:** `0`

**Default** `15`

### Example

```json
"minimum_sparse_infill_area": 16.09
```


## Configuration notes

You can put here your personal notes. This text will be added to the G-code header comments.

**Key:** `notes`

**Type:** `String`

**Default** ``

### Example

```json
"notes": ""
```


## Only one wall on first layer

Use only one wall on first layer, to give more space to the bottom infill pattern

**Key:** `only_one_wall_first_layer`

**Type:** `Bool`

**Default** `false`

### Example

```json
"only_one_wall_first_layer": true
```


## Only one wall on top surfaces

Use only one wall on flat top surface, to give more space to the top infill pattern

**Key:** `only_one_wall_top`

**Type:** `Bool`

**Default** `false`

### Example

```json
"only_one_wall_top": true
```


## Enable

This option will drop the temperature of the inactive extruders to prevent oozing. It will enable a tall skirt automatically and move extruders outside such skirt when changing temperatures.

**Key:** `ooze_prevention`

**Type:** `Bool`

**Default** `false`

### Example

```json
"ooze_prevention": true
```


## Acceleration (outer wall)

Acceleration of outer wall. Using a lower value can improve quality

**Key:** `outer_wall_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `500`

### Example

```json
"outer_wall_acceleration": 378.08
```


## Jerk (outer wall)

Jerk of outer walls

**Key:** `outer_wall_jerk`

**Type:** `Float`

**Min:** `0`

**Default** `9`

### Example

```json
"outer_wall_jerk": 10.29
```


## Outer wall

Line width of outer wall. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `outer_wall_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"outer_wall_line_width": "1%"
```


## Speed (outer wall)

Speed of outer wall which is outermost and visible. It's used to be slower than inner wall speed to get better quality.

**Key:** `outer_wall_speed`

**Type:** `Float`

**Min:** `1`

**Default** `60`

### Example

```json
"outer_wall_speed": 49.59
```


## Speed (10%-25% overhang)

Speed for line of wall which has degree of overhang between 10% and 25% line width. 0 means using original wall speed

**Key:** `overhang_1_4_speed`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `0.0`

### Example

```json
"overhang_1_4_speed": 0.64
```


## Speed (25%-50% overhang)

Speed for line of wall which has degree of overhang between 25% and 50% line width. 0 means using original wall speed

**Key:** `overhang_2_4_speed`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `0.0`

### Example

```json
"overhang_2_4_speed": 0.56
```


## Speed (50%-75% overhang)

Speed for line of wall which has degree of overhang between 50% and 75% line width. 0 means using original wall speed

**Key:** `overhang_3_4_speed`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `0.0`

### Example

```json
"overhang_3_4_speed": "3%"
```


## Speed (75%-100% overhang)

Speed for line of wall which has degree of overhang between 75% and 100% line width. 0 means using original wall speed

**Key:** `overhang_4_4_speed`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `0.0`

### Example

```json
"overhang_4_4_speed": "4%"
```


## Reverse on odd

Extrude perimeters that have a part over an overhang in the reverse direction on odd layers. This alternating pattern can drastically improve steep overhang.

**Key:** `overhang_reverse`

**Type:** `Bool`

**Default** `false`

### Example

```json
"overhang_reverse": true
```


## Reverse threshold

Number of mm the overhang need to be for the reversal to be considered useful. Can be a % of the perimeter width.\nValue 0 enables reversal on every odd layers regardless.

**Key:** `overhang_reverse_threshold`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `50%`

### Example

```json
"overhang_reverse_threshold": "45%"
```


## Classic mode

Enable this option to use classic mode

**Key:** `overhang_speed_classic`

**Type:** `Bool`

**Default** `false`

### Example

```json
"overhang_speed_classic": true
```


## Post-processing Scripts

If you want to process the output G-code through custom scripts, just list their absolute paths here. Separate multiple scripts with a semicolon. Scripts will be passed the absolute path to the G-code file as the first argument, and they can access the Slic3r config settings by reading environment variables.

**Key:** `post_process`

**Type:** `Strings`

**Default** `[""]`

### Example

```json
"post_process": [""]
```


## Precise wall(experimental)

Improve shell precision by adjusting outer wall spacing. This also improves layer consistency.

**Key:** `precise_outer_wall`

**Type:** `Bool`

**Default** `false`

### Example

```json
"precise_outer_wall": true
```


## Brim width (prime tower)

Brim width of the prime tower

**Key:** `prime_tower_brim_width`

**Type:** `Float`

**Min:** `0`

**Default** `3.0`

### Example

```json
"prime_tower_brim_width": 2.7
```


## Prime tower width

Width of prime tower

**Key:** `prime_tower_width`

**Type:** `Float`

**Min:** `2`

**Default** `60.0`

### Example

```json
"prime_tower_width": 47.84
```


## Prime volume

The volume of material to prime extruder on tower.

**Key:** `prime_volume`

**Type:** `Float`

**Min:** `1`

**Default** `45.0`

### Example

```json
"prime_volume": 55.47
```


## Flow ratio

The material may have volumetric change after switching between molten state and crystalline state. This setting changes all extrusion flow of this filament in gcode proportionally. Recommended value range is between 0.95 and 1.05. Maybe you can tune this value to get nice flat surface when there has slight overflow or underflow

**Key:** `print_flow_ratio`

**Type:** `Float`

**Min:** `0`

**Max:** `2`

**Default** `1`

### Example

```json
"print_flow_ratio": 1.05
```


## Print sequence

Print sequence, layer by layer or object by object

**Key:** `print_sequence`

**Type:** `Enum`

**Default** `ByLayer`

**Enum values:**


### Example

```json
"print_sequence": "by object"
```


## Raft contact Z distance

Z gap between object and raft. Ignored for soluble interface

**Key:** `raft_contact_distance`

**Type:** `Float`

**Min:** `0`

**Default** `0.1`

### Example

```json
"raft_contact_distance": 0.08
```


## Raft expansion

Expand all raft layers in XY plane

**Key:** `raft_expansion`

**Type:** `Float`

**Min:** `0`

**Default** `1.5`

### Example

```json
"raft_expansion": 1.52
```


## Raft density (initial layer)

Density of the first raft or support layer

**Key:** `raft_first_layer_density`

**Type:** `Percent`

**Min:** `10`

**Max:** `100`

**Default** `90`

### Example

```json
"raft_first_layer_density": "99%"
```


## Raft expansion (initial layer)

Expand the first raft or support layer to improve bed plate adhesion

**Key:** `raft_first_layer_expansion`

**Type:** `Float`

**Min:** `0`

**Default** `2.0`

### Example

```json
"raft_first_layer_expansion": 1.73
```


## Raft layers

Object will be raised by this number of support layers. Use this function to avoid wrapping when print ABS

**Key:** `raft_layers`

**Type:** `Int`

**Min:** `0`

**Max:** `100`

**Default** `0`

### Example

```json
"raft_layers": 2
```


## Avoid crossing wall

Detour and avoid to travel across wall which may cause blob on surface

**Key:** `reduce_crossing_wall`

**Type:** `Bool`

**Default** `false`

### Example

```json
"reduce_crossing_wall": false
```


## Reduce infill retraction

Don't retract when the travel is in infill area absolutely. That means the oozing can't been seen. This can reduce times of retraction for complex model and save printing time, but make slicing and G-code generating slower

**Key:** `reduce_infill_retraction`

**Type:** `Bool`

**Default** `false`

### Example

```json
"reduce_infill_retraction": false
```


## Resolution

G-code path is genereated after simplifing the contour of model to avoid too much points and gcode lines in gcode file. Smaller value means higher resolution and more time to slice

**Key:** `resolution`

**Type:** `Float`

**Min:** `0`

**Default** `0.01`

### Example

```json
"resolution": 0.01
```


## Role base wipe speed

The wipe speed is determined by the speed of the current extrusion role.e.g. if a wipe action is executed immediately following an outer wall extrusion, the speed of the outer wall extrusion will be utilized for the wipe action.

**Key:** `role_based_wipe_speed`

**Type:** `Bool`

**Default** `true`

### Example

```json
"role_based_wipe_speed": true
```


## Seam gap

In order to reduce the visibility of the seam in a closed loop extrusion, the loop is interrupted and shortened by a specified amount.\nThis amount can be specified in millimeters or as a percentage of the current extruder diameter. The default value for this parameter is 10%.

**Key:** `seam_gap`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `10%`

### Example

```json
"seam_gap": "11%"
```


## Seam position

The start position to print each part of outer wall

**Key:** `seam_position`

**Type:** `Enum`

**Default** `Aligned`

**Enum values:**


### Example

```json
"seam_position": "nearest"
```


## Prime all printing extruders

If enabled, all printing extruders will be primed at the front edge of the print bed at the start of the print.

**Key:** `single_extruder_multi_material_priming`

**Type:** `Bool`

**Default** `true`

### Example

```json
"single_extruder_multi_material_priming": false
```


## Skirt distance

Distance from skirt to brim or object

**Key:** `skirt_distance`

**Type:** `Float`

**Min:** `0`

**Max:** `10`

**Default** `2`

### Example

```json
"skirt_distance": 1.65
```


## Skirt height

How many layers of skirt. Usually only one layer

**Key:** `skirt_height`

**Type:** `Int`

**Max:** `10000`

**Default** `1`

### Example

```json
"skirt_height": 0
```


## Skirt loops

Number of loops for the skirt. Zero means disabling skirt

**Key:** `skirt_loops`

**Type:** `Int`

**Min:** `0`

**Max:** `10`

**Default** `1`

### Example

```json
"skirt_loops": 0
```


## Speed (skirt)

Speed of skirt, in mm/s. Zero means use default layer extrusion speed.

**Key:** `skirt_speed`

**Type:** `Float`

**Min:** `0`

**Default** `50.0`

### Example

```json
"skirt_speed": 56.94
```


## Slicing Mode

Use "Even-odd" for 3DLabPrint airplane models. Use "Close holes" to close all holes in the model.

**Key:** `slicing_mode`

**Type:** `Enum`

**Default** `Regular`

**Enum values:**


### Example

```json
"slicing_mode": "regular"
```


## Number of slow layers

The first few layers are printed slower than normal. The speed is gradually increased in a linear fashion over the specified number of layers.

**Key:** `slow_down_layers`

**Type:** `Int`

**Min:** `0`

**Default** `0`

### Example

```json
"slow_down_layers": 3
```


## Slow down for curled perimeters

Enable this option to slow printing down in areas where potential curled perimeters may exist

**Key:** `slowdown_for_curled_perimeters`

**Type:** `Bool`

**Default** `false`

### Example

```json
"slowdown_for_curled_perimeters": false
```


## Speed (small perimeters)

This separate setting will affect the speed of perimeters having radius <= small_perimeter_threshold (usually holes). If expressed as percentage (for example: 80%) it will be calculated on the outer wall speed setting above. Set to zero for auto.

**Key:** `small_perimeter_speed`

**Type:** `FloatOrPercent`

**Min:** `1`

**Default** `50%`

### Example

```json
"small_perimeter_speed": "43%"
```


## Small perimeters threshold

This sets the threshold for small perimeter length. Default threshold is 0mm

**Key:** `small_perimeter_threshold`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"small_perimeter_threshold": 3.92
```


## Solid infill

Filament to print solid infill

**Key:** `solid_infill_filament`

**Type:** `Int`

**Min:** `1`

**Default** `1`

### Example

```json
"solid_infill_filament": 1
```


## Acceleration (sparse infill)

Acceleration of sparse infill. If the value is expressed as a percentage (e.g. 100%), it will be calculated based on the default acceleration.

**Key:** `sparse_infill_acceleration`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `100%`

### Example

```json
"sparse_infill_acceleration": "112%"
```


## Sparse infill density

Density of internal sparse infill, 100% means solid throughout

**Key:** `sparse_infill_density`

**Type:** `Percent`

**Min:** `0`

**Max:** `100`

**Default** `20`

### Example

```json
"sparse_infill_density": "21%"
```


## Infill

Filament to print internal sparse infill.

**Key:** `sparse_infill_filament`

**Type:** `Int`

**Min:** `1`

**Default** `1`

### Example

```json
"sparse_infill_filament": 1
```


## Sparse infill

Line width of internal sparse infill. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `sparse_infill_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"sparse_infill_line_width": "4%"
```


## Sparse infill pattern

Line pattern for internal sparse infill

**Key:** `sparse_infill_pattern`

**Type:** `Enum`

**Default** `Cubic`

**Enum values:**


### Example

```json
"sparse_infill_pattern": "archimedeanchords"
```


## Speed (sparse infill)

Speed of internal sparse infill

**Key:** `sparse_infill_speed`

**Type:** `Float`

**Min:** `1`

**Default** `100`

### Example

```json
"sparse_infill_speed": 124.82
```


## Spiral vase

Spiralize smooths out the z moves of the outer contour. And turns a solid model into a single walled print with solid bottom layers. The final generated model has no seam

**Key:** `spiral_mode`

**Type:** `Bool`

**Default** `false`

### Example

```json
"spiral_mode": true
```


## Staggered inner seams

This option causes the inner seams to be shifted backwards based on their depth, forming a zigzag pattern.

**Key:** `staggered_inner_seams`

**Type:** `Bool`

**Default** `false`

### Example

```json
"staggered_inner_seams": true
```


## Temperature variation

Temperature difference to be applied when an extruder is not active. Enables a full-height "sacrificial" skirt on which the nozzles are periodically wiped.

**Key:** `standby_temperature_delta`

**Type:** `Int`

**Min:** `0`

**Max:** `1500`

**Default** `-5`

### Example

```json
"standby_temperature_delta": 0
```


## Pattern angle

Use this setting to rotate the support pattern on the horizontal plane.

**Key:** `support_angle`

**Type:** `Float`

**Min:** `0`

**Max:** `359`

**Default** `0`

### Example

```json
"support_angle": 4.72
```


## Base pattern

Line pattern of support

**Key:** `support_base_pattern`

**Type:** `Enum`

**Default** `Rectilinear`

**Enum values:**


### Example

```json
"support_base_pattern": "lightning"
```


## Base pattern spacing

Spacing between support lines

**Key:** `support_base_pattern_spacing`

**Type:** `Float`

**Min:** `0`

**Default** `2.5`

### Example

```json
"support_base_pattern_spacing": 2.42
```


## Bottom interface spacing

Spacing of bottom interface lines. Zero means solid interface

**Key:** `support_bottom_interface_spacing`

**Type:** `Float`

**Min:** `0`

**Default** `0.5`

### Example

```json
"support_bottom_interface_spacing": 0.55
```


## Bottom Z distance

The z gap between the bottom support interface and object

**Key:** `support_bottom_z_distance`

**Type:** `Float`

**Default** `0.2`

### Example

```json
"support_bottom_z_distance": 0.18
```


## Support critical regions only

Only create support for critical regions including sharp tail, cantilever, etc.

**Key:** `support_critical_regions_only`

**Type:** `Bool`

**Default** `false`

### Example

```json
"support_critical_regions_only": true
```


## Normal Support expansion

Expand (+) or shrink (-) the horizontal span of normal support

**Key:** `support_expansion`

**Type:** `Float`

**Default** `0`

### Example

```json
"support_expansion": 1.23
```


## Support/raft base

Filament to print support base and raft. "Default" means no specific filament for support and current filament is used

**Key:** `support_filament`

**Type:** `Int`

**Min:** `0`

**Default** `1`

### Example

```json
"support_filament": 0
```


## Bottom interface layers

Number of bottom interface layers. -1 means same with use top interface layers

**Key:** `support_interface_bottom_layers`

**Type:** `Int`

**Min:** `-1`

**Default** `0`

**Enum values:**


### Example

```json
"support_interface_bottom_layers": -1
```


## Support/raft interface

Filament to print support interface. "Default" means no specific filament for support interface and current filament is used

**Key:** `support_interface_filament`

**Type:** `Int`

**Min:** `0`

**Default** `1`

### Example

```json
"support_interface_filament": 1
```


## Interface use loop pattern

Cover the top contact layer of the supports with loops. Disabled by default.

**Key:** `support_interface_loop_pattern`

**Type:** `Bool`

**Default** `false`

### Example

```json
"support_interface_loop_pattern": false
```


## Interface pattern

Line pattern of support interface. Default pattern for non-soluble support interface is Rectilinear, while default pattern for soluble support interface is Concentric

**Key:** `support_interface_pattern`

**Type:** `Enum`

**Default** `Rectilinear`

**Enum values:**


### Example

```json
"support_interface_pattern": "auto"
```


## Top interface spacing

Spacing of interface lines. Zero means solid interface

**Key:** `support_interface_spacing`

**Type:** `Float`

**Min:** `0`

**Default** `0.5`

### Example

```json
"support_interface_spacing": 0.51
```


## Speed (support interface)

Speed of support interface

**Key:** `support_interface_speed`

**Type:** `Float`

**Min:** `1`

**Default** `80`

### Example

```json
"support_interface_speed": 74.7
```


## Top interface layers

Number of top interface layers

**Key:** `support_interface_top_layers`

**Type:** `Int`

**Min:** `0`

**Default** `3`

**Enum values:**


### Example

```json
"support_interface_top_layers": 3
```


## Line width (support)

Line width of support. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `support_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"support_line_width": "1%"
```


## Support/object xy distance

XY separation between an object and its support

**Key:** `support_object_xy_distance`

**Type:** `Float`

**Min:** `0`

**Max:** `10`

**Default** `0.35`

### Example

```json
"support_object_xy_distance": 0.39
```


## On build plate only

Don't create support on model surface, only on build plate

**Key:** `support_on_build_plate_only`

**Type:** `Bool`

**Default** `false`

### Example

```json
"support_on_build_plate_only": true
```


## Remove small overhangs

Remove small overhangs that possibly need no supports.

**Key:** `support_remove_small_overhang`

**Type:** `Bool`

**Default** `true`

### Example

```json
"support_remove_small_overhang": false
```


## Speed (support)

Speed of support

**Key:** `support_speed`

**Type:** `Float`

**Min:** `1`

**Default** `80`

### Example

```json
"support_speed": 76.75
```


## Support style

Style and shape of the support. For normal support, projecting the supports into a regular grid will create more stable supports (default), while snug support towers will save material and reduce object scarring.\nFor tree support, slim and organic style will merge branches more aggressively and save a lot of material (default organic), while hybrid style will create similar structure to normal support under large flat overhangs.

**Key:** `support_style`

**Type:** `Enum`

**Default** `Default`

**Enum values:**


### Example

```json
"support_style": "tree_hybrid"
```


## Threshold angle

Support will be generated for overhangs whose slope angle is below the threshold.

**Key:** `support_threshold_angle`

**Type:** `Int`

**Min:** `1`

**Max:** `90`

**Default** `30`

### Example

```json
"support_threshold_angle": 32
```


## Top Z distance

The z gap between the top support interface and object

**Key:** `support_top_z_distance`

**Type:** `Float`

**Default** `0.2`

### Example

```json
"support_top_z_distance": 0.15
```


## Support type

normal(auto) and tree(auto) is used to generate support automatically. If normal(manual) or tree(manual) is selected, only support enforcers are generated

**Key:** `support_type`

**Type:** `Enum`

**Default** `NormalAuto`

**Enum values:**


### Example

```json
"support_type": "tree(auto)"
```


## Thick bridges

If enabled, bridges are more reliable, can bridge longer distances, but may look worse. If disabled, bridges look better but are reliable just for shorter bridged distances.

**Key:** `thick_bridges`

**Type:** `Bool`

**Default** `false`

### Example

```json
"thick_bridges": true
```


## Timelapse

If smooth or traditional mode is selected, a timelapse video will be generated for each print. After each layer is printed, a snapshot is taken with the chamber camera. All of these snapshots are composed into a timelapse video when printing completes. If smooth mode is selected, the toolhead will move to the excess chute after each layer is printed and then take a snapshot. Since the melt filament may leak from the nozzle during the process of taking a snapshot, prime tower is required for smooth mode to wipe nozzle.

**Key:** `timelapse_type`

**Type:** `Enum`

**Default** `Traditional`

**Enum values:**


### Example

```json
"timelapse_type": "0"
```


## Top shell layers

This is the number of solid layers of top shell, including the top surface layer. When the thickness calculated by this value is thinner than top shell thickness, the top shell layers will be increased

**Key:** `top_shell_layers`

**Type:** `Int`

**Min:** `0`

**Default** `4`

### Example

```json
"top_shell_layers": 4
```


## Top shell thickness

The number of top solid layers is increased when slicing if the thickness calculated by top shell layers is thinner than this value. This can avoid having too thin shell when layer height is small. 0 means that this setting is disabled and thickness of top shell is absolutely determained by top shell layers

**Key:** `top_shell_thickness`

**Type:** `Float`

**Min:** `0`

**Default** `0.6`

### Example

```json
"top_shell_thickness": 0.58
```


## Top surface flow ratio

This factor affects the amount of material for top solid infill. You can decrease it slightly to have smooth surface finish

**Key:** `top_solid_infill_flow_ratio`

**Type:** `Float`

**Min:** `0`

**Max:** `2`

**Default** `1`

### Example

```json
"top_solid_infill_flow_ratio": 0.78
```


## Acceleration (top surface)

Acceleration of top surface infill. Using a lower value may improve top surface quality

**Key:** `top_surface_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `500`

### Example

```json
"top_surface_acceleration": 532.55
```


## Jerk (top surface)

Jerk for top surface

**Key:** `top_surface_jerk`

**Type:** `Float`

**Min:** `1`

**Default** `9`

### Example

```json
"top_surface_jerk": 7.89
```


## Top surface

Line width for top surfaces. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `top_surface_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"top_surface_line_width": "2%"
```


## Top surface pattern

Line pattern of top surface infill

**Key:** `top_surface_pattern`

**Type:** `Enum`

**Default** `Monotonic`

**Enum values:**


### Example

```json
"top_surface_pattern": "monotonicline"
```


## Speed (top surface)

Speed of top surface infill which is solid

**Key:** `top_surface_speed`

**Type:** `Float`

**Min:** `1`

**Default** `100`

### Example

```json
"top_surface_speed": 106.0
```


## Acceleration (travel)

Acceleration of travel moves

**Key:** `travel_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `10000`

### Example

```json
"travel_acceleration": 8967.09
```


## Jerk (travel)

Jerk for travel

**Key:** `travel_jerk`

**Type:** `Float`

**Min:** `1`

**Default** `12`

### Example

```json
"travel_jerk": 12.78
```


## Speed (travel)

Speed of travel which is faster and without extrusion

**Key:** `travel_speed`

**Type:** `Float`

**Min:** `1`

**Default** `120`

### Example

```json
"travel_speed": 101.56
```


## Z travel speed

Speed of vertical travel along z axis. This is typically lower because build plate or gantry is hard to be moved. Zero means using travel speed directly in gcode, but will be limited by printer's ability when run gcode

**Key:** `travel_speed_z`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"travel_speed_z": 3.65
```


## Adaptive layer height (tree support)

Enabling this option means the height of  tree support layer except the first will be automatically calculated

**Key:** `tree_support_adaptive_layer_height`

**Type:** `Bool`

**Default** `true`

### Example

```json
"tree_support_adaptive_layer_height": false
```


## Preferred Branch Angle

The preferred angle of the branches, when they do not have to avoid the model. Use a lower angle to make them more vertical and more stable. Use a higher angle for branches to merge faster.

**Key:** `tree_support_angle_slow`

**Type:** `Float`

**Min:** `10`

**Max:** `85`

**Default** `25`

### Example

```json
"tree_support_angle_slow": 28.28
```


## Auto brim width

Enabling this option means the width of the brim for tree support will be automatically calculated

**Key:** `tree_support_auto_brim`

**Type:** `Bool`

**Default** `true`

### Example

```json
"tree_support_auto_brim": true
```


## Tree support branch angle

This setting determines the maximum overhang angle that t he branches of tree support allowed to make.If the angle is increased, the branches can be printed more horizontally, allowing them to reach farther.

**Key:** `tree_support_branch_angle`

**Type:** `Float`

**Min:** `0`

**Max:** `60`

**Default** `40.0`

### Example

```json
"tree_support_branch_angle": 45.49
```


## Tree support branch angle (organic)

This setting determines the maximum overhang angle that t he branches of tree support allowed to make.If the angle is increased, the branches can be printed more horizontally, allowing them to reach farther.

**Key:** `tree_support_branch_angle_organic`

**Type:** `Float`

**Min:** `0`

**Max:** `60`

**Default** `40.0`

### Example

```json
"tree_support_branch_angle_organic": 41.85
```


## Tree support branch diameter

This setting determines the initial diameter of support nodes.

**Key:** `tree_support_branch_diameter`

**Type:** `Float`

**Min:** `1`

**Max:** `10`

**Default** `5.0`

### Example

```json
"tree_support_branch_diameter": 4.24
```


## Branch Diameter Angle

The angle of the branches' diameter as they gradually become thicker towards the bottom. An angle of 0 will cause the branches to have uniform thickness over their length. A bit of an angle can increase stability of the organic support.

**Key:** `tree_support_branch_diameter_angle`

**Type:** `Float`

**Min:** `0`

**Max:** `15`

**Default** `5`

### Example

```json
"tree_support_branch_diameter_angle": 4.68
```


## Branch Diameter with double walls

Branches with area larger than the area of a circle of this diameter will be printed with double walls for stability. Set this value to zero for no double walls.

**Key:** `tree_support_branch_diameter_double_wall`

**Type:** `Float`

**Min:** `0`

**Max:** `100`

**Default** `3.0`

### Example

```json
"tree_support_branch_diameter_double_wall": 3.22
```


## Tree support branch diameter (organic)

This setting determines the initial diameter of support nodes.

**Key:** `tree_support_branch_diameter_organic`

**Type:** `Float`

**Min:** `1`

**Max:** `10`

**Default** `2.0`

### Example

```json
"tree_support_branch_diameter_organic": 2.17
```


## Tree support branch distance

This setting determines the distance between neighboring tree support nodes.

**Key:** `tree_support_branch_distance`

**Type:** `Float`

**Min:** `1`

**Max:** `10`

**Default** `5.0`

### Example

```json
"tree_support_branch_distance": 4.79
```


## Tree support branch distance (organic)

This setting determines the distance between neighboring tree support nodes.

**Key:** `tree_support_branch_distance_organic`

**Type:** `Float`

**Min:** `1`

**Max:** `10`

**Default** `1.0`

### Example

```json
"tree_support_branch_distance_organic": 1.17
```


## Tree support brim width

Distance from tree branch to the outermost brim line

**Key:** `tree_support_brim_width`

**Type:** `Float`

**Min:** `0`

**Default** `3`

### Example

```json
"tree_support_brim_width": 2.68
```


## Tip Diameter

Branch tip diameter for organic supports.

**Key:** `tree_support_tip_diameter`

**Type:** `Float`

**Min:** `0`

**Max:** `100`

**Default** `0.8`

### Example

```json
"tree_support_tip_diameter": 0.74
```


## Branch Density

Adjusts the density of the support structure used to generate the tips of the branches. A higher value results in better overhangs but the supports are harder to remove, thus it is recommended to enable top support interfaces instead of a high branch density value if dense interfaces are needed.

**Key:** `tree_support_top_rate`

**Type:** `Percent`

**Min:** `5`

**Default** `30`

### Example

```json
"tree_support_top_rate": "31%"
```


## Tree support wall loops

This setting specify the count of walls around tree support

**Key:** `tree_support_wall_count`

**Type:** `Int`

**Min:** `0`

**Default** `1`

### Example

```json
"tree_support_wall_count": 0
```


## Wall distribution count

The number of walls, counted from the center, over which the variation needs to be spread. Lower values mean that the outer walls don't change in width

**Key:** `wall_distribution_count`

**Type:** `Int`

**Min:** `1`

**Default** `1`

### Example

```json
"wall_distribution_count": 1
```


## Wall filament

Filament to print walls

**Key:** `wall_filament`

**Type:** `Int`

**Min:** `1`

**Default** `1`

### Example

```json
"wall_filament": 1
```


## Wall generator

Classic wall generator produces walls with constant extrusion width and for very thin areas is used gap-fill. Arachne engine produces walls with variable extrusion width

**Key:** `wall_generator`

**Type:** `Enum`

**Default** `Arachne`

**Enum values:**


### Example

```json
"wall_generator": "arachne"
```


## Order of inner wall/outer wall/infil

Print sequence of inner wall, outer wall and infill.

**Key:** `wall_infill_order`

**Type:** `Enum`

**Default** `InnerOuterInfill`

**Enum values:**


### Example

```json
"wall_infill_order": "infill/outer wall/inner wall"
```


## Wall loops

Number of walls of every layer

**Key:** `wall_loops`

**Type:** `Int`

**Min:** `0`

**Max:** `1000`

**Default** `2`

### Example

```json
"wall_loops": 1
```


## Wall transitioning threshold angle

When to create transitions between even and odd numbers of walls. A wedge shape with an angle greater than this setting will not have transitions and no walls will be printed in the center to fill the remaining space. Reducing this setting reduces the number and length of these center walls, but may leave gaps or overextrude

**Key:** `wall_transition_angle`

**Type:** `Float`

**Min:** `1`

**Max:** `59`

**Default** `10.0`

### Example

```json
"wall_transition_angle": 10.24
```


## Wall transitioning filter margin

Prevent transitioning back and forth between one extra wall and one less. This margin extends the range of extrusion widths which follow to [Minimum wall width - margin, 2 * Minimum wall width + margin]. Increasing this margin reduces the number of transitions, which reduces the number of extrusion starts/stops and travel time. However, large extrusion width variation can lead to under- or overextrusion problems. It's expressed as a percentage over nozzle diameter

**Key:** `wall_transition_filter_deviation`

**Type:** `Percent`

**Min:** `0`

**Default** `25`

### Example

```json
"wall_transition_filter_deviation": "21%"
```


## Wall transition length

When transitioning between different numbers of walls as the part becomes thinner, a certain amount of space is allotted to split or join the wall segments. It's expressed as a percentage over nozzle diameter

**Key:** `wall_transition_length`

**Type:** `Percent`

**Min:** `0`

**Default** `100`

### Example

```json
"wall_transition_length": "94%"
```


## Wipe on loops

To minimize the visibility of the seam in a closed loop extrusion, a small inward movement is executed before the extruder leaves the loop.

**Key:** `wipe_on_loops`

**Type:** `Bool`

**Default** `false`

### Example

```json
"wipe_on_loops": false
```


## Wipe speed

The wipe speed is determined by the speed setting specified in this configuration.If the value is expressed as a percentage (e.g. 80%), it will be calculated based on the travel speed setting above.The default value for this parameter is 80%

**Key:** `wipe_speed`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `80%`

### Example

```json
"wipe_speed": "60%"
```


## Maximal bridging distance

Maximal distance between supports on sparse infill sections.

**Key:** `wipe_tower_bridging`

**Type:** `Float`

**Default** `10.0`

### Example

```json
"wipe_tower_bridging": 9.56
```


## Stabilization cone apex angle

Angle at the apex of the cone that is used to stabilize the wipe tower. Larger angle means wider base.

**Key:** `wipe_tower_cone_angle`

**Type:** `Float`

**Min:** `0`

**Max:** `90`

**Default** `0.0`

### Example

```json
"wipe_tower_cone_angle": 3.2
```


## Wipe tower purge lines spacing

Spacing of purge lines on the wipe tower.

**Key:** `wipe_tower_extra_spacing`

**Type:** `Percent`

**Min:** `100`

**Max:** `300`

**Default** `100.0`

### Example

```json
"wipe_tower_extra_spacing": "76%"
```


## Wipe tower extruder

The extruder to use when printing perimeter of the wipe tower. Set to 0 to use the one that is available (non-soluble would be preferred).

**Key:** `wipe_tower_extruder`

**Type:** `Int`

**Min:** `0`

**Default** `0`

### Example

```json
"wipe_tower_extruder": 1
```


## No sparse layers (EXPERIMENTAL)

If enabled, the wipe tower will not be printed on layers with no toolchanges. On layers with a toolchange, extruder will travel downward to print the wipe tower. User is responsible for ensuring there is no collision with the print.

**Key:** `wipe_tower_no_sparse_layers`

**Type:** `Bool`

**Default** `false`

### Example

```json
"wipe_tower_no_sparse_layers": true
```


## Wipe tower rotation angle

Wipe tower rotation angle with respect to x-axis.

**Key:** `wipe_tower_rotation_angle`

**Type:** `Float`

**Default** `0.0`

### Example

```json
"wipe_tower_rotation_angle": 3.45
```


## Purging volumes - load/unload volumes (extruder)

This vector saves required volumes to change from/to each tool used on the wipe tower. These values are used to simplify creation of the full purging volumes below.

**Key:** `wiping_volumes_extruders`

**Type:** `Floats`

**Default** `[70.0, 70.0, 70.0, 70.0, 70.0, 70.0, 70.0, 70.0, 70.0, 70.0]`

### Example

```json
"wiping_volumes_extruders": [
    74.68,
    74.65,
    74.75,
    71.39,
    72.61,
    71.67,
    71.64,
    73.38,
    73.0,
    74.98
  ]
```


## X-Y contour compensation

Contour of object will be grown or shrunk in XY plane by the configured value. Positive value makes contour bigger. Negative value makes contour smaller. This function is used to adjust size slightly when the object has assembling issue

**Key:** `xy_contour_compensation`

**Type:** `Float`

**Default** `0`

### Example

```json
"xy_contour_compensation": 1.34
```


## X-Y hole compensation

Holes of object will be grown or shrunk in XY plane by the configured value. Positive value makes holes bigger. Negative value makes holes smaller. This function is used to adjust size slightly when the object has assembling issue

**Key:** `xy_hole_compensation`

**Type:** `Float`

**Default** `0`

### Example

```json
"xy_hole_compensation": 2.89
```
