# Setup Notes

## Apps (Root)

DEPRECATED: the old approach was as follows:

```zsh

> rpm-ostree install zsh figlet fortume-mod stow

> usermod --shell /usr/sbin/zsh root
> usermod --shell /usr/sbin/zsh jerry


```

The preferred aproach is to install these using homebrew:

```zsh

> brew install zsh figlet fortune stow


```

and explicitly configure the terminal to use zsh.

## Config (Root)

Set the hostname:

```zsh

> hostnamectl set-hostname <hostname>


```

Turn of the motd:

```zsh

> ujust toggle-user-motd


```

## Config (User)

Configure window switcher to show windows from all workspaces:

```zsh

> gsettings get org.gnome.shell.window-switcher current-workspace-only
> gsettings set org.gnome.shell.window-switcher current-workspace-only false


```

Set terminal opacity to 95%:

```zsh

> ujust ptyxis-transparency 0.95


```

The old way to do the above:

```zsh

> dconf write /org/gnome/Ptyxis/Profiles/<profile-id>/opacity 0.95


```

Setup SSH - create a public / private key pair:

```zsh

> ssh-keygen -t rsa


```

Turn of the motd:

```zsh

> ujust toggle-user-motd


```

# Installation Notes

# Update / Upgrade Notes
