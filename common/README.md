# Setup

## Google Chrome Issue

There is an issue with the latest google chrome rpm - it adds two desktop entries with a
mis-configured entry in one of them, resulting in two chrome icons in the app overview.
A temporary fix:

```zsh

> cp /usr/share/applications/com.google.Chrome.desktop ~/.local/share/applications

> sed -i "2a\\NotShowIn=GNOME;KDE" ~/.local/share/applications/com.google.Chrome.desktop


```

## Archives (Root)

```zsh

> mkdir Bak && cd Bak/

> tar -xzvf /Path/To/Archives/Root/Bin.tar.gz


```

## Archives (User)

```zsh

> mkdir Bak && cd Bak/

> tar -xzvf /Path/To/Archives/User/Bin.tar.gz

...


```
