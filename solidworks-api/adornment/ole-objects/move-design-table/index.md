---
layout: article
title: Move design table object using SOLIDWORKS API
caption: Move Design Table OLE Object
description: Example demonstrates how to resize and move the design table OLE object in the model graphics area
image: /solidworks-api/adornment/ole-objects/move-design-table/design-table-ole-object.png
labels: [adornment, boundary, design table, example, move, ole object, solidworks api]
redirect_from:
  - /2018/03/move-design-table-ole-object.html
---
This example demonstrates how to resize and move the design table OLE object in the graphics area using [ISwOLEObject::Boundaries](http://help.solidworks.com/2018/english/api/sldworksapi/solidworks.interop.sldworks~solidworks.interop.sldworks.iswoleobject~boundaries.html) SOLIDWORKS API method.

{% include img.html src="design-table-ole-object.png" width=640 height=226 alt="Design Table OLE object in the graphics area" align="center" %}

In this example an existing design table element will be moved to the right on the distance equals to object's width

{% include_relative Macro.vba.codesnippet %}