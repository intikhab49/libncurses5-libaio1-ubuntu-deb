Ubuntu Library Dependencies
This repository contains rare Ubuntu dependency packages that are difficult to find, useful for legacy applications or specific environments. These .deb files are provided as-is for use in compatible Ubuntu systems.
Dependencies Included

libaio1_0.3.112-5_amd64.deb: Asynchronous I/O library for Ubuntu.
libncurses5_6.1+20181013-2+deb10u2_amd64.deb: Shared libraries for terminal handling (NCURSES 5).
libncurses5-dev_6.1-1ubuntu1.18.04_amd64.deb: Development files for NCURSES 5.
libtinfo5_6.1+20181013-2+deb10u2_amd64.deb: Terminal interface library (low-level terminfo).

Installation
To install these dependencies on a compatible Ubuntu system, follow these steps:

Clone the Repository:Clone this repository to download the .deb files:
git clone https://github.com/intikhab49/lib-depedencies.git
cd lib-depedencies


Install the Packages:Use dpkg to install all .deb files in the repository:
sudo dpkg -i libaio1_0.3.112-5_amd64.deb \
             libncurses5_6.1+20181013-2+deb10u2_amd64.deb \
             libncurses5-dev_6.1-1ubuntu1.18.04_amd64.deb \
             libtinfo5_6.1+20181013-2+deb10u2_amd64.deb


Resolve Missing Dependencies:If any dependencies are missing, fix them with:
sudo apt-get install -f


Verify Installation:Check that the packages are installed:
dpkg -l | grep -E 'libaio1|libncurses5|libtinfo5'



Notes

These packages are specific to 64-bit Ubuntu systems (amd64 architecture).
Always verify compatibility with your system before installation (e.g., Ubuntu 18.04 or compatible versions).
Use at your own risk, as these are older versions of libraries that may not receive updates.

Contributing
If you have other rare dependencies to share, feel free to open a pull request or contact the repository owner.
License
This repository does not modify the original .deb files; they are redistributed as provided. Refer to the original package licenses for usage terms.
