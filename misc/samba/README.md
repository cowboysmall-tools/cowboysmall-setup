# Samba Setup

## Mounting the Shared Game Directory

Copy the credentials file to the Games directory

```zsh

> cp misc/samba/.smb-credentials ~/

```

Edit the credentials file

```

username=myname
password=mypass

```

Install the mount / umount scripts

```zsh

> install -D misc/samba/smb-mount -t $HOME/.local/bin
> install -D misc/samba/smb-umount -t $HOME/.local/bin


```

Usage

```zsh

> smb-mount Games/retrodeck

...

> smb-umount Games/retrodeck


```
