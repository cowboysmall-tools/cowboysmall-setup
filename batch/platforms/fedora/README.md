# Notes

## DNF Cache

if there are problems caused by broken mirrors and you cannot install a package, then
try the following steps - open the file:

```zsh

> nano -w /etc/dnf/dnf.conf

```

and either remove or comment out the `fastestmirror` entry:

```

[main]
max_parallel_downloads=10
# fastestmirror=True

```

save and close the file, and then execute the following:

```zsh

> dnf clean expire-cache

> dnf upgrade --refresh

```

then re-try installing any packages that failed to install due to problem mirrors.

## Remove Dropped / Obsoleted Packages

After upgrading you may want to remove these
old Gnome apps that have been dropped / replaced:

```zsh

> dnf remove totem evince eog devhelp rhythmbox gnome-screenshot


```

Also, investigate the following:

```

Last metadata expiration check: 0:00:11 ago on Thu 30 Oct 2025 20:01:23.
Dependencies resolved.
================================================================================================================================================================================================================================================
 Package                                                               Architecture                                       Version                                                     Repository                                           Size
================================================================================================================================================================================================================================================
Removing:
 chkconfig                                                             x86_64                                             1.33-3.fc43                                                 @System                                             758 k
 initscripts                                                           x86_64                                             10.26-4.fc43                                                @System                                             1.1 M
 initscripts-rename-device                                             x86_64                                             10.26-4.fc43                                                @System                                              20 k

Transaction Summary
================================================================================================================================================================================================================================================
Remove  3 Packages


```
