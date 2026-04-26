# GDM Setup

## Scaling and Other Settings

It may be necessary to force the scaling of GDM - in which case do the following:

```zsh

> machinectl shell gdm@ /bin/bash

```

You are now in a GDM shell. To set the scaling factor:

```zsh

> gsettings set org.gnome.desktop.interface scaling-factor 2
> gsettings get org.gnome.desktop.interface scaling-factor


```

and to optionally change the accent colour:

```zsh

> gsettings set org.gnome.desktop.interface accent-color "blue"
> gsettings get org.gnome.desktop.interface accent-color


```

Note: The above no longer works since Gnome 49 - you will also need to perform the following:

```zsh

> cp /var/lib/gdm/.config/dconf/user /var/lib/gdm/seat0/config/dconf/user


```

If you copied monitor settings to the gdm home directory you will also need to perform
the following step:

```zsh

> cp /var/lib/gdm/.config/monitors.xml /var/lib/gdm/seat0/config/monitors.xml


```

You may also need to do the following to restore SELinux security contexts:

```zsh

> restorecon -RFv /var/lib/gdm/


```
