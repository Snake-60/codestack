---
title: Область видимости переменных в Visual Basic
caption: Область видимости переменных
description: Статья, объясняющая различные области видимости переменных (публичные и приватные на уровне класса, локальные) в Visual Basic
image: custom-module-named-module1.png
order: 4
---
В языке Visual Basic переменные могут быть объявлены в разных областях видимости (уровень модуля, локальные в функции, внутри блока кода) с разными модификаторами доступа (private или public), которые определяют их видимость в коде.

## Класс или модуль (также известные как члены)

Обычно объявляются в заголовке класса (вне функций и процедур). Переменные-члены имеют 2 уровня видимости (private и public).

### Private

Объявляются с использованием ключевого слова *Dim* или *Private* и видны только функциям и процедурам в пределах этого класса или модуля.

*Module1*

~~~vb
Dim member As Integer
Private member1 As String

Sub Init()
    member = 10 'видна внутри функции Init модуля
    member1 = "A"
End Sub
~~~

Приватные переменные не могут быть доступны извне модуля или класса. Ошибка компиляции: метод или член данных не найден возникает при попытке доступа к приватному члену извне класса или модуля.

![Ошибка компиляции: метод или член данных не найден при вызове приватно объявленной переменной извне класса](not-found-member-on-private-variable.png){ width=500 }

### Public

Публичные переменные объявляются с использованием ключевого слова *Public* и могут быть доступны как из текущего модуля или класса, так и из внешнего модуля или класса.

*Module1*
~~~vb jagged
Dim publicMember As Integer
~~~

*Module2*
~~~vb jagged
Sub main()
    Module1.publicMember = 20 'переменная доступна и назначена из внешнего модуля
End Sub
~~~

Альтернативно публичный член может быть объявлен с ключевым словом *Global*. Он будет вести себя так же, как *Public*, однако может быть объявлен только в [модуле](/visual-basic/modules/) и не может быть объявлен в [пользовательской форме](/visual-basic/user-forms/) или [модуле класса](/visual-basic/classes/).

## Локальные

Локальные переменные объявляются в области видимости конкретного блока кода или функции и видны только внутри этого блока для кода, появляющегося после объявления переменной

~~~ vb jagged
Dim var1 As Double
var1 = 0.5 'var1 видна здесь
var2 = 0.25 'var2 не видна на этом шаге, так как объявлена в следующей строке
Dim var2 As Double
~~~

### Блок кода
Переменные, определенные в циклах или условных операторах

~~~ vb jagged
If res Then
    Dim localVar As Integer 'локальная переменная, определенная внутри блока кода If
    localVar = 25
End If
~~~

Хотя локальные переменные блока кода видны только внутри этого блока, то же имя переменной не может быть использовано в другом блоке кода.

### Функция или процедура

Переменные, определенные в контексте функции или процедуры. Эти переменные видны внутри функции или любых вложенных блоков кода.

~~~ vb
Sub main()
    Dim localVar As String
    Dim localBoolVar As Boolean
    localVar = "Hello World"
    If localBoolVar Then 'локальная переменная доступна в условном операторе
        localVar = "New Hello World" 'локальная переменная изменена внутри тела условного оператора
    End If
End Sub
~~~

### Параметр функции или процедуры

Переменные определены в сигнатуре функции. Эти объявления переменных эквивалентны локальной переменной функции, объявленной в первой строке тела функции, т.е. переменные видны для всех блоков кода внутри этой функции.

~~~ vb
Sub DoWork(paramVar As Double, paramVar2 As Integer)
End Sub
~~~

Этот пример демонстрирует поведение переменных, объявленных в разных областях видимости:

*Module1*
![Модуль Module1 в проекте Visual Basic](custom-module-named-module1.png)

{% code-snippet { file-name: different-scopes-example-module1.vba } %}

*Главный модуль*

{% code-snippet { file-name: different-scopes-example.vba } %}

Вывод в [Immediate Window](visual-basic/vba/vba-editor/windows#immediate-window)

![Вывод значений переменных](immediate-window-output.png){ width=350 }

## Таблица областей видимости

При следующей структуре проекта:

![VBA проект](vb-project.png)

Каждый из файлов имеет следующие объявления:

### UserForm

~~~ vb jagged
Public VarFormPublic As String
Private VarFormPrivate As String
Dim VarFormDim As String
Dim VarFormGlobal As String 'не может быть объявлена
~~~

### Module

~~~ vb jagged
Public VarModulePublic As String
Global VarModuleGlobal As String
Dim VarModuleDim As String
Private VarModulePrivate As String
~~~

### Class

~~~ vb jagged
Public VarClassPublic As String
Dim VarClassDim As String
Private VarClassPrivate As String
Dim VarClassGlobal As String 'не может быть объявлена
~~~

Таблица ниже описывает видимость переменных в разных файлах

|Имя переменной|UserForm|Module|Module1|Class
|---|---|--|--|--|
VarFormPublic|✓|✓|✓|✓|
VarFormPrivate|✓|☓|☓|☓|
VarFormDim|✓|☓|☓|☓|
VarFormGlobal|-|-|-|-|
VarModulePublic|✓|✓|✓|✓|
VarModuleGlobal|✓|✓|✓|✓|
VarModuleDim|☓|✓|☓|☓|
VarModulePrivate|☓|✓|☓|☓|
VarClassPublic|✓|✓|✓|✓|
VarClassPrivate|☓|☓|☓|✓|
VarClassDim|☓|☓|☓|✓|
VarClassGlobal|-|-|-|-|
