## Device Firmware Update {#device-firmware-update}

If the device firmware is updatable, the update must be verified.

The verifier is determined by the entity with write access to the device firmware location. The entity performing verification must be the same entity performing the update.

For example, if the device firmware is in the device internal location, which is not accessible by the host firmware, such as TPM, then the device must do the verification and update. If the device firmware is in the device internal location, but it is accessible by the host firmware, such as EC, then the host firmware may do the verification and update. If device firmware is on the external storage and loaded by system firmware, then the system firmware must do the verification and update.

Table 4-2: Device Firmware Update Verification

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | Firmware Update Verification | OEM or IHV | Depends |
| **CDI** | Firmware Update TCB Code | OEM or IHV | Depends |
|  | Firmware Update Signature Database (Policy) | OEM or IHV | Depends |
| **UDI** | Device Firmware Update Package | IHV | Originally on external storage (e.g. Hard drive, USB, Memory, or Read-Write Flash), loaded into device firmware unlockable environment. |