---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: ada6b5050a2a08af89720aa3afeaf1dcd876768a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449570"
---
# Disable-AzureRmDataCollection

## 摘要
在收集資料時，無法改善 AzurePowerShell Cmdlet。 除非您明確加入宣告，否則不會收集資料。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
您可以透過加入宣告資料收集來改善使用 Microsoft 雲端和 Azure PowerShell 的體驗。
Azure PowerShell 不會在未經您同意的情況下收集資料，您必須在第一次執行 Cmdlet 時，在 Azure PowerShell 提示您 AzureRmDataCollection 收集資料時，再回答 [是]。
Microsoft 匯總收集的資料，以識別使用方式、找出常見問題，以及改善使用 Azure PowerShell 的體驗。
Microsoft Azure PowerShell 不會收集任何私人資料，或任何個人的可識別資訊。

執行 Disable-AzureRMDataCollection Cmdlet 來停用目前使用者的資料收集。
這可防止目前的使用者在第一次執行 Cmdlet 時收到關於資料收集的提示。

若要為目前的使用者啟用資料收集，請執行 Enable-AzureRmDataCollection Cmdlet。

## 示例

### 範例1：停用目前使用者的資料收集
```
PS C:\> Disable-AzureRmDataCollection
```

這個範例示範如何停用目前使用者的資料收集。 

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### 所有

## 筆記

## 相關連結

[Enable-AzureRmDataCollection](./Enable-AzureRmDataCollection.md)

