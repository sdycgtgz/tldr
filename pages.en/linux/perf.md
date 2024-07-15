# perf

> Framework for Linux performance counter measurements.
> More information: <https://perf.wiki.kernel.org>.

- Display basic performance counter stats for a command:

`perf stat {{gcc hello.c}}`

- Display system-wide real-time performance counter profile:

`sudo perf top`

- Run a command and record its profile into `perf.data`:

`sudo perf record {{command}}`

* uses perf(1) to sample stack traces (-g) across all CPUs (-a) at 49 Hertz (-F 49: samples per second) for 30 seconds

`sudo perf record -F 49 -a -g -- sleep 30`

- Record the profile of an existing process into `perf.data`:

`sudo perf record -p {{pid}}`

- Read `perf.data` (created by `perf record`) and display the profile:

`sudo perf report`

`sudo perf script`

* traces system calls by default, and is perf(1)’s version of strace(1)

`perf trace -p $(pgrep mysqld)`

* trace summarizes syscalls with -s

`perf trace -s -p $(pgrep mysqld)`
