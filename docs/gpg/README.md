# GPG Keys

## List GPG Keys

Execute the following to list all installed GPG keys:

```

> rpm -q gpg-pubkey --qf '%{NAME}-%{VERSION}-%{RELEASE}\t%{SUMMARY}\n'

```
