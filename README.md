# Hackintosh-HP-14-BS743TU

[![ThinkPad](https://img.shields.io/badge/HP-14--BS743TU-blue.svg)](https://support.hp.com/sg-en/document/c06049042)
[![MacOS High Sierra](https://img.shields.io/badge/High_Sierra-10.15-red.svg)](https://www.apple.com/)
[![MacOS Mojave](https://img.shields.io/badge/Mojave-10.14-red.svg)](https://www.apple.com/)
[![MacOS Catalina](https://img.shields.io/badge/Catalina-10.15-red.svg)](https://www.apple.com/)
[![MacOS BigSur](https://img.shields.io/badge/Big_Sur-11.5-red.svg)](https://www.apple.com/)
[![MacOS Monterey](https://img.shields.io/badge/Monterey-12.1-red.svg)](https://www.apple.com/)
[![MacOS Ventura](https://img.shields.io/badge/Ventura-13.2.1-red.svg)](https://www.apple.com/)
[![Release](https://img.shields.io/badge/Download-latest-brightgreen.svg)](https://github.com/muhrizki1996/Hackintosh-HP-14-BS743TU/releases/latest)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.9.0-blue.svg)](https://github.com/acidanthera/OpenCorePkg/releases/latest)

This is my complete EFI folder to be used for hackintosh on HP 14-BS743TU notebook with multibooting:
- macOS High Sierra 10.13.x
- macOS Mojave 10.14.x
- macOS Catalina 10.15.x
- macOS Big Sur 11.x
- macOS Monterey 12.x
- macOS Ventura 13.x
 
<img src="/img/Screenshot.png?raw=true" alt="macOS Screenshot" align="center">
 
> ## How to Get
- Clone whole repo: $ `git clone https://github.com/muhrizki1996/Hackintosh-HP-14-BS743TU`
- Download [Specific Folder](https://minhaskamal.github.io/DownGit/#/home) only.
 
> ## Notebook Specs
<img src="/img/HP-14-BS743TU.png?raw=true" alt="HP 14-BS743TU" align="right" width="433" height="325">

- [x] <b>Model</b>: HP 14-BS743TU
- [x] <b>CPU</b>: Intel® Core™ i3-6006U (2 GHz, 3 MB cache, 2 cores)
- [x] <b>GPU</b>: Intel HD Graphics 520 @ 1GB
- [x] <b>RAM</b>: 4 GB DDR4-2133 SDRAM (1 x 4 GB)
- [x] <b>Storage</b>: 1TB SATA HDD @ 5400rpm (GUID Partition Table) + 120GB SATA SSD (Via HDD Caddy)
- [x] <b>Audio</b>: Realtek ALC282 HD Audio Controller
- [x] <b>Wifi</b>: Realtek RTL8723DE
- [x] <b>Ethernet</b>: Realtek RTL8168H/8111H
- [x] <b>Bluetooth</b>: Broadcom BCM4350C2
- [x] <b>Others</b>: 1 USB 2.0 ports, 2 USB 3.1 ports, TouchPad, VGA port, HDMI port, WebCam HP TrueVision HD, 14" diagonal HD SVA BrightView WLED-backlit (1366 x 768), 3.5mm Combo Headphone Jack, SD Media Card Reader, 4-cell, 41 Wh Li-ion Battery
- [x] <b>BIOS</b>: xxx
 
> ## EFI Contains
- [x] <b>OpenCore binary, config.plist</b>, drivers for uefi, themes, etc..
- [x] <b>Patched ACPI Tables (mostly SSDT)</b> for Sleep, etc..
- [x] <b>3rd party kexts</b> for working devices under macOS Big Sur (11.x) and macOS Ventura (13.x)
 
<details>
<summary><strong> What's Worked </strong></summary>
<br>

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| QE/CI Enabled Graphics               | ✅   | OpenCore Inject + WhateverGreen.kext + BrightnessKeys.kext |
| Brightness Adjustments               | ✅   | WhateverGreen.kext |
| Realtek ALC282 Audio out             | ✅   | AppleALC.kext with Layout ID = 03 |
| Realtek RTL8168H/8111H               | ✅   | RealtekRTL8111.kext |
| Broadcom BCM4350C2 Bluetooth         | ✅   | BlueToolFixup.kext and BrcmPatchRAM.kext + bt.command |
| Touchpad                             | ✅   | VodooPS2Controller.kext |
| Multimedia Keys                      | ✅   | Works as on Windows / Linux |
| Battery Indicator                    | ✅   | ECEnabler.kext |
| WebCam HP TrueVision HD              | ✅   | Native + FaceTimeHDCam.kext for spoofing UVC WebCams as FaceTime HD (not working on macOS Big Sur and newer) |
| USB2.0 Port + USB 3.0 Port           | ✅   | USBPorts.kext |
| Sleep and Wake                       | ✅   | Native + SSDT Patch for Sleep while Power plugged in |
| Mac App Store Access                 | ✅   | Native |
| iMessage and FaceTime                | ✅   | Native |
| HDMI Port                            | ✅   | Tested on Infocus |
| VGA Port                             | ✅   | Tested on Asus Monitor |
| SD Card Reader                       | ✅   | Tested SanDisk 16GB SD Card |
 
</details>

<details>
<summary><strong> List of Gestures </strong></summary>
<br>

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| 2 Finger Swipe Left                  | ✅   | Forward. |
| 2 Finger Swipe Right                 | ✅   | Backward. |
| 3 Finger Swipe Left                  | ✅   | Right Space/Full Screen apps switch. |
| 3 Finger Swipe Right                 | ✅   | Left Space/Full Screen apps switch. |
| 3 Finger Swipe Up                    | ✅   | Toggle Full screen Switch. |
| 3 Finger + Thumb Swipe Up            | ✅   | Show Desktop. |
| 3 Finger + Thumb Swipe Down          | ✅   | Hide Desktop. |
| 3 Finger Swipe Down                  | ❌   | Do Nothing. |
| 4 Finger Swipe Up                    | ❌   | Do Nothing. |
| 4 Finger Swipe Down                  | ❌   | Do Nothing. |

</details>
 
<details>
<summary><strong> Not Working </strong></summary>
<br>

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| Realtek RTL8723DE                    | ❌   | Replace with TP-Link TL-WN725N with chris1111 Wireless USB OC Big Sur Adapter kext |

</details>
 
<details>
<summary><strong> Not Tested </strong></summary>
<br>

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| Hand Off                             | ❌   | Not tested yet. |

</details>
 
> ## Notes

1. Please generate newly and fresh Serial Number, MLB, ROM, and UUID for your Hack.
2. EFI can be used for USB Installer and Normal Boot.
3. For Bluetooth to be working, you must run file "bt.command" every boot.
 
> ## Support

<details>
<summary><strong> Video Tutorials </strong></summary>
<br>

- [Multibooting](https://www.youtube.com/watch?v=vXMNyiEgD6o) Windows, Ubuntu, PhoenixOS & macOS using Clover (UEFI)
- Video demonstration about [Full Graphics Acceleration support](https://www.youtube.com/watch?v=) (QE/CI enabled) under macOS [Soon!].

</details>

<details>
<summary><strong> Credits </strong></summary>
<br>

- [Apple](https://www.apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for all the kexts/utilities that they made.
- [Rehabman](https://github.com/RehabMan) and [Daliansky](https://github.com/daliansky) for the patches and guides and kexts.
- [Dortania](https://github.com/dortania) for for the OpenCore Install Guide.
- [badruzeus](https://github.com/badruzeus) for inspirational Repo and Repo README Layout.
- [banhbaoxamlan](https://github.com/banhbaoxamlan) for inspirational Repo README Layout.
- [Olarila](https://www.olarila.com/topic/6278-olarila-vanilla-images-macos-installer/) Vanilla Images.
- [Olarila](https://www.olarila.com/topic/5676-hackintosh-efi-folder-with-clover-and-opencore/) EFI Mods for Clover and OpenCore.

</details>
