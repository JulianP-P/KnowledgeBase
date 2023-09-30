## Одномерные массивы

массив -сплошные данные

contiguous - сплошной

В некоторых языках программирования в переменной массива хранится адрес первой ячейки. Тогда индекс говорит о смещении относительно этой ячейки памяти. Тогда индексайия жестко закреплена с 0.

В Fortran переменная для массива хранит описатель массива, а не адрес ячейки памяти

decriptor - описатель

```
real A(10)
A = [1, 2 ]

A = 0

A = (/(0, k=1,5),(2,k=6.10)/)

A(1) = -2
A(3) = 2*A(1) + A(5)


```

### Смещение элементов массива - циклический сдвиг массива

```
real(10) A
A = CShift(A, 1, -1)

или конечный сдвиг

A = EOShift(A, 1, 11,) ! сдвиг на 1, последнее заполняем числом 11

или сечение массива
A = [A(2:10), 11]
```

## Двумерные массивы

Двумерные массивы развертываются в оперативную памяти начиная с 1 индекса (по левому индексу)
Обязательно обеспечиваем регулярный доступ к памяти! regular access - регулярный доступ


**Регулярный доступ** - это доступ к элементам в том порядке, в котором они располагаются в оперативной памяти.

```
real A(2,4) ! 2 строки и 4 столбца


real A(1:2, 1:4), B
```
Индексы меня.тся слева на право (наоборот как в математике)

```
real A (2,4) = [2,5,7,9,0,1,4,8]

A(2,4) = [2  7  0  4 &
          5  9  1  8]
```
```
real, allocatable :: A(:, :), B(:, :)
alocate (A(N,M)) ! хранение по столбцам
alocate (B(M,N)) ! хранение по строкам
! Во втором случае обязательно указать:
! B(j,i), j - номер столбца,  i - номер строки
! не стоит представлять это как строки
! записанные в столбцы - представлять это как способ индексации: B(j, i)
```
Нет технологий, которые хранят только по строкам или только по столбцам массивы
Разработчик, определяя назначение индексов, определяет тем самым хранение по строкам или по строкам
При нестандартном назначении индексов обызательно писать об этом в комментарии