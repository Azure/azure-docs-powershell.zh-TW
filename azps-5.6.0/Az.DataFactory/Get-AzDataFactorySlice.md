---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: 497899400c05697fb9b273a89743172b672e4892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907750"
---
# Get-AzDataFactorySlice

## 簡介
在 Azure Data Factory 中為資料集獲取資料區。

## 語法

### ByFactoryName (預設) 
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzDataFactorySlice** Cmdlet 會取得 Azure Data Factory 中資料集的資料區。
指定開始時間和結束時間，以定義要查看的資料區範圍。
資料區的狀態為下列其中一個值： 
- PendingExecution。
尚未開始進行資料管理。 
- InProgress.
正在處理資料。 
- 準備。
資料處理已完成。
資料區已準備好供從屬區塊使用。 
- 失敗。
產生該區塊的執行失敗。 
- 跳。
Data Factory 會略過處理該區塊。 
- 重試。
Data Factory 會重試產生該區塊的執行。 
- 已達時日。資料處理已過時。 
- PendingValidation.
資料交叉分析區正在等待驗證，然後再進行處理。 
- 重試驗證。
Data Factory 會重新驗證交叉分析區。 
- 驗證失敗。
交叉區驗證失敗。
針對每個區塊，您可以使用 Cmdlet 查看產生該區Get-AzDataFactoryRun詳細資訊。

## 例子

### 範例 1：取得資料集的資料區
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

此命令會針對名為 WikiADF 的資料工廠中名為 WikiAggregatedData 的資料集，獲得所有資料區。
該命令在 StartDateTime 參數指定的時間之後，就會產生區塊。
下列範例程式碼會每小時在 JSON 檔案的 JavaScript 物件標記法 (此) 可用性。
可用性：{ period： "Hour"， periodMultiplier： 1 } 部分結果已就緒，其他為 PendingExecution。
Ready slices have have run.
擱置的區隔區會以每個小時結尾的間隔等待執行，Set-AzDataFactoryPipelineActivePeriod Cmdlet 指定的時間間隔。
在此範例中，管線和區段的開始與結束期間都有 24 小時 (24 小時) 。

### 範例 2

在 Azure Data Factory 中為資料集獲取資料區。  (自動) 

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## 參數

### -DataFactory
指定 **PSDataFactory** 物件。
此 Cmdlet 會獲得屬於此參數指定之資料工廠的區塊。

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
此 Cmdlet 會獲得屬於此參數指定之資料工廠的區塊。

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
指定此 Cmdlet 會獲得資料區之資料集的名稱。

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
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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
將時間週期的結尾指定為 **DateTime** 物件。
此 Cmdlet 會在此參數指定之時間之前產生區塊。
有關 **DateTime** 物件的資訊，請鍵入 `Get-Help Get-Date` 。
*EndDateTime* 必須以 ISO8601 格式指定，如下列範例所示：2015-01-01Z 2015-01T00：00：00Z 2015-01-01T00 ：00：00.000Z (UTC) 2015-01-01T00：00：00：00-08：00 (太平洋標準時間) 預設時區設計工具為 UTC。

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
指定 Azure 資源組的名稱。
此 Cmdlet 會獲得屬於此參數指定之群組的區塊。

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
將時間週期的開始指定為 **DateTime** 物件。
此 Cmdlet 會在此參數指定的時間之後產生切區。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## 輸出

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## 筆記
* 關鍵字：azure、azurerm、arm、resource、management、manager、data、azure

## 相關連結

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


