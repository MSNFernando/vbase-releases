# vBase releases

Installer images for vBase hosts: the USB stick a server boots and runs from.

## Write a stick

The easy way is **vBase Imager** (Windows, macOS, Linux): it lists the releases here, downloads one,
checks it and writes the stick. Or download `vbase-<version>.img.xz` below and write it with
balenaEtcher, Rufus (DD mode) or `xzcat vbase-0.1.img.xz | sudo dd of=/dev/sdX bs=4M conv=fsync status=progress`.

- **USB stick: 32 GB or larger**, USB 3, from a known brand. The server keeps its settings (and, on the
  control-plane node, its database) on the stick.
- Server: x86-64 with UEFI (Secure Boot can stay on), virtualisation enabled in the firmware.

## Check a download

```sh
sha256sum -c SHA256SUMS --ignore-missing
```

## What's here

Images, their checksums, release notes and `os_list.json` (the list vBase Imager reads). The source code
is not in this repository.
