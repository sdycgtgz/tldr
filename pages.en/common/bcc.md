# bcc

> BCC is a toolkit for creating efficient kernel tracing and manipulation programs, and includes several useful tools and examples. It makes use of extended BPF (Berkeley Packet Filters), formally known as eBPF, a new feature that was first added to Linux 3.15. Much of what BCC uses requires Linux 4.1 and above.
> More information: <https://github.com/iovisor/bcc>.
> 其中`profile`等用法可参考<<性能之巅>>第二版6.6.14-6.6.19和第15章

# Tracing



# Examples



- examples/tracing/[bitehist.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/bitehist.py): Block I/O size histogram. [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/bitehist_example.txt).
- examples/tracing/[disksnoop.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/disksnoop.py): Trace block device I/O latency. [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/disksnoop_example.txt).
- examples/[hello_world.py](https://github.com/iovisor/bcc/blob/master/examples/hello_world.py): Prints "Hello, World!" for new processes.
- examples/tracing/[mysqld_query.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/mysqld_query.py): Trace MySQL server queries using USDT probes. [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/mysqld_query_example.txt).
- examples/tracing/[nodejs_http_server.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/nodejs_http_server.py): Trace Node.js HTTP server requests using USDT probes. [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/nodejs_http_server_example.txt).
- examples/tracing/[stacksnoop](https://github.com/iovisor/bcc/blob/master/examples/tracing/stacksnoop.py): Trace a kernel function and print all kernel stack traces. [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/stacksnoop_example.txt).
- tools/[statsnoop](https://github.com/iovisor/bcc/blob/master/tools/statsnoop.py): Trace stat() syscalls. [Examples](https://github.com/iovisor/bcc/blob/master/tools/statsnoop_example.txt).
- examples/tracing/[task_switch.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/task_switch.py): Count task switches with from and to PIDs.
- examples/tracing/[tcpv4connect.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/tcpv4connect.py): Trace TCP IPv4 active connections. [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/tcpv4connect_example.txt).
- examples/tracing/[trace_fields.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/trace_fields.py): Simple example of printing fields from traced events.
- examples/tracing/[undump.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/undump.py): Dump UNIX socket packets. [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/undump_example.txt)
- examples/tracing/[urandomread.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/urandomread.py): A kernel tracepoint example, which traces random:urandom_read. [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/urandomread_example.txt).
- examples/tracing/[vfsreadlat.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/vfsreadlat.py) examples/tracing/[vfsreadlat.c](https://github.com/iovisor/bcc/blob/master/examples/tracing/vfsreadlat.c): VFS read latency distribution. [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/vfsreadlat_example.txt).
- examples/tracing/[kvm_hypercall.py](https://github.com/iovisor/bcc/blob/master/examples/tracing/kvm_hypercall.py): Conditional static kernel tracepoints for KVM entry, exit and hypercall [Examples](https://github.com/iovisor/bcc/blob/master/examples/tracing/kvm_hypercall.txt).

# Tools

- tools/[argdist](https://github.com/iovisor/bcc/blob/master/tools/argdist.py): Display function parameter values as a histogram or frequency count. [Examples](https://github.com/iovisor/bcc/blob/master/tools/argdist_example.txt).
- tools/[bashreadline](https://github.com/iovisor/bcc/blob/master/tools/bashreadline.py): Print entered bash commands system wide. [Examples](https://github.com/iovisor/bcc/blob/master/tools/bashreadline_example.txt).
- tools/[bpflist](https://github.com/iovisor/bcc/blob/master/tools/bpflist.py): Display processes with active BPF programs and maps. [Examples](https://github.com/iovisor/bcc/blob/master/tools/bpflist_example.txt).
- tools/[capable](https://github.com/iovisor/bcc/blob/master/tools/capable.py): Trace security capability checks. [Examples](https://github.com/iovisor/bcc/blob/master/tools/capable_example.txt).
- tools/[compactsnoop](https://github.com/iovisor/bcc/blob/master/tools/compactsnoop.py): Trace compact zone events with PID and latency. [Examples](https://github.com/iovisor/bcc/blob/master/tools/compactsnoop_example.txt).
- tools/[criticalstat](https://github.com/iovisor/bcc/blob/master/tools/criticalstat.py): Trace and report long atomic critical sections in the kernel. [Examples](https://github.com/iovisor/bcc/blob/master/tools/criticalstat_example.txt)
- tools/[deadlock](https://github.com/iovisor/bcc/blob/master/tools/deadlock.py): Detect potential deadlocks on a running process. [Examples](https://github.com/iovisor/bcc/blob/master/tools/deadlock_example.txt).
- tools/[drsnoop](https://github.com/iovisor/bcc/blob/master/tools/drsnoop.py): Trace direct reclaim events with PID and latency. [Examples](https://github.com/iovisor/bcc/blob/master/tools/drsnoop_example.txt).
- tools/[funccount](https://github.com/iovisor/bcc/blob/master/tools/funccount.py): Count kernel function calls. [Examples](https://github.com/iovisor/bcc/blob/master/tools/funccount_example.txt).
- tools/[inject](https://github.com/iovisor/bcc/blob/master/tools/inject.py): Targeted error injection with call chain and predicates [Examples](https://github.com/iovisor/bcc/blob/master/tools/inject_example.txt).
- tools/[klockstat](https://github.com/iovisor/bcc/blob/master/tools/klockstat.py): Traces kernel mutex lock events and display locks statistics. [Examples](https://github.com/iovisor/bcc/blob/master/tools/klockstat_example.txt).
- tools/[opensnoop](https://github.com/iovisor/bcc/blob/master/tools/opensnoop.py): Trace open() syscalls. [Examples](https://github.com/iovisor/bcc/blob/master/tools/opensnoop_example.txt).
- tools/[readahead](https://github.com/iovisor/bcc/blob/master/tools/readahead.py): Show performance of read-ahead cache [Examples](https://github.com/iovisor/bcc/blob/master/tools/readahead_example.txt).
- tools/[reset-trace](https://github.com/iovisor/bcc/blob/master/tools/reset-trace.sh): Reset the state of tracing. Maintenance tool only. [Examples](https://github.com/iovisor/bcc/blob/master/tools/reset-trace_example.txt).
- tools/[stackcount](https://github.com/iovisor/bcc/blob/master/tools/stackcount.py): Count kernel function calls and their stack traces. [Examples](https://github.com/iovisor/bcc/blob/master/tools/stackcount_example.txt).
- tools/[syncsnoop](https://github.com/iovisor/bcc/blob/master/tools/syncsnoop.py): Trace sync() syscall. [Examples](https://github.com/iovisor/bcc/blob/master/tools/syncsnoop_example.txt).
- tools/[threadsnoop](https://github.com/iovisor/bcc/blob/master/tools/threadsnoop.py): List new thread creation. [Examples](https://github.com/iovisor/bcc/blob/master/tools/threadsnoop_example.txt).
- tools/[tplist](https://github.com/iovisor/bcc/blob/master/tools/tplist.py): Display kernel tracepoints or USDT probes and their formats. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tplist_example.txt).
- tools/[trace](https://github.com/iovisor/bcc/blob/master/tools/trace.py): Trace arbitrary functions, with filters. [Examples](https://github.com/iovisor/bcc/blob/master/tools/trace_example.txt).
- tools/[ttysnoop](https://github.com/iovisor/bcc/blob/master/tools/ttysnoop.py): Watch live output from a tty or pts device. [Examples](https://github.com/iovisor/bcc/blob/master/tools/ttysnoop_example.txt).
- tools/[ucalls](https://github.com/iovisor/bcc/blob/master/tools/lib/ucalls.py): Summarize method calls or Linux syscalls in high-level languages. [Examples](https://github.com/iovisor/bcc/blob/master/tools/lib/ucalls_example.txt).
- tools/[uflow](https://github.com/iovisor/bcc/blob/master/tools/lib/uflow.py): Print a method flow graph in high-level languages. [Examples](https://github.com/iovisor/bcc/blob/master/tools/lib/uflow_example.txt).
- tools/[ugc](https://github.com/iovisor/bcc/blob/master/tools/lib/ugc.py): Trace garbage collection events in high-level languages. [Examples](https://github.com/iovisor/bcc/blob/master/tools/lib/ugc_example.txt).
- tools/[uobjnew](https://github.com/iovisor/bcc/blob/master/tools/lib/uobjnew.py): Summarize object allocation events by object type and number of bytes allocated. [Examples](https://github.com/iovisor/bcc/blob/master/tools/lib/uobjnew_example.txt).
- tools/[ustat](https://github.com/iovisor/bcc/blob/master/tools/lib/ustat.py): Collect events such as GCs, thread creations, object allocations, exceptions and more in high-level languages. [Examples](https://github.com/iovisor/bcc/blob/master/tools/lib/ustat_example.txt).
- tools/[uthreads](https://github.com/iovisor/bcc/blob/master/tools/lib/uthreads.py): Trace thread creation events in Java and raw pthreads. [Examples](https://github.com/iovisor/bcc/blob/master/tools/lib/uthreads_example.txt).

# Memory and Process Tools



- tools/[execsnoop](https://github.com/iovisor/bcc/blob/master/tools/execsnoop.py): Trace new processes via exec() syscalls. [Examples](https://github.com/iovisor/bcc/blob/master/tools/execsnoop_example.txt).
- tools/[exitsnoop](https://github.com/iovisor/bcc/blob/master/tools/exitsnoop.py): Trace process termination (exit and fatal signals). [Examples](https://github.com/iovisor/bcc/blob/master/tools/exitsnoop_example.txt).
- tools/[killsnoop](https://github.com/iovisor/bcc/blob/master/tools/killsnoop.py): Trace signals issued by the kill() syscall. [Examples](https://github.com/iovisor/bcc/blob/master/tools/killsnoop_example.txt).
- tools/[kvmexit](https://github.com/iovisor/bcc/blob/master/tools/kvmexit.py): Display the exit_reason and its statistics of each vm exit. [Examples](https://github.com/iovisor/bcc/blob/master/tools/kvmexit_example.txt).
- tools/[memleak](https://github.com/iovisor/bcc/blob/master/tools/memleak.py): Display outstanding memory allocations to find memory leaks. [Examples](https://github.com/iovisor/bcc/blob/master/tools/memleak_example.txt).
- tools/[oomkill](https://github.com/iovisor/bcc/blob/master/tools/oomkill.py): Trace the out-of-memory (OOM) killer. [Examples](https://github.com/iovisor/bcc/blob/master/tools/oomkill_example.txt).
- tools/[pidpersec](https://github.com/iovisor/bcc/blob/master/tools/pidpersec.py): Count new processes (via fork). [Examples](https://github.com/iovisor/bcc/blob/master/tools/pidpersec_example.txt).
- tools/[rdmaucma](https://github.com/iovisor/bcc/blob/master/tools/rdmaucma.py): Trace RDMA Userspace Connection Manager Access events. [Examples](https://github.com/iovisor/bcc/blob/master/tools/rdmaucma_example.txt).
- tools/[shmsnoop](https://github.com/iovisor/bcc/blob/master/tools/shmsnoop.py): Trace System V shared memory syscalls. [Examples](https://github.com/iovisor/bcc/blob/master/tools/shmsnoop_example.txt).
- tools/[slabratetop](https://github.com/iovisor/bcc/blob/master/tools/slabratetop.py): Kernel SLAB/SLUB memory cache allocation rate top. [Examples](https://github.com/iovisor/bcc/blob/master/tools/slabratetop_example.txt).

# Performance and Time Tools



- tools/[dbslower](https://github.com/iovisor/bcc/blob/master/tools/dbslower.py): Trace MySQL/PostgreSQL queries slower than a threshold. [Examples](https://github.com/iovisor/bcc/blob/master/tools/dbslower_example.txt).
- tools/[dbstat](https://github.com/iovisor/bcc/blob/master/tools/dbstat.py): Summarize MySQL/PostgreSQL query latency as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/dbstat_example.txt).
- tools/[funcinterval](https://github.com/iovisor/bcc/blob/master/tools/funcinterval.py): Time interval between the same function as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/funcinterval_example.txt).
- tools/[funclatency](https://github.com/iovisor/bcc/blob/master/tools/funclatency.py): Time functions and show their latency distribution. [Examples](https://github.com/iovisor/bcc/blob/master/tools/funclatency_example.txt).
- tools/[funcslower](https://github.com/iovisor/bcc/blob/master/tools/funcslower.py): Trace slow kernel or user function calls. [Examples](https://github.com/iovisor/bcc/blob/master/tools/funcslower_example.txt).
- tools/[hardirqs](https://github.com/iovisor/bcc/blob/master/tools/hardirqs.py): Measure hard IRQ (hard interrupt) event time. [Examples](https://github.com/iovisor/bcc/blob/master/tools/hardirqs_example.txt).
- tools/[mysqld_qslower](https://github.com/iovisor/bcc/blob/master/tools/mysqld_qslower.py): Trace MySQL server queries slower than a threshold. [Examples](https://github.com/iovisor/bcc/blob/master/tools/mysqld_qslower_example.txt).
- tools/[ppchcalls](https://github.com/iovisor/bcc/blob/master/tools/ppchcalls.py): Summarize ppc hcall counts and latencies. [Examples](https://github.com/iovisor/bcc/blob/master/tools/ppchcalls_example.txt).
- tools/[softirqs](https://github.com/iovisor/bcc/blob/master/tools/softirqs.py): Measure soft IRQ (soft interrupt) event time. [Examples](https://github.com/iovisor/bcc/blob/master/tools/softirqs_example.txt).
- tools/[syscount](https://github.com/iovisor/bcc/blob/master/tools/syscount.py): Summarize syscall counts and latencies. [Examples](https://github.com/iovisor/bcc/blob/master/tools/syscount_example.txt).

# CPU and Scheduler Tools



- tools/[cpudist](https://github.com/iovisor/bcc/blob/master/tools/cpudist.py): Summarize on- and off-CPU time per task as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/cpudist_example.txt)
- tools/[cpuunclaimed](https://github.com/iovisor/bcc/blob/master/tools/cpuunclaimed.py): Sample CPU run queues and calculate unclaimed idle CPU. [Examples](https://github.com/iovisor/bcc/blob/master/tools/cpuunclaimed_example.txt)
- tools/[llcstat](https://github.com/iovisor/bcc/blob/master/tools/llcstat.py): Summarize CPU cache references and misses by process. [Examples](https://github.com/iovisor/bcc/blob/master/tools/llcstat_example.txt).
- tools/[offcputime](https://github.com/iovisor/bcc/blob/master/tools/offcputime.py): Summarize off-CPU time by kernel stack trace. [Examples](https://github.com/iovisor/bcc/blob/master/tools/offcputime_example.txt).
- tools/[offwaketime](https://github.com/iovisor/bcc/blob/master/tools/offwaketime.py): Summarize blocked time by kernel off-CPU stack and waker stack. [Examples](https://github.com/iovisor/bcc/blob/master/tools/offwaketime_example.txt).
- tools/[profile](https://github.com/iovisor/bcc/blob/master/tools/profile.py): Profile CPU usage by sampling stack traces at a timed interval. [Examples](https://github.com/iovisor/bcc/blob/master/tools/profile_example.txt).
- tools/[runqlat](https://github.com/iovisor/bcc/blob/master/tools/runqlat.py): Run queue (scheduler) latency as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/runqlat_example.txt).
- tools/[runqlen](https://github.com/iovisor/bcc/blob/master/tools/runqlen.py): Run queue length as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/runqlen_example.txt).
- tools/[runqslower](https://github.com/iovisor/bcc/blob/master/tools/runqslower.py): Trace long process scheduling delays. [Examples](https://github.com/iovisor/bcc/blob/master/tools/runqslower_example.txt).
- tools/[wakeuptime](https://github.com/iovisor/bcc/blob/master/tools/wakeuptime.py): Summarize sleep to wakeup time by waker kernel stack. [Examples](https://github.com/iovisor/bcc/blob/master/tools/wakeuptime_example.txt).
- tools/[wqlat](https://github.com/iovisor/bcc/blob/master/tools/wqlat.py): Summarize work waiting latency on workqueue. [Examples](https://github.com/iovisor/bcc/blob/master/tools/wqlat_example.txt).

# Network and Sockets Tools



- tools/[gethostlatency](https://github.com/iovisor/bcc/blob/master/tools/gethostlatency.py): Show latency for getaddrinfo/gethostbyname[2] calls. [Examples](https://github.com/iovisor/bcc/blob/master/tools/gethostlatency_example.txt).
- tools/[bindsnoop](https://github.com/iovisor/bcc/blob/master/tools/bindsnoop.py): Trace IPv4 and IPv6 bind() system calls (bind()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/bindsnoop_example.txt).
- tools/[netqtop](https://github.com/iovisor/bcc/blob/master/tools/netqtop.py) tools/[netqtop.c](https://github.com/iovisor/bcc/blob/master/tools/netqtop.c): Trace and display packets distribution on NIC queues. [Examples](https://github.com/iovisor/bcc/blob/master/tools/netqtop_example.txt).
- tools/[sofdsnoop](https://github.com/iovisor/bcc/blob/master/tools/sofdsnoop.py): Trace FDs passed through unix sockets. [Examples](https://github.com/iovisor/bcc/blob/master/tools/sofdsnoop_example.txt).
- tools/[solisten](https://github.com/iovisor/bcc/blob/master/tools/solisten.py): Trace TCP socket listen. [Examples](https://github.com/iovisor/bcc/blob/master/tools/solisten_example.txt).
- tools/[sslsniff](https://github.com/iovisor/bcc/blob/master/tools/sslsniff.py): Sniff OpenSSL written and readed data. [Examples](https://github.com/iovisor/bcc/blob/master/tools/sslsniff_example.txt).
- tools/[tcpaccept](https://github.com/iovisor/bcc/blob/master/tools/tcpaccept.py): Trace TCP passive connections (accept()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpaccept_example.txt).
- tools/[tcpconnect](https://github.com/iovisor/bcc/blob/master/tools/tcpconnect.py): Trace TCP active connections (connect()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpconnect_example.txt).
- tools/[tcpconnlat](https://github.com/iovisor/bcc/blob/master/tools/tcpconnlat.py): Trace TCP active connection latency (connect()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpconnlat_example.txt).
- tools/[tcpdrop](https://github.com/iovisor/bcc/blob/master/tools/tcpdrop.py): Trace kernel-based TCP packet drops with details. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpdrop_example.txt).
- tools/[tcplife](https://github.com/iovisor/bcc/blob/master/tools/tcplife.py): Trace TCP sessions and summarize lifespan. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcplife_example.txt).
- tools/[tcpretrans](https://github.com/iovisor/bcc/blob/master/tools/tcpretrans.py): Trace TCP retransmits and TLPs. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpretrans_example.txt).
- tools/[tcprtt](https://github.com/iovisor/bcc/blob/master/tools/tcprtt.py): Trace TCP round trip time. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcprtt_example.txt).
- tools/[tcpstates](https://github.com/iovisor/bcc/blob/master/tools/tcpstates.py): Trace TCP session state changes with durations. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpstates_example.txt).
- tools/[tcpsubnet](https://github.com/iovisor/bcc/blob/master/tools/tcpsubnet.py): Summarize and aggregate TCP send by subnet. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpsubnet_example.txt).
- tools/[tcpsynbl](https://github.com/iovisor/bcc/blob/master/tools/tcpsynbl.py): Show TCP SYN backlog. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpsynbl_example.txt).
- tools/[tcptop](https://github.com/iovisor/bcc/blob/master/tools/tcptop.py): Summarize TCP send/recv throughput by host. Top for TCP. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcptop_example.txt).
- tools/[tcptracer](https://github.com/iovisor/bcc/blob/master/tools/tcptracer.py): Trace TCP established connections (connect(), accept(), close()). [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcptracer_example.txt).
- tools/[tcpcong](https://github.com/iovisor/bcc/blob/master/tools/tcpcong.py): Trace TCP socket congestion control status duration. [Examples](https://github.com/iovisor/bcc/blob/master/tools/tcpcong_example.txt).

# Storage and Filesystems Tools



- tools/[bitesize](https://github.com/iovisor/bcc/blob/master/tools/bitesize.py): Show per process I/O size histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/bitesize_example.txt).
- tools/[cachestat](https://github.com/iovisor/bcc/blob/master/tools/cachestat.py): Trace page cache hit/miss ratio. [Examples](https://github.com/iovisor/bcc/blob/master/tools/cachestat_example.txt).
- tools/[cachetop](https://github.com/iovisor/bcc/blob/master/tools/cachetop.py): Trace page cache hit/miss ratio by processes. [Examples](https://github.com/iovisor/bcc/blob/master/tools/cachetop_example.txt).
- tools/[dcsnoop](https://github.com/iovisor/bcc/blob/master/tools/dcsnoop.py): Trace directory entry cache (dcache) lookups. [Examples](https://github.com/iovisor/bcc/blob/master/tools/dcsnoop_example.txt).
- tools/[dcstat](https://github.com/iovisor/bcc/blob/master/tools/dcstat.py): Directory entry cache (dcache) stats. [Examples](https://github.com/iovisor/bcc/blob/master/tools/dcstat_example.txt).
- tools/[biolatency](https://github.com/iovisor/bcc/blob/master/tools/biolatency.py): Summarize block device I/O latency as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/biolatency_example.txt).
- tools/[biotop](https://github.com/iovisor/bcc/blob/master/tools/biotop.py): Top for disks: Summarize block device I/O by process. [Examples](https://github.com/iovisor/bcc/blob/master/tools/biotop_example.txt).
- tools/[biopattern](https://github.com/iovisor/bcc/blob/master/tools/biopattern.py): Identify random/sequential disk access patterns. [Examples](https://github.com/iovisor/bcc/blob/master/tools/biopattern_example.txt).
- tools/[biosnoop](https://github.com/iovisor/bcc/blob/master/tools/biosnoop.py): Trace block device I/O with PID and latency. [Examples](https://github.com/iovisor/bcc/blob/master/tools/biosnoop_example.txt).
- tools/[dirtop](https://github.com/iovisor/bcc/blob/master/tools/dirtop.py): File reads and writes by directory. Top for directories. [Examples](https://github.com/iovisor/bcc/blob/master/tools/dirtop_example.txt).
- tools/[filelife](https://github.com/iovisor/bcc/blob/master/tools/filelife.py): Trace the lifespan of short-lived files. [Examples](https://github.com/iovisor/bcc/blob/master/tools/filelife_example.txt).
- tools/[filegone](https://github.com/iovisor/bcc/blob/master/tools/filegone.py): Trace why file gone (deleted or renamed). [Examples](https://github.com/iovisor/bcc/blob/master/tools/filegone_example.txt).
- tools/[fileslower](https://github.com/iovisor/bcc/blob/master/tools/fileslower.py): Trace slow synchronous file reads and writes. [Examples](https://github.com/iovisor/bcc/blob/master/tools/fileslower_example.txt).
- tools/[filetop](https://github.com/iovisor/bcc/blob/master/tools/filetop.py): File reads and writes by filename and process. Top for files. [Examples](https://github.com/iovisor/bcc/blob/master/tools/filetop_example.txt).
- tools/[mdflush](https://github.com/iovisor/bcc/blob/master/tools/mdflush.py): Trace md flush events. [Examples](https://github.com/iovisor/bcc/blob/master/tools/mdflush_example.txt).
- tools/[mountsnoop](https://github.com/iovisor/bcc/blob/master/tools/mountsnoop.py): Trace mount and umount syscalls system-wide. [Examples](https://github.com/iovisor/bcc/blob/master/tools/mountsnoop_example.txt).
- tools/[virtiostat](https://github.com/iovisor/bcc/blob/master/tools/virtiostat.py): Show VIRTIO device IO statistics. [Examples](https://github.com/iovisor/bcc/blob/master/tools/virtiostat_example.txt).

# Filesystems Tools



- tools/[btrfsdist](https://github.com/iovisor/bcc/blob/master/tools/btrfsdist.py): Summarize btrfs operation latency distribution as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/btrfsdist_example.txt).
- tools/[btrfsslower](https://github.com/iovisor/bcc/blob/master/tools/btrfsslower.py): Trace slow btrfs operations. [Examples](https://github.com/iovisor/bcc/blob/master/tools/btrfsslower_example.txt).
- tools/[ext4dist](https://github.com/iovisor/bcc/blob/master/tools/ext4dist.py): Summarize ext4 operation latency distribution as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/ext4dist_example.txt).
- tools/[ext4slower](https://github.com/iovisor/bcc/blob/master/tools/ext4slower.py): Trace slow ext4 operations. [Examples](https://github.com/iovisor/bcc/blob/master/tools/ext4slower_example.txt).
- tools/[nfsslower](https://github.com/iovisor/bcc/blob/master/tools/nfsslower.py): Trace slow NFS operations. [Examples](https://github.com/iovisor/bcc/blob/master/tools/nfsslower_example.txt).
- tools/[nfsdist](https://github.com/iovisor/bcc/blob/master/tools/nfsdist.py): Summarize NFS operation latency distribution as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/nfsdist_example.txt).
- tools/[vfscount](https://github.com/iovisor/bcc/blob/master/tools/vfscount.py): Count VFS calls. [Examples](https://github.com/iovisor/bcc/blob/master/tools/vfscount_example.txt).
- tools/[vfsstat](https://github.com/iovisor/bcc/blob/master/tools/vfsstat.py): Count some VFS calls, with column output. [Examples](https://github.com/iovisor/bcc/blob/master/tools/vfsstat_example.txt).
- tools/[xfsdist](https://github.com/iovisor/bcc/blob/master/tools/xfsdist.py): Summarize XFS operation latency distribution as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/xfsdist_example.txt).
- tools/[xfsslower](https://github.com/iovisor/bcc/blob/master/tools/xfsslower.py): Trace slow XFS operations. [Examples](https://github.com/iovisor/bcc/blob/master/tools/xfsslower_example.txt).
- tools/[zfsdist](https://github.com/iovisor/bcc/blob/master/tools/zfsdist.py): Summarize ZFS operation latency distribution as a histogram. [Examples](https://github.com/iovisor/bcc/blob/master/tools/zfsdist_example.txt).
- tools/[zfsslower](https://github.com/iovisor/bcc/blob/master/tools/zfsslower.py): Trace slow ZFS operations. [Examples](https://github.com/iovisor/bcc/blob/master/tools/zfsslower_example.txt).

# Networking


- examples/networking/[distributed_bridge/](https://github.com/iovisor/bcc/blob/master/examples/networking/distributed_bridge): Distributed bridge example.
- examples/networking/[http_filter/](https://github.com/iovisor/bcc/blob/master/examples/networking/http_filter): Simple HTTP filter example.
- examples/networking/[simple_tc.py](https://github.com/iovisor/bcc/blob/master/examples/networking/simple_tc.py): Simple traffic control example.
- examples/networking/[simulation.py](https://github.com/iovisor/bcc/blob/master/examples/networking/simulation.py): Simulation helper.
- examples/networking/neighbor_sharing/[tc_neighbor_sharing.py](https://github.com/iovisor/bcc/blob/master/examples/networking/neighbor_sharing/tc_neighbor_sharing.py) examples/networking/neighbor_sharing/[tc_neighbor_sharing.c](https://github.com/iovisor/bcc/blob/master/examples/networking/neighbor_sharing/tc_neighbor_sharing.c): Per-IP classification and rate limiting.
- examples/networking/[tunnel_monitor/](https://github.com/iovisor/bcc/blob/master/examples/networking/tunnel_monitor): Efficiently monitor traffic flows.
- examples/networking/vlan_learning/[vlan_learning.py](https://github.com/iovisor/bcc/blob/master/examples/networking/vlan_learning/vlan_learning.py) examples/[vlan_learning.c](https://github.com/iovisor/bcc/blob/master/examples/networking/vlan_learning/vlan_learning.c): Demux Ethernet traffic into worker veth+namespaces.

# BPF Introspection

- introspection/[bps.c](https://github.com/iovisor/bcc/blob/master/introspection/bps.c): List all BPF programs loaded into the kernel. 'ps' for BPF programs. [Examples](https://github.com/iovisor/bcc/blob/master/introspection/bps_example.txt).
