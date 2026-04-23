# Go Setup

## Issues

If modules fail to install due to checksum mismatches try executing the following:

```zsh

> go clean -modcache
> go mod tidy


```
