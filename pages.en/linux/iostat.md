# iostat

> Report statistics for devices and partitions.
> More information: <https://manned.org/iostat>.

- Display a report of CPU and disk statistics since system startup:

`iostat`

- Display a report of CPU and disk statistics with units converted to megabytes:

`iostat -m`

- Display CPU statistics:

`iostat -c`

- Display disk statistics with disk names (including LVM):

`iostat -N`

- Display extended disk statistics with disk names for device "sda":

`iostat -xN {{sda}}`

- Display incremental reports of CPU and disk statistics every 2 seconds:

`iostat {{2}}`

- 扩展输出

`iostat -sxz {{1}}`

- Useful

`iostat -dmstxz -p ALL 1`

# Option

- -c: Display CPU report 
- -d: Display disk report 
- -k: Use kilobytes instead of (512-byte) blocks 
- -m: Use megabytes instead of (512-byte) blocks 
- -p: Include per-partition statistics 
- -t: Timestamp output 
- -x: Extended statistics 
- -s: Short (narrow) output 
- -z: Skip displaying zero-activity summaries

# Result

- tps: Transactions per second (IOPS) 
- kB_read/s, kB_wrtn/s: Kilobytes read per second, and written per second 
- kB_read, kB_wrtn: Total kilobytes read and written

- tps: Transactions issued per second (IOPS) 
- kB/s: Kbytes per second 
- rqm/s: Requests queued and merged per second 
- await: Average I/O response time, including time queued in the OS and the I/O response time of the device (ms) 
- aqu-sz: Average number of requests both waiting in the driver request queue and active on the device 
- areq-sz: Average request size in Kbytes 
- %util: Percent of time the device was busy processing I/O requests (utilization)
- r/s, w/s, d/s, f/s: Read, write, discard, and flush requests completed from the disk device per second (after merges) 
- rkB/s, wkB/s, dkB/s: Read, write, and discard Kbytes from the disk device per second 
- %rrqm/s, %wrqm/s, %drqm/s: Read, write, and discard requests queued and merged as a percentage of the total requests for that type 
- r_await, w_await, d_await, f_await: Read, write, discard, and flush average response time, including time queued in the OS and the response time from the device (ms) 
- rareq-sz, wareq-sz, dareq-sz: Read, write, and discard average size (Kbytes)
- 
