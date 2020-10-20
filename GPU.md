# GPUs

~~Get an RTX GPU, I want to see people suffer as they slowly realize that they don't even have support in High Sierra. Let the Nvidia fans die a slow and painful death, let this be a reminder to never cross our lord and savior Tim Apple~~
If you don't want a headache, stay away from all Nvidia GPUs that aren't Kepler based. Currently(and likely forever), Turing and Volta GPUs have no support whatsoever in any version of macOS while Pascal and Maxwell have their support stopping in High Sierra while also requiring Web Drivers so they're not native GPUs(this is important because that means another point of failure)

> B-b-but are the drivers out yet?

![Web Drivers](WebDrivers.gif)

For GPUs we recommend, check out the [GPU Buyers Guide](https://dortania.github.io/GPU-Buyers-Guide/)
And for those who are running unsupported GPUs, there's still hope for you! With our patent pending [**How to disable your unsupported GPU for macOS Guide**](https://dortania.github.io/Getting-Started-With-ACPI/Desktops/desktop-disable.html), even a simpleton like you can experience the glories of Mojave and beyond!

> Are there any GPU board partners I should avoid when buying a GPU?

Why I'm glad you asked, most manufactures actually have a pretty good track record with Hackintoshes but there's 2 specific brands to avoid. While it is possible to install with these GPUs, there still is a high possibility of issues arising like instability and black screens:

* XFX(may work with CSM/legacy mode turned off, make sure it's in UEFI mode)
* PowerColor
* MSI(Navi specifically, Vega and Polaris are fine)

Note: AMD Navi support is still quite finicky, with WhateverGreen not being updated yet

::: tip Recommendations

So our overall recommendation for GPUs:

* Newer AMD GPUs:
  * Polaris 10 and 20(RX 4XX, 5XX)
  * Vega 10 and 20(RX Vega 56, 64 and VII)
  * Navi 10(RX 5XXX)
* Overall brand recommendations:
  * Sapphire
  * Asus
  * Gigabyte
:::

**GPUs that aren't supported AT ALL**

Ampere

* RTX 3090
* RTX 3080
* RTX 3070

Turing

* Titan RTX
* RTX 2080 Ti
* RTX 2080 Super
* RTX 2080
* RTX 2070 Super
* RTX 2070
* RTX 2060 Super
* RTX 2060
* GTX 1660 Ti
* GTX 1660
* GTX 1650

* Quadro RTX 8000
* Quadro RTX 6000
* Quadro RTX 5000
* Quadro RTX 4000

Volta

* Titan V
* Titan V CEO Edition

* Quadro GV100

Lexa

* RX 540/X
* RX 550/X

**GPUs to avoid**

Pascal

* GTX Titan X(GP 102-400 Pascal core)
* GTX Titan Xp(GP 102-450 Pascal core)
* GTX 1080/Ti
* GTX 1070/Ti
* GTX 1060
* GTX 1050/Ti
* GT 1030

* Quadro P400
* Quadro P600
* Quadro P620
* Quadro P1000
* Quadro P2000
* Quadro P4000
* Quadro P5000
* Quadro P6000
* Quadro GP100

Maxwell

* GTX Titan X(GM 200 Maxwell core)
* GTX 980/ti
* GTX 970
* GTX 960
* GTX 950
* GTX 750/ti
* GTX 745

* Quadro K620
* Quadro K1200
* Quadro K220
* Quadro M2000
* Quadro M4000
* Quadro M5000
* Quadro M6000
