21.09
## Управляющие операторы

### Условный оператор if

Способы создания конструкции
```
1.
имя:  if (условие) then
        операторы_Т
      else
        операторы_F
      end if имя

2.
имя:  if (условие) then
        операторы_Т
      end if имя

3.
      if (условие) Оператор_Т
! или
     if (условие) &
        Оператор_Т
```

### Оператор выбора select case
```
select case (выражение)
        case (множество_значений_1)
          операторы
        case (множество_значений_1)
          операторы
        case default
          операторы
end select
```
Выражений должно быть целого, символьного илил логического типа

Переменные-флаги - хранят результаты проверок

Пример, как их можно избежать
```
read(*, *) op

calc: block
        select case (op)
                case ('+'); res = a+b
                case ('+'); res = a+b
                case ('+'); res = a+b
                case ('+'); res = a+b
                case default
                        write (ERROR_UNIT, *) "ERROR!"
                        exit calc
        end select
        write (*, *) "Result ...", res
end block calc
```
