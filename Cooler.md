# Coolers

The most popular liquid coolers are all-in-one (AIO). They are closed loop kits that come pre-assembled. Whether you get one from NZXT, Corsair, or EVGA - they all use the same internal hardware provided by Asetek. If you're uncertain which AIO kit you should purchase, the YouTube channel GamersNexus provides extremely thorough reviews.

The ease of use and installation of these kits make them very popular for PC builders. A majority of these builders are gamers, and as such the software provided by the branded kits are only available for Windows. Thus open-source community made software was created for Linux and even macOS. The kits connect to your motherboard via the internal USB 2.0 header. When creating a USB map you need to consider this or else you will not be able to control it.

Like all hardware, they go through revisions. First generation AIO kits from Asetek did not have any form of volatile or persistent memory. When the computer was shutdown, the settings were lost. Upon start up the accompanying software would load the settings a user saved in the application. This changed with later revisions. There are two ways OEMs went about this:

1. Kits like those from NZXT, have volatile memory that persists as long as the PSU is left powered on (I). If the hardware switch is flipped to the off (O) position, settings are lost. You can reboot between Windows and macOS without issue.
2. EVGA kits have persistent memory. Changing your settings with the software in Windows allows you to write the settings to the memory. If the PSU is powered off (O), settings are not lost. You can reboot between Windows and macOS without issue.

It is impossible to control AIO kits from the motherboard. They are not designed this way. The three pin connector for the CPU header is only there to report the Pump and Radiator fan speeds. It is a one-way communication. It does not respond to Voltage or PWM controls. The only way to control these variables is through the USB header with software.

There are Python based utilities for controlling your kit on GitHub. Though with revisions in the last four years, this is usually unnecessary. Setting it up once in Windows will be enough until you turn off the PSU. Most of them are command line based and only for Linux and Windows. Their sole intent was to replace the often buggy OEM provided software. Python based [liquidctl](https://github.com/jonasmalacofilho/liquidctl) is developed for macOS and works for a few models from NZXT, EVGA, and Corsair.

There are no real compatibility issues with AIO kits and macOS. They will work regardless of booted OS as long as they are initially setup with Windows.