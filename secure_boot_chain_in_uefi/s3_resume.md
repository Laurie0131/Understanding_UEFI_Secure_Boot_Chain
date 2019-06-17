## S3 Resume {#s3-resume}

S3 resume is a special boot path defined by the ACPI specification. During normal boot, firmware may save the system configuration and place the system in the S3 “sleep” state. During S3 resume phase, firmware loads the resume state to quickly “wakeup” the system and return to an operational state.

During S3 resume, firmware should not accept untrusted external inputs. The system configuration, referred to as the S3 Boot Script, should be stored in a secure place. [EDK II implements a lockbox for the S3 resume state](https://github.com/tianocore-docs/Docs/raw/master/White_Papers/A_Tour_Beyond_BIOS_Implementing_S3_resume_with_EDKII_V2.pdf). This implementation provides no UDI for S3 resume, so all components should be treated as CDI.