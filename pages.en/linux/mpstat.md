# mpstat

> Report CPU statistics.
> More information: [https://manned.org/mpstat](https://manned.org/mpstat).

- Display CPU statistics every 2 seconds:

`mpstat {{2}}`

- Display 5 reports, one by one, at 2 second intervals:

`mpstat {{2}} {{5}}`

- Display 5 reports, one by one, from a given processor, at 2 second intervals:

`mpstat -P {{0}} {{2}} {{5}}`

- print the per-CPU report. By default, mpstat(1) prints only the system-wide summary line (all)

`mpstat -P ALL 1`

# Result
- CPU: Logical CPU ID, or all for summary
- %usr: User-time, excluding %nice
- %nice: User-time for processes with a nice’d priority
- %sys: System-time (kernel)
- %iowait: I/O wait
- %irq: Hardware interrupt CPU usage
- %soft: Software interrupt CPU usage
- %steal: Time spent servicing other tenants
- %guest: CPU time spent in guest virtual machines
- %gnice: CPU time to run a niced guest
- %idle: Idle

