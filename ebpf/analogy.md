# Here actual EBPF analogy is documented what are we using exactly

## Inodes

* In ext4 systems we get to see inodes

* Here is a reddit post if you want to read more about it.

* They are unique ids for a single file which can be used for filtering

* For ntfs file system the unique id changes to a 8 bit hash

## BPF Maps

* These are used for storing inodes where we use lookup function to get logs of exact file provided via cli

* Events & structures are transferred in maps

## BPF RING BUFFER

* This is a kind of map

* This is use to save logs into memory incase the machine gets slower. By incorporating it we can ensure that logs are not being dropped

* Memory limit increases, along with max entries are 4096, 8192, 16384, 32768

* More on Map Type 'BPF_MAP_TYPE_RINGBUF' - eBPF Docs 

## BPF Per CPU Array

* Kind of a map to store struct in memory

* In order to tackle storage issue as ebpf provides only 512 bytes of storage we preferred BPF_PERCPU_ARRAY which means that only we can utilize storage upto 32KB

* This per-CPU version has a separate array for each logical CPU.

* More on ebpf.io

## EBPF Debug logs

* These are located in /sys/kernel/debug/tracing/trace_pipe

* Do a cat command on the above to read it

