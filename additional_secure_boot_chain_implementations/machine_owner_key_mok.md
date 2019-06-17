## Machine Owner Key (MOK) {#machine-owner-key-mok}

Multiple Linux distributions have implemented UEFI Secure Boot, but this creates problems deploying 3<sup>rd</sup> party modules and custom-built kernels alongside components signed by the UEFI certificate Authority (CA). The Machine Owner Key [MOK](https://wiki.ubuntu.com/UEFI/SecureBoot) concept can be used with a signed shim loader to enable key management at the user/sysadmin level.

Figure 3-1 and Table 3-1 provide an overview of MOK.

![](media/image8.png)

Figure 3-1: Linux MOK Boot, (source: “[UEFI Secure Boot Webinar](https://www.suse.com/media/presentation/uefi_secure_boot_webinar.pdf)”)

Table 3-1: Linux MOK Boot

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | OS Kernel Verification | OSV | External storage |
| **CDI** | Shim | OSV | External storage |
|  | MOK list | User | Variable |
| **UDI** | OS Kernel | User | External storage |