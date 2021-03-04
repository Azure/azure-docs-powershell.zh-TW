---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: e85976b4d4b5de508e1a4f25338b21abdb0c097f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909789"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## 簡介
獲得批次工作準備和釋出工作狀態。

## 語法

### 識別碼 (預設) 
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzBatchJobPreparationAndReleaseTaskStatus** Cmdlet 會取得批次工作的 Azure Batch 工作準備和發行工作狀態。
您必須為此 *Cmdlet* 提供 Id 參數或 **PSCloudJob** 實例。

## 例子

### 範例 1：取得工作的準備工作和釋出狀態
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

此命令會針對工作「測試」獲得工作準備和釋出工作狀態。
使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。

### 範例 2：使用指定篩選和選取來取得工作的工作準備和發行狀態
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

此命令會獲得節點 "tvm-2316545714_1-20170613t201733z" 上的工作準備和發行工作狀態，並使用 Select 子句指定只傳回 JobPreparationTaskExecutionInformation 資訊

## 參數

### -BatchCoNtext
BatchAccountCoNtext 實例，用於與批次處理服務互動。
使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。

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

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -展開
指定 Open Data Protocol (OData) expand 子句。
指定此參數的值，以取得您取得之主實體的關聯實體。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -篩選
指定 OData 篩選子句。
如果您未指定篩選，此 Cmdlet 會針對該工作，會返回所有工作準備和釋出工作狀態。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
指定應取回準備和釋出工作的工作識別碼。
您無法指定萬用字元。

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

### -InputObject
指定 **PSCloudJob 物件** ，代表工作以取得準備和釋出工作狀態。
若要取得 **PSCloudJob 物件** ，請使用 Get-AzBatchJob Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
指定要退回的工作準備和釋出工作狀態數量上限。
如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。
預設值為 1000。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -選取
指定 OData select 子句。
指定此參數的值以取得特定屬性，而不是所有物件屬性。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Batch。Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext

## 輸出

### Microsoft.Azure.Commands.Batch。Models.PSJobPreparationAndReleaseTaskExecutionInformation

## 筆記

## 相關連結

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Azure Batch Cmdlet](/powershell/module/Az.Batch/)
