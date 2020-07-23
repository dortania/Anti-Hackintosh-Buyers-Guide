# Networking

This section is specifically for dedicated NICs, generally most networking is supported either natively, like with Aquantia, or has drivers provided Mieze:

* [IntelMausiEthernet.kext](https://github.com/Mieze/IntelMausiEthernet)
   * For majority of Intel Controllers
* [SmallTree-I211-AT-patch](https://github.com/khronokernel/SmallTree-I211-AT-patch/releases)
   * For I211-AT which is commonly found on AMD boards
* [AtherosE2200Ethernet.kext](https://github.com/Mieze/AtherosE2200Ethernet)
   * For majority of Atheros Controllers
* [RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X)
   * For Realtek's Gigabit Ethernet
* [LucyRTL8125Ethernet](https://github.com/Mieze/LucyRTL8125Ethernet)
   * For Realtek's 2.5Gb Ethernet

Certain consumer NICs don't have support such as:
* Realtek L8200A(Only found in Asus boards)
* Intel I225-V 

For the i225-V, you can actually spoof it to a i225LM which is officially supported: [Example](https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#deviceproperties)


The issues come in when you either involve onboard server NICs or dedicated hardware like Mellanox's MNPA19-XTR 10Gbe NIC. You need to be quite vigilante and see if either the manufactures or the Hackintosh community have developed drivers, or instead, you can take the safe route and grab a 10Gbe Aquantia AQtion AQC-107 NIC as these are shipped in the iMacPro1,1, Macmini8,1 and MacPro7,1 so full native support. Note that [certain brands need patches](https://www.insanelymac.com/forum/topic/330614-aquantia-10-gb-ethernet-support-thread-10132-upwards/)

[SmallTree](https://www.small-tree.com/categories/10gb-ethernet-cards/) is the other popular option

**NICs cards to avoid**

* Intel Server NICs(including both 1Gbe and 10Gbe, [there's work arounds for X520 and X540 NICs](https://www.tonymacx86.com/threads/how-to-build-your-own-imac-pro-successful-build-extended-guide.229353/)
* HP Server NICs(including both 1Gbe and 10Gbe, generally rebranded Qlogic)
* Dell Server NICs(including both 1Gbe and 10Gbe, generally rebranded Broadcom or Intel)
* Mellanox NICs
