# ps

> Information about running processes.
> More information: <https://manned.org/ps>.

- List all running processes:

`ps aux`

- List all running processes including the full command string:

`ps auxww`

- Search for a process that matches a string (the brackets will prevent `grep` from matching itself):

`ps aux | grep {{[s]tring}}`

- List all processes of the current user in extra full format:

`ps --user $(id -u) -F`

- List all processes of the current user as a tree:

`ps --user $(id -u) f`

- Get the parent PID of a process:

`ps -o ppid= -p {{pid}}`

- Sort processes by memory consumption:

`ps --sort size`

- Custom

`ps -eo pid,pmem,vsz,rss,comm`

# Result

-  %MEM: Main memory usage (physical memory, RSS) as a percentage of the total in the system

-  RSS: Resident set size (Kbytes) 

-  VSZ: Virtual memory size (Kbytes)

# Notice

- While RSS shows main memory usage, it includes shared memory segments such as system libraries, which may be mapped by dozens of processes. If you were to sum the RSS column, you might find that it exceeds the memory available in the system, due to overcounting of this shared memory. See Section 7.2.9(<<性能之巅>>第二版), Shared Memory, for background on shared memory, and the later pmap(1) command for analysis of shared memory usage.



