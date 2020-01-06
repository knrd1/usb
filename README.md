# Test USB disk write and read speed / USB 2.0 - USB 3.0 - USB 3.1 - USB 3.1 Type C

## 1. USB 2.0:

### a) dd: TEST Disk WRITE Speed:

```
# time dd if=/dev/zero of=/mnt/usb_2.0/test.img bs=1G count=1 oflag=dsync
1+0 records in
1+0 records out
1073741824 bytes (1.1 GB, 1.0 GiB) copied, 175.153 s, 6.1 MB/s

real	2m55.210s
user	0m0.000s
sys   0m0.699s
```

### b) dd: TEST Disk READ Speed:

```
# /sbin/sysctl -w vm.drop_caches=3
vm.drop_caches = 3
# time dd if=/mnt/usb_2.0/test.img of=/dev/null bs=1G count=1 oflag=dsync
1+0 records in
1+0 records out
1073741824 bytes (1.1 GB, 1.0 GiB) copied, 78.0803 s, 13.8 MB/s

real	1m18.149s
user	0m0.001s
sys   0m2.400s
```

## 2) USB 3.0:

### a) dd: TEST Disk WRITE Speed:

```
# time dd if=/dev/zero of=/mnt/usb_3.0/test.img bs=1G count=1 oflag=dsync
1+0 records in
1+0 records out
1073741824 bytes (1.1 GB, 1.0 GiB) copied, 72.9299 s, 14.7 MB/s

real	1m13.003s
user	0m0.000s
sys   0m1.160s
```

### b) dd: TEST Disk READ Speed:

```
# time dd if=/mnt/usb_3.0/test.img of=/dev/null bs=1G count=1 oflag=dsync
1+0 records in
1+0 records out
1073741824 bytes (1.1 GB, 1.0 GiB) copied, 8.10894 s, 132 MB/s

real	0m8.169s
user	0m0.004s
sys   0m1.722s
```

## 3) USB 3.1:

### a) dd: TEST Disk WRITE Speed:

```
# time dd if=/dev/zero of=/mnt/usb_3.1/test.img bs=1G count=1 oflag=dsync
1+0 records in
1+0 records out
1073741824 bytes (1.1 GB, 1.0 GiB) copied, 19.5971 s, 54.8 MB/s

real	0m19.679s
user	0m0.000s
sys   0m1.167s
```

### b) dd: TEST Disk READ Speed:

```
# /sbin/sysctl -w vm.drop_caches=3
vm.drop_caches = 3
# time dd if=/mnt/usb_3.1/test.img of=/dev/null bs=1G count=1 oflag=dsync
1+0 records in
1+0 records out
1073741824 bytes (1.1 GB, 1.0 GiB) copied, 7.97046 s, 135 MB/s

real	0m8.049s
user	0m0.000s
sys   0m1.772s
```

## 4) USB 3.1 Type C:

### a) dd: TEST Disk WRITE Speed:

```
# time dd if=/dev/zero of=/mnt/usb_3.1-type-c/test.img bs=1G count=1 oflag=dsync
1+0 records in
1+0 records out
1073741824 bytes (1.1 GB, 1.0 GiB) copied, 20.1686 s, 53.2 MB/s

real	0m20.243s
user	0m0.005s
sys   0m1.229s
```

### b) dd: TEST Disk READ Speed:

```
# /sbin/sysctl -w vm.drop_caches=3
vm.drop_caches = 3
# time dd if=/mnt/usb_3.1-type-c/test.img of=/dev/null bs=1G count=1 oflag=dsync
1+0 records in
1+0 records out
1073741824 bytes (1.1 GB, 1.0 GiB) copied, 8.09574 s, 133 MB/s

real	0m8.168s
user	0m0.000s
sys   0m1.684s
```
