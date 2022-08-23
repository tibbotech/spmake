# spmake
Makefile to build the ISPBOOOT.BIN image

How to use:

1) check values in sp_make.inc.mk
2) run
```
make -f ./sp_make.mk
```

Target file ISPBOOOT.BIN is an image file separated for partitions:
| Offset   | Binary       | For CPU  |
| -------- | ------------ | -------- |
| 0xFFFFFF | XBoot        | a926     |
| 0xFFFFFF | B-chip fw    | a926     |
| 0xFFFFFF | U-Boot       | cortexa9 |
| 0xFFFFFF | DTS          |    -     |
| 0xFFFFFF | Linux Kernel | cortexa9 |
| 0xFFFFFF | RootFS       | cortexa9 |

If the file(s) are not exist script try to download it from

https://archives.tibbo.com/downloads/LTPS/FW/LTPPg2/parts/


