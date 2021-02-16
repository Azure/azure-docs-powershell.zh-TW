---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136743"
---
# Disable-AzDataCollection

## 摘要
在收集資料時，無法改善 Azure PowerShell Cmdlet。 預設會收集資料，除非您明確退出宣告。

## 句法

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明

這個 `Disable-AzDataCollection` Cmdlet 是用來退出宣告資料收集。 Azure PowerShell 預設會自動收集遙測資料。 若要停用資料收集，您必須明確退出宣告。Microsoft 會匯總收集的資料以識別使用方式、找出常見問題，以及改善 Azure PowerShell 的體驗。 Microsoft Azure PowerShell 不會收集任何私人或個人資料。 如果您先前已退出宣告，請執行 `Enable-AzDataCollection` Cmdlet，在目前的電腦上重新啟用目前使用者的資料收集。

## 示例

### 範例1：停用目前使用者的資料收集

下列範例顯示如何停用目前使用者的資料收集。

```powershell
Disable-AzDataCollection
```

## 參數

### -DefaultProfile

用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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

這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)。

## 輸入

### 所有

## 輸出

### System.void

## 筆記

## 相關連結

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
