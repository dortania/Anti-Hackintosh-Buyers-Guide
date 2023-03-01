# AMD

AMD CPUs can work in macOS but require patches to macOS. Due to the issues listed below, we strongly advise against using AMD CPUs. For people still willing to use an AMD CPU, the [OpenCore Install Guide]() does provide instructions for macOS High Sierra (10.13+) and newer.

Compatible AMD CPUs:

* Bulldozer (15h)
  * AMD FX Series
* Jaguar (16h)
* Ryzen (17h + 19h)
  * Ryzen 1000-5000 Series
  * Athlon 2xxGE
  * Threadripper

::: tip High Thread Counts

macOS supports a maximum of 64 threads. High-end Threadrippers can exceed this, and require Simultaneous Multi-Threading disabled.

:::

::: details AMD CPU Limitations in macOS

* Adobe Support
  * Most of Adobe's suite relies on Intel's Memfast instruction set, resulting in crashes with AMD CPUs
  * You can disable functionality like RAW support to avoid the crashing: [Adobe Fixes](https://gist.github.com/naveenkrdy/26760ac5135deed6d0bb8902f6ceb6bd)
* 32-Bit support
  * For those still relying on 32-Bit software in Mojave and below, note that the Vanilla patches do not support 32-bit instructions
  * A work-around is to install a [custom kernel](https://files.amd-osx.com/?dir=Kernels), however you lose iMessage support and no support is provided for these kernels
* Cubase, REAPER, and other audio software crash when launched
  * REAPER works *if* using the Clang build
  * There is no fix for Cubase at the moment
  * Waves plugins also cause crashes
* Virtual Machines relying on AppleHV do not work
  * This includes VMWare, Parallels, Docker, Android Studio, etc
  * VirtualBox is the sole exception as they have their own hypervisor
  * VMware 10 and Parallels 13.1.0 do support their own hypervisor, however using such outdated VM software poses a large security threat
* Xcode's Apple Watch simulator is broken in Catalina
  * Mojave works fine
* Microphone input requires VoodooHDA, which may have worse audio quality
* Audio drift issues on Ryzen APUs (G series Chips)
  * USB DAC is only fix besides new CPU
* Delayed updates

:::