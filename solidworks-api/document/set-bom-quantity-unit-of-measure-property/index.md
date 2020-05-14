---
layout: article
title: Set BOM Quantity (Unit Of Measure) property using SOLIDWORKS API
caption: Set BOM Quantity (Unit Of Measure) Property In The Model
description: Example demonstrates how to modify the BOM quantity field in the properties dialog
image: /solidworks-api/document/set-bom-quantity-unit-of-measure-property/bom-quantity-property.png
labels: [bom quantity, example, qty, unit of measure]
redirect_from:
  - /2018/03/set-bom-quantity-unit-of-measure.html
---
This example demonstrates how to modify the BOM quantity field in the properties dialog using SOLIDWORKS API.

{% include img.html src="bom-quantity-property.png" width=640 height=170 alt="Option to specify the property linked to Unit Of Measure" align="center" %}

This option allows overwriting the quantity value of the component in the BOM table

{% include img.html src="bom-table-unit-of-measure.png" width=640 alt="Bill Of Materials table displaying the altered quantity of the components" align="center" %}

In order to change this property it is required to set the hidden *UNIT_OF_MEASURE* custom property via [ICustomPropertyManager](http://help.solidworks.com/2018/english/api/sldworksapi/solidworks.interop.sldworks~solidworks.interop.sldworks.icustompropertymanager.html) SOLIDWORKS API interface.

{% include_relative Macro.vba.codesnippet %}