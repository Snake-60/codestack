---
layout: article
title: Determine the type Of active document using SOLIDWORKS API
caption: Determine The Type Of Active Document
description: Example displays the message box of the type of the document currently active in SOLIDWORKS
image: /images/codestack-snippet.png
labels: [assembly, document, drawing, example, part, type]
redirect_from:
  - /2018/03/determine-type-of-active-document.html
---
This example displays the message box of the type of the document currently active in SOLIDWORKS. This will work regardless the document is saved or not.  [IModelDoc2::GetType](http://help.solidworks.com/2018/english/api/sldworksapi/SOLIDWORKS.Interop.sldworks~SOLIDWORKS.Interop.sldworks.IModelDoc2~GetType.html) SOLIDWORKS API method can be used to return the type enumeration which will identify the document as SOLIDWORKS Part, Assembly or Drawing.

{% include_relative Macro.vba.codesnippet %}