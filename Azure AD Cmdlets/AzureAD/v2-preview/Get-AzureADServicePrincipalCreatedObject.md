---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipalCreatedObject

## SYNOPSIS
Get objects created by a service principal.

## SYNTAX

```
Get-AzureADServicePrincipalCreatedObject -ObjectId <String> [-All <Boolean>] [-Top <Int32>]
```

## DESCRIPTION
The Get-AzureADServicePrincipalCreatedObject cmdlet gets an object created by a service principal in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Retrieve the objects that were created by a service principal
```
PS C:\> $ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
PS C:\> Get-AzureADServicePrincipalCreatedObject -ObjectId $ServicePrincipalId
```

The first command gets the ID of a service principal by using the Get-AzureADServicePrincipal (./Get-AzureADServicePrincipal.md)cmdlet. 
The command stores the ID in the $ServicePrincipalId variable.

The second command gets objects created by the service principal identified by $ServicePrincipalId.

## PARAMETERS

### -All
If true, return all objects created by the service principal.
If false, return the number of objects specified by the Top parameter

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
Specifies the ID of a service principal in Azure AD.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADServicePrincipal]()
