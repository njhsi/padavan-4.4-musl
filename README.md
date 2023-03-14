# padavan-4.4 #

This is forked from https://github.com/snowDice/padavan-4.4.git commit: f4bc7b6d525273830ba353a6d2605be0342e59df


Padavan 4.4 with musl libc, instead of uclibc. benefits: 
- small footprints in memory
- maybe better performance
- to run openwrt packages

How to apply:
- prepare the original clone, of the noted commit
- # patch -p1 < toolchain-mipsel.diff_commit_f4bc7b6d525273830ba353a6d2605be0342e59df
- # patch -p1 < trunk.diff_commit_f4bc7b6d525273830ba353a6d2605be0342e59df
- build it by the README.md in the original clone

Notes:
- crosstool-ng.diff_commit_1b0c227c0526d1f5a31355921640676995477d91 is for reference, as the diff to original crosstoo-ng
- some packages were disabled, check the config file and user/Makefile
- stablility not fully tested, it CAN/SHALL brick or burn your devices
- rt-ac85p tested in a weekend
