# perf-tools
> More information: <https://github.com/brendangregg/perf-tools>.
> A miscellaneous collection of in-development and unsupported performance analysis tools for Linux ftrace and perf_events (aka the "perf" command). Both ftrace and perf are core Linux tracing tools, included in the kernel source. Your system probably has ftrace already, and perf is often just a package add (see Prerequisites).
> These tools are designed to be easy to install (fewest dependencies), provide advanced performance observability, and be simple to use: do one thing and do it well. This collection was created by Brendan Gregg (author of the DTraceToolkit).
> Many of these tools employ workarounds so that functionality is possible on existing Linux kernels. Because of this, many tools have caveats (see man pages), and their implementation should be considered a placeholder until future kernel features, or new tracing subsystems, are added.
> These are intended for Linux 3.2 and newer kernels. For Linux 2.6.x, see Warnings.
# Using ftrace:

- [iosnoop](https://github.com/brendangregg/perf-tools/blob/master/iosnoop): trace disk I/O with details including latency. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/iosnoop_example.txt).

- [iolatency](https://github.com/brendangregg/perf-tools/blob/master/iolatency): summarize disk I/O latency as a histogram. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/iolatency_example.txt).

- [execsnoop](https://github.com/brendangregg/perf-tools/blob/master/execsnoop):系统级别跟踪新的进程的执行. trace process exec()/execve with command line argument details. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/execsnoop_example.txt).

- [opensnoop](https://github.com/brendangregg/perf-tools/blob/master/opensnoop): trace open() syscalls showing filenames. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/opensnoop_example.txt).

- [killsnoop](https://github.com/brendangregg/perf-tools/blob/master/killsnoop): trace kill() signals showing process and signal details. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/killsnoop_example.txt).

- fs/[cachestat](https://github.com/brendangregg/perf-tools/blob/master/fs/cachestat): basic cache hit/miss statistics for the Linux page cache. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/cachestat_example.txt).

- net/[tcpretrans](https://github.com/brendangregg/perf-tools/blob/master/net/tcpretrans): show TCP retransmits, with address and other details. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/tcpretrans_example.txt).

- system/[tpoint](https://github.com/brendangregg/perf-tools/blob/master/system/tpoint): trace a given tracepoint. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/tpoint_example.txt).

- kernel/[funccount](https://github.com/brendangregg/perf-tools/blob/master/kernel/funccount): count kernel function calls, matching a string with wildcards. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/funccount_example.txt).

- kernel/[functrace](https://github.com/brendangregg/perf-tools/blob/master/kernel/functrace): trace kernel function calls, matching a string with wildcards. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/functrace_example.txt).

- kernel/[funcslower](https://github.com/brendangregg/perf-tools/blob/master/kernel/funcslower): trace kernel functions slower than a threshold. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/funcslower_example.txt).

- kernel/[funcgraph](https://github.com/brendangregg/perf-tools/blob/master/kernel/funcgraph): trace a graph of kernel function calls, showing children and times. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/funcgraph_example.txt).

- kernel/[kprobe](https://github.com/brendangregg/perf-tools/blob/master/kernel/kprobe): dynamically trace a kernel function call or its return, with variables. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/kprobe_example.txt).

- user/[uprobe](https://github.com/brendangregg/perf-tools/blob/master/user/uprobe): dynamically trace a user-level function call or its return, with variables. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/uprobe_example.txt).

- tools/[reset-ftrace](https://github.com/brendangregg/perf-tools/blob/master/tools/reset-ftrace): reset ftrace state if needed. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/reset-ftrace_example.txt).

# Using perf_events:

- misc/[perf-stat-hist](https://github.com/brendangregg/perf-tools/blob/master/misc/perf-stat-hist): power-of aggregations for tracepoint variables. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/perf-stat-hist_example.txt).

- [syscount](https://github.com/brendangregg/perf-tools/blob/master/syscount): 系统级别统计系统调用.count syscalls by syscall or process. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/syscount_example.txt).

- disk/[bitesize](https://github.com/brendangregg/perf-tools/blob/master/disk/bitesize): histogram summary of disk I/O size. [Examples](https://github.com/brendangregg/perf-tools/blob/master/examples/bitesize_example.txt).

# Using eBPF:

- As a preview of things to come, see the bcc tracing [Tools section](https://github.com/iovisor/bcc/blob/master/README.md#tracing). These use [bcc](https://github.com/iovisor/bcc), a front end for using [eBPF](http://www.brendangregg.com/blog/2015-05-15/ebpf-one-small-step.html). bcc+eBPF will allow some of these tools to be rewritten and improved, and additional tools to be created.
