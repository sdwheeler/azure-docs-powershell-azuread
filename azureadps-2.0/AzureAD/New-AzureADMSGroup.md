---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# New-AzureADMSGroup

## SYNOPSIS
Creates an Azure AD group.

## SYNTAX

```
New-AzureADMSGroup [-Description <String>] -DisplayName <String> [-IsAssignableToRole <Boolean>]
 -MailEnabled <Boolean> -MailNickname <String> -SecurityEnabled <Boolean>
 [-GroupTypes <System.Collections.Generic.List`1[System.String]>] [-Visibility <String>] [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADMSGroup cmdlet creates an Azure Active Directory (Azure AD) group.

## Examples

### Example : Create a group assignable to role
```
PS C:\> New-AzureADMSGroup -DisplayName "HelpDesk admin group" -Description "Group assignable to role" -MailEnabled $False -MailNickname "helpDeskAdminGroup" -SecurityEnabled $True -IsAssignableToRole $True -Visibility "Private"

Id                            : 1026185e-25df-4522-a380-7ab697a7241c
Description                   : Group assignable to role
OnPremisesSyncEnabled         : 
DisplayName                   : HelpDesk admin group
Mail                          : 
MailEnabled                   : False
IsAssignableToRole            : True 
MailNickname                  : helpDeskAdminGroup
ProxyAddresses                : {} 
SecurityEnabled               : True 
GroupTypes                    : {}
```

## PARAMETERS

### -Description
Specifies a description for the group.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Specifies a display name for the group.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MailEnabled
Indicates whether this group is mail enabled.

Currently, you cannot create mail enabled groups in Azure AD.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MailNickname
Specifies a mail nickname for the group.
If MailEnabled is $False you must still specify a mail nickname.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityEnabled
Indicates whether the group is security enabled.
For security groups, this value must be $True.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupTypes
Specifies that the group is a unified or dynamic group. 

Notes: 

* This parameter currently cannot be used to create dynamic groups. To create a dynamic group in PowerShell, you must use the Azure AD Preview module.


```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Visibility
Specifies the visibility of the group's content and members list.
This parameter can take one of the following values:

* "Public" - Anyone can view the contents of the group
* "Private" - Only members can view the content of the group
* "HiddenMembership" - Only members can view the content of the group and only members, owners, Global/Company Administrator, User Administrator and Helpdesk Administrators can view the members list of the group.

If no value is provided, the default value will be "Public".

Notes:

* This parameter is only valid for groups that have the groupType set to "Unified".
* If a group has this attribute set to "HiddenMembership" it cannot be changed later.
* Anyone can join a group that has this attribute set to "Public". If the attribute is set to Private or HiddenMembership, only owner(s) can add new members to the group and requests to join the group need approval of the owner(s).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsAssignableToRole
Indicates whether group can be assigned to a role. This property can only be set at the time of group creation and cannot be modified on an existing group.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object

## NOTES

See the [migration guide for New-AzureADMSGroup](./migrate/New-AzureADMSGroup.md) to the Microsoft Graph PowerShell.

This cmdlet is currently in Public Preview.
While a cmdlet is in Public Preview, we may make changes to the cmdlet which could have unexpected effects.
We recommend that you do not use this cmdlet in a production environment.

## RELATED LINKS

[Get-AzureADMSGroup](Get-AzureADMSGroup.md)

[Remove-AzureADMSGroup](Remove-AzureADMSGroup.md)

[Set-AzureADMSGroup](Set-AzureADMSGroup.md)

[Using attributes to create advanced rules](https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/)

