---
applicable: Exchange Server 2013, Exchange Server 2016
schema: 2.0.0
---

# Get-SettingOverride

## SYNOPSIS
This cmdlet is available only in on-premises Exchange.

Use the Get-SettingOverride cmdlet to view existing setting overrides that store Exchange 2016 customizations in Active Directory instead of in text files on the server.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Get-SettingOverride [[-Identity] <SettingOverrideIdParameter>] [-DomainController <Fqdn>] [<CommonParameters>]
```

## DESCRIPTION
You use setting overrides to configure and store Exchange 2016 server customizations in Active Directory. In previous versions of Exchange, these customizations were stored in web.config or exe.config XML application configuration files. The customizations in these files were lost when you installed the next Exchange Cumulative Update (CU) or Service Pack (SP). The customizations that are associated with the \*-SettingOverride cmdlets persist in Active Directory across Exchange 2016 CUs and SPs.

Incorrect usage of the \*-SettingOverride cmdlets can cause serious damage to your Exchange organization. This damage could require you to reinstall Exchange. Only use these cmdlets as instructed by product documentation or under the direction of Microsoft Customer Service and Support.

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1
```
Get-SettingOverride | Format-List Name,Reason,ComponentName,SectionName,Parameters,Server
```

This example displays a summary list of all setting override objects.

### Example 2
```
Get-SettingOverride -Identity "IM Server Integration"
```

This example displays a detailed information for the setting override object named IM Server Integration.

## PARAMETERS

### -DomainController
The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
The Identity parameter specifies the setting override that you want to view. You can use any value that uniquely identifies the override. For example:

- Name

- Distinguished name (DN)

- GUID

```yaml
Type: SettingOverrideIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016

Required: False
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?linkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?linkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/3052da37-a77c-423b-a4ce-3022a6dbf19e.aspx)
