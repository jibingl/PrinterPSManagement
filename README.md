# Printers Management by PowerShell
---
**1. Stag/Add dirver packets (_.inf_ files) into Windows Driver Store**
```
pnputil /add-driver c:\oem\*.inf
```
> PnPUtil (PnPUtil.exe) is a cmd tool that lets an administrator perform actions on driver packages, like add, installation, deletion, and looking for.
> A driver package must be staged to the Driver Store before the package can be used to install any devices.
> []https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/pnputil-command-syntax

Staging a drive packet into the Driver Store performs verified and validated.
* Verifying integration: INF file must have a _CatelogFile_ directive in the *Version* section; Any file referenced by INF file; _Catalog file_ signed with a trusted signature. 
* Validating: User permission; Syntax of driver files.



```
Add-PrinterDriver 
```

