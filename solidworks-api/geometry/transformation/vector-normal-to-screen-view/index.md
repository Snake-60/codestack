---
layout: article
title: Create vector normal to screen view using SOLIDWORKS API
caption: Create Vector Normal To Screen View
description: Example demonstrates how to draw a sketch line which is perpendicular (normal) to the current view orientation relative to the screen
image: /solidworks-api/geometry/transformation/vector-normal-to-screen-view/sw-view-screen-transformation.png
labels: [example, normal, screen, solidworks api, transformation, view]
redirect_from:
  - /2018/04/solidworks-api-transformation-create-vector-normal-to-screen-view.html
---
This example demonstrates how to draw a sketch line which is perpendicular (normal) to the current view orientation relative to the screen using SOLIDWORKS API.

The line will start at the point at the middle of the screen and will be perpendicular to the screen orientation. That means that initially it will be rendered as point until view rotates.

[IModelView::Transform](http://help.solidworks.com/2018/english/api/sldworksapi/solidworks.interop.sldworks~solidworks.interop.sldworks.imodelview~transform.html) SOLIDWORKS API property is used to extract the transformation matrix of current orientation of the view.

{% include img.html src="sw-view-screen-transformation.png" width=320 height=208 alt="Line created perpendicular to the current graphics view" align="center" %}

{% include_relative Macro.vba.codesnippet %}