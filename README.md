# Printers Management by PowerShell

**1. Stag/Add dirver packets (_.inf_ files) into Windows Driver Store**
```
pnputil /add-driver <the-path-to-driver>\*.inf
Example 1: pnputil /add-driver c:\Users\Administrator\Download\hp\eng\laster5l.inf
Example 2: pnputil /add-driver c:\Users\Administrator\Download\hp\eng\*.inf
```
> _PnPUtil.exe_ is a cmd tool that lets an administrator perform actions on driver packages, like add, installation, deletion, and looking for.
> A driver package must be staged to the Driver Store before the package can be used to install any devices.
> [_PnPUtil Syntax] (https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/pnputil-command-syntax)

Staging a drive packet into the Driver Store performs verified and validated.
* Verifying integration: INF file must have a _CatelogFile_ directive in the *Version* section; Any file referenced by INF file; _Catalog file_ signed with a trusted signature. 
* Validating: User permission; Syntax of driver files.



```
Add-PrinterDriver 
```

