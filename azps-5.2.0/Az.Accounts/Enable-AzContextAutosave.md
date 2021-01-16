---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284548"
---
# Enable-AzContextAutosave

## 摘要
Azure 內容是代表您的作用中訂閱執行命令的 PowerShell 物件，以及連線至 Azure 雲端所需的驗證資訊。 如果是 Azure 內容，則在您每次切換訂閱時，Azure PowerShell 不需要重新驗證您的帳戶。 如需詳細資訊，請參閱 [Azure PowerShell 內容物件](https://docs.microsoft.com/powershell/azure/context-persistence)。

這個 Cmdlet 可讓 Azure 內容資訊在您啟動 PowerShell 進程時儲存並自動載入。 例如，開啟新視窗時。

## 句法

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明

允許在 PowerShell 程式啟動時，儲存 Azure 內容資訊並自動載入。 內容會在執行任何影響內容的 Cmdlet 結束時儲存。 例如，任何設定檔 Cmdlet。 如果您使用的是使用者驗證，則可以在執行任何 Cmdlet 期間更新權杖。

## 示例

### 範例1：為目前的使用者啟用 autosaving 認證

針對目前的使用者開啟認證自動儲存。 每當開啟 PowerShell 視窗時，就會記住您目前的內容，而不需要登入。

```powershell
Enable-AzContextAutosave
```

### 範例2

當您在這個 PowerShell 會話中開啟 PowerShell 視窗時，允許儲存及自動載入 Azure 認證、帳戶及訂閱資訊。  (自動生成) 

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## 參數

### -DefaultProfile

用於與 Azure 進行通訊的認證、租使用者及訂閱

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

決定內容變更的範圍。 例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。 對範圍所做的變更 `CurrentUser` 會影響使用者開始的所有 PowerShell 會話。 如果特定會話需要有不同的設定，請使用範圍 `Process` 。

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

在執行 Cmdlet 之前提示您進行確認。

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

顯示在執行 Cmdlet 時會發生什麼情況。
無法執行 Cmdlet。

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

### 一般參數

這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### CoNtextAutosaveSettings 的常見驗證。

## 筆記

## 相關連結
