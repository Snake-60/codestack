---
layout: article
title: Change system page setup options in SOLIDWORKS using API in macro
caption: Change System Page Setup Options
description: Changing system level (application) page setup options (printer paper size, scale, etc.) for printing using SOLIDWORKS API
image: /solidworks-api/options/application/system-page-setup/page-setup.png
labels: [print,page setup,preferences]
---
{% include img.html src="page-setup.png" width=350 alt="Page Setup" align="center" %}

This example demonstrates how to change the system page setup option (paper size and scale) and set the current document options to use the system settings using SOLIDWORKS API.

This example also demonstrates how to retrieve the system specific paper size integer for [IPageSetup::PrinterPaperSize](http://help.solidworks.com/2016/english/api/sldworksapi/SolidWorks.Interop.sldworks~SolidWorks.Interop.sldworks.IPageSetup~PrinterPaperSize.html) by specifying the paper name.

{% include_relative Macro.vba.codesnippet %}