---
layout: default
title: "SLA Print"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Print"
---

Configuration options for a configuration file in the `sla_print` directory. No examples provided, as there are not currently any built-in profiles for SLA printers.

## Default SLA print profile

Default print profile associated with the current printer profile. On selection of the current printer profile, this print profile will be activated.

**Key:** `default_sla_print_profile`

**Type:** `String`

**Default** ``

### Example

```json

```


## Faded layers

Number of the layers needed for the exposure time fade from initial exposure time to the exposure time

**Key:** `faded_layers`

**Type:** `Int`

**Min:** `3`

**Max:** `20`

**Default** `10`

### Example

```json
"faded_layers": 8
```


## Filename format

User can self-define the project file name when export

**Key:** `filename_format`

**Type:** `String`

**Default** `{input_filename_base}_{filament_type[0]}_{print_time}.gcode`

### Example

```json

```


## Hollowing closing distance

Hollowing is done in two steps: first, an imaginary interior is calculated deeper (offset plus the closing distance) in the object and then it's inflated back to the specified offset. A greater closing distance makes the interior more rounded. At zero, the interior will resemble the exterior the most.

**Key:** `hollowing_closing_distance`

**Type:** `Float`

**Min:** `0`

**Max:** `10`

**Default** `2.0`

### Example

```json
"hollowing_closing_distance": 1.92
```


## Enable hollowing

Hollow out a model to have an empty interior

**Key:** `hollowing_enable`

**Type:** `Bool`

**Default** `false`

### Example

```json
"hollowing_enable": false
```


## Hollowed model wall thickness

Minimum wall thickness of a hollowed model.

**Key:** `hollowing_min_thickness`

**Type:** `Float`

**Min:** `1`

**Max:** `10`

**Default** `3.0`

### Example

```json
"hollowing_min_thickness": 3.34
```


## Hollowing accuracy

Performance vs accuracy of calculation. Lower values may produce unwanted artifacts.

**Key:** `hollowing_quality`

**Type:** `Float`

**Min:** `0`

**Max:** `1`

**Default** `0.5`

### Example

```json
"hollowing_quality": 0.56
```


## Layer height

Slicing height for each layer. Smaller layer height means more accurate and more printing time

**Key:** `layer_height`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"layer_height": 0.1
```


## Pad around object

Create pad around object and ignore the support elevation

**Key:** `pad_around_object`

**Type:** `Bool`

**Default** `false`

### Example

```json
"pad_around_object": true
```


## Pad around object everywhere

Force pad around object everywhere

**Key:** `pad_around_object_everywhere`

**Type:** `Bool`

**Default** `false`

### Example

```json
"pad_around_object_everywhere": true
```


## Pad brim size

How far should the pad extend around the contained geometry

**Key:** `pad_brim_size`

**Type:** `Float`

**Min:** `0`

**Max:** `30`

**Default** `1.6`

### Example

```json
"pad_brim_size": 1.55
```


## Use pad

Add a pad underneath the supported model

**Key:** `pad_enable`

**Type:** `Bool`

**Default** `true`

### Example

```json
"pad_enable": true
```


## Max merge distance

Some objects can get along with a few smaller pads instead of a single big one. This parameter defines how far the center of two smaller pads should be. If they are closer, they will get merged into one pad.

**Key:** `pad_max_merge_distance`

**Type:** `Float`

**Min:** `0`

**Default** `50.0`

### Example

```json
"pad_max_merge_distance": 50
```


## Pad object connector penetration

How much should the tiny connectors penetrate into the model body.

**Key:** `pad_object_connector_penetration`

**Type:** `Float`

**Min:** `0`

**Default** `0.3`

### Example

```json
"pad_object_connector_penetration": 0.26
```


## Pad object connector stride

Distance between two connector sticks which connect the object and the generated pad.

**Key:** `pad_object_connector_stride`

**Type:** `Float`

**Min:** `0`

**Default** `10`

### Example

```json
"pad_object_connector_stride": 11.02
```


## Pad object connector width

Width of the connector sticks which connect the object and the generated pad.

**Key:** `pad_object_connector_width`

**Type:** `Float`

**Min:** `0`

**Default** `0.5`

### Example

```json
"pad_object_connector_width": 0.39
```


## Pad object gap

The gap between the object bottom and the generated pad in zero elevation mode.

**Key:** `pad_object_gap`

**Type:** `Float`

**Min:** `0`

**Max:** `10`

**Default** `1`

### Example

```json
"pad_object_gap": 0.76
```


## Pad wall height

Defines the pad cavity depth. Set to zero to disable the cavity. Be careful when enabling this feature, as some resins may produce an extreme suction effect inside the cavity, which makes peeling the print off the vat foil difficult.

**Key:** `pad_wall_height`

**Type:** `Float`

**Min:** `0`

**Max:** `30`

**Default** `0.0`

### Example

```json
"pad_wall_height": 0
```


## Pad wall slope

The slope of the pad wall relative to the bed plane. 90 degrees means straight walls.

**Key:** `pad_wall_slope`

**Type:** `Float`

**Min:** `45`

**Max:** `90`

**Default** `90.0`

### Example

```json
"pad_wall_slope": 45
```


## Pad wall thickness

The thickness of the pad and its optional cavity walls.

**Key:** `pad_wall_thickness`

**Type:** `Float`

**Min:** `0`

**Max:** `30`

**Default** `2.0`

### Example

```json
"pad_wall_thickness": 1
```


## Slice gap closing radius

Cracks smaller than 2x gap closing radius are being filled during the triangle mesh slicing. The gap closing operation may reduce the final print resolution, therefore it is advisable to keep the value reasonably low.

**Key:** `slice_closing_radius`

**Type:** `Float`

**Min:** `0`

**Default** `0.049`

### Example

```json
"slice_closing_radius": 0.005
```


## Support base diameter

Diameter in mm of the pillar base

**Key:** `support_base_diameter`

**Type:** `Float`

**Min:** `0`

**Max:** `30`

**Default** `4.0`

### Example

```json
"support_base_diameter": 3
```


## Support base height

The height of the pillar base cone

**Key:** `support_base_height`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"support_base_height": 1
```


## Support base safety distance

The minimum distance of the pillar base from the model in mm. Makes sense in zero elevation mode where a gap according to this parameter is inserted between the model and the pad.

**Key:** `support_base_safety_distance`

**Type:** `Float`

**Min:** `0`

**Max:** `10`

**Default** `1`

### Example

```json
"support_base_safety_distance": 1.2
```


## Support on build plate only

Only create support if it lies on a build plate. Don't create support on a print.

**Key:** `support_buildplate_only`

**Type:** `Bool`

**Default** `false`

### Example

```json
"support_buildplate_only": false
```


## Critical angle

The default angle for connecting support sticks and junctions.

**Key:** `support_critical_angle`

**Type:** `Float`

**Min:** `0`

**Max:** `90`

**Default** `45`

### Example

```json
"support_critical_angle": 45
```


## Pinhead front diameter

Diameter of the pointing side of the head

**Key:** `support_head_front_diameter`

**Type:** `Float`

**Min:** `0`

**Default** `0.4`

### Example

```json
"support_head_front_diameter": 0.6
```


## Head penetration

How much the pinhead has to penetrate the model surface

**Key:** `support_head_penetration`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"support_head_penetration": 0.4
```


## Pinhead width

Width from the back sphere center to the front sphere center

**Key:** `support_head_width`

**Type:** `Float`

**Min:** `0`

**Max:** `20`

**Default** `1.0`

### Example

```json
"support_head_width": 2
```


## Max bridge length

The max length of a bridge

**Key:** `support_max_bridge_length`

**Type:** `Float`

**Min:** `0`

**Default** `15.0`

### Example

```json
"support_max_bridge_length": 10
```


## Max bridges on a pillar

Maximum number of bridges that can be placed on a pillar. Bridges hold support point pinheads and connect to pillars as small branches.

**Key:** `support_max_bridges_on_pillar`

**Type:** `Int`

**Min:** `0`

**Max:** `50`

**Default** `3`

### Example

```json
"support_max_bridges_on_pillar": 2
```


## Max pillar linking distance

The max distance of two pillars to get linked with each other. A zero value will prohibit pillar cascading.

**Key:** `support_max_pillar_link_distance`

**Type:** `Float`

**Min:** `0`

**Default** `10.0`

### Example

```json
"support_max_pillar_link_distance": 11.09
```


## Object elevation

How much the supports should lift up the supported object. If "Pad around object" is enabled, this value is ignored.

**Key:** `support_object_elevation`

**Type:** `Float`

**Min:** `0`

**Max:** `150`

**Default** `5.0`

### Example

```json
"support_object_elevation": 5
```


## Controls the bridge type between two neighboring pillars. Can be zig-zag, cross (double zig-zag) or dynamic which will automatically switch between the first two depending on the distance of the two pillars.

[No documentation provided]

**Key:** `support_pillar_connection_mode`

**Type:** `Enum`

**Default** `dynamic`

**Enum values:**


### Example

```json
"support_pillar_connection_mode": "zigzag"
```


## Pillar diameter

Diameter in mm of the support pillars

**Key:** `support_pillar_diameter`

**Type:** `Float`

**Min:** `0`

**Max:** `15`

**Default** `1.0`

### Example

```json
"support_pillar_diameter": 1
```


## Pillar widening factor

Merging bridges or pillars into another pillars can increase the radius. Zero means no increase, one means full increase. The exact amount of increase is unspecified and canchange in the future.

**Key:** `support_pillar_widening_factor`

**Type:** `Float`

**Min:** `0`

**Max:** `1`

**Default** `0.0`

### Example

```json
"support_pillar_widening_factor": 0
```


## Support points density

This is a relative measure of support points density.

**Key:** `support_points_density_relative`

**Type:** `Int`

**Min:** `0`

**Default** `100`

### Example

```json
"support_points_density_relative": 83
```


## Minimal distance of the support points

No support points will be placed closer than this threshold.

**Key:** `support_points_minimal_distance`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"support_points_minimal_distance": 1.08
```


## Small pillar diameter percent

The percentage of smaller pillars compared to the normal pillar diameter which are used in problematic areas where a normal pilla cannot fit.

**Key:** `support_small_pillar_diameter_percent`

**Type:** `Percent`

**Min:** `1`

**Max:** `100`

**Default** `50`

### Example

```json
"support_small_pillar_diameter_percent": "60%"
```


## Generate supports

Generate supports for the models

**Key:** `supports_enable`

**Type:** `Bool`

**Default** `true`

### Example

```json
"supports_enable": true
```
