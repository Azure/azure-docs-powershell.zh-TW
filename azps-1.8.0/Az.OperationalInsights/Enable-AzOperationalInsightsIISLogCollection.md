---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 75b037903adf52b1ba1407ff40e2bfbb610a6dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621312"
---
# Enable-AzOperationalInsightsIISLogCollection

## 摘要
從工作區中的電腦開始收集 IIS 記錄。

## 句法

### ByWorkspaceName (預設) 
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByWorkspaceObject
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**Enable-AzOperationalInsightsIISLogCollection** Cmdlet 會開始收集網際網路資訊服務 (IIS) 記錄從工作區中的連線電腦。

## 示例

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -ResourceGroupName
指定包含電腦之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -工作區
指定這個 Cmdlet 在其中運作的工作區。

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
指定此 Cmdlet 作用中的工作區名稱。

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSWorkspace 中的 OperationalInsights。

### System.object

## 輸出

### Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource

## 筆記

## 相關連結

[Disable-AzOperationalInsightsIISLogCollection](./Disable-AzOperationalInsightsIISLogCollection.md)


