---
title: "Ink/Stitch XML Namespace"
permalink: /namespace/
excerpt: "Document of all metadata tags and embroidery attributes - in future"

classes: wide
---
This page contains a description of all metadata tags and embroidery attributes.

See the [namespace github discussion](https://github.com/inkstitch/inkstitch/issues/202).

## Namespace Declaration

`<svg>` attribute: `xmlns:inkstitch="http://inkstitch.org/namespace"`

## Embroider

|Attribute of `<path>`                              | Data Type| Description |
|---|---|---|
|**AutoFill**|
|*embroider_auto_fill*                              | boolean  | True: automatic routed fill stitching (Auto-Fill)<br>False: fill |
|embroider_angle                                    | float    | angle |
|embroider_expand_mm                                | float    | expand the shape before fill stitching, to compensate for gaps between shapes. |
|embroider_max_stitch_length_mm                     | float    | max. stitch length in mm |
|embroider_row_spacing_mm                           | float    | stitch length in mm |
|embroider_running_stitch_length_mm                 | float    | running stitch length in mm |
|embroider_staggers                                 | float    | stagger this many times before repeating |
|*embroider_fill_underlay*                          | boolean  | enable Auto-Fill underlay |
|embroider_fill_underlay_angle                      | float    | underlay angle |
|embroider_fill_underlay_inset_mm                   | float    | underlay inset in mm |
|embroider_fill_underlay_max_stitch_length_mm       | float    | underlay max. stitch length in mm |
|embroider_fill_underlay_row_spacing_mm             | float    | underlay row spacing in mm |
|**Fill**|
|*embroider_auto_fill*                              | boolean  | True: automatic routed fill stitching (Auto-Fill)<br>False: fill |
|embroider_angle                                    | float    | angle |
|embroider_flip                                     | boolean  | flip start (right to left) |
|embroider_max_stitch_length_mm                     | float    | max. stitch length in mm |
|embroider_row_spacing_mm                           | float    | stitch length in mm |
|embroider_staggers                                 | float    | stagger this many times before repeating |
|**Stroke**|
|**↳ Stroke: Running Stitch**|
|embroider_zigzag_spacing_mm                        | float    | Stroke/Satin column: zig-zag spacing (peak-to-peak) in mm |
|embroider_running_stitch_length_mm                 | float    | AutoFill/Stroke: running stitch length in mm |
|embroider_repeats                                  | float    | Stroke: defines how many times to run down and back along the path |
|**↳ Stroke: Zig-Zag**|
|*embroider_satin_column*                           | boolean  | True: satin column<br>False: stroke (zig-zag stitch) |
|embroider_running_stitch_length_mm                 | float    | AutoFill/Stroke: running stitch length in mm |
|embroider_zigzag_spacing_mm                        | float    | Stroke/Satin column: zig-zag spacing (peak-to-peak) in mm |
|embroider_repeats                                  | float    | Stroke: defines how many times to run down and back along the path |
|**↳ Stroke: Manual Stitch**|
|*embroider_manual_stitch*                          | boolean  | True: manual stitch<br>False: stroke (running stitch / zig-zag stitch |
|**Satin Column**|
|*embroider_satin_column*                           | boolean  | True: satin column<br>False: stroke (zig-zag stitch) |
|embroider_pull_compensation_mm                     | float    | Satin column: pull compensation in mm|
|embroider_zigzag_spacing_mm                        | float    | Stroke/Satin column: zig-zag spacing (peak-to-peak) in mm |
|*embroider_center_walk_underlay*                   | boolean  | Satin column: enable center walk underlay |
|embroider_center_walk_underlay_stitch_length_mm    | float    | Satin column: center-walk underlay stitch length in mm |
|*embroider_contour_underlay*                       | boolean  | Satin column: enable Contour underlay |
|embroider_contour_underlay_inset_mm                | float    | Satin column: contour underlay inset amount in mm |
|embroider_contour_underlay_stitch_length_mm        | float    | Satin column: contour underlay stitch length in mm |
|*embroider_zigzag_underlay*                        | boolean  | Satin column: enable zig-zag underlay |
|embroider_zigzag_underlay_inset_mm                 | float    | Satin Column: zig-zag underlay inset in mm |
|embroider_zigzag_underlay_spacing_mm               | float    | Satin Column: zig-zag underlay spacing in mm |

## Visual Commands

|Attribute of `<use>`| Description|
|---|---|
|xlink:href="#inkstitch_fill_start"   | Fill Start |
|xlink:href="#inkstitch_fill_end"     | Fill End   |
|xlink:href="#inkstitch_stop"         | Stop       |
|xlink:href="#inkstitch_trim"         | Trim       |
|xlink:href="#inkstitch_ignore"       | Ignore     |

## Print PDF

|Elements within `<metadata>`                     | Data Type           | Description                                       |
|---|---|---|
|inkstitch:paper-size                             | string              | Paper Format: A4, Letter                          |
|inkstitch:operator-overview                      | boolean             | Wether operator overview should be displayed      |
|inkstitch:operator-detailedview                  | boolean             | Wether operator detailedview should be displayed  |
|inkstitch:client-overview                        | boolean             | Wether client overview should be displayed        |
|inkstitch:client-detailedview                    | boolean             | Wether client detailedview should be displayed    |
|inkstitch:operator-detailedview-thumbnail-size   | integer             | Size of operator detailedview thumbnails in mm    |
|inkstitch:thread-palette                         | string              | Name of the thread palette                        |
|inkstitch:title                                  | string              | Job title                                         |
|inkstitch:client-name                            | string              | Client name                                       |
|inkstitch:purchase-order                         | string              | Purchase order                                    |
|inkstitch:client-overview-transform              | string              | CSS 2D tranformation: matrix(n,n,n,n,n,n)         |
|inkstitch:color-000000                           | string              | Name of the color specified by RGB color value  (here: 000000) |
|inkstitch:thread-000000                          | string              | Name of the thread specified by RGB color value (here: 000000) |
|inkstitch:operator-notes-block1                  | string              | Color block note specified by block number (here: 1) |
