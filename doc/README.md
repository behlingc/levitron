Digital controlled levitron
=============================================================

# Objective

A digital controlled levitron is build based on the analogue one from the german book ***Keine Panik vor Regelungstechnik! 2nd edition***.

The frame will be designed with Freecad and the PCB will be designed with KiCAD. The software will be
created in C on Arduino IDE.

# Development Host System Setup

## Linux System Type

The following Linux command gives all OS info:

```bash
$ lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 24.04.2 LTS
Release:	24.04
Codename:	noble
```

## Needed packages

### KiCad

```bash
sudo add-apt-repository --yes ppa:kicad kicad-9.0-releases
sudo apt update
sudo apt install --install-recommends kicad
```
See: [KiCad - Install on Ubuntu](https://www.kicad.org/download/details/ubuntu/)

### FreeCAD

***NOTE:*** FreeCAD apt package is broken for Ubuntu 24.04.2 LTS at the time of writing. Hence, snap is used for installation.

```bash
sudo snap install core
sudo snap install freecad
```
See: [How to Install FreeCAD on Ubuntu 24.04, 22.04 or 20.04 - Install FreeCAD via Snap Command](https://linuxcapable.com/how-to-install-freecad-on-ubuntu-linux/#Method_2_Install_FreeCAD_via_Snap)

### Git

```bash
sudo apt-get update
sudo apt-get install git-all
```

#### Git setup


```bash
git config --global user.name "Carsten Behling"
git config --global user.email xxx@xxx.com
```

See: [Git - 1.6 Getting Started - First-Time Git Setup - Your Identity](https://git-scm.com/book/ms/v2/Getting-Started-First-Time-Git-Setup)

You may use a keypair for repository access:

```bash
ssh-keygen -t ed25519 -C "xxx@xxx.com"
```

Let a repository administrator add the resulting key from ***~/.ssh/id_ed25519.pub*** to ***Settings->Deploy keys***
to this repository.

You should be able to push now.


### Arduino 2 IDE

Download [Arduino 2.3.5 for Linux ZIP](https://downloads.arduino.cc/arduino-ide/arduino-ide_2.3.5_Linux_64bit.zip?_gl=1*fafsil*_up*MQ..*_ga*NDY3OTIwNzQwLjE3NDM5NTEwNDQ.*_ga_NEXN8H46L5*MTc0Mzk1MTA0My4xLjAuMTc0Mzk1MTA0My4wLjAuMjg4MDAxMjA1).

Extract to your home folder.

See: [Arduino - Downloading and installing the Arduino IDE 2 - Linux](https://docs.arduino.cc/software/ide-v2/tutorials/getting-started/ide-v2-downloading-and-installing/#linux)

## Access to serial port

```sh
sudo adduser $USER dialout
```

Logout/login is required.

See: [Ask Ubuntu - How to add dialup group?](https://askubuntu.com/questions/207999/how-to-add-dialup-group)

