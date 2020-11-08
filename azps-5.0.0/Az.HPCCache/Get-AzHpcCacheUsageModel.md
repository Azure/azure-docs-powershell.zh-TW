---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 4552de7be0f2a489aa152a922e39df623736f842
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139259"
---
# Get-AzHpcCacheUsageModel

## 摘要
取得 NFS 儲存目標的所有 usageModels。

## 句法

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzHpcCacheUsageModel** Cmdlet 會傳回 NFS 儲存目標的使用模式清單。

## 示例

### 範例1
```powershell
PS C:\> Get-AzHpcCacheUsageModel
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### PSHpcUsageModels （HPCCache）的

### System.object
## 筆記

## 相關連結
