# vmstat
> Report information about processes, memory, paging, block IO, traps, disks and CPU activity.
> More information: <https://manned.org/vmstat>.
- Display virtual memory statistics:
`vmstat`
- Display reports every 2 seconds for 5 times:
`vmstat {{2}} {{5}}`

- changing the output units to megabytes using the -S option (use m for 1000000, and M for 1048576)

`vmstat -Sm {{1}}`

# Result
- r: Run-queue length—the total number of runnable threads 
- us: User-time percent 
- sy: System-time (kernel) percent 
- id: Idle percent 
- wa: Wait I/O percent, which measures CPU idle when threads are blocked on disk I/O 
- st: Stolen percent, which for virtualized environments shows CPU time spent servicing other tenants
- swpd: Amount of swapped-out memory 
- free: Free available memory 
- buff: Memory in the buffer cache 
- cache: Memory in the page cache 
- si: Memory swapped in (paging) 
- so: Memory swapped out (paging)
# Notice
- All of these values are system-wide averages across all CPUs, with the exception of r, which is the total.
- On Linux, the r column is the total number of tasks waiting plus those running. For other operating systems (e.g., Solaris) the r column only shows tasks waiting, not those running. The original vmstat(1) by Bill Joy and Ozalp Babaoglu for 3BSD in 1979 begins with an RQ column for the number of runnable and running processes, as the Linux vmstat(8) currently does.
- If the si and so columns are continually nonzero, the system is under memory pressure and is swapping to a swap device or file (see swapon(8)). Other tools, including those that show memory by process (e.g., top(1), ps(1)), can be used to investigate what is consuming memory.
