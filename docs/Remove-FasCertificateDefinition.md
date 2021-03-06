# Remove-FasCertificateDefinition

## Synopsis
Delete a Certificate Definition Object.

## Syntax

```
Remove-FasCertificateDefinition -Name <String> [-Address <String>] [-UserName <String>] [-Password <String>]
 [<CommonParameters>]
```

## Description
Delete a Certificate Definition Object. 
The FAS server will no longer be able to issue certificates of this type.

Note that Certificate Definition objects can only be created and managed by the FAS Server administrator, although they can be referenced by "Rule" administrators.

## Examples

### Example 1
PS C:\\\>

```
C:\PS> $CitrixFasAddress=(Get-FasServer)[0].Address
C:\PS> Remove-FasCertificateDefinition -Name (Get-FasCertificateDefinition)[0].Name
```

Description

-----------

Lists the Certificate Definition objects configured on the FAS Server, and deletes the first one.

## Parameters

### -Name
Specify the name of the Certificate Definition to delete.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (required)
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Address
Address of FAS Server (or $NULL to use $CitrixFasAddress)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $CitrixFasAddress
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserName
User name to use for authentication to FAS server ($NULL for current user account)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $NULL
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Password
Password for authentication to FAS server ($NULL for current user account)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $NULL
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Inputs

### Variable, based on property name.
This cmdlet does accept input from the pipeline but only by property name.

## Outputs

### void
This cmdlet does not return a value

## Notes

## Related Links

[New-FasCertificateDefinition]()

[Set-FasCertificateDefinition]()

[Remove-FasCertificateDefinition]()


