# OpenBSD on a MacbookAir5,1

This a place for me to keep track of what's working, what's not, and any workarounds I'm using.

## Step #1: buy some helpful accessories

* buy a wireless adapter, OpenBSD does not have a driver for the built in wifi chip
* buy a thumb drive to use for installation
* buy a usb hard drive for backups between upgrades

## Step #2: download OpenBSD and create a USB installer

* download the OpenBSD 5.5-beta 2014-01-17 amd64 snapshot
* download the matching ports source
* download the matching kernel source
* download the matching userland source
* install on a USB drive using VMware
* copy the installation stuff onto the USB drive

## Step #3: install OpenBSD on your MacbookAir5,1

* boot to usb
* race through the installation process before the screen goes blank

## Step #4: disable features that cause hangs

* disable acpivout
* disable apmd

## Notes

* This guide will soon be out of date. OpenBSD is a moving target. Sorry.
* Different Macbook Air models require different steps. Starting with the MacbookAir6,1 or later you shoudln't even try unless you're an OpenBSD developer trying to hack on the kernel.

## Why

* I started thinking about the value of open source after the Snowden revelations. I concluded that I would like more open source in my diet.
* Apple makes the best laptops. Open source hardware would be better, but we're not there yet. Plus, I already own Apple hardware.
* OpenBSD makes the best OS. Its open source and the developers care about code quality the way Apple cares about chamfered edges on their hardware. You haven't lived until you've used an OpenBSD man page.

## Further Reading

* Joshua Stein
* donate to OpenBSD
