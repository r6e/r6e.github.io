---
layout: default
title: "SLA Printer"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Printer"
---

Configuration options for a configuration file for an SLA printer in the `machine` directory. No examples provided, as there are not currently any built-in profiles for SLA printers.

## absolute_correction

**Key:** `absolute_correction`

**Type:** `float`

**Default:** `0.0`

## area_fill

**Key:** `area_fill`

**Type:** `float`

**Default:** `50.0`

**Min:** `0`

## Bed custom model

**Key:** `bed_custom_model`

**Type:** `string`

**Default:** (empty)

## Bed custom texture

**Key:** `bed_custom_texture`

**Type:** `string`

**Default:** (empty)

## display_height

**Key:** `display_height`

**Type:** `float`

**Default:** `68.0`

**Min:** `1`

## display_mirror_x

**Key:** `display_mirror_x`

**Type:** `boolean`

**Default:** `true`

## display_mirror_y

**Key:** `display_mirror_y`

**Type:** `boolean`

**Default:** `null`

## display_orientation

**Key:** `display_orientation`

**Type:** `enum`

**Default:** `portrait`

**Values:**
* **Landscape**: `landscape`
* **Portrait**: `portrait`

## X

**Key:** `display_pixels_x`

**Type:** `integer`

**Default:** `2560`

**Min:** `100`

## Y

**Key:** `display_pixels_y`

**Type:** `integer`

**Default:** `1440`

**Min:** `100`

## display_width

**Key:** `display_width`

**Type:** `float`

**Default:** `120.0`

**Min:** `1`

## Elephant foot compensation

Shrink the initial layer on build plate to compensate for elephant foot effect

**Key:** `elefant_foot_compensation`

**Type:** `float`

**Default:** `0.0`

**Min:** `0`

## elefant_foot_min_width

**Key:** `elefant_foot_min_width`

**Type:** `float`

**Default:** `0.2`

**Min:** `0`

## fast_tilt_time

**Key:** `fast_tilt_time`

**Type:** `float`

**Default:** `5.0`

**Min:** `0`

## gamma_correction

**Key:** `gamma_correction`

**Type:** `float`

**Default:** `1.0`

**Max:** `1`

**Min:** `0`

## Inherits profile

Name of parent profile

**Key:** `inherits`

**Type:** `string`

**Default:** `null`

## max_exposure_time

**Key:** `max_exposure_time`

**Type:** `float`

**Default:** `100`

**Min:** `0`

## max_initial_exposure_time

**Key:** `max_initial_exposure_time`

**Type:** `float`

**Default:** `150`

**Min:** `0`

## min_exposure_time

**Key:** `min_exposure_time`

**Type:** `float`

**Default:** `0`

**Min:** `0`

## min_initial_exposure_time

**Key:** `min_initial_exposure_time`

**Type:** `float`

**Default:** `0`

**Min:** `0`

## Printable area

**Key:** `printable_area`

**Type:** `[[integer, integer]]`

**Default:** `[[0, 0], [200, 0], [200, 200], [0, 200]]`

## Printable height

Maximum printable height which is limited by mechanism of printer

**Key:** `printable_height`

**Type:** `float`

**Default:** `100.0`

**Max:** `2000`

**Min:** `0`

## Printer technology

Printer technology

**Key:** `printer_technology`

**Type:** `enum`

**Default:** `FFF`

**Values:**
* `FFF`
* `SLA`

## relative_correction

**Key:** `relative_correction`

**Type:** `[float]`

**Default:** `[1.0, 1.0]`

**Min:** `0`

## relative_correction_x

**Key:** `relative_correction_x`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## relative_correction_y

**Key:** `relative_correction_y`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## relative_correction_z

**Key:** `relative_correction_z`

**Type:** `float`

**Default:** `1.0`

**Min:** `0`

## slow_tilt_time

**Key:** `slow_tilt_time`

**Type:** `float`

**Default:** `8.0`

**Min:** `0`

