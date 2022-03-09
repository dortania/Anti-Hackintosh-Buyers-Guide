# Storage

Storage is a section that can be quite confusing as there a lot of mixed reports regarding PCIe/NVMe based devices, many of these reports are based off old information from back when PCIe/NVMe drives were not natively supported like block size mattering or require kexts/.efi drivers. Well, High Sierra brought native support for these types of drives but certain ones still do not work and can cause instability if not removed/blocked out at an ACPI level.

The other big issue surrounds all Samsung NVMe drives, specifically that they're known to slow down macOS, not play well with TRIM and even create instability at times. This is due to the Phoenix controller found on Samsung drives that macOS isn't too fond of, much preferring the Phison controller found in Sabrent Rocket drives and Western Digital's in-house controllers(WD SN750). The easiest way to see this is with boot up, most systems running Samsung drives will have extra long boot times and have their drives run hotter due to the software TRIM failing(hardware TRIM still should be enabled but no partiality). Also some older Intel drives and Kingston NVMe drives also experience these issues.

And while not an issue anymore, do note that all of Apple's PCIe drives are 4K sector-based so for best support only choose drives with such sectors.

**Note for laptop users**: Intel SSDs don't always play nicely with laptops and can cause issues, avoid when possible

**SSD/Storage Options that are NOT supported:**

* Any eMMC based storage (commonly found in netbooks, some tablets and low end computer models.)
* Samsung PM981 and PM991(commonly found in OEM systems like laptops)
  * Even if PM981 has been fixed with [NVMeFix](https://github.com/acidanthera/NVMeFix/releases) version 1.0.2 there is still plenty of kernel panics issues
* Micron 2200S
  * Many users have report boot issues with this drive
* SK Hynix PC711
  * The proprietary Hynix NVMe controller on this drive is not supported at all, and it will not boot with macOS

**SSDs to avoid**

Samsung:

* Samsung 970 Evo Plus (While not natively supported out of the box, a [firmware update from Samsung](https://www.samsung.com/semiconductor/minisite/ssd/download/tools/) will allow these drives to operate in macOS)

Intel:

* Intel 600p([Any fix for Intel 600p NVMe Drive? #1286](https://github.com/acidanthera/bugtracker/issues/1286))
  * note the Intel 660p are fine

For all NVMe SSDs, its recommended to use [NVMeFix.kext](https://github.com/acidanthera/NVMeFix) to fix power and energy consumption on these drives
