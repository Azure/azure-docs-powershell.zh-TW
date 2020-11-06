---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453428"
---
# Get-AzureRmMlOpClusterKey

## 摘要
取得與 operationalization 群集相關聯的便捷鍵。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 從 Cmdlet 輸入參數取得 operationalization 群集的金鑰。
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### 從 OperationalizationCluster 實例定義取得 operationalization 群集的金鑰。
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### 從 Azure 資源識別碼取得 operationalization 群集的金鑰。
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## 說明
取得群集屬性時，並不會傳回與 operationalization 群集相關聯的儲存空間帳戶、容器註冊表及其他服務的按鍵。 必須進行特定的呼叫來取得金鑰，因為它們是機密資訊。

## 示例

### 範例1
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

傳回與 operationalization 群集相關聯之服務的機密金鑰。

## 參數

### -InputObject
Operationalization 群集物件。

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
Operationalization 群集的名稱。

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Operationalization 群集之資源群組的名稱。

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Operationalization 群集的 Azure 資源 id。

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## 輸入

### PSOperationalizationCluster 中的 MachineLearningCompute。
System.object


## 輸出

### PSOperationalizationClusterCredentials 中的 MachineLearningCompute。


## 筆記

## 相關連結

