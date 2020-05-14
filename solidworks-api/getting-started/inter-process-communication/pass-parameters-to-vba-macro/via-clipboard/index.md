---
layout: article
title: Passing the parameters to SOLIDWORKS VBA Macro via clipboard
caption: Via Clipboard
description: Passing the custom string parameters to VBA macro from .NET application or another macro via clipboard
image: /solidworks-api/getting-started/inter-process-communication/pass-parameters-to-vba-macro/via-clipboard/msg-box-macro-argument.png
labels: [argument, clipboard, example, parameter, solidworks api]
redirect_from:
  - /2018/04/pass-arguments-to-vba-macro-via-clipboard.html
---
System clipboard allows to store different types of data (that includes but not limited to text, image, html etc.). As the simplest way, the custom argument may be written to the text buffer, but this will clear all the data already in the buffer (if any). This may introduce confusion and result in bad user experience as running the macro may overwrite the text already copied into the clipboard.  

Alternative way is to write the data into the custom buffer with unique name so it is not explicitly exposed to the user and will remain accessible via code only.

Let's start with the 'target' macro which will be called from the different 'master' macro.  

{% include_relative read-argument-from-vba.vba.codesnippet %}

In the example above argument value passed from the 'master' macro will be extracted and displayed to the user in the message box in the 'target' macro:

{% include img.html src="msg-box-macro-argument.png" width=400 height=132 alt="Message box in macro displaying the passed argument value" align="center" %}

The helper class reads the buffer value from the **__SwMacroArgs__** format. This is a custom name which is known to both 'master' macro (which will write the value of argument) and the 'target' macro (which will read the value). This can be renamed to any other custom name if needed.

{% include_relative argument-helper-get-argument.vba.codesnippet %}

In order to call the macro and pass the argument it is required to set the buffer value for **__SwMacroArgs__** format as the unicode string. Below are examples which demonstrate how to do this in different programming languages

<details>
<summary>VBA Macro</summary>

Argument Helper Module

{% include_relative argument-helper-set-argument.vba.codesnippet %}

Macro

{% include_relative call-macro-with-argument-vba.vba.codesnippet %}

</details>

<details>
<summary>C#</summary>

{% include_relative call-macro-with-arguments-csharp.cs.codesnippet %}

</details>

<details>
<summary>VB.NET</summary>

{% include_relative call-macro-with-arguments-vb.net.vb.codesnippet %}

</details>

**NOTE: the examples above do not handle 'race conditions' (when multiple macros with different arguments may be run in parallel). Use Mutex or Semaphore objects to synchronise the access to shared resources.**