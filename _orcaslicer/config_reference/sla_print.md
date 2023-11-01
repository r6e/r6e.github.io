---
layout: default
title: "SLA Print"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Print"
---

Configuration options for a configuration file in the `sla_print` directory.

## Compatible machine

**Key:** `compatible_printers`

**Type:** `[string]`

**Default:** `null`

## Compatible machine condition

A boolean expression using the configuration values of an active printer profile. If this expression evaluates to true, this profile is considered compatible with the active printer profile.

**Key:** `compatible_printers_condition`

**Type:** `string`

**Default:** `null`

## default_sla_print_profile

**Key:** `default_sla_print_profile`

**Type:** `string`

**Default:** `null`

## faded_layers

**Key:** `faded_layers`

**Type:** `integer`

**Default:** `10`

**Max:** `20`

**Min:** `3`

## Filename format

User can self-define the project file name when export

**Key:** `filename_format`

**Type:** `string`

**Default:** `{input_filename_base}_{filament_type[0]}_{print_time}.gcode`

## hollowing_closing_distance

**Key:** `hollowing_closing_distance`

**Type:** `float`

**Default:** `2.0`

**Max:** `10`

**Min:** `0`

## hollowing_enable

**Key:** `hollowing_enable`

**Type:** `boolean`

**Default:** `null`

## hollowing_min_thickness

**Key:** `hollowing_min_thickness`

**Type:** `float`

**Default:** `3.0`

**Max:** `10`

**Min:** `1`

## hollowing_quality

**Key:** `hollowing_quality`

**Type:** `float`

**Default:** `0.5`

**Max:** `1`

**Min:** `0`

## Inherits profile

Name of parent profile

**Key:** `inherits`

**Type:** `string`

**Default:** `null`

## Layer height

Slicing height for each layer. Smaller layer height means more accurate and more printing time

**Key:** `layer_height`

**Type:** `float`

**Default:** `0.2`

**Min:** `0`

## pad_around_object

**Key:** `pad_around_object`

**Type:** `boolean`

**Default:** `null`

## pad_around_object_everywhere

**Key:** `pad_around_object_everywhere`

**Type:** `boolean`

**Default:** `null`

## pad_brim_size

**Key:** `pad_brim_size`

**Type:** `float`

**Default:** `1.6`

**Max:** `30`

**Min:** `0`

## pad_enable

**Key:** `pad_enable`

**Type:** `boolean`

**Default:** `true`

## pad_max_merge_distance

**Key:** `pad_max_merge_distance`

**Type:** `float`

**Default:** `50.0`

**Min:** `0`

## pad_object_connector_penetration

**Key:** `pad_object_connector_penetration`

**Type:** `float`

**Default:** `0.3`

**Min:** `0`

## pad_object_connector_stride

**Key:** `pad_object_connector_stride`

**Type:** `float`

**Default:** `10`

**Min:** `0`

## pad_object_connector_width

**Key:** `pad_object_connector_width`

**Type:** `float`

**Default:** `0.5`

**Min:** `0`

## pad_object_gap

**Key:** `pad_object_gap`

**Type:** `float`

**Default:** `1`

**Max:** `10`

**Min:** `0`

## pad_wall_height

**Key:** `pad_wall_height`

**Type:** `float`

**Default:** `0.0`

**Max:** `30`

**Min:** `0`

## pad_wall_slope

**Key:** `pad_wall_slope`

**Type:** `float`

**Default:** `90.0`

**Max:** `90`

**Min:** `45`

## pad_wall_thickness

**Key:** `pad_wall_thickness`

**Type:** `float`

**Default:** `2.0`

**Max:** `30`

**Min:** `0`

## Slice gap closing radius

Cracks smaller than 2x gap closing radius are being filled during the triangle mesh slicing. The gap closing operation may reduce the final print resolution, therefore it is advisable to keep the value reasonably low.

**Key:** `slice_closing_radius`

**Type:** `float`

**Default:** `0.049`

**Min:** `0`

## support_base_diameter

**Key:** `support_base_diameter`

**Type:** `float`

**Default:** `4.0`

**Max:** `30`

**Min:** `0`

## support_base_height

**Key:** `support_base_height`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## support_base_safety_distance

**Key:** `support_base_safety_distance`

**Type:** `float`

**Default:** `1`

**Max:** `10`

**Min:** `0`

## support_buildplate_only

**Key:** `support_buildplate_only`

**Type:** `boolean`

**Default:** `null`

## support_critical_angle

**Key:** `support_critical_angle`

**Type:** `float`

**Default:** `45`

**Max:** `90`

**Min:** `0`

## support_head_front_diameter

**Key:** `support_head_front_diameter`

**Type:** `float`

**Default:** `0.4`

**Min:** `0`

## support_head_penetration

**Key:** `support_head_penetration`

**Type:** `float`

**Default:** `0.2`

**Min:** `0`

## support_head_width

**Key:** `support_head_width`

**Type:** `float`

**Default:** `1.0`

**Max:** `20`

**Min:** `0`

## support_max_bridge_length

**Key:** `support_max_bridge_length`

**Type:** `float`

**Default:** `15.0`

**Min:** `0`

## support_max_bridges_on_pillar

**Key:** `support_max_bridges_on_pillar`

**Type:** `integer`

**Default:** `3`

**Max:** `50`

**Min:** `0`

## support_max_pillar_link_distance

**Key:** `support_max_pillar_link_distance`

**Type:** `float`

**Default:** `10.0`

**Min:** `0`

## support_object_elevation

**Key:** `support_object_elevation`

**Type:** `float`

**Default:** `5.0`

**Max:** `150`

**Min:** `0`

## support_pillar_connection_mode

**Key:** `support_pillar_connection_mode`

**Type:** `enum`

**Default:** `dynamic`

**Values:**
* **Zig-zag**: `zigzag`
* **Cross**: `cross`
* **Dynamic**: `dynamic`

## support_pillar_diameter

**Key:** `support_pillar_diameter`

**Type:** `float`

**Default:** `1.0`

**Max:** `15`

**Min:** `0`

## support_pillar_widening_factor

**Key:** `support_pillar_widening_factor`

**Type:** `float`

**Default:** `0.0`

**Max:** `1`

**Min:** `0`

## support_points_density_relative

**Key:** `support_points_density_relative`

**Type:** `integer`

**Default:** `100`

**Min:** `0`

## support_points_minimal_distance

**Key:** `support_points_minimal_distance`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## support_small_pillar_diameter_percent

**Key:** `support_small_pillar_diameter_percent`

**Type:** `percent`

**Default:** `50`

**Max:** `100`

**Min:** `1`

## supports_enable

**Key:** `supports_enable`

**Type:** `boolean`

**Default:** `true`

