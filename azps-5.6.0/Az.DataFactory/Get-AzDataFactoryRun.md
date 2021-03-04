---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: 2dbab7978716d6bb960c1804abf9e86246571e29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907754"
---
# Get-AzDataFactoryRun

## 簡介
在 Azure Data Factory 中為資料集的資料區執行。

## 語法

### ByFactoryName (預設) 
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzDataFactoryRun** Cmdlet 會針對 Azure Data Factory 中資料集的資料區區執行。
資料工廠中的資料集是由時間軸的區塊所組成。
分割區的寬度取決於排程，無論是每小時或每天。
執行是一個處理區塊的單位。
在重試或因失敗而重新執行區塊時，可能針對某一個區塊執行一或多個執行。
一個區塊會以其開始時間來識別。
若要取得分割區開始時間，請使用 Get-AzDataFactorySlice Cmdlet。
例如，若要執行下列區塊，請使用開始時間 2015-04-02T20：00：00。
ResourceGroupName ： ADF DataFactoryName ： SPDataFactory0924 DatasetName ： MarketingCampaignEffectivenessBlobDataset Start ： 5/2/2014 8：00：00 PM End ： 5/3/2014 8：00：00 PM 重試Count： 0 狀態 ： Ready LatencyStatus：

## 例子

### 範例 1：取得資料集
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

此命令會針對名為 DAWikiAggregatedData 的資料工廠中，從 2014 年 05 月 21 日 4：00 GMT 開始的資料工廠，執行所有作業。

## 參數

### -DataFactory
指定 **PSDataFactory** 物件。
此 Cmdlet 會針對屬於此參數指定之資料工廠的區塊執行。

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
此 Cmdlet 會針對屬於此參數指定之資料工廠的區塊執行。

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
指定資料集的名稱。
此 Cmdlet 會針對屬於此參數指定之資料集的區塊執行。

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

### -ResourceGroupName
指定 Azure 資源組的名稱。
此 Cmdlet 會針對屬於此參數指定之群組的區塊執行出廠設定。

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
此 Cmdlet 會針對符合此時段的資料區執行。
*StartDateTime* 必須以 ISO8601 格式指定，如下列範例所示：2015-01-01Z 2015-01T00：00：00Z 2015-01-01T00 ：00：00.000Z (UTC) 2015-01-01T00：00：00：00-08：00 (太平洋標準時間) 預設時區設計工具為 UTC。

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

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun

## 筆記
* 關鍵字：azure、azurerm、arm、resource、management、manager、data、azure

## 相關連結

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


