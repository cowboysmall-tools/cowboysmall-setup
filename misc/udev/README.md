# Udev Setup

## Boxput BPR3S Plus Air Mouse Remote Control

Copy the hwdb file to the following location:

```zsh

> sudo cp misc/udev/99-bpr3s.hwdb /etc/udev/hwdb.d/


```

Update and reload the hardware database:

```zsh

> sudo systemd-hwdb update
> sudo udevadm trigger


```
