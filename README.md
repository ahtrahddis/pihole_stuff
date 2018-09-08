Files and stuff from my Pihole implementation.

I am currently using:

- Odroid C1+
- Armbian ~~Ubuntu xenial~~ Debian Jessie: https://dl.armbian.com/odroidc1/Debian_jessie_default.7z
- Pihole

For the basic Armbian stuff (static ip, hostname, timezone etc) you can run:

	armbian-config


What I Sdid was:

1. configured a static IP network:

	nano /etc/network/interfaces

2. changed default SSH port

	nano /etc/ssh/sshd_config
	
3. updated OS

	apt-get update && apt-get dist-upgrade
	

In order to install Pihole I did the following:

	wget -O basic-install.sh https://install.pi-hole.net
	bash basic-install.sh

Armbian-config offers an option to install Pihole but I did not test it.

After Pihole installation I downloaded and modified my adlists.list file, enabling most of the extra sources:

	wget https://raw.githubusercontent.com/archphile/pihole_stuff/master/adlists.list -O /etc/pihole/adlists.list
	pihole -g

Finally some Odroid related stuff:

	wget https://raw.githubusercontent.com/archphile/pihole_stuff/master/rc.local-odroid-c1 -O /etc/rc.local

and

	wget https://raw.githubusercontent.com/archphile/pihole_stuff/master/log2ram -O /etc/default/log2ram
	

For the tp-adblock.txt file, please read the following link:

http://thepenguin.eu/2018-05-27-an-adblock-list-for-rooted-xiaomi-smartphones/
