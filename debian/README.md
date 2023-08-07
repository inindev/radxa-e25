## stock debian bookworm linux for the radxa e25

<i>Note: This script is intended to be run from a 64 bit arm device such as a rock 5b or an odroid m1.</i>

<br/>

**build debian bookworm using debootstrap**
```
sudo su
sh make_debian_img.sh
```

<i>the build will produce the target file mmc_2g.img.xz</i>

<br/>

**copy the image to mmc media**
```
sudo sh -c 'xzcat mmc_2g.img.xz > /dev/sdX && sync'
```

<br/>

**multiple build options are available by editing make_debian_img.sh**
```
media='mmc_2g.img' # or block device '/dev/sdX'
deb_dist='bookworm'
hostname='radxa-e25-arm64'
acct_uid='debian'
acct_pass='debian'
```
