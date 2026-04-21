# Update / Upgrade Notes

## Remove Dropped Packages

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
