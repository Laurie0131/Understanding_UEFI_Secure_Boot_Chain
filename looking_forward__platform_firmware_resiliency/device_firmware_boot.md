## Device Firmware Boot {#device-firmware-boot}

If device firmware is not in TCB, it must be verified by the system firmware or device firmware in TCB.

During system boot, host firmware may choose to verify some device firmware components. For device firmware stored in the device’s internal storage, verification may happen based upon device policy. For device firmware images in external storage loaded at runtime, verification is mandatory. Device firmware verification may follow the same rules as the system firmware verification. Device firmware is only loaded after it is verified.

Table 4-1: Device Firmware Boot Verification

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | Device Firmware Verification | OEM or IHV | Flash (Read Only Code), Device ROM. |
| **CDI** | System Firmware or Device firmware TCB | OEM or IHV | Flash (Read Only Code), ROM |
|  | Device Firmware Signature Database (Policy) | OEM or IHV | Flash (Read Only Data), ROM |
| **UDI** | Device Firmware | IHV | Device Internal Storage (or) |