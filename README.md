# Z390-Designare-OC
about Z390 Designare opencore hackintosh

dont update to 13.3 if -  some issue is wifi BT and ethernet not working
simple fix is add kernel patch 
1. Identifier: com.apple.iokit.IOPCIFamily
2. Base: __ZN11IOPCIBridge20addBridgeMemoryRangeEyyb
3. Comment: CaseySJ - Fix AppleVTD issue in 13.3+
4. Find: 4C89F6E8 9AFF0000
5. Replace: 4C89F690 90909090
6. MinKernel: 22.4.0
7. Count: 1
8. Enabled: True
## or disable appleVTD

![alt text](https://github.com/cupecups/Z390-Designare-OC/blob/main/vent.png)
