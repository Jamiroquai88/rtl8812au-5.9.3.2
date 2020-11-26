# rtl8812au-5.9.3.2

## Realtek 8812AU driver version 5.9.3.2

Only supports 8812AU chipset.

Initial upload.

### Building

To build and install module manually:
```sh
$ make
$ sudo make install
```

To use dkms install:

```sh
  (as root, or sudo) copy source folder contents to /usr/src/rtl8812au-5.9.3.2
```

```sh
$ sudo dkms add -m rtl8812au -v 5.9.3.2
$ sudo dkms build -m rtl8812au -v 5.9.3.2
$ sudo dkms install -m rtl8812au -v 5.9.3.2
```

To use dkms uninstall and remove:

```sh
$ sudo dkms remove -m rtl8812au -v 5.9.3.2 --all
```

### NetworkManager

As others have noted, people using NetworkManager need to add this stanza to /etc/NetworkManager/NetworkManager.conf

```sh
  [device]
  wifi.scan-rand-mac-address=no
```
