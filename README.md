# Xiaomi_Route_R3A
# MTD Full Backup

Today(20260221), This Route has been broken<br>
So,I upload these Backup Files

# Info
The 2.4GHz SSID Xiaomi_E370_1C8F
The 5GHz SSID Xiaomi_E370_1C8F_5G
admin & wifi password is 00000000
SN=18969/20034507
CountryCode=CN
# From Dmesg Get Information:
```dmesg
[    1.650000] flash manufacture id: 20, device id 70 18
[    1.650000] XM25QH128A/XT25F128A(20 70180000) (16384 Kbytes)
[    1.660000] mtd .name = raspi, .size = 0x01000000 (16M) .erasesize = 0x00010000 (64K) .numeraseregions = 0
[    1.670000] Creating 11 MTD partitions on "raspi":
[    1.670000] 0x000000000000-0x000001000000 : "ALL"
[    1.680000] 0x000000000000-0x000000030000 : "Bootloader"
[    1.690000] 0x000000030000-0x000000040000 : "Config"
[    1.690000] 0x000000040000-0x000000050000 : "Bdata"
[    1.700000] 0x000000050000-0x000000060000 : "Factory"
[    1.710000] 0x000000060000-0x000000070000 : "crash"
[    1.710000] 0x000000070000-0x000000080000 : "crash_syslog"
[    1.720000] 0x000000080000-0x000000180000 : "overlay"
[    1.730000] 0x000000180000-0x0000007e0000 : "OS1"
[    1.730000] mtd: try split OS1 partition
[    1.740000] mtd: split_firmware
[    1.740000] mtd: firmware_partition->size   0x660000
[    1.750000] mtd: firmware_partition->offset 0x180000
[    1.750000] mtd: uimage_len 1425915
[    1.750000] mtd: uimage_len 1441792
[    1.760000] mtd: rootfs_partition->size   0x500000
[    1.760000] mtd: rootfs_partition->offset 0x2e0000
[    1.770000] mtd: partition "rootfs" created automatically, ofs=2E0000, len=500000 
[    1.780000] 0x0000002e0000-0x0000007e0000 : "rootfs"
[    1.780000] 0x0000007e0000-0x000000e40000 : "OS2"
[    1.790000] 0x000000e40000-0x000001000000 : "common"
```

# backup command history
```ash
dd if=/dev/mtd0 of=/tmp/backup/ALL
dd if=/dev/mtd1 of=/tmp/backup/Bootloader
dd if=/dev/mtd2 of=/tmp/backup/Config
dd if=/dev/mtd3 of=/tmp/backup/Bdata
dd if=/dev/mtd4 of=/tmp/backup/Factory
dd if=/dev/mtd5 of=/tmp/backup/crash
dd if=/dev/mtd6 of=/tmp/backup/crash_syslog
dd if=/dev/mtd7 of=/tmp/backup/overlay
dd if=/dev/mtd8 of=/tmp/backup/OS1
dd if=/dev/mtd9 of=/tmp/backup/rootfs
dd if=/dev/mtd10 of=/tmp/backup/OS2
dd if=/dev/mtd11 of=/tmp/backup/common
```
# other
config file has more information

The xz format can be decompressed using 7z.