# Cowboysmall Setup

Collected setup scripts, tools, and documentation for setting up systems

## NPM Global Prefix

Create global prefix directory:

```zsh

> mkdir ~/.npm-global
> npm config set prefix "~/.npm-global"


```

and then add it to .zshrc:

```

export NPM_PREFIX=$HOME/.npm-global
export PATH=$NPM_PREFIX/bin:$PATH


```

install extensions:

```zsh

> npm install --global web-ext


```

## Go Issues

Check the health of installed nvim plugin modules by executing the following:

```

> :checkhealth go


```

If modules fail to install due to checksum mismatches try executing the following:

```zsh

> go clean -modcache
> go mod tidy


```

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
