---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADServicePrincipalOwnedObject

## SYNOPSIS
Gets an object owned by a service principal.

## SYNTAX

```
Get-AzureADServicePrincipalOwnedObject -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADServicePrincipalOwnedObject cmdlet gets an object that is owned by a service principal in Azure Active Directory (Azure AD).

## EXAMPLES

### Example 1: Retrieve the owned objects of a service principal
```
PS C:\> $ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
PS C:\> Get-AzureADServicePrincipalOwnedObject -ObjectId $ServicePrincipalId
```

The first command gets the ID of a service principal by using the Get-AzureADServicePrincipal (./Get-AzureADServicePrincipal.md)cmdlet. 
The command stores the ID in the $ServicePrincipalId variable.

The second command gets the owned objects of a service principal identified by $ServicePrincipalId.

## PARAMETERS

### -All
If true, return all objects owned by this service principal.
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADServicePrincipal](Get-AzureADServicePrincipal.md)

