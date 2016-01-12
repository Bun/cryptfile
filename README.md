# cryptfile

A tool to make managing encrypted filesystem-in-a-file easier.

Usage:

    # Create a new LUKS file
    sudo cryptfile format example.img 32M

    # Mount the LUKS file to `mnt`
    sudo cryptfile mount example.img mnt

    # If you're mounting for the first time, you should also make the
    # filesystem accessible to you:
    sudo chown `id -u`:`id -g` mnt

    # Unmount
    sudo cryptfile umount example.img


## TODO

* More control over LUKS options
* Test and fix resizing (shrinking seems to be broken!)


## Dependencies

* Python 3
* Standard mount tools: `mount`, `umount`, `losetup`
* Cryptsetup (Debian: `cryptsetup-bin`, Gentoo: `sys-fs/cryptsetup`)
