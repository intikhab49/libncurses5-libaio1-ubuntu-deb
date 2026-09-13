<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1C1917,50:E95420,100:FDBA74&height=170&section=header&text=Legacy%20Ubuntu%20Libraries&fontSize=46&fontColor=ffffff&fontAlignY=38&desc=libaio1%20%C2%B7%20libncurses5%20%C2%B7%20libtinfo5%20.deb%20packages&descSize=17&descAlignY=60&animation=fadeIn" width="100%" alt="Legacy Ubuntu Libraries — libaio1, libncurses5, libtinfo5 .deb packages"/>

# Download libaio1, libncurses5 & libtinfo5 .deb Packages for Ubuntu (amd64)

**Fix `libncurses.so.5`, `libtinfo.so.5` and `libaio.so.1: cannot open shared object file` errors when legacy software won't start on a modern Ubuntu system.**

<p>
  <img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu"/>
  <img src="https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white" alt="Debian"/>
  <img src="https://img.shields.io/badge/arch-amd64-555555?style=for-the-badge" alt="amd64"/>
  <img src="https://img.shields.io/badge/dpkg-.deb-2EA043?style=for-the-badge" alt=".deb packages"/>
</p>

</div>

---

Newer Ubuntu releases dropped or renamed several old shared libraries. Older binaries — database clients and servers, vendor installers, embedded toolchains, classic terminal apps — still link against them and fail with errors like:

```text
error while loading shared libraries: libncurses.so.5: cannot open shared object file: No such file or directory
error while loading shared libraries: libtinfo.so.5: cannot open shared object file: No such file or directory
error while loading shared libraries: libaio.so.1: cannot open shared object file: No such file or directory
```

This repository keeps the original `.deb` packages in one place so you can install them without hunting through old archives.

## 📦 Included packages

| Package | File | Provides |
|---|---|---|
| **libaio1** | `libaio1_0.3.112-5_amd64.deb` | Linux asynchronous I/O library (`libaio.so.1`) |
| **libncurses5** | `libncurses5_6.1+20181013-2+deb10u2_amd64.deb` | NCURSES 5 terminal handling shared libraries (`libncurses.so.5`) |
| **libncurses5-dev** | `libncurses5-dev_6.1-1ubuntu1.18.04_amd64.deb` | NCURSES 5 development headers |
| **libtinfo5** | `libtinfo5_6.1+20181013-2+deb10u2_amd64.deb` | Low-level terminfo library (`libtinfo.so.5`) |

## 🚀 Installation

```bash
git clone https://github.com/intikhab49/libncurses5-libaio1-ubuntu-deb.git
cd libncurses5-libaio1-ubuntu-deb

sudo dpkg -i libtinfo5_6.1+20181013-2+deb10u2_amd64.deb \
             libncurses5_6.1+20181013-2+deb10u2_amd64.deb \
             libncurses5-dev_6.1-1ubuntu1.18.04_amd64.deb \
             libaio1_0.3.112-5_amd64.deb

sudo apt-get install -f      # resolve any missing dependencies
```

Verify:

```bash
dpkg -l | grep -E 'libaio1|libncurses5|libtinfo5'
```

> [!TIP]
> Only need the Asynchronous I/O library on Ubuntu 24.04+? The distro now ships it as `libaio1t64` — `sudo apt install libaio1t64` and symlink `libaio.so.1t64` to `libaio.so.1` is an alternative to the `.deb` here.

## ⚠️ Notes

- **amd64 (64-bit x86) only.**
- These are **old library versions** that no longer receive security updates. Install them only for the software that needs them.
- Check compatibility with your release first (packages originate from Debian 10 and Ubuntu 18.04).
- Files are redistributed unmodified; each package keeps its original upstream license.

## 🤝 Contributing

Have another hard-to-find legacy dependency? Open a pull request or an issue.

---

<div align="center">

**Maintained by [Intikhab Azam](https://github.com/intikhab49)** — AI & automation engineer · DevOps · Linux

<sub>Keywords: libncurses5 Ubuntu 22.04 · libncurses5 Ubuntu 24.04 · libtinfo5 download · libaio1 not found · libaio.so.1 · libncurses.so.5 cannot open shared object file · .deb package · dpkg install</sub>

</div>
