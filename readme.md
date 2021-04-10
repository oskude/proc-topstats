# proc-topstats

a linux kernel module that provides simple system stats in `/proc/topstats/*`.

```
$> cat /proc/topstats/cpu
1845064 157643
1845417 157995
1845303 157768
1844202 157017
$> cat /proc/topstats/mem
8017568 3449556 2057216
```

## `/proc/topstats/cpu`

```
<total> <used>
```

- _line number_ implies cpu number.
- `<total>` _jiffies_ elapsed.
- `<used>` amount of `<total>` in use by programs, that cannot be used by other programs.

## `/proc/topstats/mem`

```
<total> <used> <cached>
```

- `<total>` kilobytes of memory.
- `<used>` amount of `<total>` in use by programs, that can not be used by other programs.
- `<cached>` amount of `<used>` in use for caches, that can be freed by user.
