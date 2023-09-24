R## Введение в GNU/Linux
**Target platform (целевая платформа)** - платформа, где будет запускаться приложение

**Instrumental platfornm (интсрументальная платформа)** - платформа, где создается приложение

Возможно возникновение проблем при попытках перенести программу на другую платформу,тогда для исправления этого, приходится переписывать программу (программа не переносится на уровне исходного кода).

В рамках проекта GNU был создан стандарт POSIX

**POSIX** (англ. Portable Operating Systems Interface — переносимый интерфейс операционных систем) — набор стандартов, описывающий определённые интерфейсы, предоставляемые операционными системами.

Создан для обеспечения переносимости прикладного ПО на уровне исходного кода с помощью использования стандартизованного переносимого интерфейса для взаимодействия с операционной системой.

Есть системы, которые полностью соответсвуют стандарту POSIX (например, MAC OS, QNX), а есть те, которые соответсвуют не полностью, но совместимы (например, Linux, FreeBSD, NetBSD).

Дистрибутив - форма расспространения ПО.

## Репозитории Debian

- oldstable - Предыдущий стабильный релиз (Stretch).
- stable - Текущий стабильный релиз (Buster).
- testing - Следующий создаваемый релиз (Bullseye).
- unstable - Нестабильный разрабатываемый релиз (Sid), куда поступают новые или обновлённые пакеты.
- experimental - Не совсем релиз, но репозиторий, где пакеты проверяются, если они не подходят для unstable
- backports - Не релиз, но репозиторий для обновлённых пакетов для stable.

<img src="https://github.com/JulianP-P/KnowledgeBase/blob/e5eb26e97063d7d05bc6a06737558de9a94bcf79/AlgorithmsAndProgrramming/img/repos.png" width=50% height=50%>

Основная ветка, которая включается в каждый дистрибутив - это main. 
Здесь содержится только свободное программное обеспечение. 

Ветка contrib содержит программы, зависящие от несвободных программ. 

Ветка non-free содержит сами несвободные программы