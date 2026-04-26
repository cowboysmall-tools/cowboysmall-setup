# Plymouth Setup

## Scaling (Fedora)

It may be necessary to force the scaling of plymouth - in which case execute the following:

```zsh

> grubby --update-kernel=ALL --args=plymouth.force-scale=2


```

alternatively you could edit the file `/etc/default/grub`:

```zsh

> nano -w /etc/default/grub


```

and update the `GRUB_CMDLINE_LINUX` variable to the following:

```

> GRUB_CMDLINE_LINUX="rhgb quiet plymouth.force-scale=2"


```

## Scaling (Bazzite)

On bazzite you will need to do the following:

```zsh

> rpm-ostree kargs --editor


```

and add the following arguments:

```

> plymouth.force-scale=2


```
