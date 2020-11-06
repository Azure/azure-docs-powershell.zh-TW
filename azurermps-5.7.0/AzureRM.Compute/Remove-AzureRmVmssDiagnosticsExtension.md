---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448775"
---
# Remove-AzureRmVmssDiagnosticsExtension

## 摘要
從 VMSS 移除診斷延伸。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmVmssDiagnosticsExtension** Cmdlet 會從虛擬機器縮放集 (VMSS) 中移除診斷延伸。

## 示例

### 範例1：從 VMSS 移除診斷延伸
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

這個命令會從 VMSS 中移除診斷延伸。

## 參數

### -名稱
指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
指定要移除延伸的 VMSS。

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。

未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

[附加 AzureRmVmssDiagnosticsExtension](./Add-AzureRmVmssDiagnosticsExtension.md)

[移除-AzureRmVMDiagnosticsExtension](./Remove-AzureRmVMDiagnosticsExtension.md)

[移除-AzureRmVmssExtension](./Remove-AzureRmVmssExtension.md)


