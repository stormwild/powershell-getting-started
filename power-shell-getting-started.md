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