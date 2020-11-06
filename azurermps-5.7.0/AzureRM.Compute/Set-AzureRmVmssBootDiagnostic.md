---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: 868bf95ca2f54105143f122665ffa89732ada167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449928"
---
# Set-AzureRmVmssBootDiagnostic

## 摘要
設定虛擬機器縮放設定啟動診斷設定檔。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
設定虛擬機器縮放設定啟動診斷設定檔。

## 示例

### 範例1：設定 VMSS 的啟動診斷配置檔案屬性
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

這個命令會為名為 ContosoVMSS 的 VMSS 設定啟動診斷配置檔案屬性。

## 參數

### -啟用
是否應該在虛擬機器規模集上啟用引導診斷程式。

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
要用來放置主控台輸出和螢幕擷取畫面的儲存空間帳戶 URI。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
指定 VMSS 物件。
您可以使用 New-AzureRmVmssConfig Cmdlet 來建立物件。

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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### VirtualMachineScaleSet 中的 [Azure. 管理]
系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = b77a5c561934e089]] System. 字串

## 輸出

### VirtualMachineScaleSet 中的 [Azure. 管理]

## 筆記

## 相關連結

