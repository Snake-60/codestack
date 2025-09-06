---
layout: default
title: Library of macros and scripts to automate SOLIDWORKS
caption: "'Goodies'"
description: Useful automation macros and scripts to increase your productivity when working in SOLIDWORKS
image: macros-library.svg
labels: [tools,solidworks,macro]
search: false
styles:
  - /_assets/styles/catalogue.css
group-descriptions:
  Model: Automation of 3D Models (parts and assemblies) and 2D drawings
  Materials: Automation of SOLIDWORKS materials database and properties in parts
  Frame: Automation of SOLIDWORKS menus, toolbars, 3rd party add-ins, documents management
  Developers: Helpful utilities for developers building software utilizing SOLIDWORKS API
  Custom Properties: Automation of SOLIDWORKS generic, configuration and cut-list custom properties
  Part: 'Automation of SOLIDWORKS part documents (*.sldprt): geometry, feature tree'
  Assembly: 'Automation of SOLIDWORKS assembly documents (*.sldasm): components, mates'
  Drawing: 'Automation of SOLIDWORKS drawing documents (*.slddrw): tables, views, sheets'
  Security: Enabling additional security and protection for the models and applications using SOLIDWORKS API
  Sketch: Automation of SOLIDWORKS sketch, segments and relations
  Performance: Boosting operational performance of SOLIDWORKS documents and application
  Geometry: 'SOLIDWORKS geometry automation: custom features, topology optimization'
  Import/Export: Automation of importing and exporting SOLIDWORKS files to different formats
  Motion Study: Automation of SOLIDWORKS Motion Study module
  Options: SOLIDWORKS document and system option automation
  Cut-List: 'Automation of SOLIDWORKS cut-lists in Sheet Metal and Weldment parts and drawings'
redirect-from:
  - /p/solidworks-goodies.html
---
# Библиотека макросов для автоматизации SOLIDWORKS
{% social-share %}

[Запросить макрос](https://github.com/xarial/codestack/issues/new?labels=macro-request){ target="_blank" class="download-button" }

![Библиотека макросов SOLIDWORKS](macros-library.svg){ width=400 }

Эта страница содержит библиотеку полезных макросов, утилит и скриптов для инженеров SOLIDWORKS. Макросы сгруппированы по категориям: детали, сборки, чертежи, производительность и т.д.

Следуйте разделу [Программирование VBA и VSTA макросов с использованием SOLIDWORKS API](/solidworks-api/getting-started/macros/) для получения руководств по использованию и созданию макросов в SOLIDWORKS.

Не можете найти нужный макрос? Отправьте форму [запроса макроса](https://github.com/xarial/codestack/issues/new?labels=macro-request), и наша команда рассмотрит ваш запрос и постарается добавить макрос в библиотеку.

## Лучшие практики организации библиотеки макросов

[Toolbar+](https://cadplus.xarial.com/toolbar/) является частью бесплатного и открытого набора инструментов [CAD+ Toolset](https://cadplus.xarial.com/) для SOLIDWORKS, который позволяет организовать библиотеку макросов в пользовательских панелях инструментов, интегрированных в среду SOLIDWORKS. Надстройка также позволяет управлять многопользовательской средой, храня конфигурацию в централизованном месте.

![Пользовательские кнопки макросов на панели инструментов](macro-library-toolbar.png){ width=450 }

Альтернативно кнопки макросов можно создавать с использованием собственной функциональности SOLIDWORKS. Прочитайте [Создание кнопок макросов на панелях инструментов SOLIDWORKS](/solidworks-api/getting-started/macros/macro-buttons/) для получения дополнительной информации.

Изучите этот раздел, чтобы найти инструменты повышения продуктивности и автоматизации, которые соответствуют вашим потребностям.

Для получения дополнительных надстроек повышения продуктивности посетите страницу [SOLIDWORKS Labs](/labs/solidworks/).

## Пакетное выполнение

В некоторых случаях может потребоваться пакетное выполнение макросов для нескольких файлов или папок с файлами SOLIDWORKS. Попробуйте [Batch+](https://cadplus.xarial.com/batch/) - бесплатное автономное приложение, часть бесплатного и открытого набора инструментов [CAD+ Toolset](https://cadplus.xarial.com/).

---
{% catalogue { type: sw-tool } %}
