# CPUs

## CPUs to avoid:

While AMD CPUs can work but we advise against them due to numerous issues still plaguing them as they're not natively supported. They require quite a bit more work to get setup but for those who like would prefer AMD there is the [AMD Vanilla Guide](https://vanilla.amd-osx.com). 

Common issues with AMD:
* Adobe Products don't always work and there is no fix for lightroom at the moment
   * some fixes can be found here: [Adobe Fixes](https://adobe.amd-osx.com/)
   * Do note these fixes just disable functionality, they're not real fixes
* Cubase, REAPER, and other audio software crashes on launch
   * REAPER works *if* using the Clang build
   * There is no fix for Cubase at the moment
   * Waves plugins also cause crashes
* Virtual Machine running off of AppleHV's framework will not work(ie: Parallels 15)
   * VirtualBox works fine as it doesn't use AppleHV
* Docker broken
   * Docker toolbox is based off of VirtualBox, many features are unavailable with this
* Xcode AppleWatch simulator is broken in Catalina
   * Mojave works fine
* Microphone input is not available with AppleALC requiring VoodooHDA(quite a bit worse audio quality and overall instability)
* Audio Drift issues on Ryzen APUs(G series Chips)
   * USB DAC is only fix besides new CPU
* Difficult to setup Sleep(or impossible on some systems)
* No CPU Power Management
* Not all USB ports work on some boards
   * This is due to not being assigned in ACPI, you need to manually add them in your DSDT
* Delayed updates
* ~~3rd Gen Threadripper is not supported on bare-metal~~
  * Latest BIOS and OpenCore now boot with TRx40 CPUs

AMD CPUs:
* AMD Ryzen 1000 Series
* AMD Ryzen 2000 Series
* AMD Ryzen 3000 Series
* AMD Athlon
* AMD ThreadRipper
* AMD FX Series

With Intel, the thanks to most of the CPUs being quite similar they have support when the CPU is spoofed to a supported model. The only downside is that the iGPU rarely work on Atom/Pentium/Celeron these models meaning a cheap iGPU Hackintosh is impossible with these CPUs. Regarding X99/LGA 2011-V3 CPUs, there's the issue that these CPUs were never shipped in a real Mac so quite a few issues are present when running macOS on these systems. Avoid if possible

**Dual Socket User Note**: Do note that the macOS kernel only supports a maximum of 64 threads. So for baller setups please be aware. And for dual socket users, you will need to use [AppleMCEReporterDisabler](https://github.com/acidanthera/bugtracker/files/3703498/AppleMCEReporterDisabler.kext.zip) in macOS Catalina

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
:::

## Unsupported CPUs

So with outright unsupported CPUs, you're split into 2 camps: Either too old to run or too new that patches aren't supported

**Too old to run**:

This mainly consists of CPUs that are missing the SSE4.2 instruction set required for Mojave and newer, you can get around this by replacing the telemetry plugin but not ideal. See [trashOS repo](https://github.com/khronokernel/trashOS) for more info

* Wolfdale (Intel Core2 Duo series)
   * E7xxx
   * E8xxx
* Yorkfeild (Intel Core2 Quad series)
   * E8xxx
   * E9xxx

Then there's the CPUs that are missing the SSE4.1 and older instruction sets, with these support is stuck an OS X 10.11 El Capitan
