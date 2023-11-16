---
layout: default
title: "SLA Print"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Print"
---

Configuration options for a configuration file in the `sla_print` directory. No examples provided, as there are not currently any built-in profiles for SLA printers.

## Default sla print profile

[No documentation provided]

**Key:** `default_sla_print_profile`

**Type:** `String`

**Default** ``

### Example

```json
"default_sla_print_profile": ""
```


## Faded layers

[No documentation provided]

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
"filename_format": ""
```


## Hollowing closing distance

[No documentation provided]

**Key:** `hollowing_closing_distance`

**Type:** `Float`

**Min:** `0`

**Max:** `10`

**Default** `2.0`

### Example

```json
"hollowing_closing_distance": 1.61
```


## Hollowing enable

[No documentation provided]

**Key:** `hollowing_enable`

**Type:** `Bool`

**Default** `false`

### Example

```json
"hollowing_enable": false
```


## Hollowing min thickness

[No documentation provided]

**Key:** `hollowing_min_thickness`

**Type:** `Float`

**Min:** `1`

**Max:** `10`

**Default** `3.0`

### Example

```json
"hollowing_min_thickness": 3.65
```


## Hollowing quality

[No documentation provided]

**Key:** `hollowing_quality`

**Type:** `Float`

**Min:** `0`

**Max:** `1`

**Default** `0.5`

### Example

```json
"hollowing_quality": 0.46
```


## Layer height

Slicing height for each layer. Smaller layer height means more accurate and more printing time

**Key:** `layer_height`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"layer_height": 0.22
```


## Pad around object

[No documentation provided]

**Key:** `pad_around_object`

**Type:** `Bool`

**Default** `false`

### Example

```json
"pad_around_object": false
```


## Pad around object everywhere

[No documentation provided]

**Key:** `pad_around_object_everywhere`

**Type:** `Bool`

**Default** `false`

### Example

```json
"pad_around_object_everywhere": true
```


## Pad brim size

[No documentation provided]

**Key:** `pad_brim_size`

**Type:** `Float`

**Min:** `0`

**Max:** `30`

**Default** `1.6`

### Example

```json
"pad_brim_size": 1.45
```


## Pad enable

[No documentation provided]

**Key:** `pad_enable`

**Type:** `Bool`

**Default** `true`

### Example

```json
"pad_enable": true
```


## Pad max merge distance

[No documentation provided]

**Key:** `pad_max_merge_distance`

**Type:** `Float`

**Min:** `0`

**Default** `50.0`

### Example

```json
"pad_max_merge_distance": 39.06
```


## Pad object connector penetration

[No documentation provided]

**Key:** `pad_object_connector_penetration`

**Type:** `Float`

**Min:** `0`

**Default** `0.3`

### Example

```json
"pad_object_connector_penetration": 0.24
```


## Pad object connector stride

[No documentation provided]

**Key:** `pad_object_connector_stride`

**Type:** `Float`

**Min:** `0`

**Default** `10`

### Example

```json
"pad_object_connector_stride": 12.1
```


## Pad object connector width

[No documentation provided]

**Key:** `pad_object_connector_width`

**Type:** `Float`

**Min:** `0`

**Default** `0.5`

### Example

```json
"pad_object_connector_width": 0.49
```


## Pad object gap

[No documentation provided]

**Key:** `pad_object_gap`

**Type:** `Float`

**Min:** `0`

**Max:** `10`

**Default** `1`

### Example

```json
"pad_object_gap": 1.14
```


## Pad wall height

[No documentation provided]

**Key:** `pad_wall_height`

**Type:** `Float`

**Min:** `0`

**Max:** `30`

**Default** `0.0`

### Example

```json
"pad_wall_height": 3.77
```


## Pad wall slope

[No documentation provided]

**Key:** `pad_wall_slope`

**Type:** `Float`

**Min:** `45`

**Max:** `90`

**Default** `90.0`

### Example

```json
"pad_wall_slope": 70.16
```


## Pad wall thickness

[No documentation provided]

**Key:** `pad_wall_thickness`

**Type:** `Float`

**Min:** `0`

**Max:** `30`

**Default** `2.0`

### Example

```json
"pad_wall_thickness": 1.6
```


## Slice gap closing radius

Cracks smaller than 2x gap closing radius are being filled during the triangle mesh slicing. The gap closing operation may reduce the final print resolution, therefore it is advisable to keep the value reasonably low.

**Key:** `slice_closing_radius`

**Type:** `Float`

**Min:** `0`

**Default** `0.049`

### Example

```json
"slice_closing_radius": 0.06
```


## Support base diameter

[No documentation provided]

**Key:** `support_base_diameter`

**Type:** `Float`

**Min:** `0`

**Max:** `30`

**Default** `4.0`

### Example

```json
"support_base_diameter": 4.88
```


## Support base height

[No documentation provided]

**Key:** `support_base_height`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"support_base_height": 1.21
```


## Support base safety distance

[No documentation provided]

**Key:** `support_base_safety_distance`

**Type:** `Float`

**Min:** `0`

**Max:** `10`

**Default** `1`

### Example

```json
"support_base_safety_distance": 0.82
```


## Support buildplate only

[No documentation provided]

**Key:** `support_buildplate_only`

**Type:** `Bool`

**Default** `false`

### Example

```json
"support_buildplate_only": true
```


## Support critical angle

[No documentation provided]

**Key:** `support_critical_angle`

**Type:** `Float`

**Min:** `0`

**Max:** `90`

**Default** `45`

### Example

```json
"support_critical_angle": 40.51
```


## Support head front diameter

[No documentation provided]

**Key:** `support_head_front_diameter`

**Type:** `Float`

**Min:** `0`

**Default** `0.4`

### Example

```json
"support_head_front_diameter": 0.38
```


## Support head penetration

[No documentation provided]

**Key:** `support_head_penetration`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"support_head_penetration": 0.2
```


## Support head width

[No documentation provided]

**Key:** `support_head_width`

**Type:** `Float`

**Min:** `0`

**Max:** `20`

**Default** `1.0`

### Example

```json
"support_head_width": 1.22
```


## Support max bridge length

[No documentation provided]

**Key:** `support_max_bridge_length`

**Type:** `Float`

**Min:** `0`

**Default** `15.0`

### Example

```json
"support_max_bridge_length": 11.56
```


## Support max bridges on pillar

[No documentation provided]

**Key:** `support_max_bridges_on_pillar`

**Type:** `Int`

**Min:** `0`

**Max:** `50`

**Default** `3`

### Example

```json
"support_max_bridges_on_pillar": 3
```


## Support max pillar link distance

[No documentation provided]

**Key:** `support_max_pillar_link_distance`

**Type:** `Float`

**Min:** `0`

**Default** `10.0`

### Example

```json
"support_max_pillar_link_distance": 9.66
```


## Support object elevation

[No documentation provided]

**Key:** `support_object_elevation`

**Type:** `Float`

**Min:** `0`

**Max:** `150`

**Default** `5.0`

### Example

```json
"support_object_elevation": 5.93
```


## Support pillar connection mode

[No documentation provided]

**Key:** `support_pillar_connection_mode`

**Type:** `Enum`

**Default** `slapcmDynamic`

**Enum values:**


### Example

```json
"support_pillar_connection_mode": "cross"
```


## Support pillar diameter

[No documentation provided]

**Key:** `support_pillar_diameter`

**Type:** `Float`

**Min:** `0`

**Max:** `15`

**Default** `1.0`

### Example

```json
"support_pillar_diameter": 1.1
```


## Support pillar widening factor

[No documentation provided]

**Key:** `support_pillar_widening_factor`

**Type:** `Float`

**Min:** `0`

**Max:** `1`

**Default** `0.0`

### Example

```json
"support_pillar_widening_factor": 1
```


## Support points density relative

[No documentation provided]

**Key:** `support_points_density_relative`

**Type:** `Int`

**Min:** `0`

**Default** `100`

### Example

```json
"support_points_density_relative": 93
```


## Support points minimal distance

[No documentation provided]

**Key:** `support_points_minimal_distance`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"support_points_minimal_distance": 1.09
```


## Support small pillar diameter percent

[No documentation provided]

**Key:** `support_small_pillar_diameter_percent`

**Type:** `Percent`

**Min:** `1`

**Max:** `100`

**Default** `50`

### Example

```json
"support_small_pillar_diameter_percent": "55%"
```


## Supports enable

[No documentation provided]

**Key:** `supports_enable`

**Type:** `Bool`

**Default** `true`

### Example

```json
"supports_enable": true
```
