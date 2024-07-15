# sar

> Monitor performance of various Linux subsystems.
> More information: <https://manned.org/sar>.
>
> 也可参考格雷格<<性能之巅>>第二版的4.4章节,可以用sadf查看不同格式的统计数据`sadf -j -- -n TCP`

- Report I/O and transfer rate issued to physical devices, one per second (press CTRL+C to quit):

`sar -b {{1}}`

- Report a total of 10 network device statistics, one per 2 seconds:

`sar -n DEV {{2}} {{10}}`

- Report CPU utilization, one per 2 seconds:

`sar -u ALL {{2}}`

- Report a total of 20 memory utilization statistics, one per second:

`sar -r ALL {{1}} {{20}}`

- Report the run queue length and load averages, one per second:

`sar -q {{1}}`

- Report paging statistics, one per 5 seconds:

`sar -B {{5}}`

# Result

> 统计信息含义和单位详见<<性能之巅>>第二版表7.5

-  -B: Paging statistics 
-  -H: Huge pages statistics 
-  -r: Memory utilization 
-  -S: Swap space statistics 
-  -W: Swapping statistics
