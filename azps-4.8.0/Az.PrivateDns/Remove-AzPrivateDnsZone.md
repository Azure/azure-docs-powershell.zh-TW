---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126955"
---
# Remove-AzPrivateDnsZone

## 摘要
從資源群組中移除私人 DNS 區域。

## 句法

### 預設)  (的欄位
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 面向
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
AzPrivateDnsZone Cmdlet 會從指定 **的** 資源群組中永久刪除私人網功能變數名稱稱系統 (DNS) 區域。
該區域中包含的所有記錄集也都會刪除。
您可以使用 *PrivateZone* 參數或使用管線運算子來傳遞 **PrivateDnsZone** 物件，或者也可以指定 *Name* 和 *ResourceGroupName* 參數。
您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。
使用 **PrivateDnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **PrivateDnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。
這可為併發區域變更提供保護。
這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。

## 示例

### 範例1：移除私人區域
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

這個命令會從名為 MyResourceGroup 的資源群組中移除名為 myzone.com 的區域。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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
指定此 Cmdlet 移除之專用 DNS 區域的名稱。
您也必須指定 *ResourceGroupName* 參數。
或者，您也可以使用 *zone* 參數指定 DNS 區域。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
使用 **PrivateDnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **PrivateDnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。
這可為併發區域變更提供保護。
這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。

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
用來傳送操作的結果 (布林) ，以從管線中移除私有區域。

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

### -PrivateZone
要刪除的私人區域物件。

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含要移除之區域的資源群組的名稱。
您也必須指定 *ZoneName* 參數。
或者，您也可以使用 **PrivateDnsZone** 物件來指定 DNS 區域，方法是透過管線或 *zone* 參數傳遞。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
私人 DNS 區域 ResourceID。

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSPrivateDnsZone 中的 PrivateDns。

### System.object

## 輸出

### System.object

## 筆記

## 相關連結

[AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[新-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
