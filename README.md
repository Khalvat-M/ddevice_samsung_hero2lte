Copyright 2021 - The Khalvat-M project

Device configuration for Samsung Galaxy S7 Edge Unified variants (SM-G935F, SM-G935W8, SM-G935S, SM-G935L).
========================================

Basic   | Specification List
-------:|:-------------------------
CPU     | Quad-core 2.6 GHz + Quad-core 1.6 GHz
Chipset | Samsung Exynos 8890
GPU     | ARM Mali-T880 MP12
Memory  | 4 GB
Shipped Android Version | 6.0.1
Storage | 32/64 GB
MicroSD | Up to 256 GB
Battery | Li-Ion 3000 mAh
Dimensions | 150,9 mm x 72,6 mm x 7,7 mm
Display | 2560 x 1440 pixel, 5.5"
Rear Camera  | 12 MP, f/1.7, 25mm, phase detection autofocus, LED flash
Front Camera | 5 MP, f/1.7, 21mm
Release Date | March 2016


![Galaxy S7 Edge](https://github.com/Khalvat-M/device_samsung_hero2lte/blob/11.0/information/hero2lte.gif)


# For building Android R
### create `.repo/local_manifests/roomservice.xml` with the following content:

***
```xml
<?xml version="1.0" encoding="UTF-8"?>
 <manifest>
        
 <remote  name="khalvat"
    fetch="https://github.com/Khalvat-M"
    revision="11.0" />

 <remote  name="linos"
    fetch="https://github.com/LineageOS"
    revision="lineage-18.1" />

    <!--LineageOS -->
    <project name="android_hardware_samsung" path="hardware/samsung" remote="linos" />
    <project name="android_hardware_samsung_slsi_exynos" path="hardware/samsung/slsi/exynos"  remote="linos" />
    <project name="android_device_samsung_slsi_sepolicy" path="device/samsung_slsi/sepolicy"  remote="linos" />
    <project name="android_hardware_samsung_nfc" path="hardware/samsung/nfc"  remote="linos" />
    
    <!--Device -->
   <project name="device_samsung_hero2lte" path="device/samsung/hero2lte" remote="khalvat" />
   <project name="device_samsung_universal8890-common" path="device/samsung/universal8890-common" remote="khalvat" />
        
    <!--Kernel -->
    <project name="kernel_samsung_universal8890" path="kernel/samsung/universal8890" remote="khalvat" />
    
    <!--Vendor -->
    <project name="vendor_samsung" path="vendor/samsung" remote="khalvat" />
                  
 </manifest>
```
