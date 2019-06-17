## coreboot {#coreboot}

The open source [coreboot](https://coreboot.org) firmware project implements [verified boot](https://doc.coreboot.org/security/vboot/index.html?highlight=verified%20boot), which is similar to a combination of OBB verification and UEFI Secure Boot.

Figure 3-2 shows the verified boot flow. Table 3-2 shows keys used in the verified boot flow.

![](media/image9.png)

Figure 3-2: coreboot Verified Boot (source: “[Verified Boot in Chrome OS and how to make it work for you](https://static.googleusercontent.com/media/research.google.com/en/pubs/archive/42038.pdf)”)

Table 3-2: Keys used by coreboot verified boot (source: “[Verified Boot: Surviving in the Internet of Insecure Things](https://www.coreboot.org/images/c/ce/Verified_Boot_-_Surviving_in_the_Internet_of_Insecure_Things.pdf)”)

![](media/image10.png)

Table 3-3: coreboot Verified Boot (for firmware)

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | Read/Write Firmware Verification | OEM | Flash (Read Only Region) |
| **CDI** | Read-Only Firmware | OEM | Flash (Read Only Region) |
|  | Root key | OEM | RO firmware, Google Binary Blob (GBB) |
| **UDI** | Read/Write Firmware | OEM | Flash (Read Write Region) |

Table 3-4: coreboot Verified Boot (for OS)

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | OS Kernel Verification | OEM | Flash (Read Write Region) |
| **CDI** | Read-Write Firmware | OEM | Flash (Read Write Region) |
|  | Kernel Subkey | OSV | R/W firmware, Google Binary Blob (GBB) |
| **UDI** | OS Kernel | OSV | External storage |