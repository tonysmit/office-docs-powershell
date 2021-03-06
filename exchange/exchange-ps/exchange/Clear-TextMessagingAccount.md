---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online
schema: 2.0.0
---

# Clear-TextMessagingAccount

## SYNOPSIS
!!! Exchange Server 2010

Use the Clear-TextMessagingAccount cmdlet to remove the text messaging settings from a user's account.

!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

This cmdlet is available in on-premises Exchange and in the cloud-based service. Some parameters and settings may be exclusive to one environment or the other.

The Clear-TextMessagingAccount cmdlet allows a user to remove the text messaging settings from their own mailbox. An administrator can't use this cmdlet to remove the text messaging settings from another user's mailbox.

## SYNTAX

```
Clear-TextMessagingAccount [-Identity] <MailboxIdParameter> [-Confirm] [-DomainController <Fqdn>]
 [-IgnoreDefaultScope] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2010

The Clear-TextMessagingAccount cmdlet clears all of a user's text messaging settings, including communication and notification settings.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Text messaging settings" entry in the Client Access Permissions topic.

!!! Exchange Server 2013

The Clear-TextMessagingAccount cmdlet clears all of a user's text messaging settings, including communication and notification settings.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Text messaging user settings" entry in the Clients and mobile devices permissions topic.

!!! Exchange Server 2016, Exchange Online

The Clear-TextMessagingAccount cmdlet clears all of a user's text messaging settings, including communication and notification settings.

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Clear-TextMessagingAccount -Identity "TonySmith"
```

This example clears the text messaging account settings and notification settings from Tony Smith's mailbox.

### Example 1 -------------------------- (Exchange Server 2013)
```
Clear-TextMessagingAccount -Identity "TonySmith"
```

This example clears the text messaging account settings and notification settings from Tony Smith's mailbox.

### Example 1 -------------------------- (Exchange Server 2016)
```
Clear-TextMessagingAccount -Identity tony@contoso.com
```

This example clears the text messaging account settings and notification settings from Tony's mailbox.

### Example 1 -------------------------- (Exchange Online)
```
Clear-TextMessagingAccount -Identity tony@contoso.com
```

This example clears the text messaging account settings and notification settings from Tony's mailbox.

### Example 2 -------------------------- (Exchange Server 2010)
```
Clear-TextMessagingAccount -Identity "Contoso\TonySmith" -Confirm $true
```

This example clears the text messaging account settings and notification settings from Tony Smith's mailbox and displays a confirmation message.

### Example 2 -------------------------- (Exchange Server 2013)
```
Clear-TextMessagingAccount -Identity "Contoso\TonySmith" -Confirm $true
```

This example clears the text messaging account settings and notification settings from Tony Smith's mailbox and displays a confirmation message.

### Example 3 -------------------------- (Exchange Server 2010)
```
Clear-TextMessagingAccount -Identity "tony@contoso.com"
```

This example clears the text messaging account settings and notification settings from Tony Smith's mailbox.

### Example 3 -------------------------- (Exchange Server 2013)
```
Clear-TextMessagingAccount -Identity "tony@contoso.com"
```

This example clears the text messaging account settings and notification settings from Tony Smith's mailbox.

## PARAMETERS

### -Identity
!!! Exchange Server 2010, Exchange Server 2013

The Identity parameter specifies the target mailbox. You can use one of the following values:

- CommonName

- DisplayName

- FirstName

- LastName

- Alias



!!! Exchange Server 2016, Exchange Online

The Identity parameter specifies the target mailbox. You can any value that uniquely identifies the mailbox.

For example:

- Name

- Display name

- Alias

- Distinguished name (DN)

- Canonical DN

- \<domain name\>\\\<account name\>

- Email address

- GUID

- LegacyExchangeDN

- SamAccountName

- User ID or user principal name (UPN)



```yaml
Type: MailboxIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: True
Position: 1
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
!!! Exchange Server 2010

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

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

### -IgnoreDefaultScope
!!! Exchange Server 2010, Exchange Server 2013

The IgnoreDefaultScope parameter instructs the command to ignore the default recipient scope setting for the Exchange Management Shell session and use the entire forest as the scope. This allows the command to access Active Directory objects that aren't currently in the default scope. Using the IgnoreDefaultScope parameter introduces the following restrictions:

- You can't use the DomainController parameter. The command uses an appropriate global catalog server automatically.



!!! Exchange Server 2016, Exchange Online

The IgnoreDefaultScope switch tells the command to ignore the default recipient scope setting for the Exchange Management Shell session, and to use the entire forest as the scope. This allows the command to access Active Directory objects that aren't currently available in the default scope.

Using the IgnoreDefaultScope switch introduces the following restrictions:

- You can't use the DomainController parameter. The command uses an appropriate global catalog server automatically.

- You can only use the DN for the Identity parameter. Other forms of identification, such as alias or GUID, aren't accepted.



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

[Online Version](https://technet.microsoft.com/library/ebc17689-0c30-4d0b-9a53-d81a909458d3.aspx)

