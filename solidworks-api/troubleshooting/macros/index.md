---
title: 'Устранение неполадок макросов SOLIDWORKS: проблемы и решения'
caption: 'Устранение неполадок макросов: проблемы и решения'
description: Обзор и решения наиболее распространенных ошибок при запуске макросов в SOLIDWORKS
labels: [macro, not working, problem, solidworks api, troubleshooting, vba]
styles:
  - /_assets/styles/catalogue.css
redirect-from:
  - /2018/04/macros-troubleshooting-issues-and-resolutions.html
---
Макрос SOLIDWORKS - это наиболее распространенный способ автоматизации и расширения функциональности SOLIDWORKS через его API.
Макросы могут быть разработаны внутри компании или загружены с различных веб-сайтов, включая форум SOLIDWORKS, 3D Content Central, [CodeStack](/solidworks-tools) и т.д., или даже записаны из SOLIDWORKS.

Но в некоторых случаях макрос не работает как ожидалось. Обычно это один из следующих сценариев:

* Макрос, который раньше работал правильно, перестал работать.
* Макрос работает на некоторых рабочих станциях, но не на других.
* Макрос работает правильно для некоторых моделей, но не для других.

В этой статье я рассмотрю наиболее распространенные симптомы ошибок в макросах.

Просмотрите список ошибок, чтобы найти наиболее распространенные решения.

Нажмите на ссылку, чтобы получить подробное описание проблем, их причин и шаги по устранению проблемы.

## Список ошибок

* Run-time Error '91': Object variable or With block variable not set (Ошибка времени выполнения '91': объектная переменная или переменная блока With не задана)
  * [Решение 1](/solidworks-api/troubleshooting/macros/assembly-drawing-lightweight-components/)
  * [Решение 2](/solidworks-api/troubleshooting/macros/macro-multiple-entry-points/)
  * [Решение 3](/solidworks-api/troubleshooting/macros/create-sketch-segments-error/)
  * [Решение 4](/solidworks-api/troubleshooting/macros/preconditions-not-met/)
  * [Решение 5](/solidworks-api/troubleshooting/macros/selection-inconsistency/)

* Compile Error: Can't find project or library (Ошибка компиляции: не удается найти проект или библиотеку)
  * [Решение 1](/solidworks-api/troubleshooting/macros/missing-solidworks-type-library-references/)

* Run-time error '424': Object required (Ошибка времени выполнения '424': Требуется объект)
  * [Решение 1](/solidworks-api/troubleshooting/macros/merged-macro-error/)

* Run-time error '13': Type mismatch (Ошибка времени выполнения '13': Несоответствие типов)
  * [Решение 1](/solidworks-api/troubleshooting/macros/preconditions-not-met/)

* Compile Error: User-defined type not defined (Ошибка компиляции: пользовательский тип не определен)
  * [Решение 1](/solidworks-api/troubleshooting/macros/swb-macro-error/)

* Run-time error '438': object doesn't support this property or method (Ошибка времени выполнения '438': объект не поддерживает это свойство или метод)
  * [Решение 1](/solidworks-api/troubleshooting/macros/future-version-apis/)

* Run-time error '429': ActiveX component can't create object (Ошибка времени выполнения '429': компонент ActiveX не может создать объект)
  * [Решение 1](/solidworks-api/troubleshooting/macros/missing-com-component/)

* Run-time Error '5': Invalid procedure call or argument (Ошибка времени выполнения '5': недопустимый вызов процедуры или аргумент)
  * [Решение 1](/solidworks-api/troubleshooting/macros/model-title-inconsistency-displaying-extension/)

* Compile error: The code in this project must be updated for use on 64-bit systems is displayed. Please review and update Declare statements and then mark item with the PtrSafe attribute (Ошибка компиляции: код в этом проекте должен быть обновлен для использования в 64-битных системах. Пожалуйста, просмотрите и обновите операторы Declare, а затем пометьте элемент атрибутом PtrSafe)
  * [Решение 1](/solidworks-api/troubleshooting/macros/32-windows-api-functions-incorrect-use/)

* Cannot Open (for VBA macros) (Не удается открыть (для VBA макросов))
  * [Решение 1](/solidworks-api/troubleshooting/macros/too-long-macro-path/)

* Compile error: Invalid outside procedure error (Ошибка компиляции: недопустимо вне процедуры)
  * [Решение 1](/solidworks-api/troubleshooting/macros/too-long-vba-macro-line/)

* SolidWorksMacro doesn't contain a definition for 'swApp' (VSTA) (SolidWorksMacro не содержит определение для 'swApp' (VSTA))
  * [Решение 1](/solidworks-api/troubleshooting/macros/vsta-invalid-namespace/)

* Cannot open (for VSTA macros) (Не удается открыть (для VSTA макросов))
  * [Решение 1](/solidworks-api/troubleshooting/macros/run-vsta-macro-error/)

{% catalogue { type: sw-macro-fix } %}
