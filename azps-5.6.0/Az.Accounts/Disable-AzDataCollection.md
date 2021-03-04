---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 54af80b230c3cb031e8927a82ec3536cc1a81ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914218"
---
# Disable-AzDataCollection

## 簡介
選擇不收集資料以改善 Azure PowerShell Cmdlet。 除非您明確退出宣告，否則預設會收集資料。

## 語法

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述

`Disable-AzDataCollection`Cmdlet 是用來退出宣告資料收集。 Azure PowerShell 預設會自動收集遙測資料。 若要停用資料收集，您必須明確退出宣告。Microsoft 會匯總收集的資料，以識別使用模式、識別常見問題，以及改善 Azure PowerShell 的體驗。 Microsoft Azure PowerShell 不會收集任何私人或個人資料。 如果您先前已退出宣告，請執行 Cmdlet，以重新啟用目前電腦上目前 `Enable-AzDataCollection` 使用者的資料收集。

## 例子

### 範例 1：停用目前使用者的資料收集

下列範例顯示如何停用目前使用者的資料收集。

```powershell
Disable-AzDataCollection
```

## 參數

### -DefaultProfile

用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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

### 沒有

## 輸出

### System.Void

## 筆記

## 相關連結

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
