Intel&reg; provides a tool to check and update the graphics drivers of the **Intel&reg; HD Graphics** integrated GPU.

<span class="label label-warning">Heads up!</span> This tool is really useful to let your Linux Distro works well. For example, the latest **Ubuntu 17.10** use [Wayland](https://wiki.ubuntu.com/Wayland) as default display server and the standard i915 GPU driver doesn't manage properly Wayland as expected. We suggest to use the Intel® Graphics update tool for Linux to resolve lack graphical issues.

You can follow this link to **download** the latest [Intel® Graphics update tool for Linux](https://01.org/linuxgraphics/downloads/update-tool).

Whether running for the first time or upgrading from an earlier release, be sure to run the following.
In order to "trust" the Intel® Graphics Update Tool for Linux* OS, you will need to add keys to Ubuntu's* software package manager ("apt"). Open a terminal, and execute these lines:

    wget https://download.01.org/gfx/RPM-GPG-GROUP-KEY-ilg
    sudo apt-key add RPM-GPG-GROUP-KEY-ilg

In addition, also run the update and upgrade from Ubuntu*

    sudo apt-get update
    sudo apt-get upgrade

After that you can install and run the tool to install the latest Intel&reg; driver.

### Install the Intel® Graphics update tool in Ubuntu 17.10

Since the latest Intel® Graphics update tool for Linux* OS V2.0.6 is not available yet for Ubuntu 17.10, you need to use the 17.04 version and a little trick.

Just change temporarily `/etc/lsb-release` to correspond to Ubuntu 17.04 Zesty Zapus, it will work fine.  
First, make a backup of the file:

    sudo cp /etc/lsb-release /etc/lsb-release.bk

Then edit the file with your favourite text editor(e.g. nano for example):

    sudo nano /etc/lsb-release

Replace contents with:

    DISTRIB_ID=Ubuntu
    DISTRIB_RELEASE=17.04
    DISTRIB_CODENAME=zesty
    DISTRIB_DESCRIPTION="Ubuntu 17.04"

Save the file and now you can install the tool.

When you are done installing the tool and the drivers, you can simply revert the changes:

    sudo rm -f /etc/lsb-release
    sudo cp /etc/lsb-release.bk /etc/lsb-release
