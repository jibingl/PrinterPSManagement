# Printers Management by PowerShell

**1. Manage dirver packets (_.inf_ files) in _Windows Driver Store_**

**_PnPUtil.exe_** is a cmd tool that lets an administrator perform actions on driver packages, like add, installation, deletion, and looking for.
A driver package must be staged to the _Driver Store_ before the package can be used to install any devices.
```
pnputil /add-driver <the-path-to-driver>\*.inf
Example 1: pnputil /add-driver c:\Users\Administrator\Download\hp\eng\laster5l.inf    #Add a driver file
Example 2: pnputil /add-driver c:\Users\Administrator\Download\hp\eng\*.inf           #Add multiple driver files
```
> [_PnPUtil Syntax] (https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/pnputil-command-syntax)

_Staging_ performs **verification** and **validation** on the driver packets:
* Verifying integration: INF file must have a _CatelogFile_ directive in the *Version* section; Any file referenced by INF file; _Catalog file_ signed with a trusted signature. 
* Validating: User permission; Syntax of driver files.

After _Staging_, Windows system generates a _Published Name_ for the added drivers. The format is `oem*.inf` where * represented by a number.
The `oem*.inf` stored in `C:\Windows\INF_ folder`; The added driver packets saved in `C:\Windows\System32\DriverStore\`.

---

**2. _PrintManagement_ cmdlets**

Add a local printer:
```
Add-PrinterDriver 
```

