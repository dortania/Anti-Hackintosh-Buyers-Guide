# RAM

**General Guidance**

With RAM, it's generally the same logic for Windows: Make sure the CPU's memory controller can support the speeds you wish to run. macOS seems to be a bit more memory sensitive than Windows so you may get random lock-ups/kernel panics and the more memory you add, the more you need to lower the frequency to ease the memory controller. Generally, 32GB 3000MHz will run just fine on an i7 8700k but an i7 6700k may have to drop to 2666MHz for stability.

**XMP and Sleep/Other Issues**

It's hard enough to get sleep working on your Hack as it is, and XMP *can* make it harder. There is significant anecdotal evidence that for some motherboards, memory kits, and platforms, enabling XMP (sometimes called DOCP on AMD platforms) overclock profiles will break sleep on your system. Users report sleep working again after disabling the XMP profile, or simply performing a manual overclock at a lesser frequency than the XMP profile. Some USB issues have also been reported loosely tied to XMP, like an inability to unmount removable drives reliably. However, none of the XMP related issues are common, and your particular motherboard/CPU/RAM combination may not be affected.
