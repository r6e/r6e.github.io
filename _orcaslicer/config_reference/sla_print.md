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
"hollowing_closing_distance": 1.63
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
"hollowing_min_thickness": 2.96
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
"hollowing_quality": 0.57
```


## Layer height

Slicing height for each layer. Smaller layer height means more accurate and more printing time

**Key:** `layer_height`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"layer_height": 0.19
```


## Pad around object

[No documentation provided]

**Key:** `pad_around_object`

**Type:** `Bool`

**Default** `false`

### Example

```json
"pad_around_object": true
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
"pad_brim_size": 1.48
```


## Pad enable

[No documentation provided]

**Key:** `pad_enable`

**Type:** `Bool`

**Default** `true`

### Example

```json
"pad_enable": false
```


## Pad max merge distance

[No documentation provided]

**Key:** `pad_max_merge_distance`

**Type:** `Float`

**Min:** `0`

**Default** `50.0`

### Example

```json
"pad_max_merge_distance": 58.26
```


## Pad object connector penetration

[No documentation provided]

**Key:** `pad_object_connector_penetration`

**Type:** `Float`

**Min:** `0`

**Default** `0.3`

### Example

```json
"pad_object_connector_penetration": 0.26
```


## Pad object connector stride

[No documentation provided]

**Key:** `pad_object_connector_stride`

**Type:** `Float`

**Min:** `0`

**Default** `10`

### Example

```json
"pad_object_connector_stride": 10.1
```


## Pad object connector width

[No documentation provided]

**Key:** `pad_object_connector_width`

**Type:** `Float`

**Min:** `0`

**Default** `0.5`

### Example

```json
"pad_object_connector_width": 0.58
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
"pad_object_gap": 1.03
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
"pad_wall_height": 1.57
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
"pad_wall_slope": 81.94
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
"pad_wall_thickness": 2.44
```


## Slice gap closing radius

[No documentation provided]

**Key:** `slice_closing_radius`

**Type:** `Float`

**Min:** `0`

**Default** `0.049`

### Example

```json
"slice_closing_radius": 0.05
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
"support_base_diameter": 3.56
```


## Support base height

[No documentation provided]

**Key:** `support_base_height`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"support_base_height": 1.24
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
"support_base_safety_distance": 1.1
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
"support_critical_angle": 38.29
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
"support_head_penetration": 0.16
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
"support_head_width": 0.89
```


## Support max bridge length

[No documentation provided]

**Key:** `support_max_bridge_length`

**Type:** `Float`

**Min:** `0`

**Default** `15.0`

### Example

```json
"support_max_bridge_length": 18.05
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
"support_max_pillar_link_distance": 10.78
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
"support_object_elevation": 5.01
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
"support_pillar_diameter": 1.23
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
"support_pillar_widening_factor": 0
```


## Support points density relative

[No documentation provided]

**Key:** `support_points_density_relative`

**Type:** `Int`

**Min:** `0`

**Default** `100`

### Example

```json
"support_points_density_relative": 86
```


## Support points minimal distance

[No documentation provided]

**Key:** `support_points_minimal_distance`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"support_points_minimal_distance": 1.12
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
"support_small_pillar_diameter_percent": "56%"
```


## Supports enable

[No documentation provided]

**Key:** `supports_enable`

**Type:** `Bool`

**Default** `true`

### Example

```json
"supports_enable": false
```
