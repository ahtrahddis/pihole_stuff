Files and stuff from my Pihole implementation.

I am currently using:

- Odroid C1+
- Armbian Ubuntu xenial: https://dl.armbian.com/odroidc1/Ubuntu_xenial_default.7z
- Pihole

In order to install Pihole I did the following:

`$ wget -O basic-install.sh https://install.pi-hole.net` <br>
`$ bash basic-install.sh`

After Pihole installation I downloaded an dmodified my adlists.list file:

`$ wget https://raw.githubusercontent.com/archphile/pihole_stuff/master/adlists.list -O /etc/pihole/adlists.list`


Finally some Odroid related stuff:

`$ https://raw.githubusercontent.com/archphile/pihole_stuff/master/rc.local-odroid-c1 -O /etc/rc.local`
