## Signed Recovery {#signed-recovery}

NIST [SP800-193](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-193.pdf) defines three principles supporting platform resiliency:

*   Protection,

*   Detection

*   Recovery

Signed UEFI capsule update and Intel® BIOS Guard provide these protections. Intel® Boot Guard and OBB verification provide detection. If firmware corruption is detected, the firmware can perform recovery to prevent a permanent denial of service (PDOS) attack. EDK II implements a signed recovery (see Table 2-10).

Table 2-10: Firmware Recovery Verification

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | Firmware Recovery Verification | OEM | Originally on flash, loaded into DRAM. |
| **CDI** | Firmware Recovery TCB Code | OEM | Originally on flash, loaded into DRAM. |
|  | Firmware Recovery Signature Database (Policy) | OEM | Originally on flash, loaded into DRAM. |
| **UDI** | Firmware Recovery Package | OEM | Originally on external storage (e.g. Hard drive, USB, Memory, or Flash), loaded into DRAM |

#### Signing {#signing}

The UDI is provided a new firmware image, the same as the UEFI Capsule Update implementation. The entire firmware binary must be signed using the OEM private key.

#### Public Key Storage {#public-key-storage}

The OEM public key should be embedded in the original firmware &amp; recovery launcher module.

#### Verification {#verification}

If firmware corruption is detected during boot, the recovery boot path is triggered. In this scenario, TP is the firmware recovery launcher module. This module loads the recovery image from a known source and verifies the signature. If TP passes verification, the recovery image is loaded and the recovery launcher module transfers control to the recovery image. If recovery verification fails, the recovery image is discarded and the recovery launcher attempts to locate additional recovery images. If all recovery images fail verification, the recovery process is aborted.

NOTE: The signed recovery image itself may be updatable even if it is on the flash region.