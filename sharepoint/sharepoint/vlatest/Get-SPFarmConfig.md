---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/26d6e44c-a606-47a1-a3e0-c4919670f684(Office.15).aspx
schema: 2.0.0
---

# Get-SPFarmConfig

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Get-SPFarmConfig [-AssignmentCollection <SPAssignmentCollection>] [-ServiceConnectionPoint]
```

## DESCRIPTION
The Get-SPFarmConfig cmdlet retrieves global settings for the local farm that are not members of the SPFarm object.
This cmdlet creates a new PSCustomObject object from the collection of properties returned from the local farm, and then adds this object to the pipeline.
The PSCustomObject object can be read, or modified and passed to the Set-SPFarmConfig cmdlet to change parameter values.

The properties collected in the PSCustomObject object must be farm-wide settings, and must be configurable only once for the entire farm.
The parameter name added to the PSCustomObject object must match exactly the input parameter name for the Set-SPFarmConfig cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### -------------EXAMPLE---------------- (SharePoint Server 2013)
```
C:\PS>$a = Get-SPFarmConfig

C:\PS>$a.AjaxTimeout = 200

C:\PS>$a | Set-SPFarmConfig
```

This example uses the Get-SPFarmConfig cmdlet to add the Ajax Timeout setting to the PSCustomObject object, sets the value for Ajax Timeout, and then passes PSCustomObject to the Set-SPFarmConfig cmdlet to change the Ajax Timeout setting.
Ajax Timeout, a farm-wide setting, is a member of the SPWebService object and cannot be accessed with a Windows PowerShell cmdlet.

You can perform the same operations with either of the following commands.

### -------------EXAMPLE---------------- (SharePoint Server 2016)
```
C:\PS>$a = Get-SPFarmConfig

C:\PS>$a.AjaxTimeout = 200

C:\PS>$a | Set-SPFarmConfig
```

This example uses the Get-SPFarmConfig cmdlet to add the Ajax Timeout setting to the PSCustomObject object, sets the value for Ajax Timeout, and then passes PSCustomObject to the Set-SPFarmConfig cmdlet to change the Ajax Timeout setting.
Ajax Timeout, a farm-wide setting, is a member of the SPWebService object and cannot be accessed with a Windows PowerShell cmdlet.

You can perform the same operations with either of the following commands.

## PARAMETERS

### -AssignmentCollection
Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceConnectionPoint
Gets the information stored in the current farm's service connection point in Active Directory.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
