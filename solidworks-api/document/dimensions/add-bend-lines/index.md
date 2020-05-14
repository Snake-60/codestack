---
layout: article
title: Add dimensions to bend lines using SOLIDWORKS API
caption: Add Dimensions To Bend Lines
description: Example demonstrates how to add dimensions to bend lines in the drawing view of sheet metal flat pattern
image: /solidworks-api/document/dimensions/add-bend-lines/sw-bend-lines.png
labels: [bend lines, dimension, example, solidworks api]
redirect_from:
  - /2018/03/solidworks-api-dimensions-dimension-bend-lines.html
---
This example demonstrates how to add dimensions to bend lines in the drawing view of sheet metal flat pattern using SOLIDWORKS API.

{% include img.html src="sw-bend-lines.png" width=400 height=150 alt="Dimension between bend lines in the sheet metal flat pattern drawing" align="center" %}

It is required to select the sketch lines using the select data object with the view assigned, otherwise the dimensions creating will fail.

[IModelDoc2::AddDimension2](http://help.solidworks.com/2018/english/api/sldworksapi/solidworks.interop.sldworks~solidworks.interop.sldworks.imodeldoc~adddimension2.html) SOLIDWORKS API is used to add the dimension. Dimension is positioned at (0, 0, 0) coordinate. Refer the [Dimension Visible Entities]({{ "/solidworks-api/document/drawing/view-dimension-drawing-entities/" | relative_url }}) example for code snippet for calculating the optimal dimension position.

{% include_relative Macro.vba.codesnippet %}