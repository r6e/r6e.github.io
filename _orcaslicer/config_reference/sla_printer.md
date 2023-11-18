---
layout: default
title: "SLA Printer"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "SLA Printer"
---

Configuration options for a configuration file for an SLA printer in the `machine` directory. No examples provided, as there are not currently any built-in profiles for SLA printers.

## Printer absolute correction

Will inflate or deflate the sliced 2D polygons according to the sign of the correction.

**Key:** `absolute_correction`

**Type:** `Float`

**Default** `0.0`

### Example

```json
"absolute_correction": 0.18
```


## Area fill

The percentage of the bed area. 
If the print area exceeds the specified value, 
then a slow tilt will be used, otherwise - a fast tilt

**Key:** `area_fill`

**Type:** `Float`

**Min:** `0`

**Default** `50.0`

### Example

```json
"area_fill": 58.37
```


## Bed custom model

[No documentation provided]

**Key:** `bed_custom_model`

**Type:** `String`

**Default** ``

### Example

```json

```


## Bed custom texture

[No documentation provided]

**Key:** `bed_custom_texture`

**Type:** `String`

**Default** ``

### Example

```json

```


## Display height

Height of the display

**Key:** `display_height`

**Type:** `Float`

**Min:** `1`

**Default** `68.0`

### Example

```json
"display_height": 83.36
```


## Display horizontal mirroring

Enable horizontal mirroring of output images

**Key:** `display_mirror_x`

**Type:** `Bool`

**Default** `true`

### Example

```json
"display_mirror_x": false
```


## Display vertical mirroring

Enable vertical mirroring of output images

**Key:** `display_mirror_y`

**Type:** `Bool`

**Default** `false`

### Example

```json
"display_mirror_y": true
```


## Display orientation

Set the actual LCD display orientation inside the SLA printer. Portrait mode will flip the meaning of display width and height parameters and the output images will be rotated by 90 degrees.

**Key:** `display_orientation`

**Type:** `Enum`

**Default** `sladoPortrait`

**Enum values:**


### Example

```json
"display_orientation": "landscape"
```


## Display pixels (X)

Number of pixels in X dimension

**Key:** `display_pixels_x`

**Type:** `Int`

**Min:** `100`

**Default** `2560`

### Example

```json
"display_pixels_x": 1969
```


## Display pixels (Y)

Number of pixels in Y dimension

**Key:** `display_pixels_y`

**Type:** `Int`

**Min:** `100`

**Default** `1440`

### Example

```json
"display_pixels_y": 1389
```


## Display width

Width of the display

**Key:** `display_width`

**Type:** `Float`

**Min:** `1`

**Default** `120.0`

### Example

```json
"display_width": 129.9
```


## Elephant foot compensation

Shrink the initial layer on build plate to compensate for elephant foot effect

**Key:** `elefant_foot_compensation`

**Type:** `Float`

**Min:** `0`

**Default** `0.0`

### Example

```json
"elefant_foot_compensation": 4.97
```


## Elephant foot minimum width

Minimum width of features to maintain when doing elephant foot compensation.

**Key:** `elefant_foot_min_width`

**Type:** `Float`

**Min:** `0`

**Default** `0.2`

### Example

```json
"elefant_foot_min_width": 0.2
```


## Fast tilt

Time of the fast tilt

**Key:** `fast_tilt_time`

**Type:** `Float`

**Min:** `0`

**Default** `5.0`

### Example

```json
"fast_tilt_time": 4.5
```


## Printer gamma correction

This will apply a gamma correction to the rasterized 2D polygons. A gamma value of zero means thresholding with the threshold in the middle. This behaviour eliminates antialiasing without losing holes in polygons.

**Key:** `gamma_correction`

**Type:** `Float`

**Min:** `0`

**Max:** `1`

**Default** `1.0`

### Example

```json
"gamma_correction": 0.86
```


## Maximum exposure time

Maximum exposure time

**Key:** `max_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `100`

### Example

```json
"max_exposure_time": 90.72
```


## Maximum initial exposure time

Maximum initial exposure time

**Key:** `max_initial_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `150`

### Example

```json
"max_initial_exposure_time": 139.96
```


## Minimum exposure time

Minimum exposure time

**Key:** `min_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"min_exposure_time": 3.42
```


## Minimum initial exposure time

Minimum initial exposure time

**Key:** `min_initial_exposure_time`

**Type:** `Float`

**Min:** `0`

**Default** `0`

### Example

```json
"min_initial_exposure_time": 2.57
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
      81.51,
      120.54
    ],
    [
      88.77,
      83.36
    ],
    [
      75.94,
      96.4
    ],
    [
      82.48,
      107.86
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
"printable_height": 91.7
```


## Printer technology

Printer technology

**Key:** `printer_technology`

**Type:** `Enum`

**Default** `FFF`

**Enum values:**


### Example

```json
"printer_technology": "FFF"
```


## Printer scaling correction

Printer scaling correction

**Key:** `relative_correction`

**Type:** `Floats`

**Min:** `0`

**Default** `[1.0, 1.0]`

### Example

```json
"relative_correction": [
    0.9,
    0.76
  ]
```


## Printer scaling X axis correction

Printer scaling correction in X axis

**Key:** `relative_correction_x`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"relative_correction_x": 0.81
```


## Printer scaling Y axis correction

Printer scaling correction in Y axis

**Key:** `relative_correction_y`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"relative_correction_y": 1.23
```


## Printer scaling Z axis correction

Printer scaling correction in Z axis

**Key:** `relative_correction_z`

**Type:** `Float`

**Min:** `0`

**Default** `1.0`

### Example

```json
"relative_correction_z": 0.86
```


## Slow tilt

Time of the slow tilt

**Key:** `slow_tilt_time`

**Type:** `Float`

**Min:** `0`

**Default** `8.0`

### Example

```json
"slow_tilt_time": 7.92
```
