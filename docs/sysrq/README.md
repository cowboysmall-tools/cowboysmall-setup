# SysRq


## Enable immediately

To enable it immediately execute the following:

```zsh

> sysctl -w kernel.sysrq=1


```

## Enable at boot

To enable it every time the system boots create a file in the following location:

```zsh

> nano -w /etc/sysctl.d/90-sysrq.conf


```

and add the following to it:

```zsh

kernel.sysrq = 1


```

The "Magic SysRq Key" will be enabled at next boot. To enable it immediately execute the following:

```zsh

> systemctl restart systemd-sysctl.service


```
