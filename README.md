# ALUs experiments

Various benchmarks and tests in order to determine the best strategy for optimizations.
Has been applied for [ALUs](https://github.com/cgi-estonia-space/ALUs) and [asar-focus](https://github.com/cgi-estonia-space/asar-focus) processors.

## Host memory allocation benchmark

Lenovo Legion 5\
CPU: Intel i7 10750h\
RAM: 32GB\
    product: Comet Lake PCH Shared SRAM\
    vendor: Intel Corporation\
    width: 64 bits\
    clock: 33MHz (30.3ns)


```
Initializing 1000MiB
Init times (buffer creation) ms
ALLOCATE_ONLY                           0
ALLOCATE_WRITE_SINGLE_ITEM              0
ALLOCATE_READ                           113
ALLOCATE_MMAP                           146
ALLOCATE_MADVISE                        146
ALLOCATE_WRITE_SINGLE_BYTE_TO_EACH_PAGE 217
ALLOCATE_MEMSET_ALL_BUFFER              263

Write times ms
ALLOCATE_MEMSET_ALL_BUFFER              64
ALLOCATE_WRITE_SINGLE_BYTE_TO_EACH_PAGE 64
ALLOCATE_MADVISE                        64
ALLOCATE_MMAP                           68
ALLOCATE_ONLY                           305
ALLOCATE_WRITE_SINGLE_ITEM              310
ALLOCATE_READ                           331

Total times ms
ALLOCATE_MADVISE                        210
ALLOCATE_MMAP                           214
ALLOCATE_WRITE_SINGLE_BYTE_TO_EACH_PAGE 282
ALLOCATE_ONLY                           305
ALLOCATE_WRITE_SINGLE_ITEM              310
ALLOCATE_MEMSET_ALL_BUFFER              328
ALLOCATE_READ                           445
```
