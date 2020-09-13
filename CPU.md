# CPUs

## CPUs to avoid:

### AMD CPUs

While AMD CPUs can work, we advise against them due to numerous issues still plaguing them as they're not natively supported. They require quite a bit more work to get setup, but for those who like would prefer AMD, the [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide) has a section for AMD CPUs.

Common issues with AMD:
* Adobe products don't always work
   * Some fixes can be found here: [Adobe Fixes](https://adobe.amd-osx.com/)
   * Do note these fixes just disable functionality; they're not real fixes and have the possibilty to break other things
* Cubase, REAPER, and other audio software crash on launch
   * REAPER works *if* using the Clang build
   * There is no fix for Cubase at the moment
   * Waves plugins also cause crashes
* Virtual machine software using Apple's Hypervisor Framework does not work (ie: Parallels 15 and VMware Fusion 11)
   * VirtualBox works fine as it doesn't use AppleHV
   * Fusion 10.1.5 is the last known working version on AMD CPUs
* Docker broken
   * Docker Toolbox is an alternative which uses VirtualBox, but is legacy and may not be equivalent to Docker Desktop
* Xcode's Apple Watch simulator is broken in Catalina
   * Mojave works fine
* Microphone input is not available with AppleALC, requiring VoodooHDA (quite a bit worse audio quality and overall instability)
* Audio drift issues on Ryzen APUs (G series Chips)
   * USB DAC is the only known possible workaround but not guaranteed to work
* Difficult to setup sleep (or impossible on some systems)
* No CPU power management
   * There has been work on this - see (insert trulyspinach link here)
* Not all USB ports work on some boards
   * This is due to not being assigned in ACPI; see the USB Map guide or is it in the post install guide now
* Delayed updates
* ~~3rd Gen Threadripper is not supported on bare-metal~~
  * Latest BIOS and OpenCore now boot with TRx40 CPUs

Supported AMD CPUs:
* AMD Ryzen Series
* AMD Athlons based on Ryzen CPUs
* AMD ThreadRipper
* AMD FX and APUs

### Intel CPUs

With Intel, thanks to most of the CPUs being quite similar, they have support when the CPU is spoofed to a supported model. The only downside is that the iGPU rarely work on Atom/Pentium/Celeron models, meaning a cheap iGPU Hackintosh is impossible with these CPUs.

Regarding X99/LGA 2011-V3 CPUs, these CPUs were never shipped in a real Mac so quite a few issues are present when running macOS on these systems. Avoid them if possible.

**Dual Socket User Note**: Do note that the macOS kernel only supports a maximum of 64 threads. Dual socket users will also need to use [AppleMCEReporterDisabler](https://github.com/acidanthera/bugtracker/files/3703498/AppleMCEReporterDisabler.kext.zip) in macOS Catalina to prevent a kernel panic.

Unrecommended Intel CPUs:
* Intel Atoms
* Intel Celerons
* Intel Pentiums
* Intel X79/LGA 2011
* Intel X99/LGA 2011-V3
* Intel X299/LGA-2066

::: tip Recommendations

So our overall recommendation for CPUs:

* Semi-modern consumer Intel CPUs
  * Ivy Bridge through Comet Lake are properly supported in macOS
  (bump to haswell)
:::

## Unsupported CPUs

So with outright unsupported CPUs, you're split into 2 camps: Either too old to run or too new that patches aren't supported.

**Too old to run**:

This mainly consists of CPUs that are missing the SSE4.2 instruction set required for Mojave and newer; you can get around this by replacing the telemetry plugin but not ideal. See [trashOS repo](https://github.com/khronokernel/trashOS) for more info.

* Wolfdale (Intel Core2 Duo series)
   * E7xxx
   * E8xxx
* Yorkfeild (Intel Core2 Quad series)
   * E8xxx
   * E9xxx

Then there's the CPUs that are missing the SSE4.1 and older instruction sets, with these support is stuck at OS X 10.11 El Capitan.
