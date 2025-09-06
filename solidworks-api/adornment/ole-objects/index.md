---
title: Управление OLE объектами в моделях с использованием SOLIDWORKS API
caption: OLE объекты
description: Коллекция макросов и примеров, демонстрирующих работу с различными встроенными OLE объектами (таблица проектирования, вложение и т.д.) с использованием SOLIDWORKS API
order: 2
labels: [ole, embeding]
---
Object Linking and Embedding (OLE) - это технология Microsoft, позволяющая вставлять объекты сторонних приложений в документы. В SOLIDWORKS OLE объекты используются для представления таблиц проектирования, вложений и любых файлов, перетащенных непосредственно в документ.

Такими объектами обычно можно манипулировать непосредственно из среды хоста. Например, встроенный файл Excel можно изменить, не выходя из окна SOLIDWORKS.

OLE объекты обычно сохраняются вместе с файлом SOLIDWORKS и могут быть удалены, изменены в размере или использованы непосредственно в графической области.

SOLIDWORKS API обеспечивает доступ к OLE объектам через интерфейс [ISwOLEObject](https://help.solidworks.com/2018/english/api/sldworksapi/SOLIDWORKS.Interop.sldworks~SOLIDWORKS.Interop.sldworks.ISwOLEObject.html). Объекты могут быть перечислены, созданы и удалены с использованием методов API интерфейса [IModelDocExtension](https://help.solidworks.com/2018/english/api/sldworksapi/SolidWorks.Interop.sldworks~SolidWorks.Interop.sldworks.IModelDocExtension.html).

Этот раздел содержит макросы и примеры, позволяющие манипулировать OLE объектами в документах с использованием SOLIDWORKS API.
