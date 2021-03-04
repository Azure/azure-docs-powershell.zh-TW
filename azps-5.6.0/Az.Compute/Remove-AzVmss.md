---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: 2ed7be0cf790a596a2a2fc9b23c0e6aa50f67623
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914162"
---
# Remove-AzVmss

## 簡介
移除 VMSS 或 VMSS 內的虛擬機器。

## 語法

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Remove-Az Vms Cmdlet** 會從 Azure 移除 (VMSS) 設定。
此 Cmdlet 也可以用來移除 VMSS 內的特定虛擬機器。
您可以使用 *InstanceId* 參數來移除 VMSS 內的特定虛擬機器。

## 例子

### 範例 1：移除 VMSS
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

此命令會移除名為 VMScaleSet001 的 VMSS，該 VMSS 屬於名為 Group001 的資源群組。

### 範例 2：從 VMSS 內移除虛擬機器
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

此命令會從名稱為 VMScaleSet002 的 VMSS 名稱為 VMScaleSet002 的虛擬機器移除實例識別碼為 3 的虛擬機器，該虛擬機器屬於名為 Group002 的資源群組。

## 參數

### -AsJob
在背景中執行 Cmdlet 並返回工作以追蹤進度。

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

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -強制
強制執行命令，但不要求使用者確認。

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

### -InstanceId
指定需要啟動的實例識別碼，做為字串陣列。
例如： `-InstanceId "0", "3"`

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定 VMSS 所屬的資源組名。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
此 Cmdlet 移除的 VMSS 名稱。
如果您指定 *InstanceId* 參數，Cmdlet 會從此參數命名的 VMSS 移除指定的虛擬機器。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
顯示 Cmdlet 執行時會發生什麼情況。 不會執行 Cmdlet。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### System.String[]

## 輸出

### Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse

## 筆記

## 相關連結

[Get-AzEvss](./Get-AzVmss.md)

[New-AzEvss](./New-AzVmss.md)

[Restart-AzEvss](./Restart-AzVmss.md)

[Set-AzEvss](./Set-AzVmss.md)

[Start-AzEvss](./Start-AzVmss.md)

[Stop-AzEvss](./Stop-AzVmss.md)

[Update-AzEvss](./Update-AzVmss.md)


