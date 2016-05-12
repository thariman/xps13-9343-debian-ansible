XPS13-9343-debian-ansible
=========

This role will install all the necessary package to get XPS13 working
on my i7/8GB - 256GB, Touch TL QHD+ (3200x1800) (Asian) Windows 8
using Broadcom wifi

Requirements
------------

from my mac
aria2c -x5 "http://cdimage.debian.org/debian-cd/8.3.0/amd64/iso-cd/debian-8.3.0-amd64-netinst.iso"
http://cdimage.debian.org/cdimage/daily-builds/daily/current/amd64/iso-cd/
insert usb thumbdrive
diskutil unmountDisk /dev/disk4
sudo dd if=debian-8.3.0-amd64-netinst.iso of=/dev/rdisk4 bs=1m
connect external usb ethernet ( debian-8.3 does not support broadcom wifi out of the box )
configure the bios for UEFI only http://www.dell.com/support/article/us/en/04/SLN297060/?docid=SLN297060
Follow first 3 screenshoot only
Press F12 when you see the Dell logo to enter boot menu
boot from thumb drive under UEFI BOOT:
Make sure it said Debian GNU/Linux UEFI Installer menu
Choose Graphical install
Partition disks Guided -use entire disk.
I use btfs for the /
Install only ssh and system essential

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
