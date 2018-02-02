# Unmount a volume

```
$ sudo umount -d /dev/xxx
```

Should there be running processes that still uses the volume

- List all processes still using the volume
- Kill all processes using the volume
```
$ fuser -v /mount
$ fuser -k /mount
```
