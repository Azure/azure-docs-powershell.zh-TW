---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450016"
---
# Set-AzureBatchComputeNodeUser

## 摘要
在批次計算節點上修改帳戶的屬性。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureBatchComputeNodeUser** Cmdlet 會修改 Azure Batch 計算節點上使用者帳戶的屬性。

## 示例

### 範例1：更新使用者帳戶
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

這個命令會修改在名為 ContosoPool 的 pool 中擁有指定 ID 的 compute 節點上名為 PFuller 的使用者帳戶。
此命令會變更帳戶密碼及到期時間。

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

### -ComputeNodeId
指定此 Cmdlet 在其上執行的計算節點的識別碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
指定使用者帳戶的到期時間。

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

### -名稱
指定此 Cmdlet 修改的使用者帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
指定使用者帳戶的密碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
指定包含此 Cmdlet 操作之計算節點之池的 ID。

```yaml
Type: System.String
Parameter Sets: (All)
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

## 輸出

## 筆記

## 相關連結

[AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[新-AzureBatchComputeNodeUser](./New-AzureBatchComputeNodeUser.md)

[移除-AzureBatchComputeNodeUser](./Remove-AzureBatchComputeNodeUser.md)

[Azure 批次 Cmdlet](./AzureRM.Batch.md)


