# PowerShell: Getting Started

by Michael Bender

This is an introductory course on PowerShell and how to use it for basic IT operations support.

## Outline 

- Intro to PowerShell
- PowerShell Basics
- Gathering Information with PowerShell
- Remoting with PowerShell
- Building a User Inventory Script with PowerShell

## What is PowerShell

Execution engine to interface with your environment using a variety of tools.

## Windows PowerShell

## PowerShell Core

OpenSource
Cross-Platform
Not all of Windows Specific Commands

## Get-Service

```ps
$data =  get-service |
>> where-Object Status -eq  'Stopped' |
>> select-object Name,Status

$data | out-file .\service.csv
```

```ps
$data | export-csv .\services2.csv
```

## $PSVersionTable

```ps
$PSVersionTable
```

Output

```sh

Name                           Value
----                           -----
PSVersion                      5.1.18362.1171
PSEdition                      Desktop
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
BuildVersion                   10.0.18362.1171
CLRVersion                     4.0.30319.42000
WSManStackVersion              3.0
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1


PS C:\Windows\system32>
```

PowerShell Core

```ps

Name                           Value
----                           -----
PSVersion                      7.1.2
PSEdition                      Core
GitCommitId                    7.1.2
OS                             Microsoft Windows 10.0.18363
Platform                       Win32NT
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0…}
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
WSManStackVersion              3.0
```