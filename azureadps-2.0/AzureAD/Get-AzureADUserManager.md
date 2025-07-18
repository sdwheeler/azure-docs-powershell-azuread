---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADUserManager

## SYNOPSIS
Gets the manager of a user.

## SYNTAX

```
Get-AzureADUserManager -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADUserManager cmdlet gets the manager of a user in the Microsoft Entra ID.

## EXAMPLES

### Example 1: Get the manager of a user
```
PS C:\>Get-AzureADUserManager -ObjectId "aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb"

ObjectId                             ObjectType
--------                             ----------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 User
```

This command gets the manager of the specified user.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event.
The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
The unique identifier of a user in the Microsoft Entra ID (UPN or ObjectId)

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

See the [migration guide for Get-AzureADUserManager](./migrate/Get-AzureADUserManager.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[Remove-AzureADUserManager](Remove-AzureADUserManager.md)

[Set-AzureADUserManager](Set-AzureADUserManager.md)
