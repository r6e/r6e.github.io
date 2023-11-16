---
layout: default
title: "SLA Printer"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Printer"
---

Configuration options for a configuration file for an SLA printer in the `machine` directory. No examples provided, as there are not currently any built-in profiles for SLA printers.

## Absolute correction

[No documentation provided]

**Key:** `absolute_correction`

**Type:** `Float`

**Default** `0.0`

### Example

```json
"absolute_correction": 2.94
```


## Area fill

[No documentation provided]

**Key:** `area_fill`

**Type:** `Float`

**Min:** `0`

**Default** `50.0`

### Example

```json
"area_fill": 53.51
```


## Bed custom model

[No documentation provided]

**Key:** `bed_custom_model`

**Type:** `String`

**Default** ``

### Example

```json
"bed_custom_model": ""
```


## Bed custom texture

[No documentation provided]

**Key:** `bed_custom_texture`

**Type:** `String`

**Default** ``

### Example

```json
"bed_custom_texture": ""
```


## Display height

[No documentation provided]

**Key:** `display_height`

**Type:** `Float`

**Min:** `1`

**Default** `68.0`

### Example

```json
"display_height": 73.48
```


## Display mirror x

[No documentation provided]

**Key:** `display_mirror_x`

**Type:** `Bool`

**Default** `true`

### Example

```json
"display_mirror_x": true
```


## Display mirror y

[No documentation provided]

**Key:** `display_mirror_y`

**Type:** `Bool`

**Default** `false`

### Example

```json
"display_mirror_y": false
```


## Display orientation

[No documentation provided]

**Key:** `display_orientation`

**Type:** `Enum`

**Default** `sladoPortrait`

**Enum values:**


### Example

```json
"display_orientation": "landscape"
```


## Display pixels (X)

[No documentation provided]

**Key:** `display_pixels_x`

**Type:** `Int`

**Min:** `100`

**Default** `2560`

### Example

```json
"display_pixels_x": 1930
```


## Display pixels (Y)

[No documentation provided]

**Key:** `display_pixels_y`

**Type:** `Int`

**Min:** `100`

**Default** `1440`

### Example

```json
"display_pixels_y": 1626
```


## Display width

[No documentation provided]

**Key:** `display_width`

**Type:** `Float`

**Min:** `1`

**Default** `120.0`

### Example

```json
"display_width": 138.5
```


## Elephant foot compensation

Shrink the initial layer on build plate to compensate for elephant foot effect

**Key:** `elefant_foot_compensation`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"elefant_foot_compensation": 1.28
```


## Elefant foot min width

[No documentation provided]

**Key:** `elefant_foot_min_width`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"elefant_foot_min_width": 0.23
```


## Fast tilt time

[No documentation provided]

**Key:** `fast_tilt_time`

**Type:** `Float`

**Min:** `0`

**Default** `5.0`

### Example

```json
"fast_tilt_time": 4.65
```


## Gamma correction

[No documentation provided]

**Key:** `gamma_correction`

**Type:** `Float`

**Min:** `0`

**Max:** `1`

**Default** `1.0`

### Example

```json
"gamma_correction": 0.78
```


## Inherits profile

Name of parent profile

**Key:** `inherits`

**Type:** `String`

**Default** ``

### Example

```json
"inherits": ""
```


## Max exposure time

[No documentation provided]

**Key:** `max_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `100`

### Example

```json
"max_exposure_time": 113.99
```


## Max initial exposure time

[No documentation provided]

**Key:** `max_initial_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `150`

### Example

```json
"max_initial_exposure_time": 164.77
```


## Min exposure time

[No documentation provided]

**Key:** `min_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"min_exposure_time": 3.09
```


## Min initial exposure time

[No documentation provided]

**Key:** `min_initial_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"min_initial_exposure_time": 0.2
```


## Printable area

[No documentation provided]

**Key:** `printable_area`

**Type:** `Points`

**Default** `[[0, 0], [200, 0], [200, 200], [0, 200]]`

### Example

```json
"printable_area": [
    [
      77.76,
      97.69
    ],
    [
      94.75,
      111.05
    ],
    [
      77.57,
      118.26
    ],
    [
      117.11,
      123.76
    ]
  ]
```


## Printable height

Maximum printable height which is limited by mechanism of printer

**Key:** `printable_height`

**Type:** `Float`

**Min:** `0`

**Max:** `2000`

**Default** `100.0`

### Example

```json
"printable_height": 118.32
```


## Printer technology

Printer technology

**Key:** `printer_technology`

**Type:** `Enum`

**Default** `FFF`

**Enum values:**


### Example

```json
"printer_technology": "SLA"
```


## Relative correction

[No documentation provided]

**Key:** `relative_correction`

**Type:** `Floats`

**Min:** `0`

**Default** `[1.0, 1.0]`

### Example

```json
"relative_correction": [
    0.77,
    0.96
  ]
```


## Relative correction x

[No documentation provided]

**Key:** `relative_correction_x`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"relative_correction_x": 1.14
```


## Relative correction y

[No documentation provided]

**Key:** `relative_correction_y`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"relative_correction_y": 0.98
```


## Relative correction z

[No documentation provided]

**Key:** `relative_correction_z`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"relative_correction_z": 1.14
```


## Slow tilt time

[No documentation provided]

**Key:** `slow_tilt_time`

**Type:** `Float`

**Min:** `0`

**Default** `8.0`

### Example

```json
"slow_tilt_time": 6.43
```
