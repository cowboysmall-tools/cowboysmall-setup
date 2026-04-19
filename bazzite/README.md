# Setup Notes

## Grub

It may be necessary to force the scaling of plymouth - in which case execute the following:

```zsh

> rpm-ostree kargs --editor


```

And add the following arguments:

```

> plymouth.force-scale=2


```

## GDM

It may be necessary to force the scaling of GDM - in which case execute the following:

```zsh

> machinectl shell gdm@ /bin/bash

> gsettings set org.gnome.desktop.interface scaling-factor 2
> gsettings get org.gnome.desktop.interface scaling-factor

> gsettings set org.gnome.desktop.interface accent-color "blue"
> gsettings get org.gnome.desktop.interface accent-color


```

Specify your preferred scaling factor and accent color.

Note: The above no longer works since Gnome 49 - you will need to also perform the following:

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

## Apps (Root)

```zsh

> rpm-ostree install zsh figlet fortume-mod stow

> usermod --shell /usr/sbin/zsh root
> usermod --shell /usr/sbin/zsh jerry


```

## Config (Root)

```zsh

> hostnamectl set-hostname <hostname>

> ujust toggle-user-motd


```

## Config (User)

```zsh

> gsettings get org.gnome.shell.window-switcher current-workspace-only
> gsettings set org.gnome.shell.window-switcher current-workspace-only false

> dconf write /org/gnome/Ptyxis/Profiles/<profile-id>/opacity 0.95

> ssh-keygen -t rsa

> ujust toggle-user-motd


```

# Installation Notes

# Update / Upgrade Notes
