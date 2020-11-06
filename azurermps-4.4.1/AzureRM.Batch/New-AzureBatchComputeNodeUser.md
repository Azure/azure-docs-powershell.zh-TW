---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450033"
---
# New-AzureBatchComputeNodeUser

## 摘要
在批次計算節點上建立使用者帳戶。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 標識號
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的 AzureBatchComputeNodeUser** Cmdlet 會在 Azure Batch 計算節點上建立使用者帳戶。

## 示例

### 範例1：建立擁有管理認證的使用者帳戶
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

這個命令會在具有識別碼 ComputeNode01 的 [計算] 節點上建立使用者帳戶。
節點位於 ID 為 MyPool01 的池中。
使用者名稱為 TestUser、密碼為 Password、帳戶在七天后到期，且帳戶具有管理認證。

### 範例2：使用管線在計算節點上建立使用者帳戶
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

這個命令會使用 **AzureBatchComputeNode** Cmdlet 取得名為 ComputeNode01 的計算節點。
該節點位於 ID 為 MyPool01 的池中。
命令會使用管線運算子，將該計算節點傳到目前的 Cmdlet。
此命令會建立一個使用者帳戶，並將使用者名稱 TestUserand 密碼密碼。

## 參數

### -BatchCoNtext
指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。
若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
將此 Cmdlet 建立使用者帳戶的計算節點指定為 **PSComputeNode** 物件。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
指定此 Cmdlet 建立使用者帳戶的計算節點識別碼。

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
指定新使用者帳戶的到期時間。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsAdmin
表示 Cmdlet 會建立擁有管理認證的使用者帳戶。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定新的本機 Windows 帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
指定使用者帳戶密碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
指定包含要在其上建立使用者帳戶之計算節點的 pool 的 ID。

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### BatchAccountCoNtext
形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值

### PSComputeNode
形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[AzureBatchComputeNode](./Get-AzureBatchComputeNode.md)

[移除-AzureBatchComputeNodeUser](./Remove-AzureBatchComputeNodeUser.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)


