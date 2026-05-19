# NPM Setup

## Global Prefix

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
