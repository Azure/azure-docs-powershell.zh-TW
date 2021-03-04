---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 8c1058345d78289a7601fa390e202e428554b50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910122"
---
# Remove-AzDnsZone

## 簡介
從資源群組移除 DNS 區域。

## 語法

### 領域
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 物件
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 描述
**Remove-AzDnsZone** Cmdlet 會永久刪除指定資源 (DNS) 區域中的網域名稱系統。
區域中包含的所有記錄集也會一併刪除。
您可以使用 Name 參數或管道運算子傳遞 **DnsZone** 物件，或者您也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。
您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。
使用透過管線或區域參數) 傳遞 **的 Dns Zone** 物件 (來指定區域時，如果區域在 Azure DNS 中已經變更，則區域不會刪除，因為已取回本地 **Dns Zone** 物件 (只有直接在 DNS 區域資源計數上執行作業做為變更，區域中的記錄集作業不會) 。
這可保護同時區域變更。
您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除該區域。

## 例子

### 範例 1：移除區域
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

此命令會從名為 MyResourceGroup myzone.com資源群組移除名為 myResourceGroup 的區域。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 移除的 DNS 區功能變數名稱稱。
您也必須指定 *ResourceGroupName* 參數。
或者，您可以使用 Zone 參數指定 DNS *區域。*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -覆寫
使用透過管線或區域參數) 傳遞 **的 Dns Zone** 物件 (來指定區域時，如果區域在 Azure DNS 中已經變更，則區域不會刪除，因為已取回本地 **Dns Zone** 物件 (只有直接在 DNS 區域資源計數上執行作業做為變更，區域中的記錄集作業不會) 。
這可保護同時區域變更。
您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除該區域。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Passthru

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含要移除之區域的資源組名。
您也必須指定 *ZoneName* 參數。
或者，您可以使用透過管線或區域參數傳遞的 **Dns Zone** 物件來指定 *DNS* 區域。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -區域
指定要刪除的 DNS 區域。
傳遞 **的 DnsZone** 物件也可以透過管線傳遞。
或者，您可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定要刪除的 DNS 區域。

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

### Microsoft.Azure.Commands.dns.DnsZone

## 輸出

### System.Boolean

## 筆記
由於刪除 DNS 區域的潛在嚴重影響，此 Cmdlet 預設會提示確認 $ConfirmPreference Windows PowerShell 變數有 None 外的任何值。
如果您 *指定確認或* 確認 *：$True，* 此 Cmdlet 會先提示您確認再執行。
如果您指定 *確認：$False，Cmdlet* 不會提示您確認。 

## 相關連結

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
