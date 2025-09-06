---
title: Окна редактора VBA
description: Обзор различных окон, доступных в редакторе VBA
image: immediate-window-menu.png
---
## Immediate Window (Окно непосредственного просмотра)

Immediate Window - это консоль, которая собирает выходные сообщения, выводимые из кода.

Окно Immediate обычно используется при отладке и устранении неполадок как простой способ вывода журнала или текущего состояния переменных.

Чтобы включить это окно, нажмите команду *View->Immediate Window* или сочетание клавиш *Ctrl+G*.

![Immediate Window Menu](immediate-window-menu.png)

Окно можно закрепить на любой панели в редакторе VBA.

Для вывода сообщений в это окно используйте команду *Debug.Print*

~~~ vb jagged
Dim str As String
str = "Hello World"
Debug.Print "Some Message"
Debug.Print str
~~~

![Output in the immediate window](imediate-window-output.png)

## Watch Window (Окно наблюдения)
