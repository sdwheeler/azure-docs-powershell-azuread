---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADContactDirectReport

## SYNOPSIS
Get the direct reports for a contact.

## SYNTAX

```
Get-AzureADContactDirectReport -ObjectId <String> [-All <Boolean>] [-Top <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADContactDirectReport cmdlet gets the direct reports for a contact.

## EXAMPLES

### Example 1: Get the direct reports of a contact
```
PS C:\> $Contact = Get-AzureADContact -Top 1
PS C:\> Get-AzureADContactDirectReport -ObjectId $Contact.ObjectId
```

The first command gets a contact by using the Get-AzureADContact (./Get-AzureADContact.md)cmdlet, and then stores it in the $Contact variable.

The second command gets the direct reports for $Contact.

## PARAMETERS

### -All
If true, return all direct reports.
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
Specifies the ID of a contact in Azure Active Directory.

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

See the [migration guide for Get-AzureADContactDirectReport](./migrate/Get-AzureADContactDirectReport.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[Get-AzureADContact](Get-AzureADContact.md)

