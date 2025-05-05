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


