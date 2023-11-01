---
layout: default
title: "SLA Material"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Material"
---

Configuration options for a configuration file in the `sla_materials` directory.

## bottle_cost

**Key:** `bottle_cost`

**Type:** `float`

**Default:** `0.0`

**Min:** `0`

## bottle_volume

**Key:** `bottle_volume`

**Type:** `float`

**Default:** `1000.0`

**Min:** `50`

## bottle_weight

**Key:** `bottle_weight`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## Compatible machine

**Key:** `compatible_printers`

**Type:** `[string]`

**Default:** `null`

## Compatible machine condition

A boolean expression using the configuration values of an active printer profile. If this expression evaluates to true, this profile is considered compatible with the active printer profile.

**Key:** `compatible_printers_condition`

**Type:** `string`

**Default:** `null`

## Compatible process profiles

**Key:** `compatible_prints`

**Type:** `[string]`

**Default:** `null`

## Compatible process profiles condition

A boolean expression using the configuration values of an active print profile. If this expression evaluates to true, this profile is considered compatible with the active print profile.

**Key:** `compatible_prints_condition`

**Type:** `string`

**Default:** `null`

## default_sla_material_profile

**Key:** `default_sla_material_profile`

**Type:** `string`

**Default:** `null`

## exposure_time

**Key:** `exposure_time`

**Type:** `float`

**Default:** `10`

**Min:** `0`

## Inherits profile

Name of parent profile

**Key:** `inherits`

**Type:** `string`

**Default:** `null`

## initial_exposure_time

**Key:** `initial_exposure_time`

**Type:** `float`

**Default:** `15`

**Min:** `0`

## initial_layer_height

**Key:** `initial_layer_height`

**Type:** `float`

**Default:** `0.3`

**Min:** `0`

## material_colour

**Key:** `material_colour`

**Type:** `string`

**Default:** `#29B2B2`

## material_correction

**Key:** `material_correction`

**Type:** `[float]`

**Default:** `[1.0, 1.0, 1.0]`

**Min:** `0`

## material_correction_x

**Key:** `material_correction_x`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## material_correction_y

**Key:** `material_correction_y`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## material_correction_z

**Key:** `material_correction_z`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## material_density

**Key:** `material_density`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## material_print_speed

**Key:** `material_print_speed`

**Type:** `enum`

**Default:** `fast`

**Values:**
* **Slow**: `slow`
* **Fast**: `fast`

## material_type

**Key:** `material_type`

**Type:** `string`

**Default:** `Tough`

**Values:**
* `Tough`
* `Flexible`
* `Casting`
* `Dental`
* `Heat-resistant`

## material_vendor

**Key:** `material_vendor`

**Type:** `string`

**Default:** (empty)

