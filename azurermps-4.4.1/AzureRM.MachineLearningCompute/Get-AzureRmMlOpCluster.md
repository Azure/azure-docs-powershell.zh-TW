---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452483"
---
# Get-AzureRmMlOpCluster

## 摘要
取得 operationalization 群集物件。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
依名稱、資源群組或訂閱來取得 operationalization 群集物件。

## 示例

### 範例1
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

依名稱取得特定的 operationalization 群集。

### 範例2
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

取得資源群組中的所有 operationalization 群集。

### 範例3
```
PS C:\> Get-AzureRmMlOpCluster
```

取得訂閱中的所有 operationalization 群集。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
Operationalization 群集的名稱。

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Operationalization 群集之資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSOperationalizationCluster 中的 MachineLearningCompute。

### [System.object]。清單 ' 1 [MachineLearningCompute. PSOperationalizationCluster，MachineLearningCompute，版本 = 0.1.0.0，Culture = 中性，PublicKeyToken = null]]。）））

## 筆記

## 相關連結

