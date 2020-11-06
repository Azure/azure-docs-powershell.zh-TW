---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
ms.openlocfilehash: 4ebdb51fdc6129f0e980282b6588324505e62bcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452443"
---
# Send-Feedback

## 摘要
透過一組引導提示，將意見反應傳送給 Azure PowerShell 小組。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
Send-Feedback Cmdlet 會將意見反應傳送給 Azure PowerShell 小組。

## 示例

### 範例1：
```
PS C:\> Send-Feedback

With zero (0) being the least and ten (10) being the most, how likely are you to recommend Azure PowerShell to a friend or colleague?

10

What does Azure PowerShell do well?

Response.

Upon what could Azure PowerShell improve?

Response.

Please enter your email if you are interested in providing follow up information:

your@email.com
```

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### System.void

## 筆記

## 相關連結

