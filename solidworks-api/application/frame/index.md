---
title: Настройка главного окна приложения с использованием SOLIDWORKS API
caption: Главное окно
description: Автоматизация главного окна SOLIDWORKS (меню, панели инструментов, диспетчер команд) с использованием API
labels: [frame,menu,toolbar,commands]
---
Элементы, отображаемые в главном окне приложения SOLIDWORKS, такие как меню, диспетчер команд и вкладки, панели инструментов, могут быть настроены с использованием интерфейсов SOLIDWORKS API [IFrame](https://help.solidworks.com/2018/english/api/sldworksapi/SolidWorks.Interop.sldworks~SolidWorks.Interop.sldworks.IFrame.html) и [ISldWorks](https://help.solidworks.com/2018/english/api/sldworksapi/SolidWorks.Interop.sldworks~SolidWorks.Interop.sldworks.ISldWorks.html).

Кроме того, объект frame предоставляет доступ к дескриптору окон SOLIDWORKS через метод [IFrame::GetHWnd](https://help.solidworks.com/2018/english/api/sldworksapi/solidworks.interop.sldworks~solidworks.interop.sldworks.iframe~gethwnd.html), что позволяет использовать [Windows API для вызова команд SOLIDWORKS](https://blog.codestack.net/2019/03/solidworks-api-command-doesnt-exist.html).

Этот раздел содержит примеры использования SOLIDWORKS API и Windows API для автоматизации главного окна приложения.
