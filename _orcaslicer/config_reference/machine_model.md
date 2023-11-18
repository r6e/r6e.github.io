---
layout: default
title: "Machine Model"
date: "2023-10-31 18:00:00 -0600"
categories: "3D Printing"
category_title: "Machine Model"
---

Configuration options for a configuration file with `"type": "machine_model"`.

## Bed exclude area

Unprintable area in XY plane. For example, X1 Series printers use the front left corner to cut filament during filament change. The area is expressed as polygon by points in following format: "XxY, XxY, ..."

**Key:** `bed_exclude_area`

**Type:** `Points`

**Default** `[[0, 0]]`

### Example

```json
"bed_exclude_area": ["0x0"]
```


## Bed model

[No documentation provided]

**Key:** `bed_model`

**Type:** `String`

**Default** ``

### Example

```json
"bed_model": "gmax2_bed.stl"
```


## Bed texture

[No documentation provided]

**Key:** `bed_texture`

**Type:** `String`

**Default** ``

### Example

```json
"bed_texture": "biqu_b1_buildplate_texture.png"
```


## Default materials

[No documentation provided]

**Key:** `default_materials`

**Type:** `Strings`

**Default** ``

### Example

```json
"default_materials": "Comgrow Generic PLA;Comgrow Generic PETG;Comgrow Generic ABS"
```


## Extruders count

[No documentation provided]

**Key:** `extruders_count`

**Type:** `Int`

**Default** ``

### Example

```json
"extruders_count": 2
```


## Family

[No documentation provided]

**Key:** `family`

**Type:** `String`

**Default** ``

### Example

```json
"family": "Kingroon"
```


## Hotend model

[No documentation provided]

**Key:** `hotend_model`

**Type:** `String`

**Default** ``

### Example

```json
"hotend_model": "hotend.stl"
```


## Model id

[No documentation provided]

**Key:** `model_id`

**Type:** `String`

**Default** ``

### Example

```json
"model_id": "Voron_Switchwire_250"
```


## Nozzle diameter

Diameter of nozzle

**Key:** `nozzle_diameter`

**Type:** `Floats`

**Max:** `100`

**Default** `[0.4]`

### Example

```json
"nozzle_diameter": "0.4;0.6"
```


## Thumbnail

[No documentation provided]

**Key:** `thumbnail`

**Type:** `String`

**Default** ``

### Example

```json
"thumbnail": "MK4IS_thumbnail_v2.png"
```


## Model variants

Different variants of machine available, usually different nozzle sizes

**Key:** `variants`

**Type:** `Strings`

**Default** `[0.4]`

### Example

```json
"variants": "0.4; 0.6; 0.8"
```
