---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: ce2c4060d6471cc65c6b343e86c1e15b74ca5414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914206"
---
# Enable-AzDataCollection

## 簡介
讓 Azure PowerShell 收集資料以改善 Azure PowerShell Cmdlet 的使用者體驗。 執行此 Cmdlet 會加入宣告目前電腦上目前使用者的資料收集。 除非您明確退出宣告，否則預設會收集資料。

## 語法

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述

`Enable-AzDataCollection`Cmdlet 是用來加入宣告資料收集。 Azure PowerShell 預設會自動收集遙測資料。 Microsoft 會匯總收集的資料，以識別使用模式、識別常見問題，以及改善 Azure PowerShell 的體驗。
Microsoft Azure PowerShell 不會收集任何私人或個人資料。 若要停用資料收集，您必須執行明確退出宣告 `Disable-AzDataCollection` 。

## 例子

### 範例 1：為目前使用者啟用資料收集

下列範例顯示如何為目前使用者啟用資料收集。

```powershell
Enable-AzDataCollection
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

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
