# cryptfile

A set of tools to make managing encrypted filesystem-in-a-files easier.

Usage:

    # Create a new LUKS file
    cryptfile format example.img 32M

    # Mount the LUKS file to `mnt`
    cryptfile mount example.img mnt

    # Unmount
    cryptfile umount example.img


## TODO

* More control over LUKS options
* Test and fix resizing (shrinking seems to be broken!)


## Dependencies

* Python 3
* Start mount tools: `mount`, `umount`, `losetup`
* Cryptsetup (`cryptsetup-bin`, `sys-fs/cryptsetup`)
