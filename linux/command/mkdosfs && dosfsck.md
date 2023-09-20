1. 设置 FAT 格式分配单元大小（cluster）
```shell
# 分配单元大小为64kb(65536)
linux> sudo mkdosfs -s 128 /path/to/dev
```
2. 查看 MS-DOS FAT 文件系统
```shell
linux> sudo dosfsck -v -n /dev/mmcblk0p1
fsck.fat 4.2 (2021-01-31)
Checking we can access the last sector of the filesystem
Boot sector contents:
System ID "MSDOS5.0"
Media byte 0xf8 (hard disk)
       512 bytes per logical sector
     32768 bytes per cluster
      1168 reserved sectors
First FAT starts at byte 598016 (sector 1168)
         2 FATs, 32 bit entries
   3895296 bytes per FAT (= 7608 sectors)
Root directory start at cluster 2 (arbitrary size)
Data area starts at byte 8388608 (sector 16384)
    973711 data clusters (31906562048 bytes)
63 sectors/track, 255 heads
        32 hidden sectors
  62333920 sectors total
Checking for unused clusters.
Checking free cluster summary.
/dev/mmcblk0p1: 513 files, 908331/973711 clusters
```
从上可以看出 设备 mmcblk0p1 分配单元大小（簇大小，cluster）为32768 即 32kb