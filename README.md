# snapclean
script to clean up/out old snaps/cache.

currently it runs through disabled snaps and removes them by version numbers and deletes the cache directory (/var/lib/snapd/cache)

possibly future changes might include configurable amount of time for the snap to have been disabled, but so far I see no point for it.

sample run:
```
root@smaug:~# snapclean
snap remove --revision=1601 aws-cli
aws-cli (revision 1601) removed
snap remove --revision=545 brave
brave (revision 545) removed
snap remove --revision=359 canonical-livepatch
canonical-livepatch (revision 359) removed
snap remove --revision=2947 core18
core18 (revision 2947) removed
snap remove --revision=2599 core20
core20 (revision 2599) removed
snap remove --revision=2111 core22
core22 (revision 2111) removed
snap remove --revision=1151 core24
core24 (revision 1151) removed
snap remove --revision=2242 doctl
doctl (revision 2242) removed
snap remove --revision=202 gnome-42-2204
gnome-42-2204 (revision 202) removed
snap remove --revision=605 google-cloud-sdk
google-cloud-sdk (revision 605) removed
snap remove --revision=3676 kubectl
kubectl (revision 3676) removed
snap remove --revision=15760 multipass
multipass (revision 15760) removed
snap remove --revision=24792 snapd
snapd (revision 24792) removed
snap remove --revision=796 thunderbird
thunderbird (revision 796) removed
before: /dev/mapper/ssd-vlib 21G 6.4G 14G 33% /var/lib
after: /dev/mapper/ssd-vlib 21G 4.0G 16G 21% /var/lib

```
