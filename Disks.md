# Disks

## Resizing 

After resizing in the Proxmox VE web the following commands can be useful to expand a partition

```shell
$ sudo lvresize --resizefs --extents +100%FREE /dev/mapper/ubuntu--vg-ubuntu--lv
$ sudo pvresize /dev/sda3
```
