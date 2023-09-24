Язык высокого уровня - язык, при котором не нужно обращаться к системам команд.
Чистое программирование - Отсутствие побочных эффектов.
## Команды 
IMPLICIT NONE - означает отключение неявных средств
#### Высокоуровневая структура кода
```
PROGRAM example1
!комментарий
IMPLICT NONE
   INTEGER :: hours,mins,secs,temp
   PRINT *,'Type the hours, minutes ans seconds'
   READ *, hours, mins, secs
   temp = 60* ( hours*60 + mins ) + secs
   PRINT *, 'Timr in seconds = ', temp
END PROGRAM example1
```
1. Начало программы
`PROGRAM example1`
3. Спецификация (невыполняемые операторы): объявление типов и размерности данных

    1. Выделить память под данные `INTEGER :: hours,mins,secs,temp`

   `hours,mins,secs` - входные данные, `temp` - временная переменная
5. Исполняемая часть: выполняемые операторы
6. Конец программы
`END PROGRAM example1`
   
