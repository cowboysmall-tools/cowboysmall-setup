# GPG Keys

## List GPG Keys

Execute the following to list all installed GPG keys:

```zsh

> rpm -q gpg-pubkey --qf '%{NAME}-%{VERSION}-%{RELEASE}\t%{SUMMARY}\n'

```
