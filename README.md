# Copy to VM

Copy files from host Windows machine to local virtual machine

## Overview

Found this nifty PowerShell cmdlet `Copy-VMFile` to copy a file to a virtual machine, so I put it inside this script with parameters and simple logging for ease of use.

## Script Parameters

| **Parameters** | **Description** |
| -------------- | --------------- |
| `-VirtualMachineName` | Name of the virtual machine we are copying the file to |
| `-SourcePath` | Absolute path to the source file we are copying from the host machine, including the file name  |
| `-DestinationPath` | Absolute path of the destination path we are copying to on the VM, including the file name |

## Running the Script

1. Open a PowerShell session as Administrator

2. Optionally run the following to allow the current session to run scripts not digitally signed:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

3. For example:

```powershell
.\Copy-to-VM.ps1 `
  -VirtualMachineName "Example-VM-Name" `
  -SourcePath "C:\Example-File.txt" `
  -DestinationPath "D:\Example-Directory\Example-File.txt" `
```

## Dependencies

* [Hyper-V Module](https://docs.microsoft.com/en-us/powershell/module/hyper-v/?view=win10-ps)

  * [Copy-VMFile](https://docs.microsoft.com/en-us/powershell/module/hyper-v/copy-vmfile?view=win10-ps)

## Owner

[Michael A. Agarenzo](https://magarenzo.com)
