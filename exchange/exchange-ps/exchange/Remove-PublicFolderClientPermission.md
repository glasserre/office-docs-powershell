---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online
schema: 2.0.0
---

# Remove-PublicFolderClientPermission

## SYNOPSIS
This cmdlet is available in on-premises Exchange and in the cloud-based service. Some parameters and settings may be exclusive to one environment or the other.

Use the Remove-PublicFolderClientPermission cmdlet to remove permissions from public folders.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Remove-PublicFolderClientPermission [-Identity] <PublicFolderIdParameter> -AccessRights <MultiValuedProperty>
 -User <PublicFolderUserIdParameter> [-Confirm] [-DomainController <Fqdn>] [-Server <ServerIdParameter>]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Remove-PublicFolderClientPermission -Identity \"My Public Folder" -User Chris -AccessRights CreateItems -Server "My Server"
```

In Exchange Server 2010, this example removes permission for the user Chris to create items in the public folder My Public Folder on the server My Server.

### Example 1 -------------------------- (Exchange Server 2013)
```
Remove-PublicFolderClientPermission -Identity "\My Public Folder" -User Contoso\Chris
```

This example removes permission for the user Chris to the public folder My Public Folder.

### Example 1 -------------------------- (Exchange Server 2016)
```
Remove-PublicFolderClientPermission -Identity "\My Public Folder" -User Contoso\Chris
```

This example removes permission for the user Chris to the public folder My Public Folder.

### Example 1 -------------------------- (Exchange Online)
```
Remove-PublicFolderClientPermission -Identity "\My Public Folder" -User Contoso\Chris
```

This example removes permission for the user Chris to the public folder My Public Folder.

## PARAMETERS

### -AccessRights
The AccessRights parameter specifies the rights being removed. This parameter accepts the following values:

- ReadItems The user has the right to read items within the specified public folder.

- CreateItems The user has the right to create items within the specified public folder.

- EditOwnedItems The user has the right to edit the items that the user owns in the specified public folder.

- DeleteOwnedItems The user has the right to delete items that the user owns in the specified public folder.

- EditAllItems The user has the right to edit all items in the specified public folder.

- DeleteAllItems The user has the right to delete all items in the specified public folder.

- CreateSubfolders The user has the right to create subfolders in the specified public folder.

- FolderOwner The user is the owner of the specified public folder. The user has the right to view and move the public folder and create subfolders. The user can't read items, edit items, delete items, or create items.

- FolderContact The user is the contact for the specified public folder.

- FolderVisible The user can view the specified public folder, but can't read or edit items within the specified public folder.

In addition to the access rights, you can create rights based upon roles, which includes multiple access rights. This parameter accepts the following values for roles:

- NoneFolderVisible

- OwnerCreateItems, ReadItems, CreateSubfolders, FolderOwner, FolderContact, FolderVisible, EditOwnedItems, EditAllItems, DeleteOwnedItems, DeleteAllItems

- PublishingEditorCreateItems, ReadItems, CreateSubfolders, FolderVisible, EditOwnedItems, EditAllItems, DeleteOwnedItems, DeleteAllItems

- EditorCreateItems, ReadItems, FolderVisible, EditOwnedItems, EditAllItems, DeleteOwnedItems, DeleteAllItems

- PublishingAuthorCreateItems, ReadItems, CreateSubfolders, FolderVisible, EditOwnedItems, DeleteOwnedItems

- AuthorCreateItems, ReadItems, FolderVisible, EditOwnedItems, DeleteOwnedItems

- NonEditingAuthorCreateItems, ReadItems, FolderVisible

- ReviewerReadItems, FolderVisible

- ContributorCreateItems, FolderVisible

```yaml
Type: MultiValuedProperty
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Identity
The Identity parameter specifies the GUID or public folder name that represents a specific public folder. You can also include the path by using the format \\TopLevelPublicFolder\\PublicFolder.

You can omit the parameter label so that only the public folder name or GUID is supplied.

```yaml
Type: PublicFolderIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: True
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -User
The User parameter specifies the user principal name (UPN), domain\\user, or alias of the user whose permissions are being removed.

```yaml
Type: PublicFolderUserIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: -Confirm:$false.

- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
This parameter is available only in on-premises Exchange.

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
The Server parameter specifies the server on which to perform the selected operations.

```yaml
Type: ServerIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/cc35b182-d90d-4f0a-9e4c-cd97bd81b4f3.aspx)