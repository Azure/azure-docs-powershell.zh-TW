---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 8bca1314433f8fcbcc0c9f395783bbb3d9835ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914210"
---
# Enable-AzContextAutosave

## 簡介
Azure 上下文是代表您作用中訂閱以執行命令的 PowerShell 物件，以及連接至 Azure 雲端所需的驗證資訊。 使用 Azure 上下文時，Azure PowerShell 不需要每次切換訂閱時重新驗證您的帳戶。 詳細資訊請參閱 Azure [PowerShell 上下文物件](https://docs.microsoft.com/powershell/azure/context-persistence)。

此 Cmdlet 可讓您在啟動 PowerShell 程式時儲存並自動載入 Azure 上下文資訊。 例如，開啟新視窗時。

## 語法

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述

允許儲存 Azure 上下文資訊，並自動載入 PowerShell 程式啟動時。 上下文會儲存于影響上下文的任何 Cmdlet 執行結束時。 例如，任何設定檔 Cmdlet。 如果您使用的是使用者驗證，則權杖可以在執行任何 Cmdlet 的過程中更新。

## 例子

### 範例 1：為目前使用者啟用自動儲存認證

開啟目前使用者的認證自動儲存。 每當您開啟 PowerShell 視窗時，系統就會記住您目前的情況，而不會登陸。

```powershell
Enable-AzContextAutosave
```

### 範例 2

當您在此 PowerShell 會話中開啟 PowerShell 視窗時，允許儲存並自動載入 Azure 認證、帳戶和訂閱資訊。  (自動) 

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## 參數

### -DefaultProfile

用於與 Azure 通訊的認證、租使用者和訂閱

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

### -範圍

決定上下文變更的範圍。 例如，變更是否僅適用于目前的程式，或此使用者啟動的所有會話。 使用範圍進行變更會影響使用者啟動的所有 `CurrentUser` PowerShell 會話。 如果特定會話需要有不同的設定，請使用範圍 `Process` 。

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Common.Authentication.CoNtextAutosaveSettings

## 筆記

## 相關連結
