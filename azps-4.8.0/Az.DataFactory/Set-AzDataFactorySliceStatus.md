---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127095"
---
# Set-AzDataFactorySliceStatus

## 摘要
在 Azure 資料工廠中設定資料集的扇面狀態。

## 句法

### ByFactoryName (預設) 
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzDataFactorySliceStatus** Cmdlet 會設定 Azure 資料工廠中資料集的扇面狀態。

## 示例

### 範例1：設定所有扇面的狀態
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

這個命令會將名為 DAWikiAggregatedData 的資料集的所有磁區狀態設定為在名為 WikiADF 的資料工廠中等待。
*UpdateType* 參數的值為 UpstreamInPipeline，因此命令會針對資料集和所有相依資料集設定每個扇面的狀態。
相依資料集是在管線中作為活動的輸入資料集使用。
這個命令會傳回 $True 的值。

## 參數

### -DataFactory
指定 **PSDataFactory** 物件。
這個 Cmdlet 會修改屬於此參數指定之資料工廠的扇面狀態。

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
指定資料工廠的名稱。
這個 Cmdlet 會修改屬於此參數指定之資料工廠的扇面狀態。

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatasetName
指定此 Cmdlet 要修改其扇面的資料集名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -EndDateTime
將時段的結尾指定為 **DateTime** 物件。
此時間是資料切片的結尾。
如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。
*EndDateTime* 必須在 ISO8601 格式中指定，如下列範例所示： 2015-01-01Z 2015-01-01T00 .. 00： 00Z 2015-01-01T00：00： 00.000 z (UTC) 2015-01-01T00：00：00： 00 (太平洋標準時間) 預設的時區指示符是 UTC。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資源群組的名稱。
這個 Cmdlet 會修改屬於此參數指定之群組的扇面狀態。

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDateTime
指定時段的開頭作為 **DateTime** 物件。
此時間是資料切片的開頭。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -狀態
指定要指派給資料切片的狀態。
此參數可接受的值為：
- 等待.
資料切片正在等待驗證原則，然後再進行處理。 
- 即可.
資料處理已完成，且資料切片已準備就緒。
- 正在.
正在進行資料處理。 
- 成功.
資料處理失敗。
- 略過.
已跳過處理資料切片的過程。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateType
指定切片的更新類型。
此參數可接受的值為：
- 某.
針對指定的時間範圍，設定資料集每個扇面的狀態。 
- UpstreamInPipeline.
針對資料集和所有相依資料集設定每個磁區的狀態，這些資料集會作為管線中活動的輸入資料集使用。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.object

## 輸出

### System.object

## 筆記
* 關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠

## 相關連結

[AzDataFactorySlice](./Get-AzDataFactorySlice.md)


