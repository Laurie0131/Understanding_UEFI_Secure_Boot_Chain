## SMM Runtime Communication {#smm-runtime-communication}

System Management Mode (SMM) is a special highly privileged processor execution mode. One usage of SMM is that the Firmware may provide some special service in SMM, which is referred to as an SMI handler. The SMI handler uses a shared buffer ([SMM Communication Buffer](https://github.com/tianocore-docs/Docs/raw/master/White_Papers/A_Tour_Beyond_BIOS_Secure_SMM_Communication.pdf)), to convey information to the service consumer during OS runtime. Table 2-11 describes SMM Runtime Communication Verification.

Table 2-11: SMM Runtime Communication Verification

| **Item** | **Entity** | **Provider** | **Location** |
| --- | --- | --- | --- |
| **TP** | SMM Communication Verifier Code | OEM | Originally on flash, loaded in SMRAM |
| **CDI** | SMI handler | OEM | Originally on flash, loaded in SMRAM |
| **UDI** | SMM communication buffer | Any | DRAM |

The SMM communication buffer is not signed because any program may use the buffer to invoke SMM services. SMM communication is treated as an attack surface, so the SMI handler must verify the contents of the SMM communication buffer. Since there is no signature, common verification is limited to prevent SMM attacks since it cannot verify the originator.