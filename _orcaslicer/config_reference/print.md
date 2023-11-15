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
"accel_to_decel_factor": "41%"
```


## Adaptive layer height [deprecated]

[No documentation provided]

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
"bottom_shell_layers": 2
```


## Bottom shell thickness

The number of bottom solid layers is increased when slicing if the thickness calculated by bottom shell layers is thinner than this value. This can avoid having too thin shell when layer height is small. 0 means that this setting is disabled and thickness of bottom shell is absolutely determained by bottom shell layers

**Key:** `bottom_shell_thickness`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"bottom_shell_thickness": 2.5
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
"bottom_solid_infill_flow_ratio": 1.07
```


## Bottom surface pattern

Line pattern of bottom surface infill, not bridge infill

**Key:** `bottom_surface_pattern`

**Type:** `Enum`

**Default** `Monotonic`

**Enum values:**


### Example

```json
"bottom_surface_pattern": "zig-zag"
```


## Bridge

Acceleration of bridges. If the value is expressed as a percentage (e.g. 50%), it will be calculated based on the outer wall acceleration.

**Key:** `bridge_acceleration`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `50%`

### Example

```json
"bridge_acceleration": "47%"
```


## Bridge infill direction

Bridging angle override. If left to zero, the bridging angle will be calculated automatically. Otherwise the provided angle will be used for external bridges. Use 180°for zero angle.

**Key:** `bridge_angle`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"bridge_angle": 1.92
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
"bridge_density": "79%"
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
"bridge_flow": 1.17
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


## Bridge speed

Speed of bridge and completely overhang wall

**Key:** `bridge_speed`

**Type:** `Float`

**Min:** `1`

**Default** `25`

### Example

```json
"bridge_speed": 23.52
```


## Brim ear detection radius

The geometry will be decimated before dectecting sharp angles. This parameter indicates the minimum length of the deviation for the decimation.\n0 to deactivate

**Key:** `brim_ears_detection_length`

**Type:** `Float`

**Min:** `0`

**Default** `1`

### Example

```json
"brim_ears_detection_length": 1.04
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
"brim_ears_max_angle": 147.66
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
"brim_object_gap": 2
```


## Brim type

This controls the generation of the brim at outer and/or inner side of models. Auto means the brim width is analysed and calculated automatically.

**Key:** `brim_type`

**Type:** `Enum`

**Default** `AutoBrim`

**Enum values:**


### Example

```json
"brim_type": "inner_only"
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
"brim_width": 3.23
```


## Normal printing

The default acceleration of both normal printing and travel except initial layer

**Key:** `default_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `500.0`

### Example

```json
"default_acceleration": 541.85
```


## Default jerk

Default

**Key:** `default_jerk`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"default_jerk": 4.26
```


## Detect overhang wall

Detect the overhang percentage relative to line width and use different speed to print. For 100%% overhang, bridge speed is used.

**Key:** `detect_overhang_wall`

**Type:** `Bool`

**Default** `true`

### Example

```json
"detect_overhang_wall": false
```


## Detect thin wall

Detect thin wall which can't contain two line width. And use single line to print. Maybe printed not very well, because it's not closed loop

**Key:** `detect_thin_wall`

**Type:** `Bool`

**Default** `false`

### Example

```json
"detect_thin_wall": true
```


## Draft shield

[No documentation provided]

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


## Slow down for overhang

Enable this option to slow printing down for different overhang degree

**Key:** `enable_overhang_speed`

**Type:** `Bool`

**Default** `true`

### Example

```json
"enable_overhang_speed": true
```


## Enable prime tower

[No documentation provided]

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

[No documentation provided]

**Key:** `enforce_support_layers`

**Type:** `Int`

**Min:** `0`

**Max:** `5000`

**Default** `0`

### Example

```json
"enforce_support_layers": 2
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
"filter_out_gap_fill": 3.16
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
"flush_into_support": false
```


## Fuzzy Skin

Randomly jitter while printing the wall, so that the surface has a rough look. This setting controls the fuzzy position

**Key:** `fuzzy_skin`

**Type:** `Enum`

**Default** `None`

**Enum values:**


### Example

```json
"fuzzy_skin": "external"
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
"fuzzy_skin_point_distance": 0.6
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
"fuzzy_skin_thickness": 0.35
```


## Gap infill

Speed of gap infill. Gap usually has irregular line width and should be printed more slowly

**Key:** `gap_infill_speed`

**Type:** `Float`

**Min:** `1`

**Default** `30`

### Example

```json
"gap_infill_speed": 27.78
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
"gcode_label_objects": false
```


## Convert holes to polyholes

Search for almost-circular holes that span more than one layer and convert the geometry to polyholes. Use the nozzle size and the (biggest) diameter to compute the polyhole.\nSee http://hydraraptor.blogspot.com/2011/02/polyholes.html

**Key:** `hole_to_polyhole`

**Type:** `Bool`

**Default** `false`

### Example

```json
"hole_to_polyhole": true
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
"hole_to_polyhole_twisted": false
```


## Independent support layer height

[No documentation provided]

**Key:** `independent_support_layer_height`

**Type:** `Bool`

**Default** `true`

### Example

```json
"independent_support_layer_height": false
```


## Sparse infill anchor length

Connect an infill line to an internal perimeter with a short segment of an additional perimeter. If expressed as percentage (example: 15%) it is calculated over infill extrusion width. Slic3r tries to connect two close infill lines to a short perimeter segment. If no such perimeter segment shorter than infill_anchor_max is found, the infill line is connected to a perimeter segment at just one side and the length of the perimeter segment taken is limited to this parameter, but no longer than anchor_length_max. \nSet this parameter to zero to disable anchoring perimeters connected to a single infill line.

**Key:** `infill_anchor`

**Type:** `FloatOrPercent`

**Default** `400%`

**Enum values:**


### Example

```json
"infill_anchor": "382%"
```


## Maximum length of the infill anchor

[No documentation provided]

**Key:** `infill_anchor_max`

**Type:** `FloatOrPercent`

**Default** `20.0`

**Enum values:**


### Example

```json
"infill_anchor_max": "24%"
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
"infill_direction": 35.76
```


## Infill jerk

Jerk for infill

**Key:** `infill_jerk`

**Type:** `Float`

**Min:** `1`

**Default** `9`

### Example

```json
"infill_jerk": 8.17
```


## Infill/Wall overlap

Infill area is enlarged slightly to overlap with wall for better bonding. The percentage value is relative to line width of sparse infill

**Key:** `infill_wall_overlap`

**Type:** `Percent`

**Default** `15`

### Example

```json
"infill_wall_overlap": "12%"
```


## Initial layer acceleration

Acceleration of initial layer. Using a lower value can improve build plate adhesive

**Key:** `initial_layer_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `300`

### Example

```json
"initial_layer_acceleration": 326.77
```


## Initial layer infill

Speed of solid infill part of initial layer

**Key:** `initial_layer_infill_speed`

**Type:** `Float`

**Min:** `1`

**Default** `60.0`

### Example

```json
"initial_layer_infill_speed": 67.37
```


## Initial layer jerk

Jerk for initial layer

**Key:** `initial_layer_jerk`

**Type:** `Float`

**Min:** `1`

**Default** `9`

### Example

```json
"initial_layer_jerk": 8.02
```


## Initial layer line width

Line width of initial layer. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `initial_layer_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"initial_layer_line_width": "4%"
```


## First layer minimum wall width

The minimum wall width that should be used for the first layer is recommended to be set to the same size as the nozzle. This adjustment is expected to enhance adhesion.

**Key:** `initial_layer_min_bead_width`

**Type:** `Percent`

**Min:** `0`

**Default** `85`

### Example

```json
"initial_layer_min_bead_width": "82%"
```


## Initial layer height

Height of initial layer. Making initial layer height to be thick slightly can improve build plate adhension

**Key:** `initial_layer_print_height`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"initial_layer_print_height": 0.15
```


## Initial layer speed

Speed of initial layer except the solid infill part

**Key:** `initial_layer_speed`

**Type:** `Float`

**Min:** `1`

**Default** `30`

### Example

```json
"initial_layer_speed": 35.13
```


## Initial layer travel speed

Travel speed of initial layer

**Key:** `initial_layer_travel_speed`

**Type:** `FloatOrPercent`

**Min:** `1`

**Default** `100%`

### Example

```json
"initial_layer_travel_speed": "98%"
```


## Inner wall acceleration

Acceleration of inner walls

**Key:** `inner_wall_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `10000`

### Example

```json
"inner_wall_acceleration": 10225.13
```


## Inner wall jerk

Jerk of inner walls

**Key:** `inner_wall_jerk`

**Type:** `Float`

**Min:** `0`

**Default** `9`

### Example

```json
"inner_wall_jerk": 10.19
```


## Inner wall line width

Line width of inner wall. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `inner_wall_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"inner_wall_line_width": "4%"
```


## Inner wall speed

Speed of inner wall

**Key:** `inner_wall_speed`

**Type:** `Float`

**Min:** `1`

**Default** `60`

### Example

```json
"inner_wall_speed": 69.68
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


## Internal bridge speed

Speed of internal bridge. If the value is expressed as a percentage, it will be calculated based on the bridge_speed. Default value is 150%.

**Key:** `internal_bridge_speed`

**Type:** `FloatOrPercent`

**Min:** `1`

**Default** `150%`

### Example

```json
"internal_bridge_speed": "140%"
```


## Internal solid infill acceleration

Acceleration of internal solid infill. If the value is expressed as a percentage (e.g. 100%), it will be calculated based on the default acceleration.

**Key:** `internal_solid_infill_acceleration`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `100%`

### Example

```json
"internal_solid_infill_acceleration": "119%"
```


## Internal solid infill line width

Line width of internal solid infill. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `internal_solid_infill_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"internal_solid_infill_line_width": "4%"
```


## Internal solid infill pattern

Line pattern of internal solid infill. if the detect nattow internal solid infill be enabled, the concentric pattern will be used for the small area.

**Key:** `internal_solid_infill_pattern`

**Type:** `Enum`

**Default** `Monotonic`

**Enum values:**


### Example

```json
"internal_solid_infill_pattern": "alignedrectilinear"
```


## Internal solid infill speed

Speed of internal solid infill, not the top and bottom surface

**Key:** `internal_solid_infill_speed`

**Type:** `Float`

**Min:** `1`

**Default** `100`

### Example

```json
"internal_solid_infill_speed": 98.6
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
"ironing_angle": -0.77
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
"ironing_flow": "9%"
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
"ironing_spacing": 0.11
```


## Ironing speed

Print speed of ironing lines

**Key:** `ironing_speed`

**Type:** `Float`

**Min:** `1`

**Default** `20`

### Example

```json
"ironing_speed": 24.54
```


## Ironing Type

Ironing is using small flow to print on same height of surface again to make flat surface more smooth. This setting controls which layer being ironed

**Key:** `ironing_type`

**Type:** `Enum`

**Default** `NoIroning`

**Enum values:**


### Example

```json
"ironing_type": "topmost"
```


## Line width

[No documentation provided]

**Key:** `line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"line_width": "1%"
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
"make_overhang_printable_angle": 54.32
```


## Make overhang printable hole area

Maximum area of a hole in the base of the model before it's filled by conical material.A value of 0 will fill all the holes in the model base.

**Key:** `make_overhang_printable_hole_size`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"make_overhang_printable_hole_size": 1.37
```


## Max bridge length

Max length of bridges that don't need support. Set it to 0 if you want all bridges to be supported, and set it to a very large value if you don't want any bridges to be supported.

**Key:** `max_bridge_length`

**Type:** `Float`

**Min:** `0`

**Default** `10`

### Example

```json
"max_bridge_length": 11.65
```


## Avoid crossing wall - Max detour length

Maximum detour distance for avoiding crossing wall. Don't detour if the detour distance is large than this value. Detour length could be specified either as an absolute value or as percentage (for example 50%) of a direct travel path. Zero to disable

**Key:** `max_travel_detour_distance`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `0.0`

### Example

```json
"max_travel_detour_distance": "4%"
```


## Extrusion rate smoothing

[No documentation provided]

**Key:** `max_volumetric_extrusion_rate_slope`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"max_volumetric_extrusion_rate_slope": 0.62
```


## Smoothing segment length

[No documentation provided]

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
"min_bead_width": "106%"
```


## Minimum feature size

Minimum thickness of thin features. Model features that are thinner than this value will not be printed, while features thicker than the Minimum feature size will be widened to the Minimum wall width. It's expressed as a percentage over nozzle diameter

**Key:** `min_feature_size`

**Type:** `Percent`

**Min:** `0`

**Default** `25`

### Example

```json
"min_feature_size": "22%"
```


## One wall threshold

[No documentation provided]

**Key:** `min_width_top_surface`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `300%`

### Example

```json
"min_width_top_surface": "285%"
```


## Minimum sparse infill threshold

Sparse infill area which is smaller than threshold value is replaced by internal solid infill

**Key:** `minimum_sparse_infill_area`

**Type:** `Float`

**Min:** `0`

**Default** `15`

### Example

```json
"minimum_sparse_infill_area": 13.11
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
"only_one_wall_top": false
```


## Ooze prevention

[No documentation provided]

**Key:** `ooze_prevention`

**Type:** `Bool`

**Default** `false`

### Example

```json
"ooze_prevention": false
```


## Outer wall acceleration

Acceleration of outer wall. Using a lower value can improve quality

**Key:** `outer_wall_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `500`

### Example

```json
"outer_wall_acceleration": 493.58
```


## Outer wall jerk

Jerk of outer walls

**Key:** `outer_wall_jerk`

**Type:** `Float`

**Min:** `0`

**Default** `9`

### Example

```json
"outer_wall_jerk": 10.47
```


## Outer wall line width

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


## Outer wall speed

Speed of outer wall which is outermost and visible. It's used to be slower than inner wall speed to get better quality.

**Key:** `outer_wall_speed`

**Type:** `Float`

**Min:** `1`

**Default** `60`

### Example

```json
"outer_wall_speed": 58.66
```


## (10%, 25%)

[No documentation provided]

**Key:** `overhang_1_4_speed`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `0.0`

### Example

```json
"overhang_1_4_speed": 0.95
```


## [25%, 50%)

[No documentation provided]

**Key:** `overhang_2_4_speed`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `0.0`

### Example

```json
"overhang_2_4_speed": "3%"
```


## [50%, 75%)

Speed for line of wall which has degree of overhang between 50% and 75% line width. 0 means using original wall speed

**Key:** `overhang_3_4_speed`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `0.0`

### Example

```json
"overhang_3_4_speed": "1%"
```


## [75%, 100%)

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
"overhang_reverse_threshold": "48%"
```


## Classic mode

Enable this option to use classic mode

**Key:** `overhang_speed_classic`

**Type:** `Bool`

**Default** `false`

### Example

```json
"overhang_speed_classic": false
```


## Post-processing Scripts

If you want to process the output G-code through custom scripts, just list their absolute paths here. Separate multiple scripts with a semicolon. Scripts will be passed the absolute path to the G-code file as the first argument, and they can access the Slic3r config settings by reading environment variables.

**Key:** `post_process`

**Type:** `Strings`

**Default** `[""]`

### Example

```json
"post_process": [
    "",
    "",
    ""
  ]
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


## Prime tower brim width

Brim width

**Key:** `prime_tower_brim_width`

**Type:** `Float`

**Min:** `0`

**Default** `3.0`

### Example

```json
"prime_tower_brim_width": 3.48
```


## Prime tower width

Width of prime tower

**Key:** `prime_tower_width`

**Type:** `Float`

**Min:** `2`

**Default** `60.0`

### Example

```json
"prime_tower_width": 45.19
```


## Prime volume

The volume of material to prime extruder on tower.

**Key:** `prime_volume`

**Type:** `Float`

**Min:** `1`

**Default** `45.0`

### Example

```json
"prime_volume": 53.02
```


## Print flow ratio

The material may have volumetric change after switching between molten state and crystalline state. This setting changes all extrusion flow of this filament in gcode proportionally. Recommended value range is between 0.95 and 1.05. Maybe you can tune this value to get nice flat surface when there has slight overflow or underflow

**Key:** `print_flow_ratio`

**Type:** `Float`

**Min:** `0`

**Max:** `2`

**Default** `1`

### Example

```json
"print_flow_ratio": 0.9
```


## Print sequence

Print sequence, layer by layer or object by object

**Key:** `print_sequence`

**Type:** `Enum`

**Default** `ByLayer`

**Enum values:**


### Example

```json
"print_sequence": "by layer"
```


## Raft contact Z distance

Z gap between object and raft. Ignored for soluble interface

**Key:** `raft_contact_distance`

**Type:** `Float`

**Min:** `0`

**Default** `0.1`

### Example

```json
"raft_contact_distance": 0.11
```


## Raft expansion

Expand all raft layers in XY plane

**Key:** `raft_expansion`

**Type:** `Float`

**Min:** `0`

**Default** `1.5`

### Example

```json
"raft_expansion": 1.26
```


## Initial layer density

Density of the first raft or support layer

**Key:** `raft_first_layer_density`

**Type:** `Percent`

**Min:** `10`

**Max:** `100`

**Default** `90`

### Example

```json
"raft_first_layer_density": "89%"
```


## Initial layer expansion

Expand the first raft or support layer to improve bed plate adhesion

**Key:** `raft_first_layer_expansion`

**Type:** `Float`

**Min:** `0`

**Default** ``

### Example

```json
"raft_first_layer_expansion": 2.17
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
"reduce_crossing_wall": true
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
"seam_gap": "12%"
```


## Seam position

The start position to print each part of outer wall

**Key:** `seam_position`

**Type:** `Enum`

**Default** `Aligned`

**Enum values:**


### Example

```json
"seam_position": "random"
```


## Prime all printing extruders

If enabled, all printing extruders will be primed at the front edge of the print bed at the start of the print.

**Key:** `single_extruder_multi_material_priming`

**Type:** `Bool`

**Default** `true`

### Example

```json
"single_extruder_multi_material_priming": true
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
"skirt_distance": 2.15
```


## Skirt height

How many layers of skirt. Usually only one layer

**Key:** `skirt_height`

**Type:** `Int`

**Max:** `10000`

**Default** `1`

### Example

```json
"skirt_height": 1
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
"skirt_loops": 1
```


## Skirt speed

Speed of skirt, in mm/s. Zero means use default layer extrusion speed.

**Key:** `skirt_speed`

**Type:** `Float`

**Min:** `0`

**Default** `50.0`

### Example

```json
"skirt_speed": 51.26
```


## Slicing Mode

Use \"Even-odd\" for 3DLabPrint airplane models. Use \"Close holes\" to close all holes in the model.

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


## Small perimeters

This separate setting will affect the speed of perimeters having radius <= small_perimeter_threshold (usually holes). If expressed as percentage (for example: 80%) it will be calculated on the outer wall speed setting above. Set to zero for auto.

**Key:** `small_perimeter_speed`

**Type:** `FloatOrPercent`

**Min:** `1`

**Default** `50%`

### Example

```json
"small_perimeter_speed": "40%"
```


## Small perimeters threshold

This sets the threshold for small perimeter length. Default threshold is 0mm

**Key:** `small_perimeter_threshold`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"small_perimeter_threshold": 0.19
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


## Sparse infill acceleration

Acceleration of sparse infill. If the value is expressed as a percentage (e.g. 100%), it will be calculated based on the default acceleration.

**Key:** `sparse_infill_acceleration`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `100%`

### Example

```json
"sparse_infill_acceleration": "102%"
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
"sparse_infill_density": "23%"
```


## Sparse infill filament

Filament to print internal sparse infill.

**Key:** `sparse_infill_filament`

**Type:** `Int`

**Min:** `1`

**Default** `1`

### Example

```json
"sparse_infill_filament": 1
```


## Sparse infill line width

Line width of internal sparse infill. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `sparse_infill_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"sparse_infill_line_width": "2%"
```


## Sparse infill pattern

Line pattern for internal sparse infill

**Key:** `sparse_infill_pattern`

**Type:** `Enum`

**Default** `Cubic`

**Enum values:**


### Example

```json
"sparse_infill_pattern": "3dhoneycomb"
```


## Sparse infill speed

Speed of internal sparse infill

**Key:** `sparse_infill_speed`

**Type:** `Float`

**Min:** `1`

**Default** `100`

### Example

```json
"sparse_infill_speed": 105.62
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

[No documentation provided]

**Key:** `standby_temperature_delta`

**Type:** `Int`

**Min:** `0`

**Max:** `0`

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
"support_angle": 1.5
```


## Base pattern

Line pattern of support

**Key:** `support_base_pattern`

**Type:** `Enum`

**Default** `Rectilinear`

**Enum values:**


### Example

```json
"support_base_pattern": "rectilinear"
```


## Base pattern spacing

Spacing between support lines

**Key:** `support_base_pattern_spacing`

**Type:** `Float`

**Min:** `0`

**Default** `2.5`

### Example

```json
"support_base_pattern_spacing": 2.69
```


## Bottom interface spacing

Spacing of bottom interface lines. Zero means solid interface

**Key:** `support_bottom_interface_spacing`

**Type:** `Float`

**Min:** `0`

**Default** `0.5`

### Example

```json
"support_bottom_interface_spacing": 0.4
```


## Bottom Z distance

The z gap between the bottom support interface and object

**Key:** `support_bottom_z_distance`

**Type:** `Float`

**Default** `0.2`

### Example

```json
"support_bottom_z_distance": 0.23
```


## Support critical regions only

Only create support for critical regions including sharp tail, cantilever, etc.

**Key:** `support_critical_regions_only`

**Type:** `Bool`

**Default** `false`

### Example

```json
"support_critical_regions_only": false
```


## Normal Support expansion

Expand (+) or shrink (-) the horizontal span of normal support

**Key:** `support_expansion`

**Type:** `Float`

**Default** `0`

### Example

```json
"support_expansion": 0.62
```


## Support/raft base

[No documentation provided]

**Key:** `support_filament`

**Type:** `Int`

**Min:** `0`

**Default** `1`

### Example

```json
"support_filament": 1
```


## Bottom interface layers

[No documentation provided]

**Key:** `support_interface_bottom_layers`

**Type:** `Int`

**Min:** `-1`

**Default** `0`

**Enum values:**


### Example

```json
"support_interface_bottom_layers": 0
```


## Support/raft interface

[No documentation provided]

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
"support_interface_pattern": "rectilinear"
```


## Top interface spacing

Spacing of interface lines. Zero means solid interface

**Key:** `support_interface_spacing`

**Type:** `Float`

**Min:** `0`

**Default** `0.5`

### Example

```json
"support_interface_spacing": 0.62
```


## Support interface

Speed of support interface

**Key:** `support_interface_speed`

**Type:** `Float`

**Min:** `1`

**Default** `80`

### Example

```json
"support_interface_speed": 60.16
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
"support_interface_top_layers": 2
```


## Support line width

Line width of support. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `support_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"support_line_width": 0.95
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
"support_object_xy_distance": 0.42
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


## Support speed

Speed of support

**Key:** `support_speed`

**Type:** `Float`

**Min:** `1`

**Default** `80`

### Example

```json
"support_speed": 99.45
```


## Support style

Style and shape of the support. For normal support, projecting the supports into a regular grid will create more stable supports (default), while snug support towers will save material and reduce object scarring.\nFor tree support, slim and organic style will merge branches more aggressively and save a lot of material (default organic), while hybrid style will create similar structure to normal support under large flat overhangs.

**Key:** `support_style`

**Type:** `Enum`

**Default** `Default`

**Enum values:**


### Example

```json
"support_style": "organic"
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
"support_threshold_angle": 31
```


## Top Z distance

The z gap between the top support interface and object

**Key:** `support_top_z_distance`

**Type:** `Float`

**Default** `0.2`

### Example

```json
"support_top_z_distance": 0.19
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
"thick_bridges": false
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
"top_shell_thickness": 0.72
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
"top_solid_infill_flow_ratio": 0.79
```


## Top surface acceleration

Acceleration of top surface infill. Using a lower value may improve top surface quality

**Key:** `top_surface_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `500`

### Example

```json
"top_surface_acceleration": 378.9
```


## Top surface jerk

Jerk for top surface

**Key:** `top_surface_jerk`

**Type:** `Float`

**Min:** `1`

**Default** `9`

### Example

```json
"top_surface_jerk": 7.01
```


## Top surface line width

Line width for top surfaces. If expressed as a %, it will be computed over the nozzle diameter.

**Key:** `top_surface_line_width`

**Type:** `FloatOrPercent`

**Min:** `0`

**Max:** `1000`

**Default** `0.0`

### Example

```json
"top_surface_line_width": "4%"
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


## Top surface speed

Speed of top surface infill which is solid

**Key:** `top_surface_speed`

**Type:** `Float`

**Min:** `1`

**Default** `100`

### Example

```json
"top_surface_speed": 90.03
```


## Travel acceleration

Acceleration of travel moves

**Key:** `travel_acceleration`

**Type:** `Float`

**Min:** `0`

**Default** `10000`

### Example

```json
"travel_acceleration": 8288.41
```


## Travel jerk

Jerk for travel

**Key:** `travel_jerk`

**Type:** `Float`

**Min:** `1`

**Default** `12`

### Example

```json
"travel_jerk": 13.12
```


## Travel speed

Speed of travel which is faster and without extrusion

**Key:** `travel_speed`

**Type:** `Float`

**Min:** `1`

**Default** `120`

### Example

```json
"travel_speed": 111.97
```


## Z travel speed

[No documentation provided]

**Key:** `travel_speed_z`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"travel_speed_z": 0.01
```


## Tree support adaptive layer height

Enabling this option means the height of  tree support layer except the first will be automatically calculated

**Key:** `tree_support_adaptive_layer_height`

**Type:** `Bool`

**Default** `true`

### Example

```json
"tree_support_adaptive_layer_height": true
```


## Preferred Branch Angle

[No documentation provided]

**Key:** `tree_support_angle_slow`

**Type:** `Float`

**Min:** `10`

**Max:** `85`

**Default** `25`

### Example

```json
"tree_support_angle_slow": 31.24
```


## Auto brim width

Enabling this option means the width of the brim for tree support will be automatically calculated

**Key:** `tree_support_auto_brim`

**Type:** `Bool`

**Default** `true`

### Example

```json
"tree_support_auto_brim": false
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
"tree_support_branch_angle": 39.36
```


## Tree support branch angle organic

This setting determines the maximum overhang angle that t he branches of tree support allowed to make.If the angle is increased, the branches can be printed more horizontally, allowing them to reach farther.

**Key:** `tree_support_branch_angle_organic`

**Type:** `Float`

**Min:** `0`

**Max:** `60`

**Default** `40.0`

### Example

```json
"tree_support_branch_angle_organic": 43.18
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
"tree_support_branch_diameter": 4.52
```


## Tree support branch diameter angle

[No documentation provided]

**Key:** `tree_support_branch_diameter_angle`

**Type:** `Float`

**Min:** `0`

**Max:** `15`

**Default** `5`

### Example

```json
"tree_support_branch_diameter_angle": 3.97
```


## Branch Diameter with double walls

[No documentation provided]

**Key:** `tree_support_branch_diameter_double_wall`

**Type:** `Float`

**Min:** `0`

**Max:** `100`

**Default** `3.0`

### Example

```json
"tree_support_branch_diameter_double_wall": 3.2
```


## Tree support branch diameter organic

This setting determines the initial diameter of support nodes.

**Key:** `tree_support_branch_diameter_organic`

**Type:** `Float`

**Min:** `1`

**Max:** `10`

**Default** `2.0`

### Example

```json
"tree_support_branch_diameter_organic": 1.58
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
"tree_support_branch_distance": 5.58
```


## Tree support branch distance organic

This setting determines the distance between neighboring tree support nodes.

**Key:** `tree_support_branch_distance_organic`

**Type:** `Float`

**Min:** `1`

**Max:** `10`

**Default** `1.0`

### Example

```json
"tree_support_branch_distance_organic": 1.09
```


## Tree support brim width

Distance from tree branch to the outermost brim line

**Key:** `tree_support_brim_width`

**Type:** `Float`

**Min:** `0`

**Default** `3`

### Example

```json
"tree_support_brim_width": 2.73
```


## Tip Diameter

[No documentation provided]

**Key:** `tree_support_tip_diameter`

**Type:** `Float`

**Min:** `0`

**Max:** `100`

**Default** `0.8`

### Example

```json
"tree_support_tip_diameter": 0.65
```


## Branch Density

[No documentation provided]

**Key:** `tree_support_top_rate`

**Type:** `Percent`

**Min:** `5`

**Default** `30`

### Example

```json
"tree_support_top_rate": "33%"
```


## Tree support wall loops

This setting specify the count of walls around tree support

**Key:** `tree_support_wall_count`

**Type:** `Int`

**Min:** `0`

**Default** `1`

### Example

```json
"tree_support_wall_count": 1
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
"wall_infill_order": "inner-outer-inner wall/infill"
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
"wall_transition_angle": 7.84
```


## Wall transitioning filter margin

Prevent transitioning back and forth between one extra wall and one less. This margin extends the range of extrusion widths which follow to [Minimum wall width - margin, 2 * Minimum wall width + margin]. Increasing this margin reduces the number of transitions, which reduces the number of extrusion starts/stops and travel time. However, large extrusion width variation can lead to under- or overextrusion problems. It's expressed as a percentage over nozzle diameter

**Key:** `wall_transition_filter_deviation`

**Type:** `Percent`

**Min:** `0`

**Default** `25`

### Example

```json
"wall_transition_filter_deviation": "19%"
```


## Wall transition length

When transitioning between different numbers of walls as the part becomes thinner, a certain amount of space is allotted to split or join the wall segments. It's expressed as a percentage over nozzle diameter

**Key:** `wall_transition_length`

**Type:** `Percent`

**Min:** `0`

**Default** `100`

### Example

```json
"wall_transition_length": "104%"
```


## Wipe on loops

To minimize the visibility of the seam in a closed loop extrusion, a small inward movement is executed before the extruder leaves the loop.

**Key:** `wipe_on_loops`

**Type:** `Bool`

**Default** `false`

### Example

```json
"wipe_on_loops": true
```


## Wipe speed

The wipe speed is determined by the speed setting specified in this configuration.If the value is expressed as a percentage (e.g. 80%), it will be calculated based on the travel speed setting above.The default value for this parameter is 80%

**Key:** `wipe_speed`

**Type:** `FloatOrPercent`

**Min:** `0`

**Default** `80%`

### Example

```json
"wipe_speed": "76%"
```


## Maximal bridging distance

Maximal distance between supports on sparse infill sections.

**Key:** `wipe_tower_bridging`

**Type:** `Float`

**Default** `10.0`

### Example

```json
"wipe_tower_bridging": 11.31
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
"wipe_tower_cone_angle": 0.48
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
"wipe_tower_extra_spacing": "118%"
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
"wipe_tower_rotation_angle": 2.91
```


## Purging volumes - load/unload volumes

This vector saves required volumes to change from/to each tool used on the wipe tower. These values are used to simplify creation of the full purging volumes below.

**Key:** `wiping_volumes_extruders`

**Type:** `Floats`

**Default** `[70.0, 70.0, 70.0, 70.0, 70.0, 70.0, 70.0, 70.0, 70.0, 70.0]`

### Example

```json
"wiping_volumes_extruders": [
    73.5,
    73.0,
    70.26
  ]
```


## X-Y contour compensation

Contour of object will be grown or shrunk in XY plane by the configured value. Positive value makes contour bigger. Negative value makes contour smaller. This function is used to adjust size slightly when the object has assembling issue

**Key:** `xy_contour_compensation`

**Type:** `Float`

**Default** `0`

### Example

```json
"xy_contour_compensation": 1.62
```


## X-Y hole compensation

Holes of object will be grown or shrunk in XY plane by the configured value. Positive value makes holes bigger. Negative value makes holes smaller. This function is used to adjust size slightly when the object has assembling issue

**Key:** `xy_hole_compensation`

**Type:** `Float`

**Default** `0`

### Example

```json
"xy_hole_compensation": 3.33
```
