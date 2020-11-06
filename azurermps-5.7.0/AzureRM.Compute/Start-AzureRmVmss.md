---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 4c1bc282b4a5aa0bf8c324ec523b5c823ce3cd14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449918"
---
# Start-AzureRmVmss

## 摘要
在 VMSS 中啟動 VMSS 或一組虛擬機器。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmVmss** Cmdlet 會啟動虛擬機器縮放集 (VMSS) 或一組虛擬機器中的所有虛擬機器。
您可以使用 *InstanceId* 參數來選取一組虛擬機器。

## 示例

### 範例1：在 VMSS 中啟動一組特定的虛擬機器
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

這個命令會啟動由屬於名為 ContosoVMSS 之 VMSS 的實例識別碼字串陣列所指定的一組特定虛擬機器。

### 範例2：啟動 VMSS 中的所有虛擬機器
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

這個命令會啟動屬於名為 ContosoVMSS 之 VMSS 的所有虛擬機器。

## 參數

### -InstanceId
指定為字串陣列，即 Cmdlet 啟動之實例的識別碼或 Id。
例如： `-InstanceId "0", "3"`

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定 VMSS 之資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
指定此 Cmdlet 啟動虛擬機器的 VMSS 名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

###  
這個 Cmdlet 不會產生任何輸出。

## 筆記

## 相關連結

[AzureRmVmss](./Get-AzureRmVmss.md)

[新-AzureRmVmss](./New-AzureRmVmss.md)

[移除-AzureRmVmss](./Remove-AzureRmVmss.md)

[重新開機-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[停止 AzureRmVmss](./Stop-AzureRmVmss.md)

[更新-AzureRmVmss](./Update-AzureRmVmss.md)


