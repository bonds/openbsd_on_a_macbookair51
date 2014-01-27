# OpenBSD on a MacbookAir5,1

This a place for me to keep track of what's working, what's not, and any workarounds I'm using.

## Step #1: buy some helpful accessories

* Buy a [urtwn](http://www.amazon.com/Edimax-EW-7811Un-Wireless-Adapter-Wizard/dp/B003MTTJOY/ref=sr_1_1?ie=UTF8&qid=1390798318&sr=8-1&keywords=usb+wifi) based wireless networking adapter and/or an [axe](http://www.amazon.com/Apple-MC704ZM-A-Ethernet-Adapter/dp/B00486070K/ref=sr_1_3?ie=UTF8&qid=1390798382&sr=8-3&keywords=apple+ethernet+adapter) based wired adapter. OpenBSD [does not support](https://github.com/bonds/openbsd_on_a_macbookair51/issues/2) the builtin wireless chipset, so you'll need something for internet access.
* Buy a thumb drive to use for installation. I rather like this [USB adapter](http://www.amazon.com/ELAGO-Mobile-Reader-World-Smallest-EL-RD-012/dp/B002K7EJDK/ref=pd_sim_e_1) combined with this [SDHC card](http://www.amazon.com/SanDisk-microSDXC-Memory-Adapter-SDSDQU-064G-AFFP-A/dp/B009QZH6JS/ref=pd_bxgy_e_text_y), myself.
* Buy a usb hard drive for backups between upgrades.

## Step #2: download OpenBSD and create a USB installer

* download the OpenBSD 5.5-beta 2014-01-17 amd64 snapshot
* download the matching ports source
* download the matching kernel source
* download the matching userland source
* download the urtwn firmware
* install on a USB drive using VMware
* copy the installation stuff onto the USB drive
  * installer files
  * source code
  * firmware

## Step #3: install OpenBSD on your MacbookAir5,1

* boot to usb
* enable full disk encryption
* overcome obstacle 1: [the screen goes blank after a while](https://github.com/bonds/openbsd_on_a_macbookair51/issues/1)
* finish install, reboot, and login
* copy sources and untar them in the right places
* install the wireless firmware
* configure the wireless adapter

## Step #4: disable features that cause hangs

* [disable acpivout to avoid hangs](https://github.com/bonds/openbsd_on_a_macbookair51/issues/4) when running X-Windows
* [disable apmd to avoid hangs](https://github.com/bonds/openbsd_on_a_macbookair51/issues/3) when running X-Windows

## Stuff That Works Awesome

* OpenBSD 5.5-beta 2014-01-17
* Gnome 3, with some exceptions noted below
* sound
* multitouch trackpad with two-finger scroll, 3 finger right-click ??
* adjust display brightness
* manually adjust cpu speed from the command line

## Stuff That's Unreliable

* wireless networking adapters overheat and disconnect themselves
* Seahorse, the Gnome default password manager, crashes all the time
* Empathy, the Gnome default chat client, crashes all the time
* adjusting volume level in Gnome too quickly leads to the volume set vs displayed to get out of sync

## Stuff That Does Not Work At All

* built-in wireless
* automatic cpu speed adjustments based on usage
* suspend and resume in general, suspend and resume on lid close in particular
* keyboard backlight
* adjusting display brightness using the built-in function keys

## Notes

* This guide will soon be out of date. OpenBSD is a moving target. Sorry.
* The OpenBSD devs do not come here. This is not an official anything. You (the reader) and I are probably the only ones looking at this. That is to say, don't file bugs here in the hope someone will notice and/or do something about them. In fact, probably best not to file bugs here in general, let me do it. ;)
* I am an OpenBSD newb. I'm just stumbling along, piecing together what I can through trial, error, Googling, and asking questions. I don't know the OpenBSD innards at all. Take all this with a grain of salt.
* Different Macbook Air models require different steps. Starting with the MacbookAir6,1 or later you shoudln't even try unless you're an OpenBSD developer trying to hack on the kernel.

## Why

* I started thinking about the value of open source after the Snowden revelations. I concluded that I would like more open source in my diet.
* Apple makes the best laptops. Open source hardware would be better, but we're not there yet. Plus, I already own Apple hardware.
* OpenBSD makes the best OS. Its open source and the developers care about code quality the way Apple cares about chamfered edges on their hardware. You haven't lived until you've used an OpenBSD man page.

## Further Reading

* Joshua Stein
* donate to OpenBSD
