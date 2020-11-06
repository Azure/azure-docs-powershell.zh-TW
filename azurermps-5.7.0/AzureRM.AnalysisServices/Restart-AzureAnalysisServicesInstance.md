---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 0a89ee592e6f6f6d4d9e56df6d7e4df32b010524
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449426"
---
# Restart-AzureAnalysisServicesInstance

## 摘要
在目前登入的環境中重新開機 Analysis Services 伺服器的實例，如 Add-AzureAnalysisServicesAccount 命令中所指定

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
```

## 說明
Restart-AzureAnalysisServicesInstance Cmdlet 會重新開機 Azure Analysis Services 伺服器的實例

## 示例

### 範例1
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

這個命令會在 Add-AzureAnalysisServicesAccount 命令中指定的環境中，重新開機伺服器「testserver」

## 參數

### -實例
要重新開機之 Analysis Services 伺服器實例的名稱

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
如果命令成功，則指定此值會傳回 true。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### System.object

## 筆記
別名： Restart-AzureAsInstance

## 相關連結

