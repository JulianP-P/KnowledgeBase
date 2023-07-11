## Профилирование с помощью async-profiler
Запускается с помощью команды `./do_profiler.sh *pid*`

Сдержание do_profiler.sh
```bash
#!/bin/bash
ASYNC_PROFILER=./async-profiler-1.8.2-linux-x64/profiler.sh
echo "Start profile process $1"
var=0
while sleep 1 ; do $ASYNC_PROFILER -e wall -d 300 -b 10000000 -f flamegraph_%p_$((var))_%t.svg -s -o svg $1 ; done
```
