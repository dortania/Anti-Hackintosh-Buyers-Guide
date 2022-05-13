# Wireless

For wireless, keep in mind that macOS has a very limited selection for native Wifi and Bluetooth cards. Midi made a great list on supported models that you can find in the [r/Hackintosh FAQ](https://www.reddit.com/r/hackintosh/wiki/faq#wiki_wifi_compatibility). For those who are either motherboard shopping or just looking for dedicated wireless, keep in mind that the following wireless cards are not supported or may have limited compatibility:

**Wireless cards that aren't supported AT ALL**

* Any Realtek based WiFi

**Wireless cards to avoid**

* Any USB based (Ralink and Realtek) as these generally aren't as reliable and some macOS functions like Handoff and Apple Watch Unlock may not function correctly
  * Many USB based WiFi cards will "work" but may be reliant on third party software and will not function natively
  * Some users have reported limited success with Bluetooth USB adapters but [YMMV](https://www.urbandictionary.com/define.php?term=ymmv)
* Recent development efforts have enabled (limited) WiFi and Bluetooth functionality in macOS for Intel Wireless cards
  * ***There are still major caveats to using Intel Wifi cards, including but not limited to issues with WiFi performance, broken Continuity/Handoff/Apple Watch Unlock, and more. Avoid them unless you are forced to use one, like if you are using a laptop with soldered WiFi or CNVi***
  * Intel WiFi is enabled through either [**itwlm.kext** or **Airportitwlm.kext**](https://github.com/OpenIntelWireless/itlwm)
  * Intel Bluetooth is enabled through [**IntelBluetoothFirmware.kext**](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) (paired with [**BlueToolFixup.kext**](https://github.com/acidanthera/BrcmPatchRAM) in macOS 12 and newer due to changes in Apple's Bluetooth stack)
  * Compatibility is always changing, so please refer to the [OpenIntelWireless Docs](https://openintelwireless.github.io) and [OpenIntelWireless GitHub Repo](https://github.com/OpenIntelWireless) for updated installation instructions and compatibility
* Killer WiFi cards may be usable depending on the model
  * Recent Killer Wireless cards now use Intel WiFi chipsets
  * This means that they ***can*** work in macOS, with the same caveats as and compatibility restrictions as above

Those who would like a list of supported models can check out the [Wireless Buyers Guide](https://dortania.github.io/Wireless-Buyers-Guide/)
