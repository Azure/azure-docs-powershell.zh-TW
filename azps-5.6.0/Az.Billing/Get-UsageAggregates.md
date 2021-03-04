---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 1947b060f6b1d2fcf7e4380d3a1ece808ea29785
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911193"
---
# Get-UsageAggregates

## 簡介
獲得報告的 Azure 訂閱使用方式詳細資料。

## 語法

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-UsageAggregates** Cmdlet 會根據下列屬性取得匯總的 Azure 訂閱使用量資料： 
- 報告使用量的開始與結束時間。
- 每日或每小時的匯總精確度。
- 相同資源之多個實例的實例層級詳細資料。
為取得一致的結果，所返回的資料是根據 Azure 資源報告使用方式詳細資料時所根據。
詳細資訊請參閱 Microsoft 開發人員網路庫中的 Azure Billing REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) 參考資料。

## 例子

### 範例 1：取回訂閱資料
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

此命令會針對 2015/5/2 和 2015/5/5 之間的訂閱，取回報告使用量資料。

## 參數

### -AggregationGranularity
指定資料的匯總精確度。
有效的值為：每日和每小時。
預設值為每日。

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
指定從上一個呼叫的回應內內容所取的延續權杖。
對於大型結果集，會使用連續權杖來分頁回應。
延續權杖可做為進度的書簽。
如果您未指定此參數，資料會從 *在 ReportedStartTime* 中指定的一天或一小時的開頭進行取用。
我們建議您追蹤回應頁面中的下一個連結，但請注意資料。

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

### -ReportedEndTime
指定在 Azure 計費系統中記錄資源使用量時的報告結束時間。
Azure 是一個分散式系統，橫跨全球的多個資料中心，因此實際使用資源的時間之間會延遲，即資源使用時間，以及到達計費系統時 ，即報告的資源使用量時間。
若要取得一段期間所報告之訂閱的所有使用事件，請根據報告的時間進行查詢。
即使您是按報告的時間進行查詢，Cmdlet 還是會根據資源使用時間匯總回應資料。
資源使用狀況資料是分析資料的實用樞紐。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -報告StartTime
指定在 Azure 計費系統中記錄資源使用量時的報告開始時間。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -顯示詳細
指出此 Cmdlet 是否會以使用方式資料來返回實例層級詳細資料。
預設值會$True。
如果$False，服務會匯總伺服器端的結果，因此會較少的匯總群組。
例如，如果您經營三個網站，根據預設，您就會收到三個供網站使用的專案。
不過，當值為 $False時，同一個 **subscriptionId、meterId、usageStartTime** 和  **usageEndTime** 的所有資料會轉換為單行專案。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commerce.UsageAggregates.models.UsageAggregationGetResponse

## 筆記

## 相關連結
