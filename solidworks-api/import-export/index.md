---
title: Импорт и экспорт файлов с использованием SOLIDWORKS API
caption: Импорт/Экспорт
description: Коллекция примеров и статей, связанных с импортом и экспортом файлов с использованием SOLIDWORKS API
image: import-export.svg
order: 7
---
![Импорт и экспорт файлов SOLIDWORKS с помощью SOLIDWORKS API](import-export.svg){ width=250 }

SOLIDWORKS API позволяет экспортировать файл в иностранный формат через [IModelDocExtension::SaveAs2](https://help.solidworks.com/2019/english/api/sldworksapi/solidworks.interop.sldworks~solidworks.interop.sldworks.imodeldocextension~saveas2.html), и требуется только указать соответствующее расширение для иностранного файла (например, stp, x_t, igs и т.д.).

Для импорта иностранного файла необходимо использовать метод SOLIDWORKS API [ISldWorks::LoadFile4](https://help.solidworks.com/2019/english/api/sldworksapi/solidworks.interop.sldworks~solidworks.interop.sldworks.isldworks~loadfile4.html). Параметры этой функции позволяют указать дополнительные опции импорта.

Этот раздел содержит примеры кода, макросы и скрипты для автоматизации функциональности импорта и экспорта SOLIDWORKS.
