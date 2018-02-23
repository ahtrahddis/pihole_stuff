Files and stuff from my Pihole implementation.

I am currently using:

- Odroid C1+
- Armbian Ubuntu xenial: https://dl.armbian.com/odroidc1/Ubuntu_xenial_default.7z
- Pihole

For the basic Armbian stuff (static ip, hostname, timezone etc) I run:

`$ armbian-config`

Although the above tool can update the system, I always prefer to do it manually:

`$ apt-get update && apt-get upgrade`

In order to install Pihole I did the following:

`$ wget -O basic-install.sh https://install.pi-hole.net` <br>
`$ bash basic-install.sh`

Armbian-config offers an option to install Pihole but I did not test it.

After Pihole installation I downloaded and modified my adlists.list file, enabling most of the extra sources:

`$ wget https://raw.githubusercontent.com/archphile/pihole_stuff/master/adlists.list -O /etc/pihole/adlists.list` <br>
`$ pihole -g`

Finally some Odroid related stuff:

`$ wget is 3https://raw.githubusercontent.com/archphile/pihole_stuff/master/rc.local-odroid-c1 -O /etc/rc.local`
