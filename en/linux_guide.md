---
title: "How to connect Kurikku on Linux"
old_id: 6
---

For linux doesn't exists good switcher, which can handle any of distro. This guide will help some dudes who uses (Ubuntu/Debian and Arch/Manjaro, maybe another distro (like PopOS, Fedora, I don't checked)

Script for parsing ips: `curl -s https://ip.kurikku.pw/current.json | python -c "from __future__ import print_function; import sys, json; j = json.load(sys.stdin); print('\n# Kurikku\n' + '\n'.join('{} {}'.format(k, v) for k, v in {i: ' '.join([k for k, v in j.items() if v == i]) for _, i in j.items()}.items()))" | sudo tee -a /etc/hosts > /dev/null`

---
# Debian/Ubuntu
Maybe another dpkg based system, I don't tested!
#### To Install:
1. Fetch latest ip addresses and enter in `/etc/hosts` with ***script for parsing ips***
2. Download our certificate from here: [*click*](https://ip.kurikku.pw/kurikku.crt)
3. Copy this certificate to ca-certificates folder: `sudo cp kurikku.crt /usr/local/share/ca-certificates/`
4. Now update ca-certificates: `sudo update-ca-certificates`
You ready to go!

#### To Uninstall:
1. Remove hosts manually from `/etc/hosts`
2. Remove certificate from `/usr/local/share/ca-certificates/`
3. And update ca-certificates: `sudo update-ca-certificates --fresh`

---
# Arch/Manjaro
#### To Install:
1. Fetch latest ip addresses and enter in `/etc/hosts` with ***script for parsing ips***
2. Download our certificate from here: [*click*](https://ip.kurikku.pw/kurikku.crt)
3. Put this certificate in linux main certificate storage: `sudo mv kurikku.crt /etc/ca-certificates/trust-source/anchors`
4. Run: `sudo trust extract-compat && sudo update-ca-trust`
You ready to go!

#### To Uninstall:
1. Remove hosts manually from `/etc/hosts`
2. Delete certificate file from `/etc/ca-certificates/trust-source/anchors`
3. Run: `sudo trust extract-compat && sudo update-ca-trust`

---
#  Fedora
(Not tested)

#### To Install:
1. Fetch latest ip addresses and enter in `/etc/hosts` with ***script for parsing ips***
2. Download our certificate from here: [*click*](https://ip.kurikku.pw/kurikku.crt)
3. Put this certificate in linux main certificate storage: `sudo mv kurikku.crt /etc/pki/ca-trust/source/anchors`
4. Run: `sudo trust extract-compat && sudo update-ca-trust`
You ready to go!

#### To Uninstall:
1. Remove hosts manually from `/etc/hosts`
2. Delete certificate file from `/etc/pki/ca-trust/source/anchors`
3. Run: `sudo trust extract-compat && sudo update-ca-trust`
