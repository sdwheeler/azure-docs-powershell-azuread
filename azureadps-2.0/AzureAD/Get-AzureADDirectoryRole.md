---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
ms.custom: sfi-ga-nochange
---

# Get-AzureADDirectoryRole

## SYNOPSIS
Gets a directory role.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADDirectoryRole [-Filter <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADDirectoryRole -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADDirectoryRole cmdlet gets a directory role from Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get a directory role by ID
```
PS C:\>Get-AzureADDirectoryRole -ObjectId "62e90394-69f5-4237-9190-012177145e10"

ObjectId                             DisplayName                        Description
--------                             -----------                        -----------
62e90394-69f5-4237-9190-012177145e10 Global Administrator              Can manage all aspects of Azure AD and Microsoft services that use Azure AD identities.
```

### Example 2: Get all directory roles
```
PS C:\>Get-AzureADDirectoryRole

ObjectId                             DisplayName                        Description
--------                             -----------                        -----------
62e90394-69f5-4237-9190-012177145e10 Global Administrator               Can manage all aspects of Azure AD and Microsoft services that use Azure AD identities.
2b3a80bc-51a4-476d-8e09-cd8b6cdde5ea Directory Writers                  Can read and write basic directory information. For granting access to applications, not intended for users.
526b7173-5a6e-49dc-88ec-b677a9093709 User Administrator                 Can manage all aspects of users and groups, including resetting passwords for limited admins.
542f5aef-b23f-4e34-a838-6f2b9205b3d6 Directory Synchronization Accounts Only used by Azure AD Connect service.
68239fa3-6b01-4396-aeb4-6af38a1b6abf Directory Readers                  Can read basic directory information. Commonly used to grant directory read access to applications and guests.
8c6a5c45-e93e-4f2b-81be-b57ad4c43ddd Privileged Role Administrator      Can manage role assignments in Azure AD, and all aspects of Privileged Identity Management.
8f8a1cf4-d535-4ccd-8552-7267c7ee0a88 Helpdesk Administrator             Can reset passwords for non-administrators and Helpdesk Administrators.
d96eb2b3-0970-4827-8f26-6008efd86511 Security Administrator             Can read security information and reports, and manage configuration in Azure AD and Office 365.
```

## PARAMETERS

### -Filter
The oData v3.0 filter statement. 
Controls which objects are returned.

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

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
Specifies the ID of a directory role in Azure AD.

```yaml
Type: String
Parameter Sets: GetById
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

See the [migration guide for Get-AzureADDirectoryRole](./migrate/Get-AzureADDirectoryRole.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[Enable-AzureADDirectoryRole](Enable-AzureADDirectoryRole.md)
