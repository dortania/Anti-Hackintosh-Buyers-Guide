# Coolers

The most popular liquid coolers are all-in-one (AIO). They are closed loop kits that come preassembled. If you're uncertain which AIO kit you should purchase, the YouTube channel GamersNexus provides extremely thorough reviews. The kits connect to your motherboard via the internal USB 2.0 header. When creating a USB map you need to consider this or you will not be able to control it.

Excluding others and first generation AIO kits from Asetek, they have will have either volatile or persistent memory:

1. NZXT and Corsair have volatile memory that persists as long as the PSU is left powered on (I).
2. EVGA kits have persistent memory. Changing settings with the software in Windows allows you to write to memory. If the PSU is powered off (O), settings are not lost.

Almost all use the same internal hardware provided by Asetek. It is impossible to control them with the motherboard. They are not designed this way. The three pin connector for the CPU header is only there to report the Pump and Radiator fan speeds. It is a one-way communication. The only way to control these variables is through the USB header with software. Other AIO kits that are not based on Asetek have the ability to be controlled via the motherboard via the 4 pin CPU header. Thermaltake and Deep Cool are some examples.

There are Python based utilities for controlling your kit on GitHub, though this is usually unnecessary, as setting it up once in Windows will be enough until you turn off the PSU. Python based [liquidctl](https://github.com/jonasmalacofilho/liquidctl) is developed for macOS and works for a few models from NZXT, EVGA, and Corsair.

There are no real compatibility issues with AIO kits and macOS. They will work regardless of booted OS as long as they are initially setup with Windows.
