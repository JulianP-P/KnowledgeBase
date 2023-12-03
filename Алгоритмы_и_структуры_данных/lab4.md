memory leaks - утечка памяти

Если на вход функции приходит ссылка, то проверяем, связанна ли она `type(node), pointer :: cuurent; if(Associated(current))...`

Если не делаем `deallocate(tmp)`, то объект становится недостижимым (unreachable)

Собственный код = исполняемый код для конкретной платформы

Добавляем в начало списка новый объект
```
type(entry), allocatable :: top, temp
temp = entry( new_value, new_indexm temp)
call move_alloc( top, temp%next) - отдает размещение от одного объекта к другому, а первый объект становится не размещен
call move_alloc(temp, top)
```

Перепрыгеуть объекту самому через себя
`top = top%next`
или
```
call move_alloc(Elem%next, temp)
call move_alloc(temp, Elem)
```

Двунаправленный список создаем при острой необходимости

## Полиморфизм
- возможность работать с объектами разной природы

```
! Структура данных для узла списка.
! Инициализация обязательна!
type node
!type, abstract :: node
   class(node), pointer :: next  => Null()
end type node

type, extends(node) :: variable
   character(kind=CH_)  :: char = ""
end type variable

type, extends(variable) :: operation
end type operation

type, extends(node) :: operand
    integer(I_) :: value = 0
 end type operand

type, extends(node) :: left_bracket
  character(kind=CH_) :: bracket = CH__"("
end type left_bracket

type, extends(node) :: right_bracket
    character(kind=CH_)  :: bracket = CH__")"
end type right_bracket
```

## Кодирование динамических структур данных средствами функционального программирования

переменная-ссылка

Обобщенное программирование - jeneric programming

