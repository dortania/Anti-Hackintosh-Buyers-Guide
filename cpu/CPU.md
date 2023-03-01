# CPUs

Most Intel CPUs are supported and have instructions in the [OpenCore Install Guide](). Recent AMD CPUs work with additional macOS patches. The general requirements are listed below, with further details about AMD and Intel CPUs at the bottom of the page.

::: details CPU Requirements

Architecture Requirements:

* Both 32-bit and 64-bit CPUs are supported
  * 32-bit CPUs are supported from 10.4.1 to 10.6.8
  * 64-bit CPUs are supported in 10.4.1 and newer

AVX Requirements:

* AVX 2.0 is required for Ventura and newer

SSE Requirements:

* SSE3 is required for all Intel versions of OS X/macOS
* SSSE3 is required for all 64-bit versions of OS X/macOS
  * For CPUs missing SSSE3 (i.e. certain 64-bit Pentiums), we recommend running 32-bit userspace (`i386-user32`)
* SSE4 is required for macOS 10.12 and newer
* SSE4.2 is required for macOS 10.14 and newer
  * SSE4.1 CPUs are supported with [telemetrap.kext](https://forums.macrumors.com/threads/mp3-1-others-sse-4-2-emulation-to-enable-amd-metal-driver.2206682/post-28447707)
  * Newer AMD drivers also require SSE4.2 for Metal support. To resolve this, see here: [MouSSE: SSE4.2 emulation](https://forums.macrumors.com/threads/mp3-1-others-sse-4-2-emulation-to-enable-amd-metal-driver.2206682/)

Firmware Requirements:

* OS X 10.4.1 through 10.4.7 require EFI32 (i.e. IA32 (32-bit) version of OpenCore)
  * OS X 10.4.8 through 10.7.5 support both EFI32 and EFI64
* OS X 10.8 and newer require EFI64 (i.e. x64 (64-bit) version of OpenCore)
* OS X 10.7 through 10.9 require OpenPartitionDxe.efi to boot the Recovery partition

Kernel Requirements:

* OS X 10.4 and 10.5 require 32-bit kexts due to only supporting 32-bit kernelspace
  * OS X 10.6 and 10.7 support both 32 and 64-bit kernelspace
* OS X 10.8 and newer require 64-bit kexts due to only supporting 64-bit kernelspace
  * Run `lipo -archs` to know what architectures your kext supports (remember to run this on the binary itself and not the .kext bundle)

Core/Thread Count Limits:

* OS X 10.10 and below may not boot with more than 24 threads (evident by a `mp_cpus_call_wait() timeout` panic)
* OS X 10.11 and newer have a 64 thread limit
* `cpus=` boot argument can be used as a workaround, or disabling hyperthreading

:::

### [Intel Requirements](./Intel.md)
### [AMD Requirements](./AMD.md)

::: tip Recommendations

If buying a new CPU, the recommendation is to go with a modern Intel CPU (Coffee Lake or newer).

:::

