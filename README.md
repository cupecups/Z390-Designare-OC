![alt text](https://github.com/cupecups/Z390-Designare-OC/blob/main/1311.png)

# Z390-Designare-OC
about Z390 Designare opencore hackintosh

update to 13.3.1 ~with caution - have some issue with wifi BT and ethernet not working when appleVTD enable and issue with more 16gb ram_
fixed with opencore 0.9.2 and enable DisableIoMapperMapping on kernel - Quirk
#
simple fix is add kernel patch (for opencore 0.9.1 or lower with ventura 13.3.x)
1. Identifier: com.apple.iokit.IOPCIFamily
2. Base: __ZN11IOPCIBridge20addBridgeMemoryRangeEyyb
3. Comment: CaseySJ - Fix AppleVTD issue in 13.3+
4. Find: 4C89F6E8 9AFF0000
5. Replace: 4C89F690 90909090
6. MinKernel: 22.4.0
7. Count: 1
8. Enabled: True
## or disable appleVTD
1. enable disableIOmapper on kernel quirk or disable intel VT-D on bios
2. add boot arg e1000=0


thanks to CaseySJ

