---
title: Кодирование и декодирование данных в формате строки Base64 в Visual Basic 6 (VBA)
caption: Строка Base64
description: Кодирование и декодирование байтового массива в формат строки Base64 в Visual Basic 6 (VBA)
labels: [base64,encoding,decoding]
---
Строка Base64 позволяет хранить данные байтового массива в строковом формате

## Кодирование

~~~vb
Dim arr(5) As Byte
arr(0) = 1: arr(1) = 5: arr(2) = 2
arr(3) = 21: arr(4) = 101: arr(5) = 51

Dim base64Str As String
base64Str = ConvertToBase64String(arr) 'AQUCFWUz
~~~

{% code-snippet { file-name: encode-base64.vba } %}

## Декодирование

~~~vb
Dim base64Str As String
base64Str = "AQUCFWUz"

dim vArr As Variant
vArr = Base64ToArray(base64Str) 'Байтовый массив: 1, 5, 2, 21, 101, 51
~~~

{% code-snippet { file-name: decode-base64.vba } %}
